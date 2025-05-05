# 🚀 Serverless Flask API on AWS Lambda with Zappa

This project demonstrates deploying a Flask web application serverlessly using AWS Lambda and API Gateway, powered by Zappa.
## ⚠️ Python Compatibility Notice

> 🐍 **Zappa and AWS Lambda do not support Python 3.13 or newer.**

If you are using Python 3.13+ locally, you **must install Python 3.9** or any version **between 3.7 and 3.12** to ensure compatibility.

Use tools like [`pyenv`](https://github.com/pyenv/pyenv) to manage multiple Python versions.

Example:
```bash
pyenv install 3.9.18
pyenv local 3.9.18
```

## 🧰 Stack
- **Flask** (Python micro-framework)
- **AWS Lambda** (serverless runtime)
- **API Gateway** (HTTP endpoint)
- **Zappa** (Python tool for serverless deployments)
- **S3** (for deployment package storage)

---

## ✅ Features
- Serverless HTTP API
- 100% pay-as-you-go (no EC2 or servers running)
- Easy CI/CD potential with GitHub + Zappa
- Great for small APIs, webhooks, and lightweight services

---

## 📁 Project Structure
```
flask-serverless/
├── app.py
├── requirements.txt
├── zappa_settings.json
└── venv/
```

---

## 🚀 Deployment Steps




### 1. Setup environment
```bash
python3 -m venv venv
source venv/bin/activate
pip install flask zappa
```
### 2. Initialize Zappa
```
zappa init
```
### 3. Deploy to AWS Lambda
```
zappa deploy dev
```
### 4. Update if needed
```
zappa update dev
```
### 🔄 Example Endpoint
Once deployed, visit:

https://your-api-id.execute-api.us-east-1.amazonaws.com/dev/
Response:
Hello From Flask on AWS Lambda!

### 🧼 Cleanup
```
zappa undeploy dev
```
### 📌 Next Steps (Coming Soon)
 - Rebuild using Terraform (Lambda, API Gateway, IAM)

 - Add CI/CD via GitHub Actions
