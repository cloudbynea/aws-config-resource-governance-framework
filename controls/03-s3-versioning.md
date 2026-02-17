# Control 03: S3 Versioning Enforcement

## Control Objective
Ensure S3 buckets have versioning enabled to support recovery from accidental deletion or overwrite and improve resilience.

## Risk Addressed
Without versioning, data loss events are harder to recover from and can create operational and compliance impact.

## Detection Mechanism (AWS Config)
Managed rule:
- s3-bucket-versioning-enabled

Scope:
- AWS resources → S3 Bucket

## Remediation (Manual)
1. Open S3.
2. Select the noncompliant bucket.
3. Go to Properties.
4. Under Bucket Versioning, click Edit.
5. Enable versioning.
6. Save changes.

## Validation
1. Return to AWS Config → Rules.
2. Select s3-bucket-versioning-enabled.
3. Actions → Re-evaluate.
4. Confirm status changes to Compliant.

## Evidence to Capture
- Rule showing Noncompliant resource(s)
- S3 versioning enabled
- Rule showing Compliant after re-evaluation
