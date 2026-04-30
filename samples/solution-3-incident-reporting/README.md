# Solution 3: Incident Reporting

## What This Solution Demonstrates

This solution provides a complete **incident reporting and management system** combining a Canvas App for field users, a Model-Driven App for administrators, and a Power Automate flow for notifications. It shows how multiple Power Platform components work together in a realistic enterprise scenario.

### Components Included

| Component | Type | Description |
|---|---|---|
| Incident Reporting App | **Canvas App** | Phone-layout app for reporting incidents with image upload |
| Incident Management App | **Model-Driven App** | Admin view for reviewing and managing reported incidents |
| Incident Assignment Flow | **Power Automate** | Automated flow to assign incidents to the appropriate team |
| Incident Reports Table | **Dataverse Table** | Custom table storing incident records |
| SharePoint Connection | **Connection Reference** | For storing uploaded incident images |
| Outlook Connection | **Connection Reference** | For sending notification emails |

### Key Features

- Visually appealing phone-layout UI for field incident reporting
- Image upload integration with SharePoint
- Automated email notifications via Outlook when incidents are assigned
- Model-Driven App for centralised incident management and analytics
- Environment variables for configurable SharePoint site and list URLs

## Source

- **Author:** [Shaheer Ahmad](https://github.com/shaheerahmadch)
- **Source Repository:** [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/incident-reporting)
- **Original ZIP:** [incident-reporting.zip](https://github.com/pnp/powerplatform-samples/blob/main/samples/incident-reporting/solution/incident-reporting.zip)
- **License:** Community sample (PnP)

## Prerequisites

- A Power Platform environment with a **Dataverse** database
- A **Premium Power Apps licence** (required for Dataverse connectivity)
- A **SharePoint site** with a list named `IncidentReports` containing these columns:
  - `Title` (Single line of text, required)
  - `Description` (Multiple lines of text, optional)
  - `IncidentImage` (Image, optional)
  - `IncidentType` (Choice, required)
  - `IncidentDate` (Date and Time, required)
- An active **Outlook** mailbox for the notification flow

## How to Import

1. Download `solution.zip` from this folder.
2. Go to [https://make.powerapps.com](https://make.powerapps.com) and select your target environment.
3. Navigate to **Solutions** → **Import solution**.
4. Browse to `solution.zip` and follow the on-screen wizard.
5. During import, configure the connection references for SharePoint and Outlook.
6. After import, set the environment variables to point to your SharePoint site and list.
7. Turn on the Power Automate flow from within the solution.
