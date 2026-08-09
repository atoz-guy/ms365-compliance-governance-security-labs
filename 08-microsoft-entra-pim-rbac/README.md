# Lab: Baseline Identity Hardening with Microsoft Entra Security Defaults

## Objective
Implement baseline Zero Trust security policies on a Microsoft Entra ID free tenant to enforce mandatory Multi-Factor Authentication (MFA) and block legacy authentication protocols.

## Execution
1. **Navigate to Properties:** Opened the [Microsoft Azure portal](https://portal.azure.com/), went to **Microsoft Entra ID**, and selected **Properties** from the management menu.
2. **Configure Security Defaults:** Scrolled to the **Security defaults** section and verified that the tenant protection baseline was toggled to **Enabled**.
3. **Global Enforcement:** Ensured all administrative and standard user accounts are automatically forced to register for and utilize MFA upon sign-in.

## Validation & Evidence
* **Baseline Enforcement Verification:** Confirmed via the tenant properties dashboard that the organization is actively protected by security defaults.
* **Protocol Restriction:** Legacy authentication protocols are automatically blocked across the directory.

![Security Defaults Enabled](Default%20directory%20screen%20shot.png)


## Security Defaults Configuration Evidence

When building identity governance labs on a free Microsoft Entra ID tenant, advanced security tools like **Privileged Identity Management (PIM)** and custom **Conditional Access Policies** are unavailable due to licensing tier limits (which require Entra ID P1/P2 or Entra Suite subscriptions). 

**Security Defaults** was chosen as the ideal architectural fallback for the following reasons:
* **Zero Cost Implementation:** Available out-of-the-box on free developer and testing tenants without requiring paid licenses or sandbox sign-up hurdles.
* **Core Protection Baseline:** Automatically enforces multi-factor authentication (MFA) using the Microsoft Authenticator app for all users and administrators.
* **Protocol Hardening:** Automatically blocks legacy authentication protocols (like POP3, IMAP, and SMTP basic auth), which are primary vectors for credential harvesting attacks.
* **Pragmatic Engineering:** Demonstrates an ability to work within constraints and secure an enterprise environment using native controls when premium enterprise tools are inaccessible.
