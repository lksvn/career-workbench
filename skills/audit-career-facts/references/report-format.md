# Audit report format

## Summary

State the overall result and counts by severity. Distinguish:

- structural validity;
- factual consistency;
- evidence coverage;
- narrative and translation parity;
- privacy and portability.

## Findings

Order findings by severity, then category. Use this shape:

```text
[severity] category — short title
Affected: file and record or section
Evidence: concise observed facts
Risk: why the difference matters
Recommendation: smallest safe correction
```

Do not include a findings section when there are no actionable findings.

## Unverified scope

List sources, repositories, credentials, dates, or claims that could not be checked. Absence of verification is not automatically a defect when the uncertainty is already represented correctly.

## Checks performed

List the audit passes and tools or schemas actually used. Never claim schema validation when only YAML parsing was performed.
