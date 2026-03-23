# 🌐 Terraform AWS Static Website (Secure CloudFront + S3)

## 📌 Overview

This project demonstrates how to deploy a secure, production-style static website on AWS using Infrastructure-as-Code with Terraform.

Instead of exposing an S3 bucket publicly, this architecture follows best practices:

* Private S3 bucket (no public access)
* CloudFront CDN for global delivery
* Origin Access Control (OAC) to securely connect CloudFront to S3

---

## 🏗️ Architecture

User → CloudFront (CDN) → Private S3 Bucket

* **CloudFront** handles HTTPS, caching, and global distribution
* **S3** stores static website files (HTML)
* **Terraform** provisions and manages all infrastructure

---

## ⚙️ Technologies Used

* Terraform (Infrastructure-as-Code)
* AWS S3 (object storage)
* AWS CloudFront (CDN)
* HTML (static frontend)

---

## 🚀 Features

* Fully automated infrastructure deployment
* Secure S3 bucket (no public access)
* CDN-backed website with HTTPS
* Reproducible environment using Terraform
* Automated upload of website files

---

## ▶️ Deployment Steps

### 1. Clone the repo

```bash
git clone https://github.com/RURational2000/terraform-aws-static-site
cd terraform-aws-static-site
```

### 2. Initialize Terraform

```bash
terraform init
```

### 3. Apply configuration

```bash
terraform apply
```

Type `yes` when prompted.

---

## 🌍 Access the Website

After deployment, Terraform will output a CloudFront URL:
'''
`https://<distribution-id>.cloudfront.net`
'''

⚠️ Note: Initial deployment may take 5–10 minutes due to CloudFront provisioning.

---

## 🧹 Cleanup

To avoid AWS charges:

```bash
terraform destroy
```

---

## 🔒 Security Highlights

* S3 bucket is fully private
* Access restricted via CloudFront Origin Access Control (OAC)
* No public bucket policies
* HTTPS enforced via CloudFront

---

## 💼 What I Learned

* How to use Terraform to provision AWS infrastructure
* Differences between public and private cloud architectures
* How CloudFront securely serves content from S3
* Debugging AWS permission and access control issues

---

## 📈 Future Improvements

* Add custom domain with Route 53
* Configure SSL certificate using AWS ACM
* Integrate CI/CD pipeline for automatic deployments
* Add cache invalidation on updates

---

## 👤 Author

Stephen E. Frost
Linkedin Profile: <https://www.linkedin.com/in/steveefrost/>
