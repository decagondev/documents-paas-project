# Product Requirements Document (PRD)  
ENTERPRISE EDITION – Government-Grade Secure PaaS  
Version 1.0 | December 2025 | Classification: Public

### 1. Product Name & Positioning
**Internal Codename:** ENTERPRISE  
**Public Name (TBA):** [Redacted – Sovereign Enterprise Cloud / Regulated Secure Cloud]  
**Tagline:** “The platform that passes BSI C5, DORA, NIS2, and NESA audits on day one – without apologies.”

This is the €50 M, 24-month programme that delivers the highest-assurance platform you can actually buy and run production workloads on in 2026–2027.

### 2. Non-Negotiable Enterprise Guarantees
(These are contractually enforceable and regulator-accepted)

| # | Guarantee | Assurance Method |
|---|-----------|------------------|
| 1 | SELinux enforcing mode from first boot – never disabled | Boot parameter + kernel lockdown + measured boot |
| 2 | Every container and VM confined by a unique SELinux type + AppArmor profile | Custom policy with 400+ types, certified EAL4+ |
| 3 | Zero trust networking: only 22 + 443 open by default, everything else blocked by host firewall + eBPF | Immutable nftables + Cilium replacement |
| 4 | Full supply-chain provenance and vulnerability blocking before deployment | AI agents + Trivy Enterprise + in-house C/C++/Java/JS static analysis |
| 5 | All encryption keys stay inside EU/UAE jurisdiction at all times | HSM-backed KMS (Thales Luna / Utimaco) in Frankfurt & Dubai |
| 6 | Immutable root filesystem with full audit trail | OSTree-style updates + git-backed /etc |

### 3. Core Technology Stack (Enterprise Edition)

| Layer                  | Technology (final locked choice)                              | Why it wins regulators & pentesters |
|------------------------|---------------------------------------------------------------|-------------------------------------|
| Base OS                | Debian 13 “Trixie” minimal + custom linux-image-enterprise    | Stability + 10-year LTS + huge ecosystem |
| Kernel                 | linux-image-6.6+ with lockdown=confidentiality + grsecurity-style hardening + custom config | Proven in DoD environments |
| Mandatory Access Control | Custom SELinux policy “enterprise” (targeted + 400 new types) + AppArmor enforcing | Dual MAC – the gold standard for EAL4+ |
| Cryptography           | OpenSSL 3.2 FIPS module + Libsodium + HSM integration         | FIPS 140-3 Level 3 ready |
| Container Runtime      | Rootless Podman 5.x + Bubblewrap + seccomp-bpf                | No root, no privilege escalation |
| System Containers / VMs| LXD 6.0 (Incus fork) + KVM + sVirt + libvirt                  | Lightweight VMs when needed |
| Orchestration          | Nomad 1.9 + Consul + custom Terraform provider               | Simpler & more secure than Kubernetes |
| Storage                | ZFS root (optional ext4) + encrypted datasets                 | Snapshots, compression, checksums |
| Reverse Proxy          | Traefik v3 + auto-LetsEncrypt + mutual TLS                    | Zero-touch HTTPS |
| Web UI                 | Enterprise Dashboard (clean Cockpit + React/TypeScript frontend) | Single pane, corporate dark theme |
| CI/CD Security         | Self-hosted GitHub Actions runners + AI scanning agents + SonarQube Enterprise | Full control, no shared runners |
| Logging & Audit        | auditd + systemd-journal + ELK stack (air-gapped)             | Tamper-proof logs |

### 4. Certification & Compliance Scope

| Certification                  | Target Level          | Lab / Auditor             | Target Date |
|--------------------------------|-----------------------|---------------------------|-------------|
| Common Criteria                | EAL4+ (ALR3)          | Brightsight or atsec      | Q1 2027    |
| FIPS 140-3                     | Level 3 (module)      | Acumen / Lightship        | Q4 2026    |
| BSI C5:2025                    | Type 2 attestation    | TÜViT                     | Q1 2027    |
| ISO 27001 + SOC 2 Type II      | Full scope            | Schellman                 | Q4 2026    |
| TISAX (automotive)             | Label 3               | TÜV SÜD                   | Q2 2027    |
| UAE NESA + Dubai ISR           | Enhanced Grade        | DarkMatter / PwC UAE      | Q3 2027    |

### 5. Infrastructure (Colocation – Sovereign Ready)

| Location       | Provider          | Racks | Power | Ownership Model |
|----------------|-------------------|-------|-------|-----------------|
| Frankfurt      | Maincubes / Equinix FR8 | 4   | 80 kW | Long-term lease + cage |
| Dubai Internet City | Khazna / Equinix DX2 | 3   | 60 kW | Long-term lease + cage |
| Interconnect   | Private VLAN + IPsec/WireGuard tunnel | — | — | — |

### 6. MVP Scope – Enterprise 1.0 (Q1 2027)

| Epic | Deliverable | Success Criteria |
|------|-------------|------------------|
| E1   | Hardened base image + certified SELinux policy | setenforce 1 survives full red-team week |
| E2   | Enterprise Dashboard v1 (React + Cockpit backend) | All critical functions in one UI |
| E3   | Self-hosted secure runners + AI scanning pipeline | Every push scanned in < 4 min |
| E4   | Frankfurt cage live + first 3 paying customers | €3 M ARR at launch |
| E5   | EAL4+ certificate in hand | Signed by Brightsight/atsec |

### 7. Non-Goals (Enterprise 1.0)
- Full microkernel / formal verification (that’s Fortress)  
- Serverless functions in v1  
- GPU workloads in v1  
- Public cloud regions outside DE/UAE

### 8. Success Metrics (24 Months)
- EAL4+ certificate issued  
- ≥ 50 paying customers  
- ≥ €50 M ARR  
- Zero breaches or regulator fines  
- Reference customers in at least three regulated verticals (fintech, health, public sector)

This is the platform that lets you check every compliance box in 2027 – and still ship code every day.
