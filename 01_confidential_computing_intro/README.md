# 🔐 Week 1 — Introduction to Confidential Computing

A few months ago, I came across a term that immediately caught my attention — **Confidential Computing**.  
At first, I thought, *“Alright, another security buzzword.”*  
But the more I explored, the more it changed how I think about data protection — and about computing itself.

---

## 🧠 What Is Confidential Computing?

We often talk about two layers of data security:
- 🔒 **Encryption at rest** – protecting data when it’s stored.  
- 🌐 **Encryption in transit** – securing data while it’s being transmitted.  

But what about when data is *in use*?

When an application processes information in memory, that data becomes temporarily visible — and that’s exactly when attackers or even privileged systems could peek inside.  

**Confidential Computing** fills that gap.  
It protects data **while it’s being processed**, using hardware-based regions inside the CPU called **Trusted Execution Environments (TEEs)**.  

Inside these TEEs, code and data run privately — isolated from the operating system, hypervisor, and even the cloud provider itself.

---

## ⚙️ Real-World Implementations (2025)

| Cloud Provider | Technology | Description |
|----------------|-------------|-------------|
| **Microsoft Azure** | AMD SEV-SNP, Intel TDX | Confidential VMs protecting workloads through memory isolation |
| **AWS** | Nitro Enclaves | Provides isolated compute environments for secure data processing |
| **Google Cloud** | AMD SEV-SNP *(Intel TDX in preview)* | Confidential VMs supporting hardware-level data encryption |

---

## 🌍 Why It Matters

This isn’t just another layer of cloud security — it’s a step toward **trustable computation**.  
It allows sensitive workloads to run safely even on infrastructure that isn’t fully trusted.  
Confidential Computing is becoming a foundational technology for:
- Privacy-preserving AI  
- Secure data sharing and collaboration  
- Confidential cloud workloads  
- Multi-party computation  

---

## 🧩 Key Concept: Trusted Execution Environment (TEE)

A **TEE** is a secure area within a processor that provides:
1. **Isolation** — code and data are protected from the rest of the system.  
2. **Integrity** — ensures that software inside the TEE hasn’t been tampered with.  
3. **Confidentiality** — keeps data encrypted and inaccessible from outside.  

Examples:
- **Intel SGX**
- **AMD SEV-SNP**
- **Intel TDX**
- **AWS Nitro Enclaves**

---

## 🙌 Closing Note

For me, this technology feels like the *missing piece* — the ability to **trust computation itself**, not just storage or communication.  

This week’s focus is understanding the *core motivation* behind Confidential Computing and setting the stage for deeper dives into TEEs, attestation, and real-world implementations in the upcoming weeks.

---

**Next:** [Week 2 – Trusted Execution Environments (TEEs)](../02_trusted_execution_environments/README.md)
