### FAQ
#### 1. How to configure log collection, do you need to install plug-ins?

To collect the cloud product logs, you just need to select the cloud product type and log type as well as the instance to be collected on the Log Source Settings page for configuration. No plug-in needs to be manually installed.

To collect the business application logs, you just need to fill in the collection path and the VM Instances to be collected. The collection agent will be automatically installed in the Virtual Machine selected.

#### 2. After deleting the resource, can you still view the log data of the resource?

During the validity period of log data, even if the resource is deleted, the log data collected in the past can still be viewed. After the deletion, the log data will not be collected again.

#### 3. If the resource is overdue, will the log data continue to be collected?

According to the characteristics of different cloud resources, as long as the resource is in your name and is running normally, the log will continue to be collected.

#### 4. After deleting the log subject, can the log data still be viewed?

The log data under the log subject cannot be recovered after deletion, please operate with care.

#### 5. Where is the collected cloud product log data stored? Can it be exported?

The collected cloud product logs will be uniformly stored in the JD Cloud platform. The export function of log data is currently not supported. To export log data, you can set a dump task to dump the log data to the OSS, and then download the log data to be downloaded in the OSS.

#### 6. How long can the log data be saved?

Currently, the log data can be saved for 7 days, 15 days, and 30 days. It cannot be viewed after expiration. The user can modify the save time in the Log Subject.

#### 7. How do I disable the Log Service?  
If you no longer need to use the Log Service, delete the log subject and log collection to clear the log data.

#### 8. Why can't I find the log data?  
The log data may not be found for the following reasons:  
- No log data is generated;  
- The query conditions are incorrect. Please change the keyword or statement of the query and query according to the provided query rules;  
- Data collection latency. Log data collection may have the latency of about 1 minute, you can query after one minute;  
If you still can't query the data, please contact us by ticket.

