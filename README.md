
# DropDash – Secure Temporary File Storage

Hi 👋

DropDash is a secure, cloud-based temporary file sharing web application designed to allow users to upload files, generate time-limited download links, and securely share files with optional password protection.
This repository contains the complete project documentation (PDF) detailing the system design, implementation, security, performance testing, and research work.

Due to an issue during system migration, the **original source code files were corrupted and could not be recovered**. Because of that, I’ve uploaded the **complete project documentation (PDF)**, which explains the entire system in detail — from architecture and implementation to security and performance testing.

Even without the code, **everything about how the project works is clearly explained in the report**.

---

## Why I built DropDash

While working on the project, I noticed that common file-sharing methods like email attachments and third-party tools have a lot of limitations:

* File size restrictions
* No proper control over who can access files
* Security and privacy concerns

So I built **DropDash** to make file sharing **simple, secure, and temporary**, where users have full control over their files.

---

## What DropDash does

DropDash allows users to:

* Upload files of any type or size
* Generate a **temporary download link**
* Set an **expiration time** for the file
* Optionally protect the file with a **password**

Once the file expires, it can no longer be accessed.

---

## How the system works (in simple terms)

* The **frontend** lets users upload files, choose an expiration time, and set a password if needed.
* The **backend** processes the upload, stores the file securely in the cloud, and generates a temporary download link.
* The file is stored in **Microsoft Azure**, and downloads are optimized using a CDN so they are fast and reliable.
* When someone tries to download a file, the system checks:

  * Whether the link has expired
  * Whether the correct password was entered

Only then is access granted.

The full architecture and flow diagrams are available inside the PDF.

---

## Security considerations

Security was a major focus of this project:

* All communication happens over **HTTPS**
* Files are stored securely using **Azure Blob Storage**
* Download links are generated using **time-limited secure tokens**
* Passwords are **hashed**, not stored in plain text
* Expired files are automatically invalidated

The security design is based on cloud-security research covered in the literature review section of the report.

---

## Performance and testing

I tested the application under load to make sure it works reliably:

* Handled **hundreds of concurrent users**
* Maintained stable response times
* Recorded **zero errors** during load testing
* Used Azure CDN to improve download speeds globally

Detailed performance results and screenshots are included in the report.

---

## Research & literature review

As part of the project, I also conducted a **literature review** on:

* Cloud computing fundamentals
* Secure cloud storage
* Data encryption techniques
* Access control and privacy in cloud systems

This research directly influenced how I designed the system and chose the technologies.

---

## Technologies I used

* **Frontend:** HTML, CSS, JavaScript
* **Backend:** Python, Flask
* **Cloud:** Microsoft Azure

  * Blob Storage
  * Table Storage
  * CDN
  * App Service
  * Azure Functions
* **Security:** HTTPS, secure access tokens, password hashing
* **Tools:** Git, Visual Studio Code

---

## What’s in the PDF

The attached PDF contains:

* Complete system architecture
* Backend and frontend logic explanation
* Azure setup and configuration
* Security implementation details
* Load testing and performance analysis
* UI screenshots
* Literature review and references

If you want to understand the project fully, **the PDF covers everything**.

---

## Final note

Even though the source code is not available, this project reflects my **hands-on experience with backend development, cloud services, security, and system design**.

If you’d like to discuss the project or have any questions, feel free to reach out.

📧 Email: shaikirshad4771@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/irshad-shaik-b42791202
**– Shaik Irshad**

