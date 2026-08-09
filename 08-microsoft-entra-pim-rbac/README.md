# Lab: Baseline Identity Hardening with Microsoft Entra Security Defaults(GTG)

## Objective
Implement baseline Zero Trust security policies on a Microsoft Entra ID free tenant to enforce mandatory Multi-Factor Authentication (MFA) and block legacy authentication protocols.

## Execution
1. **Navigate to Properties:** You open up the Microsoft Azure portal, jump straight into **Microsoft Entra ID**, and click on **Properties** right from the management menu on the side. [Microsoft Azure portal](https://portal.azure.com/)
2. **Configure Security Defaults:** You scroll down to find the **Security defaults** section and flip the tenant protection baseline toggle over to **Enabled**.
3. **Global Enforcement:** You make sure that every single account in the directory—from regular standard users to top-level admins, is automatically forced to register for and start using multi-factor authentication every time they sign in.

## Validation & Evidence
* **Baseline Enforcement Verification:** You take a close look at the tenant properties dashboard and confirm that the whole organization is officially protected by security defaults.
* **Protocol Restriction:** You lock down the entire directory so that outdated legacy authentication methods are completely blocked out.

![Security Defaults Enabled](Default%20directory%20screen%20shot.png)


## Security Defaults Configuration Evidence

When building identity governance labs on a free Microsoft Entra ID tenant, advanced security tools like **Privileged Identity Management (PIM)** and custom **Conditional Access Policies** are unavailable due to licensing tier limits (which require Entra ID P1/P2 or Entra Suite subscriptions). 

**Security Defaults** was chosen as the ideal architectural fallback for the following reasons:
* **Zero Cost Implementation:** It doesn't cost anything or require paid licenses, meaning you can set it up instantly on free developer and testing tenants without dealing with sandbox hurdles.
* **Core Protection Baseline:** It automatically forces multi-factor authentication using the Microsoft Authenticator app for everyone on the directory, covering both standard users and administrators.
* **Protocol Hardening:** It automatically shuts down outdated sign-in methods like POP3, IMAP, and SMTP basic auth, which hackers constantly target to harvest credentials.
* **Pragmatic Engineering:** It proves you know how to work around tight limitations and lock down an environment using built-in controls when the expensive enterprise tools are out of reach.
