# Live Visitor Counter 🌐👥

A real-time, serverless website visitor counter that shows how many people are currently browsing your site. Built entirely on AWS with zero servers to manage — it scales automatically and costs almost nothing to run.

Check out the live demo below!

## ✨ See It Live
[**👉 Try the Live Counter Here**](https://resume-visitor-website.s3.us-east-1.amazonaws.com/index.html)  
*(Link your actual S3 website endpoint above)*

## 📸 What It Looks Like

### Main Dashboard
![Website Screenshot 1](./images/website-screenshot-1.png)

### Live Count in Action
![Website Screenshot 2](./images/website-screenshot-2.png)

## 🏗️ How It Works (The Simple Version)

1. **You open the website** → hosted in an S3 bucket.
2. **Your browser pings the API** → hits API Gateway.
3. **A Lambda function wakes up** → updates the visitor count.
4. **DynamoDB stores the number** → quick and reliable.
5. **The website updates live** → you see the new count instantly.

No servers, no headaches. Just code that runs when people show up.

![Architecture Diagram](./images/architecture.png)

## 🧩 The Tech Behind It

| Part | What It Does | Picture |
|------|--------------|---------|
| **S3** | Holds the website files (HTML, CSS, JS). | ![S3](./images/s3.png) |
| **API Gateway** | Front door for the visitor-count API. | ![API Gateway](./images/api.png) |
| **Lambda** | Serverless function that updates the count. | ![Lambda](./images/lambda.png) |
| **DynamoDB** | Database that stores the live visitor number. | ![DynamoDB](./images/dynamodb.png) |

## 🚀 Getting Started

Want to run your own?

### What You'll Need:
- An AWS account (free tier works)
- AWS CLI set up on your machine
- Your website files (HTML/CSS/JS)

### Steps to Deploy:
1. **Upload your site** to a new S3 bucket and enable static hosting.
2. **Create a DynamoDB table** with `visitorCount` as the primary key.
3. **Write and deploy** the Lambda function (Python/Node.js) that increments the count.
4. **Set up API Gateway** to trigger that Lambda.
5. **Update your website's JavaScript** to call your new API endpoint.
6. **Open your S3 website URL** and watch the counter go up!


## 📁 What's in This Repo
