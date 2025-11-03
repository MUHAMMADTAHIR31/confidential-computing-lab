# AWS Confidential Computing

## Overview

Amazon Web Services (AWS) provides confidential computing capabilities primarily through AWS Nitro Enclaves and support for Intel SGX on EC2 instances.

## Services & Features

### AWS Nitro Enclaves
- Isolated compute environments within EC2 instances
- No persistent storage, interactive access, or external networking
- Cryptographic attestation support
- Integration with AWS KMS
- Available on multiple EC2 instance families

### EC2 Instances with TEE Support
- Support for Intel SGX on specific instance types
- Bare metal instances for maximum control
- Various instance families (M5, M6, C5, R5, etc.)

## Key Capabilities

### Attestation
- Nitro Attestation for enclaves
- Integration with AWS Certificate Manager
- AWS KMS conditional access based on attestation

### Integration
- **AWS KMS**: Conditional key usage based on enclave attestation
- **AWS Secrets Manager**: Secure secrets delivery to enclaves
- **Amazon CloudWatch**: Monitoring and logging
- **AWS IAM**: Fine-grained access control

### Supported Regions
- Nitro Enclaves available in most major AWS regions
- Check current availability for specific instance types

## Use Cases

- Secure processing of payment card data
- Key management and HSM alternatives
- Multi-party computation
- Machine learning on encrypted data
- Blockchain and cryptocurrency applications

## Pricing

- Nitro Enclaves: No additional charge beyond EC2 instance cost
- Instance pricing varies by type and region
- Memory and vCPUs allocated to enclave reduce parent instance resources

## Development Tools

- AWS Nitro Enclaves CLI
- Nitro Enclaves SDK (C, Rust)
- Docker integration for enclave applications
- AWS CloudFormation support

## Advantages

- Deep integration with AWS ecosystem
- Strong isolation guarantees from Nitro System
- No additional cost for enclave functionality
- Comprehensive documentation and examples

## Limitations

- Enclaves have no network access (must proxy through parent)
- Limited to specific EC2 instance types
- Regional availability may vary

## Research Topics

- Performance benchmarking vs. other AWS instances
- Cost optimization strategies
- CI/CD integration for enclave applications
- Attestation flow implementation
- Integration patterns with AWS services

## Notes

_Document your AWS-specific experiments here_

## Resources

- [AWS Nitro Enclaves User Guide](https://docs.aws.amazon.com/enclaves/latest/user/nitro-enclave.html)
- [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)
- [AWS Nitro System](https://aws.amazon.com/ec2/nitro/)
- [AWS KMS with Nitro Enclaves](https://docs.aws.amazon.com/kms/latest/developerguide/services-nitro-enclaves.html)
