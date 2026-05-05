# Odoo 19 Web Controller
> Prompt: "Create route `[Endpoint]` in `[Module]`. Use `.agent/workflows/odoo_controller.md`"

## Execution
- **Scaffold**: Create `controllers/main.py`. Include in `controllers/__init__.py`.
- **Class**: Inherit `odoo.http.Controller`.
- **Route**: Decorate with `@http.route('...', type='http/json', auth='public/user')`.
- **Security**: Apply `csrf=False` only if strictly necessary (e.g., external webhooks).

## Verification
- Restart server.
- Hit endpoint via `curl` or browser. Ensure correct 2xx HTTP response.

## Fail Conditions
- Route conflicts with core Odoo paths.
- `auth='public'` exposes private data.
- 500 error from unhandled Python exceptions.
