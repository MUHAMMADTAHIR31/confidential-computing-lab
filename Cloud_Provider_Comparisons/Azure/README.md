# Azure Confidential Computing

## Overview

Microsoft Azure offers comprehensive confidential computing services through Azure Confidential Computing (ACC), featuring support for Intel SGX, AMD SEV-SNP, and Intel TDX technologies.

## Services & Features

### Azure Confidential VMs
- AMD SEV-SNP based VMs with memory encryption
- Intel TDX support (preview/limited availability)
- Full VM-level confidentiality
- Minimal application changes required

### DCsv2/DCsv3 Series (Intel SGX)
- Application-level enclaves
- EPC (Enclave Page Cache) memory up to 256 GB
- Support for both Linux and Windows

### Azure Confidential Containers
- Confidential container groups in ACI
- Confidential AKS (Azure Kubernetes Service) nodes
- Container-level isolation

### Azure Confidential Ledger
- Immutable ledger backed by TEEs
- Built on Confidential Consortium Framework (CCF)

## Key Capabilities

### Attestation
- Microsoft Azure Attestation (MAA) service
- Support for SGX, SEV-SNP, and TDX attestation
- Custom attestation policies
- Integration with Managed HSM

### Integration
- **Azure Key Vault**: Managed HSM with confidential computing
- **Azure SQL**: Always Encrypted with secure enclaves
- **Azure Machine Learning**: Confidential inference
- **Azure Confidential Ledger**: Tamper-proof storage

### Supported Regions
- Multiple regions across North America, Europe, and Asia
- Availability varies by VM series and TEE technology

## Use Cases

- Confidential databases (Azure SQL with secure enclaves)
- Secure multi-party computation
- Confidential AI/ML inference
- Blockchain and distributed ledgers
- Healthcare and financial data processing

## Pricing

- Premium pricing for confidential VM series
- Varies by VM size, region, and commitment level
- Azure Hybrid Benefit applicable
- Reserved instances available for cost savings

## Development Tools

- Open Enclave SDK (cross-platform for SGX)
- Azure Attestation SDK
- Visual Studio integration
- Confidential Consortium Framework (CCF)

## Advantages

- Widest variety of TEE technologies supported
- Strong Azure service integration
- Mature attestation infrastructure (MAA)
- Good documentation and developer resources
- Support for both application and VM-level confidentiality

## Limitations

- Regional availability varies by technology
- Premium pricing for confidential VMs
- Learning curve for SGX development
- Limited memory for SGX enclaves on older series

## Research Topics

- Performance comparison: SGX vs. SEV-SNP vs. TDX
- Migration from standard VMs to confidential VMs
- Azure Attestation service implementation
- Confidential Kubernetes patterns
- Cost-benefit analysis

## Notes

_Document your Azure-specific experiments here_

## Resources

- [Azure Confidential Computing](https://azure.microsoft.com/en-us/solutions/confidential-compute/)
- [Azure Confidential VMs](https://learn.microsoft.com/en-us/azure/confidential-computing/confidential-vm-overview)
- [Microsoft Azure Attestation](https://learn.microsoft.com/en-us/azure/attestation/overview)
- [Open Enclave SDK](https://github.com/openenclave/openenclave)
- [Confidential Consortium Framework](https://github.com/microsoft/CCF)
