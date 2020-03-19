# Context

This json file give the ability to provision ec2 instances with:

   AWS Auto Scaling group and the following configuration using Cloud Formation: 

   * It has Minimum 2 Centos 7 ec2 instances and Maximum 10 Centos 7 ec2 instances.
   * If CPU utilization is above 20% for 5 minutes, it adds one Centos 7 instance and wait for another 10  minutes.
   * If CPU utilization is less than 7% for 5 minutes, it removes one Centos 7 instance and wait for another 10 minutes.

# This template has the following: 

* A Launch Configuration that defines the configuration for Amazon EC2 instances that are launched by Auto Scaling (eg Instance Type,  AMI)
* An Auto Scaling group that defines how many instances to launch
* CloudWatch Alarms that define metrics to monitor to determine when to scale
* Auto Scaling policies that define how many instances to add/remove when the CloudWatch Alarms are triggered


# Prerequsites

 * must have an aws account and set all necessary permissions needed e.g (Iam role, etc)
 * Then go to cloud formation create a stack and upload this template for it to provision the services for this project.


