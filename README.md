# Google Cloud Healthcare

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
