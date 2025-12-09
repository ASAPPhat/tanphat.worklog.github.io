---
title: "Week 6 Worklog"
date: "2025-10-22"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

**Week Duration: October 13 - 19, 2025**

### Week 6 Objectives:

- Master RDS database deployment and management
- Learn application deployment with Auto Scaling
- Understand monitoring with CloudWatch
- Practice DynamoDB for NoSQL workloads
- Learn networking and content delivery

### Tasks to be carried out this week:

| Day       | Task                                                                                                                                                                                                                                                                 | Start Date | Completion Date | Reference Material                                                                 |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ---------------------------------------------------------------------------------- |
| Monday    | - Create VPC, EC2 security group, RDS security group <br> - Set up DB subnet group <br> - Launch EC2 instance for RDS <br> - Create RDS Database instance <br> - Deploy application <br> - Back up and restore databases                                             | 10/13/2025 | 10/13/2025      | <https://000005.awsstudygroup.com/vi/>                                             |
| Tuesday   | - Set up VPC for Auto Scaling <br> - Create EC2 Instance and database with Amazon RDS <br> - Create AMI from EC2 and Launch template <br> - Create target group and Load balancer <br> - Create Auto Scaling Group <br> - Test manual, schedule, and dynamic scaling | 10/14/2025 | 10/14/2025      | <https://000006.awsstudygroup.com/vi/>                                             |
| Wednesday | - CloudWatch fundamentals and metrics <br> - Amazon DynamoDB configuration and management                                                                                                                                                                            | 10/15/2025 | 10/15/2025      | <https://000008.awsstudygroup.com/vi/> <br> <https://000060.awsstudygroup.com/vi/> |
| Thursday  | - **Workshop Data Science on AWS:** <br>&emsp; + AWS AI/ML Stack <br>&emsp; + Amazon Comprehend, Translate, Textract <br>&emsp; + Amazon Polly, Transcribe, Rekognition                                                                                              | 10/16/2025 | 10/16/2025      | Workshop Link                                                                      |
| Friday    | - AWS Networking and Content Delivery fundamentals <br> - CloudFront, Route 53, and CDN best practices                                                                                                                                                               | 10/17/2025 | 10/17/2025      | <https://000092.awsstudygroup.com/vi/>                                             |
| Saturday  | - Review Secure Architectures (IAM, MFA, SCP, Encryption, Security Groups, NACLs) <br> - Review GuardDuty, Shield, WAF, Secrets Manager <br> - Cost optimization review                                                                                              | 10/18/2025 | 10/18/2025      | <https://cloudjourney.awsstudygroup.com/>                                          |

### Week 6 Achievements:

- **Mastered Amazon RDS Database Deployment:**

  - Created VPC, security groups, and DB subnet groups
  - Successfully launched RDS database instances
  - Configured database backups and automated restore procedures
  - Deployed applications with secure database connectivity
  - Implemented Multi-AZ deployments for high availability
  - Understood RDS parameter groups and option groups

- **Implemented Auto Scaling Solutions:**

  - Created custom AMIs from EC2 instances
  - Configured launch templates with specific configurations
  - Set up Application Load Balancers with target groups
  - Implemented manual, scheduled, and dynamic scaling policies
  - Tested scaling solutions under load
  - Monitored scaling activities and performance metrics
  - Configured scaling group lifecycle hooks

- **Mastered CloudWatch Monitoring and Observability:**

  - Configured CloudWatch metrics for all AWS resources
  - Created custom dashboards for real-time monitoring
  - Set up alarms and notifications for critical events
  - Implemented log aggregation and analysis
  - Understood metric math and custom metrics
  - Created detailed monitoring strategies

- **Explored DynamoDB NoSQL Database:**

  - Configured DynamoDB tables and indexes
  - Understood partition keys and sort keys
  - Practiced read/write capacity management
  - Explored DynamoDB Streams for event processing
  - Configured TTL (Time-to-Live) for data expiration
  - Learned DynamoDB best practices

- **Learned AWS AI/ML Services:**

  - Explored AWS AI/ML Stack architecture
  - Used Amazon Comprehend for text analysis and entity recognition
  - Practiced Amazon Translate for language translation
  - Experimented with Amazon Textract for document processing
  - Configured Amazon Polly for text-to-speech conversion
  - Used Amazon Transcribe for speech-to-text transcription
  - Explored Amazon Rekognition for image and video analysis

- **Mastered AWS Networking and Content Delivery:**

  - Configured CloudFront CDN for global content distribution
  - Set up CloudFront distributions with S3 origins
  - Used Route 53 for DNS management and routing policies
  - Implemented geo-routing and failover strategies
  - Understood caching behavior and invalidation
  - Applied networking best practices

- **Reviewed and Strengthened Security Architecture:**

  - Reinforced IAM, MFA, and Service Control Policies (SCPs)
  - Reviewed encryption strategies (KMS, TLS/ACM)
  - Studied AWS GuardDuty for threat detection
  - Understood AWS Shield for DDoS protection
  - Reviewed AWS WAF for application protection
  - Practiced with AWS Secrets Manager
  - Understood VPN connections and hybrid networking

- **Practical Troubleshooting:**
  - Resolved connectivity problems between instances
  - Fixed routing conflicts in VPCs
  - Corrected security group misconfigurations
  - Validated end-to-end application connectivity
