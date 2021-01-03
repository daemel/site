---
title: Export Quickstart
parent: Tools
grand_parent: FHIR
nav_order: 1
---

# Export Quickstart 

![Microsoft and FHIR](/assets/images/msftfhir.png)

### Introduction 
The FHIR Export Quickstart is to help setup exporting FHIR data on a regular basis. Below is a simple architecture and steps.

![FHIRExportQuickstartArchitecture](/assets/images/FHIRExportQuickstartArchitecture.jpg)

Steps in data flow:
1. Timer triggers Logic App - default trigger time is 1:00 AM UTC
2. Logic Apps calls Key Vault for secrets
3. Logic App – calls FHIR service with GET $export
4. FHIR service pushed bulk export to preset storage location

### Prerequisites
Before deploying make sure you have:
- An Azure Subscription
- Azure API for FHIR deployed with data
- Configured Export for API for FHIR. Documentation for config - https://docs.microsoft.com/en-us/azure/healthcare-apis/configure-export-data
- Installed the Az Powershell Module

```PowerShell
Install-Module Az
```


### Support or Contact

For more information on health solutions email us **@ <a href="mailto:HealthArchitectures@microsoft.com">HealthArchitectures</a>**