# Phase 1: Install Local MCP Server

This phase installs the local MCP server for Claude Desktop.
Complete this before uploading any Skill ZIP.

## Disclaimer and Consent (Required)

- Educational/classroom use only.
- Not for active betting support or real-money wagering decisions.

By continuing, you acknowledge these installation risks:

1. Local code execution and script execution on your machine.
2. Automatic installation of dependencies/runtimes may occur.
3. Claude Desktop configuration files will be updated.
4. External data sources may be unavailable or inaccurate.
5. Results are informational only and can be wrong.

## macOS

1. Open `mcp/AB_AI_pred_market`.
2. Double-click `install_for_students_macos.command`.
3. If prompted, allow the script to run.
4. Wait for `Installation complete`.
5. Quit Claude Desktop fully, then reopen it.

Optional verification:

1. Run `verify_student_install_macos.command`.
2. Confirm all checks pass.

## Windows

1. Open `mcp/AB_AI_pred_market`.
2. Double-click `install_for_students_windows.cmd`.
3. If prompted, allow PowerShell/script execution.
4. Wait for `Installation complete`.
5. Quit Claude Desktop fully, then reopen it.

Optional verification:

1. Run `verify_student_install_windows.cmd`.
2. Confirm all checks pass.

## What this installer configures

1. Finds or installs Python 3.11+.
2. Creates `.venv-student`.
3. Installs `AB_AI_pred_market`.
4. Updates Claude Desktop MCP config with server entry `AB_AI_pred_market`.

## Smoke test prompt

After restart, test in Claude Desktop:

`Find prediction markets about election and show top 5 with source platform and links.`
