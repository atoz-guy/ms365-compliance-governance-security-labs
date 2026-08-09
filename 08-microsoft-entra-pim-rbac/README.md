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
