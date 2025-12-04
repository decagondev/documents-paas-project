# ENTERPRISE EDITION  
Secure Platform-as-a-Service (PaaS)  
Investor Deck – €50 Million Series A  
December 2025  

### Title Slide  
ENTERPRISE  
The Government-Grade Secure PaaS  
EAL4+ | FIPS 140-3 | German/UAE Sovereign Cloud | Zero-Trust by Default  

“Most companies need Fort Knox security.  
They just can’t wait 5 years or pay €200 million for it.”  

### The Same Problem – Realistic Time & Budget  
2025–2027 regulatory wave:  
- EU DORA, NIS2, CRA, eIDAS 2  
- German KRITIS & BSI C5:2025  
- UAE NESA, Dubai ISR, Abu Dhabi ADSS  
All require demonstrable high-assurance hosting for fintech, health-tech, critical SaaS, and public-sector workloads – today, not in 2030.

Current “secure” platforms (AWS GovCloud, Azure Confidential, Google Sovereign) still run on the same Linux kernel with 25 M lines of code and no mandatory access control that survives real penetration testing.

### The ENTERPRISE Solution  
A production-ready, regulator-approved secure PaaS launched in < 24 months instead of 5+ years.

| Pillar                              | Technology Choice (Enterprise)                  | Assurance Level |
|-------------------------------------|--------------------------------------------------|-----------------|
| Kernel & MAC                        | Custom Debian-based kernel + certified SELinux policy (targeted + custom types) | EAL4+ augmented |
| Cryptographic Modules               | FIPS 140-3 validated (OpenSSL + custom HSM integration) | Level 3 |
| Root of Trust                       | TPM 2.0 + Secure Boot + measured boot + remote attestation | — |
| Container/VM Isolation              | Rootless Podman + KVM + sVirt + AppArmor enforcing | — |
| Supply-Chain Security               | AI agents in GitHub Actions + on-prem SonarQube Enterprise + Trivy + Syft + in-house C/C++/Java/JS scanners | — |
| Sovereign Infrastructure           | Tier-3+ colocation cages in Frankfurt (Equinix/Maincubes) + Dubai Internet City | Keys never leave EU/UAE |
| Web UI & Automation                 | Clean enterprise dashboard (Cockpit + custom frontend) | — |

Result: The most secure platform you can actually buy and deploy in 2026–2027.

### Target Customers & Pricing (Year 1–3)  

| Segment                          | Example Clients                              | ACV         | Sales Cycle |
|----------------------------------|----------------------------------------------|-------------|-------------|
| Regulated Fintech & Insurtech    | N26, Solaris, Wefox, Allianz direct          | €800k–€3 M | 6–9 mo     |
| Health-tech & Pharma             | Doctolib, Ada Health, Roche Diagnostics      | €1–4 M     | 9–12 mo    |
| Public Sector & GovTech          | German federal states, UAE smart-city projects| €2–8 M     | 12–18 mo   |
| Critical SaaS (EU-based)         | Personio, Celonis, Forto                     | €600k–€2 M| 4–8 mo     |

Conservative Year 3 ARR target with €50 M raise: €78 M (120 customers averaging €650 k)

### Use of Proceeds – €50 Million  

| Category                                      | Amount (€M) | %    | Details |
|-----------------------------------------------|-------------|------|-----------------------------------------------------|
| SELinux Policy Development & EAL4+ Certification| 4.5        | 9%   | Brightsight/atsec/TÜViT sponsorship, full penetration lab |
| Sovereign Colo Build-out (Frankfurt + Dubai)  | 8.9        | 18%  | 4 racks DE + 3 racks UAE, HSMs, private interconnect |
| Team (67 heads → 110 heads by Year 3)         | 19.8       | 40%  | Berlin HQ + Dubai satellite, heavy C/C++/Python/DevOps |
| AI Supply-Chain Security R&D + GPU cluster   | 4.2        | 8%   | On-prem scanning cluster + proprietary models |
| Go-to-Market, Compliance & First 10 Logos     | 8.0        | 16%  | Legal, audits (SOC 2, ISO 27001, TISAX, NESA), marketing |
| Working Capital + 20 % Contingency            | 4.6        | 9%   | Buffer + 18-month runway post-MVP |
| **Total**                                     | **50**      | 100% | |

### Milestones – 24 Months to Positive Cash Flow  

| Quarter      | Milestone |
|--------------|------------|
| Q1 2026      | Company incorporated, first 35 hires, SELinux policy repo frozen |
| Q3 2026      | Private beta with 3 design partners (German fintech + UAE gov entity) |
| Q1 2027      | EAL4+ certificate issued + BSI C5 attestation |
| Q2 2027      | Public launch – first 10 paying customers |
| Q4 2027      | €18 M ARR run-rate |
| Q2 2028      | Break-even |

### Why This Beats Every Competitor Today  
| Feature                        | ENTERPRISE | AWS GovCloud | Azure Government | Google Sovereign Controls | Traditional VPS/Colo |
|--------------------------------|------------|-----------|------------|----------------------------|----------------------|
| Mandatory Access Control enforcing from boot | Yes       | No        | No         | No                         | Rarely              |
| EAL4+ / FIPS 140-3 certified  | Yes       | Partial   | Partial    | No                         | No                  |
| Keys never leave EU/UAE       | Yes       | No        | No         | No                         | Depends             |
| AI supply-chain scanning on-prem | Yes    | No        | No         | No                         | No                  |
| Launch timeline               | 18–24 mo  | Available | Available  | 2026+                      | Immediate but insecure |

### The Ask  
€50 million Series A at €200 million pre-money valuation  
Led by European deep-tech & fintech VCs, German/UAE strategic investors, and regulated institutions who need this yesterday.

We are not asking you to wait for perfect security.  
We are delivering government-grade security you can buy in 2027.
