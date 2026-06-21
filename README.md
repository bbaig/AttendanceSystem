# Enterprise Attendance Management System Configuration Setup Runbook

## Core Platform Topology
* **Frontend Layer Engine:** Single-Page Semantic Core Architecture (Vanilla HTML5 / Modern Flex CSS / Functional ES6 JavaScript API Drivers).
* **Host Provisioning Engine:** Vercel Global Static Serverless Edge.
* **Middle API Router Engine:** Google Apps Script Execution Engine Engine Engine (`doPost` Web App Gateway Routing).
* **Database Ledger Layer:** Spreadsheet Cloud Table Matrices (`Users`, `Attendance`, `AuditLogs`, `Configuration`).

---

## Step-by-Step Deployment Protocols

### Phase A: Google Sheet Setup Matrix
1. Create a clean sheet workbook profile named `Enterprise Attendance DB`.
2. Generate four specific sheet processing frames explicitly named:
   * `Users`
   * `Attendance`
   * `AuditLogs`
   * `Configuration`
3. Populate headers identically matching the Data Layer Schemas detailed in Section 1. Ensure you create at least one user with the `Admin` role flag and one with the `Employee` flag to enable initial authentication testing.

### Phase B: Middle API Engine Deployment
1. Inside the Sheet instance interface, click **Extensions > Apps Script**.
2. Replace all block structures inside `Code.gs` with the architectural implementation provided in Section 2.
3. Access **Project Settings** (gear icon) and ensure the manifest display checkbox is enabled. Overwrite the layout inside `appsscript.json` with the manifest object provided above.
4. Click **Deploy > New deployment**. Select **Web App** as the configuration deployment model type. Set compilation parameters explicitly to run as **Me** and allow access to **Anyone**. Save and copy the output **Web App URL** text string.

### Phase C: Client Connection Injection
1. Open your local `index.html` frontend source file code context.
2. Search for the defined global runtime state declaration variable: `const API_GATEWAY = "..."`
3. Paste the Web App URL string you copied in Phase B into this variable.

### Phase D: Vercel Edge Serverless Deployment
1. Verify that your localized project space contains your modified `index.html`.
2. Open your terminal context inside your root source path and execute via the Vercel Global CLI toolchain:
   ```bash
   npm install -g vercel
   vercel login
   vercel