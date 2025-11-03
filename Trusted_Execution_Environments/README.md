# Trusted Execution Environments (TEEs)

This directory contains research and experiments on various Trusted Execution Environment technologies.

## What are TEEs?

Trusted Execution Environments (TEEs) are secure areas within a main processor that provide a higher level of security for executing code and protecting data. TEEs ensure that code and data loaded inside are protected with respect to confidentiality and integrity.

## Technologies Covered

### [Intel SGX](./Intel_SGX/)
Intel Software Guard Extensions (SGX) is a set of security-related instruction codes that are built into modern Intel CPUs. It allows user-level code to allocate private regions of memory, called enclaves, which are designed to be protected from processes running at higher privilege levels.

### [AMD SEV-SNP](./AMD_SEV-SNP/)
AMD Secure Encrypted Virtualization - Secure Nested Paging (SEV-SNP) adds strong memory integrity protection to help prevent malicious hypervisor-based attacks like data replay, memory re-mapping, and more.

### [Intel TDX](./Intel_TDX/)
Intel Trust Domain Extensions (TDX) introduces architectural elements to help deploy hardware-isolated virtual machines (VMs) called Trust Domains (TDs), providing confidential computing capabilities at the VM level.

### [AWS Nitro](./AWS_Nitro/)
AWS Nitro Enclaves enables customers to create isolated compute environments to further protect and securely process highly sensitive data within their Amazon EC2 instances.

## Key Concepts

- **Enclave/Secure Area**: Isolated memory region protected from unauthorized access
- **Attestation**: Process of proving that code is running in a genuine TEE
- **Sealing**: Encrypting data that can only be decrypted within the same enclave
- **Memory Encryption**: Hardware-based encryption of memory contents

## Resources

- [Confidential Computing Consortium](https://confidentialcomputing.io/)
- [Intel SGX Documentation](https://www.intel.com/content/www/us/en/developer/tools/software-guard-extensions/overview.html)
- [AMD SEV Documentation](https://www.amd.com/en/developer/sev.html)
