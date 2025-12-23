# MCP Servers Configuration

**Note:** This document is for backup purposes only.

This file contains the configuration details for the MCP (Model Context Protocol) servers used in the Gemini CLI.

## GitHub MCP Server

*   **URL:** `https://api.githubcopilot.com/mcp/`
*   **Authentication:** Uses a GitHub API key.
*   **Timeout:** 5001ms

## Filesystem MCP Server

*   **Description:** Provides access to the local filesystem.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-filesystem "C:\Users\Sharing\Documents" "C:\Users\Sharing\Desktop"
    ```

## Playwright MCP Server

*   **Description:** Enables browser automation using Playwright.
*   **Installation/Execution:**
    ```bash
    npx -y @playwright/mcp@latest
    ```

## Context7 MCP Server

*   **Description:** Provides access to the Context7 service.
*   **Installation/Execution:**
    ```bash
    npx -y @upstash/context7-mcp@latest --api-key YOUR_CONTEXT7_API_KEY
    ```
    **Note:** Replace `YOUR_CONTEXT7_API_KEY` with your actual API key.

## Sequential Thinking MCP Server

*   **Description:** Enables sequential thinking capabilities.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-sequential-thinking
    ```

## Memory MCP Server

*   **Description:** Provides memory capabilities.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-memory
    ```
