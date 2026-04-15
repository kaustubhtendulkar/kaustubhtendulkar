<h1 align="center">Hi, I'm Kaustubh Tendulkar</h1>

<p align="center">
  <img src="assets/profile-photo.png" alt="Kaustubh Tendulkar" width="180" />
</p>

<p align="center">
	<b>Dynamics 365 CE Consultant at HSO | Bridging CRM & Agentic AI</b><br/>
	Copilot Studio • AI Builder • Plugin Architecture • Azure Integration • Data Migration • CI/CD & ALM
</p>

<p align="center">
	<a href="https://www.linkedin.com/in/kaustubhtendulkar/" target="_blank">
		<img src="https://img.shields.io/badge/LinkedIn-kaustubhtendulkar-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" />
	</a>
	<img src="https://img.shields.io/badge/Location-Netherlands-orange?style=flat" alt="Location" />
	<img src="https://img.shields.io/badge/Experience-14%2B%20Years-brightgreen?style=flat" alt="Experience" />
	<img src="https://img.shields.io/badge/MCPS-Microsoft_Certified-blue?style=flat&logo=microsoft" alt="MCPS" />
	<img src="https://img.shields.io/badge/GitHub_Copilot-Skills_Author-8957e5?style=flat&logo=githubcopilot&logoColor=white" alt="Copilot Skills" />
</p>

---

## About Me

Dynamics 365 CE and Power Platform consultant with **14+ years** of experience delivering enterprise CRM solutions across discovery, architecture, development, integration, migration, and ALM — now at the intersection of **CRM and Agentic AI**.

I specialize in building **scalable plugin architectures**, **Azure integration patterns**, and **data migration frameworks** with strong engineering practices — BDD testing, CI/CD governance, and infrastructure-as-code.

Currently exploring how **Copilot Studio**, **AI Builder**, and **Azure OpenAI** are reshaping business applications. I author reusable **GitHub Copilot Skills** that encode domain expertise into shareable, version-controlled workflow packages — enabling teams to scaffold production-ready Dynamics 365 solutions in minutes.

---

## What I Build

| Domain | Capabilities |
|---|---|
| **Plugin Development** | 4-layer plugin architecture (Plugin → Controller → Validator → Repository), fluent registration API, DAXIF deployment |
| **Testing** | BDD with Reqnroll + FakeXrmEasy, strongly-typed entity mocking, automated coverage |
| **Azure Integration** | Service Bus, Azure Functions, Logic Apps — relay patterns, webhook endpoints, high-volume migration orchestration |
| **Data Migration** | ADF-based frameworks, activity party & M:N migration, staging tables, ID-mapping strategies |
| **TypeScript / PCF** | Model-driven app web resources, PCF controls, structured transpilation flows |
| **ALM & DevOps** | Multi-environment Azure Pipelines, solution packaging, DAXIF sync, XrmContext generation |
| **AI Tooling** | Copilot Studio, AI Builder, Agentic AI patterns, GitHub Copilot Skills authoring, centralized skill distribution, AI-driven code scaffolding |

---

## Featured Repositories

