# Product Requirements Document (PRD)  
ACCELERATOR EDITION – The Immediate Secure PaaS  
Version 1.0 | December 2025 | Classification: Public / Open Source Friendly

### 1. Product Name & Positioning
**Internal Codename:** ACCELERATOR  
**Public Name (TBA):** [YourBrand] Secure Platform / [YourBrand] Cloud  
**Tagline:** “The most secure platform you can run production on in 2026 – open-source core, zero excuses.”

This is the €15 M, 9–18 month sprint that ships the exact same DNA as Fortress/Enterprise but stripped to what can be built, hardened, and sold tomorrow.

### 2. The Five Accelerator Promises (contractually enforceable from day one)

| # | Promise | How we deliver it in v1.0 |
|---|---------|----------------------------|
| 1 | SELinux enforcing from first boot – forever | Kernel boot param + lockdown=confidentiality + immutable grub |
| 2 | No process ever runs as root | 100 % rootless Podman + user namespaces + Bubblewrap |
| 3 | Every deploy is automatically scanned and blocked if dangerous | Built-in GitHub Actions runners + Trivy + Grype + Syft + lightweight open-source AI agent |
| 4 | Only ports 22 and 443 open to the internet | Immutable ufw/nftables rules baked into image |
| 5 | One-click sovereign deployment (Germany or UAE) | Pre-built images + Terraform module for Maincubes/Equinix |

### 3. Final Technology Stack – Accelerator 1.0 (all production-ready today)

| Layer                  | Technology (locked)                                      | Reason |
|------------------------|----------------------------------------------------------|--------|
| Base OS                | Debian 13 minimal netboot                                 | Fastest, most stable |
| Kernel                 | linux-image-amd64 6.6+ with custom hardened config + lockdown=confidentiality | Already DoD-used |
| MAC                    | SELinux enforcing (refpolicy targeted + our 120-type policy) + AppArmor enforcing | Dual MAC = belt + suspenders |
| Filesystem             | ZFS root optional (default on install) – encrypted datasets | Snapshots + checksums |
| Container Runtime      | Rootless Podman 5.x + Buildah + Skopeo                   | Industry shift away from Docker |
| System Containers      | LXD 6.0 (Incus fork) – with snapshotted root           | Lightweight VMs |
| Full VMs               | KVM + libvirt + virt-manager (optional)                  | When you really need one |
| Orchestration          | Simple systemd + custom Bash/Ansible or optional Nomad   | Zero K8s complexity |
| Web UI                 | Accelerator Dashboard – clean React + Cockpit backend, dark corporate theme | One beautiful pane |
| Reverse Proxy          | Traefik v3 – auto LetsEncrypt + mTLS support             | Zero config TLS |
| CI/CD Runners          | Self-hosted GitHub Actions runners (on the same cluster) | No data leaves your cage |
| Supply-Chain Scanning  | Trivy + Grype + Syft + open-source LLM agent (Llama 3 8B fine-tuned) | < 3 min full scan |
| Updates                | Unattended-upgrades + kernel live-patch (optional)       | Near-zero downtime |
| Hardening Extras       | kernel.kptr_restrict=2, dmesg_restrict, protected_fifos/regular, auditd full rules | Standard CIS Level 2 + extra |

### 4. Compliance & Assurance (realistic & fast)

| Item                     | Level Delivered at Launch | Timeline |
|--------------------------|---------------------------|----------|
| SELinux Policy Review    | External red-team + bug bounty | Month 6 |
| Penetration Test         | Two independent firms     | Month 7 |
| SOC 2 Type I             | Ready                     | Month 8 |
| ISO 27001                | Ready                     | Month 10 |
| BSI C5 Type 1            | Ready                     | Month 12 |
| TÜViT light audit        | Optional add-on           | +€80k   |

(No EAL4+ in v1 – that’s Enterprise. But we still beat 99.9 % of clouds on day one.)

### 5. Infrastructure – Accelerator 1.0

| Location       | Initial Footprint | Ownership | Expansion Path |
|----------------|-------------------|-----------|----------------|
| Germany (Frankfurt area) | 1 full rack (42 U, 20 kW) | Long-term lease (Maincubes / Equinix) | +2–3 racks Year 2 |
| Dubai (optional at launch) | ½ rack co-lo     | Lease     | Full rack when needed |

### 6. MVP Scope – Accelerator 1.0 (public launch Month 9)

| Epic | Deliverable | Done When |
|------|-------------|-----------|
| E1   | Hardened bootable ISO + Calamares installer (ZFS + full disk encryption profile) | Month 4 |
| E2   | Accelerator Dashboard v1 + one-click deploy of Traefik + Podman + LXD | Month 5 |
| E3   | Self-hosted secure GitHub Actions runners + full scanning pipeline | Month 6 |
| E4   | 30 paying customers live + €1 M ARR run-rate | Month 9 |
| E5   | Public documentation + Terraform modules + marketplace templates | Month 9 |

### 7. Explicit Non-Goals (Accelerator 1.0)
- Kubernetes (we will never ship K8s)  
- Formal verification or EAL4+  
- Serverless / FaaS  
- GPU / AI training workloads  
- Multi-region active-active in v1

### 8. Success Metrics (18 Months)
- ≥ 300 paying customers  
- ≥ €25 M ARR  
- < 5 support tickets per week about “security”  
- Public GitHub repo > 15 k stars  
- Zero successfull public exploits

This is the platform that ships next year, makes money immediately, and becomes the default secure substrate for every startup and mid-size company that actually cares.

All three PRDs complete:  
FORTRESS → ENTERPRISE → ACCELERATOR

Your move – which one do we build first? (Most founders pick Accelerator → cash-flow → fund Enterprise → dream of Fortress.)
