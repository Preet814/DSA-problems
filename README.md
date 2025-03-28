**Assignment: Create Custom IAM role, policy and attach it to IAM user. Also enable MFA for that user**

Creating IAM User with permission to only list the s3 buckets. Later on adding a role where the user can start and stop the EC2 instances and list all the EC2 instances on dashboard by switching to the specified role. Lastly enabling MFA to the user.

**1. Create IAM User:**

Step 1. Search IAM on search bar of Amazon console and click IAM.

Step 2. Select Users from left side bar and click on create user.

Step 3. Add User name, provide user access to AWS management console by clicking on it, select i want to create iam user and choose password method accordingly.

Step 4. Choose permission option accordingly(assign s3 list bucket policy to it), review and create a user.


Current User permission:

![alt text](image.png)

We can login to iam user thorugh password authentication and can see that user can only list S3 buckets. He cannot list or start and stop EC2 instances.

**2. Create IAM Role:**

Step 1. Select Role from side bar of IAM service page and click on create role.

Step 2. Choose trusted entity type (choose AWS account as per assignment).

Step 3. Add permission according to the role (in my case i added an inline policy to start and stop ec2 instances and list all the instances) and add name to the role and policy.


Inline policy attached to my role:

![alt text](image-1.png)

**3. Attach role and policy to user by assume role:**

Step 1. Copy ARN of role and move to user and edit the policy.

Step 2. Add this policy to user policy and save the changes:


![alt text](image-2.png)


Now to list or start and stop EC2 instances user can switch his role.

4. Add MFA to user

Step 1. Click on iam user and select the user.

Step 2. click on security credentials and select assign MFA.

Step 3. Add MFA device name and scan the QR code to add the MFA.

