# 🔍 Exa MCP Server

Exa ist ein leistungsstarker MCP-Server für AI-gestützte Websuchen, der speziell für Entwickler und technische Recherchen optimiert ist.

## 📋 Überblick

Exa bietet eine fortschrittliche Suchplattform, die es KI-Assistenten ermöglicht, präzise und kontextrelevante Informationen aus dem Web zu extrahieren. Der Dienst ist besonders für Entwickler und technische Anwendungsfälle optimiert.

### Hauptfunktionen

- **Präzise Websuche** mit Fokus auf Entwicklerinhalte
- **Echtzeit-Crawling** von Webseiten
- **Konfigurierbare Suchergebnisanzahl**
- **Anpassbare Crawling-Strategie** (immer oder als Fallback)
- **Vollständige Inhaltsextraktion** von relevanten Websites

## 🛠️ Installation

### Installation über Smithery CLI

Die einfachste Methode zur Installation ist über den Smithery CLI:

```bash
npx -y @smithery/cli@latest install exa --client cursor
```

### Manuelle Konfiguration

Es gibt verschiedene Methoden zur manuellen Konfiguration des Exa MCP-Servers:

#### Methode 1 (Empfohlen)

Konfiguriere den MCP-Server in der Datei `~/.cursor/mcp.json`:

**Windows**:
```json
{
  "mcpServers": {
    "exa": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "exa-labs/exa-mcp-server"
      ],
      "env": {
        "EXA_API_KEY": "xxxx"
      }
    }
  }
}
```

**Linux/Mac**:
```json
{
  "mcpServers": {
    "exa": {
      "command": "npx",
      "args": ["exa-labs/exa-mcp-server"],
      "env": {
        "EXA_API_KEY": "xxxx"
      }
    }
  }
}
```

#### Methode 2

Installiere den Server global und verweise darauf in der Konfiguration:

```bash
npm install -g exa-mcp-server
```

**Windows Konfiguration**:
```json
{
  "mcpServers": {
    "exa": {
      "command": "cmd",
      "args": [
        "/c",
        "exa-mcp-server"
      ],
      "env": {
        "EXA_API_KEY": "xxxxxxxxx"
      }
    }
  }
}
```

### Smithery Konfiguration

**Windows**:
```json
{
  "mcpServers": {
    "exa": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@smithery/cli@latest",
        "run",
        "exa",
        "--config",
        "{\"exaApiKey\":\"xxxxxxxxxxxxxxxxxx\"}"
      ]
    }
  }
}
```

**Linux/Mac**:
```json
{
  "mcpServers": {
    "exa": {
      "command": "npx",
      "args": [
        "-y",
        "@smithery/cli@latest",
        "run",
        "exa",
        "--config",
        "{\"exaApiKey\":\"xxxxxxxxxxxxxxxxxx\"}"
      ]
    }
  }
}
```

## 🔑 API-Schlüssel erhalten

Um den Exa MCP Server zu nutzen, benötigst du einen API-Schlüssel:

1. Besuche das [Exa API Dashboard](https://dashboard.exa.ai/api-keys)
2. Erstelle ein Konto oder melde dich an
3. Erstelle einen neuen API-Schlüssel
4. Kopiere den Schlüssel und füge ihn in deine MCP-Konfiguration ein

## 🚀 Verwendung

Der Exa MCP Server bietet folgende Hauptfunktion:

```
Tool: mcp_exa_search
Parameter:
  - query: Der Suchbegriff
  - numResults: (Optional) Anzahl der Suchergebnisse (Standard: 5)
  - livecrawl: (Optional) Crawling-Strategie: "always" oder "fallback"
```

### Beispiele

**Einfache Suche**:
```
mcp_exa_search({"query": "React useEffect Hook Erklärung"})
```

**Erweiterte Suche mit mehr Ergebnissen**:
```
mcp_exa_search({"query": "Python async await Beispiele", "numResults": 10})
```

**Suche mit erzwungenem Live-Crawling**:
```
mcp_exa_search({"query": "neueste Typescript Features", "livecrawl": "always"})
```

## 💡 Anwendungsfälle

- **Technische Recherche**: Finde aktuelle Dokumentation und Best Practices
- **Code-Beispiele**: Suche nach implementierungsrelevanten Codebeispielen
- **Fehlersuche**: Recherchiere Fehlermeldungen und Lösungen für bekannte Probleme
- **Aktuelle Entwicklungen**: Halte dich über neueste Framework-Updates informiert
- **Konzeptverständnis**: Finde tiefgehende Erklärungen zu technischen Konzepten

## 🔗 Links

- [Exa MCP Server GitHub](https://github.com/exa-labs/exa-mcp-server)
- [Smithery Exa Server](https://smithery.ai/server/exa)
- [Exa API Dashboard](https://dashboard.exa.ai/api-keys) 