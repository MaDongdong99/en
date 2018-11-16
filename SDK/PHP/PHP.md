
# Introduction #
  Welcome to the JD Cloud Developer Php Tool Kit (Php SDK). With the JD Cloud Php SDK, you can access the services provided by JD Cloud without complex programming. 

  To facilitate the understanding of some concepts and parameters in the SDK, it's recommended to first review [JD Cloud OpenAPI Use Getting Started](http://www.jdcloud.com/help/detail/355/isCatalog/0) before using the SDK. To understand the specific parameters and meanings of each API, refer to the program comments or the API documentation for specific product lines under the OpenAPI & SDK.



# Environment Preparation #
 1. The JD Cloud Php SDK is suitable for Php 5.5 and above.

 2. Before calling JD Cloud open API, it's necessary to apply for accesskey and secretKey Key Pair (AK/SK) in advance in Account Management of JD Cloud User Center[AccessKey Management Page](https://uc.jdcloud.com/accesskey/index). AK/ SK information shall be kept properly and if lost, it is likely to allow illegal users to use this information to operate your resources on the cloud, resulting in data or property losses.



# SDK Usage Method #
It is recommended to install the JD Cloud Php SDK with Composer: 

First add in composer.json

	"require" : {
		"php" : ">=5.5",
		"jdcloud-api" : ">=1.0",
	}
    

Then use the Composer installation

    php composer.phar install

or

    composer install 


You can also download the SDK source code yourself. The source code address is [PhpSDK](https://github.com/jdcloud-api/jdcloud-sdk-php).

 

With any problems in the use of SDK, welcome to communicate at the[SDK Use Problem Feedback page](https://github.com/jdcloud-api/jdcloud-sdk-php/issues) for the Github project.


Note: JD Cloud does not provide other downloading ways, please be sure to use the above-mentioned official download method.

 

## Call Example ##
The following is an example of a call to creat an individual VM Instance in details

	use Jdcloud\Credentials\Credentials;
    use Jdcloud\Result;
    use Jdcloud\Vm\VmClient;
    public function testCreateInstances()
    {
        $vm = new VmClient([
            'credentials'  => new Credentials('35DDDCFFB86CF2D494F0F3B6B0B3EF68', '93C107EF1F3A0C46C6329C04F561A29E'),
            'version' => 'latest',
            'scheme' => 'https',
            'http'    => [
                'verify' => 'C:/ca-bundle.crt'
            ]
        ]);
        
        
        try{
            $res = $vm->createInstances([
                'regionId'  => 'cn-north-1',
                'instanceSpec' => [
                    'az' => 'cn-north-1a',
                    'imageId' => '8e187a0a-ea7c-4ad1-ba32-f21e52fb8926',
                    'instanceType' =>  'g.n2.medium',
                    'name' => 'phpcreate',
                    'primaryNetworkInterface' => [
                        'networkInterface' => [
                            'subnetId' => 'subnet-ll47yy373i'
                         ]
                    ],
                    'systemDisk' => [
                        'diskCategory' => 'local'
                    ]
                ]
            ]);
            print_r($res);
            print("Request Id: ". $res['requestId']. "\n");
            print_r($res['result']);
        }catch (\Jdcloud\Exception\JdcloudException $e) {
            print("Detail Message: " . $e->getMessage(). "\n");
            print("Request Id: ". $e->getJdcloudRequestId(). "\n");
            print("Error Type: ". $e->getJdcloudErrorType(). "\n");
            print("Error Code: " . $e->getJdcloudErrorCode(). "\n");
            print("Error Detail Status: ". $e->getJdcloudErrorStatus(). "\n");
            print("Error Detail Message: ". $e->getJdcloudErrorMessage(). "\n");
        }
    }

If you need to set up an additional header, for example, call an interface that opens the MFA operation protection, you need to pass x-jdcloud-security-token, as follows:

        $res = $vm->deleteInstances([
            'regionId'  => 'cn-north-1',
            'instanceId'  => 'xxx',
            'extraHeaders' => [
                'x-jdcloud-security-token' => 'xxxx'
            ]
        ]);