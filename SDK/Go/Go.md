
# JD Cloud Golang SDK

[![GoDoc](https://godoc.org/github.com/jdcloud-api/jdcloud-sdk-go?status.svg)](https://godoc.org/github.com/jdcloud-api/jdcloud-sdk-go)

Welcome to the JD Cloud Developer Golang Kit (Go SDK). With JD Cloud Go SDK, you can access the services provided by JD Cloud without complex programming.
To facilitate the understanding of some concepts and parameters in the SDK, it's recommended to review the Getting Started to OpenAPI before using the SDK.

## Environment Preparation
1. The JD Cloud Go SDK is suitable for Go 1.6 and above.
2. Before calling JD Cloud open API, it's necessary to apply for accesskey and secretKey Key Pair (AK/SK) in advance in Account Mmanagement of JD Cloud User Center[AccessKey Management Page](https://uc.jdcloud.com/accesskey/index). AK/ SK information shall be kept properly and if lost, it is likely to allow illegal users to use this information to operate your resources on the cloud, resulting in data or property losses.

## Download & Installation
1. Download address of JD Cloud Go SDK:[Go SDK](https://github.com/jdcloud-api/jdcloud-sdk-go).
2. You can also obtain the installation package using the following command, which is downloaded to the first path src directory in the GOPATH environment variable.

    `go get github.com/jdcloud-api/jdcloud-sdk-go/core github.com/satori/go.uuid`

## Call SDK
### The calling of the service side SDK is mainly divided into four steps:
1. Set accessKey and secretKey
2. Create Business Client
3. Set Request Parameters
4. Response to implementation requests

### The general code is as follows:
``` go
package main

import (
	"fmt"
  	. "github.com/jdcloud-api/jdcloud-sdk-go/services/vm/apis"
	. "github.com/jdcloud-api/jdcloud-sdk-go/services/vm/client"
	. "github.com/jdcloud-api/jdcloud-sdk-go/core"
)

func main() {
	accessKey := "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
	secretKey := "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
	credentials := NewCredentials(accessKey, secretKey)
	client := NewVmClient(credentials)

	req := NewDescribeInstancesRequest("cn-north-1")
	resp, err := client.DescribeInstances(req)
	if err != nil {
		return
	}
	fmt.Println(resp.Result.Instances)
	fmt.Println(resp.Result.TotalCount)
	fmt.Println(len(resp.Result.Instances))
}
```
If you need to set up an additional header, for example, call an interface that opens the MFA operation protection, you need to pass x-jdcloud-security-token, as follows:

```go
req := NewDeleteInstanceRequest("cn-north-1", "i-xxxxx")
req.AddHeader("x-jdcloud-security-token", "xxx")
resp, err := client.DeleteInstance(req)
```

Refer to the test cases in demo and access each business line interface of JD Cloud.
