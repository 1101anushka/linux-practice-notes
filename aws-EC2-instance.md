# Linux + AWS EC2 Practice Notes (DevOps Journey)

## Overview
This document contains my hands-on practice of Linux commands using an AWS EC2 (Ubuntu) instance.  
I connected to the instance using SSH from my local machine (Git Bash).

---

# AWS EC2 SETUP (STEP-BY-STEP)

## Launch EC2 Instance

- Logged into AWS Console
- Navigated to **EC2 Dashboard**
- Clicked **Launch Instance**

### Configuration:
- Name: linux-practice
- AMI: Ubuntu (latest LTS)
- Instance type: t2.micro (free tier)
- Key pair: Created new `.pem` file
- Network: Allowed SSH (Port 22)

 Clicked **Launch Instance**

---

## Connect to EC2 via SSH

Moved `.pem` file to local system and used Git Bash:

```bash
chmod 400 my-key.pem
ssh -i my-key.pem ubuntu@<public-ip>
