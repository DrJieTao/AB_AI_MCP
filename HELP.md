# AB_AI_pred_market Share Bundle Help

## Required Disclaimer

- This package is for classroom use and educational purposes only.
- It is not for active betting support, wagering strategy, or real-money betting decisions.
- Students should install this package on their own personal devices.

## Required Risk Acknowledgment (Install MCP + Skill)

Before proceeding, users should explicitly acknowledge:

1. Local scripts and code will execute during install and usage.
2. Claude/tool interactions may process sensitive user-entered data.
3. Installer modifies local Claude Desktop configuration.
4. Runtime dependencies may be installed automatically on the host machine.
5. External market/API data may be stale, incomplete, or unavailable.
6. Tool/model output can be incorrect and must not be treated as financial advice.
7. Misuse for betting can lead to financial loss and possible policy/regulatory issues.
8. Skills from untrusted sources can introduce security and prompt-injection risks.

Proceed only if these risks are understood and accepted.

This folder is a classroom-ready share package that includes:

- MCP server: `mcp/AB_AI_pred_market`
- Wrapper skill: `skill/prediction-markets-cmp`
- Ready-to-share archives: `distribution/`

Use this order:

1. Install the local MCP server first.
2. Upload and enable the Skill ZIP second.

## What this bundle does

- Adds MCP tools to Claude Desktop for prediction market lookup.
- Adds a deterministic wrapper workflow for search, compare, monitor, and local-history synthesis.
- Avoids shipping generated test outputs and temporary artifacts.

## Included install guides

For installation details, use these files:

- `mcp/AB_AI_pred_market/INSTALL.md`
- `mcp/AB_AI_pred_market/CLASSROOM_DISTRIBUTION.md`
- `mcp/AB_AI_pred_market/TROUBLESHOOTING.md`
- `mcp/AB_AI_pred_market/README.md`
- `MCP_INSTALL_LOCAL.md`
- `SKILL_UPLOAD.md`

## Streamlined two-phase setup

### Phase 1: Local MCP server (required first)

Follow `MCP_INSTALL_LOCAL.md`.

Quick path:

- macOS: run `mcp/AB_AI_pred_market/install_for_students_macos.command`
- Windows: run `mcp/AB_AI_pred_market/install_for_students_windows.cmd`

Optional verification:

- macOS: `mcp/AB_AI_pred_market/verify_student_install_macos.command`
- Windows: `mcp/AB_AI_pred_market/verify_student_install_windows.cmd`

### Phase 2: Skill ZIP upload (after MCP install)

Follow `SKILL_UPLOAD.md`.

Use either ZIP:

- `distribution/prediction-markets-cmp-skill.zip`
- `skill/prediction-markets-cmp.zip`

Upload flow in Claude:

1. Enable `Code execution and file creation` in `Settings > Capabilities`.
2. Open `Customize > Skills`.
3. Click `+` then `+ Create skill`.
4. Choose `Upload a skill` and upload the ZIP.
5. Toggle the uploaded skill on.

## Visual quickstart (student view)

Use this as a visual checklist while following `MCP_INSTALL_LOCAL.md` and `SKILL_UPLOAD.md`:

1. Unzip package and open folder.
2. Double-click installer file:
- macOS: `mcp/AB_AI_pred_market/install_for_students_macos.command`
- Windows: `mcp/AB_AI_pred_market/install_for_students_windows.cmd`
3. Approve OS security prompts when asked.
4. Wait for `Installation complete`.
5. Fully quit and reopen Claude Desktop.
6. Open Claude settings and confirm Skills are enabled:
- `Settings > Capabilities > Code execution and file creation`
7. Upload skill ZIP:
- `Customize > Skills > + > + Create skill > Upload a skill`
- Select `distribution/prediction-markets-cmp-skill.zip`
8. Toggle the uploaded skill on.
9. Run one MCP test prompt and one Skill test prompt.

Expected prompts/warnings students may see:

- macOS warning for unsigned script: choose Open.
- macOS password prompt during Homebrew install.
- Windows SmartScreen / script prompt: choose Run / allow.
- Windows package install notice from winget.

If what you see does not match this sequence, stop and continue with the troubleshooting section below.

## Preflight check (before install)

Students should verify these items before running installers:

1. Claude Desktop is installed and updated.
2. Stable internet connection is available.
3. You can install software on this machine (admin permission if required).
4. Enough free disk space for Python and dependencies.
5. You are installing on your own personal device and can allow installer prompts.

Optional quick checks:

- macOS Terminal: `xcode-select -p` (if missing, macOS may prompt for developer tools during setup)
- Windows PowerShell: `winget --version` (required for automatic Python install path)

If any check fails, stop and fix it before installation.

## What if things go wrong? (plain-language support)

If setup fails, do not panic. Most issues are fixable in a few minutes.

Use this order:

1. Try the quick fix listed below for your issue.
2. Retry the step once.
3. If it still fails, contact your instructor as a last resort and share the requested evidence.

### macOS common issues

1. Problem: "The installer will not open."
- Try this: right-click `install_for_students_macos.command` and choose Open.
- If blocked again: open macOS security prompt and allow the file, then retry.
- Official help: https://support.claude.com/en/articles/10949351-getting-started-with-local-mcp-servers-on-claude-desktop

