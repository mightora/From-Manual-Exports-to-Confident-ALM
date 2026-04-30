# Solution 5: Advanced Validations UDF Component Library

## What This Solution Demonstrates

This solution contains a **Power Apps component library** with **User Defined Functions (UDFs)** that provide advanced validation capabilities for canvas apps. It demonstrates the UDF feature in Power Apps — allowing reusable Power Fx functions to be packaged as a component library and shared across multiple apps.

### Components Included

| Component | Type | Description |
|---|---|---|
| Advanced Validations | **Component Library** | Reusable library of validation User Defined Functions |

### Validation Functions Included

- **Email validation** – verifies a value matches standard email format
- **Phone number validation** – checks common phone number patterns
- **Custom regex pattern matching** – validates a string against a supplied regular expression
- **Required field validation** – checks that a field is not blank
- **Numeric range validation** – verifies a number falls within defined min/max bounds

### Key Features

- UDF-based design — functions are called like native Power Fx formulas
- No external connectors or premium licences required
- Real-time feedback mechanism — easily drive visual indicators in your app
- Importable as a standard Power Platform solution

## Source

- **Author:** [Shaheer Ahmad](https://github.com/shaheerahmadch)
- **Source Repository:** [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/advanced-validations-udf)
- **Original ZIP:** [advanced-validations-udf.zip](https://github.com/pnp/powerplatform-samples/blob/main/samples/advanced-validations-udf/solution/advanced-validations-udf.zip)
- **License:** Community sample (PnP)

## Prerequisites

- Any Power Platform environment (no Dataverse required)
- No premium licence required

## How to Import

1. Download `solution.zip` from this folder.
2. Go to [https://make.powerapps.com](https://make.powerapps.com) and select your target environment.
3. Navigate to **Solutions** → **Import solution**.
4. Browse to `solution.zip` and follow the on-screen wizard.
5. Once imported, you can reference the **Advanced Validations** component library from any new or existing canvas app in the same environment via **Insert** → **Get more components** → **Import components**.
