# Compliance Lifecycle: Detection

## Purpose
Establish continuous visibility into resource configuration drift and identify noncompliant resources against defined governance standards.

## Mechanism
AWS Config continuously records configuration state for selected resource types and evaluates them against managed rules.

Key components:
- Recorder: captures configuration changes
- Delivery channel: stores configuration history in S3
- Rules: evaluate compliance and report results

## What “Noncompliant” Means
A resource is flagged as noncompliant when its current configuration does not satisfy the rule conditions. This is a detective control outcome.

Examples in this framework:
- S3 bucket without SSE-KMS default encryption
- EC2 instance missing required tags or disallowed tag values
- S3 bucket without versioning enabled

## Operational Notes
- Initial evaluations may take a few minutes after rule creation.
- Results can be accelerated using Actions → Re-evaluate on a rule.
- Compliance outcomes should be validated on the resource itself before remediation.

## Evidence to Capture
- Dashboard compliance status showing Noncompliant rule(s) and resource(s)
- Rule details page showing affected resources in scope
