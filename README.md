Cloud Automation using Python (Boto3)

This repository demonstrates how to automate common AWS tasks using Python and Boto3.
It includes simple, practical examples to help you get started with cloud automation:

S3: Create and list buckets

EC2: Launch a basic instance (demo only)

Monitoring: Describe EC2 instances and fetch CloudWatch CPU utilization metrics

⚠️ Important Notes

These scripts are for learning and prototypes only — not production-ready.

Never commit real AWS credentials. Use:

IAM Roles

AWS CLI configuration

Environment variables

The EC2 provisioning script is intentionally minimal — adapt it with VPC, Subnet, Key Pair, and Security Group before production use.

📂 Repository Structure

provision_s3.py – Create an S3 bucket and list buckets

provision_ec2.py – Launch a simple EC2 instance (requires AMI ID update)

monitor_ec2.py – Describe EC2 instances & fetch CloudWatch CPU utilization

requirements.txt – Python dependencies

env.example.txt – Example environment variables (never commit real values)

load_env.sh – Helper script to load .env for local testing

🚀 Quick Start (Local Setup)

Create a virtual environment & install dependencies

python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt


Provide AWS credentials
Recommended: Use AWS CLI profiles or IAM Roles.
For local testing, copy and edit the example env file:

cp env.example.txt .env


Update .env with:

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_REGION

Load environment variables (optional)

source load_env.sh


Run examples

python3 provision_s3.py my-unique-bucket-name-12345
python3 provision_ec2.py
python3 monitor_ec2.py

🛡️ Safety Guidelines

Running the EC2 script may incur AWS charges — terminate instances when done.

Prefer IAM roles or CLI profiles over static keys.

Double-check AWS limits and region-specific AMI IDs before launching resources.

👉 With these examples, you can kickstart your journey into AWS Cloud Automation with Pytho
