# Google Cloud Key Management Service Comparison

This document provides a detailed comparison of Google Cloud's Key Management Service (KMS) options: **Software-backed KMS**, **Cloud HSM**, and **Cloud External Key Manager (EKM)**. It outlines their features, security levels, use cases, and limitations to help you choose the right key management solution for your needs.

## Overview

Google Cloud offers three key management options within its Key Management Service (KMS) framework:
- **Cloud KMS (Software)**: A fully managed, software-based key management service for scalable encryption needs.
- **Cloud HSM**: A managed service using FIPS 140-2 Level 3 certified Hardware Security Modules for high-security requirements.
- **Cloud EKM**: Allows key management through external providers for maximum control and data sovereignty.

## Comparison Table

| Feature                     | Cloud KMS (Software)                     | Cloud HSM                                | Cloud EKM                                |
|-----------------------------|------------------------------------------|------------------------------------------|------------------------------------------|
| **Security Level**          | FIPS 140-2 Level 1 (Software)           | FIPS 140-2 Level 3 (Hardware)           | Varies (Depends on external provider)    |
| **Key Storage**             | Software-based, Google infrastructure    | FIPS 140-2 Level 3 HSMs                 | External provider’s infrastructure        |
| **Key Control**             | Managed by Google                       | Managed by Google, keys stay in HSM      | Fully controlled by customer/external provider |
| **Message Size Limit**      | 64 KiB                                  | 8 KiB                                   | Varies by provider                       |
| **Latency**                 | Lower                                   | Higher (especially for asymmetric keys) | Depends on external provider              |
| **Compliance**              | General-purpose, less strict             | PCI DSS, HIPAA, GDPR, FedRAMP High      | Depends on provider, supports HYOK        |
| **Use Case**                | General encryption, scalable apps       | High-security, regulated industries      | Data sovereignty, third-party trust       |
| **Integration**             | Seamless with Google Cloud services      | Seamless with CMEK-enabled services      | Requires external provider integration   |
| **Management Overhead**     | Low (Fully managed)                     | Low (Google manages HSMs)               | High (Customer manages external provider) |

## Detailed Breakdown

### 1. Cloud KMS (Software-backed)
- **Description**: A fully managed service for creating, managing, and using cryptographic keys stored in software.
- **Security**: Uses FIPS 140-2 Level 1 validated cryptographic modules.
- **Key Features**:
  - Supports symmetric and asymmetric keys.
  - Integrates with Google Cloud services like BigQuery, Cloud Storage, and Compute Engine.
  - Key rotation, audit logging, and IAM-based access control.
  - Message size limit: 64 KiB.
  - Regional key storage for data residency compliance.
- **Use Cases**: General-purpose encryption for applications with moderate security needs.
- **Advantages**:
  - Cost-effective and scalable.
  - Low latency for cryptographic operations.
  - Easy to manage with no hardware overhead.
- **Limitations**:
  - Less secure than hardware-based options.
  - May not meet strict compliance requirements (e.g., FIPS 140-2 Level 3).

### 2. Cloud HSM
- **Description**: A managed service storing keys in FIPS 140-2 Level 3 certified Hardware Security Modules (HSMs).
- **Security**: Tamper-resistant hardware with FIPS 140-2 Level 3 certification.
- **Key Features**:
  - Keys never leave the HSM.
  - Supports symmetric and asymmetric keys.
  - Message size limit: 8 KiB.
  - Provides attestation for compliance.
  - Compatible with CMEK-enabled Google
