# Legacy Application Modernization with Azure DevOps CI/CD and AI Assistance

## Overview
This repository documents a real-world legacy application modernization effort focused on reducing deployment risk through automation, CI/CD, and pragmatic AI assistance.

The goal was not a full rewrite, but to safely introduce source control, repeatable builds, and auditable deployments into a high-risk legacy environment.

---

## Problem
Legacy applications were deployed manually with no source control and no reliable versioning. Production versions were often unclear due to infrequent, unstable updates. Builds depended on a single laptop, and deployments required manually unpacking and copying files to specific directories with strict naming conventions.

The process was high-risk, slow, and difficult to audit or roll back.

---

## Approach
1. Created a Git repository in Azure DevOps and enforced pull request policies on the main branch; trained existing team members on Git fundamentals.
2. Upgraded the application from Visual Studio 2012 to Visual Studio 2022 and established a reliable local build.
3. Partnered with the platform team to define standardized shared folder structures for UAT and PROD releases.
4. Used AI assistance to generate, debug, and refine Azure DevOps YAML pipelines for build, test, and deployment.
5. Implemented Azure DevOps Boards to link helpdesk tickets, user stories, change requests, and deployments, creating full traceability from request to release.
6. Used AI to generate presentation content for leadership demos.

---

## Pipeline Architecture
The CI/CD pipeline is fully defined in YAML and supports:
- Automated builds
- Controlled deployments to UAT and PROD
- Approval gates aligned with CAB and operational controls
- Rapid rollback when needed

See `/docs/pipeline-flow.md` for details.

---

## Where AI Helped
- Debugging dependency and reference issues during the upgrade from Visual Studio 2012 to 2022
- Initial creation and iterative debugging of Azure DevOps YAML pipelines
- Validation of approval gate placement and deployment safety
- Accelerating leadership communication through AI-assisted presentation generation

AI was used to reduce cognitive load, not replace human judgment.

---

## What Worked / What Didn’t

### Worked
- Established an end-to-end, auditable change process
- Significantly reduced deployment risk
- Enabled application rollback within minutes instead of days

### Didn’t
- Converting some legacy applications (Access 2010, VS 2005 websites) to support modern pipelines was not cost-effective
- Several ERP-backed reports (Oracle) were better suited for commercial replacement or full redevelopment

---

## Artifacts
- Pipeline flow diagram
- Example Azure DevOps YAML pipelines
- Leadership presentation (sanitized)

---

## Who This Is For
- Teams maintaining legacy applications
- Organizations with high deployment risk
- Engineers introducing CI/CD into conservative environments
- Leaders seeking safe, incremental modernization
