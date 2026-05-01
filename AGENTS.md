## Project Overview
Python 3.12 MCP server that exposes Ghidra reverse-engineering operations to MCP clients through a local Ghidra HTTP bridge.

## Structure Map
```text
ghidra-mcp/
|- main.py              # MCP server entrypoint, tool registry, Ghidra HTTP client helpers, and transport startup
|- pyproject.toml       # Package metadata, Python requirement, dependencies, console script, and build backend
|- uv.lock              # Locked dependency graph for reproducible uv installs
\- README.md            # Project README; currently empty
```

## Development Guide
```bash
# Build package
uv build

# Verify syntax and entrypoint wiring
uv run python -m compileall main.py
uv run ghidra-mcp --help
```

No test suite or typecheck command is currently configured.
