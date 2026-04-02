# Classroom Distribution Guide (Local Claude Desktop)

This guide is for instructors distributing the local `AB_AI_pred_market` MCP server to students using Claude Desktop.

## Classroom-Only Disclaimer

- This toolchain is for educational/classroom use only.
- It is not intended for active betting support, wagering recommendations, or real-money decision support.
- Instructors should explicitly communicate this limitation before students install.

## Required Student Risk Acknowledgment

Before students install both MCP and Skill, require explicit acknowledgment of these risks:

1. Local code execution and script execution on student machines.
2. Claude and tools may process user-provided content that could include sensitive data.
3. Installer changes local Claude Desktop config and may install dependencies.
4. External API/data reliability is not guaranteed (downtime, stale data, partial coverage).
5. Model/tool output may be wrong and should not be treated as financial advice.
6. Misuse for betting can cause financial loss and may violate policy/law.
7. Imported Skills can be unsafe if sourced from untrusted origins.

Suggested consent statement:

"I understand this package is for classroom use only, not for betting support, and I accept the listed technical, privacy, and accuracy risks."

## Goal

Students should install locally with as little terminal work as possible.

Install expectation: students must install on their own personal devices.

## What to Distribute

Distribute the `AB_AI_pred_market` folder containing:

- `install_for_students_macos.command`
- `verify_student_install_macos.command`
- `install_for_students_windows.cmd`
- `install_for_students_windows.ps1`
- `verify_student_install_windows.cmd`
- `verify_student_install_windows.ps1`
- `ab_ai_pred_market/`
- `pyproject.toml`

Optional (recommended for support):

- `TROUBLESHOOTING.md`
- `README.md`

## Instructor Prep (one-time)

From `AB_AI_pred_market` run:

```bash
chmod +x install_for_students_macos.command
chmod +x verify_student_install_macos.command
```

Then zip and share the folder.

## Student Steps (Windows)

1. Unzip the folder.
2. Double-click `install_for_students_windows.cmd`.
3. If Windows prompts for permission, allow it.
4. Wait for "Installation complete".
If Python is missing, installer attempts to install Python 3.12 with winget.
5. Quit Claude Desktop fully and reopen it.
6. (Optional check) Run `verify_student_install_windows.cmd`.

## Student Steps (macOS)

1. Unzip the folder.
2. Right-click `install_for_students_macos.command` and choose Open.
3. If macOS warns about an unsigned file, click Open again.
4. Wait for "Installation complete".
If Python is missing, the installer automatically installs Homebrew and Python 3.12 (internet + admin password may be required).
5. Quit Claude Desktop fully and reopen it.
6. (Optional check) Run `verify_student_install_macos.command`.

## Simple Classroom Verification Prompt

After restart, students can test with:

"Find prediction markets about election and show top 5 with source platform and links."

If tools are not visible, run `verify_student_install_macos.command` and consult `TROUBLESHOOTING.md`.

## Notes for Non-Technical Students

- No manual config editing is required by default.
- Installer automatically creates a private Python environment in `.venv-student`.
- Installer automatically updates `~/Library/Application Support/Claude/claude_desktop_config.json` and preserves other MCP servers.
- If Python is not already installed, installer attempts to install Homebrew and Python automatically.
- On Windows, installer attempts Python installation through winget when Python is missing.

## What if things go wrong? (Instructor support map)

Use plain language with students and start with these common cases:

1. "Installer will not open"
- macOS: have student right-click installer and choose Open.
- Windows: have student run `.cmd` file and allow the prompt on their own device.

2. "Dependency install failed"
- macOS: check internet and password prompt acceptance for Homebrew/Python install.
- Windows: check `winget --version`; if missing, have student install Python manually.

3. "Installed, but no tools in Claude"
- Fully quit and reopen Claude Desktop.
- Run OS verify script and review output.

4. "Skill ZIP upload fails"
- Ensure `Code execution and file creation` is enabled.
- Re-upload the packaged classroom ZIP for the skill.

Ask students to provide:

1. Screenshot of exact error.
2. OS type (macOS/Windows).
3. Last successful step.
4. Verify script output.

Escalation rule:

- Students should contact the instructor only as a last resort after trying the listed fixes once.

Official references for support staff:

- Local MCP setup/troubleshooting:
	https://support.claude.com/en/articles/10949351-getting-started-with-local-mcp-servers-on-claude-desktop
- Skills setup/troubleshooting:
	https://support.claude.com/en/articles/12512180-use-skills-in-claude
- Skill ZIP structure rules:
	https://support.claude.com/en/articles/12512198-how-to-create-custom-skills
- Claude support channels:
	https://support.claude.com/en/articles/9015913-how-to-get-support
