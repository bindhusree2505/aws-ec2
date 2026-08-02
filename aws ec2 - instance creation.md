# Windows EC2 Server Creation

## Introduction

Windows EC2 is a virtual server provided by Amazon Web Services (AWS). It allows users to run Windows-based applications without purchasing physical hardware.

## Prerequisites

- AWS Account
- EC2 Dashboard Access
- Key Pair (.pem)
- Internet Connection

## Step 1 - Launch Instance

Open the AWS Management Console.

Go to **EC2 Dashboard** and click **Launch Instance**.

## Step 2 - Configure Instance Name

**Example:**

`Windows-Server`

## Step 3 - Choose Amazon Machine Image (AMI)

**Select:**

- Microsoft Windows Server 2022 Base (64-bit)

The AMI contains the operating system required to launch the server.

## Step 4 - Select Instance Type

**Choose:**

`t3.micro`

This instance type is suitable for learning purposes.

## Step 5 - Create a Key Pair

Create a new RSA Key Pair.

Download the private key (.pem) and keep it in a safe location. This file is required to retrieve the Windows administrator password.

## Step 6 - Configure Network Settings

Allow the following inbound rules:

- RDP (3389)
- HTTP (80)

## Step 7 - Configure Storage

Allocate **30 GB** storage.

## Step 8 - Launch Instance

Review the configuration and click **Launch Instance**.

Wait until the instance status becomes **Running**.

---

# Accessing the Windows Server

## Step 1

Select the running EC2 instance.

Click **Connect**.

Choose the **RDP Client** option.

## Step 2

Download the **Remote Desktop File** if required.

Copy the **Public DNS** or **Public IP Address**.

Open **Remote Desktop Connection (RDP)** on your Windows computer.

Paste the Public DNS or Public IP and click **Connect**.

## Step 3

The default username is:

`Administrator`

To get the password:

- Click **Get Windows Password**
- Upload the downloaded **.pem** key file
- Click **Decrypt Password**
- Copy the generated password

## Step 4

Enter the username and decrypted password.

Click **OK**.

The Windows EC2 desktop will open successfully.

## Conclusion

The Windows EC2 server has been created successfully and is ready for software installation or application hosting.

# Screenshots

## Launch Instance
<img width="1366" height="687" alt="Screenshot 2026-08-02 171916" src="https://github.com/user-attachments/assets/9035f2bf-5306-4a99-a6f7-9c686700e00e" />
<img width="1366" height="683" alt="Screenshot 2026-08-02 171949" src="https://github.com/user-attachments/assets/4b989ff5-533e-4d6d-95f0-e8fc478385e8" />
<img width="1366" height="691" alt="Screenshot 2026-08-02 170056" src="https://github.com/user-attachments/assets/376a559e-b1a5-402c-b540-145fc83c8601" />
<img width="1366" height="683" alt="Screenshot 2026-08-02 172007" src="https://github.com/user-attachments/assets/3b7912ea-8c0c-4eec-8214-511913ef8ef6" />







