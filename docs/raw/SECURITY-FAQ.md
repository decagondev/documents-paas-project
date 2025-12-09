# Security FAQ

1. **Which scanner software is being used?**  
   Purely open-source and bespoke, no proprietary scanners at all:  
   - Container / SBOM / supply-chain: Trivy, Grype, Syft (latest 2025 versions)  
   - Runtime & host scanning: OpenVAS/GVM 22.4+ (our own fork with reduced noise and custom NASL checks), plus ~1,400 in-house Nuclei templates we maintain ourselves (many derived from red-team exercises)  
   - Custom AI-enhanced layer: our own lightweight ML models (scikit-learn + PyTorch) that sit on top of the above tools for anomaly scoring, dependency-graph risk analysis, and false-positive suppression  
   Everything is orchestrated via GitLab runners and our internal scan scheduler – fully auditable, no black-box commercial engines.

2. **Is OT (operational technology) also being scanned?**  
   Not in the standard PaaS delivery – the platform is built for regulated IT/cloud-native workloads.  
   When customers explicitly need OT visibility (e.g., energy, manufacturing), we integrate on a project basis with open-source/passive tools (GrassMarlin, PLCscan, Zeek ICS extensions) or federate with an existing Nozomi/Claroty deployment via API. No active OT scanning is performed unless the customer’s OT team signs off and we write safe, custom Scapy-based queries together.

3. **Are there agents available for device monitoring? (EDR/XDR functions)**  
   Yes – deliberately lightweight and open-source:  
   - Primary runtime/agent: Falco (eBPF + kernel hooks) for container and host behavioral monitoring  
   - Host-level collection and basic EDR: Wazuh agents (we deploy the open-source version,, no HIPS component enabled by default)  
   - Central correlation: Wazuh manager + OpenSearch cluster + our own alert triage rules  
   No commercial EDR/XDR (CrowdStrike, SentinelOne, etc.) is bundled. Customers who already run one can forward via syslog/STIX/TAXII.

4. **How is compliance ensured on the devices?**  
   Immutable, hardened baseline + continuous verification:  
   - OS: Debian 13 with full-disk encryption, measured boot (TPM 2.0), and custom SELinux enforcing policies (we ship ~400–450 types/roles depending on edition)  
   - Patch & config management: unattended-upgrades + Ansible playbooks locked to our golden image; all packages and container images are re-validated with Trivy/Grype on every update  
   - Zero-trust networking: rootless Podman, WireGuard service mesh, nftables deny-by-default  
   - Drift detection: daily OpenSCAP scans against CIS L1/L2 + our own stricter profiles, plus Wazuh File Integrity Monitoring  
   Compliance is enforced by design and automation – not by a separate commercial tool.

5. **Which part of the software has been certified?**  
   Important clarification under the new company structure:  
   - Individual open-source components carry their own upstream certifications where applicable (e.g., Debian in scope for some BSI/DISA listings, Podman/Falco FIPS-validated crypto modules when built correctly, SELinux policies audited by Red Hat, etc.).  
   - The overall integrated platform is **bespoke per deployment** and is **not pre-certified as a product**.  
   - Each customer deployment must undergo its own certification or conformance process in situ (ISO 27001 scope extension, SOC 2 bridging attestation, BSI C5 site audit, TISAX assessment, etc.).  
   We provide full documentation packages, SBOMs, penetration-test reports from our red team, and hardened reference architectures so that your auditors or regulators can certify the actual running system quickly – many customers have already done this successfully in 2024–2025.

6. **What exactly is the role of the AI within the system?**  
   Very focused and transparent:  
   - Post-processing of Trivy/Grype/Nuclei/OpenVAS findings → risk scoring and false-positive reduction  
   - Behavioral baselining on Falco events (small supervised models we retrain quarterly with our own red-team data)  
   - Supply-chain anomaly detection on SBOM dependency graphs  
   No autonomous response, no generative LLMs, no magic – just explainable ML that security analysts can override or retrain.

7. **Which security areas is the solution supposed to cover?**  
   Sovereign, cloud-native PaaS with strong DevSecOps and supply-chain focus:  
   - Secure software supply chain (SBOM + signing + scanning)  
   - Hardened container runtime & host protection  
   - Vulnerability management (open-source stack)  
   - Runtime threat detection (Falco + Wazuh)  
   - Compliance automation and audit readiness  
   It is explicitly **not** a full commercial SOC/NOC replacement. Customers either run their own security operations on top or contract our managed security team (12–38 people depending on edition) for 24/7 monitoring and response.

8. **Overall: will this system belong to us or run fully within our infrastructure? Multi-site plans?**  
   Yes – 100 % customer-owned and customer-operated (or operated by us on your behalf under strict German/UAE data-sovereignty rules).  
   - Everything can run completely on-premise or in your private cloud – no data or keys ever leave your control.  
   - Multi-site rollouts are fully supported: we have reference deployments today across Frankfurt, Dubai, and two customer sites in Austria/Switzerland. Adding another site is just shipping more nodes and extending the WireGuard mesh + OpenSearch federation.
