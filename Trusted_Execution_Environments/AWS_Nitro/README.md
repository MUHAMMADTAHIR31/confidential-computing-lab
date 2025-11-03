# AWS Nitro Enclaves

## Overview

AWS Nitro Enclaves enables customers to create isolated compute environments to further protect and securely process highly sensitive data such as personally identifiable information (PII), healthcare, financial, and intellectual property data within their Amazon EC2 instances.

## Key Features

- **Isolation**: No persistent storage, interactive access, or external networking
- **Cryptographic Attestation**: Verify enclave identity and integrity
- **Flexible**: Run on various EC2 instance types
- **Integration**: Works with AWS KMS for key management
- **Open Source**: Nitro Enclaves SDK is open source

## Architecture

- **Parent Instance**: EC2 instance that hosts the enclave
- **Enclave**: Isolated compute environment with dedicated CPU and memory
- **Secure Local Channel**: Communication via vsock between parent and enclave
- **Nitro Hypervisor**: Enforces isolation boundaries

## Use Cases

- Processing payment card data
- Secure key management and cryptographic operations
- Multi-party computation
- DRM and content protection
- Secrets management

## Attestation Process

1. Enclave generates attestation document
2. Document includes enclave measurements (PCRs)
3. Signed by AWS Nitro root of trust
4. Can be verified by AWS KMS or external services

## Research Topics

- Performance characteristics
- Integration patterns with AWS services
- Development and debugging workflows
- Cost optimization strategies

## Notes

_Document your experiments and findings here_

## Resources

- [AWS Nitro Enclaves Documentation](https://docs.aws.amazon.com/enclaves/latest/user/nitro-enclave.html)
- [Nitro Enclaves SDK](https://github.com/aws/aws-nitro-enclaves-sdk-c)
- [Nitro Enclaves CLI](https://github.com/aws/aws-nitro-enclaves-cli)
