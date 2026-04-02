# AB_AI_pred_market

`AB_AI_pred_market` is a local MCP server for Claude Desktop focused on prediction market retrieval.

## MCP Tools

- `search_markets(keyword, platform, status)`
- `get_market(ticker, platform)`

## Canonical Output Schema

All platform results are normalized to:

- `title`
- `probability`
- `volume`
- `url`
- `platform`
- `closes_at`

## Coverage Safety

- Kalshi keyword retrieval includes fallback list filtering when direct search returns zero.
- Hard rate limiting is enforced in server runtime.

## Install

```bash
/opt/homebrew/bin/python3 -m pip install --user --break-system-packages .
```

Then configure Claude Desktop with `claude_desktop_config.json.example`.

## Run Coverage Test (before packaging)

```bash
/opt/homebrew/bin/python3 scripts/test_api_coverage.py
```

Reports are written into `reports/`.
