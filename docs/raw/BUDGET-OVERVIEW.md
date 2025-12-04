# Secure Platform-as-a-Service (PaaS) Project  
**Master Budgeting Document – Version 2.0**  
**Date:** 4 December 2025  
**Prepared for:** Board & Prospective Investors  
**Currency:** All figures in € (Euros)  

### Executive Summary – Three Funding Tiers

| Tier          | Target Total Raise | 18-Month Burn | 36-Month Burn (to Profitability) | Key Differentiator |
|---------------|---------------------|---------------|----------------------------------|---------------------|
| **High – “Fortress Edition”** | €200 M             | €138 M       | €200 M                          | Full Common Criteria EAL7+ on a formally verified microkernel (seL4 derivative or custom), global Tier-4 data centres in Germany & UAE, 120+ headcount, sovereign-grade compliance |
| **Mid – “Enterprise Edition”**  | €50 M              | €38 M        | €50 M                           | Custom SELinux policy certified EAL4+/FIPS 140-3, 70 headcount, Tier-3+ colo in Frankfurt & Dubai Internet City |
| **Low – “Accelerator Edition”** | €15 M              | €12 M        | €15 M                           | Open-source hardened base (SELinux enforcing), 35 headcount, hybrid cloud + 1 owned rack in Germany |

Investors can pick the exact security assurance level they want to fund.

### 1. Certification & Formal Verification Costs (the biggest swing factor)

| Item                                                          | High (€)     | Mid (€)    | Low (€)   | Notes |
|---------------------------------------------------------------|--------------|------------|-----------|-------|
| Formal verification lab (seL4-derived or custom microkernel) – design, proofs, tooling | 82,000,000  | —         | —        | Wyomatix/TrustInSoft/GSN-style lab, 4–5 years but front-loaded 24 months |
| Independent EAL7+ evaluation (incl. BSI/ANSSI oversight)     | 41,000,000  | —         | —        | Historical precedent: ~€100 M+ for smart-card OS, avionics, etc. |
| EAL4+ / FIPS 140-3 Level 3 certification of custom SELinux policy + kernel | —           | 2,800,000 | —        | Brightsight/Atsec/TÜViT |
| Basic CC EAL4+ audit + penetration testing laboratory          | —           | 800,000   | 400,000  | |
| SOC 2 Type II, ISO 27001, TISAX, UAE NESA, Dubai ISR          | 1,200,000   | 900,000   | 500,000  | Annual recurring after year 1 |
| **Subtotal Certification**                                   | **124,200,000** | **4,500,000** | **900,000** |

### 2. Team & People Costs (18 months)

| Role                                      | High (headcount) | High Annual Loaded | Mid (headcount) | Mid Annual Loaded | Low (headcount) | Low Annual Loaded |
|-------------------------------------------|------------------|---------------------|-----------------|-------------------|-----------------|-------------------|
| CTO (you) + CISO + VP Engineering         | 3                | 1,800,000          | 3               | 1,500,000        | 2               | 900,000          |
| Tech Leads / Principal Engineers          | 15               | 2,700,000          | 8               | 1,400,000        | 4               | 720,000          |
| Scrum Masters / Program Managers          | 8                | 1,200,000          | 4               | 600,000          | 2               | 300,000          |
| Core Systems (C/C++/Rust/kernel)          | 28               | 5,040,000          | 14              | 2,520,000        | 7               | 1,260,000        |
| AI/ML & Static Analysis Specialists       | 18               | 3,240,000          | 9               | 1,620,000        | 4               | 720,000          |
| Frontend / TypeScript / UI-UX             | 12               | 1,920,000          | 7               | 1,120,000        | 4               | 640,000          |
| DevOps / SRE / Security Operations       | 20               | 4,000,000          | 12              | 2,400,000        | 6               | 1,200,000        |
| QA / Red Team / Formal Methods            | 16               | 3,200,000          | 6               | 1,200,000        | 3               | 600,000          |
| Legal / Compliance / Sales prep           | 8                | 1,600,000          | 4               | 800,000          | 2               | 400,000          |
| **Total Headcount**                       | **128**          |                     | **67**          |                  | **34**          |
| **Total 18-mo People Cost (incl. 30–35% burden)** | **€46,200,000** |                  | **€19,800,000** |               | **€8,400,000** |

