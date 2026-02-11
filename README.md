# 🧹 AWS EBS Snapshot Cleanup – Serverless Cost Optimization 💸 

## 🧠 Problem
Over time, unused EBS snapshots (especially from deleted EC2 volumes) can accumulate and cause unnecessary AWS costs. These often get left behind unknowingly by developers or teams.

## 💡 Solution
This **serverless AWS Lambda function** automates the cleanup of stale EBS snapshots, helping to **optimize cloud costs**.

## 🚀 Features 
- Uses **Boto3** to interact with AWS EC2 API
- Identifies and deletes:
  - Snapshots with no volume
  - Snapshots of volumes not attached to any running EC2 instance
- Can be scheduled to run periodically using **AWS EventBridge**
- IAM-controlled secure access

## 📁 Files
- `lambda_function.py`: Main Lambda function logic

## 🔐 IAM Permissions Required 
Attach the following permissions to the Lambda role:
- `ec2:DescribeSnapshots`
- `ec2:DeleteSnapshot`
- `ec2:DescribeVolumes`
- `ec2:DescribeInstances`

## 🛠️ Setup & Deployment
1. Create a Lambda function in AWS Console
2. Set Python as runtime
3. Paste code from `lambda_function.py`
4. Attach appropriate IAM role with the above permissions
5. (Optional) Add a cron trigger via **EventBridge** to automate execution

## 🖥️ Sample Output


## 📈 Benefits
- Saves money by removing orphaned resources
- Fully automated and serverless
- Easy to integrate into DevOps/cloud ops workflows

## 📸 Future Enhancements
- SNS notifications for deleted snapshots
- Exclude snapshots with specific tags (e.g., `keep=true`)
- Monitor usage via CloudWatch metrics

---

Made with ☁️ by Alok – just cleaning up AWS, one snapshot at a time 😎

