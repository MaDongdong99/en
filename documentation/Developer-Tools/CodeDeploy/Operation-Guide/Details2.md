## Deployment Details

The deployment progress can be viewed in the "Deployment Details". The "Cancel" function is supported in the deployment process. When the deployment is ended, the "Rollback" function is supported for the latest(not frist) deployment task succeeded.

![Alt text](https://github.com/jdcloudcom/cn/blob/edit/image/CodeDeploy/Ch/Oper-12%EF%BC%88Ch%EF%BC%89.png)


**Cancel**

The deploying task will be canceled. Please note that the rollback is not supported for the deployed task, i.e. the program package versions of different instances are inconsistent in the same deployment group.

**Rollback**

For a deployment group, only the manual rollback operation to the latest deployment task succeeded is supported. For details, please refer to "Operation Guide-Deployment Workflow".

**View Configuration**

Click **View Configuration** to view the detailed configuration information of this deployment task.

**View Log**

Click **View Log** in the specified instance to view the deployment log.

Show logs as per the workflow structure. For details, please refer to "Operation Guide-Deployment Workflow"
