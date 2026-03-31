Linux Volume Management & AWS EBS (DevOps Notes)

Overview

Volume management is essential in DevOps for:
- Managing storage
- Scaling disks dynamically
- Handling production data

This includes:
- Linux volumes
- AWS EBS
- LVM (Logical Volume Manager)
  

1. Linux Storage Basics

Types of Storage

- Physical Volume (PV) → Actual disk (e.g., /dev/xvdf)
- Volume Group (VG) → Collection of disks
- Logical Volume (LV) → Usable partition



2. Physical vs Logical vs Volume Group

| Type | Meaning |
|------|--------|
| Physical Volume (PV) | Real disk |
| Volume Group (VG) | Pool of disks |
| Logical Volume (LV) | Virtual partition |



3. Mounting Volumes in Linux

Step 1: Check disks
lsblk
👉 Step 2: Create filesystem
sudo mkfs.ext4 /dev/xvdf
👉 Step 3: Create mount directory
sudo mkdir /mnt/data
👉 Step 4: Mount volume
sudo mount /dev/xvdf /mnt/data
👉 Step 5: Verify
df -h


4. AWS EBS (Elastic Block Store)

👉 What is EBS?
Block storage in AWS
Attached to EC2 instances
Used for persistent storage
👉 Steps to Attach EBS
Go to EC2 → Volumes
Create Volume
Attach to instance
Connect via SSH
Check using:
lsblk


5. Managing EBS on EC2
   
Format disk
sudo mkfs.ext4 /dev/xvdf
Mount disk
sudo mount /dev/xvdf /mnt/data
Auto-mount on reboot

Edit fstab:

sudo nano /etc/fstab

Add:

/dev/xvdf /mnt/data ext4 defaults 0 0

6. LVM (Logical Volume Manager)
   
👉 Why LVM?
Resize storage dynamically
Combine multiple disks
Flexible partitioning
🔧 LVM Setup Steps
Step 1: Create Physical Volume
sudo pvcreate /dev/xvdf
Step 2: Create Volume Group
sudo vgcreate my_vg /dev/xvdf
Step 3: Create Logical Volume
sudo lvcreate -L 5G -n my_lv my_vg
Step 4: Format Logical Volume
sudo mkfs.ext4 /dev/my_vg/my_lv
Step 5: Mount Logical Volume
sudo mount /dev/my_vg/my_lv /mnt/data


7. Resize Logical Volume
Extend volume
sudo lvextend -L +2G /dev/my_vg/my_lv
Resize filesystem
sudo resize2fs /dev/my_vg/my_lv


8. Using LVM with AWS EBS
Real DevOps Scenario
Attach new EBS volume
Add to existing VG
Extend LV without downtime
Steps:
sudo pvcreate /dev/xvdg
sudo vgextend my_vg /dev/xvdg
sudo lvextend -L +5G /dev/my_vg/my_lv
sudo resize2fs /dev/my_vg/my_lv


Key Learnings
Understood Linux storage architecture
Learned AWS EBS usage
Practiced mounting volumes
Implemented LVM for dynamic storage
Learned real-world scaling techniques
