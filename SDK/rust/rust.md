# JD Cloud Rust Signature Library
## Basic Description
JD Cloud Rust signature tools provide the function of requesting signatures when Rust language accesses JD Cloud OpenAPI.

Before you calling the open API of JD Cloud, please apply for the key pair of accesskey and secretKey (AK/SK for short) in the [AccessKey Management Page](https://uc.jdcloud.com/accesskey/index) under the User Center Account Management of JD Cloud. Please properly keep your AK/SK information. If lost, your cloud resources may be operated by illegal users with this information, and you may suffer data and property loss.


## Usage: Ordinary Method

### Cargo.toml

Add the following field to your Cargo.toml

```
[dependencies]
jdcloud_signer = "0.1"
```

### Example of use

For detailed examples, please refer to [client.rs](https://github.com/jdcloud-api/jdcloud-sdk-rust-signer/blob/master/examples/client.rs)

```sh
$ export JDCLOUD_AK="..."
$ export JDCLOUD_SK="..."
$ cargo run --example client
    Finished dev [unoptimized + debuginfo] target(s) in 0.37s
     Running `target/debug/examples/client`
status: 200 OK
content-type: "application/json; charset=utf-8"
transfer-encoding: "chunked"
connection: "close"
date: "Mon, 22 Jul 2019 09:18:34 GMT"
x-jdcloud-request-id: "bkrovrdrv8ewru46782326noreauvdsf"
x-jdcloud-operationid: "describeInstances"
x-jdcloud-upstream-latency: "310"
x-jdcloud-proxy-latency: "30"
via: "jd-gateway/1.0.1"
requestId: "bkrovrdrv8ewru46782326noreauvdsf"
```

## Usage: Signature-only Mode

If you don't like `reqwest` and intend to use your own http library, then you can choose the signature-only mode.

We will add the following Header fields when signing

* `User-Agent`: If not designated, it shall be set as "JdcloudSdkRust/0.1.0". If designated, it shall not be modified.
* `X-Jdcloud-Date`: Current Time.
* `X-Jdcloud-Nonce`: Random Number.
* `Authorization`: Signature.

### Cargo.toml

Add the following field to your Cargo.toml

```
[dependencies]
jdcloud_signer = { version = "0.1", default-features = false }
```

### Example of use

```rust
use jdcloud_signer::{Credential, Signer};
use http::Request;

fn main() {
    let ak = "...";
    let sk = "...";
    let credential = Credential::new(ak, sk);
    let signer = Signer::new(credential, "vm".to_string(), "cn-north-1".to_string());

    let mut req = Request::builder();
    let mut req = req.method("GET")
        .uri("https://vm.jdcloud-api.com/v1/regions/cn-north-1/instances")
        .body("".to_string()).unwrap();
    signer.sign_request(&mut req).unwrap();
    println!("{}", req);
}
```

For more calling examples, please refer to [SDK Use Demo](https://github.com/jdcloud-api/jdcloud-sdk-rust-signer/tree/master/examples)





**Note:**

- JD Cloud does not provide other download methods. Please be sure to adopt the above official download method.

- The latest version number provided by JD Cloud product shall be used as the version number. For example: The latest version number used by VM in the example can be searched in API [Update History](../../API/Virtual-Machines/ChangeLog.md).

- Each cloud product has its own Client. When API of this product is called, the Client of such product will be used. For example: When VmClient of Virtual Machines is used, only APIs of Virtual Machines (Vm) can be called; when AgClient of Availability Group is used, only APIs of Availability Group (Ag) can be called.


 
