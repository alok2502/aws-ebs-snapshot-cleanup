# aws-ebs-snapshot-cleanup
A serverless AWS Lambda function to automatically delete stale EBS snapshots for cost optimization.

# AWS EBS Snapshot Cleanup - Lambda Function

## 🧠 Problem
EBS snapshots left behind after EC2/Volume deletion can accumulate and lead to unnecessary AWS billing.

## ✅ Solution
This AWS Lambda function identifies and deletes EBS snapshots that are:
- Not attached to any volume
- OR attached to a volume that no longer exists or is not in use

## 💡 Features
- Uses Boto3 to interact with EC2 API
- Deletes stale snapshots safely
- Scheduled via AWS EventBridge (cron)
- IAM-secured access to only necessary resources

## 📂 Files
- `lambda_function.py` – main Lambda script

## 📦 Deployment
1. Create a Lambda function with Python runtime
2. Add necessary IAM permissions
3. Deploy the code and test manually
4. Add a scheduled trigger using EventBridge

## 📸 Sample Output


## 📈 Future Ideas
- SNS notifications
- Tag-based exclusions
- Cleanup of unattached EBS volumes

---

Contributions welcome! ⭐

