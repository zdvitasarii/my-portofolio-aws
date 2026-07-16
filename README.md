🌾 Smart Paddy Monitoring - Bekasi | AWS Cloud Project
> Cloud-Based IoT Solution for Sustainable Agriculture in Indonesia
> **Live Demo:** `https://kebun-pintar-devita-1207.s3-website.ap-southeast-3.amazonaws.com` (ganti dengan URL kamu)
> **Region:** Asia Pacific (Jakarta) `ap-southeast-3` | **Status:** ✅ Live - July 2026
![AWS](https://img.shields.io/badge/AWS-S3-orange) ![IoT](https://img.shields.io/badge/AWS-IoT%20Core-green) ![Status](https://img.shields.io/badge/Status-LIVE-brightgreen) ![Made in Indonesia](https://img.shields.io/badge/Made%20in-Bekasi%2C%20Indonesia-red)
📸 Preview
![Project Live Screenshot](./screenshot.jpg)
Real-time sensor data simulation - Lab 2 LIVE
---
🎯 About The Project
Kebun Pintar adalah sistem monitoring sawah cerdas yang memanfaatkan AWS Cloud untuk membantu petani di Bekasi memantau kondisi lahan secara real-time. Project ini dibangun sebagai langkah awal menuju karir sebagai Cloud Engineer dengan fokus pada AgriTech dan Food Security.
Proyek ini adalah bagian dari perjalanan saya menjadi Calon Engineer Pertanian Pintar Jepang.
🏗️ Architecture
Lab 1 - Static Website Hosting (COMPLETED)
```
User (Browser) -> Amazon S3 (Static Hosting) -> index.html
Region: ap-southeast-3 Jakarta for low latency
```
Lab 2 - Live Data Simulation (COMPLETED)
```
Simulated IoT Sensors -> JavaScript (setInterval 3s) -> Frontend Dashboard
Future: Real Sensors -> AWS IoT Core (MQTT) -> Lambda -> DynamoDB -> Frontend
```
✨ Key Features
[x] Deployed on AWS S3 Static Website Hosting in Jakarta Region
[x] Configured Bucket Policy & Public Access for secure public website
[x] Troubleshooting & Fix: Resolved `404 NoSuchKey` and `index.html.html` double extension error
[x] Real-time Dashboard: Soil Moisture, Temperature, pH, Water Level (Live update every 3s)
[x] Responsive Design & Low-cost Serverless Architecture
[ ] Next: Integration with real AWS IoT Core, CloudWatch Alarms, and DynamoDB
🛠️ Tech Stack
Cloud: AWS S3, AWS IoT Core (Simulated), Amazon CloudWatch
Frontend: HTML5, CSS3, JavaScript (Vanilla)
Tools: AWS Console, Git & GitHub, VS Code
Concepts: Static Hosting, Bucket Policies, Region Selection, Troubleshooting
🚀 How to Deploy (Replicate this project)
Create S3 Bucket: `your-bucket-name` in `ap-southeast-3`
Enable Static website hosting -> Index document: `index.html`
Disable Block all public access & Add Bucket Policy for public read:
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "PublicRead",
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::your-bucket-name/*"
  }]
}
```
Upload `index.html` (make sure single extension, not `.html.html`)
Access via S3 Website Endpoint.
🧠 What I Learned
> This project taught me that Cloud Engineering is not just about coding, but about **infrastructure, deployment, and problem-solving**. Fixing a simple double extension error taught me more about how S3 resolves object keys than any tutorial.
How S3 Static Hosting works under the hood
Importance of Region selection for latency & compliance
Debugging S3 404 errors (NoSuchKey)
Simulating IoT data for frontend development before hardware integration
👩‍💻 Author
Devita Sari
📍 Bekasi, West Java, Indonesia
🌱 Aspiring Cloud Engineer | AgriTech Enthusiast | Future Japan Engineer
📧 devitasari1207@gmail.com
🔗 LinkedIn: [linkedin.com/in/devitasari] (ganti link kamu)
🌐 Portfolio: [Live Demo Link]
📄 License
MIT License - Feel free to fork and learn!
---
© 2026 Kebun Pintar Devita | Built with ❤️ on AWS Cloud | From Bekasi to Tokyo
