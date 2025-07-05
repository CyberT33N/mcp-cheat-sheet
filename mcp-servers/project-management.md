# Project Management

Diese MCP-Server bieten Integrationen mit Projektmanagement- und Produktivitätstools, um Aufgaben, Projekte und Workflows zu verwalten.

## Verfügbare Server

### mcp-atlassian
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

- <img src="https://github.com/sengokudaikon.png?size=120" width="12px" height="12px" /> **[Aider MCP Server](https://github.com/sengokudaikon/aider-mcp-server)** - Connects AI assistants to file editing capabilities for efficient project management, enabling users to edit, create, and manage files with integrated git status checks.

- <img src="https://github.com/shaileshahuja.png?size=120" width="12px" height="12px" /> **[GitHub PR Comments Server](https://github.com/shaileshahuja/github-pr-mcp)** - Fetches comments from GitHub Pull Requests, including details about file paths and replies, utilizing the GitHub API for structured data access.

- <img src="https://github.com/shanksxz.png?size=120" width="12px" height="12px" /> **[GitHub Repository Context](https://github.com/shanksxz/gh-mcp-server)** - Fetch and utilize contents from GitHub repositories to provide context for AI interactions. Enables access to file contents, repository structures, and allows for filtering and exclusion of specific paths.

- <img src="https://github.com/Sheshiyer.png?size=120" width="12px" height="12px" /> **[Git MCP Server](https://github.com/Sheshiyer/git-mcp-v2)** - Provides enhanced Git operations through a standardized interface for AI assistants, enabling efficient management of repositories, branches, tags, and remote interactions.

- <img src="https://github.com/Shougakusei.png?size=120" width="12px" height="12px" /> **[AI Pull Request Generator](https://github.com/Shougakusei/plan_pr_mcp)** - Automates the creation of pull requests and code generation by leveraging AI for task planning and code synthesis. Integrates seamlessly with GitHub to enhance development workflows through AI-driven productivity enhancements.

- <img src="https://github.com/SiddheshDongare.png?size=120" width="12px" height="12px" /> **[GIT-Pilot](https://github.com/SiddheshDongare/GIT-Pilot)** - Automate GitHub repository management, issue tracking, and pull request handling through a comprehensive API wrapper. It includes features for secure authentication, rate limit management, and error handling.

- <img src="https://github.com/SimonB97.png?size=120" width="12px" height="12px" /> **[Windows CLI Server](https://github.com/SimonB97/win-cli-mcp-server)** - Enables secure command-line interactions on Windows systems with controlled access to PowerShell, CMD, Git Bash, and remote systems using SSH.

- <img src="https://github.com/skurekjakub.png?size=120" width="12px" height="12px" /> **[Git Stuff Server](https://github.com/skurekjakub/GitStuffServer)** - Generate Git merge diffs by providing a merge commit hash and executing Git commands via a PowerShell script. Retrieve detailed diff content seamlessly through an MCP interface.

- <img src="https://github.com/sourcebot-dev.png?size=120" width="12px" height="12px" /> **[Sourcebot Code Search Server](https://github.com/sourcebot-dev/sourcebot)** - Enables regex-based code search across multiple code hosts such as GitHub, GitLab, and BitBucket to retrieve relevant code snippets and repository information. Provides LLM agents with enhanced context for improved reasoning and response quality without requiring local repository checkouts.

- <img src="https://github.com/suenot.png?size=120" width="12px" height="12px" /> **[AI Commit Message Generator](https://github.com/suenot/aicommit-mcp)** - Generate AI-driven git commit messages based on repository changes to enhance version control workflows, with capabilities for executing commit operations and checking git status.

- <img src="https://github.com/Sunwood-ai-labs.png?size=120" width="12px" height="12px" /> **[Aira MCP Server](https://github.com/Sunwood-ai-labs/aira-mcp-server)** - Creates commit messages from git staged files, retrieves git status information, and manages Gitflow operations.

- <img src="https://github.com/Sunwood-ai-labs.png?size=120" width="12px" height="12px" /> **[GitHub Kanban Server](https://github.com/Sunwood-ai-labs/github-kanban-mcp-server)** - Manage GitHub issues in a Kanban board format for streamlined task oversight and enhanced collaboration. Automate workflows and visualize project progress using large language models (LLMs).

- <img src="https://github.com/Sunwood-ai-labs.png?size=120" width="12px" height="12px" /> **[Iris MCP Server](https://github.com/Sunwood-ai-labs/release-notes-generator-iris-mcp-server)** - Automatically generates structured release notes by detecting differences between Git repository tags and saves the output in Markdown format. Provides customizable templates for categorizing new features, improvements, and bug fixes to enhance the release documentation process.

- <img src="https://github.com/Sunwood-ai-labs.png?size=120" width="12px" height="12px" /> **[GitLab Kanban Server](https://github.com/Sunwood-ai-labs/gitlab-kanban-mcp-server)** - Manage GitLab Kanban boards by creating, updating, and deleting tasks through a standardized protocol, enabling efficient project management and seamless integration with applications.

- <img src="https://github.com/tay3223.png?size=120" width="12px" height="12px" /> **[mcp-server-gitlab](https://github.com/tay3223/mcp-server-gitlab)** - Connects to private GitLab instances and provides an API layer for accessing projects, files, commits, and merge requests, thereby streamlining development workflows.

- <img src="https://github.com/taylor-lindores-reeves.png?size=120" width="12px" height="12px" /> **[MCP GitHub Projects](https://github.com/taylor-lindores-reeves/mcp-github-projects)** - Connect and manage Agile Sprint-based projects using GitHub Projects, integrating with GitHub's GraphQL Projects v2 API to create and manage related tasks and issues. Streamline workflows by automating interactions with GitHub repositories and ensuring type safety through TypeScript implementation.

- <img src="https://github.com/timbuchinger.png?size=120" width="12px" height="12px" /> **[GitHub MCP Server](https://github.com/timbuchinger/mcp-github)** - Interact with GitHub repositories and manage issues by listing and creating them efficiently. Provides secure authentication and includes error handling and validation features.

- <img src="https://github.com/tuanle96.png?size=120" width="12px" height="12px" /> **[GitHub API MCP Server](https://github.com/tuanle96/mcp-github)** - Interact with GitHub repositories to manage files, issues, and pull requests while preserving Git history. Perform batch operations and utilize advanced search features for efficient project management.

- <img src="https://github.com/twolven.png?size=120" width="12px" height="12px" /> **[CodeSavant](https://github.com/twolven/mcp-codesavant)** - CodeSavant enables code manipulation and execution across various programming languages while maintaining version control and change history. It supports reading, writing, executing code, and searching within code files.

- <img src="https://github.com/ualUsham.png?size=120" width="12px" height="12px" /> **[GitHub Integration Server](https://github.com/ualUsham/mcp-github)** - Interact with GitHub repositories, manage issues, and automate workflows using GitHub's API. Enhance API responses and streamline interactions between LLMs and GitHub features.

- <img src="https://github.com/vipink1203.png?size=120" width="12px" height="12px" /> **[GitHub Enterprise License Insights](https://github.com/vipink1203/mcp-github-enterprise)** - Securely access GitHub Enterprise license data and user details for automated monitoring and analysis. Query license summaries, user roles, and organization memberships via designated endpoints.

- <img src="https://github.com/null.png?size=120" width="12px" height="12px" /> **[GitHub Repository Explorer](https://github.com/vinhphamai23/mcp-git-ingest)** - Provide tools to programmatically explore and read GitHub repository structures and important files. Generate directory trees and fetch file contents to help users understand repository layouts and codebases efficiently. Enable seamless integration with MCP clients for repository analysis workflows.

- <img src="https://github.com/wonnyboi.png?size=120" width="12px" height="12px" /> **[SSAFY Project Summary](https://github.com/wonnyboi/mcp-server)** - Automates the collection of project information from GitHub for students, assisting in resume writing, interview question generation, and portfolio management. Provides tools for project-based self-introduction and interview practice to streamline career preparation.

- <img src="https://github.com/x51xxx.png?size=120" width="12px" height="12px" /> **[GitHub Explorer](https://github.com/x51xxx/github-explorer-mcp)** - Access GitHub repository information, including file content and directory structure, while enhancing projects with metadata such as stars and forks. Clone repositories locally for efficient data processing and utilize a caching system to optimize performance.

- <img src="https://github.com/xiaoshishu911.png?size=120" width="12px" height="12px" /> **[Introduction to GitHub](https://github.com/xiaoshishu911/skills-introduction-to-github)** - Facilitates learning GitHub basics, including branch creation and repository management. Supports collaboration on projects through guided steps and documentation.

- <img src="https://github.com/Yash-Kavaiya.png?size=120" width="12px" height="12px" /> **[GitHub MCP Server](https://github.com/Yash-Kavaiya/github-mcp-server)** - Integrate directly with GitHub APIs to automate workflows, extract repository data, and create AI-powered tools for interaction within the GitHub ecosystem.

- <img src="https://github.com/yeakub108.png?size=120" width="12px" height="12px" /> **[AI Development Assistant](https://github.com/yeakub108/mcp-server)** - Provides intelligent coding assistance by generating code plans, conducting code reviews, and analyzing UI designs. Offers functionalities such as single and multi-file reading for efficient data processing.

- <img src="https://github.com/yjiace.png?size=120" width="12px" height="12px" /> **[Yunxiao DevOps Server](https://github.com/yjiace/alibabacloud-devops-mcp-server)** - Facilitates interaction with the Yunxiao platform for tasks such as code repository management, file operations, code reviews, and project management. Automates workflow processes to enhance team productivity and reduce repetitive tasks in software development environments.

- <img src="https://github.com/yoda-digital.png?size=120" width="12px" height="12px" /> **[GitLab MCP Server](https://github.com/yoda-digital/mcp-gitlab-server)** - Interact seamlessly with GitLab to manage repositories, track activities, and automate workflows. Tools are available for creating issues, merge requests, and monitoring project events.

- <img src="https://github.com/ZephyrDeng.png?size=120" width="12px" height="12px" /> **[GitLab Integration Server](https://github.com/ZephyrDeng/mcp-server-gitlab)** - Integrate with GitLab to manage projects, tasks, and merge requests while automating interactions using GitLab's RESTful APIs.

- <img src="https://github.com/zereight.png?size=120" width="12px" height="12px" /> **[GitLab communication server](https://github.com/zereight/gitlab-mcp)** - Integrate with the GitLab API to access repositories, manage issues, and perform various actions seamlessly through a standardized protocol. This server offers enhancements and bug fixes over the original GitLab MCP server.

- <img src="https://github.com/zxfgds.png?size=120" width="12px" height="12px" /> **[Toolkit](https://github.com/zxfgds/mcp-toolkit)** - Interact with local systems, databases, and external services through file operations, database management, and GitHub integration. Perform secure and efficient commands and transactions to enhance AI applications with real-world capabilities.

- <img src="https://github.com/a-bonus.png?size=120" width="12px" height="12px" /> **[Google Docs Server](https://github.com/a-bonus/google-docs-mcp)** - Connect to Google Docs for reading and appending text to documents programmatically, enabling automated workflows and document interaction through AI assistants.
- <img src="https://github.com/aallsbury.png?size=120" width="12px" height="12px" /> **[QuickBooks Time MCP Server](https://github.com/aallsbury/qb-time-mcp-server)** - Access all QuickBooks Time API functionalities through a single interface, enabling management of job codes, reports, timesheets, and user tools.
- <img src="https://github.com/aaronsb.png?size=120" width="12px" height="12px" /> **[Targetprocess MCP Server](https://github.com/aaronsb/apptio-target-process-mcp)** - Manage project entities in Targetprocess, including querying, creating, and updating user stories and bugs through natural language interaction. Generate custom reports and insights without switching to the Targetprocess user interface.
- <img src="https://github.com/aaronsb.png?size=120" width="12px" height="12px" /> **[Google Workspace MCP Server](https://github.com/aaronsb/google-workspace-mcp)** - Integrate with Google Workspace APIs to manage emails and calendar events. Automate email sorting, filtering, and response tracking for enhanced productivity.
- <img src="https://github.com/aaronsb.png?size=120" width="12px" height="12px" /> **[Confluence Cloud](https://github.com/aaronsb/confluence-cloud-mcp)** - Interact with Confluence Cloud to manage spaces, pages, and content, including page creation, updates, and search functionalities.
- <img src="https://github.com/aaronsb.png?size=120" width="12px" height="12px" /> **[Jira Insights](https://github.com/aaronsb/jira-insights-mcp)** - Manage Jira Insights asset schemas by creating, reading, updating, and deleting object schemas and types. Query objects using AQL for enhanced data insights and streamlined Jira management.
- <img src="https://github.com/abhiz123.png?size=120" width="12px" height="12px" /> **[Todoist MCP Server](https://github.com/abhiz123/todoist-mcp-server)** - Integrate with the Todoist API for natural language task management, allowing users to create, update, complete, and delete tasks as well as search and filter tasks based on various criteria.
- <img src="https://github.com/adrian-dotco.png?size=120" width="12px" height="12px" /> **[Harvest Natural Language Time Entry Server](https://github.com/adrian-dotco/harvest-mcp-server)** - Log time entries in Harvest using natural language inputs, with specific features for handling leave requests. It supports configurable work hours, timezone adjustments, and smart parsing of dates and projects.
- <img src="https://github.com/adiletD.png?size=120" width="12px" height="12px" /> **[Supabase MCP Server](https://github.com/adiletD/feature-request-collection-mcp)** - Connect to Supabase to efficiently query and manage feature suggestions. Retrieve user feedback and feature requests directly from a Supabase database in real-time.
- <img src="https://github.com/aech-ai.png?size=120" width="12px" height="12px" /> **[Teams Messenger Integration Server](https://github.com/aech-ai/mcp-teams-test)** - Integrates Microsoft Teams chat and messaging with MCP-compatible clients, offering advanced search, persistent storage, and live event streaming. Utilizes PostgreSQL and DuckDB for efficient message retrieval and management, while providing a CLI client for local testing and token management.
- <img src="https://github.com/agentmail-to.png?size=120" width="12px" height="12px" /> **[AgentMail MCP Server](https://github.com/agentmail-to/agentmail-mcp)** - Integrate with the AgentMail API to manage email functionalities effectively and improve communication processes within applications.
- <img src="https://github.com/agentmail-to.png?size=120" width="12px" height="12px" /> **[AgentMail Toolkit](https://github.com/agentmail-to/agentmail-toolkit)** - Integrate email functionality to dynamically manage inboxes, list messages, and send or reply to emails through an AI assistant. This server utilizes the AgentMail API for efficient email automation and management.
- <img src="https://github.com/ahmad2x4.png?size=120" width="12px" height="12px" /> **[Seq MCP Server](https://github.com/ahmad2x4/mcp-server-seq)** - Interact with Seq's logging and monitoring system via its API endpoints, providing access to various features for managing signals and events.
- <img src="https://github.com/ahonn.png?size=120" width="12px" height="12px" /> **[Google Search Console](https://github.com/ahonn/mcp-server-gsc)** - Provides access to Google Search Console, enabling retrieval of search analytics data along with customizable reporting periods for rich data analysis.
- <img src="https://github.com/alexeydubinin.png?size=120" width="12px" height="12px" /> **[hh-jira-mcp-server](https://github.com/alexeydubinin/hh-jira-mcp-server)** - Connects to Jira for real-time data access and manipulation, enhancing project management through integration of tasks into applications.
- <img src="https://github.com/alexarevalo9.png?size=120" width="12px" height="12px" /> **[TickTick API Server](https://github.com/alexarevalo9/ticktick-mcp-server)** - Manage tasks, projects, and habits with the TickTick API, providing capabilities for task creation, updates, and tracking along with secure OAuth authentication. Supports full control over task properties including priorities, deadlines, and subtasks.
- <img src="https://github.com/AliNagy.png?size=120" width="12px" height="12px" /> **[Godspeed Task Management Connector](https://github.com/AliNagy/godspeed-mcp)** - Manage tasks efficiently using the Godspeed Task Management API. Create, update, and organize tasks seamlessly within applications.
- <img src="https://github.com/alvinjchoi.png?size=120" width="12px" height="12px" /> **[Google Tasks MCP](https://github.com/alvinjchoi/gtasks-mcp)** - Integrate with Google Tasks to manage tasks through natural language commands, supporting task creation, updates, deletions, and organization across multiple lists. Query tasks easily and automate completion marking, enhancing productivity workflows.
- <img src="https://github.com/andypost.png?size=120" width="12px" height="12px" /> **[Trello MCP Server](https://github.com/andypost/mcp-server-ts-trello)** - Integrate with Trello to manage boards, lists, and cards through the Model Context Protocol. Provides tools for AI assistants to perform asynchronous operations and manage Trello data using a TypeScript implementation.
- <img src="https://github.com/ayasahmad.png?size=120" width="12px" height="12px" /> **[Jira Context Server](https://github.com/ayasahmad/Jira-Context-MCP)** - Integrate with Jira to access issue details, manage assigned tickets, filter issues by type, and track changes within development environments. Automate workflows and streamline issue resolution with direct access to Jira's API.
- <img src="https://github.com/ayasahmad.png?size=120" width="12px" height="12px" /> **[Jira Context Server](https://github.com/ayasahmad/Jira-Context-MCP)** - Integrate with Jira to fetch issue details, list assigned tickets, filter issues by type, and track recent changes. Facilitate automation of Jira workflows and enhance productivity within development environments.
- <img src="https://github.com/brianstone.png?size=120" width="12px" height="12px" /> **[Jira Integration Server](https://github.com/brianstone/jira-mcp-server)** - Manage Jira issues through the MCP protocol, including creating, searching, assigning, unassigning, and editing issues to enhance project management workflows.
- <img src="https://github.com/Buga-luga.png?size=120" width="12px" height="12px" /> **[Cursor](https://github.com/Buga-luga/cursor-mcp)** - Integrate AI capabilities within desktop applications through the Cursor IDE, facilitating enhanced code editing and development workflows with Claude AI. This MCP implementation acts as a bridge to streamline interaction between AI models and desktop software.
- <img src="https://github.com/cablate.png?size=120" width="12px" height="12px" /> **[Calendar Tools](https://github.com/cablate/mcp-google-calendar)** - Manage calendar events by creating, listing, updating, and deleting them efficiently.
