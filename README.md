Claude + MCP + DTools Integration

Overview
This document explains how to set up and use Claude AI with MCP (Modular Command Platform) and DTools.
The goal is to build an MCP server that exposes tools and resources which can be consumed by Claude for advanced AI-driven workflows.

Prerequisites
- Python 3.10+
- Node.js 18+
- Visual Studio Code
- Claude Pro account
- uv (Python package manager)

Project Setup

Step 1: Create Project Folder
1. Open Visual Studio Code
2. Create a new folder for the project
3. Open the terminal

Step 2: Install uv and Initialize Project
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

uv init claude-mcp-dtools
cd claude-mcp-dtools

Step 3: Add MCP Dependency
uv add "mcp[cli]"

Step 4: Install MCP Server Script
uv run mcp install main.py

Creating MCP Server

Create a file named main.py

Add a Tool
All MCP tools are defined and registered inside the main.py file. This file contains the core business logic,
DTools integrations, and MCP tool definitions used by Claude.

Add a Resource
Resources are implemented within main.py and exposed through MCP for Claude to consume dynamically.

Running the Server
python main.py

Integrating with Claude
- Open Claude Desktop
- Configure MCP server in Claude settings
- Allow tool access
- Claude can now invoke tools and resources exposed by MCP

Using DTools
DTools can be layered on top of MCP tools to enable scalable automation and intelligent orchestration.

Disclaimer
This document and implementation are provided by Officehubtech for reference purposes only.
Officehubtech is not responsible for any data loss, system issues, or damages arising from the use of this setup.

© Officehubtech

