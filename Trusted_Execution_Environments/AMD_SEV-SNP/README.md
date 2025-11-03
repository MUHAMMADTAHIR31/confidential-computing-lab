# AMD SEV-SNP (Secure Encrypted Virtualization - Secure Nested Paging)

## Overview

AMD SEV-SNP is an extension of AMD's SEV technology that adds strong memory integrity protection to help prevent malicious hypervisor-based attacks such as data replay, memory re-mapping, and other attacks.

## Key Features

- **Memory Encryption**: Encrypts VM memory with per-VM keys
- **Memory Integrity**: Prevents unauthorized modifications to VM memory
- **Secure Nested Paging**: Protects guest page tables
- **VM Isolation**: Strong isolation between VMs and from the hypervisor

## Evolution of AMD SEV

1. **SEV**: Basic VM memory encryption
2. **SEV-ES**: Encrypted State - protects CPU register state
3. **SEV-SNP**: Secure Nested Paging - adds memory integrity protection

## Use Cases

- Confidential virtual machines in cloud environments
- Multi-tenant secure computing
- Regulatory compliance (HIPAA, GDPR)
- Protecting sensitive workloads from cloud providers

## Research Topics

- Performance benchmarking
- Migration strategies
- Integration with Kubernetes/containers
- Attestation mechanisms

## Notes

_Document your experiments and findings here_

## Resources

- [AMD SEV Documentation](https://www.amd.com/en/developer/sev.html)
- [SEV-SNP Whitepaper](https://www.amd.com/system/files/TechDocs/SEV-SNP-strengthening-vm-isolation-with-integrity-protection-and-more.pdf)
- [Linux SEV Guest Support](https://www.kernel.org/doc/html/latest/virt/coco/sev-guest.html)
