# Intel SGX (Software Guard Extensions)

## Overview

Intel Software Guard Extensions (SGX) is a set of instruction codes built into Intel CPUs that allows applications to create hardware-encrypted enclaves—private regions of memory that are protected from processes running at higher privilege levels.

## Key Features

- **Hardware-based Memory Encryption**: Protects enclave code and data from unauthorized access
- **Attestation**: Remote and local attestation to verify enclave authenticity
- **Sealing**: Encrypt data that only the enclave can decrypt
- **Small TCB**: Minimal Trusted Computing Base reduces attack surface

## Use Cases

- Secure key management
- Digital rights management (DRM)
- Secure multi-party computation
- Blockchain and cryptocurrency wallets
- Privacy-preserving machine learning

## Research Topics

- Enclave development and SDK usage
- Performance overhead analysis
- Side-channel attack mitigation
- Integration with cloud services

## Notes

_Document your experiments and findings here_

## Resources

- [Intel SGX Developer Guide](https://www.intel.com/content/www/us/en/developer/tools/software-guard-extensions/overview.html)
- [Intel SGX SDK](https://github.com/intel/linux-sgx)
- [SGX Hardware List](https://github.com/ayeks/SGX-hardware)
