## Initiate Deployment

Access the **Initiate Deployment Task** page,

![Alt text](https://github.com/jdcloudcom/cn/blob/edit/image/CodeDeploy/Ch/Oper-9%EF%BC%88Ch%EF%BC%89.png)

There are options as below:

- Deployment description: Optional, it is the description information for this deployment
- Deployment source: Multiple deployment sources are supported, including "URL Upload", "CodeBuild" and "Object Storage Service". When the "URL Upload" is selected, the URL address and MD5 shall be filled; when the "CodeBuild" is selected, the application name of CodeBuild and SN of successful construction shall be selected; and when the "Object Storage Service" is selected, the Object Storage Service Bucket and file shall be selected.
- File type: Select the package type
- Deployment operation command: You are allowed to pack the operating commands into a code package or fill them in the page.

   - Enter deployment operation command: A convenient and easy-to-use form is provided to meet basic demands of most users, please select the "Form" function and fill in specific operation commands. At the same time, to cope with complex operation commands, yaml files can be filled. For writing specifications, please refer to "Operation Guide File-Jdcloud-codedeploy"
  
      - Deployment content: A maximum of 5 pairs of sources and destinations are supported. For details, please refer to “Operation Guide-source and destination in Jdcloud-codedeploy File”
     
      - Stop script path: Refer to the command or script used for stopping a program in case of rollback and deployment update
     
      - Start script path: Refer to the command and script used for starting a program in case of rollback and deployment update
     
      - Check script path: Refer to the command or script used for checking deployment results upon completion of the deployment The return value 0 means successful, while the return value other than 0 means failed
      
      - Executing script account: Refer to the account used when executing hooks in the deployment operation. This account shall be the existing account of the system. Otherwise, the account cannot be deployed
     
      - Script time-out period: The time-out period for script execution is in second
     
   - Use Jdcloud-codedeploy.yml of code root directory: The appSpec file containing the deployment operation command, in the name of appSpec.yml, is added in the code root directory. For writing specifications, please refer to "Operation Guide-AppSpec File"

![Alt text](https://github.com/jdcloudcom/cn/blob/edit/image/CodeDeploy/Ch/Oper-10%EF%BC%88Ch%EF%BC%89.png)


After filling in the deployment task information, please click **Initiate Deployment** to trigger deployment.
