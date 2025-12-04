# ACCELERATOR EDITION  
Secure Platform-as-a-Service (PaaS)  
Investor Deck – €15 Million Pre-Seed / Seed  
December 2025  

### Title Slide  
ACCELERATOR  
The Fastest, Most Secure Open-Source PaaS on Earth  
Hardened by Default | Ships in 2026 | Revenue from Day 180  

“99 % of developers and startups want real security tomorrow – not in 2030 and not for €200 million.”

### The Problem – Again  
Every week another zero-day, another supply-chain disaster, another regulator breathing down necks.  
Startups, scale-ups, and mid-sized SaaS companies cannot use raw AWS/Hetzner/DigitalOcean anymore – but they also cannot wait for sovereign EAL7 clouds that don’t exist yet.

### The ACCELERATOR Solution  
We took the exact same architecture we already designed for the Fortress and Enterprise editions and stripped it to the absolute minimum viable secure platform that still beats everything currently for sale.

| Pillar                          | Accelerator Choice (all production-ready today)               | Security Level |
|---------------------------------|---------------------------------------------------------------|----------------|
| Base OS                         | Debian 13 minimal + custom hardened kernel                    | Lockdown=confidentiality |
| Mandatory Access Control        | SELinux enforcing + custom policy (targeted + extra types)   | DoD-grade MAC |
| Filesystem                      | ZFS root (optional) + snapshots + encryption                 | Military-grade |
| Container runtime               | Rootless Podman + Bubblewrap sandboxing                      | Rootless + seccomp |
| VM / system containers          | LXD 6 (Incus) + KVM + sVirt                                   | Full isolation |
| Supply-chain security           | Built-in GitHub Actions runners with Trivy, Grype, Syft + lightweight AI agent (open-source model) | Real-time SBOM + vuln scanning |
| Web UI                          | Clean Cockpit + custom dashboard (dark corporate theme)      | Single pane |
| Reverse proxy                   | Traefik v3 + auto-LetsEncrypt                                 | Zero-touch TLS |
| Infrastructure                  | 1 owned rack in Germany + optional Dubai expansion later     | Sovereign-capable |

Result: A platform that is 10× more secure than Fly.io / Render / Railway and launches in 9–12 months instead of 5 years.

### Target Customers & Pricing (Months 6–36)

| Segment                         | Example Clients                                      | Monthly Price | ACV         |
|---------------------------------|------------------------------------------------------|---------------|-------------|
| Fast-growing EU startups        | Qonto, Spendesk, Gorillas-style, 50–500 employees    | €2k–€25k     | €60k–€300k |
| Mid-size SaaS & B2B             | Typeform, Pitch, Front, 200–2000 employees          | €15k–€80k    | €180k–€960k |
| Regulated but agile             | Neobanks, health-tech, gov-tech wanting quick win    | €30k–€120k   | €360k–€1.4 M |
| DevSecOps teams & agencies      | Consulting firms white-labeling secure hosting       | €8k–€40k     | €96k–€480k |

Conservative Year-3 ARR with €15 M raise: €42 M (450 customers averaging €93 k ARR)

### Use of Proceeds – €15 Million  

| Category                                      | Amount (€M) | %    | Details |
|-----------------------------------------------|-------------|------|-----------------------------------------------------|
| Core team (34 → 55 heads by Year 2)           | 8.4        | 56%  | Berlin-based, heavy on C/Python/DevOps, small Dubai outpost |
| SELinux policy finalisation + red-team audit  | 0.9        | 6%   | TÜViT light audit + bug bounty |
| 1 owned rack Germany + basic Dubai presence   | 3.0        | 20%  | Maincubes/Equinix FR8 + Khazna/Equinix DX |
| AI scanning cluster + tooling                 | 0.9        | 6%   | Small on-prem GPU nodes + open models |
| Go-to-market & first 50 paying customers      | 1.2        | 8%   | Conferences, content, founder-led sales |
| Working capital + 20 % contingency            | 0.6        | 4%   | Buffer |
| **Total**                                     | **15.0**   | 100% | 24+ month runway |

### Milestones – 18 Months to Profitability  

| Month       | Milestone |
|-------------|------------|
| Month 1–3   | Company live, first 20 hires, ISO shipped to 5 design partners |
| Month 6     | Public beta – 30 paying customers |
| Month 9     | €1 M ARR run-rate |
| Month 12    | €6 M ARR, Germany rack at 85 % capacity |
| Month 15    | Dubai expansion live |
| Month 18    | Cash-flow positive |

### Why We Win the “Good Enough, Right Now” Market  

| Feature                        | ACCELERATOR | Fly.io / Render / Railway | Hetzner / OVH | Regular VPS |
|--------------------------------|-------------|---------------------------|---------------|-------------|
| SELinux enforcing from boot   | Yes        | No                        | No            | No          |
| Rootless containers by default| Yes        | No                        | No            | No          |
| Built-in supply-chain scanning| Yes        | Add-on only               | No            | No          |
| Sovereign-ready (DE/UAE)      | Yes        | No                        | Partial       | Partial     |
| Time to first paying customer | 6 months   | Today                     | Today         | Today       |
| Gross margin after infra      | 78 %       | 55–65 %                   | 40–50 %       | 30–40 %     |

### The Ask  
€15 million Pre-Seed / Seed at €60 million pre-money valuation  
Led by European seed/deep-tech funds, ex-Cloudflare/HashiCorp angels, and strategic SaaS founders who want this yesterday.

We are not promising perfect security in 2030.  
We are shipping the most secure platform you can run production on in 2026 – and making money while the big clouds are still talking about it.
