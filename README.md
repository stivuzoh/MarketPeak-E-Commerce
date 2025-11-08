MarketPeak_Ecommerce Readme file
# 🚀 Step-by-Step Guide: E-Commerce Website Deployment with Git & AWS

## 📋 Project Overview
Deploying an e-commerce website using Git version control and AWS EC2 instance with Apache web server.

---

## 🛠️ Step 1: Create Directory and Initialize Git 📁
```bash
$ mkdir MarketPeak_ECommerce
$ cd MarketPeak_ECommerce
$ git init
```
![Step 1](Step1%20Creating%20a%20directory%20and%20initializing%20Git.png)
Initialized empty Git repository for the e-commerce project

---

## 📥 Step 2: Download E-Commerce Template 🎨
```bash
$ unzip 'c:/Users/uzoma/Downloads/Ecommerce Template.zip.zip'
```
![Step 2](Step2%20Ecommerce%20website%20template%20downloaded%20and%20unzipped.png)
Extracted template files including HTML, CSS, images, and JavaScript files

---

## 🔍 Step 3: Check Git Status 📊
```bash
$ git status
```
![Step 3](Step3%20File%20Untracked.png)
Files are untracked - ready to be added to version control

---

## ➕ Step 4: Add Files to Staging ✅
```bash
$ git add .
```
![Step 4](Step4%20File%20added.png)
All files added to staging area with line ending warnings

---

## 🔄 Step 5: Verify Staged Files 👀
```bash
$ git status
```
![Step 5](Step5%20Running%20git%20status%20to%20check%20if%20files%20have%20been%20added.png)
Files successfully staged and ready for commit

---

## 💾 Step 6: Configure Git and Commit 🔧
```bash
$ git config --global user.name "stivuzoh"
$ git config --global user.email "stephenuzomawasaki@yahoo.com"
$ git commit -m "Initial commit with basic e-commerce site structure"
```
![Step 6](Step6%20Credentials%20added%20and%20file%20commited.pngpng)
Initial commit created with 35 files

---

## ☁️ Step 7: Push to GitHub 🚀
```bash
$ git remote add origin https://github.com/stivuzoh/MarketPeak-E-Commerce
$ git push -u origin master
```
![Step 7](Step7%20file%20pushed%20to%20github.pngpng)
Code successfully pushed to GitHub repository

---

## 🖥️ Step 8: Launch AWS EC2 Instance 🌐
Launched EC2 instance with key pair: `devops.pem`
![Step 8](Step8%20aws%20instance%20launched.pngpng)
AWS instance ready for connection

---

## 🔗 Step 9: Connect to EC2 Instance 🔑
```bash
$ ssh -i "devops.pem" ec2-user@ec2-18-218-122-122.us-east-2.compute.amazonaws.com
```
![Step 9](Step9%20Successfully%20connected%20online%20using%20my%20ssh%20key.pngpng)
Successfully connected to EC2 instance

---

## 🔐 Step 10: Generate SSH Key Pair 🗝️
```bash
$ ssh-keygen
```
![Step 10](Step10%20ssh%20keypair%20generated.pngpng)
SSH key pair generated for GitHub authentication

---

## 🔗 Step 11: Add SSH Key to GitHub 📝
Added public key to GitHub SSH keys section  
![Step 11](Step11%20SSH%20Keypair%20added%20to%20githup.pngpng)
SSH key configured for secure GitHub access

---

## 📥 Step 12: Clone Repository on EC2 🔄
```bash
$ git clone git@github.com:stivuzoh/MarketPeak-E-Commerce.git
```
![Step 12](Step12%20Repo%20cloned.pngpng)
Repository cloned to EC2 instance

---

## 🖥️ Step 13: Install Apache Web Server ⚡
```bash
$ sudo yum install httpd -y
$ sudo systemctl start httpd
$ sudo systemctl enable httpd
```
![Step 13](Step13%20Apache%20web%20server%20installed.pngpng)
Apache web server installed and activated

---

## 📂 Step 14: Deploy Website Files 🗃️
```bash
$ sudo rm -rf /var/www/html/*
$ sudo cp -r ~/MarketPeak-E-Commerce/* /var/www/html/
$ sudo systemctl reload httpd
```
![Step 14](Step14%20httpd%20file%20copied.pngpng)
Website files deployed to web server directory

---

## 🌐 Step 15: Verify Website Live ✅
Website accessible via browser  
![Step 15](Step15%20web%20picture%20from%20browser.pngpng)
E-commerce website successfully deployed and live

---

## 🌿 Step 16: Create Development Branch 🔀
```bash
$ git checkout -b development
$ git status
```
![Step 16](Step16%20Git%20branch%20created%20with%20untracked%20files.pngpng)
Development branch created with file changes

---

## 💾 Step 17: Commit Changes 📝
```bash
$ git add .
$ git commit -m "Add new features or fix bugs"
```
![Step 17](Step17%20files%20commited.pngpng)
Changes committed to development branch

---

## 🔄 Step 18: Create Pull Request on GitHub 🤝
Merged development branch to master via GitHub PR  
![Step 18](Step18%20Pull%20request%20and%20merged%20in%20Github.pngpng)
Pull request successfully merged

---

## 🔀 Step 19: Merge Locally 📥
```bash
$ git checkout master
$ git merge development
```
![Step 19](Step19%20File%20merged%20on%20cli.pngpng)
Changes merged locally using fast-forward

---

## 🚀 Step 20: Push Development Branch ☁️
```bash
$ git push origin development
```
![Step 20](Step20%20File%20pushed%20to%20github.pngpng)
Development branch pushed to remote

---

## 🔄 Step 21: Final Sync ✅
```bash
$ git pull origin master
$ sudo systemctl reload httpd
```
![Step 21](Step21%20Final%20push%20to%20github.pngpng)
Latest changes pulled and web server reloaded

---

## 🎯 Conclusion ✅

### ✅ Successfully Accomplished:
- 🏗️ Project Setup: Created Git repository and added e-commerce template  
- ☁️ Cloud Deployment: Launched AWS EC2 instance and deployed website  
- 🔐 Security: Configured SSH keys for secure GitHub access  
- 🌐 Web Hosting: Installed and configured Apache web server  
- 🔄 Version Control: Implemented Git branching strategy with development workflow  
- 🤝 Collaboration: Used pull requests for code review and merging  

### 🛠️ Technologies Used:
- Git & GitHub for version control  
- AWS EC2 for cloud hosting  
- Apache HTTP Server for web hosting  
- SSH for secure remote access  
- HTML/CSS/JavaScript for frontend  

### 📈 Key Learnings:
- End-to-end web deployment pipeline  
- Git branching and merging strategies  
- AWS EC2 instance management  
- Linux server administration  
- Continuous deployment practices  
