# Lab4-CloudWatch-Monitoring
# AWS Lab 4️⃣ — CloudWatch Monitoring & Logging for EC2

## 🎯 Goal
Enable operational monitoring on EC2 using Amazon CloudWatch Agent with secure, centralized metric collection.

## 🔧 What I did:
- Attached `AmazonCloudWatchAgentServerPolicy` to existing IAM Role.
- Diagnosed and fixed SSH access issue (Security Group + dynamic IP change).
- Installed and configured CloudWatch Agent on Amazon Linux 2023.
- Ran interactive wizard and thoughtfully answered config prompts:
  - Disabled CollectD and StatsD
  - Focused on host-level metrics (CPU, memory, disk)
  - Accepted 1-minute resolution
  - Did NOT store config in SSM for this lab
- Started agent with `systemctl` and confirmed service `active`.
- Verified metrics flowing into CloudWatch → CWAgent namespace.

## 🔒 Security notes:
- Principle of Least Privilege throughout.
- Security Group opened temporarily for SSH from my IP only.
- IAM Role used — no hardcoded credentials.

## 🧠 Skills practiced:
- IAM policy management
- CloudWatch Agent configuration
- Real-world diagnostics and secure access controls
- EC2 operational monitoring and observability setup

## 📂 Screenshots (to be added later):
- IAM Role w/ CloudWatch policy
- CloudWatch Metrics console showing metrics from this instance
- Agent running (`systemctl status amazon-cloudwatch-agent`)
