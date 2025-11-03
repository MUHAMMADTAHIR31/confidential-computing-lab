# 🔐 Confidential Computing Lab

Welcome to my research repository on **Confidential Computing** — a field focused on protecting data *while it’s being processed*.  
This project documents my ongoing learning, experiments, and analysis of technologies that enable trusted and verifiable computation across hardware and cloud environments.

---

## 🧠 Overview

Traditional security protects data:
- **At rest** → using encryption on disks or storage systems  
- **In transit** → using protocols like TLS/HTTPS  

But **when data is being used**, it’s typically decrypted in memory — exposed to the OS, hypervisor, or administrators.  
**Confidential Computing** closes this gap by using **Trusted Execution Environments (TEEs)** — secure hardware regions that isolate and encrypt data even during processing.

---

## 📘 Contents

| Folder | Description |
|--------|--------------|
| [`01_confidential_computing_intro/`](./01_confidential_computing_intro/) | Week 1 – Introduction to Confidential Computing |
| [`02_trusted_execution_environments/`](./02_trusted_execution_environments/) | Overview of TEEs: Intel SGX, AMD SEV-SNP, Intel TDX, AWS Nitro |
| [`03_remote_attestation/`](./03_remote_attestation/) | Understanding attestation flows (SGX DCAP, SEV-SNP, TDX) |
| [`04_fabric_private_chaincode/`](./04_fabric_private_chaincode/) | Experiments with Hyperledger Fabric Private Chaincode (FPC) |
| [`05_confidential_containers/`](./05_confidential_containers/) | Exploration of Confidential Containers (CoCo) and SGX-SIM |
| [`06_cloud_providers_comparison/`](./06_cloud_providers_comparison/) | Comparison of Confidential VM offerings across AWS, Azure, and GCP |

---

## 🚀 Research Focus

This repository supports my master’s research exploring:
- Trusted Execution Environments (TEEs)
- Remote Attestation mechanisms
- Secure workload isolation
- Blockchain privacy (FPC)
- Confidential Containers
- Cross-cloud comparisons of Confidential Computing services  

The goal is to bridge conceptual understanding with practical implementation and experimentation.

---

## 🌍 Acknowledgment

This work is inspired by the efforts of the [Confidential Computing Consortium (CCC)](https://confidentialcomputing.io/), which brings together researchers, hardware vendors, and cloud providers to make privacy-preserving computing accessible and standardized.

---

## 📫 Connect

If you’re exploring or researching similar areas, feel free to connect and exchange insights!  

**LinkedIn:** [Muhammad Tahir Korejo](https://www.linkedin.com/in/muhammad-tahir-83a431204/)  
**Tags:** `#ConfidentialComputing` `#IntelTDX` `#AMDSEVSNP` `#IntelSGX` `#PrivacyTech` `#Hyperledger` `#ResearchJourney`
