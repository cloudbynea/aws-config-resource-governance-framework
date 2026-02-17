# Roadmap: Future Enhancements

## Automation
- Add auto-remediation using Lambda for:
  - Enforcing SSE-KMS default encryption
  - Applying mandatory tags based on account/OU metadata
  - Enabling S3 versioning for specific bucket classes

## Preventive Guardrails
- Implement AWS Organizations SCPs to prevent:
  - S3 bucket creation without encryption policies
  - EC2 creation without required tags (where applicable)

## Scale
- Add AWS Config Aggregator for multi-account visibility
- Package rules using Conformance Packs for standardized rollout

## Reporting
- Integrate with AWS Security Hub
- Build compliance dashboards for executive reporting

## Key Management
- Enforce customer-managed KMS keys (CMKs) instead of AWS-managed keys
- Define key policies and rotation standards
