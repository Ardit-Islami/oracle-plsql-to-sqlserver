# oracle-plsql-to-sqlserver

High-signal, runnable examples translating **Oracle PL/SQL fundamentals** into **SQL Server T-SQL** equivalents.

This repo exists to turn a company-provided PL/SQL course into **portable, employer-agnostic evidence** of database programming ability: procedural SQL, error handling, cursors, triggers, and “how the same idea looks in a different engine”.

## What this demonstrates (skills signal)

* **Procedural database programming**: variables, control flow, loops, modular code
* **Stored program units**: procedures & functions (PL/SQL ↔ T-SQL patterns)
* **Error handling**: Oracle exceptions ↔ SQL Server TRY/CATCH + THROW/RAISERROR patterns
* **Cursors**: explicit cursor mechanics and why/when to avoid them
* **Triggers**: auditing and integrity patterns
* **Cross-dialect translation**: mapping constructs between Oracle and SQL Server (practical, not theoretical)

## Repo structure

Each concept is implemented twice:

* `oracle/` — Oracle PL/SQL scripts
* `sqlserver/` — SQL Server T-SQL equivalents

Folder mapping:

* `01_basics/` — block structure, variables, types, control flow
* `02_procedures_functions/` — procedures, functions, parameters, modularization
* `03_exceptions/` (Oracle) / `03_error_handling/` (SQL Server) — error patterns, custom errors
* `04_cursors/` — cursor patterns + alternatives
* `05_triggers/` — DML triggers, auditing, guardrails

File naming convention:

* `<nn>_<topic>.sql` (e.g., `01_vars_and_types.sql`) to keep progression clear.

## How to use

### Option A — SQL Server (SSMS)

1. Open any script under `sqlserver/` in SSMS.
2. Run it against a local/dev database.
3. Scripts are written to be self-contained where possible (create objects, run demo calls, show output).

### Option B — Oracle

Run scripts under `oracle/` using one of:

* Oracle SQL Developer
* SQL*Plus
* Any Oracle environment provided by the course

(Oracle setup details depend on your environment; see course guidance or your preferred local setup.)

## Translation principles (what I’m practicing)

This repo focuses on “closest equivalent” rather than assuming the engines are identical.

Examples:

* **PL/SQL EXCEPTION** → **T-SQL TRY/CATCH**
* **SQLCODE/SQLERRM** → **ERROR_NUMBER()/ERROR_MESSAGE()**
* **Oracle SEQUENCE** → **SQL Server SEQUENCE or IDENTITY**
* **Oracle packages** → (no direct equivalent) **schema + stored procs/functions** in SQL Server
* **Collections / RECORD types** → **table variables / temp tables / user-defined table types** (when appropriate)

Where a feature is not 1:1, the SQL Server file includes a short note explaining the tradeoff.

## Portfolio-relevant

Many learners finish a vendor course with only a certificate. I wished to ensure that this repo adds:

* **Runnable code** (proof of execution, not just theory)
* **Cross-engine competency** (useful in mixed-stack teams)
* **Database-engineering habits** (clear structure, naming, and reproducible examples)

## Course context

The learning source is a company-provided Oracle PL/SQL Fundamentals course.
All code and notes here are written independently as practice artifacts—no proprietary company data is included.

## License

MIT
