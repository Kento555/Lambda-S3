# Lambda-S3
1. What is the purpose of the execution role on the Lambda function?  
   The execution role is an IAM role that grants Lambda permissions to interact with AWS services. Specifically, in this case:  

   It allows Lambda to read the event data from S3.  
   It grant access to write logs to Amazon CloudWatch Logs for debugging and monitoring.  
   It ensures the function operates within the least privilege principle.  

2. What is the purpose of the resource-based policy on the Lambda function?
   A resource-based policy defines who (which AWS services, accounts, or users) can invoke the Lambda function.

   In this case, when S3 event notifications is set up, AWS automatically adds a resource-based policy to allow the S3 bucket to invoke the Lambda function.
   This ensures that only the configured S3 bucket can trigger the function, preventing unauthorized access.

3. If the function needs to upload a file into an S3 bucket, what updates are required?
   Execution Role Update (IAM Policy for Lambda)
   To allow the Lambda function to upload files to S3, the execution role needs the following permissions:

   s3:PutObject – Allows Lambda to upload objects to the bucket.
   s3:ListBucket (optional) – Allows checking if the file exists before uploading.

Execution role:  
![image](https://github.com/user-attachments/assets/b367774b-26e3-4af7-b492-0c6598275468)  

![image](https://github.com/user-attachments/assets/acceace5-426d-4b68-898a-113e6c67ef0a)

![image](https://github.com/user-attachments/assets/4603e04e-397d-498e-b0e7-51bba8e59eae)

Resource based policy:  
![image](https://github.com/user-attachments/assets/48797b43-aea8-41bd-a73d-2a25869f5c88)  

![image](https://github.com/user-attachments/assets/a4c35593-8f2b-4db0-91ff-801383b6d48b) 





