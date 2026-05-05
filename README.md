# Hi, I'm Carrie Warner 👋
Senior Technical Writer. 25+ years writing docs people use under pressure.

*Profile last updated: May 2026*

I built a GitHub Actions pipeline at Mattermost that cut draft production time by 5x and reduced support tickets by 30%+ across 60+ consecutive releases. I also used Claude to validate Mattermost's entire permissions surface against the codebase directly, shifting that work from SME-dependent review to AI-assisted analysis with SME confirmation. It was faster, and it found gaps the previous process had missed.

I've built documentation functions from scratch at 4 companies, hiring and directing writers, contractors, co-op students, and open-source community contributors along the way. I work directly with codebases, engineering PRs, customer support teams, while aligning with sales and marketing, and the people deploying the product in production. My documentation has supported deployments in Defence, Intelligence, and regulated enterprise environments where incomplete docs have real consequences.

[**LinkedIn**](https://linkedin.com/in/carriewarner)

## Contribution Metrics (2020–2026)
![Authored PRs](https://img.shields.io/badge/Authored_PRs-2%2C058%2B-blue?style=for-the-badge&logo=github)
![Influenced PRs](https://img.shields.io/badge/Influenced_PRs-3%2C634%2B-orange?style=for-the-badge&logo=github)
![Community Merges](https://img.shields.io/badge/Community_Merges-1%2C654-green?style=for-the-badge&logo=opensourceinitiative)

---

## Some of my best work

I operate at the intersection of engineering reality and customer-consumable truth. I specialize in high-stakes markets where documentation is a strategic business asset and a regulated upstream dependency. 
Here are 3 samples of my work and what it took to get there:

1. [Configuration Settings Overhaul](#configuration-settings-overhaul)
2. [Advanced Permissions Backend Infrastructure](#advanced-permissions-backend-infrastructure)
3. [Microsoft Intune MAM Configuration](#microsoft-intune-mam-configuration)

### Configuration Settings Overhaul

[2020 state](https://web.archive.org/web/20201125075451/https://docs.mattermost.com/administration/config-settings.html) versus [today](https://docs.mattermost.com/administration-guide/configure/configuration-settings.html) 

Mattermost's entire server-side configuration surface lived on 1 page. No default values. No valid options. No consequences. No SKU availability. No environment variable syntax. System Administrators in air-gapped and regulated environments were filing support tickets to confirm details that should have been in the docs.

- **What I built**: A new documentation standard covering 12 restructured pages. Every setting documents the `config.json` key, system console UI path, environment variable syntax, data type, default value, all valid options with consequences, and SKU availability. I designed a badge system for SKU-level availability and implemented it across the entire product surface.

- **The constraint I solved at the platform level**: Splitting the content broke a legitimate workflow that pre-sales engineers, support, and Technical Account Managers (TAMs) had built around single-page search. Reversing the page split wasn't the right call. I contracted a full-stack developer to build a custom Sphinx extension that returns configuration settings as first-class search results, including name, description, defaults, and environment variable syntax, without requiring a click-through. The workflow concern disappeared.

- **Outcome**: Support tickets and TAM inquiries about configuration settings dropped sharply. The most consistent direct feedback from customers in production: getting the full configuration answer in the search result made high-stakes work faster.

### Advanced Permissions Backend Infrastructure

[Docs page](https://docs.mattermost.com/administration-guide/onboard/advanced-permissions-backend-infrastructure.html) · [2020 archived state](https://web.archive.org/web/20201104171059/https://docs.mattermost.com/deployment/permissions-backend.html) · [Academy video lesson](https://academy.mattermost.com/courses/2146232/lectures/51522838)

Mattermost's permissions system controls who can do what in a security-critical, self-hosted platform. When I took over the page, it listed 65 permissions with a name, scope, and one-line description. No built-in roles. No per-role permission assignments. No SKU availability. No API guidance. And permission-level changes were shipping in Engineering PRs without triggering doc updates.

- **What I built**: 15+ built-in roles fully documented with complete permission sets, representing several hundred individual permission assignments. SKU availability across the full permissions surface. API guidance for retrieving permissions by role name. An Academy course I wrote, recorded, and produced independently.

- **The discovery**: While researching the codebase, I found that admins with direct database access can define custom roles with custom permission contexts by modifying the Roles and Schemes tables directly. Engineering hadn't documented it because they don't encourage direct database modification. But this is a self-hosted product, and expert admins have a legitimate path to permissions customization most didn't know existed. I put it in the Academy video lesson, not the official docs. That was the right call for the audience and the risk level. When Engineering reviewed the Academy video for technical accuracy, several developers who had been at Mattermost for years said they had no idea the system supported this. Some went to the codebase to verify before they believed it.

- **The SME gap**: As the original developers of the permissioning system moved on, no one in Engineering could reliably validate whether the documented permissions were complete without deep code analysis. I shifted the validation workflow using Claude to analyze the codebase, confirm published permissions against source, and identify gaps. There were gaps. That made validation faster and more reliable than the SME-dependent process had been.

### Microsoft Intune MAM Configuration

[Docs page](https://docs.mattermost.com/deployment-guide/mobile/configure-microsoft-intune-mam.html) · [PR #8599](https://github.com/mattermost/docs/pull/8599)

A large enterprise customer required Microsoft Intune Mobile Application Management support as a condition of their deployment. This wasn't a normal release cycle feature. Getting it right on first publication mattered.

- **The constraint**: No test environment. No enrolled device. No Intune or Azure AD admin console access. No UI to reference. My only inputs were 3 Engineering codebases, 2 server PRs, 1 mobile PR, and Claude, which I used to analyze each codebase and extract configuration parameters, dependencies, the required sequence of operations, and behaviour that wasn't documented in the Engineering PRs.

- **What I built**: Persona-segmented documentation across multiple pages from the first commit, with distinct paths for IT security teams and risk assessors, administrators configuring Intune, Azure AD, and Mattermost, and end users navigating enrollment and authentication. The developer who built the feature thought in terms of the admin's configuration tasks. I thought in terms of everyone who would need to act, decide, or understand something before the deployment could succeed. The lead mobile engineer's review identified what the code couldn't tell me: only 1 configuration model was supported and any deviation would fail, the prerequisite sequence was rigid, and the UI labels in the draft didn't match production. 30 commits and 4 weeks later, the PR merged.

- **Outcome**: The customer was successfully deployed and onboarded. The Technical Account Manager and lead engineer both said the docs saved the day multiple times during onboarding and built trust with the customer. That one customer opened a category of enterprise doors that required this functionality as table stakes.

---

## Strategic Business Impact

#### Defense & Intelligence Sales Enablement
* **Project:** Mobile Deployment Overhaul for Regulated Industries.
* **Impact:** Restructured mobile deployment into 3 comprehensive guides covering air-gapped environments, custom builds, and EMM integration (Intune/MAM).
* **Result:** Directly enabled enterprise sales closures in Defense/Intel sectors by providing necessary technical verification.

#### Plugin Ecosystem (Developer Experience)
* **Project:** Centralization of Integration Documentation.
* **Impact:** Consolidated 9+ plugin docs from fragmented GitHub READMEs (GitHub, Jira, Zoom) into unified product documentation.
* **Result:** Improved discoverability and developer experience, reducing fragmentation in the integration ecosystem.

#### Product Docs Infrastructure Modernization
* **Project:** Platform Modernization & Sphinx Architecture.
* **Role:** Technical Director. Defined vision and directed full-stack contractors through 51+ infrastructure PRs.
* **Result:** Modernized build pipelines and migrated from ReadTheDocs to a high-performance Furo theme.

#### Security, Logging, & Audit Compliance
* **Project:** Enterprise Compliance Documentation.
* **Impact:** Replaced legacy docs with comprehensive logging system guides covering audit events and AD/LDAP configurations.
* **Result:** Essential for compliance in regulated industries and positioning for Enterprise Advanced tier sales.

---

## Stack

- **Docs platforms**: Sphinx, Furo, Markdown, reStructuredText
- **Workflows**: GitHub, Git, GitHub Actions, docs-as-code pipelines
- **Scripting**: Python, Bash
- **AI-integrated workflows**: Claude for codebase analysis, PR monitoring, draft pipelines
- **Domains**: Self-hosted enterprise platforms, DevSecOps, air-gapped environments, compliance documentation (SOC2, HIPAA adjacent), Defence and Intelligence sectors

---

Ontario, Canada · Open to remote roles · [LinkedIn](https://linkedin.com/in/carriewarner)
