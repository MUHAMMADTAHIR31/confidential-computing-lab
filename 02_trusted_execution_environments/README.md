# 🧩 Week 2 — Trusted Execution Environments (TEEs)

After exploring the idea of **Confidential Computing** in Week 1, this week I focused on the hardware foundation that makes it all possible — the **Trusted Execution Environment (TEE)**.

---

## 🧠 What Is a TEE?

A **Trusted Execution Environment (TEE)** is a secure area inside a processor where code and data can run privately and safely.  
Even the operating system, hypervisor, or cloud provider cannot access what happens inside.

A TEE provides three essential guarantees:

| Property | Description |
|-----------|-------------|
| 🔒 **Isolation** | Sensitive operations are separated from the main system. |
| 🧠 **Integrity** | Only verified, untampered code can execute. |
| 🪄 **Confidentiality** | Data remains encrypted in memory and protected from unauthorized access. |

---

## ⚙️ How It Works

When an application needs to process sensitive data, it makes a **secure call** to the TEE (known as an *ECALL*).  
The TEE executes the operation inside a protected memory region and returns the result (*OCALL*) — without exposing the data to the normal system.

---

## 🧩 Major TEE Implementations

| Technology           | Provider / Platform                  | Isolation Level | Key Features                                                                 |
|----------------------|--------------------------------------|-----------------|------------------------------------------------------------------------------|
| Intel SGX            | Intel CPUs / Azure DCsv2/DCsv3       | Process-level   | Enclaves for sensitive apps, fine-grained control, DCAP attestation          |
| AMD SEV-SNP          | AMD EPYC / Azure, GCP                | VM-level        | Encrypts VM memory, Secure Nested Paging, guest-owner attestation            |
| ARM TrustZone        | ARM / Mobile, Edge                   | System-level    | Secure vs Normal World separation — used in phones and IoT                   |

---

## 🔐 How Memory Protection Works

- **Intel SGX** → Uses a Memory Encryption Engine (MEE) to encrypt enclave memory.
- **AMD SEV-SNP** → Encrypts full VM memory with per-VM keys and adds integrity checks.
- **Intel TDX** → Extends isolation to entire VMs; adds page-table and DMA protection.
- **Nitro Enclaves** → Isolates CPU and memory resources via Nitro Hypervisor (partitioning rather than encryption).

---

## 🧾 Why TEEs Matter

TEEs are the hardware backbone of Confidential Computing.  
They enable secure processing even on untrusted infrastructure, allowing:

- Privacy-preserving AI and analytics
- Secure financial or healthcare data processing
- Multi-party computation and data collaboration
- Compliance with privacy and sovereignty regulations

Without TEEs, protecting data while in use would simply not be possible.

---

## 🔜 Next Step

In Week 3, I'll explore Remote Attestation — how systems outside the TEE can verify that the code running inside it is authentic and untampered.

👉 **Next:** Week 3 – Remote Attestation

---

## 🧩 References

- Intel® SGX and TDX Developer Guides
- AMD SEV-SNP Technical Overview (2025)
- AWS Nitro Enclaves Documentation
- Confidential Computing Consortium White Papers