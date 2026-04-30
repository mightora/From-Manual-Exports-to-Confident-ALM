# Power Platform Samples

This directory contains real, publicly available Microsoft Power Platform sample solutions sourced from the [PnP Power Platform Samples](https://github.com/pnp/powerplatform-samples) community repository and other public sources. All solutions are **unmanaged** and can be imported directly into a Dataverse environment.

---

## Solution Samples

| Folder | Solution | Types | Source |
|---|---|---|---|
| [solution-1-leave-request](./solution-1-leave-request/) | Leave Request Template | Canvas App, Model-Driven App, Dataverse | [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/leave-request) |
| [solution-2-dynamic-forms](./solution-2-dynamic-forms/) | Dynamic Forms | Canvas App, Dataverse, Power Fx | [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/dynamic-forms) |
| [solution-3-incident-reporting](./solution-3-incident-reporting/) | Incident Reporting | Canvas App, Model-Driven App, Power Automate, Dataverse | [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/incident-reporting) |
| [solution-4-creator-kit-template](./solution-4-creator-kit-template/) | Creator Kit Template | Canvas App, Power Automate | [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/creator-kit-template) |
| [solution-5-advanced-validations](./solution-5-advanced-validations/) | Advanced Validations UDF | Dataverse Component Library, Power Fx UDFs | [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/advanced-validations-udf) |
| [solution-6-editable-subgrid](./solution-6-editable-subgrid/) | Editable Subgrid | Canvas App | [pnp/powerplatform-samples](https://github.com/pnp/powerplatform-samples/tree/main/samples/editable-subgrid) |

---

## Power Pages Sample

| Folder | Sample | Format | Source |
|---|---|---|---|
| [power-pages-yaml](./power-pages-yaml/) | Courses Registration Portal | YAML / Power Pages CLI source control format | [mtt-personal-work/powerpages-courses-registration-00](https://github.com/mtt-personal-work/powerpages-courses-registration-00) |

---

## How to Use the Solution Samples

Each solution folder contains:
- `solution.zip` — the unmanaged Power Platform solution ZIP, ready to import
- `README.md` — describes what the solution demonstrates, its components, prerequisites, and import steps

### Quick Import Steps

1. Go to [https://make.powerapps.com](https://make.powerapps.com)
2. Select your target environment
3. Navigate to **Solutions** → **Import solution**
4. Browse to the `solution.zip` in the relevant folder
5. Follow the on-screen wizard

> See each folder's `README.md` for solution-specific prerequisites and post-import configuration steps.

---

## Coverage

These samples together cover the following Power Platform areas:

- ✅ **Canvas Apps** — solutions 1, 2, 3, 4, 6
- ✅ **Model-Driven Apps** — solutions 1, 3
- ✅ **Power Automate Flows** — solutions 3, 4
- ✅ **Dataverse components** — solutions 1, 2, 3, 5
- ✅ **Power Pages (YAML / CLI format)** — power-pages-yaml folder

---

## Attribution

All solution samples are sourced from the [PnP Power Platform community samples repository](https://github.com/pnp/powerplatform-samples), which is published under community open-source terms. The Power Pages YAML sample is sourced from [mtt-personal-work/powerpages-courses-registration-00](https://github.com/mtt-personal-work/powerpages-courses-registration-00).
