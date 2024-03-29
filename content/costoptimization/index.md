# Cost Optimization Workshop

# AWS hosted-event

To complete the workshop your facilitator will provide you with a participant hash code, this is the key to unlock your temporary AWS account which has been pre-populated with all the infrastructure and access you will need to complete this workshop.

## Login to the AWS Workshop Portal

AWS Workshop Studio has created an AWS account for you and deployed the workshop resources in it. Follow the following steps to access the AWS console. You will need the Participant Hash provided upon entry, and your email address to track your unique session.

1. Click [AWS Workshop Portal](https://catalog.us-east-1.prod.workshops.aws/).

2. Click **Get started**.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-00.png?classes=lab_picture_small)

3. Click **Email One-Time Password (OTP)** button.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-01.png?classes=lab_picture_small)

4. Enter your own email account and click the **Send passcode** button.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-02.png?classes=lab_picture_small)

5. In the email inbox, check the subject Your one-time passcode email and copy the passcode. Paste the copied passcode as shown below, then press the Sign in button.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-03.png?classes=lab_picture_small)

6. Enter a 12-digit access code, please ask your workshop instructor.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/hashcode.png?classes=lab_picture_small)

7. On the next screen, check **I agree with the Terms and Conditions** to accept terms and conditions and press the **Join event** to receive a login link to log in to the console.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-04.png?classes=lab_picture_small)

8. Click on the **Get started** button to access the workshop instructions.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-05.png?classes=lab_picture_small)

9. Click **Open AWS console** to access to the AWS Management Console.

![Images/AWSCUR1.png](/static/costoptimization/getting-started/setup-event-engine-06.png?classes=lab_picture_small)

> [!NOTE]
> **Congratulations!** You have successfully logged into the AWS Console.

## Continuous Cost Optimization Workshop#1