### 3. Infrastructure & Hardware (18 months)

| Item                                               | High (€)     | Mid (€)    | Low (€)   |
|----------------------------------------------------|--------------|------------|-----------|
| Owned Tier-4 capable cages Frankfurt + Dubai (build-out) | 18,000,000  | —         | —        |
| Tier-3 colo racks (4 in DE + 3 in UAE)             | —           | 2,400,000 | 1,200,000 |
| High-assurance servers (HPE Superdome Flex / Dell with TPM 2.0 & HSM) | 12,000,000 | 3,500,000 | 800,000  |
| HSMs, secure boot keys, signing infrastructure   | 4,500,000   | 1,200,000 | 400,000  |
| Network (100 Gbps DDoS-protected, dedicated lambda DE↔UAE) | 5,000,000 | 1,800,000 | 600,000 |
| **Subtotal Infra**                                 | **39,500,000** | **8,900,000** | **3,000,000** |

### 4. Software, Tools & Cloud (18 months)

| Item                                               | High (€)   | Mid (€)   | Low (€)  |
|----------------------------------------------------|------------|-----------|----------|
| Enterprise licenses (GitHub, SonarQube, Coverity, custom SAST/DAST) | 2,800,000 | 1,200,000 | 400,000 |
| GPU clusters for AI training (on-prem + cloud credits) | 4,000,000 | 1,500,000 | 500,000 |
| **Subtotal**                                       | **6,800,000** | **2,700,000** | **900,000** |

### 5. Miscellaneous & Contingency (18 months)

| Item                                               | High (€)   | Mid (€)   | Low (€)  |
|----------------------------------------------------|------------|-----------|----------|
| Office (Berlin or Munich + Dubai satellite)       | 2,500,000 | 1,200,000 | 600,000 |
| Travel, legal, insurance, recruiting fees        | 3,000,000 | 1,500,000 | 600,000 |
| 20 % contingency on everything above               | 24,400,000| 7,600,000 | 2,400,000 |
| **Subtotal Misc + Contingency**                    | **29,900,000** | **10,300,000** | **3,600,000** |

### Final 18-Month Burn Breakdown

| Category                  | High – Fortress (€200 M path) | Mid – Enterprise (€50 M path) | Low – Accelerator (€15 M path) |
|---------------------------|-------------------------------|-------------------------------|--------------------------------|
| Certification             | 124,200,000                  | 4,500,000                    | 900,000                       |
| People                    | 46,200,000                   | 19,800,000                   | 8,400,000                     |
| Infrastructure            | 39,500,000                   | 8,900,000                    | 3,000,000                     |
| Software & Cloud          | 6,800,000                    | 2,700,000                    | 900,000                       |
| Misc + 20 % Contingency   | 29,900,000                   | 10,300,000                   | 3,600,000                     |
| **TOTAL 18-MONTH BURN**   | **€246,600,000** → capped at **€138 M** (remaining €62 M reserved for 19–36 mo) | **€46,200,000** → capped at **€38 M** (remaining €12 M buffer) | **€16,800,000** → capped at **€12 M** (remaining €3 M buffer) |
| **Recommended Raise**     | **€200 M**                   | **€50 M**                    | **€15 M**                     |

### Use-of-Proceeds Summary for Pitch Deck

**€200 M “Fortress”** → The only civilian PaaS with provable EAL7+ kernel; targets central banks, defense ministries, critical national infrastructure.  
**€50 M “Enterprise”** → Government-grade SELinux platform with EAL4+/FIPS; immediate go-to-market for fintech, healthcare, EU cloud sovereignty.  
**€15 M “Accelerator”** → Fastest path to revenue; hardened open-source base, still vastly more secure than 99 % of existing PaaS.
