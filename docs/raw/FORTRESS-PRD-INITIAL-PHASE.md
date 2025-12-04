# Product Requirements Document (PRD)  
FORTRESS EDITION – The Provably Secure Platform-as-a-Service  
Version 1.0 | December 2025 | Classification: Public (non-export controlled)

### 1. Product Name & Positioning
**Internal Codename:** FORTRESS  
**Public Name (TBA):** [Redacted – Sovereign Cloud / National Security Cloud]  
**Tagline:** “The only civilian cloud with mathematical proof of kernel correctness – EAL7+ Common Criteria”

This is the €200 M, 36-month programme to deliver the world’s first formally verified microkernel-based PaaS that achieves full Common Criteria EAL7+ (or national equivalent under BSI/ANSSI mutual recognition).

### 2. Non-Negotiable Security Guarantees (the “Fortress Promises”)
Every single one must be mathematically proven or formally certified:

| # | Guarantee | Assurance Method |
|---|-----------|------------------|
| 1 | Information cannot flow between customer tenants under any circumstance (including kernel exploits) | Full functional correctness proof of microkernel isolation |
| 2 | No executable code can run on the host that has not been cryptographically signed and attested at boot | Verified measured boot + remote attestation (TCG D-RTM) |
| 3 | Every container, VM, and CI/CD runner is confined by a mathematically verified capability boundary | seL4-style capability proofs extended to user-space |
| 4 | Absence of all CWEs in the kernel (buffer overflows, use-after-free, TOCTOU, etc.) | Comprehensive formal verification (Isabelle/HOL or Coq) |
| 5 | Supply-chain attacks are detected and blocked before deployment | AI + formal model checking of SBOM + binary provenance |

### 3. Core Technology Stack (Fortress Edition only)

| Layer | Technology | Justification |
|-------|------------|---------------|
| Microkernel | Custom seL4 derivative or clean-room Genode-based microkernel written in Rust + verified C | Only two kernels worldwide have full functional correctness proofs; we will extend one |
| Formal Verification Framework | Isabelle/HOL + CakeML + custom refinements | Industry gold standard used by seL4, CertiK, and TrustInSoft |
| Cryptographic Modules | FIPS 140-3 Level 3 HSM-integrated (Thales/Utimaco) + post-quantum ready | Required for EAL7+ |
| Virtualization / Containers | Direct execution on verified kernel (no Linux emulation); lightweight unikernels + MirageOS-style libraries | Eliminates entire Linux attack surface |
| Orchestration | Nomad + custom verified scheduler (written in Rust, partially verified) | Minimal trusted computing base |
| Storage | Verified ZFS port or custom verified filesystem with proofs of crash consistency | Data integrity proofs |
| Networking | Custom verified mTCP stack + WireGuard in kernel | No OpenSSL, no kernel networking bugs |
| CI/CD Runners | In-house runners executing inside formally isolated compartments | No GitHub Actions shared runners |
| AI Security Agents | On-prem GPU cluster running proprietary formal-model-assisted scanners | Detects logic flaws no SAST tool can see |

### 4. Certification Scope & Targets

| Certification | Target Level | Sponsoring Lab | Timeline |
|---------------|--------------|----------------|----------|
| Common Criteria | EAL7+ (or national equivalent) | BSI (Germany) + ANSSI (France) mutual recognition | Q2 2028 certificate |
| BSI VSITR (Germany) | Tier 4 (highest) | BSI | Q1 2028 |
| UAE NESA / Dubai ISR | Enhanced Grade | TRA / Dubai Electronic Security Center | Q4 2028 |
| FIPS 140-3 | Level 3 (physical) | NIST CMVP | Q4 2027 |

### 5. Infrastructure (Owned & Air-Gapped Capable)

| Location | Facility Type | Capacity | Ownership |
|----------|---------------|----------|-----------|
| Frankfurt, Germany | Custom-built Tier-4 equivalent cage | 8 MW initial, expandable to 25 MW | 100 % owned SPV |
| Dubai, UAE (Jebel Ali / DIC) | Custom-built Tier-4 equivalent cage | 6 MW initial | 100 % owned SPV |
| Interconnect | Dedicated dark fibre + quantum-ready encryption | 2 × 100 Gbps protected | Private lambda |

### 6. MVP Scope – Fortress 1.0 (Q2 2028)

| Epic | Deliverable | Proof Required |
|------|-------------|----------------|
| E1 – Verified Microkernel | Full functional correctness + refinement proofs | Isabelle theorems published |
| E2 – Verified Boot & Attestation | Remote attestation protocol proofs | BSI/ANSSI accepted |
| E3 – Verified Unikernel Runtime | Customer workloads run as verified unikernels | No Linux, no syscalls |
| E4 – Sovereign Cages Online | Frankfurt cage fully operational | Physical security certification |
| E5 – First Pilot Customer | One central bank or NATO entity live | Signed reference |

### 7. Non-Goals (Fortress 1.0)
- General-purpose Linux container support (we will not run Docker)  
- Serverless / Lambda-style functions in v1  
- Multi-cloud or hybrid cloud  
- Price competitiveness with AWS (we are 50–100× more expensive by design)

### 8. Success Metrics (36 Months)
- EAL7+ certificate in hand  
- ≥ 3 live customers (central bank / defense / CNI)  
- > €300 M ARR  
- No exploitable vulnerabilities ever disclosed (the ultimate KPI)

This is the nuclear-hardened vault of cloud computing.  
Everything else is a compromise.
