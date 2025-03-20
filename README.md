# mcp-cheat-sheet


# Guides

## General
- https://www.youtube.com/watch?v=kj4eK9ylGDk





























<br><br>
________
________
<br><br>





# Model Control Protocol (MCP) – Eine Einführung

<details><summary>Click to expand..</summary>

## Was ist MCP?  
**MCP (Model Control Protocol)** ist ein **offenes Protokoll**, das es **KI-Modellen** ermöglicht, sicher mit lokalen und entfernten Ressourcen zu kommunizieren. Es bietet eine **standardisierte Schnittstelle**, um den Zugriff auf Dateien, Datenbanken, APIs und andere Dienste zu erleichtern.  

Ohne MCP arbeiten viele KI-Modelle isoliert – MCP ermöglicht eine **dynamische Integration** in reale Systeme.  

---

## Warum MCP?  
### Vorteile:
- **Erweiterbarkeit** → KI-Modelle können auf externe Datenquellen zugreifen.  
- **Standardisierung** → Einheitliches Protokoll für verschiedene Anwendungen.  
- **Sicherheit** → Kontrollierter Zugriff auf lokale und entfernte Ressourcen.  
- **Flexibilität** → Unterstützt viele Anwendungsfälle, von Dateioperationen bis zu API-Abfragen.  

---

## Komponenten von MCP  

### 1. **MCP-Server**  
Ein MCP-Server verwaltet und vermittelt Anfragen zwischen **KI-Modellen und Ressourcen**. Er bietet folgende Funktionen:  

✅ **Dateizugriff** – Lesen/Schreiben von lokalen und Cloud-Dateien.  
✅ **Datenbankverbindungen** – Abfragen an SQL/NoSQL-Datenbanken.  
✅ **API-Integrationen** – Zugriff auf Web-Dienste (z. B. Wetter, Finanzen).  
✅ **System-Interaktion** – Steuert Prozesse oder führt Befehle aus.  

Beispiel für einen MCP-Server:  
```json
{
  "request": "fetch_data",
  "source": "database",
  "query": "SELECT * FROM users"
}
```

---

### 2. **MCP-Client**  
Der Client ist eine **KI-Anwendung oder ein Modell**, das über MCP mit einem Server kommuniziert.  

🔹 **Fragt Daten an** – Sendet Anfragen an den MCP-Server.  
🔹 **Erhält Antworten** – Nutzt die erhaltenen Daten zur Weiterverarbeitung.  

Beispiel einer Client-Anfrage an einen MCP-Server:  
```json
{
  "command": "read_file",
  "file_path": "/data/user_info.json"
}
```

Und die Antwort des MCP-Servers könnte sein:  
```json
{
  "status": "success",
  "data": {
    "users": [
      { "id": 1, "name": "Alice" },
      { "id": 2, "name": "Bob" }
    ]
  }
}
```

---

## MCP in der Praxis  
### 🛠 **Anwendungsfälle:**
- **KI-Agenten mit Dateisystemzugriff** (z. B. für Dokumentenanalyse).  
- **Dynamische Web-APIs für KI** (Chatbots mit aktuellen Informationen).  
- **Verbindung zu Firmendatenbanken** (z. B. für interne Business-Analysen).  
- **Automatisierte Workflows** (KI-Modell kann Skripte oder Prozesse starten).  

### 🔥 **Bekannte MCP-Server-Implementierungen:**  
- **Langchain MCP** → KI-Agenten mit externem Wissen.  
- **OpenAI Function Calling MCP** → Sicheres API-Handling.  

---

## Fazit  
**MCP ist der Schlüssel zur nahtlosen Integration von KI-Modellen in reale Systeme.**  
Es macht KI nicht nur intelligenter, sondern auch **nützlicher** in produktiven Umgebungen. 🚀  


</details>













































<br><br>
________
________
<br><br>


# MCP Host

## n8n



## Claude Desktop



































<br><br>
<br><br>
___
<br><br>
<br><br>

# MCP Servers




<details><summary>Click to expand..</summary>

# List
- https://glama.ai/mcp/servers
- https://github.com/punkpeye/awesome-mcp-servers

