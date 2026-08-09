# Lab: Implementing Just-In-Time (JIT) Privileged Access with Microsoft Entra ID PIM

## Objective
Implement a Just-In-Time (JIT) privileged access strategy using Microsoft Entra ID Privileged Identity Management (PIM) to eliminate standing administrative rights and enforce the Principle of Least Privilege.

## Execution
1. **Navigate to PIM:** Opened the **Microsoft Entra admin center**, browsed to **Identity governance**, and selected **Privileged Identity Management**.
2. **Configure Role Settings:** Selected the **Security Administrator** role and adjusted role settings to enforce:
   * Mandatory **Multi-Factor Authentication (MFA)** upon activation.
   * Required **business justification** explaining the operational need for activation.
   * Maximum allowed activation duration restricted to **2 hours**.
3. **Assign Eligible Access:** Provisioned a dedicated admin account with an **Eligible** (rather than permanent/active) assignment status for the Security Administrator role.

## Validation
* **Initial State Verification:** Queried active roles using the test administrative account without initiating a PIM session, confirming zero standing administrative privileges.
* **Activation Workflow:** Initiated an activation request via the PIM portal, provided the mandatory business justification, and successfully completed the MFA challenge.
* **Access Confirmation:** Verified that administrative permissions were automatically granted and revoked strictly within the defined operational timeframe.