In this workshop you will learn about efficiency, implementing mechanisms that empower application owners to have clear, actionable tasks for cost and sustainability optimizations, minimizing energy consumptions and carbon footprint, building upon real-world use cases.

 * [EBS Volume Scenario 1 - migration from GP2 to GP3](https://catalog.us-east-1.prod.workshops.aws/workshops/42c0fe7e-8d1c-4d5f-8b48-c818c7952242/en-US/ebs/scenario1-ebs-volumes-migration-from-gp2-to-gp3)
 * [EC2 Scenario 4 - Right Sizing - Compute Optimizer - SSM Automation](https://catalog.us-east-1.prod.workshops.aws/workshops/42c0fe7e-8d1c-4d5f-8b48-c818c7952242/en-US/ec2/scenario4-ec2-rightsizing)
 * [RDS Scenario 5 - RDS Move to Graviton](https://catalog.us-east-1.prod.workshops.aws/workshops/42c0fe7e-8d1c-4d5f-8b48-c818c7952242/en-US/rds/6-rds-move-to-graviton)
 * [S3 Scenario 7 - Multipart Uploads](https://catalog.us-east-1.prod.workshops.aws/workshops/42c0fe7e-8d1c-4d5f-8b48-c818c7952242/en-US/s3/s3-multi-part-uploads)
 * [Scenario 8 - S3 Intelligent tiering](https://catalog.us-east-1.prod.workshops.aws/workshops/42c0fe7e-8d1c-4d5f-8b48-c818c7952242/en-US/s3/intelligent-tiering)


 > [!NOTE]
> **Congratulations!** You have compelted actionable tasks for cost optimizations.

## Continuous Cost Optimization Workshop#2

The [Cloud Intelligence Dashboards](https://d1s0yx3p3y3rah.cloudfront.net/anonymous-embed?dashboard=cudos) is an open-source framework, lovingly cultivated and maintained by a group of customer-obsessed AWSers, that provides customers actionable insights and optimization opportunities at scale of organization. Supported by the Well-Architected framework, the dashboards can be deployed by any customer using a CloudFormation template or a command-line tool in their environment. These dashboards help customers drive financial accountability, optimize cost, track usage goals, implement best-practices for governance, and achieve operational excellence across all Well Architected pillars.


 > [!IMPORTANT]
> **ℹ️ New AWS Workshop Access Code requires and your instructor will share it!** 
> 
> **Only complete `Lab 1 - Gaining Visibility in a customers account`** 

*  [Build the Cost Intelligence Dashboard, CUDOS and KPI dashboards](https://catalog.workshops.aws/co-for-partners/en-US/2-module-1/lab-1) 


![Images/cid1.png](/static/costoptimization/getting-started/cid1.png?classes=lab_picture_small)

## Challenges

### Scenarios
* Your workload is currently running an on-premises datacenter. 
* You plan to do PoC for existing web application on AWS environment in **Singapore region**.
* All virtual machines must run 24/7 except the Dev/Test instance, as developers only need it from 9 am to 6 pm on weekdays.
* The application produces 1 TB of new data every month and requires retention of data for a maximum of 30 days. 
* All data has to be encrypted.
* [AWS Pricing Calculator](https://calculator.aws/#/)
* The followings are list of inventories of the web application in the on-premise data center.

Create a simple presentation outlining your choices of AWS Cloud Financial Management Services and explain your rationale behind the selection.

**On-Premises Environment**
| Name  | OS | Application | Disk | On-Prem(vCPU) | On-Prem Memory(GiB) | Avg CPU Utilization(%) | Max CPU Utilization(%)| Avg Mem(GiB) | Max Mem(GiB) | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Application | Linux  | Flask  | 40GB  | 8  | 32  | 50  | 70  | 8  | 24  |
| WebServer01  | Linux | Php & Apache  | 40GB  | 16  | 64  | 10  | 25  | 4  | 20  |
| Redis  | Linux  | Redis v.4 | 40GB  | 4  | 16  | 10  | 20  | 7  | 11  |
| Posgre-Master  | Linux  | PosgreSQL v.13  | 40GB | 4  | 16  | 50  | 70  | 3  | 5  |
| Dev/Test | Linux  | Flask  | 40GB  | 2  | 8  | 40  | 60  | 4  | 6  |
| Blob storage | N/A  | N/A  | 100TB 


**A Sample To-Be Architecture**
![Images/sample-arc.png](/static/costoptimization/getting-started/sample-architecture.png?classes=lab_picture_small)

### Challenge#1

Choose Amazon EC2 instance types based on existing on-premise CPU and memory specifications, and calculate the costs using [AWS Pricing Calculator](https://calculator.aws/#/). **Question: What are your estimated monthly costs for each AWS resource?**


### Challenge#2 

Based on CPU and memory utilization, identify the most cost-efficient instance types. **Questions: What are your estimated monthly costs for the optimized AWS resources?** 

* Earning points for challenge#2 vary depending on **Cost Savings opportunity(%)**

    | Monthly Cost Savings opportunity(%)  | Points |
    | ------------- | ------------- |
    | ~10%  | 1  | 
    | ~20%  | 2  | 
    | ~30%  | 3  | 
    | ~40%  | 4  | 
    | ~50%  | 5  | 

> [!IMPORTANT]
> **ℹ️ Please make sure the CPU utilization will not reach 100%.** 

### Challenge#3 

Up to this point, you have rightsized AWS resources manually. What if you have more than 100 instances that require rightsizing? In such cases, you'll require a data-driven strategy that relies on historical utilization data and automation to consistently pinpoint cost-saving opportunities.

AWS offers a range of [AWS Cloud Financial Management Services](https://aws.amazon.com/aws-cost-management/) tailored to specific use cases, as illustrated below:

![Images/AWSCFMs.png](/static/costoptimization/getting-started/AWSCFMs.png?classes=lab_picture_small)

**Quesion: Which AWS Cloud Financial Management Services will you utilize, and what are your reasons for selecting them?**

# Survey

ℹ️ Please let us know what you thought of this session and how we can improve the experience for you in the future by completing [**this survey**](https://www.pulse.aws/survey/QSHA7GUN) at the end of the lab.
