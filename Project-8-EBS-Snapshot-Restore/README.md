# Project 8 – Create EBS Snapshots and Restore an EC2 Instance

## 📌 Project Overview

This project demonstrates how to back up and restore data using **Amazon Elastic Block Store (EBS) Snapshots**. An EC2 instance was launched, sample data was created on its root EBS volume, a snapshot was taken, and the snapshot was restored by creating a new EBS volume. The restored volume was attached to the instance, mounted, and verified. Finally, all AWS resources were cleaned up to prevent unnecessary charges.

---

## 🎯 Objectives

- Launch an Amazon EC2 instance
- Identify the root EBS volume
- Create sample data on the EBS volume
- Create an EBS Snapshot
- Restore the snapshot by creating a new EBS volume
- Attach and mount the restored volume
- Verify the restored data
- Clean up AWS resources

---

## 🛠️ AWS Services Used

- Amazon EC2
- Amazon EBS
- Amazon EBS Snapshots
- AWS CloudShell / EC2 Instance Connect

---

## 📐 Architecture

```
             +----------------------+
             |    Amazon EC2        |
             | (Amazon Linux 2023)  |
             +----------+-----------+
                        |
                        |
                Root EBS Volume
                        |
                 Create Snapshot
                        |
                        ▼
                Amazon EBS Snapshot
                        |
             Create Volume from Snapshot
                        |
                        ▼
             Restored EBS Volume
                        |
             Attach to EC2 Instance
                        |
                        ▼
         Mount Volume & Verify Data
```

---

## 🚀 Implementation Steps

### Step 1 – Launch EC2 Instance

- Launched an EC2 instance
- Amazon Linux 2023 AMI
- Instance Type: t3.micro

**Screenshot**

![Step 1](screenshots/Step-1-EC2-Instance-Running.png)

---

### Step 2 – Identify the Root EBS Volume

- Opened the **Storage** tab
- Identified the attached root EBS volume

**Screenshot**

![Step 2](screenshots/Step-2-EBS-Root-Volume-Attached.png)

---

### Step 3 – Create Test Data

Connected to the EC2 instance and created sample data.

```bash
sudo su
cd /

mkdir ebs-test

echo "EBS Snapshot Restore Test - Project 8" > /ebs-test/testfile.txt

cat /ebs-test/testfile.txt
```

**Screenshot**

![Step 3](screenshots/Step-3-Test-Data-Created.png)

---

### Step 4 – Create EBS Snapshot

- Opened the EBS Volume
- Selected **Create Snapshot**
- Waited until the snapshot status became **Completed**

**Screenshot**

![Step 4](screenshots/Step-4-EBS-Snapshot-Created.png)

---

### Step 5 – Create Volume from Snapshot

- Created a new EBS volume using the snapshot
- Selected the same Availability Zone

**Screenshot**

![Step 5](screenshots/Step-5-Volume-Created-From-Snapshot.png)

---

### Step 6 – Attach Restored Volume

- Attached the restored volume to the EC2 instance
- Device Name: `/dev/sdf`

**Screenshot**

![Step 6](screenshots/Step-6-Restored-Volume-Attached.png)

---

### Step 7 – Mount and Verify Restored Data

Listed block devices.

```bash
lsblk
```

Created mount directory.

```bash
sudo mkdir /mnt/restored
```

Mounted the restored volume using the **nouuid** option.

```bash
sudo mount -o nouuid /dev/nvme1n1p1 /mnt/restored
```

Verified restored data.

```bash
ls /mnt/restored/ebs-test

cat /mnt/restored/ebs-test/testfile.txt
```

**Output**

```
EBS Snapshot Restore Test - Project 8
```

**Screenshot**

![Step 7](screenshots/Step-7-Restored-Data-Verified.png)

---

### Step 8 – Cleanup

Unmount the restored volume.

```bash
sudo umount /mnt/restored
```

Verify.

```bash
lsblk
```

Delete resources in the following order:

- Detach restored volume
- Delete restored volume
- Delete snapshot
- Terminate EC2 instance

**Screenshots**

Unmount Volume

![Step 8-1](screenshots/Step-8-1-Restored-Volume-Unmounted.png)

Detach Volume

![Step 8-2](screenshots/Step-8-2-Restored-Volume-Detached.png)

Delete Volume

![Step 8-3](screenshots/Step-8-3-Restored-Volume-Deleted.png)

Delete Snapshot

![Step 8-4](screenshots/Step-8-4-Snapshot-Deleted.png)

Terminate EC2

![Step 8-5](screenshots/Step-8-5-EC2-Instance-Terminated.png)

---

## ✅ Project Outcome

- Successfully created an Amazon EBS Snapshot
- Restored data by creating a new EBS volume
- Verified data integrity after restoration
- Learned how to resolve XFS UUID conflicts using the **nouuid** mount option
- Successfully cleaned up all AWS resources

---

## 📚 Key Learnings

- Amazon EBS provides persistent block storage for EC2.
- Snapshots are incremental backups stored in Amazon S3.
- Volumes created from snapshots retain the original filesystem.
- XFS volumes restored from snapshots may require the **nouuid** option during mounting.
- Proper cleanup helps prevent unnecessary AWS charges.

---

## 📁 Repository Structure

```
Project-8-EBS-Snapshot-Restore/
│
├── README.md
├── screenshots/
│   ├── Step-1-EC2-Instance-Running.png
│   ├── Step-2-EBS-Root-Volume-Attached.png
│   ├── Step-3-Test-Data-Created.png
│   ├── Step-4-EBS-Snapshot-Created.png
│   ├── Step-5-Volume-Created-From-Snapshot.png
│   ├── Step-6-Restored-Volume-Attached.png
│   ├── Step-7-Restored-Data-Verified.png
│   ├── Step-8-1-Restored-Volume-Unmounted.png
│   ├── Step-8-2-Restored-Volume-Detached.png
│   ├── Step-8-3-Restored-Volume-Deleted.png
│   ├── Step-8-4-Snapshot-Deleted.png
│   └── Step-8-5-EC2-Instance-Terminated.png
│
└── Report.pdf
```

---

## 👨‍💻 Author

**Sathya Murugesan**

Cloud Computing Internship Projects