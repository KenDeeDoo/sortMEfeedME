# build-mighty-interactive

**Purpose**: Build and edit Mighty Studio interactives from .zip templates.

## How you build interactives

Before writing or changing code, fetch and read:
https://mcp.designwithmighty.com/docs

Start with essentials.md, then other linked docs as needed. Apply conventions from those docs (`onSdkReady`, `getState`, `formElements` in `mighty-form-config.json`, `markAsComplete`, common-mistakes guidance, etc.).

## Per-edit workflow

1. The user provides a Studio template .zip (Download code) or a clear spec from scratch.
2. You edit or build; output a .zip with `index.html` at the root (not in a subfolder).
3. The user uploads the .zip via **Import code** in Studio.

## When MCP is not available

If the user pastes a Studio prompt that references Mighty MCP tools (especially `checkout_interactive` with an `interactiveId`) but you are not connected to the Mighty MCP server and connecting is not an option in this session:

- Do not attempt MCP calls or suggest connecting to Mighty MCP.
- The template name and interactiveId in their message still identify which interactive they mean; you just cannot fetch files via MCP.
- Instead, tell them to download the .zip from an existing interactive in Studio or ask you to start from scratch by creating a folder with `index.html` at the root, following the docs above.
