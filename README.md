📦 AltSchool Cloud Engineering Second Semester Examination Project
🚀 Project Overview
This project is a prototype of a dynamic landing page deployed on an AWS EC2 instance. It is designed to demonstrate key DevOps and cloud deployment skills while showcasing a realistic startup idea.

👤 Developer Info
Name: Iniobong Pender-Atanaruno
Role: Lead Cloud Engineer
Project Title: The Future of AI-Powered Recycling

📣 Short Pitch
We are leveraging AI to redefine waste management through real-time object recognition, smart sorting, and optimization of recycling logistics. Our solution brings sustainability and automation into one ecosystem—empowering cities and companies to efficiently manage waste with data-driven decisions.

🧑‍💻 About Me
I am a cloud and backend engineering enthusiast with hands-on experience in server provisioning, automation with Ansible, Linux system administration, and modern frontend technologies. I hold a UI/UX certification (2022) and am proficient with HTML, CSS, Bootstrap, Apache, and Ubuntu-based deployments.

✅ Project Goals
Provision an Ubuntu server on AWS EC2.

Install and configure Apache2 web server.

Deploy a professional, animated, responsive landing page.

Enable secure HTTPs access with a self-signed SSL certificate.

Demonstrate production-level networking configuration.

🛠️ Technologies Used
AWS EC2 (Ubuntu 22.04 LTS)

Apache2

Bootstrap 5

CSS Animations

Self-Signed SSL for HTTPS

Git & GitHub for version control

📡 Public IP (Hosted Page)
Access the live page at:

👉 http://184.72.211.8



🧾 Setup Steps
1. 🖥️ Provision the Server on AWS
Created an EC2 instance using Ubuntu 22.04 LTS

Configured Security Group to allow:

Port 22 (SSH)

Port 80 (HTTP)

Port 443 (HTTPS)

Allocated and associated an Elastic IP

2. 🔧 Installed Apache Web Server
bash
Copy
Edit
sudo apt update
sudo apt install apache2 -y
Confirmed by visiting http://184.72.211.8

3. 🚀 Deployed Landing Page
Copied landing page files (HTML, CSS, JPEGs, Bootstrap) into Apache root:

bash
Copy
Edit
sudo rm -rf /var/www/html/*
sudo cp -r /path/to/landing-page/* /var/www/html/
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
Included animations via CSS and styled the layout using Bootstrap.

4. 🔒 Enabled SSL (Self-Signed Certificate)
bash
Copy
Edit
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
-keyout /etc/ssl/private/apache-selfsigned.key \
-out /etc/ssl/certs/apache-selfsigned.crt
Created a new Apache virtual host at /etc/apache2/sites-available/localhost-ssl.conf

Enabled modules and site:

bash
Copy
Edit
sudo a2enmod ssl
sudo a2ensite localhost-ssl.conf
sudo systemctl restart apache2
🖼️ Screenshot
Here’s a preview of the rendered landing page:




📁 Project Structure
bash
Copy
Edit
project-root/
│
├── index.html
├── style.css
├── /images
├── /bootstrap
├── screenshot.png
└── README.md
📚 Notes
The SSL setup is for demo/testing purposes only using a self-signed certificate.

link to my files created for the project: https://github.com/inifavour2/iniobong_card

This project does not use Node.js or a backend framework — it focuses on frontend deployment over Apache2.

