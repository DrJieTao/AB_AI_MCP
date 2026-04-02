# Phase 2: Upload Skill ZIP

Do this only after completing `MCP_INSTALL_LOCAL.md`.

## Disclaimer and Consent (Required)

- Educational/classroom use only.
- Not for active betting support or real-money wagering decisions.

By uploading and enabling this Skill, you acknowledge these risks:

1. Skill instructions/scripts can influence tool usage and execution behavior.
2. Skill/tool outputs can be incorrect, outdated, or incomplete.
3. Sensitive information can be exposed if entered in prompts or tool calls.
4. Skill content from untrusted sources may contain unsafe instructions.
5. Any betting-related use is outside intended scope and at user risk.

## Prerequisites

1. Local MCP server is already installed and working.
2. `Code execution and file creation` is enabled in Claude: `Settings > Capabilities`.

## ZIP file to upload

Use one of these equivalent files:

- `distribution/prediction-markets-cmp-skill.zip`
- `skill/prediction-markets-cmp.zip`

Both ZIP files contain the skill folder at ZIP root as required.

## Upload steps in Claude

1. Open `Customize > Skills`.
2. Click `+`, then `+ Create skill`.
3. Choose `Upload a skill`.
4. Select the ZIP file above.
5. After upload, toggle the skill on.

## Confirm the skill is active

1. In `Customize > Skills`, verify the uploaded skill appears and is enabled.
2. Run this prompt in Claude Desktop:

`Use prediction-markets-cmp to compare election markets and include relevance, probability, and links.`

## Troubleshooting

If upload fails:

1. Re-check that the ZIP contains a top-level folder, not loose files.
2. Ensure the folder includes `SKILL.md`.
3. Ensure `Code execution and file creation` remains enabled.
4. Re-upload `distribution/prediction-markets-cmp-skill.zip`.
