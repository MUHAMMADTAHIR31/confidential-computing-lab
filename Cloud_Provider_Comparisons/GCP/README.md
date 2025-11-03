# Google Cloud Platform Confidential Computing

## Overview

Google Cloud Platform (GCP) provides confidential computing through Confidential VMs and Confidential GKE Nodes, primarily leveraging AMD SEV for memory encryption.

## Services & Features

### Confidential VMs
- AMD SEV-based memory encryption
- N2D series (AMD EPYC 2nd Gen)
- C2D series (AMD EPYC 3rd Gen)
- SEV-SNP support in preview

### Confidential GKE Nodes
- Kubernetes nodes with confidential computing
- Integration with Google Kubernetes Engine
- Pod-level isolation with confidential VMs

### Confidential Dataflow
- Secure data processing in Apache Beam pipelines
- Confidential VMs for worker nodes

### Confidential Space
- Secure data clean room environment
- Multi-party computation support
- TEE-based collaboration platform

## Key Capabilities

### Attestation
- GCP Attestation service integration
- AMD SEV attestation support
- Verification of VM measurements

### Integration
- **Cloud KMS**: Key management and encryption
- **Secret Manager**: Secure secret storage and access
- **Cloud HSM**: Hardware security module integration
- **BigQuery**: Confidential data analytics
- **Vertex AI**: Confidential machine learning

### Supported Regions
- Available in multiple global regions
- Check region-specific availability for confidential VM types

## Use Cases

- Secure data analytics and BigQuery workloads
- Multi-party computation and data sharing
- Confidential machine learning training and inference
- Regulated workload processing (healthcare, finance)
- Kubernetes-based confidential applications

## Pricing

- ~3-5% premium over standard N2D/C2D instances
- Per-second billing
- Committed use discounts available
- Sustained use discounts apply

## Development Tools

- Standard GCP SDKs and APIs
- gcloud CLI support
- Terraform providers
- Cloud Build for CI/CD

## Advantages

- Easy migration from standard VMs (minimal changes)
- Transparent encryption of memory
- Integration with GKE for containerized workloads
- Competitive pricing (smaller premium)
- Strong focus on analytics and ML use cases

## Limitations

- Currently limited to AMD SEV technology
- No application-level enclave support (like SGX)
- Fewer TEE technology options compared to competitors
- Attestation capabilities less mature than AWS/Azure

## Notable Features

### Confidential Space
- Unique offering for secure multi-party computation
- Trusted execution environment for data collaboration
- Built-in data provenance and auditing

### Performance
- Minimal performance overhead (typically <1-3%)
- Transparent to applications
- No code changes required

## Research Topics

- Performance benchmarking of Confidential VMs
- Confidential GKE deployment patterns
- Integration with data analytics pipelines
- Confidential Space use cases
- Cost comparison with standard instances

## Notes

_Document your GCP-specific experiments here_

## Resources

- [GCP Confidential Computing](https://cloud.google.com/confidential-computing)
- [Confidential VMs Documentation](https://cloud.google.com/compute/confidential-vm/docs)
- [Confidential GKE](https://cloud.google.com/kubernetes-engine/docs/how-to/confidential-gke-nodes)
- [Confidential Space](https://cloud.google.com/confidential-computing/confidential-space/docs)
- [AMD SEV on GCP](https://cloud.google.com/blog/products/identity-security/introducing-google-cloud-confidential-computing-with-confidential-vms)
