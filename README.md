# Landing-zone-cloudformation
This YAML script will help to remove Default VPC and Update Password Policy

### How to use

```
File-1. DeleteVPC-IAM-Policy-update.
```

Usage: This file you only have to run in cloudformation with Admin access. It will remove default vpc from all region and update IAM Password Policy given by CIS standard. 

Note: Delete stack after running successfully. It will remove all the resources created for this requirement. 

```
File-2. Master-Template.
```
Usage: Run file in cloud-formation and enter required parameters. It will create following services.

   --> Cloudtrail with KMS Encryption Bucket.
   
   --> Cloudwatch log of cloudtrail.
   
   --> Cloudwatch alarm from cloudtrail logs. (16 Alarms-Recommended by CIS).
   
   --> Enable Guardduty.
   
   --> Enable Config service with SSE s3 bucket delivery.
   
   --> Create SNS for each service for notification.
   
   --> Create Cloudformation Admin and Execution role for Stackset.
   
### Stackset can gives you facility to run any template to cross account or cross region. 

```
File-3. EnableConfig-Allregion
```

Usage: Run this file into cloudformation stackset for creating config service in all the region.


   
   
