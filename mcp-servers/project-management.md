# Project Management

Diese MCP-Server bieten Integrationen mit Projektmanagement- und Produktivitätstools, um Aufgaben, Projekte und Workflows zu verwalten.

## Verfügbare Server
- [sooperset/mcp-atlassian](https://github.com/sooperset/mcp-atlassian) 📇 ☁️ - Model Context Protocol (MCP) server for Atlassian products (Confluence and Jira). This integration supports both Confluence & Jira Cloud and Server/Data Center deployments.

<details><summary>Click to expand..</summary>

```shell
docker pull ghcr.io/sooperset/mcp-atlassian:latest
```

```json
{
  "mcpServers": {
    "mcp-atlassian": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e", "CONFLUENCE_URL",
        "-e", "CONFLUENCE_USERNAME",
        "-e", "CONFLUENCE_API_TOKEN",
        "-e", "JIRA_URL",
        "-e", "JIRA_USERNAME",
        "-e", "JIRA_API_TOKEN",
        "ghcr.io/sooperset/mcp-atlassian:latest"
      ],
      "env": {
        "CONFLUENCE_URL": "https://your-company.atlassian.net/wiki",
        "CONFLUENCE_USERNAME": "your.email@company.com",
        "CONFLUENCE_API_TOKEN": "your_confluence_api_token", // https://id.atlassian.com/manage-profile/security/api-tokens
        "JIRA_URL": "https://your-company.atlassian.net",
        "JIRA_USERNAME": "your.email@company.com",
        "JIRA_API_TOKEN": "your_jira_api_token" // https://id.atlassian.com/manage-profile/security/api-tokens
      }
    }
  }
}
```
- https://id.atlassian.com/manage-profile/security/api-tokens

</details>

<br><br>


- [asana/mcp-server-asana](https://github.com/asana/mcp-server-asana) 📇 ☁️ - Asana integration for project and task management
- [trello/mcp-server-trello](https://github.com/trello/mcp-server-trello) 🐍 ☁️ - Trello integration for board and card management
- [jira/mcp-server-jira](https://github.com/jira/mcp-server-jira) 📇 ☁️ - Jira integration for issue tracking and project management
- [monday/mcp-server-monday](https://github.com/monday/mcp-server-monday) 📇 ☁️ - Monday.com integration for work management and collaboration
- [clickup/mcp-server-clickup](https://github.com/clickup/mcp-server-clickup) 🐍 ☁️ - ClickUp integration for productivity and project management
- [toggl/mcp-server-toggl](https://github.com/toggl/mcp-server-toggl) 📇 ☁️ - Toggl integration for time tracking and productivity analysis
- [its-dart/dart-mcp-server](https://github.com/its-dart/dart-mcp-server) 📇 ☁️ - Interact with task, doc, and project data in [Dart](https://itsdart.com), an AI-native project management tool
- [Fibery-inc/fibery-mcp-server](https://github.com/Fibery-inc/fibery-mcp-server) 📇 ☁️ - Perform queries and entity operations in your [Fibery](https://fibery.io) workspace 
