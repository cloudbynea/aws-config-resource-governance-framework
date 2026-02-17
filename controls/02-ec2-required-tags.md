# Control 02: EC2 Required Tags Enforcement

## Control Objective
Enforce mandatory governance tags on EC2 instances to enable accountability, cost allocation, and audit classification.

## Risk Addressed
Untagged or inconsistently tagged resources create operational ambiguity, reduce cost visibility, and weaken audit readiness.

## Detection Mechanism (AWS Config)
Managed rule:
- required-tags

Scope:
- AWS resources → EC2 Instance

## Required Tags
| Key         | Allowed Values              |
|-------------|----------------------------|
| CostCenter  | Any value                  |
| Environment | Prod, QA, Dev, Staging     |
| AuditLevel  | PII, Normal, PCI           |
| Name        | Any value                  |
| Owner       | Any value                  |

## Remediation (Manual)
1. Open EC2 → Instances.
2. Select the noncompliant instance.
3. Open Tags → Manage tags.
4. Add missing tags (case-sensitive).

Example:
- CostCenter = 1337
- Environment = QA
- AuditLevel = Normal
- Owner = Ryan
- Name = WebServer

## Validation
1. Return to AWS Config → Rules.
2. Select required-tags.
3. Actions → Re-evaluate.
4. Confirm status changes to Compliant.

## Evidence to Capture
- Rule showing Noncompliant resource(s)
- EC2 tags before and after
- Rule showing Compliant after re-evaluation
