# Power Pages YAML — Courses Registration Portal

## What This Sample Is

This folder contains a **Power Pages site** exported in the **YAML source-control format** produced by the [Power Platform CLI](https://learn.microsoft.com/power-platform/developer/cli/introduction) (`pac pages download`).

Unlike solution ZIP files, Power Pages sites are managed using a folder-based structure of YAML metadata files and HTML/CSS/JS content files. This format is designed to be committed to source control and deployed across environments using the CLI or CI/CD pipelines.

The sample is based on a publicly available **Courses Registration Portal** ([source repository: mtt-personal-work/powerpages-courses-registration-00](https://github.com/mtt-personal-work/powerpages-courses-registration-00)) and represents the kind of site structure you would create by running `pac pages download` against a Power Pages environment.

---

## Expected Folder Structure

When a Power Pages site is downloaded using the CLI, it produces the following folder structure:

```
power-pages-yaml/
├── website.yml                          # Root website metadata (ID, name, default language)
├── web-pages/
│   └── home/
│       ├── Home.webpage.yml             # Page metadata (template, URL, publishing state)
│       ├── Home.webpage.copy.html       # Main page body HTML
│       ├── Home.webpage.summary.html    # Summary/excerpt HTML
│       ├── Home.webpage.custom_css.css  # Page-level custom CSS
│       └── Home.webpage.custom_javascript.js
├── content-snippets/
│   └── site-name/
│       └── site-name.contentsnippet.yml # Reusable text snippet (e.g. site title)
├── web-templates/                       # Liquid template files for reusable layouts
├── weblink-sets/                        # Navigation menus and their web links
└── deployment-profiles/
    └── dev.deployment.yml               # Environment-specific overrides for dev
```

### Key File Types

| File | Purpose |
|---|---|
| `website.yml` | Root metadata — website ID, default language, header/footer template references |
| `*.webpage.yml` | Metadata for a web page — URL, page template, publishing state, display order |
| `*.webpage.copy.html` | The main body HTML content of the page |
| `*.contentsnippet.yml` | A reusable text or HTML fragment (e.g. site name, footer text) |
| `*.webtemplate.yml` | Metadata for a Liquid-based page template |
| `*.webtemplate.source.html` | The Liquid/HTML source of the web template |
| `deployment-profiles/*.deployment.yml` | Environment-specific value overrides applied at upload time |

---

## How to Download (Export) a Power Pages Site

Use the Power Platform CLI to download a site into this format:

```bash
# Authenticate to your Dataverse environment
pac auth create -u https://your-org.crm.dynamics.com

# List available Power Pages sites
pac pages list

# Download the site into a local folder
pac pages download --path ./power-pages-yaml -id <WebSiteId-GUID> --modelVersion 2
```

Replace `<WebSiteId-GUID>` with the ID returned by `pac pages list`.

---

## How to Upload (Deploy) a Power Pages Site

After making changes to the YAML or HTML files in source control, upload them back to a target environment:

```bash
# Authenticate to the target environment
pac auth create -u https://target-org.crm.dynamics.com

# Upload all changed files
pac pages upload --path ./power-pages-yaml --modelVersion 2
```

To deploy with environment-specific overrides (e.g. different site name in dev vs prod):

```bash
pac pages upload --path ./power-pages-yaml --deploymentProfile dev --modelVersion 2
```

This will apply the values in `deployment-profiles/dev.deployment.yml` on top of the base content.

---

## Using in a CI/CD Pipeline (GitHub Actions)

Below is a minimal example of a GitHub Actions workflow that uploads a Power Pages site:

```yaml
name: Deploy Power Pages

on:
  push:
    branches: [main]
    paths:
      - 'samples/power-pages-yaml/**'

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Install Power Platform Tools
        uses: microsoft/powerplatform-actions/actions-install@v1

      - name: Upload Power Pages site
        uses: microsoft/powerplatform-actions/upload-paportal@v1
        with:
          environment-url: ${{ secrets.ENVIRONMENT_URL }}
          app-id: ${{ secrets.CLIENT_ID }}
          client-secret: ${{ secrets.CLIENT_SECRET }}
          tenant-id: ${{ secrets.TENANT_ID }}
          upload-path: samples/power-pages-yaml
```

---

## Source

- **Source repository:** [mtt-personal-work/powerpages-courses-registration-00](https://github.com/mtt-personal-work/powerpages-courses-registration-00)
- **Power Pages CLI documentation:** [Use Microsoft Power Platform CLI with Power Pages](https://learn.microsoft.com/power-pages/configure/power-platform-cli)
- **Deployment profiles:** [Tutorial: Use deployment profiles](https://learn.microsoft.com/power-pages/configure/power-platform-cli-tutorial#upload-the-changes-using-deployment-profile)

## Prerequisites

- Power Platform CLI installed: `winget install Microsoft.PowerPlatformCLI` or `npm install -g @microsoft/powerplatform-cli`
- A licensed Power Pages environment (trial or production)
- Maker or System Administrator role in the target environment
