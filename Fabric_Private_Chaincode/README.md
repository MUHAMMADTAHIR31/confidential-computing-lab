# Fabric Private Chaincode (FPC)

## Overview

Fabric Private Chaincode (FPC) extends Hyperledger Fabric with support for confidential smart contracts (chaincode) that execute within Intel SGX enclaves. This enables private transactions and data privacy while maintaining the benefits of blockchain technology.

## What is FPC?

FPC allows chaincode execution in a Trusted Execution Environment (TEE), ensuring that:
- Transaction data is encrypted and only accessible within the enclave
- Smart contract logic is protected from unauthorized viewing
- Even peers hosting the chaincode cannot see the data being processed
- Confidentiality is maintained while preserving blockchain verification

## Key Features

### Data Confidentiality
- State data encrypted and only accessible within enclaves
- Transaction payloads protected from unauthorized access
- Private data remains private even from endorsing peers

### Code Privacy
- Chaincode logic can be kept confidential
- Protection of proprietary business logic
- Prevents reverse engineering of smart contracts

### Attestation & Trust
- Remote attestation proves chaincode is running in genuine SGX enclave
- Clients verify enclave identity before submitting transactions
- Hardware-based trust establishment

### Compatibility
- Extends Hyperledger Fabric
- Leverages existing Fabric features (ordering, consensus, etc.)
- Compatible with Fabric SDK

## Architecture

```
┌─────────────────────────────────────┐
│     Client Application              │
└──────────────┬──────────────────────┘
               │ (Attestation + Encrypted TX)
┌──────────────▼──────────────────────┐
│     Fabric Peer                     │
│  ┌────────────────────────────┐    │
│  │   SGX Enclave              │    │
│  │  ┌──────────────────────┐  │    │
│  │  │  FPC Chaincode       │  │    │
│  │  │  - Decrypt TX        │  │    │
│  │  │  - Execute Logic     │  │    │
│  │  │  - Encrypt State     │  │    │
│  │  └──────────────────────┘  │    │
│  └────────────────────────────┘    │
│         Encrypted State DB          │
└─────────────────────────────────────┘
```

## Use Cases

### Financial Services
- Private securities trading
- Confidential settlement systems
- Hidden order books
- Privacy-preserving DeFi

### Supply Chain
- Confidential pricing information
- Private supplier relationships
- Protected trade secrets
- Regulatory compliance with data privacy

### Healthcare
- Private medical records on blockchain
- HIPAA-compliant health information exchange
- Confidential clinical trial data

### Government & Identity
- Private identity verification
- Confidential voting systems
- Protected citizen data

## Development Workflow

1. **Write Chaincode**: Develop chaincode using FPC SDK (C++)
2. **Build Enclave**: Compile chaincode for SGX enclave
3. **Attest**: Generate attestation evidence
4. **Deploy**: Install and instantiate FPC chaincode on Fabric network
5. **Interact**: Clients verify attestation and submit encrypted transactions

## Components

- **FPC Chaincode**: Runs inside SGX enclave
- **Enclave Registry**: Tracks registered enclaves and attestations
- **FPC Client SDK**: For building client applications
- **ECC (Enclave Chaincode)**: Wrapper for secure execution
- **ERCC (Enclave Registry Chaincode)**: Manages enclave lifecycle

## Challenges & Limitations

- **Memory Constraints**: SGX EPC memory limitations
- **Performance Overhead**: Encryption/decryption and attestation costs
- **Platform Dependencies**: Requires SGX-enabled hardware
- **Development Complexity**: More complex than standard chaincode
- **Limited Language Support**: Primarily C++ (vs. Go/JavaScript for standard Fabric)

## Research Topics

- Performance benchmarking vs. standard Fabric chaincode
- Memory optimization techniques
- Attestation strategies and caching
- Integration with Fabric operations (backup, recovery, etc.)
- Migration from standard to confidential chaincode
- Multi-organization private chaincode scenarios

## Getting Started

### Prerequisites
- Hyperledger Fabric 2.x
- Intel SGX-enabled hardware (or simulation mode)
- FPC development tools
- Docker for deployment

### Installation
```bash
# Clone FPC repository
git clone https://github.com/hyperledger/fabric-private-chaincode.git

# Follow setup instructions in repository
```

## Notes

_Document your FPC experiments and findings here_

## Resources

- [FPC GitHub Repository](https://github.com/hyperledger/fabric-private-chaincode)
- [FPC Documentation](https://hyperledger.github.io/fabric-private-chaincode/)
- [Hyperledger Fabric](https://www.hyperledger.org/use/fabric)
- [FPC Paper](https://arxiv.org/abs/1909.04556)
- [Confidential Computing Consortium](https://confidentialcomputing.io/)

## Community

- Hyperledger Discord: #fabric-private-chaincode
- Mailing Lists: fabric-private-chaincode@lists.hyperledger.org
- Monthly community calls
