# Oracle Pluggable Database Configuration and Administration Assignment

## 1. Assignment Overview
The objective of this practical assignment is to demonstrate fundamental competency in Oracle Multitenant Architecture. The tasks involve creating and configuring a localized Pluggable Database (PDB), provisioning application-specific user security controls within the container structure, managing transient test environments through programmatic database lifecycles (creation, operational state switching, and safe purging), and verifying engine topology metrics using an enterprise graphic management dashboard.

---

## 2. Oracle Environment
*   **Oracle Database Version Used:** Oracle Database 21c Express Edition (XE)
*   **Operating System/Environment:** Windows 11 Home / Professional (x64)
*   **Tools Used:** 
    *   Visual Studio Code (VS Code) with the official Oracle Developer Tools for VS Code extension
    *   Oracle Enterprise Manager (OEM) Database Express
    *   Windows Command Prompt (CLI)

---

## 3. Task Documentation

### Task 1: Create and Configure a New Pluggable Database (PDB)
*   **PDB Creation Process:** Connected to the root container (`CDB$ROOT`) as a system administrator with `SYSDBA` privileges. Executed the automated database provisioning script using the explicit user naming pattern matching my student registration parameters.
*   **User Creation Process:** Switched the operational container session scope internally to the newly mapped pluggable context. Created a separate student application-level schema authenticated locally and assigned comprehensive administrative execution rights (`CONNECT`, `RESOURCE`, and `DBA`) to allow structural design work in future practical tasks.
*   **Connection Verification:** Built a standalone logical connection profile inside VS Code addressing the distinct PDB system service descriptor over local networking configurations, bypassing the root container layer entirely.

### Task 2: Create and Delete a Temporary PDB
*   **Transient Lifecycles:** Demonstrated strict database instance control routines by returning session scope back to the base environment root (`CDB$ROOT`) and creating a targeted workspace using the required temporary naming convention (`di_to_delete_pdb_324102025`).
*   **State Switching and Drop Routine:** Validated the state of the structure using catalog registry tables (`v$pdbs`), altered the state to operational (`OPEN`), safely stopped background system threads using immediate termination guidelines (`CLOSE IMMEDIATE`), and dropped the instance alongside its physical operating storage system references (`INCLUDING DATAFILES`).
*   **Final Evidentiary Audit:** Ran targeted diagnostic lookups against global container parameters to prove the database instance footprint was cleanly removed from the local Oracle file registry.

### Task 3: Oracle Enterprise Manager (OEM) Configuration
*   **Web Dashboard Access:** Successfully initialized local secure socket layers via web browser routing elements over designated administrator engine endpoints (`https://localhost:5500/em`).
*   **Monitoring and Verification:** Authenticated using system administrator tokens to access the OEM Database Express graphic dashboard to confirm real-time memory usage boundaries, engine state statistics, system architecture version controls, and the persistence of the active container architecture.

---

## 4. Challenges and Solutions

### 1. Legacy Environment Collisions and Cleanup Errors
*   **Challenge:** Initial environment deployments caused conflicts due to leftover Windows services and registry elements from older Oracle database versions (11g), resulting in configuration errors during the installation of Oracle 21c XE.
*   **Solution:** Performed a complete manual system purge by disabling matching legacy background configurations, removing lingering application folder trees, cleaning up the Windows system registry directories, and restarting the machine to clear memory before running a fresh, clean installation of version 21c.

### 2. Missing Database Targets during State Switching Loops
*   **Challenge:** Running SQL operational commands threw container management errors (`ORA-65011: Pluggable database does not exist`) during Task 2. This happened because the name in the script didn't match the database name generated during creation.
*   **Solution:** Standardized script references by cross-checking naming criteria with university rules. Explicitly matched script variables to the target container name (`di_to_delete_pdb_324102025`), ensuring accurate targeting across the creation, execution, and removal loops.

### 3. Rapidly Disappearing UI Test Indicators
*   **Challenge:** The VS Code interface connection status banner indicating a successful login test would disappear before a screenshot could be captured.
*   **Solution:** Allowed the profile connection to save cleanly and complete its setup, then used the persistent sidebar connections layout displaying the live user profile hook with its green active plug element to capture clear evidence for submission.

---

## 5. Lessons Learned
*   **Multitenant Isolation Concepts:** Gained functional insight into separating independent application databases cleanly inside a single primary container container architecture (CDB/PDB models).
*   **Administrative Security Operations:** Mastered the assignment of custom application credentials and roles safely isolated from root administrator scopes.
*   **Storage Lifecycle Automations:** Acquired practical skills in safely initializing, altering, closing, and deleting relational table spaces along with their physical disk data mapping systems using strict command sequences.
*   **Enterprise Telemetry Auditing:** Learned to monitor database operations using both command-line verification scripts and visual interface dashboards.

---

## 6. Integrity Statement
"I confirm that this assignment represents my own practical work, screenshots, and documentation. All external resources consulted have been properly acknowledged."