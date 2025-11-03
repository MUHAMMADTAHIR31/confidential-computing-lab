# Intel TDX (Trust Domain Extensions)

## Overview

Intel Trust Domain Extensions (TDX) introduces new architectural elements to deploy hardware-isolated virtual machines (VMs) called Trust Domains (TDs). TDX is designed to isolate VMs from the virtual machine manager (VMM), hypervisor, and other non-TD software on the platform.

## Key Features

- **Hardware-based VM Isolation**: Protects VMs from compromised hypervisors
- **Memory Encryption**: Per-TD memory encryption
- **Remote Attestation**: Verify TD authenticity and configuration
- **Minimal Code Changes**: Easier migration of existing workloads compared to enclave-based solutions

## Architecture

- **Trust Domain (TD)**: An isolated VM protected by Intel TDX
- **TD Partitioning**: Hardware-enforced isolation boundaries
- **Secure Arbitration Mode (SEAM)**: CPU mode for TDX operations
- **TD Key Management**: Hardware-based key derivation

## Use Cases

- Confidential cloud computing
- Secure multi-party computation at scale
- Protected AI/ML workloads
- Compliance-sensitive applications

## Comparison with SGX

- **Granularity**: TDX protects entire VMs vs SGX's application-level enclaves
- **Compatibility**: TDX requires minimal application changes
- **Memory Size**: TDX supports larger memory footprints
- **Use Case**: TDX better for lift-and-shift scenarios

## Research Topics

- Performance overhead analysis
- Migration from traditional VMs
- Integration with cloud orchestration
- Attestation flows

## Notes

_Document your experiments and findings here_

## Resources

- [Intel TDX Overview](https://www.intel.com/content/www/us/en/developer/articles/technical/intel-trust-domain-extensions.html)
- [TDX Whitepaper](https://www.intel.com/content/dam/develop/external/us/en/documents/tdx-whitepaper-final9-17.pdf)
- [Linux TDX Guest Documentation](https://www.kernel.org/doc/html/latest/x86/tdx.html)