2. Problem: "It asks for password or long install download."
- Try this: this is expected when Homebrew/Python is missing.
- What to do: stay connected to internet, enter your macOS password if you trust the classroom package, and wait until `Installation complete`.
- If it loops/fails: restart and rerun installer once.

3. Problem: "Installer finished but I still do not see tools in Claude."
- Try this: fully quit Claude Desktop, reopen it, then run verify script:
	`mcp/AB_AI_pred_market/verify_student_install_macos.command`
- Official help: local MCP troubleshooting and connection checks
	https://support.claude.com/en/articles/10949351-getting-started-with-local-mcp-servers-on-claude-desktop

### Windows common issues

1. Problem: "Windows warns me before running the installer."
- Try this: run `install_for_students_windows.cmd` and allow the script if your instructor provided the package.
- If Windows still blocks it: restart Windows once and try again.

2. Problem: "Python install failed."
- Try this: open PowerShell and run `winget --version`.
- If command is missing: install Python 3.11+ manually on your own device, then rerun installer.

3. Problem: "Installer finished but tools are missing in Claude."
- Try this: fully quit Claude Desktop, reopen it, then run:
	`mcp/AB_AI_pred_market/verify_student_install_windows.cmd`
- Official help: local MCP troubleshooting and permission guidance
	https://support.claude.com/en/articles/10949351-getting-started-with-local-mcp-servers-on-claude-desktop

### Skill upload common issues (both OS)

1. Problem: "I cannot see Skills settings."
- Try this: enable `Code execution and file creation` in `Settings > Capabilities`.
- Official help: Skills prerequisites and enable steps
	https://support.claude.com/en/articles/12512180-use-skills-in-claude

2. Problem: "Skill ZIP upload fails."
- Try this checklist:
	1) upload `distribution/prediction-markets-cmp-skill.zip`
	2) make sure ZIP is not corrupted
	3) make sure ZIP contains a top-level skill folder (not loose files)
- Official help: ZIP packaging rules for custom Skills
	https://support.claude.com/en/articles/12512198-how-to-create-custom-skills

3. Problem: "Skill uploaded, but Claude does not use it."
- Try this:
	1) confirm skill toggle is ON in `Customize > Skills`
	2) ask explicitly: `Use prediction-markets-cmp for this request`
	3) retry with a clearer task
- Official help: Skill troubleshooting
	https://support.claude.com/en/articles/12512180-use-skills-in-claude

### If you still need help

Share this with your instructor (last resort):

1. Your OS and version (macOS or Windows).
2. Screenshot of the exact error.
3. Last step completed from this file.
4. Output (or screenshot) from the verify script.

Official Claude support options:

- How to get support: https://support.claude.com/en/articles/9015913-how-to-get-support
- Skills help center article: https://support.claude.com/en/articles/12512180-use-skills-in-claude
- Local MCP help center article: https://support.claude.com/en/articles/10949351-getting-started-with-local-mcp-servers-on-claude-desktop

## Post-install checklist (student submission)

Students can submit this checklist after setup:

- [ ] I read the classroom-only and risk disclaimer.
- [ ] MCP installer completed successfully on my machine.
- [ ] I restarted Claude Desktop after install.
- [ ] MCP test prompt returned market results with sources/links.
- [ ] Skill ZIP uploaded and is enabled in `Customize > Skills`.
- [ ] Skill test prompt returned relevance/probability style output.
- [ ] I know where to find troubleshooting steps in this file.

Suggested evidence for instructor:

1. Screenshot of enabled Skill in `Customize > Skills`.
2. Screenshot of one successful MCP prompt result.
3. Screenshot of one successful Skill-guided prompt result.

## Student install

### macOS

1. Open `mcp/AB_AI_pred_market`.
2. Run `install_for_students_macos.command`.
3. Restart Claude Desktop.
4. Optional: run `verify_student_install_macos.command`.

### Windows

1. Open `mcp/AB_AI_pred_market`.
2. Run `install_for_students_windows.cmd`.
3. Restart Claude Desktop.
4. Optional: run `verify_student_install_windows.cmd`.

Notes:
- macOS installer attempts Homebrew and Python install if needed.
- Windows installer attempts Python install via winget if needed.
- Both installers create `.venv-student` and update Claude Desktop config safely.

## Separate distribution artifacts

You can distribute these two files separately:

- Local MCP package: `distribution/AB_AI_pred_market_mcp_local.zip`
- Skill upload package: `distribution/prediction-markets-cmp-skill.zip`

## How to use in Claude

After installation and restart, ask prompts like:

- Find prediction markets about election and show top 5 with sources and links.
- Compare Trump and Biden 2028 markets across platforms.
- Monitor election markets and flag large probability moves.
- Show local history trend for this market over the last 7 days.

## Skill usage notes

The wrapper skill is in:

- `skill/prediction-markets-cmp/SKILL.md`

It expects MCP responses from `AB_AI_pred_market` and runs deterministic scripts for:

- request classification,
- query expansion,
- result merge and normalization,
- local snapshot persistence,
- compare/monitor/history synthesis,
- final response rendering.

## For instructors

1. Distribute the entire `AB_AI_pred_market_share_20260331` folder.
2. Or distribute only the two separate ZIPs in `distribution/`.
3. Enforce order: MCP install first, Skill upload second.

## What was intentionally excluded

To keep this package clean, generated artifacts are excluded, including:

- report outputs,
- test output snapshots,
- live input captures,
- build directories,
- cache directories,
- temporary files.
