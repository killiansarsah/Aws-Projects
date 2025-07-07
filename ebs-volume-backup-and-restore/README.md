# 💾 My AWS Project: Working with Amazon EBS via AWS Console 🖱️

Hello! I'm **Killian Sarsah**, and this is a hands-on project I completed as part of the **AWS re/Start** program. In this project, I used only the **AWS Management Console** (🖱️ clicking, no terminal!) to manage **Amazon Elastic Block Store (EBS)** volumes, snapshots, and EC2 storage.

> 💡 This README documents every step I took — just like a case study — with 📸 screenshot placeholders for each major action.


## 🌟 What I Achieved

✅ I created and attached a new EBS volume  
✅ I mounted it on an EC2 instance (via the Console only)  
✅ I created a snapshot of the volume  
✅ I restored a volume from the snapshot  
✅ I reattached and verified the restored volume using the Console


## 🛠️ Services Used

- ✅ Amazon EC2
- ✅ Amazon Elastic Block Store (EBS)
- ✅ AWS Management Console
- ✅ EBS Snapshots (stored in Amazon S3)
- ✅ EC2 Instance Connect (Web UI only — no CLI)



## 🗺️ Architecture Overview

📌 This lab involved a **Lab EC2 Instance**, an **attached EBS volume**, and a **snapshot** that I used to create and restore a new volume.

📸 `![Architecture Overview](images/archite)`



## 🚀 Step-by-Step Lab Walkthrough (No Terminal Used)



### 🧱 Step 1: Creating a New EBS Volume

1. I logged into the **AWS Console** and opened the **EC2 Dashboard**
2. From the left menu, I chose **Elastic Block Store → Volumes**
3. I clicked **Create Volume** and entered the following:
   - **Volume type**: General Purpose SSD (gp2)
   - **Size**: 1 GiB
   - **Availability Zone**: Same as my Lab instance (e.g., `us-west-2a`)
   - **Tag**: `Name = My Volume`
4. I clicked **Create Volume** and confirmed it appeared with **state = Available**

📸 <img width="477" alt="image" src="https://github.com/user-attachments/assets/878aacf9-2f8d-48b3-a47e-2c71067fbcbf" />



### 🔗 Step 2: Attaching the Volume to an EC2 Instance

1. I selected the volume I just created: `My Volume`
2. Clicked **Actions → Attach Volume**
3. Selected the pre-launched **Lab EC2 Instance**
4. For **Device Name**, I selected `/dev/sdb`
5. I clicked **Attach Volume** and saw the volume become **In-use**

📸 <img width="959" alt="image" src="https://github.com/user-attachments/assets/6313ba38-f1cb-47dd-817d-dfac839cbcaa" />


### 💻 Step 3: Connecting to EC2 Instance (No Terminal Setup Required)

1. I went to **EC2 → Instances**
2. Selected the `Lab` instance
3. Clicked **Connect**
4. On the **EC2 Instance Connect** tab, I clicked **Connect** again
5. A browser-based terminal window opened where the volume was visible after mounting via Console

📸 <img width="959" alt="image" src="https://github.com/user-attachments/assets/c6882661-58dd-4c20-afe6-488114710283" />

<img width="959" alt="image" src="https://github.com/user-attachments/assets/fdd7d218-384f-44fe-ac3d-b4f2fde65e97" />



### 📸 Step 4: Creating a Snapshot from the Volume

1. I returned to **EC2 → Volumes**
2. Selected `My Volume`
3. Clicked **Actions → Create Snapshot**
4. Added a tag: `Name = My Snapshot`
5. Clicked **Create Snapshot**
6. Then, I went to the **Snapshots** tab to check progress (status changed from **Pending** to **Completed**)

📸 <img width="959" alt="image" src="https://github.com/user-attachments/assets/f5dc5e4e-4b94-4e0f-a782-5c3ff764d488" />


### 🔁 Step 5: Creating a New Volume from the Snapshot

1. I selected `My Snapshot` under **EC2 → Snapshots**
2. Clicked **Actions → Create Volume from Snapshot**
3. Selected the **same Availability Zone** as my EC2 instance (e.g., `us-west-2a`)
4. Added a tag: `Name = Restored Volume`
5. Clicked **Create Volume**

📸 <img width="959" alt="image" src="https://github.com/user-attachments/assets/5faca4d2-c657-4173-be4c-bc680f927ca3" />


### 🔗 Step 6: Attaching the Restored Volume

1. I selected `Restored Volume` under **EC2 → Volumes**
2. Clicked **Actions → Attach Volume**
3. Selected the same **Lab EC2 instance**
4. For **Device Name**, I selected `/dev/sdc`
5. Clicked **Attach Volume**

📸 <img width="959" alt="image" src="https://github.com/user-attachments/assets/99c82b68-ccf0-4c7b-bc3b-78d9c2191749" />

![image](https://github.com/user-attachments/assets/f290c185-d530-4558-bdca-c97078d9a5ee)



### ✅ Step 7: Verifying the Restored Volume (via Console & Browser Terminal)

1. I returned to the browser terminal window via **EC2 Instance Connect**
2. Navigated to the new mount point in the file explorer panel
3. I verified that the file I previously created (`file.txt`) existed in the restored volume



## 🎯 Final Outcome

By the end of this project, I had:

✅ Created an EBS volume from scratch  
✅ Attached it to an EC2 instance using the Console  
✅ Taken a backup snapshot via the Console  
✅ Created a new volume from that snapshot  
✅ Attached and verified the restored volume using the AWS web interface


## 👨‍💻 About Me

I'm **Killian Sarsah**, a Cloud & Data enthusiast and a graduate of the **AWS re/Start** program. I'm passionate about practical infrastructure projects like this one and enjoy documenting my hands-on experience with cloud tools.

- 🔗 GitHub: [@killian25](https://github.com/killian25)  
- 💼 LinkedIn: [Your LinkedIn Here](https://linkedin.com/in/your-profile)  



## 📚 References & Credits

- [Amazon EBS Documentation](https://docs.aws.amazon.com/ebs/latest/userguide/ebs-volumes.html)
- [Amazon EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [AWS re/Start Program](https://aws.amazon.com/training/restart/)




