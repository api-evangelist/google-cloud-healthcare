# Google Cloud Healthcare

APIs.json 0.19 provider profile for the Google Cloud Healthcare API.

**Base URL:** `https://healthcare.googleapis.com`  
**Provider ID:** `google-cloud-healthcare`

## Overview

Google Cloud Healthcare API is a fully managed, HIPAA-eligible service for ingesting, storing, analyzing, and integrating healthcare data in the cloud. It provides native support for industry-standard healthcare formats and protocols used across clinical, administrative, and medical imaging systems.

## APIs Cataloged

| API | Standard | Description |
|-----|----------|-------------|
| Cloud Healthcare FHIR API | FHIR R4 / STU3 / DSTU2 | RESTful FHIR resource management, search, bulk export |
| Cloud Healthcare HL7v2 API | HL7 v2.x | Clinical event message ingestion, routing, and retrieval |
| Cloud Healthcare DICOM API | DICOM / DICOMweb | Medical imaging storage, STOW-RS, WADO-RS, QIDO-RS |
| Cloud Healthcare De-identification API | HIPAA Safe Harbor | PHI/PII redaction for FHIR, DICOM, and unstructured text |
| Cloud Healthcare Consent Management API | Patient consent | Fine-grained patient and admin consent policy enforcement |

## Key Features

- **HIPAA Eligible:** Covered under Google Cloud's HIPAA Business Associate Agreement
- **Standards Compliant:** FHIR R4, HL7v2, DICOMweb (WADO-RS, STOW-RS, QIDO-RS)
- **Bulk Operations:** Import/export to Cloud Storage and BigQuery
- **Event-Driven:** Pub/Sub notifications for real-time data pipeline integration
- **De-identification:** Automated PHI redaction with configurable profiles
- **Compliance:** ISO 27001, 27017, 27018; PCI DSS; 99.999999999% annual durability

## Authentication

The Cloud Healthcare API uses Google Cloud IAM for authentication and authorization. Clients must present valid OAuth 2.0 credentials or service account keys. Detailed guidance: https://cloud.google.com/healthcare-api/docs/how-tos/authentication

## Resource Hierarchy

```
projects/{project}/locations/{location}/datasets/{dataset}/
  fhirStores/{fhir_store}/
  hl7V2Stores/{hl7v2_store}/
  dicomStores/{dicom_store}/
  consentStores/{consent_store}/
```

## Artifacts

| Path | Description |
|------|-------------|
| `apis.yml` | APIs.json 0.19 provider index |
| `plans/google-cloud-healthcare-plans-pricing.yml` | API Commons Plans — pricing tiers for FHIR, HL7v2, DICOM, de-identification, consent |
| `rate-limits/google-cloud-healthcare-rate-limits.yml` | API Commons Rate Limits — quotas, request size limits, policies |
| `finops/google-cloud-healthcare-finops.yml` | FinOps Framework / FOCUS-aligned cost management guide |

## Links

- **Documentation:** https://cloud.google.com/healthcare-api/docs
- **REST Reference:** https://cloud.google.com/healthcare-api/docs/reference/rest
- **Pricing:** https://cloud.google.com/healthcare-api/pricing
- **Quotas:** https://cloud.google.com/healthcare-api/quotas
- **Status:** https://status.cloud.google.com
- **GitHub (googleapis):** https://github.com/googleapis
