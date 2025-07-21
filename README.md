# Cloud-Honeypots-AWS-
Created a cloud based honeypot that helps to track and learn from attacker's behavior.
# Cloud Honeypot System (Honeytoken Traps)

## Project Description

This project implements a Cloud Honeypot System designed to detect unauthorized access attempts in an AWS environment. It utilizes decoy AWS resources—such as S3 buckets and EC2 instances—and strategically placed honeytokens to identify and analyze malicious behavior. 

The system is capable of monitoring activity using AWS CloudTrail and GuardDuty, and includes optional automation through AWS Lambda for incident response, such as disabling compromised IAM keys or tagging affected EC2 instances.

---

## Tools and Services Used

| Tool / Service       | Purpose                                                              |
|----------------------|----------------------------------------------------------------------|
| AWS S3               | Hosts fake, publicly visible files to simulate exposed sensitive data |
| AWS EC2              | Deploys unused or idle instances as decoy infrastructure             |
| Canarytokens.org     | Generates fake credentials and tokens that send alerts on use        |
| AWS CloudTrail       | Logs all API activity and access events within AWS                   |
| AWS GuardDuty        | Detects suspicious activity and provides actionable security findings |
| AWS Lambda (Optional)| Automates response actions such as tagging resources or disabling IAM keys |
| AWS SNS (Optional)   | Sends notifications for triggered alerts                             |
| AWS EventBridge      | Triggers Lambda functions based on security events or logs           |

---

## Features

- Deployment of fake AWS S3 buckets and EC2 instances to serve as honeypots
- Use of Canarytokens to detect unauthorized access to credentials or files
- Monitoring and detection of security events using CloudTrail and GuardDuty
- Optional automation using Lambda to respond to events by disabling access keys or isolating resources
- Configurable alerting via AWS SNS or email

---

## Workflow Overview

1. Set up decoy AWS resources (e.g., S3 buckets and EC2 instances)
2. Generate and place honeytokens using Canarytokens
3. Enable CloudTrail and GuardDuty for monitoring and detection
4. When activity is detected:
   - Canarytokens sends alert notifications
   - GuardDuty generates security findings
5. (Optional) Lambda function is triggered to automate the response:
   - Disable exposed IAM keys
   - Tag EC2 instances as compromised

---

## Deployement
<img width="1917" height="623" alt="image" src="https://github.com/user-attachments/assets/d43a8fff-a060-4874-83e2-1b5f6361ef8a" />

![WhatsApp Image 2025-07-21 at 11 57 19_dd707172](https://github.com/user-attachments/assets/88aedac3-685e-432c-8b40-c292e0e9ce22)
![WhatsApp Image 2025-07-21 at 11 57 20_e7de1f33](https://github.com/user-attachments/assets/be0a2303-4784-4e92-bfe6-1518bbdb642c)

![WhatsApp Image 2025-07-21 at 11 57 20_4f166e1f](https://github.com/user-attachments/assets/f8dae80e-1c7f-49d4-9997-e9f218fa59d6)

![WhatsApp Image 2025-07-21 at 11 57 20_580bd79f](https://github.com/user-attachments/assets/9d1dcea3-2f34-4960-85a7-ac09dc711f92)

![WhatsApp Image 2025-07-21 at 11 57 37_126644e3](https://github.com/user-attachments/assets/2c75e3e0-c183-4cc7-84c6-7778b59c8399)

![WhatsApp Image 2025-07-21 at 11 57 37_3330d381](https://github.com/user-attachments/assets/f6017c0a-e254-49c3-877e-6261e2a1de45)




## Educational Value

This project is intended for educational and demonstration purposes. It provides insight into modern cloud security monitoring and response techniques using AWS-native tools and open-source resources.

Suitable for:
- Students learning cloud security or cyber deception
- Security enthusiasts and researchers
- Academic and college-level cybersecurity projects

---

## Potential Improvements

- Integration with SIEM platforms for log aggregation and deeper analysis
- Deployment automation using CloudFormation or Terraform
- Real-time alert dashboard for incident tracking and visualization
- Automated network isolation based on detected behavior

---


---


