# Jenkins Backup and Restore — AWS Project

This project showcases the implementation of a fully automated Jenkins backup and restore solution using cron jobs and Bash scripting, securely integrated with AWS S3 for remote storage. A LaTeX PDF report contains all steps, code snippets, and screenshots.

<img width="1916" height="851" alt="Final" src="https://github.com/user-attachments/assets/a4714c92-1cdc-43a9-a412-45be418bd365" />


## Project Description

The goal of this project was to:

* Automate periodic backups of the Jenkins home directory.
* Upload compressed backups to Amazon S3 securely.
* Enable one-command restore functionality from S3 to Jenkins.
* Follow best practices for security, reliability, and maintainability.

### Key services and technologies used:

* Jenkins
* Amazon S3
* AWS IAM
* Linux Server (Ubuntu)
* Bash Scripting
* Cron Jobs

## Architecture Overview

* Jenkins Server hosted on EC2 or on-prem Linux machine
* IAM user created with limited S3 permissions
* Scheduled backup using `cron`
* `.tar.gz` compression of Jenkins home directory
* Upload to specific S3 bucket path
* Restore script to pull and extract backup

## Files

* 💾 SSH to Ec2 
  <img width="1577" height="246" alt="sshtobackupserver" src="https://github.com/user-attachments/assets/76d33969-3c04-4bea-8eb3-c1ac8ff15806" />

  
* ⏰ Cron Job Setup Screenshot
  <img width="973" height="111" alt="cronjob" src="https://github.com/user-attachments/assets/732d617d-5209-4ce5-971c-baa17ebff159" />

  
* ⚖️ IAM Policy Permissions
  <img width="1125" height="672" alt="s3-policy" src="https://github.com/user-attachments/assets/d135cc89-092e-4507-9a4a-b6a8d79fa7e3" />

* 📂 S3 Bucket Backup View
  <img width="1917" height="542" alt="s3bucketobjectsnap" src="https://github.com/user-attachments/assets/1de0cadf-88df-45f6-bd29-a5b9e17e47b3" />

* 🔢 Jenkins Restore Success
  <img width="1457" height="111" alt="downloadbackupfile" src="https://github.com/user-attachments/assets/af596e85-b879-45f2-98e1-349fd2279939" />

* ✍️ Backup and Upload Script Code
  <img width="1452" height="733" alt="uploadscript" src="https://github.com/user-attachments/assets/0010f9ce-f551-4021-aedb-90b135acf8e9" />

* ✍️ Restore Code
  <img width="1643" height="668" alt="copingandunziponbackup" src="https://github.com/user-attachments/assets/825c646c-9a24-4ddd-9e82-ab02560cd3cb" />


## Conclusion

* **Fully Automated Solution**: Jenkins backup and restore are now handled automatically without manual intervention.
* **Cloud Storage Integration**: Secure and reliable storage using Amazon S3.
* **IAM Best Practices**: Least privilege access configured for backup and restore scripts.
* **Efficient Compression**: Timestamped `.tar.gz` backups ensure organized storage and reduced size.
* **Cleanup Strategy**: Retains only the last 7 backups to save disk space.
* **Disaster Recovery**: Simple restoration process ensures rapid recovery from any Jenkins failure.

