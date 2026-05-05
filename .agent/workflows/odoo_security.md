# Odoo 19 Security
> Prompt: "Configure security for `[Model]` in `[Module]`. Use `.agent/workflows/odoo_security.md`"

## Execution
- **Groups**: Define `res.groups` in `security.xml` if custom roles needed.
- **Access Rights**: Define ACLs in `ir.model.access.csv`. Grant read/write/create/unlink (1 or 0) for mapped groups.
- **Record Rules**: Define `ir.rule` in `security.xml`. Set `domain_force` to restrict row-level access.
- **Order**: In `__manifest__.py`, list `security.xml` BEFORE `ir.model.access.csv`.

## Verification
- Upgrade module `-u [module]`.
- Test operations as a restricted user to ensure Access Errors trigger correctly.

## Fail Conditions
- CSV syntax error (trailing commas, missing IDs).
- Misordered manifest load crashes install.
- Over-restrictive rule breaks system admin functionality.
