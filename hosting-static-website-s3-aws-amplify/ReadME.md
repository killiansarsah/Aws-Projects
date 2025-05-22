 🌐 Website Deployment Using AWS Amplify (via S3 Bucket and Static Website Hosting)

 📌 Overview

In this project, I built a responsive website from scratch and hosted it using AWS Amplify's deployment feature. Instead of using Amazon S3 static website hosting—which can be more complex due to the need to configure bucket policies, enable public access, and manually add permissions for version control and deployment—I simplified the process by using the AWS Amplify App. Amplify streamlined hosting by allowing me to upload the website files directly from my desktop using its intuitive drag-and-drop interface, eliminating the need for additional policy configurations and making deployment much faster and more manageable.

> 💻 Built With: HTML, CSS, JavaScript  
> ☁️ Hosted On: Amazon Web Services (AWS) - S3 & Amplify  
> 🚀 Deployment Method: Manual upload via S3 → Amplify  
> 🔗 Live Site: [https://staging.d1xbtx3rrjqfob.amplifyapp.com/]  
> 📂 Source Files: Stored locally on desktop



 ⚙️ Process Breakdown

 ✅ Step 1: Website Creation

- I created the website using standard web technologies:
  - HTML for structure
  - CSS for design
  - JavaScript for interactivity 
- All files were placed in a well-structured project folder:
  ```
  my-website/
  ├── index.html
  ├── style.css
  ├── script.js
  └── assets/
  ```

 ✅ Step 2: Create an S3 Bucket

- Logged into the AWS Management Console and navigated to the S3 service
- Created a new bucket and named it: dezagbrokers
- Choose default settings for public access and bucket configuration (adjusted later for hosting)

 ![image](https://github.com/user-attachments/assets/dd841062-5ee7-4113-8cd9-ad13bf8a5a26)


 ✅ Step 3: Upload Files to the Bucket

- Uploaded the entire website folder (unzipped) directly into the DezagBrokers bucket using the AWS Console
- Ensured that `index.html` was at the root level

 ![image](https://github.com/user-attachments/assets/c17463be-6954-49f2-b9b6-f8815e5ed918)


 ✅ Step 4: Enable Static Website Hosting

- Went to the Properties tab of the dezagbrokers bucket
- Scrolled to the bottom and enabled Static website hosting
- Specified the `index.html` file as the entry point
- AWS recommended using AWS Amplify for complete hosting, so I proceeded with Amplify
 
![image](https://github.com/user-attachments/assets/2be73fbd-8929-4dc1-89c3-2d4c30b39c46)


 ✅ Step 5: Deploy with AWS Amplify

- Navigated to [AWS Amplify Console](https://console.aws.amazon.com/amplify/)
- Choose "Deploy without Git provider" (Manual deployment)

 ![image](https://github.com/user-attachments/assets/f1d2e188-a458-4c8e-aad1-9588ed1317c2)


- Amplify handled deployment and provided a live HTTPS-secured URL
 
![image](https://github.com/user-attachments/assets/6f5b2ade-0395-4dce-8544-3c4fd3a9c3e6)


 ![image](https://github.com/user-attachments/assets/78a0da0c-f530-4c39-a029-786021786cc5)


 🔐 Optional Feature: Domain Setup (Not used here)

Though I used the default Amplify URL, AWS also allows:
- Custom domain integration (via Route 53 or external provider)
- SSL certification via AWS Certificate Manager



 🧠 Lessons Learned

- Learned how to host static websites using AWS S3 and Amplify
- Understood the integration between S3's static site hosting and Amplify's deployment interface
- Practiced using AWS storage, permissions, and hosting features



 💬 Final Thoughts

This project highlights the ease of deploying static websites on AWS using both S3 and Amplify. It combines manual control with powerful cloud infrastructure, making it ideal for showcasing practical AWS deployment skills.



 🔗 Resources

- [S3 Static Website Hosting] (https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
- [AWS Amplify Hosting Overview](https://docs.amplify.aws/hosting/)
- [Manual Deployment with Amplify] (https://docs.aws.amazon.com/amplify/latest/userguide/manual-deploys.html)



 ✅ Skills Demonstrated

- Static Website Development
- AWS S3 Configuration & Hosting
- AWS Amplify Deployment (Manual)
- Cloud Hosting & HTTPS Deployment
- Web Infrastructure Setup

