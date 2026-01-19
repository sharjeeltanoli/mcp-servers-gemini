# MCP Servers Configuration

**Note:** This document is for backup purposes only.

This file contains the configuration details for the MCP (Model Context Protocol) servers used in the Gemini CLI, based on the `settings.json` backup.

## 1. GitHub MCP Server (`github`)
*   **Description:** Provides integration with GitHub to manage repositories, issues, pull requests, and file contents.
*   **Purpose:** Allows the agent to interact with your GitHub repositories directly.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-github
    ```
*   **Authentication:** Requires a GitHub Personal Access Token (PAT). This is typically set via the `GITHUB_PERSONAL_ACCESS_TOKEN` environment variable.

## 2. Filesystem MCP Server (`filesystem`)
*   **Description:** Grants the agent access to read and write files within specific directories on your local machine.
*   **Purpose:** Essential for performing file operations like creating components, reading configurations, or analyzing codebases.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-filesystem "YOUR_DOCUMENTS_PATH" "YOUR_DESKTOP_PATH"
    ```
*   **Configuration:** Replace `YOUR_DOCUMENTS_PATH` and `YOUR_DESKTOP_PATH` with the absolute paths to the directories you want the agent to access.

## 3. Playwright MCP Server (`playwright`)
*   **Description:** Enables browser automation capabilities using Playwright.
*   **Purpose:** Used for web testing, scraping, taking screenshots, and verifying web application behavior.
*   **Installation/Execution:**
    ```bash
    npx -y @playwright/mcp@latest
    ```

## 4. Vercel MCP Server (`vercel`)
*   **Description:** Integrates with the Vercel platform.
*   **Purpose:** Allows management of Vercel projects, deployments, and related resources.
*   **Connection:**
    *   **URL:** `https://mcp.vercel.com`
*   **Authentication:** Typically requires Vercel authentication, handled via the platform's OAuth or token flow.

## 5. Context7 MCP Server (`context7`)
*   **Description:** Interface for Upstash Context7.
*   **Purpose:** Likely used for retrieving context-aware documentation or knowledge base information.
*   **Installation/Execution:**
    ```bash
    npx -y @upstash/context7-mcp@latest --api-key YOUR_CONTEXT7_API_KEY
    ```
*   **Authentication:** Requires a Context7 API Key passed as an argument (`--api-key`). Replace `YOUR_CONTEXT7_API_KEY` with your actual key.

## 6. Sequential Thinking MCP Server (`sequential-thinking`)
*   **Description:** A utility server for structured problem-solving.
*   **Purpose:** Allows the agent to break down complex problems into sequential thought steps to improve reasoning accuracy.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-sequential-thinking
    ```

## 7. Memory MCP Server (`memory`)
*   **Description:** Provides a persistent memory layer.
*   **Purpose:** Enables the agent to store and retrieve information (knowledge graph) across interactions.
*   **Installation/Execution:**
    ```bash
    npx -y @modelcontextprotocol/server-memory
    ```

## 8. Tailwind CSS Server (`tailwindcss-server`)
*   **Description:** Specialized server for Tailwind CSS.
*   **Purpose:** Provides utilities for Tailwind class generation, color palettes, and configuration helpers.
*   **Installation/Execution:**
    ```bash
    tailwindcss-server
    ```
    *(Note: This assumes `tailwindcss-server` is in your system PATH or defined elsewhere in your environment)*

## 9. Next.js DevTools MCP (`next-devtools`)
*   **Description:** Development tools for Next.js applications.
*   **Purpose:** Assists with debugging, analyzing, and optimizing Next.js projects.
*   **Installation/Execution:**
    ```bash
    npx -y next-devtools-mcp@latest
    ```