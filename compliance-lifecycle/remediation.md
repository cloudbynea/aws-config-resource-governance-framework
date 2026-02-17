# Compliance Lifecycle: Remediation

## Purpose
Correct noncompliant configurations detected by AWS Config and restore baseline governance posture.

## Remediation Model Used
This implementation uses manual remediation to demonstrate the compliance lifecycle end-to-end.

Manual remediation steps typically include:
1. Navigate from AWS Config rule → affected resource
2. Confirm configuration gap
3. Apply corrective change in the service console
4. Record evidence (before/after)

## Remediation Actions in This Framework

### S3 KMS Encryption
- Enable SSE-KMS default encryption on the noncompliant bucket.
- Select an AWS KMS key (example: aws/s3).

### EC2 Required Tags
- Add missing tags using exact, case-sensitive keys and values.
- Ensure value constraints match rule parameters (Environment, AuditLevel).

### S3 Versioning
- Enable bucket versioning on the noncompliant bucket.

## Remediation Quality Criteria
- Changes align with the stated control objective.
- Changes do not introduce new risk (for example, excessive permissions).
- Evidence is captured consistently to support audit-ready documentation.
