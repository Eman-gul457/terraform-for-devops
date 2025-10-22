<h1 align="center">🌍 Terraform For DevOps — EC2 & S3 Automation</h1>

<p align="center">
  <b>Automate AWS Infrastructure using Terraform</b><br>
  <i>Created by Eman Gul | Learning Terraform & DevOps</i>
</p>

---

### 🧭 Tech Stack
<p align="center">
  <img src="https://img.shields.io/badge/Terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-%23FCC624.svg?style=for-the-badge&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/DevOps-%23007ACC.svg?style=for-the-badge&logo=azure-devops&logoColor=white" />
  <img src="https://img.shields.io/badge/Infrastructure--as--Code-%23121011.svg?style=for-the-badge&logo=git&logoColor=white" />
</p>

---

## 🎯 Goal of this Project
This project automates the setup of a simple AWS environment using **Terraform**.  
It creates the following infrastructure components:
- ✅ **Key Pair** (for SSH access)
- ✅ **Security Group** (with ports 22, 80, 8000 open)
- ✅ **EC2 Instance** (Ubuntu AMI)
- ✅ **S3 Bucket**

Everything is provisioned with a single command — **`terraform apply`** 💪

---

## 📁 Project Structure

terraform-for-devops/
├── ec2.tf
├── s3.tf
├── provider.tf
├── variables.tf
├── outputs.tf
├── terra-key-ec2.pub
├── .gitignore
├── README.md
└── screenshots/
├── terraform-apply-success.png
├── terraform-apply-output.png
├── ec2-console.png
├── s3-console.png
└── terraform-destroy-output.png

---

---

## ⚙️ Prerequisites

- Terraform installed → [Install Terraform](https://developer.hashicorp.com/terraform/downloads)
- AWS CLI configured → `aws configure`
- AWS IAM user with EC2, S3, and VPC permissions
- Public key file: `terra-key-ec2.pub` (✅ safe to upload)
- Internet connection (Terraform will download AWS plugins)

---

## 🚀 How to Run

1️⃣ Initialize Terraform
terraform init

2️⃣ Check the plan
terraform plan

3️⃣ Apply configuration
terraform apply
# Type 'yes' when asked or terraform apply -auto-approve

<img width="1069" height="476" alt="terraform_apply_output" src="https://github.com/user-attachments/assets/0dc7e58c-425e-49cd-a8e6-e609a5768fb5" />

4️⃣ View Outputs
terraform output

<img width="1069" height="476" alt="terraform_apply_output" src="https://github.com/user-attachments/assets/69d82bdf-a47b-4770-8ab5-a52ed532bf8d" />

### 💻 EC2 Console (Instance Running)
This screenshot shows your EC2 instance successfully created and running in the AWS Management Console.

<img width="1023" height="436" alt="aws-ec2-dashboard" src="https://github.com/user-attachments/assets/404a6ba8-17f4-44ca-8eb3-8914d4341d71" />

### 🪣 S3 Console (Bucket Created)
This screenshot shows the S3 bucket created by Terraform visible in the AWS S3 console.

<img width="1007" height="382" alt="s3-console-bucket" src="https://github.com/user-attachments/assets/67ae9c05-f3d9-411a-a81a-7d42a2188a81" />


5️⃣ Destroy (when done)
terraform destroy
# Type 'yes' when asked or terraform destroy -auto-approve

<img width="912" height="450" alt="terraform-destroy-output" src="https://github.com/user-attachments/assets/a90091b2-a9bc-4aa8-bd5d-5927e016b962" />

---

🔐 Security Notes
Do not upload .pem or private keys.
.gitignore must exclude:
terraform.tfstate
*.pem
*.key
Always destroy resources after testing to avoid AWS charges.
