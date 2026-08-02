# Windows Application Hosting

## Introduction

Windows Application Hosting is the process of deploying a website or web application on a Windows EC2 instance. In this practical, Internet Information Services (IIS) is used as the web server to host a static website.

## Prerequisites

- Running Windows EC2 Instance
- RDP Access
- IIS (Internet Information Services)
- Static Website Files (HTML, CSS, JavaScript)

## Step 1 - Connect to the Windows EC2 Instance

Open **Remote Desktop Connection (RDP)**.

Enter the **Public IPv4 Address** of the Windows EC2 instance.

Log in using:

- Username: `Administrator`
- Password: Decrypted password from AWS

## Step 2 - Open Server Manager

After logging in, open **Server Manager**.

Click **Add Roles and Features**.

## Step 3 - Install IIS

Choose:

- Role-based or feature-based installation
- Select the current server
- Enable **Web Server (IIS)**

Click **Next** and complete the installation.

Wait until the installation is completed successfully.

## Step 4 - Verify IIS Installation

Open a web browser inside the Windows server.

Enter:

`http://localhost`

The default IIS welcome page should be displayed.

## Step 5 - Host the Website

Open the following location:

`C:\inetpub\wwwroot`

Delete the default IIS files if required.

Copy your website files into the **wwwroot** folder.

## Step 6 - Access the Website

Open a browser on your local computer.

Enter:

`http://<Public-IP>`

If the Security Group allows **HTTP (Port 80)**, the hosted website will be displayed successfully.

## Troubleshooting

If the website is not accessible, verify the following:

- EC2 Instance is running
- HTTP (Port 80) is allowed in the Security Group
- IIS service is installed and running
- Website files are copied to the **wwwroot** folder

## Conclusion

The Windows application was successfully hosted on an AWS EC2 instance using Internet Information Services (IIS). The website can now be accessed through the instance's Public IPv4 Address.

---

# Screenshots

<img width="1366" height="720" alt="Screenshot 2026-08-02 174202" src="https://github.com/user-attachments/assets/cb5e10e6-d622-47fb-b4dc-3fcb4f93ba93" />
<img width="1000" height="420" alt="image" src="https://github.com/user-attachments/assets/3876aece-905c-44ad-8de9-4f809ee8bfab" />
<img width="1024" height="491" alt="image" src="https://github.com/user-attachments/assets/51661ab4-7a09-4af4-bdb0-3678e0679b03" />
<img width="1024" height="448" alt="image" src="https://github.com/user-attachments/assets/7ff95d75-a707-4d14-b7b5-54994d080a49" />
<img width="1024" height="447" alt="image" src="https://github.com/user-attachments/assets/27ce7586-56b4-4278-89ac-a7e739d5b34e" />
<img width="927" height="562" alt="image" src="https://github.com/user-attachments/assets/4bc7749b-74d5-4669-8800-39e3fc46e1b2" />
<img width="421" height="419" alt="image" src="https://github.com/user-attachments/assets/f243b491-f620-4a42-8d86-6a3a3c1206d9" />
<img width="788" height="564" alt="image" src="https://github.com/user-attachments/assets/beffcb04-ae76-4b0d-be02-668b60645241" />
<img width="787" height="560" alt="image" src="https://github.com/user-attachments/assets/bd79b7be-10af-461a-bc8d-3abb1c56e049" />
<img width="787" height="562" alt="image" src="https://github.com/user-attachments/assets/4f35cdb7-f9a6-4113-8038-334ee9c0467d" />
<img width="1024" height="445" alt="image" src="https://github.com/user-attachments/assets/10af23ac-c45c-42c8-b4f4-9eebb2849520" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 191601" src="https://github.com/user-attachments/assets/cd409b57-04c3-4dff-8903-6adb3d30a3ef" />










