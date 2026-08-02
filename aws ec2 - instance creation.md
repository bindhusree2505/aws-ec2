# Windows & Linux EC2 Server Creation

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

## Launch Instance - windows
<img width="1366" height="687" alt="Screenshot 2026-08-02 171916" src="https://github.com/user-attachments/assets/9035f2bf-5306-4a99-a6f7-9c686700e00e" />
<img width="1366" height="683" alt="Screenshot 2026-08-02 171949" src="https://github.com/user-attachments/assets/4b989ff5-533e-4d6d-95f0-e8fc478385e8" />
<img width="1366" height="691" alt="Screenshot 2026-08-02 170056" src="https://github.com/user-attachments/assets/376a559e-b1a5-402c-b540-145fc83c8601" />
<img width="1366" height="683" alt="Screenshot 2026-08-02 172007" src="https://github.com/user-attachments/assets/3b7912ea-8c0c-4eec-8214-511913ef8ef6" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 174141" src="https://github.com/user-attachments/assets/91e86fae-95c7-4307-ac4b-7342e11e072d" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 174202" src="https://github.com/user-attachments/assets/84bb4980-2cba-4182-93c7-51dfe40cdc1b" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 174309" src="https://github.com/user-attachments/assets/4cbb046e-8a21-4392-b522-fe1e15be98b0" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 174322" src="https://github.com/user-attachments/assets/b4a8ac3a-90e7-4614-8785-27369ccab926" />

# Linux EC2 Server Creation

## Introduction

Linux EC2 is a virtual server provided by Amazon Web Services (AWS). It allows users to create and manage Linux-based virtual machines for hosting applications, websites, databases, and development environments.

## Prerequisites

- AWS Account
- EC2 Dashboard Access
- Key Pair (.ppk)
- Internet Connection

## Step 1 - Launch Instance

Open the AWS Management Console.

Go to **EC2 Dashboard** and click **Launch Instance**.

## Step 2 - Configure Instance Name

**Example:**

`Linux-Server`

## Step 3 - Choose Amazon Machine Image (AMI)

**Select:**

- Amazon Linux 2023 AMI (64-bit)

The AMI contains the operating system required to launch the server.

## Step 4 - Select Instance Type

**Choose:**

`t3.micro`

This instance type is suitable for learning purposes and Free Tier usage.

## Step 5 - Create a Key Pair

Create a new RSA Key Pair.

Download the private key (.pem) and store it safely.

If you are using PuTTY, convert the `.pem` file to `.ppk` using **PuTTYgen** before connecting to the instance.

## Step 6 - Configure Network Settings

Allow the following inbound rules:

- SSH (22)
- HTTP (80)

## Step 7 - Configure Storage

Allocate **8 GB** storage.

## Step 8 - Launch Instance

Review the configuration and click **Launch Instance**.

Wait until the instance status becomes **Running**.

---

## Connecting to the Linux Server

### Step 1

Select the running EC2 instance.

Copy the **Public IPv4 Address**.

### Step 2

Open **PuTTY** (or any SSH client).

Load the generated `.ppk` file in PuTTY.

### Step 3

Enter the following details:

**Host Name:**

`ec2-user@<Public-IP>`

**Port:**

`22`

**Connection Type:**

`SSH`

Click **Open**.

### Step 4

When prompted, click **Accept** to trust the server.

The terminal window will open successfully.

### Step 5

Log in using the default user:

`ec2-user`

If the connection is successful, the Linux terminal will open and you can start managing the instance using Linux commands.

Example:

```bash
sudo su
```

The Linux EC2 instance is now ready for software installation and application hosting.

## Conclusion

The Linux EC2 server was successfully created and connected using SSH. The instance is now ready for software installation, configuration, and application deployment.

# Screenshots

## Launch Instance - Linux

<img width="1366" height="683" alt="Screenshot 2026-08-02 180116" src="https://github.com/user-attachments/assets/570407a5-1c1f-4fab-9247-38f53a597a4b" />
<img width="1366" height="646" alt="Screenshot 2026-08-02 180125" src="https://github.com/user-attachments/assets/e2c95fb5-8e20-4b70-8c00-093e25b10151" />
<img width="1366" height="683" alt="Screenshot 2026-08-02 180052" src="https://github.com/user-attachments/assets/10e938ba-e882-436b-ac2f-4726c1ed38fc" />
<img width="1366" height="687" alt="Screenshot 2026-08-02 180150" src="https://github.com/user-attachments/assets/5bfa834d-13c4-45a2-8549-035201b0edd8" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 181250" src="https://github.com/user-attachments/assets/fe56bf4a-339c-47ef-a72d-17f36cc7b71b" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 181312" src="https://github.com/user-attachments/assets/5909156a-6617-4944-90a4-c4678cc1a8a1" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 181352" src="https://github.com/user-attachments/assets/59f58caa-ff14-4f4b-b344-bc845180582a" />
<img width="1366" height="720" alt="Screenshot 2026-08-02 181436" src="https://github.com/user-attachments/assets/104b26ea-9e78-4460-af75-6e1efc188149" />




















