# AWS Identity Shield : Root Account Protection Through Multi Factor Authentication(MFA)

AWS Identity Shield is a hands-on cloud security project focused on protecting the AWS Root Account by implementing Multi-Factor Authentication (MFA). It demonstrates how an additional authentication layer, using a virtual MFA device and Time-Based One-Time Passwords (TOTP), helps prevent unauthorized access and strengthens AWS account security beyond password-based authentication.

## Table of Contents

1. [Introduction to AWS MFA](#introduction-to-aws-mfa)
   - [Why MFA Is Important](#why-mfa-is-important)
2. [Project Overview](#project-overview)
3. [Objectives](#objectives)
4. [Technical Environment & Security Standards](#technical-environment--security-standards)
   - [1. Cloud Environment](#1-cloud-environment)
   - [2. Authentication Configuration](#2-authentication-configuration)
   - [3. Security Frameworks & References](#3-security-frameworks--references)
   - [4. Security Objective](#4-security-objective)
5. [Tools and Technologies](#5-tools-and-technologies)
   - [Tools](#tools)
   - [Technologies](#technologies)
6. [AWS MFA Architecture](#aws-mfa-architecture)
7. [MFA Step-by-Step Implementation](#mfa-step-by-step-implementation)
8. [Project Purpose](#project-purpose)
9. [Disclaimer](#disclaimer)

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

*AWS Identity Shield is a hands-on cloud security project focused on strengthening AWS account protection through Multi-Factor Authentication (MFA).
It demonstrates how an additional authentication layer helps protect cloud identities, reduces the risk of unauthorized access, and improves password-based security.The project covers virtual MFA device configuration, QR code scanning, TOTP verification, and login validation, highlighting the importance of identity protection, secure authentication, and cloud security best practices.*

- ##  Objectives

*The main objective of **AWS Identity Shield** is to strengthen AWS account security through **Multi-Factor Authentication (MFA)**.*

- **Authentication Security:** Understand MFA and the risks of password-only authentication.
- **AWS IAM:** Explore identity management, access permissions, and root account security.
- **MFA Implementation:** Configure a virtual MFA device using QR code scanning and TOTP verification.
- **Testing & Validation:** Verify MFA registration, test secure sign-in, and document the results. 

- ##  Technical Environment & Security Standards

#### 1. Cloud Environment
- **Cloud Platform:** Amazon Web Services (AWS)
- **Target Identity:** AWS Account Root User
- **Identity Management Service:** AWS Identity and Access Management (IAM)

#### 2. Authentication Configuration
- **Authentication Method:** Multi-Factor Authentication (MFA)
- **Authentication Protocol:** RFC 6238 – Time-Based One-Time Password (TOTP)
- **MFA Device:** Virtual MFA Device
- **Authenticator Application:** Google Authenticator (Android), if used in this lab

#### 3. Security Frameworks & References
- **CIS AWS Foundations Benchmark:** Guidance for enabling MFA on the AWS root user.
- **AWS Well-Architected Framework:** Security Pillar – SEC 02, Protect identities.
- **NIST SP 800-63B:** Digital identity and authentication guidance.

#### 4. Security Objective
*To strengthen AWS root account protection through **MFA implementation**, secure identity verification, and authentication best practices.*

----

## 6. Tools and Technologies

- #### Tools

| Sr. No. | Tool Name | Purpose |
| :---: | :--- | :--- |
| 1 | **AWS Management Console** | Configure AWS account security settings. |
| 2 | **Google Authenticator** | Generate temporary MFA verification codes. |
| 3 | **Google Chrome** | Access the AWS Management Console. |
| 4 | **GitHub** | Store and showcase project documentation. |
| 5 | **Visual Studio Code** | Create and edit project documentation. |

- #### Technologies

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

*The AWS Root User is the original account owner identity created when an AWS account is registered. It has full access to the AWS account and can perform important account-level operations.*
*- **Root User:** Select this option to sign in using the email address associated with the original AWS account owner.*
  
<img width="1127" height="567" alt="1" src="https://github.com/user-attachments/assets/e3ba5793-6f0c-4fc7-be79-0b072216e489" />
                                         
*Entered the AWS root account password to complete the initial identity verification and establish the primary authentication factor.*

<img width="1340" height="692" alt="2" src="https://github.com/user-attachments/assets/baf72f31-6124-471c-a7bb-a7c56d487c78" />

*Accessed the AWS Console service search and located Identity and Access Management (IAM) to review account identity settings and security configurations.*

<img width="1347" height="673" alt="14" src="https://github.com/user-attachments/assets/b70a3ea2-d99b-4e19-8cc4-947b8f261a33" />

                                         
*IAM Dashboard is the main overview page of AWS Identity and Access Management (IAM). It helps you manage and monitor identities, permissions, and account security settings in AWS.*
*- Users – Create and manage IAM users, - User Groups – Organize users with similar permissions, - Roles – Create roles that AWS services or users can assume, - Policies – Define what actions are allowed or denied, - Access Management – Control who can access AWS resources, - Security Recommendations – Review security guidance, such as enabling MFA.*

<img width="1366" height="669" alt="3" src="https://github.com/user-attachments/assets/47a39858-9fda-4ab5-8f54-d548fef7aebe" />
                                         
*Initiated the MFA enrollment process by selecting the device type and assigning a unique identifier in the MFA Device Name field.*

*Reviewed the available Multi-Factor Authentication (MFA) methods in the AWS enrollment console and selected Authenticator App to configure a virtual MFA device for the AWS root account.*

### Available MFA options:
1. **Passkey or security key:** Uses biometrics, a device screen lock, or a FIDO2 security key.
2. **Authenticator app:** Generates time-based one-time passwords (TOTP) for account verification.
3. **Hardware TOTP token:** Generates authentication codes using a physical security device.
   

  <img width="1356" height="678" alt="4" src="https://github.com/user-attachments/assets/06fbc282-dab9-493e-8a84-4cd870095c97" />


*You are prompted to choose the type of MFA hardware or virtual device you want to add to your account.*
**Passkey or security key** – Uses biometrics (fingerprint, face, or screen lock) or a physical FIDO2 security key. AWS recommends this as it provides the highest level of protection against phishing.  
**Authenticator app** – Uses a code generated by a mobile app (like Google Authenticator, Microsoft Authenticator, or Authy).  
 **Hardware TOTP token** – Uses a physical hardware token that generates time-based codes.   

<img width="1348" height="674" alt="5" src="https://github.com/user-attachments/assets/2c716789-ce80-4d61-87d4-d5d4ea8cbb80" />

*Clicked the Next button to proceed with the Authenticator App MFA configuration process.*

<img width="1350" height="675" alt="6" src="https://github.com/user-attachments/assets/e1987a78-d174-4f91-83b5-584e766802bc" />

*Configured AWS IAM Multi-Factor Authentication (MFA) using an Authenticator App.*
*Added an extra layer of security using time-based OTP verification to prevent unauthorized access.*

<img width="1366" height="679" alt="7" src="https://github.com/user-attachments/assets/1df3d91f-8263-43f4-9573-280c9abbf5c2" />

*Downloaded and installed the Google Authenticator app from the official app store.*
*Opened the application to prepare for AWS MFA setup and TOTP code generation.*

<img width="1080" height="497" alt="google Authenticator app" src="https://github.com/user-attachments/assets/0b35e65b-cdba-4cd4-bd36-943901934eb4" />

*Google Authenticator app generated time-based verification codes that refreshed every 30 seconds. To complete MFA registration:*
*- Retrieved the first verification code from the app.*
*- Waited for the next 30-second interval and obtained the second code.*
*- Entered both sequential codes in the AWS enrollment console.*
*- Clicked Add MFA to complete device registration.*

<img width="634" height="550" alt="MFA" src="https://github.com/user-attachments/assets/df2257a2-c2d8-45c0-8272-cef9602e3cf1" />

*Authenticator App is a mobile application used to generate **time-based One-Time Passwords (TOTP)** for Multi-Factor Authentication (MFA).*
*In AWS IAM, it provides an additional layer of security by generating a **6-digit verification code** that changes every **30 seconds.***

<img width="1348" height="670" alt="8" src="https://github.com/user-attachments/assets/8daeaa8d-1a89-40d9-a112-cd0b172cd169" />

*Email verification is an additional security step in which a **One-Time Password (OTP) or verification code is sent to the registered email address.** The user must **enter the received code to verify their identity and complete the authentication process.***

<img width="1366" height="680" alt="10" src="https://github.com/user-attachments/assets/336b8aac-7eea-46f5-a07d-d4e3a5baf2c2" />

*Configured the virtual MFA device by scanning the AWS QR code with Google Authenticator, entering two consecutive verification codes, and clicking “Add MFA” to complete registration.*

<img width="1347" height="672" alt="11" src="https://github.com/user-attachments/assets/a0379583-3735-4d58-bf1f-68ee55c75bcd" />

*The My Security Credentials section provides access to the authentication and security settings associated with the currently signed-in AWS identity.*
- **Account Identity:** Identifies the signed-in identity as the AWS Root User.
- **Security Credentials:** Provides access to account authentication and security configuration options.
- **MFA Configuration:** Allows the Root User to manage Multi-Factor Authentication (MFA) devices.
- **Security Management:** Helps review and strengthen account authentication settings.

* The Account Details section displays basic information associated with the AWS account.*
- **AWS Account ID:** A unique 12-digit identifier assigned to the AWS account.
- **Account Name:** The name associated with the AWS account.
- **Email Address:** The registered email address linked to the AWS account.
- **Account Identity:** Helps identify the AWS account being accessed.

<img width="1366" height="684" alt="12" src="https://github.com/user-attachments/assets/ffabda77-f524-49bf-8e18-3b78dc91454b" />

*AWS Security Credentials is a section in the AWS Management Console used to manage account authentication methods, including MFA devices and access keys.*
-**MFA:** Provides an additional layer of account authentication.
- **Access Keys:** Allow programmatic access to AWS services through CLI, SDK, and APIs.
- **MFA Status:** Shows the number of MFA devices assigned to the account.
- **Access Key Status:** Displays the number of access keys created.

<img width="1347" height="679" alt="13" src="https://github.com/user-attachments/assets/157bc076-5eb1-4e6b-a07f-145f6f1fd433" />

*The AWS IAM Dashboard provides an overview of identity management, access permissions, account security recommendations, and IAM resources. It helps administrators manage access to AWS services securely.*

- **Security Recommendations:** Identifies important account security issues, including MFA configuration.
- **Users (0):** No IAM users have been created.
- **Roles (3):** Three IAM roles are available in the account.
- **Quick Links:** Provides shortcuts to account security and identity management settings.

<img width="1366" height="724" alt="15" src="https://github.com/user-attachments/assets/ebb70ad1-6729-47d1-8683-c404a2778aa7" />

*AWS requires an additional authentication code to verify the Root User's identity after the primary login credentials have been entered.*
- *MFA Verification:* Entered the time-based verification code generated by the registered authenticator app.
- *Identity Validation:* AWS verifies the MFA code before granting access to the account.
- *Account Protection:* Adds an additional security layer beyond password authentication.

  <img width="1366" height="676" alt="16" src="https://github.com/user-attachments/assets/7591c5f0-e804-4f42-81a9-965249443231" />

 * The AWS Console Home Dashboard provides quick access to AWS services, setup resources, and account health information.*
 - *Agent Toolkit for AWS:* Provides documentation, tested procedures, and IAM security guidance for AI coding agents.
-  *Get Setup Prompt:* Allows users to copy configuration instructions for supported AI coding assistants.
-  *Recently Visited Services:* Provides quick access to previously opened services, such as IAM, EC2, and Billing.
-  *Welcome to AWS:* Displays useful resources and guidance for getting started with AWS.
-  *AWS Health:* Provides updates about AWS service availability and account-related events.

  <img width="1345" height="674" alt="17" src="https://github.com/user-attachments/assets/c8ed86f4-da1f-4c69-9014-fb8f4b82112e" />

  

# Project Purpose

*- The primary purpose of AWS Identity Shield is to strengthen AWS account security by implementing Multi-Factor Authentication (MFA) for the AWS Root User.*
*- The project demonstrates how password-based authentication can be enhanced with an additional verification layer using Google Authenticator and Time-Based One-Time Passwords (TOTP).*
*- Through this hands-on implementation, I explored AWS Identity and Access Management (IAM), configured a virtual MFA device, verified authentication codes, and tested the MFA-enabled sign-in process.*

# Disclaimer

*This project, AWS Identity Shield, is created for educational and practical learning purposes to demonstrate AWS Root User security and Multi-Factor Authentication (MFA) implementation. All activities were performed on an authorized AWS account. This project demonstrates security best practices but does not guarantee complete protection against cyber threats or formal compliance with security standards. Never share passwords, account details, MFA QR codes, secret keys, or verification codes publicly.*



