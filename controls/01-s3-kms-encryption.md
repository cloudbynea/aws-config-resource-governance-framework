# Control 01: S3 Default Encryption with KMS

## Control Objective
Ensure all S3 buckets enforce default encryption using AWS KMS (SSE-KMS) to meet enterprise security and compliance requirements.

## Risk Addressed
Buckets without KMS-based default encryption increase the likelihood of data exposure, weaken auditability of key usage, and can violate regulatory expectations.

## Detection Mechanism (AWS Config)
Managed rule:
- s3-default-encryption-kms

Evaluation:
- Continuous

## Remediation (Manual)
1. Open S3.
2. Select the noncompliant bucket.
3. Go to Properties.
4. Under Default encryption, click Edit.
5. Set Encryption type to SSE-KMS.
6. Select an AWS KMS key (example: aws/s3).
7. Save changes.

## Validation
1. Return to AWS Config → Rules.
2. Select s3-default-encryption-kms.
3. Actions → Re-evaluate.
4. Confirm status changes to Compliant.

## Evidence to Capture
- Rule showing Noncompliant resource(s)
- Bucket default encryption set to SSE-KMS
- Rule showing Compliant after re-evaluation
