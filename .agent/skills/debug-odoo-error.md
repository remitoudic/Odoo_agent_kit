# Skill: Debug Odoo Error

## Description
This skill equips the agent to analyze tracebacks and fix common Odoo 19 errors (e.g., MissingError, ValidationError, AccessError, XML architecture errors).

## Process
1. **Analyze Traceback**: Read the Python or JavaScript traceback provided by the user. Pinpoint the exact file and line number causing the issue.
2. **Identify Error Type**:
   - *Database/ORM*: Check for missing module dependencies, unassigned required fields, or missing `ir.model.access.csv` rules.
   - *View/XML*: Look for invalid XPath expressions, referencing missing fields in the model, or mismatched XML tags.
   - *Python Logic*: Look for missing `super()` calls, incorrect domain/context syntax, or type errors.
3. **Formulate Fix**:
   - Modify the Python model logic safely.
   - Correct the XML view definition.
   - Update security rules if it's an AccessError.
4. **Validation**: Advise the user to restart the Odoo server with `-u module_name` (or `-d db_name -u module_name`) to apply the fixes and test.

## Related Workflows
Refer to `.agent/workflows/odoo_bugfix.md` for deeper debugging workflows and log analysis strategies.
