# Odoo 19 OWL Component
> Prompt: "Create OWL component for `[Purpose]` in `[Module]`. Use `.agent/workflows/odoo_owl_component.md`"

## Execution
- **Scaffold**: Create `static/src/components/[name]/` with `.js` and `.xml`.
- **JS**: Import `@odoo/owl`. Extend `Component`. Define `static template = "[module].[Name]"`. Register to appropriate Odoo registry.
- **XML**: Use `t-name="[module].[Name]"`. Use OWL directives (`t-if`, `t-on-click`, `t-model`).
- **Manifest**: Bundle under `assets` (e.g., `web.assets_backend`).

## Verification
- Run `odoo-bin -u [module]`.
- Check browser console for JS/template compilation errors.

## Fail Conditions
- Component fails to mount (missing template/registry).
- State mutations occur outside `useState`.
- Assets omitted from `__manifest__.py`.
