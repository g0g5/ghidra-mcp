# ghidra-mcp

This project is a Python package for installing and running the Python bridge for Ghidra MCP.

All Python source code comes from [LaurieWired/GhidraMCP](https://github.com/LaurieWired/GhidraMCP). This repository only repackages that source code as a PyPI package so it can be installed and invoked more easily from the command line.

## Installation

Install from GitHub with `uv tool install`:

```bash
uv tool install ghidra-mcp --from git+https://github.com/g0g5/ghidra-mcp.git
```

Note: this project only includes the Python bridge. It does not include the MCP server plugin for Ghidra. Follow the instructions in the original [LaurieWired/GhidraMCP](https://github.com/LaurieWired/GhidraMCP) repository to install and enable the Ghidra plugin.

## Usage

Before starting the bridge, make sure the MCP server plugin is running inside Ghidra and listening on the expected HTTP address, such as `http://127.0.0.1:8080/`.

A typical MCP configuration looks like this:

```json
{
  "mcp": {
    "ghidra": {
      "type": "local",
      "command": [
        "ghidra-mcp",
        "--ghidra-server",
        "http://127.0.0.1:8080/"
      ]
    }
  }
}
```
