# Restrictions

The use restrictions of JD Cloud Storage Gateway are shown as below:

### Deploy and configure relevant restrictions

- Only support Virtual Machines deployment other than provide image deployment for local IDC temporarily;
- One Storage Gateway only supports to enable one sharing file system;
- One sharing file system only supports to connect one Bucket as its backend Cloud Storage;
- Ensure to enable Virtual Machines and Object Storage Service before using Storage Gateway.

### Relevant restrictions of NFS protocol

- The Storage Gateway does not support random writing, file lock, soft link and hard link now.
- Clients accessing NFS need to be used by attaching by Root user other than other users temporarily.

### Relevant Restrictions on FTP

- mput, mget and append commands are not supported

### Related References
- [Product Overview](../Introduction/Product-Overview.md)
- [Core Concepts](../Introduction/Core-Concepts.md)
- [Deploy Storage Gateway](../Operation-Guide/Installation-Configuration.md)
- [Use NFS to access](../Operation-Guide/Use-Storage-Gateway.md)
- [Use FTP to access](../Operation-Guide/Use-FTP.md)
