# AST Injection Guide

Use AST-aware edits to reduce syntax errors and preserve code structure.

## Principles
- Prefer structural edits over raw string replacement.
- Insert code in the correct AST node or list position.
- Preserve formatting and order when possible.

## When AST Is Not Available
- Minimize edit scope and verify with tests.
- Document assumptions in auto-context or ADRs.
