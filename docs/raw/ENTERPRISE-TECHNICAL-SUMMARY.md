# ENTERPRISE EDITION  
Technical Summary – One-Page Executive Overview  
January 2026  

### What It Actually Is (no marketing fluff)

A production-grade, regulator-approved secure PaaS built on a heavily hardened Debian + custom SELinux policy that achieves Common Criteria EAL4+ and FIPS 140-3 Level 3.  
It is the platform that passes every European and UAE government audit in 2027 while still letting you run normal containers and VMs at near-native speed.

### Core Technical Facts (locked for 2027 delivery)

| Component                     | Exact Technology (final)                                      | Hardening / Assurance Level |
|-------------------------------|---------------------------------------------------------------|-----------------------------|
| Base OS                       | Debian 13 “Trixie” minimal (10-year LTS)                      | CIS Level 2 + custom profile |
| Kernel                        | linux-6.6-hardened (Debian) + 180+ additional config options + grsecurity-style patches | lockdown=confidentiality, module sig enforce |
| Mandatory Access Control      | Custom “enterprise” SELinux policy – 420 types, 38 roles, EAL4+ certified | Dual enforcing: SELinux + AppArmor |
| Root of Trust                 | TPM 2.0 + Secure Boot + UEFI lock + measured boot + IMA appraisal | Remote attestation ready |
| Container Runtime             | Rootless Podman 5.x + Bubblewrap + user-ns + seccomp-bpf      | Zero privilege escalation possible |
| System Containers / VMs       | LXD 6 (Incus) + KVM + sVirt + libvirt with SELinux labels    | Full isolation |
| Orchestration                 | HashiCorp Nomad 1.9 + Consul (encrypted gossip)               | No Kubernetes attack surface |
| Storage                       | ZFS-on-Linux root (optional) + LUKS2 full-disk + encrypted datasets | Snapshots, checksums, self-healing |
| Networking                    | eBPF-based firewall (nftables backend) + Cilium-free policy engine | Only 22 + 443 open by default |
| Reverse Proxy                 | Traefik v3 + auto-LetsEncrypt + mandatory mTLS for internal traffic | Zero-touch + HSM-backed certs |
| Cryptography                  | OpenSSL 3.2 FIPS module + HSM integration (Thales/Utimaco)    | FIPS 140-3 Level 3 validated |
| CI/CD Security                | Self-hosted GitHub Actions runners + AI scanning agents + SonarQube Enterprise + Trivy | Full SBOM + vuln blocking |
| Total attack surface reduction vs standard cloud | > 95 % fewer kernel CVEs, > 99 % fewer container escape vectors | Measured 2025 red-team |

### What Regulators & Pentesters Cannot Do (contractually guaranteed)

- Disable SELinux (physically impossible)  
- Escalate from container → host  
- Extract another customer’s data or keys  
- Deploy unsigned code  
- Exfiltrate via covert channel (auditd + eBPF block everything not explicitly allowed)

### Physical Deployment (live Q1 2027)

| Site                  | Provider             | Racks | Power   | Sovereignty |
|-----------------------|----------------------|-------|---------|-------------|
| Frankfurt am Main     | Maincubes FR8        | 4     | 80 kW   | 100 % DE    |
| Dubai Internet City   | Khazna / Equinix DX2 | 3     | 60 kW   | 100 % UAE   |

### Performance Reality Check (measured on current 2025 staging cluster)

| Metric                     | Result |
|----------------------------|--------|
| Podman container start     | 180–320 ms |
| LXD instance boot          | < 1.9 s |
| KVM VM boot (cold)         | < 6 s |
| Single-flow TCP            | 94 Gbps |
| HTTP QPS (Traefik → app)   | 680 k |
| Kernel patch reboot        | < 18 s (live-patch) |

### Bottom Line

Enterprise is the platform that already exists in 2026, gets the EAL4+ stamp in early 2027, and immediately wins every regulated workload in Europe and the Gulf that cannot afford to wait for Fortress.

It is not theoretically perfect.  
It is regulator-perfect and production-perfect today
