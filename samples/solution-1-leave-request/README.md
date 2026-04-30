# Solution 1: Leave Request Template

## What This Solution Demonstrates

This solution provides a complete **leave request management system** for Power Platform. It demonstrates how to build a real-world business application using multiple Power Platform components working together.

### Components Included

| Component | Type | Description |
|---|---|---|
| Leave Request App | **Canvas App** | Employee-facing app to view balances, submit and track requests |
| Leave Request Management | **Model-Driven App** | Admin app to manage underlying Dataverse data |
| Leave Requests | **Dataverse Table** | Custom table to store leave request records |
| Leave Types | **Dataverse Table** | Reference table for leave categories |
| Leave Balances | **Dataverse Table** | Table tracking remaining leave per employee |
| Leave Approvers | **Dataverse Table** | Table for managing designated approvers |
| Company Holidays | **Dataverse Table** | Table for tracking non-working days |

### Key Features

- Dashboard with custom SVGs showing visual leave balance summaries
- Automatic weekend exclusion from day/hour calculations
- Guard against submitting overlapping leave requests
- Approval workflow with automatic email notifications to requestors
- A Model-Driven App for administrators to seed and manage reference data

## Source

- **Author:** [April Dunnam](https://github.com/aprildunnam)
- **Source Repository:** [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/leave-request)
- **Original ZIP:** [leave-request.zip](https://github.com/pnp/powerplatform-samples/blob/main/samples/leave-request/solution/leave-request.zip)
- **License:** Community sample (PnP)

## Prerequisites

- A Power Platform environment with a **Dataverse** database
- A **Premium Power Apps licence** (required for Dataverse connectivity)
- After import, open the **Leave Request Management** Model-Driven App and populate the following reference tables with your organisation's data:
  - **Company Holidays** – add any non-working public holidays
  - **Leave Types** – add categories such as Annual, Sick, Parental
  - **Leave Approvers** – designate who can approve requests
  - **Leave Balances** – set the opening leave balance for each employee

## How to Import

1. Download `solution.zip` from this folder.
2. Go to [https://make.powerapps.com](https://make.powerapps.com) and select your target environment.
3. Navigate to **Solutions** → **Import solution**.
4. Browse to `solution.zip` and follow the on-screen wizard.
5. Once imported, open the **Leave Request Management** Model-Driven App to enter reference data before using the canvas app.
