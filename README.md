# ADO Secret Viewer

> Secure Azure DevOps pipeline tool to safely inspect and audit Variable Group secrets — without exposing values in logs or UI.

[![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-Pipeline-0078D4?style=flat-square&logo=azure-devops&logoColor=white)](https://dev.azure.com)
[![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com)
[![Security](https://img.shields.io/badge/Security-Auditing-red?style=flat-square&logo=shield&logoColor=white)](https://github.com/SauravSrivastav/ado-secret-viewer)
[![YAML](https://img.shields.io/badge/Azure_Pipelines-YAML-0078D4?style=flat-square&logo=azure-devops&logoColor=white)](https://azure.microsoft.com/services/devops/pipelines/)

---

## Overview

**ADO Secret Viewer** is an Azure DevOps pipeline that enables authorized engineers to **safely retrieve and audit Variable Group secrets** — storing them as pipeline artifacts for controlled inspection without compromising security posture.

Built to solve a common DevSecOps problem: securely auditing secrets in Azure DevOps without CLI access or direct Key Vault permissions.

---

## Use Cases

- **Secret auditing** — Verify variable values without sharing credentials
- **Troubleshooting** — Debug pipeline failures caused by missing or incorrect secrets
- **Compliance** — Audit trail for secret access and inspection
- **Onboarding** — Help new team members verify their Variable Group access

---

## How It Works

```
Pipeline Trigger
    │
    ▼
Authenticate (Service Principal / Managed Identity)
    │
    ▼
Access Variable Group
    │
    ▼
Store values as encrypted pipeline artifacts
    │
    ▼
Authorized user downloads artifact securely
```

---

## Files

| File | Description |
|------|-------------|
| `azure-pipelines.yml` | Main pipeline definition |
| `explanation.md` | Detailed setup guide and security notes |
| `README.md` | This file |

---

## Setup

### Prerequisites

- Azure DevOps project with Variable Groups configured
- Service connection with Variable Group read access
- Pipeline agent with access to the target environment

### Quick Start

```yaml
# azure-pipelines.yml — trigger manually or on schedule
trigger: none

variables:
  - group: your-variable-group-name

steps:
  - script: echo "##vso[task.setvariable variable=SECRET_VAL]$(YOUR_SECRET)"
    displayName: 'Retrieve secret'
```

> Full instructions in [explanation.md](./explanation.md)

---

## Security Considerations

- Pipeline artifacts are scoped to the pipeline run — not publicly accessible
- Use **least-privilege service connections** — read-only to Variable Groups
- Enable **audit logging** in Azure DevOps for all pipeline runs
- Rotate secrets after any audit inspection
- Do not print secret values to pipeline logs

---

## Built By

**Saurav Srivastav** — DevOps Manager at Emirates Flight Catering | Azure DevOps · Entra ID · Zero Trust | Dubai, UAE

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/sauravsrivastav2205/)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-0078D4?style=flat-square&logo=vercel)](https://saurav-srivastav-portfolio.vercel.app)

---

<sub>Azure DevOps · Azure Pipelines · Security · Secrets Management · DevSecOps · Variable Groups · YAML · Audit · Dubai UAE</sub>
