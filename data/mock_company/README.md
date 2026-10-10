# BDACC Technologies — Mock Company Corpus

## Purpose

This directory contains synthetic company documents for TrustRAG,
a permission-aware retrieval-augmented generation (RAG) assistant.

All policies, budgets, and procedures are fictional and intended
for development and evaluation. They are not real company records.

## Corpus documents

| Document ID | Document | Classification |
|---|---|---|
| GEN-001 | General company overview | internal |
| ENG-001 | Engineering incident response | restricted |
| HR-001 | HR leave policy | internal |
| FIN-001 | Finance department budget for 2026 | confidential |

The document registry is maintained in `manifest.json`.

## Roles

- `employee`: general employee access
- `engineer`: engineering documentation
- `hr`: Human Resources documentation
- `finance`: financial documentation
- `manager`: manager-relevant documentation
- `security`: security procedures
- `admin`: access to all documents in this initial corpus

Users may hold multiple roles. The proposed ACL rule permits access
when at least one authorized user role matches a document's `aclRoles`.

The initial general overview is available to `employee` and `admin`.
Incident response is available to `engineer`, `security`, and `admin`.
The leave policy is available to `employee`, `hr`, `manager`, and `admin`.
The budget is available to `finance` and `admin`.

## Metadata notes

The current manifest is a draft pending agreement on the schema contract.

Each document entry includes `doc_id`, `chunk_id`, `path`, `source`,
`timestamp`, `aclRoles`, and `classification`.

The initial chunk IDs are provisional placeholders. The ingestion
pipeline may generate multiple chunks for a source document, and each
chunk will require its own stable identifier and appropriate metadata.

The timestamp values currently represent a provisional dataset timestamp.
Their update and propagation rules must be agreed with the project team.

## Classification

- `public`: intended for access outside the company
- `internal`: intended for authenticated company employees
- `confidential`: sensitive information with restricted role access
- `restricted`: highly sensitive operational or security information

Classification labels describe sensitivity; they do not replace ACL checks.

## Scope

This initial corpus contains four Markdown documents. The role semantics,
chunk metadata contract, and enforcement behavior must be confirmed with
the TrustRAG architecture owner before being treated as finalized.
