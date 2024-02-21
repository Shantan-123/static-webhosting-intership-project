
# Static-websiteHosting-project
Certainly! Below, I've outlined a step-by-step guide for hosting a static website using **Amazon S3**. This will help you set up a simple website that can be accessed via a custom domain or an S3 endpoint.

## Hosting a Static Website on Amazon S3: A Step-by-Step Guide

### Step 1: Create an S3 Bucket
1. Sign in to the **AWS Management Console** and open the **Amazon S3 console** ¹.
2. Choose **Create bucket**.
3. Enter a **Bucket name** (e.g., `example.com`).
4. Select the **Region** where you want to create the bucket. Choose a region close to you to minimize latency and costs.
5. Accept the default settings and choose **Create**.

### Step 2: Enable Static Website Hosting
1. After creating the bucket, navigate to the **Amazon S3 console** ¹.
2. Select your bucket.
3. Click on the **Properties** tab.
4. Choose **Static website hosting**.
5. Select **Use this bucket to host a website**.
6. Specify an **Index document** (e.g., `index.html`).
7. Optionally, configure an **Error document** (e.g., `error.html`).
8. Save your changes.

### Step 3: Edit Block Public Access Settings
1. Note that enabling static website hosting requires disabling **Block Public Access**. We recommend keeping it enabled for security purposes.
2. If you still want to host a static website with all four Block Public Access settings enabled, consider using **Amazon CloudFront** for additional security ¹.

### Step 4: Add a Bucket Policy
1. To make your bucket content publicly available, add a bucket policy:
    ```json
    {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Effect": "Allow",
          "Principal": "*",
          "Action": "s3:GetObject",
          "Resource": "arn:aws:s3:::name of bucket/*"
        }
      ]
    }
    ```

### Step 5: Configure Index and Error Documents
1. In the **Static website hosting** section, configure your **Index document** (e.g., `index.html`) and **Error document** (if needed).
2. Save your changes.

### Step 6: Test Your Website Endpoint
1. Access your website using the **S3 website endpoint** provided in the **Static website hosting** section.

### Step 7: Clean Up
Remember to delete your resources if you no longer need them to avoid unnecessary costs.

That's it! You've successfully hosted a static website using Amazon S3. Feel free to customize your website by uploading your HTML, CSS, and other assets to the S3 bucket. 🚀







## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/shantanu-khidake-9505a0201)

## 🛠 Skills
HTML, CSS, AWS, S3, EC2, VPC, AWS Lambda,
Linux, Python, MySQL, Data Analysis, Power BI...


