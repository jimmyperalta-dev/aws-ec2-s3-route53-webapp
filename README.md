# 🚀 Static Website Deployment on AWS (S3 + Route 53 + CloudFront + HTTPS)

![AWS Cloud](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white)
![CloudFront](https://img.shields.io/badge/CloudFront-232F3E?style=for-the-badge)
![Route53](https://img.shields.io/badge/Route53-8C4FFF?style=for-the-badge)
![EC2](https://img.shields.io/badge/EC2-FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white)

🔗 **Live Demo:** [https://www.deployjimmy.com](https://www.deployjimmy.com)  
🔗 **API Endpoint:** [https://api.deployjimmy.com/api](https://api.deployjimmy.com/api)

## 📋 Project Overview

This project demonstrates a secure and scalable static website and backend API deployment on AWS. The static site is hosted on Amazon S3, delivered globally via CloudFront, and protected with HTTPS using AWS Certificate Manager. Domain routing is handled through Route 53. The backend is hosted on EC2 and secured via a separate CloudFront distribution.

---

## ✅ Key Features & Services

- 📦 **Amazon S3** – Static website hosting with public read-only access  
- 💻 **Amazon EC2** – Node.js backend API hosted on port 3000  
- 🔒 **CloudFront + ACM** – CDN and SSL for secure, low-latency access  
- 🌐 **Route 53** – DNS routing for both frontend and backend  
- ⚙️ **Manual AWS Deployment** – Built step-by-step for full understanding  

---

## 🗺️ Architecture Overview

![Architecture Diagram](architecture/aws-ec2-s3-route53.png)

---

## 📁 Project Structure

```bash
aws-ec2-s3-route53-webapp/
├── architecture/                  # AWS architecture diagram (PNG)
├── index.html                     # Static website content
├── error.html                     # Custom error page (optional)
├── LICENSE
├── docs/                         # Additional documentation
│   └── logical-flow.md           # Detailed logical flow explanation
└── README.md
```

---

## 🛠 Deployment Details

### 🌐 Frontend (Static Site)

1. Created and configured an S3 bucket named `www.deployjimmy.com`
   - Enabled static website hosting
   - Configured bucket policy for public read access
   - Uploaded `index.html` and `error.html`

2. Secured with HTTPS
   - Requested and validated an SSL certificate using ACM
   - Created CloudFront distribution pointing to the S3 website endpoint
   - Configured HTTPS redirect and modern security protocols

3. Domain Configuration
   - Connected domain to CloudFront via Route 53 Alias A-record
   - Verified global HTTPS access to the static site

### 🔧 Backend API

1. EC2 Configuration
   - Launched EC2 instance with Node.js backend (port 3000)
   - Configured security group to allow HTTP traffic
   - Installed PM2 for process management and auto-restart

2. API Security
   - Created ACM certificate for `api.deployjimmy.com`
   - Created CloudFront distribution pointing to EC2 on port 3000
   - Configured appropriate cache behaviors and origin settings

3. Domain Routing
   - Configured Route 53 A-record (alias) to point `api.deployjimmy.com` to CloudFront
   - Confirmed secure API delivery via HTTPS

---

## 🔗 Live Backend Endpoint

**URL:** [https://api.deployjimmy.com/api](https://api.deployjimmy.com/api)  
📦 Returns JSON response from EC2-hosted Node.js backend.

---

## 🧠 Skills Demonstrated

- AWS service integration (S3, EC2, Route 53, CloudFront, ACM)  
- Manual domain, DNS, and certificate management  
- Secure content and API delivery using CDN  
- Static + dynamic architecture without automation tools  
- Full-stack deployment workflow

---

## 🔄 Related Projects

- [EC2 Metrics Dashboard](https://github.com/jimmyperalta-dev/aws-ec2-monitoring-dashboard)
- [Serverless Contact Form API](https://github.com/jimmyperalta-dev/aws-s3-lambda-api-contactform)

---

## 👤 Author

**Jimmy Peralta**  
🛠️ Associate Media Systems Engineer | ☁️ AWS Cloud Enthusiast  
🌐 [https://www.deployjimmy.com](https://www.deployjimmy.com)