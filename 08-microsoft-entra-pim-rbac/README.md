# Lab Update: Microsoft Entra Security Defaults Configuration

## Documentation Adjustment
Since the tenant runs on a free tier where PIM and advanced Conditional Access policies are restricted, the lab documentation should be updated to reflect **Security Defaults** as the baseline Zero Trust implementation.

## Revised `README.md` Content
You can update your repository's `README.md` file to match the active configuration:

```markdown
# Lab: Baseline Identity Hardening with Microsoft Entra Security Defaults

## Objective
Implement baseline Zero Trust security policies on a Microsoft Entra ID free tenant to enforce mandatory Multi-Factor Authentication (MFA) and block legacy authentication protocols.

## Execution
1. **Navigate to Properties:** Opened the [Microsoft Azure portal](https://portal.azure.com/), went to **Microsoft Entra ID**, and selected **Properties** from the management menu.
2. **Configure Security Defaults:** Scrolled to the **Security defaults** section and verified that the tenant protection baseline was toggled to **Enabled**.
3. **Global Enforcement:** Ensured all administrative and standard user accounts are automatically forced to register for and utilize MFA upon sign-in.

## Validation
* **Baseline Enforcement Verification:** Confirmed via the tenant properties dashboard that the organization is actively protected by security defaults.
* **Protocol Restriction:** Legacy authentication protocols (such as POP/IMAP/SMTP basic auth) are automatically blocked across the directory.
