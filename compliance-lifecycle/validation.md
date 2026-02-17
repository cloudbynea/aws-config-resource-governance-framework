# Compliance Lifecycle: Validation

## Purpose
Confirm that remediation actions successfully restored compliance and that AWS Config accurately reflects the corrected state.

## Validation Steps
1. Return to AWS Config → Rules.
2. Select the relevant rule.
3. Use Actions → Re-evaluate to trigger evaluation immediately.
4. Refresh the Rules or Dashboard view.
5. Confirm compliance status changes to Compliant.

## What Success Looks Like
- Rule shows Compliant status.
- Affected resource appears as compliant in Resources in scope.
- Resource configuration matches the control objective (verified in the service console).

## Operational Notes
- Status updates may take a few minutes even after re-evaluation.
- If status does not change:
  - Confirm the correct resource was remediated
  - Confirm case-sensitive tag keys/values match the rule
  - Confirm the control requirement was applied to the correct scope

## Evidence to Capture
- Rule status showing Compliant
- Resource configuration page confirming the applied change
