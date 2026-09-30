# Awesome-Cloud-Native-Application-Protection-Platform

# Top Cloud Native Application Protection Platform (CNAPP) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on CSPM, CWPP, CIEM, IaC Security & Attack Path Analysis*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Native Application Protection Platforms (CNAPP)**. These tools help security teams protect cloud-native applications across the full lifecycle—from code and infrastructure-as-code through runtime workloads, identities, and data—by unifying posture management, workload protection, entitlement analysis, and threat detection.

**Examples** include Wiz, Orca Security, Palo Alto Prisma Cloud, Microsoft Defender for Cloud, CrowdStrike Falcon Cloud Security, Tenable Cloud Security, Lacework, Sysdig Secure, Check Point CloudGuard, and SentinelOne Singularity Cloud (the category leaders).

**Open-source emphasis**: CNAPP is a **deeply commercialized category**—no single open-source platform matches the unified scope of Wiz or Prisma Cloud. However, the open-source ecosystem provides **production-grade building blocks** for each CNAPP pillar: **Prowler** and **ScoutSuite** for CSPM, **Falco** and **Tetragon** for CWPP, **Cloudsplaining** and **PMapper** for CIEM, **Checkov** and **Trivy** for IaC/container scanning, and **Cartography** for attack path graph analysis. This section documents these components honestly, including the significant integration work required to assemble a unified CNAPP.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Wiz](https://www.wiz.io/)**
  **The fastest-growing CNAPP, built on the Wiz Security Graph.** Agentless-first architecture that scans cloud workloads without deploying agents, correlating findings across compute, identity, network, data, and code. **Wiz Defend** (cloud detection and response), **Wiz Code** (IaC and code scanning), **Wiz Cloud** (CSPM, CWPP, CIEM, DSPM), and **Wiz Defend AI-SPM** for AI workload security. **CNAPP market share leader** as of 2026.

- **[Orca Security](https://orca.security/)**
  **Agentless-first CNAPP pioneer.** Uses **SideScanning** technology that reads cloud workload block storage out-of-band to detect vulnerabilities, malware, and misconfigurations without agents. Provides **100% coverage** across AWS, Azure, GCP, Alibaba, and Oracle Cloud. Unified platform for CSPM, CWPP, CIEM, DSPM, and CI/CD security.

- **[Palo Alto Prisma Cloud](https://www.paloaltonetworks.com/prisma/cloud)**
  **The most comprehensive CNAPP, assembled from Twistlock and RedLock acquisitions.** Provides **CSPM, CWPP, CIEM, IaC, and data security** in a single platform. Named a **Leader in 2025 Gartner Magic Quadrant for CNAPP** . Provides **Kubernetes CIS Benchmark** checks with severity scoring and continuous image scanning.

- **[Microsoft Defender for Cloud](https://www.microsoft.com/en-us/security/business/microsoft-defender-cloud)**
  **Native CNAPP for Azure, extended to AWS and GCP via Azure Arc.** Provides CSPM (with Secure Score), CWPP, DevOps security, and AI security posture management (AI-SPM). Integrates with Microsoft Defender XDR for unified incident correlation. **Free foundational CSPM tier** available.

- **[CrowdStrike Falcon Cloud Security](https://www.crowdstrike.com/)**
  **Real-time CNAPP with EDR lineage and threat intelligence.** Unifies agentless and agent-based protection with **Falcon Cloud Security** for CSPM, CWPP, CIEM, and container security. **Real-time CDR** analyzes cloud activity as it happens using event streaming (not batch log processing) and stops breaches in seconds. **Extended to Google Cloud** (April 2026) with regional data sovereignty.

- **[Tenable Cloud Security](https://www.tenable.com/)**
  **Best-in-class dedicated CIEM, now integrated into Tenable's broader exposure management.** Acquired Ermetic to add cloud identity security with **granular CIEM analysis, automated least-privilege recommendations, and cross-cloud identity correlation** .

- **[Lacework](https://www.lacework.com/)**
  **Polygraph Data Platform for cloud security.** Uses machine learning and behavioral analytics to detect anomalies across AWS, Azure, GCP, and Kubernetes. **Lacework FortiCNAPP** integration with Fortinet consolidates cloud security into a unified platform.

- **[Sysdig Secure](https://sysdig.com/)**
  **Falco-powered CNAPP with best-in-class runtime detection.** Provides **runtime threat detection, vulnerability scanning, compliance, and cloud detection and response (CDR)** with eBPF instrumentation. **5-second threat detection** validated by SE Labs. Gartner Peer Insights: 4.9 stars across 91 reviews. Strong detection quality with low false positives .

- **[Check Point CloudGuard](https://www.checkpoint.com/)**
  **Unified CNAPP with strong network security integration.** Provides CSPM, CWPP, CIEM, IaC scanning, and cloud network security. **CloudGuard WAF** for application protection and **CloudGuard Posture Management** for compliance.

- **[SentinelOne Singularity Cloud](https://www.sentinelone.com/)**
  **AI-powered CNAPP with autonomous response.** Provides **Singularity Cloud Security** (CSPM, CWPP, CIEM), **Singularity Cloud Workload Security** (runtime), and **Singularity Data Lake** for security analytics. **Storyline** technology automates attack narratives across cloud and endpoint.

## Open-Source GitHub Projects

### CSPM & Posture Assessment

- **[Prowler](https://github.com/prowler-cloud/prowler)**
  **The most widely used open-source CSPM tool.** **12,000+ GitHub stars**, **Apache-2.0 licensed** . Covers **AWS, Azure, GCP, and Kubernetes** with **800+ checks** mapped to CIS benchmarks, NIST, PCI DSS, HIPAA, GDPR, and more . **Key capabilities**: Automated security assessments; **multi-cloud support**; custom check development; **compliance frameworks** (CIS, NIST, PCI, ISO 27001, SOC 2, HIPAA, GDPR); HTML, JSON, CSV, and JUnit output; **integration with AWS Security Hub, Azure Defender, and GCP Security Command Center** . **Deployment**: CLI, Docker, and AWS Lambda . **Companion tool**: **Prowler Studio** for custom check creation.

- **[ScoutSuite](https://github.com/nccgroup/ScoutSuite)**
  **Multi-cloud security auditing tool from NCC Group.** **6,000+ GitHub stars**, **GPL-2.0 licensed** . Supports **AWS, Azure, GCP, Alibaba Cloud, and Oracle Cloud Infrastructure** . **Key features**: Automated security configuration assessment; **rule-based findings** with severity scoring; HTML report generation; **multi-account and multi-subscription support**; **Docker deployment** . **Companion tool**: **ScoutSuite2** for enhanced reporting.

- **[CloudQuery](https://github.com/cloudquery/cloudquery)**
  **Open-source data movement framework for cloud asset inventory and CSPM.** Syncs data from cloud providers to SQL databases for relational analysis. **First-class support for AWS, GCP, and Azure** . Enables custom CSPM queries through SQL.

### CWPP & Runtime Security

- **[Falco](https://github.com/falcosecurity/falco)**
  **The CNCF-graduated runtime threat detection engine and the foundation of open-source CWPP.** Created by Sysdig, donated to CNCF, graduated in 2024. Monitors **system calls** and checks them against rules to detect suspicious activity. **Key capabilities**: Broadest community rule library; **Kubernetes audit log monitoring**; cloud events via APIs and plugins; **MITRE ATT&CK-aligned** predefined rules; PCI DSS and SOC 2 compliance support. **Extensible** via Falcosidekick (alert routing), Falco plugins, **Falco Talon** (no-code threat management), and Falcoctl (rule lifecycle management). **Apache-2.0**.

- **[Tetragon](https://github.com/cilium/tetragon)**
  **eBPF-native runtime security and observability enforcement from Isovalent (Cisco).** Unlike Falco (userspace rule engine), Tetragon runs eBPF-native: **TracingPolicies** define observation and optional **in-kernel enforcement**, including killing a process before the syscall completes. **Kubernetes Identity Aware Policies** (v1.1) enable granular policy application to specific pods or namespaces. **Default Ruleset** for enterprise users provides out-of-the-box monitoring. Runs lower p99 CPU overhead than Falco. **Apache-2.0**.

- **[Tracee](https://github.com/aquasecurity/tracee)**
  **eBPF-native runtime security and forensics from Aqua Security.** Built-in signature library plus **Rego policy** support. **Apache-2.0**.

- **[KubeArmor](https://github.com/kubearmor/KubeArmor)**
  **LSM-based runtime security from AccuKnox (AppArmor, SELinux, BPF-LSM).** Enforces policy at the kernel rather than only observing. **Apache-2.0**.

- **[Kubescape node-agent](https://github.com/kubescape/node-agent)**
  **eBPF-based runtime detection agent for Kubernetes from Kubescape.** **Key components**: Tracer Manager, Rule Manager (**CEL expressions**), Profile Manager, Malware Manager (**ClamAV scanning**), SBOM Manager (**Syft**). **Built-in gadgets**: exec, open, network, dns, capabilities, seccomp, etc. **Detection Rules**: CEL-based rules as Kubernetes Custom Resources. **Apache-2.0**.

### CIEM & Identity Analysis

- **[Cloudsplaining](https://github.com/salesforce/cloudsplaining)**
  **AWS IAM policy analysis tool from Salesforce.** Identifies least-privilege violations by parsing IAM policies to flag resource exposure and privilege escalation potential. Delivers findings via **risk-prioritized HTML report**. **35% coverage** across AWS IAM privilege escalation paths. **Open source**.

- **[PMapper (Principal Mapper)](https://github.com/nccgroup/PMapper)**
  **Privilege escalation pathfinding tool.** Uses a **graph model** to analyze trust policies and resource-based policies. Answers "who can reach what" by simulating authorization decisions to find actual escalation routes. **33% coverage** across AWS IAM privilege escalation paths. **Open source**.

- **[policy_sentry](https://github.com/salesforce/policy_sentry)**
  **Preventative policy generation tool from Salesforce.** Allows engineers to declare required access levels via **YAML templates** to automatically generate least-privilege IAM policies, reducing reliance on dangerous wildcards. **Open source**.

### IaC & Container Scanning

- **[Checkov](https://github.com/bridgecrewio/checkov)**
  **Open-source static analysis tool for Infrastructure as Code with 750+ built-in policies.** Language: **Python/YAML checks**. Scope: **Terraform, CloudFormation, Kubernetes, Helm, ARM** . **Deeper Terraform graph analysis** than alternatives. Available as **JetBrains IDE plugin** with real-time scan results and inline fix suggestions. **AWS CDK validator plugin** available.

- **[Trivy](https://github.com/aquasecurity/trivy)**
  **The default open-source container and IaC scanner.** One fast binary scans **container images, filesystems, IaC, and Kubernetes manifests**, generates SBOMs in CycloneDX and SPDX formats, and detects secrets. Consumes **distribution security advisories** to filter OS-package findings against what each distro has actually patched, avoiding NVD false positives. **Apache-2.0**.

- **[Grype](https://github.com/anchore/grype)**
  **Best for local, privacy-conscious, SBOM-first scanning.** Pairs with **Syft** for SBOM generation. The SBOM-first workflow allows generating the SBOM once at build time and **re-scanning that SBOM against updated vulnerability data** without pulling the image again. Supports **EPSS, KEV, and risk scoring** for threat prioritization. **Apache-2.0**.

- **[Syft](https://github.com/anchore/syft)**
  **The SBOM generator that Grype pairs with.** In head-to-head testing against 60 container images, Syft was the **most complete at 96% of expected components**, ahead of Trivy (94%) and Docker Scout (87%). **Apache-2.0**.

### Attack Path & Graph Analysis

- **[Cartography (Lyft)](https://github.com/lyft/cartography)**
  **Infrastructure graphing and querying platform.** Ingests cloud assets into a **Neo4j graph database** to enable cross-boundary queries. Provides the underlying data structure for advanced attack path analysis—map identities, resources, and their relationships for "who can reach what" analysis. **Open source**.

### Additional Strong Open-Source Options

- **CSPM**: **Prowler** (12k+ stars, 800+ checks), **ScoutSuite** (6k+ stars, multi-cloud), **CloudQuery** (SQL-based inventory) .
- **CWPP**: **Falco** (CNCF graduated, broadest rules), **Tetragon** (eBPF-native enforcement), **Tracee** (Rego policies), **KubeArmor** (LSM enforcement), **Kubescape node-agent** (CEL rules, ClamAV, SBOM) .
- **CIEM**: **Cloudsplaining** (AWS IAM analysis), **PMapper** (privilege escalation graphs), **policy_sentry** (policy generation) .
- **IaC/Container**: **Checkov** (750+ policies), **Trivy** (all-in-one scanner), **Grype** (SBOM-first), **Syft** (96% SBOM completeness) .
- **Graph Analysis**: **Cartography** (Neo4j infrastructure graph) .

**Frameworks for building custom systems**: Combine **Prowler** for multi-cloud CSPM with 800+ checks, **Falco** or **Tetragon** for CWPP runtime detection and enforcement, **Cloudsplaining** and **PMapper** for CIEM analysis, **Checkov** and **Trivy** for IaC and container scanning, and **Cartography** for attack path graph analysis. Add **Neo4j** for graph storage, **PostgreSQL** for inventory, and **Prometheus + Grafana** for observability.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- CNAPP platforms handle sensitive cloud telemetry, vulnerability, and identity data; ensure proper access controls and compliance with organizational security policies.
- **Open-source reality**: **No single open-source CNAPP platform matches the unified scope of Wiz, Prisma Cloud, or CrowdStrike.** The open-source ecosystem provides **production-grade components** for each CNAPP pillar: **Prowler** (CSPM), **Falco/Tetragon** (CWPP), **Cloudsplaining/PMapper** (CIEM), **Checkov/Trivy** (IaC/container), and **Cartography** (attack path graphs). Assembling these into a unified CNAPP requires **significant integration engineering, custom correlation logic, and ongoing operational investment**—typically 0.5–2 FTE for a mid-sized cloud environment. For organizations without dedicated cloud security engineering capacity, commercial platforms (Wiz, Orca, Prisma Cloud, Defender for Cloud) provide **faster time-to-value, unified risk correlation, and enterprise support** that open-source assembly cannot match without substantial investment.

---

**Made for cloud security architects, DevSecOps teams, SOC analysts, and platform security engineers.**
Let's make cloud-native application protection more open, transparent, and actionable.
