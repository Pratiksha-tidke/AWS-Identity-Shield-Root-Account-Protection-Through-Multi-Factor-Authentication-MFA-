# AWS Identity Shield : Root Account Protection Through Multi Factor Authentication(MFA)


 ## Table of Contents

- [ Project Overview](#1-project-overview)
- [ Objectives](#2-project-objectives)
- [ Introduction to AWS MFA](#3-introduction-to-aws-mfa)
- [ Tools and Technologies](#5-tools-and-technologies)
- [ Prerequisites](#6-prerequisites)
- [ AWS MFA Architecture](#7-aws-mfa-architecture)
- [ Step-by-Step Implementation](#8-step-by-step-implementation)
- [ Practical Screenshots](#9-practical-screenshots)
- [ Testing and Validation](#10-testing-and-validation)
- [ Security Benefits](#11-security-benefits)
- [ Challenges and Solutions](#12-challenges-and-solutions)
- [ Security Best Practices](#13-security-best-practices)
- [ Future Scope](#14-future-scope)
- [ Learning Outcomes](#15-learning-outcomes)


  ---

- ##  Introduction to AWS MFA
Multi-Factor Authentication (MFA) is a security mechanism that requires users to verify their identity using two or more authentication factors before accessing an account.In Amazon Web Services (AWS), MFA adds an extra layer of protection beyond a traditional password. It helps reduce the risk of unauthorized access, even if an account password is stolen, exposed, or compromised.AWS supports multiple MFA methods, including virtual authenticator applications, hardware MFA devices, security keys, and passkeys. A virtual authenticator generates Time-Based One-Time Passwords (TOTP) that change periodically and provide additional login verification.

### Why MFA Is Important

**Stronger Account Security:** Adds another verification step beyond passwords.
**Protection Against Credential Theft:** Makes password-only account compromise less likely to result in access.
**Privileged Account Protection:** Helps secure sensitive identities, especially the AWS root user.
**Reduced Security Risks:** Makes unauthorized sign-in more difficult.
**Improved Identity Verification:** Confirms access using an additional authentication factor.


  - ##  Project Overview

AWS Identity Shield is a hands-on cloud security project focused on strengthening AWS account protection through Multi-Factor Authentication (MFA).
It demonstrates how an additional authentication layer helps protect cloud identities, reduces the risk of unauthorized access, and improves password-based security.The project covers virtual MFA device configuration, QR code scanning, TOTP verification, and login validation, highlighting the importance of identity protection, secure authentication, and cloud security best practices.

- ##  Objectives

The main objective of **AWS Identity Shield** is to strengthen AWS account security through **Multi-Factor Authentication (MFA)**.

- **Authentication Security:** Understand MFA and the risks of password-only authentication.
- **AWS IAM:** Explore identity management, access permissions, and root account security.
- **MFA Implementation:** Configure a virtual MFA device using QR code scanning and TOTP verification.
- **Testing & Validation:** Verify MFA registration, test secure sign-in, and document the results.

- ##  Technical Environment & Security Standards

### 1. Cloud Environment
- **Cloud Platform:** Amazon Web Services (AWS)
- **Target Identity:** AWS Account Root User
- **Identity Management Service:** AWS Identity and Access Management (IAM)

### 2. Authentication Configuration
- **Authentication Method:** Multi-Factor Authentication (MFA)
- **Authentication Protocol:** RFC 6238 – Time-Based One-Time Password (TOTP)
- **MFA Device:** Virtual MFA Device
- **Authenticator Application:** Google Authenticator (Android), if used in this lab

### 3. Security Frameworks & References
- **CIS AWS Foundations Benchmark:** Guidance for enabling MFA on the AWS root user.
- **AWS Well-Architected Framework:** Security Pillar – SEC 02, Protect identities.
- **NIST SP 800-63B:** Digital identity and authentication guidance.

### 4. Security Objective
To strengthen AWS root account protection through **MFA implementation**, secure identity verification, and authentication best practices.

----

## 6. Tools and Technologies

- ### Tools

| Sr. No. | Tool Name | Purpose |
| :---: | :--- | :--- |
| 1 | **AWS Management Console** | Configure AWS account security settings. |
| 2 | **Google Authenticator** | Generate temporary MFA verification codes. |
| 3 | **Google Chrome** | Access the AWS Management Console. |
| 4 | **GitHub** | Store and showcase project documentation. |
| 5 | **Visual Studio Code** | Create and edit project documentation. |

- ### Technologies

| Sr. No. | Technology | Purpose |
| :---: | :--- | :--- |
| 1 | **Amazon Web Services (AWS)** | Cloud computing platform. |
| 2 | **Identity and Access Management (IAM)** | Manage identities and access permissions. |
| 3 | **Multi-Factor Authentication (MFA)** | Add an additional authentication layer. |
| 4 | **Time-Based One-Time Password (TOTP)** | Generate temporary verification codes. |
| 5 | **Cloud Security** | Protect cloud accounts and resources. |
| 6 | **Authentication and Access Control** | Verify identities and manage access. |
| 7 | **Virtual MFA** | Provide a software-based authentication factor. |

-----

## AWS MFA Architecture

An AWS MFA (Multi-Factor Authentication) Architecture is a security framework managed through AWS Identity and Access Management (IAM) that requires users to provide two or more distinct forms of identification before they can log into the AWS cloud environment.

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/9e791d67-d8e1-47a3-8a51-78c92c67e74d" />
                                           
## MFA Step-by-Step Implementation


The AWS Root User is the original account owner identity created when an AWS account is registered. It has full access to the AWS account and can perform important account-level operations.
- **Root User:** Select this option to sign in using the email address associated with the original AWS account owner.
  
<img width="1127" height="567" alt="1" src="https://github.com/user-attachments/assets/e3ba5793-6f0c-4fc7-be79-0b072216e489" />
                                         
Entered the AWS root account password to complete the initial identity verification and establish the primary authentication factor.

<img width="1340" height="692" alt="2" src="https://github.com/user-attachments/assets/baf72f31-6124-471c-a7bb-a7c56d487c78" />

Accessed the AWS Console service search and located Identity and Access Management (IAM) to review account identity settings and security configurations.

<img width="1347" height="673" alt="14" src="https://github.com/user-attachments/assets/b70a3ea2-d99b-4e19-8cc4-947b8f261a33" />

                                         
IAM Dashboard is the main overview page of AWS Identity and Access Management (IAM). It helps you manage and monitor identities, permissions, and account security settings in AWS.
- Users – Create and manage IAM users, - User Groups – Organize users with similar permissions, - Roles – Create roles that AWS services or users can assume, - Policies – Define what actions are allowed or denied, - Access Management – Control who can access AWS resources, - Security Recommendations – Review security guidance, such as enabling MFA.

<img width="1366" height="669" alt="3" src="https://github.com/user-attachments/assets/47a39858-9fda-4ab5-8f54-d548fef7aebe" />
                                         
Initiated the MFA enrollment process by selecting the device type and assigning a unique identifier in the MFA Device Name field.

Reviewed the available Multi-Factor Authentication (MFA) methods in the AWS enrollment console and selected Authenticator App to configure a virtual MFA device for the AWS root account.

### Available MFA options:
1. **Passkey or security key:** Uses biometrics, a device screen lock, or a FIDO2 security key.
2. **Authenticator app:** Generates time-based one-time passwords (TOTP) for account verification.
3. **Hardware TOTP token:** Generates authentication codes using a physical security device.
   

  <img width="1356" height="678" alt="4" src="https://github.com/user-attachments/assets/06fbc282-dab9-493e-8a84-4cd870095c97" />


You are prompted to choose the type of MFA hardware or virtual device you want to add to your account.   
**Passkey or security key** – Uses biometrics (fingerprint, face, or screen lock) or a physical FIDO2 security key. AWS recommends this as it provides the highest level of protection against phishing.  
**Authenticator app** – Uses a code generated by a mobile app (like Google Authenticator, Microsoft Authenticator, or Authy).  
 **Hardware TOTP token** – Uses a physical hardware token that generates time-based codes.   

<img width="1348" height="674" alt="5" src="https://github.com/user-attachments/assets/2c716789-ce80-4d61-87d4-d5d4ea8cbb80" />

Clicked the Next button to proceed with the Authenticator App MFA configuration process.

<img width="1350" height="675" alt="6" src="https://github.com/user-attachments/assets/e1987a78-d174-4f91-83b5-584e766802bc" />

