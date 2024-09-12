# EC2-Cpu-Alerting-through-SNS


**Overview :**  
In this project, We create one ec2 instance and configure cpu alarm for that instance in cloudwatch. If CPU Reaches above certain threshold level, you will get a notification through sns.

**Cloudwatch:**
It is a gatekeeper for aws account which will help you in monitoring deleting reporting and logging.

**Features of cloudwatch :** 
1.monitoring
2.alarms
3.log insights(save activity if any service try to access your service like ec2,s3,..)
4.cost optimization
5.scaling
6.log groups(activity of project perform in aws account)

**Step 1:
Create EC2 Instance**

Go to aws ec2 -> click launch ec2->select ami as amazon linux2 ami ->select instance type as t2.micro->create new keypair to connect ec2->leave remaining by default and click launch.

**Step 2 : 
Create alarm in cloudwatch**

Go to cloudwatch->click create alarm->slect metric->click ec2 instance->click per instance metrics->select cpu utilization of your created instance->choose thresold level->slect sns->create new topic->enter your mail which you want to receive notification.

Now alarm is in insufficient state. To activate it, go to your mail and confirm approval. Now alarm is changed to ok state.

**Step 3: 
To check working process** 

Use one  python script on your ec2 instance to increase your cpu percentage for testing. You will receive the mail.

You can get pythone code from chatgpt also...!
