# AutoAudit: Microsoft 365 Cloud Compliance Engine

## Project Overview
**AutoAudit** is an automated compliance assessment platform developed by a student-led enterprise team (HardHat Enterprises). The platform is designed to assess Microsoft 365 (M365) environments against recognized cybersecurity frameworks, evaluating cloud tenant settings and configurations using Rego policy logic and Microsoft Graph/Defender APIs.

This repository highlights my contributions to the project as part of the **Governance, Risk, and Compliance (GRC) Cohort** during Trimester 2, 2026 (SIT374 - Team Project A).

## My Role & Objectives
As a Junior in the GRC cohort, my primary responsibility is defining *what* AutoAudit assesses and *why*. Rather than building the scanning engine itself, I research industry benchmarks (such as the ASD Information Security Manual, Essential Eight, and CIS Benchmarks), map these controls to specific cloud tenant settings, and hand off implementable specifications to the Compliance Engine team.

## Key Contributions & Research

### 1. Essential Eight: User Application Hardening (Maturity Level 1)
I conducted the research and mapping for the ASD Essential Eight's User Application Hardening mitigation strategy. My work focused on establishing baseline cloud assessment capabilities by mapping Maturity Level 1 (ML1) controls directly to **Microsoft Intune Settings Catalog** policies.

**Key achievements in this workstream:**
*   **API Endpoint Mapping:** Identified the specific Microsoft Graph API endpoints (e.g., `GET /beta/deviceManagement/configurationPolicies/{id}/settings`) required to automate the verification of ML1 controls.
*   **Control Implementation:** Mapped the technical requirements to disable legacy software (Internet Explorer 11), block Java execution, force-install enterprise ad-blockers (e.g., uBlock Origin) to prevent malvertising, and lock browser security settings against user modification.
*   **Confidence & Evidence Rating:** Defined the assessment boundaries, noting that while the Graph API can verify policy *assignment* (a "Fair" evidence confidence level), it cannot guarantee individual endpoint application without deeper OS-level telemetry.

### 2. Bridging the Endpoint-to-Cloud Gap
During my analysis, I conducted a gap assessment between the Essential Eight endpoint requirements and the CIS Microsoft 365 Foundations Benchmark (AutoAudit's baseline framework). 

I identified that the CIS M365 Benchmark strictly targets cloud tenant infrastructure and identity security, deliberately scoping out local endpoint software configurations. By mapping the Intune Settings Catalog policies for browser hardening, I developed a new compliance capability for AutoAudit, effectively bridging the gap between cloud tenant governance and endpoint security.

## Repository Contents
*   [`/Control-Mappings/E8_User_App_Hardening_Mapping.pdf`](#) - *My comprehensive technical mapping document detailing the Intune policy paths, Graph API endpoints, and automation feasibility for the Essential Eight ML1 controls.*

## Skills & Technologies Used
*   **Frameworks:** ASD Essential Eight, CIS Microsoft 365 Foundations Benchmark, ISO/IEC 27001:2022.
*   **Technologies:** Microsoft 365, Microsoft Intune (MDM), Microsoft Graph API.
*   **Concepts:** Cloud tenant governance, policy mapping, compliance automation, JSON/YAML data structures, Rego policy logic.
