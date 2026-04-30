# Solution 4: Creator Kit Template

## What This Solution Demonstrates

This solution provides a **responsive canvas app template** built using Microsoft's [Creator Kit](https://learn.microsoft.com/power-platform/guidance/creator-kit/overview) component library. It demonstrates how to build a modern, professionally styled canvas app that manages Accounts and Contacts with document upload capabilities through SharePoint.

### Components Included

| Component | Type | Description |
|---|---|---|
| Creator Kit Template App | **Canvas App** | Responsive canvas app using Creator Kit Fluent UI components |
| Upload a File to SharePoint | **Power Automate Flow** | Flow triggered from the app to upload documents to SharePoint |
| Documents | **Environment Variable** | Configurable SharePoint document library URL |
| SharePoint Site | **Environment Variable** | Configurable SharePoint site URL |
| SharePoint Connection Reference | **Connection Reference** | For document upload via the Power Automate flow |

### Key Features

- Modern, responsive phone-layout design using Creator Kit (Fluent UI)
- Account and Contact management screens
- Document upload to SharePoint via an embedded Power Automate flow
- Environment variables for easy reconfiguration across environments
- Demonstrates the Creator Kit component pattern for professional app styling

## Source

- **Author:** [Shaheer Ahmad](https://github.com/shaheerahmadch)
- **Source Repository:** [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/creator-kit-template)
- **Original ZIP:** [creator-kit-template.zip](https://github.com/pnp/powerplatform-samples/blob/main/samples/creator-kit-template/solution/creator-kit-template.zip)
- **License:** Community sample (PnP)

## Prerequisites

- A Power Platform environment (Dataverse not required — standard connections are used)
- The **[Creator Kit](https://learn.microsoft.com/power-platform/guidance/creator-kit/setup)** must be installed in the environment before importing this solution
- A **SharePoint site** and document library for document upload functionality

## How to Import

1. Ensure the **Creator Kit** solution is already installed in your environment.
2. Download `solution.zip` from this folder.
3. Go to [https://make.powerapps.com](https://make.powerapps.com) and select your target environment.
4. Navigate to **Solutions** → **Import solution**.
5. Browse to `solution.zip` and follow the on-screen wizard.
6. During import, configure the SharePoint connection reference.
7. After import, update the environment variables with your SharePoint site and document library URLs.
