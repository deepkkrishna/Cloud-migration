AWS Cloud Migration Simulation (EC2 to RDS)

Overview

This project demonstrates a basic cloud migration scenario where a MySQL database hosted on an EC2 instance (simulating on-premise environment) is migrated to Amazon RDS.

EC2 (MySQL - Source)
        ↓
   mysqldump
        ↓
RDS MySQL (Target)

Technologies Used
	•	AWS EC2
	•	AWS RDS (MySQL)
	•	AWS VPC
	•	Terraform
	•	MySQL
	•	Linux

  Infrastructure Setup
	•	Created VPC, subnet, IGW using Terraform
	•	Launched EC2 instance in public subnet
	•	Configured security groups for SSH and MySQL access

   Migration Steps
	1.	Installed MySQL on EC2
	2.	Created sample database and inserted data
	3.	Exported database using mysqldump
	4.	Created RDS MySQL instance
	5.	Configured security group and connectivity
	6.	Imported data into RDS

  Challenges Faced
	•	IAM permission issues during Terraform provisioning
	•	AMI compatibility issues across regions
	•	Security group misconfiguration blocking DB access
	•	RDS authentication errors

   Key Learnings
	•	Infrastructure provisioning using Terraform
	•	AWS networking (VPC, subnets, security groups)
	•	Database migration techniques
	•	Troubleshooting real-world cloud issues
