# Odoo 19 Bugfix
> Prompt: "Fix bug in `[Module]` where `[Issue]`. Use `.agent/workflows/odoo_bugfix.md`"

## Execution
- **Trace**: Locate file/line from stack trace or user description.
- **Isolate**: Determine if issue is Python logic, XML view, or Data rule.
- **Fix**: Apply minimal necessary code modification. Maintain PEP8/XML standards.

## Verification
- Restart server and upgrade module `-u [module]`.
- Mentally trace fixed flow to ensure resolution without regressions.

## Fail Conditions
- Introduces regression to existing features.
- Fails to fully resolve original issue.
- Bypasses security or record rules improperly.