| Repository | Description |
|---|---|
| **[PowerPlatform-Plugins-Development](https://github.com/kaustubhtendulkar/PowerPlatform-Plugins-Development)** | Production-ready C# plugin template with 4-layer architecture, Reqnroll BDD testing, DAXIF deployment, and GitHub Copilot Skills integration |
| **[PowerPlatform-Migration-Helper-Plugins](https://github.com/kaustubhtendulkar/PowerPlatform-Migration-Helper-Plugins)** | Custom API plugins and data models for ADF-based Dataverse data migration — activity party, M:N, and high-volume scenarios |
| **[PowerPlatform-Plugins-Development-AzFunctions](https://github.com/kaustubhtendulkar/PowerPlatform-Plugins-Development-AzFunctions)** | Azure Functions integration layer for Dynamics 365 — webhook relay, Service Bus triggers, and serverless orchestration |
| **[PowerPlatform-TypeScripts-Development](https://github.com/kaustubhtendulkar/PowerPlatform-TypeScripts-Development)** | TypeScript web resource template for model-driven apps — modular event handlers, transpilation pipeline, deployment-ready |
| **[PowerPlatform-AIO-Project-Template](https://github.com/kaustubhtendulkar/PowerPlatform-AIO-Project-Template)** | All-in-one Power Platform project template — plugins, web resources, solution packaging, and ALM pipelines in a single scaffold |
| **[CentralSkillsRepository](https://github.com/kaustubhtendulkar/CentralSkillsRepository)** | Centralized library of GitHub Copilot Skills — reusable AI workflow packages synced across workspaces via push/pull mechanism |

---

## GitHub Copilot Skills

I author and maintain a library of **GitHub Copilot Skills** — AI workflow packages that encode deep domain expertise into versioned, shareable accelerators.

```
┌──────────────────────────┐         ┌──────────────────────────────┐
│  Any Workspace Repo      │         │  CentralSkillsRepository     │
│  .github/skills/         │ ──push──│  skills/                     │
│    Sync-Skills.ps1       │         │    PowerPlatform-Plugin-...  │
│    PowerPlatform-Plugin/ │ ◄─pull──│    dataverse-migration-...   │
└──────────────────────────┘         └──────────────────────────────┘
```

**Published Skills:**

| Skill | What It Does |
|---|---|
| `PowerPlatform-Plugin-Daxif` | Scaffolds complete Dynamics 365 plugin solutions — plugins, validators, controllers, repositories, Custom APIs, BDD tests, DAXIF deployment scripts |
| `dataverse-migration-scaffolder` | Scaffolds ADF migration projects — staging tables, Custom API plugins, Logic App ARM templates, multi-instance deployment |

> Skills are synchronized across repos using a `Sync-Skills.ps1` push/pull mechanism. Ask Copilot to scaffold a plugin and it automatically applies the right patterns.

---

## Architecture Patterns

<details>
<summary><b>Plugin 4-Layer Architecture</b></summary>

```
Plugin (Registration & Routing)
  └── Controller (Orchestration)
        ├── Validator (Business Rules)
        ├── DefaultValueProvider (Computed Defaults)
        └── Repository (Data Access)
```

- Fluent plugin registration via `RegisterPluginStep<T>()`
- `IDataverseContext` for dependency injection and testability
- `StronglyTypedValidator<T>` with `ValidationResult` pattern
- `QueryExpressionBuilder<T>` for type-safe complex queries

</details>

<details>
<summary><b>BDD Testing with Reqnroll + FakeXrmEasy</b></summary>

```gherkin
Feature: Account Validation

Scenario: Reject accounts without a name
    Given the following plugin registration
        | Stage          | Message Name | Execution Mode | PrimaryEntityName |
        | PreValidation  | Create       | Synchronous    | account           |
    And an account as Target with the following values
        | Property | Value |
        | name     |       |
    When the plugin AccountValidationPlugin is executed
    Then the plugin throws an error
```

- Each plugin is tested via Gherkin feature files
- FakeXrmEasy provides in-memory CRM context
- No live environment needed for CI test runs

</details>

---

## Tech Stack

| Domain | Technologies |
|---|---|
| **CRM / Platform** | Dynamics 365 CE, Dataverse, Power Platform, Power Pages |
| **Development** | C#, .NET Framework 4.6.2, TypeScript, JavaScript |
| **SDK / APIs** | Dataverse SDK, Web API, Custom APIs, REST, OAuth |
| **Azure** | Azure DevOps, Service Bus, Logic Apps, Functions, Data Factory, Blob Storage |
| **Testing** | Reqnroll (BDD), FakeXrmEasy, NUnit |
| **Deployment** | DAXIF, XrmContext, Azure Pipelines (YAML), PowerShell |
| **AI Tooling** | GitHub Copilot, Copilot Skills, Copilot Studio, AI Builder, VS Code Agent Mode |
| **Data** | KingswaySoft SSIS, SQL Server, ADF Migration Pipelines |

---

## Certifications

<p>
	<img src="https://img.shields.io/badge/PL--400-Power%20Platform%20Developer-742774?style=for-the-badge&logo=microsoft&logoColor=white" alt="PL-400" />
	<img src="https://img.shields.io/badge/PL--200-Power%20Platform%20Functional%20Consultant-742774?style=for-the-badge&logo=microsoft&logoColor=white" alt="PL-200" />
	<img src="https://img.shields.io/badge/AZ--900-Azure%20Fundamentals-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-900" />
</p>

<details>
<summary>View Full Certification List</summary>

- PL-400 — Power Platform Developer Associate (May 2025)
- PL-200 — Power Platform Functional Consultant Associate (Apr 2025)
- AZ-900 — Microsoft Azure Fundamentals (Mar 2019)
- MB2-716 — Dynamics 365 Customization and Configuration (Dec 2018)
- MB2-712 — Dynamics CRM 2016 Customization and Configuration (Apr 2017)
- MB2-704 — Dynamics CRM 2015 Application (Jan 2016)
- MB2-707 — Dynamics CRM 2015 Customization and Configuration (Jan 2016)
- MB2-701 — Extending Microsoft Dynamics CRM 2013 (Sep 2015)
- MB2-700 — Dynamics CRM 2013 Applications (Aug 2015)
- MCPS — Microsoft Certified Professional (Aug 2015)

</details>

---

## Experience Highlights

- Delivered **enterprise CRM modules** for large-scale banking and consulting engagements across Europe
- Built **production-grade developer tooling** — translation tools, audit frameworks, release automation, and migration accelerators
- Established **CI/CD delivery practices** for multi-environment Dynamics 365 deployments with Azure DevOps
- Pioneered **AI-assisted development workflows** using GitHub Copilot Skills for repeatable enterprise scaffolding
- Exploring **Copilot Studio** and **AI Builder** to embed intelligent automation into Dynamics 365 and Power Platform solutions
- Mentored delivery teams on **engineering quality**, architecture standards, and testability patterns

---

## Connect

<p>
	<a href="https://www.linkedin.com/in/kaustubhtendulkar/" target="_blank">
		<img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
	</a>
	<a href="mailto:info.ktendulkar@gmail.com">
		<img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
	</a>
</p>