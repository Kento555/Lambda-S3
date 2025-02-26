# Lambda-S3
What is the purpose of the execution role on the Lambda function?  
The execution role is an IAM role that grants Lambda permissions to interact with AWS services. Specifically, in this case:  

It allows Lambda to read the event data from S3.  
It may grant access to write logs to Amazon CloudWatch Logs for debugging and monitoring.  
It ensures the function operates within the least privilege principle.  

![image](https://github.com/user-attachments/assets/b367774b-26e3-4af7-b492-0c6598275468)  

![image](https://github.com/user-attachments/assets/acceace5-426d-4b68-898a-113e6c67ef0a)


