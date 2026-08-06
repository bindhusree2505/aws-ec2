# Linux Application Hosting

## Introduction

Linux Application Hosting is the process of deploying a website or web application on a Linux EC2 instance. In this practical, Apache HTTP Server (httpd) is used to host a static website.

## Prerequisites

- Running Linux EC2 Instance
- SSH Access using PuTTY
- WinSCP
- Apache HTTP Server (httpd)
- Static Website Files (HTML, CSS, JavaScript)

## Step 1 - Connect to the Linux EC2 Instance

Open **PuTTY**.

Enter the **Public IPv4 Address** of the Linux EC2 instance.

Log in as:

`ec2-user`

Switch to the root user.

```bash
sudo su
```

## Step 2 - Update the System

```bash
yum update -y
```

This updates all installed packages.

## Step 3 - Install Apache HTTP Server

```bash
yum install httpd -y
```

## Step 4 - Start and Enable Apache

Start Apache.

```bash
systemctl start httpd
```

Enable Apache to start automatically after every reboot.

```bash
systemctl enable httpd
```

Verify the service status.

```bash
systemctl status httpd
```

## Step 5 - Navigate to the Web Directory

Move to the default Apache web directory.

```bash
cd /var/www/html
```

Check the existing files.

```bash
ls
```

Remove the default files if required.

```bash
rm -rf *
```

## Step 6 - Change Directory Permission

Provide full permission to the web directory.

```bash
chmod -R 777 /var/www/html/
```

This allows website files to be copied into the directory.

## Step 7 - Upload Website Files using WinSCP

Open **WinSCP**.

Connect using:

- Host Name : Public IPv4 Address
- User Name : ec2-user
- Private Key : .ppk file
- Protocol : SCP

Navigate to:

```text
/var/www/html
```

Drag and drop your website files into this folder.

## Step 8 - Restart Apache Service

After uploading the files, restart Apache.

```bash
systemctl restart httpd
```

Verify the service.

```bash
systemctl status httpd
```

## Step 9 - Access the Website

Open a web browser.

Enter:

```text
http://<Public-IP>
```

If the Security Group allows **HTTP (Port 80)**, the website will be displayed successfully.

## Troubleshooting

If the website is not accessible, check the following:

- EC2 Instance is running.
- Apache service is running.
- HTTP (Port 80) is allowed in the Security Group.
- Website files are uploaded to `/var/www/html`.
- Directory permissions are configured correctly.

## Conclusion

The Linux application was successfully hosted on an AWS EC2 instance using Apache HTTP Server (httpd). The website is now accessible through the instance's Public IPv4 Address.

---

# Screenshots

- Linux Login using PuTTY
- Apache Installation
- Apache Service Status
- WinSCP Connection
- Website Files in `/var/www/html`
- Website Output using Public IP
