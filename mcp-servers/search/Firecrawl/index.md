# 🔍 Firecrawl MCP Server

Firecrawl ist ein leistungsstarker MCP-Server für Web-Scraping, Crawling und Informationsextraktion mit JavaScript-Rendering-Unterstützung.

## 📋 Überblick

Firecrawl bietet fortschrittliche Web-Scraping-Funktionen, die es KI-Assistenten ermöglichen, Webseiten zu analysieren, Inhalte zu extrahieren und tiefgreifende Recherchen durchzuführen. Der Dienst unterstützt JavaScript-Rendering und bietet verschiedene Werkzeuge für die Informationsgewinnung.

<details>
<summary><b>Hauptfunktionen</b></summary>

- **Web-Scraping mit JavaScript-Rendering**
- **URL-Erkennung und Crawling**
- **Websuche mit Inhaltsextraktion**
- **Automatische Wiederholungsversuche mit exponentieller Verzögerung**
- **Effiziente Stapelverarbeitung mit integrierter Ratenbegrenzung**
- **Kreditverbrauchsüberwachung für Cloud-API**
- **Umfassendes Protokollierungssystem**
- **Unterstützung für Cloud- und selbstgehostete FireCrawl-Instanzen**
- **Mobile/Desktop-Ansichtsunterstützung**
- **Intelligente Inhaltsfilterung mit Tag-Ein-/Ausschluss**
</details>

## 🛠️ Installation

<details>
<summary><b>Ausführen mit npx</b></summary>

```bash
env FIRECRAWL_API_KEY=fc-YOUR_API_KEY npx -y firecrawl-mcp
```
</details>

<details>
<summary><b>Manuelle Installation</b></summary>

```bash
npm install -g firecrawl-mcp
```
</details>

<details>
<summary><b>Konfiguration in Cursor</b></summary>

**Hinweis:** Erfordert Cursor Version 0.45.6+

So konfigurierst du Firecrawl MCP in Cursor:

1. Öffne die Cursor-Einstellungen
2. Gehe zu Features > MCP Servers
3. Klicke auf "+ Add New MCP Server"
4. Gib Folgendes ein:
   - Name: "firecrawl-mcp" (oder ein Name deiner Wahl)
   - Type: "command"
   - Command: `env FIRECRAWL_API_KEY=your-api-key npx -y firecrawl-mcp`

Bei Windows-Problemen versuche: `cmd /c "set FIRECRAWL_API_KEY=your-api-key && npx -y firecrawl-mcp"`

Ersetze `your-api-key` durch deinen FireCrawl API-Schlüssel.
</details>


<details>
<summary><b>Konfiguration für Cursor</b></summary>

```bash
npm install -g firecrawl-mcp
```

Windows:
```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "cmd",
      "args": ["/c", "npx", "-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "fc-xxxxxx4"
      }
    }
  }
}
```

Linux:
```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "npx",
      "args": ["-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "fc-xxxxxx4"
      }
    }
  }
}
```

</details>




<br><br>


<details>
<summary><b>Installation über Smithery (Legacy)</b></summary>

FireCrawl automatisch über Smithery für Claude Desktop installieren:

```bash
npx -y @smithery/cli install @mendableai/mcp-server-firecrawl --client claude
```
</details>

## 🔧 Konfiguration

<details>
<summary><b>Umgebungsvariablen</b></summary>

**Erforderlich für Cloud-API:**
- `FIRECRAWL_API_KEY`: Dein FireCrawl API-Schlüssel
  - Erforderlich bei Verwendung der Cloud-API (Standard)
  - Optional bei Verwendung einer selbstgehosteten Instanz mit `FIRECRAWL_API_URL`
- `FIRECRAWL_API_URL` (Optional): Benutzerdefinierter API-Endpunkt für selbstgehostete Instanzen
  - Beispiel: `https://firecrawl.your-domain.com`
  - Wenn nicht angegeben, wird die Cloud-API verwendet (erfordert API-Schlüssel)

**Optionale Konfiguration:**

Wiederholungskonfiguration:
- `FIRECRAWL_RETRY_MAX_ATTEMPTS`: Maximale Anzahl von Wiederholungsversuchen (Standard: 3)
- `FIRECRAWL_RETRY_INITIAL_DELAY`: Anfangsverzögerung in Millisekunden vor dem ersten Wiederholungsversuch (Standard: 1000)
- `FIRECRAWL_RETRY_MAX_DELAY`: Maximale Verzögerung in Millisekunden zwischen Wiederholungsversuchen (Standard: 10000)
- `FIRECRAWL_RETRY_BACKOFF_FACTOR`: Exponentieller Verzögerungsfaktor (Standard: 2)

Kreditverbrauchsüberwachung:
- `FIRECRAWL_CREDIT_WARNING_THRESHOLD`: Kreditverbrauchswarnungsschwelle (Standard: 1000)
- `FIRECRAWL_CREDIT_CRITICAL_THRESHOLD`: Kritische Kreditverbrauchsschwelle (Standard: 100)
</details>

