# Odoo 19 Model Extension
> Prompt: "Extend model `[Name]` to add `[Logic]`. Use `.agent/workflows/odoo_model_extension.md`"

## Execution
- **Identify**: Target exact `_name` of the model.
- **Python**: Use `_inherit = 'target.model'`. Call `super()` on overrides.
- **Views**: Use `<field name="inherit_id" ref="[base_view_id]"/>`. Use valid `<xpath expr="..." position="...">`.
- **Manifest**: Add parent module to `depends`. Add new XML to `data`.

## Verification
- Run `odoo-bin -c odoo.conf -u [module]`.
- Verify logs for XML inheritance errors or missing IDs.

## Fail Conditions
- Missing `depends` for inherited module.
- XPath `expr` matches 0 or >1 elements.
- `super()` omitted/incorrect in overrides.
