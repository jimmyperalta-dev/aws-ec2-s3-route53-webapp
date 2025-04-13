# 🚀 Static Website Deployment on AWS (S3 + Route 53 + CloudFront + HTTPS)

🔗 **Live Demo:** [https://www.deployjimmy.com](https://www.deployjimmy.com)  
🔗 **API Endpoint:** [https://api.deployjimmy.com/api](https://api.deployjimmy.com/api)

This project demonstrates a secure and scalable static website and backend API deployment on AWS. The static site is hosted on Amazon S3, delivered globally via CloudFront, and protected with HTTPS using AWS Certificate Manager. Domain routing is handled through Route 53. The backend is hosted on EC2 and secured via a separate CloudFront distribution.

---

## ✅ Highlights

- 📦 **Amazon S3** – Static website hosting with public read-only access  
- 💻 **Amazon EC2** – Node.js backend API hosted on port 3000  
- 🔒 **CloudFront + ACM** – CDN and SSL for secure, low-latency access  
- 🌐 **Route 53** – DNS routing for both frontend and backend  
- ⚙️ **Manual AWS Deployment** – Built step-by-step for full understanding  

---

## 📁 Project Structure

```bash
aws-ec2-s3-route53-webapp/
├── architecture/                  # AWS architecture diagram (PNG)
├── index.html                     # Static website content
├── error.html                     # Custom error page (optional)
├── LICENSE
└── README.md
```

---

## 🗺️ Architecture Overview

![Architecture Diagram](architecture/aws-ec2-s3-route53.png)

---

## 🛠 Deployment Summary

### 🌐 Frontend (Static Site)

1. Created and configured an S3 bucket named `www.deployjimmy.com`
2. Enabled static website hosting and uploaded `index.html` and `error.html`
3. Requested and validated an SSL certificate using ACM
4. Created CloudFront distribution pointing to the S3 website endpoint
5. Connected domain to CloudFront via Route 53 Alias A-record
6. Verified global HTTPS access to the static site

### 🔧 Backend API

1. Launched EC2 instance with Node.js backend (port 3000)
2. Configured security group and PM2 for uptime
3. Created ACM certificate for `api.deployjimmy.com`
4. Created CloudFront distribution pointing to EC2 on port 3000
5. Configured Route 53 A-record (alias) to point `api.deployjimmy.com` to CloudFront
6. Confirmed secure API delivery via HTTPS

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

---

## 👤 Author

**Jimmy Peralta**  
🛠️ Systems Support Engineer | ☁️ AWS Cloud Enthusiast  
🌐 [https://www.deployjimmy.com](https://www.deployjimmy.com)