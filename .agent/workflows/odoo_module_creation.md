# Odoo 19 Module Creation
> Prompt: "Create module `[Name]` handling `[Func]`. Use `.agent/workflows/odoo_module_creation.md`"

## Execution
- **Scaffold**: Create `__init__.py`, `__manifest__.py`, `models/`, `views/`, `security/`, `data/`.
- **Manifest**: Must include `name`, `version`, `depends`, `data`, `installable`.
- **Models**: Inherit `models.Model`. Add to `models/__init__.py`.
- **Security**: Create `security/ir.model.access.csv` (and `security.xml` if groups needed). Add to `manifest` (`security.xml` first).
- **Views**: Create XML for menus, actions, forms, trees. Add to `manifest`.
- **Format**: PEP8 for Python, 4-space indent for XML.

## Verification
- Run `odoo-bin -c odoo.conf -u [module]`.
- Verify 0 errors/warnings in logs.

## Fail Conditions
- Missing `depends`.
- Syntax errors in `__manifest__.py`, Python, or XML.
- Missing access rights blocking usage.
