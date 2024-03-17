  Node.js Application Deployment on AWS Elastic Beanstalk
======================================================

Step 1: Create an Elastic Beanstalk Application
-----------------------------------------------

1. Log into the AWS Management Console and navigate to the Elastic Beanstalk dashboard.
2. Click "Create New Application" and enter a unique name for your application.
3. Select "Node.js" as the platform and click "Create".

Step 2: Configure Your Environment
---------------------------------

1. After creating your application, select it from the list and click "Environment".
2. Click "Create Environment" and choose "Web Server Environment".
3. Enter a name for your environment and select the appropriate region.
4. Choose "Node.js" as the preconfigured platform version.
5. upload node.js zip file ( we can get this file from aws documentation )
6. Attach your environment to a Default VPC, make sure that it is attached to IGW
8. Click "Create Environment" and wait for the creation process to finish.
9. **Optional**: Customize settings such as network configuration, database setup, tagging, etc. based on your requirements.
10. **Optional**: Adjust instance traffic and scaling options under the "Capacity" tab.
11. **Optional**: Fine-tune update, monitoring, and logging preferences under the "Configuration" tab.

Step 3: Configure Service Access
-------------------------------

1. Navigate to the IAM Dashboard and click "Roles".
2. Click "Create Role" and select "EC2" as the trusted entity type.
3. Search for and attach the `aws-elastic beanstalk-web tier` policy.
4. Save your changes.


Step 5: Review and submit  to get a domain name 
----------------------------------

1. Review all the configuration and click submit 
2. we will get the domain name here, copy and paste it into any browser 
3.  Once finished, you should see your Node.js application running.

To update your Node.js application, modify the `index.html` content inside the updated .zip file.

Congratulations! You have successfully deployed your Node.js application on AWS Elastic Beanstalk.
