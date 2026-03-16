AWS S3 Security Lab

### Secure Cloud Storage Using Encryption, Access Control and Versioning

This hands-on lab demonstrates how to **securely configure an Amazon S3 bucket in AWS** by applying essential **cloud storage security best practices**.

Amazon S3 is widely used to store:

* application files
* backups
* logs
* images and documents

However, **misconfigured S3 buckets are one of the most common causes of cloud security breaches**.

In this lab, we learn how to **protect S3 storage using public access restrictions, encryption, and versioning**.

This lab shows step by step how a Cloud or DevSecOps engineer can **secure sensitive data stored in AWS**.

---

# 🧠 What You Will Learn

This lab teaches the fundamental **security mechanisms used to protect cloud storage**.

| Concept                | Explanation                                           |
| ---------------------- | ----------------------------------------------------- |
| S3 Bucket              | Container used to store objects (files) in AWS        |
| Block Public Access    | Prevents accidental exposure of data to the internet  |
| Versioning             | Keeps previous versions of files for recovery         |
| SSE-KMS Encryption     | Encrypts stored data using AWS Key Management Service |
| Access Control         | Ensures only authorized users can upload objects      |
| Encryption Enforcement | Rejects uploads that are not encrypted                |

These practices are commonly implemented by **Cloud Security Engineers and DevSecOps teams**.

---

# 🏗 Lab Architecture

The security model implemented in this lab:

```
User / Application
        ↓
   Secure S3 Bucket
        ↓
Block Public Access Enabled
        ↓
Server-Side Encryption (SSE-KMS)
        ↓
Versioning Enabled
        ↓
Encrypted Object Storage
```

This ensures that **all stored data remains protected and recoverable**.

---

# ⚙️ Lab Steps

## Step 1 — Create an S3 Bucket

First, create a new **Amazon S3 bucket**.

The bucket is the **storage container** where all objects will be stored.

Example configuration:

```
Bucket Name: secure-storage-lab
Region: AWS Region of your choice
```

This bucket will serve as the **secure storage location for application data**.

---

# 🚫 Step 2 — Block Public Access

Next, enable **Block Public Access**.

This setting prevents:

* public read access
* public write access
* accidental exposure of files

Public S3 buckets are a **common cause of data leaks**, so this step is essential.

---

# 🔎 Step 3 — Verify Bucket is Not Public

After enabling public access restrictions, verify that the bucket status shows:

```
Not Public
```

This confirms that **no external user on the internet can access the bucket**.

This verification step ensures the **storage is properly secured**.

---

# 📂 Step 4 — Enable Versioning

Enable **Versioning** on the bucket.

Versioning keeps **multiple versions of the same object**.

Example:

```
file_v1
file_v2
file_v3
```

Benefits:

* recover deleted files
* restore previous versions
* protect against accidental modifications

Versioning is a **best practice for data protection and recovery**.

---

# 🔐 Step 5 — Enable Default Encryption (SSE-KMS)

Next, enable **Default Server-Side Encryption** using **AWS KMS**.

Encryption ensures that **all objects stored in the bucket are automatically encrypted**.

Encryption protects:

* confidential data
* sensitive application files
* backups and logs

Even if storage is accessed, **data remains unreadable without the encryption key**.

---

# 📤 Step 6 — Upload an Object and Verify Encryption

Upload a file to the bucket.

After uploading, verify that the object shows:

```
Encryption: SSE-KMS
```

This confirms that **the file is encrypted at rest**.

This step demonstrates how AWS automatically **protects stored data**.

---

# ❌ Step 7 — Upload a Non-Encrypted Object (Access Denied)

Finally, attempt to upload a file **without encryption**.

Because encryption is enforced, AWS should return:

```
Access Denied
```

This proves that the bucket **rejects insecure uploads**, ensuring that **all stored data remains encrypted**.

---

# 🛡 Security Best Practices Demonstrated

This lab demonstrates several important **cloud security practices**:

✔ Blocking public access to storage
✔ Enforcing encryption using AWS KMS
✔ Protecting data using versioning
✔ Preventing insecure uploads
✔ Verifying encryption on stored objects

These practices are used in **real production cloud environments**.

---

# 🎯 Skills Demonstrated

Completing this lab shows practical knowledge of:

* Amazon S3 security configuration
* Cloud storage encryption
* Data protection best practices
* Access control enforcement
* Secure cloud architecture

These skills are valuable for roles such as:

* Cloud Security Engineer
* AWS Cloud Engineer
* DevSecOps Engineer
* Cybersecurity Engineer

---

# 🚀 Why This Lab Matters

Many real-world cloud security incidents occur because of **misconfigured storage buckets**.

Understanding how to secure S3 using **access control, encryption, and versioning** is therefore a **critical cloud security skill**.

This lab demonstrates the ability to **protect sensitive data in the AWS cloud**.

---