<details>
<summary><b>Konfigurationsbeispiele</b></summary>

**Für Cloud-API-Nutzung mit benutzerdefinierten Wiederholungs- und Kreditüberwachungseinstellungen:**

```bash
# Erforderlich für Cloud-API
export FIRECRAWL_API_KEY=your-api-key

# Optionale Wiederholungskonfiguration
export FIRECRAWL_RETRY_MAX_ATTEMPTS=5        # Erhöhe maximale Wiederholungsversuche
export FIRECRAWL_RETRY_INITIAL_DELAY=2000    # Starte mit 2s Verzögerung
export FIRECRAWL_RETRY_MAX_DELAY=30000       # Maximale 30s Verzögerung
export FIRECRAWL_RETRY_BACKOFF_FACTOR=3      # Aggressivere Verzögerungssteigerung

# Optionale Kreditüberwachung
export FIRECRAWL_CREDIT_WARNING_THRESHOLD=2000    # Warnung bei 2000 Krediten
export FIRECRAWL_CREDIT_CRITICAL_THRESHOLD=500    # Kritisch bei 500 Krediten
```

**Für selbstgehostete Instanz:**

```bash
# Erforderlich für selbstgehostete Instanz
export FIRECRAWL_API_URL=https://firecrawl.your-domain.com

# Optionale Authentifizierung für selbstgehostete Instanz
export FIRECRAWL_API_KEY=your-api-key  # Falls deine Instanz Authentifizierung erfordert

# Benutzerdefinierte Wiederholungskonfiguration
export FIRECRAWL_RETRY_MAX_ATTEMPTS=10
export FIRECRAWL_RETRY_INITIAL_DELAY=500     # Starte mit schnelleren Wiederholungen
```
</details>

<details>
<summary><b>Verwendung mit Claude Desktop</b></summary>

Füge dies zu deiner `claude_desktop_config.json` hinzu:

```json
{
  "mcpServers": {
    "mcp-server-firecrawl": {
      "command": "npx",
      "args": ["-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "YOUR_API_KEY_HERE",

        "FIRECRAWL_RETRY_MAX_ATTEMPTS": "5",
        "FIRECRAWL_RETRY_INITIAL_DELAY": "2000",
        "FIRECRAWL_RETRY_MAX_DELAY": "30000",
        "FIRECRAWL_RETRY_BACKOFF_FACTOR": "3",

        "FIRECRAWL_CREDIT_WARNING_THRESHOLD": "2000",
        "FIRECRAWL_CREDIT_CRITICAL_THRESHOLD": "500"
      }
    }
  }
}
```
</details>

## 🚀 Verfügbare Tools

<details>
<summary><b>1. Scrape Tool (firecrawl_scrape)</b></summary>

Extrahiere Inhalte von einer einzelnen URL mit erweiterten Optionen.

```json
{
  "name": "firecrawl_scrape",
  "arguments": {
    "url": "https://example.com",
    "formats": ["markdown"],
    "onlyMainContent": true,
    "waitFor": 1000,
    "timeout": 30000,
    "mobile": false,
    "includeTags": ["article", "main"],
    "excludeTags": ["nav", "footer"],
    "skipTlsVerification": false
  }
}
```
</details>

<details>
<summary><b>2. Batch Scrape Tool (firecrawl_batch_scrape)</b></summary>

Extrahiere Inhalte von mehreren URLs effizient mit integrierter Ratenbegrenzung und paralleler Verarbeitung.

```json
{
  "name": "firecrawl_batch_scrape",
  "arguments": {
    "urls": ["https://example1.com", "https://example2.com"],
    "options": {
      "formats": ["markdown"],
      "onlyMainContent": true
    }
  }
}
```

Die Antwort enthält eine Vorgangs-ID für die Statusprüfung:

```json
{
  "content": [
    {
      "type": "text",
      "text": "Batch operation queued with ID: batch_1. Use firecrawl_check_batch_status to check progress."
    }
  ],
  "isError": false
}
```
</details>

<details>
<summary><b>3. Check Batch Status (firecrawl_check_batch_status)</b></summary>

Überprüfe den Status eines Batch-Vorgangs.

```json
{
  "name": "firecrawl_check_batch_status",
  "arguments": {
    "id": "batch_1"
  }
}
```
</details>

<details>
<summary><b>4. Search Tool (firecrawl_search)</b></summary>

Durchsuche das Web und extrahiere optional Inhalte aus den Suchergebnissen.

```json
{
  "name": "firecrawl_search",
  "arguments": {
    "query": "your search query",
    "limit": 5,
    "lang": "en",
    "country": "us",
    "scrapeOptions": {
      "formats": ["markdown"],
      "onlyMainContent": true
    }
  }
}
```
</details>

