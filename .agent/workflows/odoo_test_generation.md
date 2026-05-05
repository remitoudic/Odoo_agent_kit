# Odoo 19 Test Generation
> Prompt: "Write tests for `[Model/Flow]` in `[Module]`. Use `.agent/workflows/odoo_test_generation.md`"

## Execution
- **Type**: Backend = Python (`tests/`), Frontend = JS Tours (`static/tests/tours/`).
- **Python Setup**: Create `tests/test_[name].py`. Inherit `common.TransactionCase`. Initialize data in `setUp()`. Prefix methods with `test_`.
- **JS Setup**: Use `@web_tour/tour` registry.
- **Data**: Create data via `self.env` in code, not XML, for isolation.

## Verification
- Run: `odoo-bin -c odoo.conf -i [module] --test-enable`
- Assert 0 failures, 0 errors.

## Fail Conditions
- Flaky tests dependent on external DB state.
- Unclean data teardown.
- Insufficient coverage of target flow.