We now have a [web-based directory](https://glama.ai/mcp/servers) that is synced with the repository.

* 📂 - [Browser Automation](#browser-automation)
* 🎨 - [Art & Culture](#art-and-culture)
* ☁️ - [Cloud Platforms](#cloud-platforms)
* 🖥️ - [Command Line](#command-line)
* 💬 - [Communication](#communication)
* 👤 - [Customer Data Platforms](#customer-data-platforms)
* 🗄️ - [Databases](#databases)
* 🛠️ - [Developer Tools](#developer-tools)
* 📂 - [File Systems](#file-systems)
* 💰 - [Finance & Fintech](#finance--fintech)
* 🧠 - [Knowledge & Memory](#knowledge--memory)
* 🗺️ - [Location Services](#location-services)
* 🎯 - [Marketing](#marketing)
* 📊 - [Monitoring](#monitoring)
* 🔎 - [Search](#search)
* 🔒 - [Security](#security)
* 🚆 - [Travel & Transportation](#travel-and-transportation)
* 🔄 - [Version Control](#version-control)
* 🛠️ - [Other Tools and Integrations](#other-tools-and-integrations)




<br><br>




### 📂 <a name="crawling"></a>Website Crawling/Scraping
- https://github.com/mendableai/firecrawl-mcp-server - Official Firecrawl MCP Server - Adds powerful web scraping to Cursor, Claude and any other LLM clients. 


<br><br>


### 📂 <a name="browser-automation"></a>Browser Automation

Web content access and automation capabilities. Enables searching, scraping, and processing web content in AI-friendly formats.
- [@blackwhite084/playwright-plus-python-mcp](https://github.com/blackwhite084/playwright-plus-python-mcp) 🌐 - An MCP python server using Playwright for browser automation,more suitable for llm
- [@executeautomation/playwright-mcp-server](https://github.com/executeautomation/mcp-playwright) 🌐⚡️ - An MCP server using Playwright for browser automation and webscrapping
- [@automatalabs/mcp-server-playwright](https://github.com/Automata-Labs-team/MCP-Server-Playwright) 🌐 🖱️ - An MCP server for browser automation using Playwright
- [@modelcontextprotocol/server-puppeteer](https://github.com/modelcontextprotocol/servers/tree/main/src/puppeteer) 📇 🏠 - Browser automation for web scraping and interaction
- [@kimtaeyoon83/mcp-server-youtube-transcript](https://github.com/kimtaeyoon83/mcp-server-youtube-transcript) 📇 ☁️ - Fetch YouTube subtitles and transcripts for AI analysis
- [@recursechat/mcp-server-apple-shortcuts](https://github.com/recursechat/mcp-server-apple-shortcuts) 📇 🏠 🍎 - An MCP Server Integration with Apple Shortcuts
- [@kimtth/mcp-aoai-web-browsing](https://github.com/kimtth/mcp-aoai-web-browsing) 🐍 🏠 - A `minimal` server/client MCP implementation using Azure OpenAI and Playwright.
- [@pskill9/web-search](https://github.com/pskill9/web-search) 📇 🏠 - An MCP server that enables free web searching using Google search results, with no API keys required.

### 🎨 <a name="art-and-culture"></a>Art & Culture

Access and explore art collections, cultural heritage, and museum databases. Enables AI models to search and analyze artistic and cultural content.

- [burningion/video-editing-mcp](https://github.com/burningion/video-editing-mcp) 📹🎬 - Add, Analyze, Search, and Generate Video Edits from your Video Jungle Collection
- [r-huijts/rijksmuseum-mcp](https://github.com/r-huijts/rijksmuseum-mcp) 📇 ☁️ - Rijksmuseum API integration for artwork search, details, and collections

### ☁️ <a name="cloud-platforms"></a>Cloud Platforms

Cloud platform service integration. Enables management and interaction with cloud infrastructure and services.

- [Cloudflare MCP Server](https://github.com/cloudflare/mcp-server-cloudflare) 🎖️ 📇 ☁️ - Integration with Cloudflare services including Workers, KV, R2, and D1
- [Kubernetes MCP Server](https://github.com/strowk/mcp-k8s-go) - 🏎️ ☁️/🏠 Kubernetes cluster operations through MCP
- [@flux159/mcp-server-kubernetes](https://github.com/Flux159/mcp-server-kubernetes) - 📇 ☁️/🏠 Typescript implementation of Kubernetes cluster operations for pods, deployments, services.
- [@manusa/Kubernetes MCP Server](https://github.com/manusa/kubernetes-mcp-server) - 🏎️ 🏠 A powerful Kubernetes MCP server with additional support for OpenShift. Besides providing CRUD operations for **any** Kubernetes resource, this server provides specialized tools to interact with your cluster.
- [johnneerdael/netskope-mcp](https://github.com/johnneerdael/netskope-mcp) 🔒 ☁️ - An MCP to give access to all Netskope Private Access components within a Netskope Private Access environments including detailed setup information and LLM examples on usage.

### 🖥️ <a name="command-line"></a>Command Line

Run commands, capture output and otherwise interact with shells and command line tools.

- [ferrislucas/iterm-mcp](https://github.com/ferrislucas/iterm-mcp) 🖥️ 🛠️ 💬 - A Model Context Protocol server that provides access to iTerm. You can run commands and ask questions about what you see in the iTerm terminal.
- [g0t4/mcp-server-commands](https://github.com/g0t4/mcp-server-commands) 📇 🏠 - Run any command with `run_command` and `run_script` tools.
- [MladenSU/cli-mcp-server](https://github.com/MladenSU/cli-mcp-server) 🐍 🏠 - Command line interface with secure execution and customizable security policies
- [tumf/mcp-shell-server](https://github.com/tumf/mcp-shell-server) A secure shell command execution server implementing the Model Context Protocol (MCP)

### 💬 <a name="communication"></a>Communication

Integration with communication platforms for message management and channel operations. Enables AI models to interact with team communication tools.

- [zcaceres/gtasks-mcp](https://github.com/zcaceres/gtasks-mcp) - 📇 ☁️ - An MCP server to Manage Google Tasks
- [hannesrudolph/imessage-query-fastmcp-mcp-server](https://github.com/hannesrudolph/imessage-query-fastmcp-mcp-server) 🐍 🏠 🍎 - An MCP server that provides safe access to your iMessage database through Model Context Protocol (MCP), enabling LLMs to query and analyze iMessage conversations with proper phone number validation and attachment handling
- [@modelcontextprotocol/server-slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) 📇 ☁️ - Slack workspace integration for channel management and messaging
- [@modelcontextprotocol/server-bluesky](https://github.com/keturiosakys/bluesky-context-server) 📇 ☁️ - Bluesky instance integration for querying and interaction
- [MarkusPfundstein/mcp-gsuite](https://github.com/MarkusPfundstein/mcp-gsuite) - 🐍 ☁️ - Integration with gmail and Google Calendar.
- [adhikasp/mcp-twikit](https://github.com/adhikasp/mcp-twikit) 🐍 ☁️ - Interact with Twitter search and timeline
- [gotoolkits/wecombot](https://github.com/gotoolkits/mcp-wecombot-server.git) - 🚀 ☁️  - An MCP server application that sends various types of messages to the WeCom group robot.
- [AbdelStark/nostr-mcp](https://github.com/AbdelStark/nostr-mcp) - 🌐 ☁️ - A Nostr MCP server that allows to interact with Nostr, enabling posting notes, and more.

### 👤 <a name="customer-data-platforms"></a>Customer Data Platforms

Provides access to customer profiles inside of customer data platforms

- [sergehuber/inoyu-mcp-unomi-server](https://github.com/sergehuber/inoyu-mcp-unomi-server) 📇 ☁️ - An MCP server to access and updates profiles on an Apache Unomi CDP server.
- [OpenDataMCP/OpenDataMCP](https://github.com/OpenDataMCP/OpenDataMCP) 🐍 ☁️ - Connect any Open Data to any LLM with Model Context Protocol.
- [tinybirdco/mcp-tinybird](https://github.com/tinybirdco/mcp-tinybird) 🐍 ☁️ - An MCP server to interact with a Tinybird Workspace from any MCP client.
- [@iaptic/mcp-server-iaptic](https://github.com/iaptic/mcp-server-iaptic) 🎖️ 📇 ☁️ - Connect with [iaptic](https://www.iaptic.com) to ask about your Customer Purchases, Transaction data and App Revenue statistics.

### 🗄️ <a name="databases"></a>Databases

Secure database access with schema inspection capabilities. Enables querying and analyzing data with configurable security controls including read-only access.

- [cr7258/elasticsearch-mcp-server](https://github.com/cr7258/elasticsearch-mcp-server) 🐍 🏠 - MCP Server implementation that provides Elasticsearch interaction
- [domdomegg/airtable-mcp-server](https://github.com/domdomegg/airtable-mcp-server) 📇 🏠 - Airtable database integration with schema inspection, read and write capabilities
- [LucasHild/mcp-server-bigquery](https://github.com/LucasHild/mcp-server-bigquery) 🐍 ☁️ - BigQuery database integration with schema inspection and query capabilities
- [ergut/mcp-bigquery-server](https://github.com/ergut/mcp-bigquery-server) 📇 ☁️ - Server implementation for Google BigQuery integration that enables direct BigQuery database access and querying capabilities
- [ClickHouse/mcp-clickhouse](https://github.com/ClickHouse/mcp-clickhouse) 🐍 ☁️ - ClickHouse database integration with schema inspection and query capabilities
- [@gannonh/firebase-mcp](https://github.com/gannonh/firebase-mcp) 🔥 ⛅️ - Firebase services including Auth, Firestore and Storage.
- [jovezhong/mcp-timeplus](https://github.com/jovezhong/mcp-timeplus) 🐍 ☁️ - MCP server for Apache Kafka and Timeplus. Able to list Kafka topics, poll Kafka messages, save Kafka data locally and query streaming data with SQL via Timeplus
- [@fireproof-storage/mcp-database-server](https://github.com/fireproof-storage/mcp-database-server) 📇 ☁️ - Fireproof ledger database with multi-user sync
- [designcomputer/mysql_mcp_server](https://github.com/designcomputer/mysql_mcp_server) 🐍 🏠 - MySQL database integration with configurable access controls, schema inspection, and comprehensive security guidelines
- [f4ww4z/mcp-mysql-server](https://github.com/f4ww4z/mcp-mysql-server) 🐍 🏠 - Node.js-based MySQL database integration that provides secure MySQL database operations
- [@modelcontextprotocol/server-postgres](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) 📇 🏠 - PostgreSQL database integration with schema inspection and query capabilities
- [@modelcontextprotocol/server-sqlite](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) 🐍 🏠 - SQLite database operations with built-in analysis features
- [@joshuarileydev/supabase-mcp-server](https://github.com/joshuarileydev/supabase) - Supabase MCP Server for managing and creating projects and organisations in Supabase
- [@alexanderzuev/supabase-mcp-server](https://github.com/alexander-zuev/supabase-mcp-server) - Supabase MCP Server with support for SQL query execution and database exploration tools
- [ktanaka101/mcp-server-duckdb](https://github.com/ktanaka101/mcp-server-duckdb) 🐍 🏠 - DuckDB database integration with schema inspection and query capabilities
- [QuantGeekDev/mongo-mcp](https://github.com/QuantGeekDev/mongo-mcp) 📇 🏠 - MongoDB integration that enables LLMs to interact directly with databases.
- [tinybirdco/mcp-tinybird](https://github.com/tinybirdco/mcp-tinybird) 🐍 ☁️ - Tinybird integration with query and API capabilities
- [kiliczsh/mcp-mongo-server](https://github.com/kiliczsh/mcp-mongo-server) 📇 🏠 - A Model Context Protocol Server for MongoDB
- [KashiwaByte/vikingdb-mcp-server](https://github.com/KashiwaByte/vikingdb-mcp-server) 🐍 ☁️ - VikingDB integration with collection and index introduction, vector store and search capabilities.
- [neo4j-contrib/mcp-neo4j](https://github.com/neo4j-contrib/mcp-neo4j) 🐍 🏠 - Model Context Protocol with Neo4j
- [isaacwasserman/mcp-snowflake-server](https://github.com/isaacwasserman/mcp-snowflake-server) 🐍 ☁️ - Snowflake integration implementing read and (optional) write operations as well as insight tracking
- [hannesrudolph/sqlite-explorer-fastmcp-mcp-server](https://github.com/hannesrudolph/sqlite-explorer-fastmcp-mcp-server) 🐍 🏠 - An MCP server that provides safe, read-only access to SQLite databases through Model Context Protocol (MCP). This server is built with the FastMCP framework, which enables LLMs to explore and query SQLite databases with built-in safety features and query validation.
- [sirmews/mcp-pinecone](https://github.com/sirmews/mcp-pinecone) 🐍 ☁️ - Pinecone integration with vector search capabilities
- [runekaagaard/mcp-alchemy](https://github.com/runekaagaard/mcp-alchemy) 🐍 🏠 - Universal SQLAlchemy-based database integration supporting PostgreSQL, MySQL, MariaDB, SQLite, Oracle, MS SQL Server and many more databases. Features schema and relationship inspection, and large dataset analysis capabilities.
- [neondatabase/mcp-server-neon](https://github.com/neondatabase/mcp-server-neon) 📇 ☁️ — An MCP Server for creating and managing Postgres databases using Neon Serverless Postgres

### 💻 <a name="developer-tools"></a>Developer Tools

Tools and integrations that enhance the development workflow and environment management.

- [GLips/Figma-Context-MCP](https://github.com/GLips/Figma-Context-MCP) 📇 🏠 - Provide coding agents direct access to Figma data to help them one-shot design implementation.
- [QuantGeekDev/docker-mcp](https://github.com/QuantGeekDev/docker-mcp) 🏎️ 🏠 - Docker container management and operations through MCP
- [zcaceres/fetch-mcp](https://github.com/zcaceres/fetch-mcp) 📇 🏠 - An MCP server to flexibly fetch JSON, text, and HTML data
- [r-huijts/xcode-mcp-server](https://github.com/r-huijts/xcode-mcp-server) 📇 🏠 🍎 - Xcode integration for project management, file operations, and build automation
- [snaggle-ai/openapi-mcp-server](https://github.com/snaggle-ai/openapi-mcp-server) 🏎️ 🏠 - Connect any HTTP/REST API server using an Open API spec (v3)
- [jetbrains/mcpProxy](https://github.com/JetBrains/mcpProxy) 🎖️ 📇 🏠 - Connect to JetBrains IDE
- [tumf/mcp-text-editor](https://github.com/tumf/mcp-text-editor) 🐍 🏠 - A line-oriented text file editor. Optimized for LLM tools with efficient partial file access to minimize token usage.
- [@joshuarileydev/simulator-mcp-server](https://github.com/JoshuaRileyDev/simulator-mcp-server) 📇 🏠 - An MCP server to control iOS Simulators
- [@joshuarileydev/app-store-connect-mcp-server](https://github.com/JoshuaRileyDev/app-store-connect-mcp-server) 📇 🏠 - An MCP server to communicate with the App Store Connect API for iOS Developers
- [@sammcj/mcp-package-version](https://github.com/sammcj/mcp-package-version) 📇 🏠 - An MCP Server to help LLMs suggest the latest stable package versions when writing code.
- [@delano/postman-mcp-server](https://github.com/delano/postman-mcp-server) 📇 ☁️ - Interact with [Postman API](https://www.postman.com/postman/postman-public-workspace/)
- [@vivekvells/mcp-pandoc](https://github.com/vivekVells/mcp-pandoc) 🗄️ 🚀 - MCP server for seamless document format conversion using Pandoc, supporting Markdown, HTML, PDF, DOCX (.docx), csv and more.
- [@pskill9/website-downloader](https://github.com/pskill9/website-downloader) 🗄️ 🚀 - This MCP server provides a tool to download entire websites using wget. It preserves the website structure and converts links to work locally.
- [@lamemind/mcp-server-multiverse](https://github.com/lamemind/mcp-server-multiverse) 📇 🏠 🛠️ - A middleware server that enables multiple isolated instances of the same MCP servers to coexist independently with unique namespaces and configurations.
- [@j4c0bs/mcp-server-sql-analyzer](https://github.com/j4c0bs/mcp-server-sql-analyzer) 🐍 - MCP server that provides SQL analysis, linting, and dialect conversion using [SQLGlot](https://github.com/tobymao/sqlglot)
- [@haris-musa/excel-mcp-server](https://github.com/haris-musa/excel-mcp-server) 🐍 🏠 - An Excel manipulation server providing workbook creation, data operations, formatting, and advanced features (charts, pivot tables, formulae).
- [@jasonjmcghee/claude-debugs-for-you](https://github.com/jasonjmcghee/claude-debugs-for-you) 📇 🏠 - An MCP Server and VS Code Extension which enables (language agnostic) automatic debugging via breakpoints and expression evaluation.

### 🧮 Data Science Tools

Integrations and tools designed to simplify data exploration, analysis and enhance data science workflows.
- [ChronulusAI/chronulus-mcp](https://github.com/ChronulusAI/chronulus-mcp) 🐍 ☁️ - Predict anything with Chronulus AI forecasting and prediction agents.
- [zcaceres/markdownify-mcp](https://github.com/zcaceres/markdownify-mcp) 📇 🏠 - An MCP server to convert almost any file or web content into Markdown
- [@reading-plus-ai/mcp-server-data-exploration](https://github.com/reading-plus-ai/mcp-server-data-exploration) 🐍 ☁️ - Enables autonomous data exploration on .csv-based datasets, providing intelligent insights with minimal effort.

### 📂 <a name="file-systems"></a>File Systems

Provides direct access to local file systems with configurable permissions. Enables AI models to read, write, and manage files within specified directories.

- [@modelcontextprotocol/server-filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) 📇 🏠 - Direct local file system access.
- [@modelcontextprotocol/server-google-drive](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive) 📇 ☁️ - Google Drive integration for listing, reading, and searching files
- [hmk/box-mcp-server](https://github.com/hmk/box-mcp-server) 📇 ☁️ - Box integration for listing, reading and searching files
- [mark3labs/mcp-filesystem-server](https://github.com/mark3labs/mcp-filesystem-server) 🏎️ 🏠 - Golang implementation for local file system access.
- [mamertofabian/mcp-everything-search](https://github.com/mamertofabian/mcp-everything-search) 🐍 🏠 🪟 - Fast Windows file search using Everything SDK
- [cyberchitta/llm-context.py](https://github.com/cyberchitta/llm-context.py) 🐍 🏠 - Share code context with LLMs via MCP or clipboard
- [Xuanwo/mcp-server-opendal](https://github.com/Xuanwo/mcp-server-opendal) 🐍 🏠 ☁️ - Access any storage with Apache OpenDAL™

### 💰 <a name="finance--fintech"></a>Finance & Fintech

Financial data access and cryptocurrency market information. Enables querying real-time market data, crypto prices, and financial analytics.

- [QuantGeekDev/coincap-mcp](https://github.com/QuantGeekDev/coincap-mcp) 📇 ☁️ - Real-time cryptocurrency market data integration using CoinCap's public API, providing access to crypto prices and market information without API keys
- [anjor/coinmarket-mcp-server](https://github.com/anjor/coinmarket-mcp-server) 🐍 ☁️ - Coinmarket API integration to fetch cryptocurrency listings and quotes
- [berlinbra/alpha-vantage-mcp](https://github.com/berlinbra/alpha-vantage-mcp) 🐍 ☁️ - Alpha Vantage API integration to fetch both stock and crypto information
- [ferdousbhai/tasty-agent](https://github.com/ferdousbhai/tasty-agent) 🐍 ☁️ - Tastyworks API integration to handle trading activities on Tastytrade
- [ferdousbhai/investor-agent](https://github.com/ferdousbhai/investor-agent) 🐍 ☁️ - Yahoo Finance integration to fetch stock market data including options recommendations

### 🧠 <a name="knowledge--memory"></a>Knowledge & Memory

Persistent memory storage using knowledge graph structures. Enables AI models to maintain and query structured information across sessions.
- [@modelcontextprotocol/server-memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) 📇 🏠 - Knowledge graph-based persistent memory system for maintaining context
- [/CheMiguel23/MemoryMesh](https://github.com/CheMiguel23/MemoryMesh) 📇 🏠 - Enhanced graph-based memory with a focus on AI role-play and story generation
- [/topoteretes/cognee](https://github.com/topoteretes/cognee/tree/dev/cognee-mcp) 📇 🏠 - Memory manager for AI apps and Agents using various graph and vector stores and allowing ingestion from 30+ data sources
- [@hannesrudolph/mcp-ragdocs](https://github.com/hannesrudolph/mcp-ragdocs) 🐍 🏠 - An MCP server implementation that provides tools for retrieving and processing documentation through vector search, enabling AI assistants to augment their responses with relevant documentation context
- [@kaliaboi/mcp-zotero](https://github.com/kaliaboi/mcp-zotero) 📇 ☁️ - A connector for LLMs to work with collections and sources on your Zotero Cloud
- [mcp-summarizer](https://github.com/0xshellming/mcp-summarizer) 📕 ☁️ - AI Summarization MCP Server, Support for multiple content types: Plain text, Web pages, PDF documents, EPUB books, HTML content

### 🗺️ <a name="location-services"></a>Location Services

Geographic and location-based services integration. Enables access to mapping data, directions, and place information.

- [@modelcontextprotocol/server-google-maps](https://github.com/modelcontextprotocol/servers/tree/main/src/google-maps) 📇 ☁️ - Google Maps integration for location services, routing, and place details
- [SecretiveShell/MCP-timeserver](https://github.com/SecretiveShell/MCP-timeserver) 🐍 🏠 - Access the time in any timezone and get the current local time
- [webcoderz/MCP-Geo](https://github.com/webcoderz/MCP-Geo) 🐍 🏠 - Geocoding MCP server for nominatim, ArcGIS, Bing
- [@briandconnelly/mcp-server-ipinfo](https://github.com/briandconnelly/mcp-server-ipinfo) 🐍 ☁️  - IP address geolocation and network information using IPInfo API

### 🎯 <a name="marketing"></a>Marketing

Tools for creating and editing marketing content, working with web meta data, product positioning, and editing guides.

- [Open Strategy Partners Marketing Tools](https://github.com/open-strategy-partners/osp_marketing_tools) 🐍 🏠 - A suite of marketing tools from Open Strategy Partners including writing style, editing codes, and product marketing value map creation.

### 📊 <a name="monitoring"></a>Monitoring

Access and analyze application monitoring data. Enables AI models to review error reports and performance metrics.

- [@modelcontextprotocol/server-sentry](https://github.com/modelcontextprotocol/servers/tree/main/src/sentry) 🐍 ☁️ - Sentry.io integration for error tracking and performance monitoring
- [@modelcontextprotocol/server-raygun](https://github.com/MindscapeHQ/mcp-server-raygun) 📇 ☁️ - Raygun API V3 integration for crash reporting and real user monitoring
- [metoro-io/metoro-mcp-server](https://github.com/metoro-io/metoro-mcp-server) 🎖️ 🏎️ ☁️ - Query and interact with kubernetes environments monitored by Metoro
- [grafana/mcp-grafana](https://github.com/grafana/mcp-grafana) 🎖️ 🐍 🏠 ☁️ - Search dashboards, investigate incidents and query datasources in your Grafana instance

### 🔎 <a name="search"></a>Search

- [@modelcontextprotocol/server-brave-search](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) 📇 ☁️ - Web search capabilities using Brave's Search API
- [@angheljf/nyt](https://github.com/angheljf/nyt) 📇 ☁️ - Search articles using the NYTimes API
- [@modelcontextprotocol/server-fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) 🐍 🏠 ☁️ - Efficient web content fetching and processing for AI consumption
- [ac3xx/mcp-servers-kagi](https://github.com/ac3xx/mcp-servers-kagi) 📇 ☁️ - Kagi search API integration
- [exa-labs/exa-mcp-server](https://github.com/exa-labs/exa-mcp-server) 🎖️ 📇 ☁️ – A Model Context Protocol (MCP) server lets AI assistants like Claude use the Exa AI Search API for web searches. This setup allows AI models to get real-time web information in a safe and controlled way.
- [fatwang2/search1api-mcp](https://github.com/fatwang2/search1api-mcp) 📇 ☁️ - Search via search1api (requires paid API key)
- [Tomatio13/mcp-server-tavily](https://github.com/Tomatio13/mcp-server-tavily) ☁️ 🐍 – Tavily AI search API
- [kshern/mcp-tavily](https://github.com/kshern/mcp-tavily.git) ☁️ 📇 – Tavily AI search API
- [blazickjp/arxiv-mcp-server](https://github.com/blazickjp/arxiv-mcp-server) ☁️ 🐍 - Search ArXiv research papers
- [mzxrai/mcp-webresearch](https://github.com/mzxrai/mcp-webresearch) 🔍📚 - Search Google and do deep web research on any topic
- [andybrandt/mcp-simple-arxiv](https://github.com/andybrandt/mcp-simple-arxiv) - 🐍 ☁️  MCP for LLM to search and read papers from arXiv
- [andybrandt/mcp-simple-pubmed](https://github.com/andybrandt/mcp-simple-pubmed) - 🐍 ☁️  MCP to search and read medical / life sciences papers from PubMed.
- [apify/mcp-server-rag-web-browser](https://github.com/apify/mcp-server-rag-web-browser) 📇 ☁️ - An MCP server for Apify's open-source RAG Web Browser Actor to perform web searches, scrape URLs, and return content in Markdown.
- [SecretiveShell/MCP-searxng](https://github.com/SecretiveShell/MCP-searxng) 🐍 🏠 - An MCP Server to connect to searXNG instances
- [Bigsy/Clojars-MCP-Server](https://github.com/Bigsy/Clojars-MCP-Server) 📇 ☁️ - Clojars MCP Server for upto date dependency information of Clojure libraries
- [Ihor-Sokoliuk/MCP-SearXNG](https://github.com/ihor-sokoliuk/mcp-searxng) 📇 🏠/☁️ - A Model Context Protocol Server for [SearXNG](https://docs.searxng.org)
- [erithwik/mcp-hn](https://github.com/erithwik/mcp-hn) 🐍 ☁️ - An MCP server to search Hacker News, get top stories, and more.
- [chanmeng/google-news-mcp-server](https://github.com/ChanMeng666/server-google-news) 📇 ☁️ - Google News integration with automatic topic categorization, multi-language support, and comprehensive search capabilities including headlines, stories, and related topics through [SerpAPI](https://serpapi.com/).
- [devflowinc/trieve](https://github.com/devflowinc/trieve/tree/main/clients/mcp-server) 🎖️📇☁️🏠 - Crawl, embed, chunk, search, and retrieve information from datasets through [Trieve](https://trieve.ai)
- [nickclyde/duckduckgo-mcp-server](https://github.com/nickclyde/duckduckgo-mcp-server) 🐍 ☁️ - Web search using DuckDuckGo
- [zhsama/duckduckgo-mcp-server](https://github.com/zhsama/duckduckgo-mpc-server/) 📇 🏠 ☁️ - This is a TypeScript-based MCP server that provides DuckDuckGo search functionality.

### 🔒 <a name="security"></a>Security

- [dnstwist MCP Server](https://github.com/BurtTheCoder/mcp-dnstwist) 📇🪟☁️ - MCP server for dnstwist, a powerful DNS fuzzing tool that helps detect typosquatting, phishing, and corporate espionage.
- [Maigret MCP Server](https://github.com/BurtTheCoder/mcp-maigret) 📇🪟☁️ - MCP server for maigret, a powerful OSINT tool that collects user account information from various public sources. This server provides tools for searching usernames across social networks and analyzing URLs.
- [Shodan MCP Server](https://github.com/BurtTheCoder/mcp-shodan) 📇🪟☁️ - MCP server for querying the Shodan API and Shodan CVEDB. This server provides tools for IP lookups, device searches, DNS lookups, vulnerability queries, CPE lookups, and more.
- [VirusTotal MCP Server](https://github.com/BurtTheCoder/mcp-virustotal) 📇🪟☁️ - MCP server for querying the VirusTotal API. This server provides tools for scanning URLs, analyzing file hashes, and retrieving IP address reports.
- [ORKL MCP Server](https://github.com/fr0gger/MCP_Security) 📇🛡️☁️ - MCP server for querying the ORKL API. This server provides tools for fetching threat reports, analyzing threat actors, and retrieving intelligence sources.
- [Security Audit MCP Server](https://github.com/qianniuspace/mcp-security-audit) 📇🛡️☁️ A powerful MCP (Model Context Protocol) Server that audits npm package dependencies for security vulnerabilities. Built with remote npm registry integration for real-time security checks.

### 🚆 <a name="travel-and-transportation"></a>Travel & Transportation

Access to travel and transportation information. Enables querying schedules, routes, and real-time travel data.

- [NS Travel Information MCP Server](https://github.com/r-huijts/ns-mcp-server) 📇 ☁️ - Access Dutch Railways (NS) travel information, schedules, and real-time updates

### 🔄 <a name="version-control"></a>Version Control

Interact with Git repositories and version control platforms. Enables repository management, code analysis, pull request handling, issue tracking, and other version control operations through standardized APIs.

- [@modelcontextprotocol/server-github](https://github.com/modelcontextprotocol/servers/tree/main/src/github) 📇 ☁️ - GitHub API integration for repository management, PRs, issues, and more
- [@modelcontextprotocol/server-gitlab](https://github.com/modelcontextprotocol/servers/tree/main/src/gitlab) 📇 ☁️ 🏠 - GitLab platform integration for project management and CI/CD operations
- [@modelcontextprotocol/server-git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) 🐍 🏠 - Direct Git repository operations including reading, searching, and analyzing local repositories
- [adhikasp/mcp-git-ingest](https://github.com/adhikasp/mcp-git-ingest) 🐍 🏠 - Read and analyze GitHub repositories with your LLM

### 🛠️ <a name="other-tools-and-integrations"></a>Other Tools and Integrations

- [apify/actors-mcp-server](https://github.com/apify/actors-mcp-server) 📇 ☁️ - Use 3,000+ pre-built cloud tools, known as Actors, to extract data from websites, e-commerce, social media, search engines, maps, and more
- [ivo-toby/contentful-mcp](https://github.com/ivo-toby/contentful-mcp) 📇 🏠 - Update, create, delete content, content-models and assets in your Contentful Space
- [mzxrai/mcp-openai](https://github.com/mzxrai/mcp-openai) 📇 ☁️ - Chat with OpenAI's smartest models
- [mrjoshuak/godoc-mcp](https://github.com/mrjoshuak/godoc-mcp) 🏎️ 🏠 - Token-efficient Go documentation server that provides AI assistants with smart access to package docs and types without reading entire source files
- [pierrebrunelle/mcp-server-openai](https://github.com/pierrebrunelle/mcp-server-openai) 🐍 ☁️ - Query OpenAI models directly from Claude using MCP protocol
- [@modelcontextprotocol/server-everything](https://github.com/modelcontextprotocol/servers/tree/main/src/everything) 📇 🏠 - MCP server that exercises all the features of the MCP protocol
- [baba786/phabricator-mcp-server](https://github.com/baba786/phabricator-mcp-server) 🐍 ☁️ - Interacting with Phabricator API
- [MarkusPfundstein/mcp-obsidian](https://github.com/MarkusPfundstein/mcp-obsidian) 🐍 ☁️ 🏠 - Interacting with Obsidian via REST API
- [calclavia/mcp-obsidian](https://github.com/calclavia/mcp-obsidian) 📇 🏠 - This is a connector to allow Claude Desktop (or any MCP client) to read and search any directory containing Markdown notes (such as an Obsidian vault).
- [anaisbetts/mcp-youtube](https://github.com/anaisbetts/mcp-youtube) 📇 ☁️ - Fetch YouTube subtitles
- [danhilse/notion_mcp](https://github.com/danhilse/notion_mcp) 🐍 ☁️ - Integrates with Notion's API to manage personal todo lists
- [rusiaaman/wcgw](https://github.com/rusiaaman/wcgw/blob/main/src/wcgw/client/mcp_server/Readme.md) 🐍 🏠 - Autonomous shell execution, computer control and coding agent. (Mac)
- [reeeeemo/ancestry-mcp](https://github.com/reeeeemo/ancestry-mcp) 🐍 🏠 - Allows the AI to read .ged files and genetic data
- [sirmews/apple-notes-mcp](https://github.com/sirmews/apple-notes-mcp) 🐍 🏠 - Allows the AI to read from your local Apple Notes database (macOS only)
- [anjor/coinmarket-mcp-server](https://github.com/anjor/coinmarket-mcp-server) 🐍 🏠 - Coinmarket API integration to fetch cryptocurrency listings and quotes
- [suekou/mcp-notion-server](https://github.com/suekou/mcp-notion-server) 📇 🏠 - Interacting with Notion API
- [amidabuddha/unichat-mcp-server](https://github.com/amidabuddha/unichat-mcp-server) 🐍/📇 ☁️ - Send requests to OpenAI, MistralAI, Anthropic, xAI, Google AI or DeepSeek using MCP protocol via tool or predefined prompts. Vendor API key required
- [evalstate/mcp-miro](https://github.com/evalstate/mcp-miro) 📇 ☁️ - Access MIRO whiteboards, bulk create and read items. Requires OAUTH key for REST API.
- [KS-GEN-AI/jira-mcp-server](https://github.com/KS-GEN-AI/jira-mcp-server) 📇 ☁️ 🍎 🪟 - Get Confluence data via CQL and read pages.
- [KS-GEN-AI/confluence-mcp-server](https://github.com/KS-GEN-AI/confluence-mcp-server) 📇 ☁️ 🍎 🪟 - Read jira data via JQL and api and execute requests to create and edit tickets.
- [sooperset/mcp-atlassian](https://github.com/sooperset/mcp-atlassian) 🐍 ☁️ - MCP server for Atlassian products (Confluence and Jira). Supports Confluence Cloud, Jira Cloud, and Jira Server/Data Center. Provides comprehensive tools for searching, reading, creating, and managing content across Atlassian workspaces.
- [pyroprompts/any-chat-completions-mcp](https://github.com/pyroprompts/any-chat-completions-mcp) - Chat with any other OpenAI SDK Compatible Chat Completions API, like Perplexity, Groq, xAI and more
- [anaisbetts/mcp-installer](https://github.com/anaisbetts/mcp-installer) 🐍 🏠 -  An MCP server that installs other MCP servers for you.
- [tanigami/mcp-server-perplexity](https://github.com/tanigami/mcp-server-perplexity) 🐍 ☁️ - Interacting with Perplexity API.
- [future-audiences/wikimedia-enterprise-model-context-protocol](https://gitlab.wikimedia.org/repos/future-audiences/wikimedia-enterprise-model-context-protocol) 🐍 ☁️  - Wikipedia Article lookup API
- [andybrandt/mcp-simple-timeserver](https://github.com/andybrandt/mcp-simple-timeserver) 🐍 🏠☁️ - An MCP server that allows checking local time on the client machine or current UTC time from an NTP server
- [andybrandt/mcp-simple-openai-assistant](https://github.com/andybrandt/mcp-simple-openai-assistant) - 🐍 ☁️  MCP to talk to OpenAI assistants (Claude can use any GPT model as his assitant)
- [@llmindset/mcp-hfspace](https://github.com/evalstate/mcp-hfspace) 📇 ☁️ - Use HuggingFace Spaces directly from Claude. Use Open Source Image Generation, Chat, Vision tasks and more. Supports Image, Audio and text uploads/downloads.
- [zueai/mcp-manager](https://github.com/zueai/mcp-manager) 📇 ☁️ - Simple Web UI to install and manage MCP servers for Claude Desktop App.
- [wong2/mcp-cli](https://github.com/wong2/mcp-cli) 📇 🏠 - CLI tool for testing MCP servers
- [isaacwasserman/mcp-vegalite-server](https://github.com/isaacwasserman/mcp-vegalite-server) 🐍 🏠 - Generate visualizations from fetched data using the VegaLite format and renderer.
- [tevonsb/homeassistant-mcp](https://github.com/tevonsb/homeassistant-mcp) 📇 🏠 - Access Home Assistant data and control devices (lights, switches, thermostats, etc).
- [allenporter/mcp-server-home-assistant](https://github.com/allenporter/mcp-server-home-assistant) 🐍 🏠 - Expose all Home Assistant voice intents through a Model Context Protocol Server allowing home control.
- [nguyenvanduocit/all-in-one-model-context-protocol](https://github.com/nguyenvanduocit/all-in-one-model-context-protocol) 🏎️ 🏠 - Some useful tools for developer, almost everything an engineer need: confluence, Jira, Youtube, run script, knowledge base RAG, fetch URL, Manage youtube channel, emails, calendar, gitlab
- [@joshuarileydev/mac-apps-launcher-mcp-server](https://github.com/JoshuaRileyDev/mac-apps-launcher) 📇 🏠 - An MCP server to list and launch applications on MacOS
- [ZeparHyfar/mcp-datetime](https://github.com/ZeparHyfar/mcp-datetime) - MCP server providing date and time functions in various formats
- [SecretiveShell/MCP-wolfram-alpha](https://github.com/SecretiveShell/MCP-wolfram-alpha) 🐍 ☁️ - An MCP server for querying wolfram alpha API.
- [Amazon Bedrock Nova Canvas](https://github.com/zxkane/mcp-server-amazon-bedrock) 📇 ☁️ - Use Amazon Nova Canvas model for image generation.
- [apinetwork/piapi-mcp-server](https://github.com/apinetwork/piapi-mcp-server) 📇 ☁️ PiAPI MCP server makes user able to generate media content with Midjourney/Flux/Kling/Hunyuan/Udio/Trellis directly from Claude or any other MCP-compatible apps.
- [gotoolkits/DifyWorkflow](https://github.com/gotoolkits/mcp-difyworkflow-server) - 🏎️ ☁️ Tools to the query and execute of Dify workflows
- [@pskill9/hn-server](https://github.com/pskill9/hn-server) - 📇 ☁️ Parses the HTML content from news.ycombinator.com (Hacker News) and provides structured data for different types of stories (top, new, ask, show, jobs).
- [@mediar-ai/screenpipe](https://github.com/mediar-ai/screenpipe) - 🎖️ 🦀 🏠 🍎 Local-first system capturing screen/audio with timestamped indexing, SQL/embedding storage, semantic search, LLM-powered history analysis, and event-triggered actions - enables building context-aware AI agents through a NextJS plugin ecosystem.
- [akseyh/bear-mcp-server](https://github.com/akseyh/bear-mcp-server) - Allows the AI to read from your Bear Notes (macOS only)
- [hmk/attio-mcp-server](https://github.com/hmk/attio-mcp-server) - 📇 ☁️ Allows AI clients to manage records and notes in Attio CRM
- [roychri/mcp-server-asana](https://github.com/roychri/mcp-server-asana) - 📇 ☁️ This Model Context Protocol server implementation of Asana allows you to talk to Asana API from MCP Client such as Anthropic's Claude Desktop Application, and many more.
- [ws-mcp](https://github.com/nick1udwig/ws-mcp) - Wrap MCP servers with a WebSocket (for use with [kitbitz](https://github.com/nick1udwig/kibitz))
- [AbdelStark/bitcoin-mcp](https://github.com/AbdelStark/bitcoin-mcp) - ₿ A Model Context Protocol (MCP) server that enables AI models to interact with Bitcoin, allowing them to generate keys, validate addresses, decode transactions, query the blockchain, and more.
- [tomekkorbak/strava-mcp-server](https://github.com/tomekkorbak/strava-mcp-server) 🐍 ☁️ - An MCP server for Strava, an app for tracking physical exercise
- [tomekkorbak/oura-mcp-server](https://github.com/tomekkorbak/oura-mcp-server) 🐍 ☁️ - An MCP server for Oura, an app for tracking sleep
- [rember/rember-mcp](https://github.com/rember/rember-mcp) 📇 🏠 - Create spaced repetition flashcards in [Rember](https://rember.com) to remember anything you learn in your chats.
- [@makehq/mcp-server](https://github.com/integromat/make-mcp-server) 🎖️ 📇 🏠 - Turn your [Make](https://www.make.com/) scenarios into callable tools for AI assistants.
- [NON906/omniparser-autogui-mcp](https://github.com/NON906/omniparser-autogui-mcp) - 🐍 Automatic operation of on-screen GUI.
- [kj455/mcp-kibela](https://github.com/kj455/mcp-kibela) - 📇 ☁️ Allows AI models to interact with [Kibela](https://kibe.la/)

## Frameworks

- [FastMCP](https://github.com/jlowin/fastmcp) 🐍 - A high-level framework for building MCP servers in Python
- [FastMCP](https://github.com/punkpeye/fastmcp) 📇 - A high-level framework for building MCP servers in TypeScript
- [Foxy Contexts](https://github.com/strowk/foxy-contexts) 🏎️ - Golang library to write MCP Servers declaratively with functional testing included
- [Genkit MCP](https://github.com/firebase/genkit/tree/main/js/plugins/mcp) 📇 – Provides integration between [Genkit](https://github.com/firebase/genkit/tree/main) and the Model Context Protocol (MCP).
- [LiteMCP](https://github.com/wong2/litemcp) 📇 - A high-level framework for building MCP servers in JavaScript/TypeScript
- [mark3labs/mcp-go](https://github.com/mark3labs/mcp-go) 🏎️ - Golang SDK for building MCP Servers and Clients.
- [mcp-framework](https://github.com/QuantGeekDev/mcp-framework) 📇 - Fast and elegant TypeScript framework for building MCP servers
- [mcp-proxy](https://github.com/punkpeye/mcp-proxy) - 📇 A TypeScript SSE proxy for MCP servers that use `stdio` transport.
- [mcp-rs-template](https://github.com/linux-china/mcp-rs-template) 🦀 - MCP CLI server template for Rust
- [metoro-io/mcp-golang](https://github.com/metoro-io/mcp-golang) 🏎️ - Golang framework for building MCP Servers, focussed on type safety
- [rectalogic/langchain-mcp](https://github.com/rectalogic/langchain-mcp) 🐍 - Provides MCP tool calling support in LangChain, allowing for the integration of MCP tools into LangChain workflows.
- [salty-flower/ModelContextProtocol.NET](https://github.com/salty-flower/ModelContextProtocol.NET) #️⃣ 🏠 - A C# SDK for building MCP servers on .NET 9 with NativeAOT compatibility ⚡ 🔌
- [spring-ai-mcp](https://github.com/spring-projects-experimental/spring-ai-mcp) ☕ 🌱 - Java SDK and Spring Framework integration for building MCP client and MCP servers with various, plugable, transport options.
- [@marimo-team/codemirror-mcp](https://github.com/marimo-team/codemirror-mcp) - CodeMirror extension that implements the Model Context Protocol (MCP) for resource mentions and prompt commands.
- [mcp-agent](https://github.com/lastmile-ai/mcp-agent) 🤖 🔌 - Build effective agents with MCP servers using simple, composable patterns.

## Utilities

- [boilingdata/mcp-server-and-gw](https://github.com/boilingdata/mcp-server-and-gw) 📇 - An MCP stdio to HTTP SSE transport gateway with example server and MCP client.
- [isaacwasserman/mcp-langchain-ts-client](https://github.com/isaacwasserman/mcp-langchain-ts-client) 📇 – Use MCP provided tools in LangChain.js
- [lightconetech/mcp-gateway](https://github.com/lightconetech/mcp-gateway) 📇 - A gateway demo for MCP SSE Server.
- [mark3labs/mcphost](https://github.com/mark3labs/mcphost) 🏎️ -  A CLI host application that enables Large Language Models (LLMs) to interact with external tools through the Model Context Protocol (MCP).
- [MCP-Connect](https://github.com/EvalsOne/MCP-Connect) 📇 - A tiny tool that enables cloud-based AI services to access local Stdio based MCP servers by HTTP/HTTPS requests.
- [SecretiveShell/MCP-Bridge](https://github.com/SecretiveShell/MCP-Bridge) 🐍 – an openAI middleware proxy to use mcp in any existing openAI compatible client
- [sparfenyuk/mcp-proxy](https://github.com/sparfenyuk/mcp-proxy) 🐍 – An MCP stdio to SSE transport gateawy.
- [upsonic/gpt-computer-assistant](https://github.com/Upsonic/gpt-computer-assistant) 🐍 – framework to build vertical AI agent

## Tips and Tricks

### Official prompt to inform LLMs how to use MCP

Want to ask Claude about Model Context Protocol?

Create a Project, then add this file to it:

https://modelcontextprotocol.io/llms-full.txt

Now Claude can answer questions about writing MCP servers and how they work

- https://www.reddit.com/r/ClaudeAI/comments/1h3g01r/want_to_ask_claude_about_model_context_protocol/


</details>



























<br><br>
<br><br>
___
<br><br>
<br><br>

# MCP Clients


<details><summary>Click to expand..</summary>






# **MCP (Multiplexed Communication Protocol) vs. SSE (Server-Sent Events)**  


<details><summary>Click to expand..</summary>

#### **1. MCP (Multiplexed Communication Protocol, z. B. stdio bei LLMs)**  
MCP ist ein Protokoll zur effizienten Kommunikation zwischen Prozessen, oft über **Standard-Input/Output (stdio)**. Es wird häufig genutzt, um mehrere Anfragen parallel und effizient abzuarbeiten, z. B. bei Large Language Models (LLMs).  

🔹 **Merkmale:**  
- Vollduplex: Kann gleichzeitig Anfragen senden & Antworten empfangen  
- Multiplexing: Mehrere Anfragen gleichzeitig in einer Verbindung  
- Schnelle Interprozesskommunikation (IPC)  
- Geringer Overhead, da keine Netzwerklatenz (bei lokaler Nutzung)  

🔹 **Anwendungsfälle:**  
- Kommunikation zwischen Host-Prozess und LLMs (z. B. OpenAI API mit stdio)  
- Effiziente Steuerung von Worker-Prozessen in einer Pipeline  
- Kommunikation in eingebetteten Systemen  

#### **2. SSE (Server-Sent Events)**  
SSE ist eine **unidirektionale** Kommunikationstechnik, bei der ein Server kontinuierlich Daten an einen Client sendet (z. B. für Live-Updates in Web-Apps).  

🔹 **Merkmale:**  
- **Nur Server → Client:** Der Client kann keine Nachrichten zurücksenden  
- **Persistent Connection:** Hält eine offene Verbindung für Echtzeit-Updates  
- **Leichtgewichtig:** Simpler als WebSockets  
- **Ereignisgesteuert:** Server kann Events an den Client pushen  

🔹 **Anwendungsfälle:**  
- Live-Updates (z. B. Newsfeeds, Aktienkurse)  
- Serverseitige Streaming-Daten  
- Chat- oder Statusmeldungen in Web-Apps  

#### **Vergleich:**  

| **Kriterium**    | **MCP (stdio)**                          | **SSE**                                |
|-----------------|----------------------------------|----------------------------------|
| **Kommunikation** | Bidirektional (Vollduplex) | Unidirektional (Server → Client) |
| **Verbindung**    | Prozessintern oder über IPC | Persistente HTTP-Verbindung |
| **Multiplexing**  | Ja (mehrere Anfragen parallel) | Nein (einseitiger Stream) |
| **Latenz**        | Sehr gering (lokale Kommunikation) | Gering, aber höher als MCP |
| **Overhead**      | Sehr niedrig | Niedrig (aber HTTP-basiert) |
| **Eignung**       | Hochperformante IPC & AI-Kommunikation | Live-Daten-Updates für Web-Clients |

#### **Fazit:**  
- **MCP (stdio)** ist für Hochgeschwindigkeitskommunikation zwischen Prozessen, z. B. LLMs oder Worker-Systeme.  
- **SSE** ist ideal für kontinuierliche Datenströme von einem Server an Web-Clients.


</details>















<br><br>
<br><br>


# List
- https://glama.ai/mcp/clients
- https://github.com/punkpeye/awesome-mcp-clients/



<details><summary>Click to expand..</summary>

### 5ire

<table>
<tr><th align="left">GitHub</th><td>https://github.com/nanbingxyz/5ire</td></tr>
<tr><th align="left">Website</th><td>https://5ire.app/</td></tr>
<tr><th align="left">License</th><td>GNU v3</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

5ire is a cross-platform desktop AI assistant, MCP client. It compatible with major service providers, supports local knowledge base and tools via model context protocol servers.

<details>
<summary>Screenshots</summary>

https://github.com/user-attachments/assets/a27494c5-437d-481c-a25f-74cfa5a2bc45

</details>

### ChatMCP

<table>
<tr><th align="left">GitHub</th><td>https://github.com/daodao97/chatmcp</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>Apache 2.0</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Dart</td></tr>
</table>

ChatMCP is an AI chat client implementing the Model Context Protocol (MCP).

<details>
<summary>Screenshots</summary>

![](./screenshots/chatmcp/preview.png)
![](./screenshots/chatmcp/settings.png)

</details>

### Claude Desktop

<table>
<tr><th align="left">GitHub</th><td>-</td></tr>
<tr><th align="left">Website</th><td>https://claude.ai/download</td></tr>
<tr><th align="left">License</th><td>Proprietary</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>-</td></tr>
</table>

The Claude desktop app brings Claude's capabilities directly to your computer, allowing for seamless integration with your workflow.

<details>
<summary>Screenshots</summary>

![](./screenshots/claude-desktop/claude-desktop.png)

</details>

### ClaudeMind

<table>
<tr><th align="left">GitHub</th><td>-</td></tr>
<tr><th align="left">Website</th><td>https://claudemind.com/</td></tr>
<tr><th align="left">License</th><td>Proprietary</td></tr>
<tr><th align="left">Type</th><td>Desktop app, JetBrains extension</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS</td></tr>
<tr><th align="left">Pricing</th><td>Per seat (from $29)</td></tr>
<tr><th align="left">Programming Languages</th><td>-</td></tr>
</table>

Experience Claude AI without limits. Use our desktop app for everyday AI assistance, or boost your coding productivity with our JetBrains plugin.

<details>
<summary>Screenshots</summary>

![](./screenshots/claudemind/ClaudeMind_Desktop_Chat_History.png)
![](./screenshots/claudemind/ClaudeMind_Desktop_NewChatPage.png)
![](./screenshots/claudemind/ClaudeMind_Desktop_Projects.png)

</details>

### Cline

<table>
<tr><th align="left">GitHub</th><td>https://github.com/cline/cline</td></tr>
<tr><th align="left">Website</th><td>https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev</td></tr>
<tr><th align="left">License</th><td>Apache 2.0</td></tr>
<tr><th align="left">Type</th><td>VSCode extension</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

Cline can handle complex software development tasks step-by-step. With tools that let him create & edit files, explore large projects, use the browser, and execute terminal commands (after you grant permission), he can assist you in ways that go beyond code completion or tech support. Cline can even use the Model Context Protocol (MCP) to create new tools and extend his own capabilities. While autonomous AI scripts traditionally run in sandboxed environments, this extension provides a human-in-the-loop GUI to approve every file change and terminal command, providing a safe and accessible way to explore the potential of agentic AI.

<details>
<summary>Screenshots</summary>

![](./screenshots/cline/cline-demo.gif)

</details>

### console-chat-gpt

<table>
<tr><th align="left">GitHub</th><td>https://github.com/amidabuddha/console-chat-gpt</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>MIT</td></tr>
<tr><th align="left">Type</th><td>CLI</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Python</td></tr>
</table>

Enjoy seamless interactions with ChatGPT, MistralAI, Claude by Anthropic, Grok by xAI, Gemini by Google and DeepSeek directly from your command line. Elevate your chat experience with efficiency and ease.

<details>
<summary>Screenshots</summary>

![](./screenshots/console-chat-gpt/markdown_preview.gif)
![](./screenshots/console-chat-gpt/python_for_loop.gif)
![](./screenshots/console-chat-gpt/settings_preview.gif)

</details>

### Cursor

<table>
<tr><th align="left">GitHub</th><td>https://github.com/getcursor/cursor</td></tr>
<tr><th align="left">Website</th><td>https://cursor.com</td></tr>
<tr><th align="left">License</th><td>Proprietary</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Freemium</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

Cursor is an AI-first code editor fork of VS Code that helps you code faster with built-in chat, edit, and debugging AI features. It supports MCP for enhanced AI capabilities and tool integration.

<details>
<summary>Screenshots</summary>

![Main Interface](./screenshots/cursor/cursor.png)
![Adding New MCP Server](./screenshots/cursor/new-server.png)
![Settings Interface](./screenshots/cursor/settings.png)
![Calling MCP Server](./screenshots/cursor/calling.png)
![MCP Server Response](./screenshots/cursor/called.png)

</details>

### Continue

<table>
<tr><th align="left">GitHub</th><td>https://github.com/continuedev/continue</td></tr>
<tr><th align="left">Website</th><td>https://continue.dev/</td></tr>
<tr><th align="left">License</th><td>Apache 2.0</td></tr>
<tr><th align="left">Type</th><td>VSCode extension, JetBrains extension</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

Continue is the leading open-source AI code assistant. You can connect any models and any context to build custom autocomplete and chat experiences inside VS Code and JetBrains.

<details>
<summary>Screenshots</summary>

![](./screenshots/continue/continue-demo.gif)

</details>

### Goose

<table>
<tr><th align="left">GitHub</th><td>https://github.com/block/goose</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>Apache 2.0</td></tr>
<tr><th align="left">Type</th><td>AI Agent</td></tr>
<tr><th align="left">Platforms</th><td>MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Rust</td></tr>
</table>

Goose is a general-purpose AI agent that can dynamically plug into new extensions and learn how to use them. It solves higher-level problems using tools from multiple extensions and can interact with multiple extensions at once.

<details>
<summary>Screenshots</summary>

![Goose Logo](./screenshots/goose/goose.png)
![Custom Extension Chat](./screenshots/goose/custom-extension-chat.png)
![Custom Extension Tools](./screenshots/goose/custom-extension-tools-9d440447ae99b18ae92819e652148abe.png)
![Extension Settings](./screenshots/goose/extension%20settings.png)
![List Tools](./screenshots/goose/list%20tools.png)

</details>

### HyperChat

<table>
<tr><th align="left">GitHub</th><td>https://github.com/BigSweetPotatoStudio/HyperChat</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>Apache 2.0<a href="https://github.com/BigSweetPotatoStudio/HyperChat/blob/main/LICENSE">*</a></td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>JavaScript</td></tr>
</table>

HyperChat is an open Chat client that can use various LLM APIs to provide the best Chat experience and implement productivity tools through the MCP protocol.

<details>
<summary>Screenshots</summary>

![](./screenshots/hyperchat/image13.png)
![](./screenshots/hyperchat/image21.png)
![](./screenshots/hyperchat/image22.png)
![](./screenshots/hyperchat/image33.png)
![](./screenshots/hyperchat/image34.png)
![](./screenshots/hyperchat/image35.png)
![](./screenshots/hyperchat/image36.png)
![](./screenshots/hyperchat/image42.png)
![](./screenshots/hyperchat/image43.png)
![](./screenshots/hyperchat/image44.png)
![](./screenshots/hyperchat/image45.png)
![](./screenshots/hyperchat/image46.png)
![](./screenshots/hyperchat/image48.png)

</details>

### kibitz

<table>
<tr><th align="left">GitHub</th><td>https://github.com/nick1udwig/kibitz</td></tr>
<tr><th align="left">Website</th><td>https://kibi.tz</td></tr>
<tr><th align="left">License</th><td>MIT</td></tr>
<tr><th align="left">Type</th><td>Mobile app, Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Mobile, Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

kibitiz is the free and open-source Replit. Minimally, it is a lightweight chat interface to the popular LLM APIs (Anthropic and OpenAI API formats supported). Experience automated tool loops: try asking your agent to use [wcgw](https://github.com/rusiaaman/wcgw) to make a change to a local repository, then fix linter and compiler errors, make a commit, and push to remote, all without user intervention! Even better, code on-the-go by setting up MCP servers on your laptop, then connecting from your mobile through [Kinode](https://github.com/kinode-dao/kinode).

<details>
<summary>Screenshots</summary>
  
https://github.com/user-attachments/assets/3f8df448-1c81-4ff2-8598-c48283a4dc00

</details>

### LibreChat

<table>
<tr><th align="left">GitHub</th><td>https://github.com/danny-avila/LibreChat</td></tr>
<tr><th align="left">Website</th><td>https://www.librechat.ai/</td></tr>
<tr><th align="left">License</th><td>MIT license</td></tr>
<tr><th align="left">Type</th><td>Web app</td></tr>
<tr><th align="left">Platforms</th><td>-</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

Enhanced ChatGPT Clone: Features Agents, Anthropic, AWS, OpenAI, Assistants API, Azure, Groq, o1, GPT-4o, Mistral, OpenRouter, Vertex AI, Gemini, Artifacts, AI model switching, message search, Code Interpreter, langchain, DALL-E-3, OpenAPI Actions, Functions, Secure Multi-User Auth, Presets, open-source for self-hosting.

<details>
<summary>Screenshots</summary>

![](./screenshots/librechat/librechat.webp)

</details>

### MCP Chatbot

<table>
<tr><th align="left">GitHub</th><td>https://github.com/3choff/mcp-chatbot</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>MIT</td></tr>
<tr><th align="left">Type</th><td>CLI</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Python</td></tr>
</table>

This chatbot example demonstrates how to integrate the Model Context Protocol (MCP) into a simple CLI chatbot. The implementation showcases MCP's flexibility by supporting multiple tools through MCP servers and is compatible with any LLM provider that follows OpenAI API standards.

### MCP CLI client

<table>
<tr><th align="left">GitHub</th><td>https://github.com/adhikasp/mcp-client-cli</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>MIT</td></tr>
<tr><th align="left">Type</th><td>CLI</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Python</td></tr>
</table>

A simple CLI to run LLM prompt and implement MCP client.

<details>
<summary>Screenshots</summary>

![](./screenshots/mcp-cli-client/usage.png)

</details>

### oterm

<table>
<tr><th align="left">GitHub</th><td>https://github.com/ggozad/oterm</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>MIT</td></tr>
<tr><th align="left">Type</th><td>CLI</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Python</td></tr>
</table>

A terminal client for Ollama, with support for MCP servers.

<details>
<summary>Screenshots</summary>

![](./screenshots/oterm/chat.png)
![](./screenshots/oterm/mcp.svg)

</details>

### Superinterface

<table>
<tr><th align="left">GitHub</th><td>https://github.com/supercorp-ai/superinterface</td></tr>
<tr><th align="left">Website</th><td>https://superinterface.ai</td></tr>
<tr><th align="left">License</th><td>Proprietary</td></tr>
<tr><th align="left">Type</th><td>Web app</td></tr>
<tr><th align="left">Platforms</th><td>Web</td></tr>
<tr><th align="left">Pricing</th><td>Freemium</td></tr>
<tr><th align="left">Programming Languages</th><td>TypeScript</td></tr>
</table>

Superinterface is AI infrastructure and a developer platform to build in-app AI assistants with support for MCP, interactive components, client-side function calling and more.

Key features:

- Use tools from MCP servers in assistants embedded via React components or script tags
- SSE transport support
- Use any AI model from any AI provider (OpenAI, Anthropic, Ollama, others)

<details>
<summary>Screenshots</summary>

![](./screenshots/superinterface/mcp-chat.png)
![](./screenshots/superinterface/interfaces.png)
![](./screenshots/superinterface/setup-1.png)
![](./screenshots/superinterface/setup-2.png)
![](./screenshots/superinterface/setup-3.png)

</details>

### Tester MCP Client

<table>
<tr><th align="left">GitHub</th><td>https://github.com/apify/tester-mcp-client</td></tr>
<tr><th align="left">Website</th><td>https://apify.com/jiri.spilka/tester-mcp-client</td></tr>
<tr><th align="left">License</th><td>Apache 2.0</td></tr>
<tr><th align="left">Type</th><td>Web app</td></tr>
<tr><th align="left">Platforms</th><td>Web</td></tr>
<tr><th align="left">Pricing</th><td>Freemium</td></tr>
<tr><th align="left">Programming Languages</th><td>JavaScript</td></tr>
</table>

A client that connects to any MCP server using Server-Sent Events (SSE) and displays conversations in a chat-like UI.  
It is a standalone Apify Actor for testing MCP servers over SSE, with support for Authorization headers.  
Built with plain JavaScript (old-school style) and hosted on Apify, it requires no setup to run.  

Key features:

- Connects to any MCP server via Server-Sent Events (SSE).  
- Works with the [Apify MCP Server](https://apify.com/apify/actors-mcp-server) to interact with one or more Apify [Actors](https://apify.com/store).  
- Dynamically utilizes tools based on context and user queries (if supported by the server).  
- Open-source—review, suggest improvements, or modify as needed.

<details>
<summary>Screenshots</summary>

![](./screenshots/tester-mcp-client/setup.png)
![](./screenshots/tester-mcp-client/chat-ui.png)

</details>

### Witsy

<table>
<tr><th align="left">GitHub</th><td>https://github.com/nbonamy/witsy</td></tr>
<tr><th align="left">Website</th><td>https://witsyai.com</td></tr>
<tr><th align="left">License</th><td>Apache 2.0</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Typescript, Vue</td></tr>
</table>

Witsy is an AI desktop assistant supporting models from all major providers and one keyboard shortcut away!

<details>
<summary>Screenshots</summary>

![](./screenshots/witsy/main.jpg)
![](./screenshots/witsy/mcp.jpg)

</details>

### Enconvo

<table>
<tr><th align="left">GitHub</th><td>https://github.com/Enconvo</td></tr>
<tr><th align="left">Website</th><td>https://enconvo.com</td></tr>
<tr><th align="left">License</th><td>Proprietary</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td> MacOS </td></tr>
<tr><th align="left">Pricing</th><td>Freemium</td></tr>
<tr><th align="left">Programming Languages</th><td>Typescript, Python , Swift</td></tr>
</table>

Enconvo is your AI Agent Launcher that revolutionizes productivity. With instant access, automate your daily tasks effortlessly. Our intelligent AI Agent system, powered by 150+ built-in tools and MCP support, learns and adapts to your workflow. Experience seamless automation and enhanced productivity with the most versatile AI assistant for macOS.

<details>
<summary>Screenshots</summary>

![](./screenshots/enconvo/agent_use_mcp.png)
![](./screenshots/enconvo/mcp_config.png)

</details>

### y-cli

<table>
<tr><th align="left">GitHub</th><td>https://github.com/luohy15/y-cli</td></tr>
<tr><th align="left">Website</th><td>-</td></tr>
<tr><th align="left">License</th><td>MIT</td></tr>
<tr><th align="left">Type</th><td>CLI</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Python</td></tr>
</table>

A tiny command-line interface chat application that brings AI conversations to your terminal. Features include chat data storage in JSONL files, interactive chat interface, support for multiple bot configurations compatible with OpenAI chat completion streaming format, Deepseek-r1 reasoning content support, and MCP client support with multiple server configurations.

<details>
<summary>Screenshots</summary>

![Interactive Chat](./screenshots/y-cli/interactive-chat.png)
![MCP Server Configurations](./screenshots/y-cli/multi-mcp-server.png)
![MCP Demo](./screenshots/y-cli/mcp.gif)

</details>

### Zed

<table>
<tr><th align="left">GitHub</th><td>https://github.com/zed-industries/zed</td></tr>
<tr><th align="left">Website</th><td>https://zed.dev/</td></tr>
<tr><th align="left">License</th><td>GNU</td></tr>
<tr><th align="left">Type</th><td>Desktop app</td></tr>
<tr><th align="left">Platforms</th><td>Windows, MacOS, Linux</td></tr>
<tr><th align="left">Pricing</th><td>Free</td></tr>
<tr><th align="left">Programming Languages</th><td>Rust</td></tr>
</table>

Zed is a high-performance, multiplayer code editor from the creators of Atom and Tree-sitter.


</details>

  
</details>
