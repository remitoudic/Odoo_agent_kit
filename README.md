# Antigravity Odoo 19 Development Workflows

This directory contains standard operating procedures (workflows) for developing Odoo 19 applications with the Antigravity AI assistant. 

## How to Use

When you want to start a new task, simply point me (Antigravity) to the relevant workflow file in your prompt. You can also use the prompt templates provided at the top of each workflow file.

For example:
> "Please create a new Odoo module for managing library books. Follow the instructions in `.agent/workflows/odoo_module_creation.md`"

I will automatically read the workflow instructions and follow the standardized steps.

## Available Workflows

### Core Backend & Structure
- **[odoo_module_creation.md](odoo_module_creation.md)**: Steps for scaffolding and creating a completely new Odoo 19 module.
- **[odoo_model_extension.md](odoo_model_extension.md)**: Steps for extending an existing Odoo model (using `_inherit`).

### Views & Frontend
- **[odoo_view_fix.md](odoo_view_fix.md)**: Guidelines for fixing or modifying Odoo XML views (forms, lists, kanban, etc.).
- **[odoo_owl_component.md](odoo_owl_component.md)**: Steps for creating or extending modern OWL (Odoo Web Library) components in JavaScript/XML.

### Logic & Security
- **[odoo_controller.md](odoo_controller.md)**: Steps for creating custom web routes and REST API endpoints.
- **[odoo_security.md](odoo_security.md)**: Advanced security setups including access rights and record rules.

### Quality Assurance
- **[odoo_bugfix.md](odoo_bugfix.md)**: Standard procedure for identifying, reproducing, and fixing bugs.
- **[odoo_test_generation.md](odoo_test_generation.md)**: Instructions for writing and running Python unit tests or JS Tour tests.

## References

- Guidelines and best practices adapted from [Cursor Directory - Odoo Plugin](https://cursor.directory/plugins/odoo).
