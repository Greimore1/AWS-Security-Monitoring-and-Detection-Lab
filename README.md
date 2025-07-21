# AWS Security Monitoring and Detection Lab

This project demonstrates the deployment of a real-world AWS detection pipeline using Terraform, CloudTrail, CloudWatch, and SNS. It simulates access key creation events and triggers alerting mechanisms to emulate real-world security operations use cases.

All infrastructure was provisioned using Terraform and automatically torn down to avoid incurring ongoing AWS charges.

---

## Tools Used

- **Terraform**
- **AWS CloudTrail**
- **AWS CloudWatch**
- **AWS SNS (Simple Notification Service)**
- **IAM**
- **AWS CLI**
- **Linux CLI (EndeavourOS)**
- **PowerShell (Windows Server)**

---

## Skills Demonstrated

**Infrastructure-as-Code (IaC):**  
Provisioned a CloudTrail log pipeline, IAM roles, CloudWatch metric filters, alarms, and SNS topics entirely via Terraform, ensuring reproducibility and version control.

**Security Detection Engineering:**  
Created a CloudWatch metric filter and alarm to detect the creation of new IAM access keys — a common privilege escalation or credential leak vector.

**Automated Alerting via SNS:**  
Integrated SNS to automatically email security alerts triggered by CloudWatch alarms. Successfully received actionable alert messages within seconds of access key creation.

**Access Key Lifecycle Management:**  
Created and deleted keys to trigger alert conditions, showcasing practical experience with IAM operations and verifying end-to-end pipeline integrity.

**CloudTrail Audit Logging:**  
Configured CloudTrail to log management events across multiple AWS services and store them in a dedicated S3 bucket for audit and retention.

---

## Screenshots

### IAM Access Key Lifecycle
<img width="1920" height="1003" alt="Untitled design1" src="https://github.com/user-attachments/assets/c17b0c4c-e1b0-4bd2-bfb7-b4ff3c3797fa" />


### Terraform CloudTrail Provisioning
<img width="1920" height="1003" alt="Untitled design" src="https://github.com/user-attachments/assets/c3d0a5c1-15db-4fde-b3a9-37288daf5ac0" />


### CloudWatch Alarm Triggered
<img width="413" height="234" alt="Screenshot From 2025-07-20 19-25-29" src="https://github.com/user-attachments/assets/120ec774-d203-4b82-b2ff-cb43d4f70c09" />


### Alarm Visualised in CloudWatch
<img width="1645" height="54" alt="Screenshot From 2025-07-20 19-25-56" src="https://github.com/user-attachments/assets/1fc464dc-6549-4e87-9001-5ebf15b4d11c" />


### SNS Email Notification for Alarm
<img width="1920" height="1003" alt="Untitled design2" src="https://github.com/user-attachments/assets/1efc1321-a98d-471f-9bb1-82a3672ce33b" />


---

## Notes

- All components were destroyed after demonstration using `terraform destroy`.
- Sensitive access key data and ARNs have been redacted.
- The optional Windows agent component was removed due to compatibility issues with `onPrem` mode in the CloudWatch Agent.
- This lab was executed on EndeavourOS with AWS CLI v2 and Terraform 1.8+.

---

