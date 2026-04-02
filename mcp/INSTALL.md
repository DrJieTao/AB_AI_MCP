# Install Guide (Claude Desktop Local)

## Important Disclaimer (Read First)

- This MCP package and related Skill are for classroom use and educational purposes only.
- They are not for active betting support, wagering decisions, or investment/trading advice.
- Do not use outputs from this toolchain to place real-money bets.

## Explicit Risk Acknowledgment (MCP + Skill)

By installing and enabling both the local MCP server and the Skill, you explicitly acknowledge and accept these risks:

1. Code execution risk: installation and Skill workflows run local code and scripts on your machine.
2. Data exposure risk: prompts, tool inputs, and tool outputs may include sensitive information if entered by users.
3. Configuration change risk: installer modifies Claude Desktop MCP configuration files.
4. Dependency risk: installer may install system/runtime dependencies (for example Python, Homebrew, winget packages).
5. Network/API risk: tools may call external endpoints and can fail, timeout, or return incomplete results.
6. Accuracy risk: market data can be stale, incorrect, missing, or mismatched to user intent.
7. Financial/legal risk: misuse for betting or financial decisions may cause monetary loss or policy/regulatory violations.
8. Security risk: Skills from untrusted sources can contain unsafe instructions or code.

Proceed only if you understand and accept all risks above.

## Recommended for students (macOS)

Use the one-click installer:

```bash
cd AB_AI_pred_market
./install_for_students_macos.command
```

This installer will:

- auto-install Python (via Homebrew) if needed,
- create `.venv-student`,
- install `AB_AI_pred_market`,
- and update Claude Desktop config safely.

## Recommended for students (Windows)

Use the one-click installer:

```powershell
cd AB_AI_pred_market
install_for_students_windows.cmd
```

This installer will:

- auto-install Python (via winget) if needed,
- create `.venv-student`,
- install `AB_AI_pred_market`,
- and update Claude Desktop config safely.

## 1) Install package

```bash
cd AB_AI_pred_market
/opt/homebrew/bin/python3 -m pip install --user --break-system-packages .
```

## 2) Configure Claude Desktop

Copy from `claude_desktop_config.json.example` and adjust absolute paths.

- macOS config path: `~/Library/Application Support/Claude/claude_desktop_config.json`
- Windows config path: `%APPDATA%\\Claude\\claude_desktop_config.json`

## 3) Restart Claude Desktop

After restart, verify tools are visible:

- `search_markets`
- `get_market`

## 4) Validate API retrieval coverage before packaging

```bash
cd AB_AI_pred_market
/opt/homebrew/bin/python3 scripts/test_api_coverage.py
```

Check `reports/api_coverage_latest.md` and ensure both platforms return non-zero coverage for at least part of the query set.
