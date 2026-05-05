# Odoo 19 View Fix
> Prompt: "Fix view `[XML ID]` to do `[Behavior]`. Use `.agent/workflows/odoo_view_fix.md`"

## Execution
- **Target**: Find exact file declaring or inheriting `[XML ID]`.
- **XPath**: Validate `expr` matches parent structure exactly. Use positions: `inside`, `after`, `before`, `replace`, `attributes`.
- **Syntax**: Ensure valid OWL compatibility, correct field names, and valid python dictionary strings for domains/contexts.

## Verification
- Run `odoo-bin -u [module]`.
- Refresh UI and confirm visual layout.

## Fail Conditions
- References non-existent model fields.
- XPath ambiguity or failure.
- View crashes with Server Error 500.
