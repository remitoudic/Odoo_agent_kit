# Skill: Extend Odoo Model

## Description
This skill allows the agent to safely extend an existing Odoo model (e.g., `res.partner`, `sale.order`) using classical or delegation inheritance.

## Process
1. **Identify the Target Model**: Determine which standard or custom model needs extension.
2. **Create Python Class**:
   ```python
   from odoo import models, fields, api

   class ExtendedModel(models.Model):
       _inherit = 'target.model.name'
       
       # Add new fields or override methods here
       custom_field = fields.Char(string="Custom Field")
   ```
3. **Add to `__init__.py`**: Ensure the new Python file is imported in the `models/__init__.py`.
4. **Update Views**: If new fields are added, use the View Modification skill to inherit the corresponding XML view and inject the new fields using XPath expressions.
5. **Update Manifest**: Ensure the original module containing the target model is listed in the `depends` section of `__manifest__.py`.

## Related Workflows
Refer to `.agent/workflows/odoo_model_extension.md` for standard practices on extending models and views.