<details>
<summary><b>5. Crawl Tool (firecrawl_crawl)</b></summary>

Starte ein asynchrones Crawling mit erweiterten Optionen.

```json
{
  "name": "firecrawl_crawl",
  "arguments": {
    "url": "https://example.com",
    "maxDepth": 2,
    "limit": 100,
    "allowExternalLinks": false,
    "deduplicateSimilarURLs": true
  }
}
```
</details>

<details>
<summary><b>6. Extract Tool (firecrawl_extract)</b></summary>

Extrahiere strukturierte Informationen aus Webseiten mit LLM-Funktionen. Unterstützt sowohl Cloud-AI als auch selbstgehostete LLM-Extraktion.

```json
{
  "name": "firecrawl_extract",
  "arguments": {
    "urls": ["https://example.com/page1", "https://example.com/page2"],
    "prompt": "Extract product information including name, price, and description",
    "systemPrompt": "You are a helpful assistant that extracts product information",
    "schema": {
      "type": "object",
      "properties": {
        "name": { "type": "string" },
        "price": { "type": "number" },
        "description": { "type": "string" }
      },
      "required": ["name", "price"]
    },
    "allowExternalLinks": false,
    "enableWebSearch": false,
    "includeSubdomains": false
  }
}
```

Beispielantwort:

```json
{
  "content": [
    {
      "type": "text",
      "text": {
        "name": "Example Product",
        "price": 99.99,
        "description": "This is an example product description"
      }
    }
  ],
  "isError": false
}
```

**Extract Tool Optionen:**
- urls: Array von URLs, aus denen Informationen extrahiert werden sollen
- prompt: Benutzerdefinierte Aufforderung für die LLM-Extraktion
- systemPrompt: Systemaufforderung zur Anleitung des LLM
- schema: JSON-Schema für strukturierte Datenextraktion
- allowExternalLinks: Extraktion aus externen Links erlauben
- enableWebSearch: Websuche für zusätzlichen Kontext aktivieren
- includeSubdomains: Subdomains in die Extraktion einbeziehen
</details>

<details>
<summary><b>7. Deep Research Tool (firecrawl_deep_research)</b></summary>

Führe tiefgreifende Webrecherchen zu einer Abfrage durch, mit intelligentem Crawling, Suche und LLM-Analyse.

```json
{
  "name": "firecrawl_deep_research",
  "arguments": {
    "query": "how does carbon capture technology work?",
    "maxDepth": 3,
    "timeLimit": 120,
    "maxUrls": 50
  }
}
```

**Parameter:**
- query (string, erforderlich): Die Forschungsfrage oder das zu erforschende Thema.
- maxDepth (number, optional): Maximale rekursive Tiefe für Crawling/Suche (Standard: 3).
- timeLimit (number, optional): Zeitlimit in Sekunden für die Forschungssitzung (Standard: 120).
- maxUrls (number, optional): Maximale Anzahl von zu analysierenden URLs (Standard: 50).
</details>

<details>
<summary><b>8. Generate LLMs.txt Tool (firecrawl_generate_llmstxt)</b></summary>

Erzeuge eine standardisierte llms.txt (und optional llms-full.txt) Datei für eine bestimmte Domain. Diese Datei definiert, wie große Sprachmodelle mit der Website interagieren sollten.

```json
{
  "name": "firecrawl_generate_llmstxt",
  "arguments": {
    "url": "https://example.com",
    "maxUrls": 20,
    "showFullText": true
  }
}
```

**Parameter:**
- url (string, erforderlich): Die Basis-URL der zu analysierenden Website.
- maxUrls (number, optional): Maximale Anzahl einzubeziehender URLs (Standard: 10).
- showFullText (boolean, optional): Ob llms-full.txt-Inhalte in der Antwort enthalten sein sollen.
</details>

## 💡 Anwendungsfälle

<details>
<summary><b>Web-Scraping und Informationsextraktion</b></summary>

- **Web-Scraping**: Extrahiere strukturierte Daten von Webseiten mit JavaScript-Rendering-Unterstützung
- **Tiefgreifende Recherche**: Führe komplexe, mehrstufige Webrecherchen zu bestimmten Themen durch
- **Inhaltsanalyse**: Extrahiere und analysiere Inhalte von Webseiten mit LLM-Unterstützung
- **Crawling**: Entdecke und verfolge Links auf Websites, um Inhalte zu sammeln
- **Strukturierte Datenextraktion**: Extrahiere spezifische Informationen nach einem vordefinierten Schema
- **Stapelverarbeitung**: Verarbeite effizient mehrere URLs mit integrierter Ratenbegrenzung
</details>

## 🔗 Links

- [FireCrawl MCP Server GitHub](https://github.com/mendableai/firecrawl-mcp-server)
- [FireCrawl Website](https://firecrawl.dev)
- [Smithery FireCrawl Server](https://smithery.ai/server/@mendableai/mcp-server-firecrawl) 