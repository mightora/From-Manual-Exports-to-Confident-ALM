# Solution 2: Dynamic Forms

## What This Solution Demonstrates

This solution demonstrates how to build a **dynamic form experience** in Power Apps using Dataverse as a data source. Rather than creating hard-coded forms, this pattern drives the form fields, labels, and validation rules from a data-driven configuration stored in Dataverse — making it easy to extend forms without changing the app itself.

### Components Included

| Component | Type | Description |
|---|---|---|
| Dynamic Forms App | **Canvas App** | Power Apps canvas app demonstrating dynamic form rendering |
| Form Configuration | **Dataverse Tables** | Tables that define field definitions, form layout, and validation rules |
| Power Fx Logic | **Power Fx** | Advanced formula patterns to render controls based on configuration |

### Key Features

- Data-driven form field definitions stored in Dataverse
- Dynamic rendering of text, choice, date, and number field types
- Configurable required/optional field rules
- Shows a pattern applicable to survey tools, registration forms, and inspection checklists

## Source

- **Author:** [Craig White](https://github.com/CraigWhite81)
- **Source Repository:** [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/dynamic-forms)
- **Original ZIP:** [DynamicFormsSample_1_0_0_1.zip](https://github.com/pnp/powerplatform-samples/blob/main/samples/dynamic-forms/solution/DynamicFormsSample_1_0_0_1.zip)
- **License:** Community sample (PnP)

## Prerequisites

- A Power Platform environment with a **Dataverse** database
- A **Premium Power Apps licence** (required for Dataverse connectivity)

## How to Import

1. Download `solution.zip` from this folder.
2. Go to [https://make.powerapps.com](https://make.powerapps.com) and select your target environment.
3. Navigate to **Solutions** → **Import solution**.
4. Browse to `solution.zip` and follow the on-screen wizard.
5. Once imported, open the canvas app from the solution and verify the Dataverse connections are correctly set up.
