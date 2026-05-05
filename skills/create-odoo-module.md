# Skill: Create Odoo Module

## Description
This skill enables the agent to scaffold a standard Odoo 19 module structure according to best practices.

## Process
1. **Identify Module Details**: Ask the user for the module's technical name, author, category, and a brief description.
2. **Create `__manifest__.py`**: Generate the manifest file with standard keys (`name`, `version`, `depends`, `data`, `installable`, `application`, `license`). Ensure it correctly declares dependencies (e.g., `base`, `mail`).
3. **Create `__init__.py`**: Initialize models and controllers at the root level.
4. **Scaffold Directories**:
   - `models/` (with `__init__.py`)
   - `views/`
   - `security/` (including an empty `ir.model.access.csv`)
   - `data/` (optional)
   - `controllers/` (with `__init__.py` - optional)
   - `static/src/` (for OWL components - optional)
5. **Verify**: Ensure the module structure is clean and ready to be loaded by Odoo without syntax errors.

## Related Workflows
Refer to `.agent/workflows/odoo_module_creation.md` for the exact step-by-step procedural workflow.
