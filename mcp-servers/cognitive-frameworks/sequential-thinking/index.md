# 🔄 Sequential Thinking MCP Server

Der Sequential Thinking MCP Server ist ein leistungsstarkes Werkzeug zur Strukturierung und Verbesserung von Denkprozessen in KI-Anwendungen durch schrittweise, aufeinander aufbauende Gedankensequenzen.

## 📋 Überblick

Sequential Thinking verbessert die Qualität von Denkprozessen in KI-Systemen, indem es einen strukturierten, schrittweisen Ansatz zum Denken ermöglicht. Es erlaubt dem KI-Modell, Gedanken sequentiell zu entwickeln, frühere Gedanken zu überprüfen und zu revidieren, und so zu fundierteren Schlussfolgerungen zu gelangen.

### Hauptfunktionen

- **Sequentielle Gedankenentwicklung**: Entwicklung von Gedankenketten mit aufeinander aufbauenden Schritten
- **Gedankenrevision**: Möglichkeit, frühere Gedanken zu überprüfen und anzupassen
- **Mehrere Gedankenstränge**: Unterstützung paralleler Gedankenprozesse für komplexe Probleme
- **Denktiefe-Konfiguration**: Anpassbare Tiefe der Gedankensequenzen
- **Automatische Zusammenfassung**: Komprimierung langer Gedankenketten für bessere Übersichtlichkeit
- **Fortschrittsverfolgung**: Überwachung des Fortschritts komplexer Denkprozesse

## ⚙️ Konfigurationsparameter

Der Sequential Thinking Server bietet folgende Konfigurationsoptionen:

1. **maxDepth** – Erhöht die Denktiefe; je höher der Wert, desto komplexer die Überlegungen
2. **parallelTasks** – Ermöglicht die gleichzeitige Verarbeitung mehrerer Gedankenstränge
3. **enableSummarization** – Fasst lange Gedankenketten automatisch zusammen
4. **thoughtCategorization** – Gruppiert ähnliche Gedanken für bessere Übersicht
5. **progressTracking** – Verfolgt den Fortschritt von Gedankengängen
6. **dynamicAdaptation** – Passt Denkstrategien basierend auf Ergebnissen dynamisch an
7. **contextWindow** – Definiert die maximale Verarbeitungsgröße des Kontextes (Standardwert: 32.768 Tokens)

## 🛠️ Installation

### Installation über Smithery CLI

Die einfachste Methode zur Installation ist über den Smithery CLI mit vollständiger Konfiguration:

```bash
npx -y @smithery/cli@latest install @smithery-ai/server-sequential-thinking --client cursor --config "{\"maxDepth\":8,\"parallelTasks\":true,\"enableSummarization\":true,\"thoughtCategorization\":true,\"progressTracking\":true,\"dynamicAdaptation\":true,\"contextWindow\":32768}"
```

### Manuelle Konfiguration

#### Docker-Konfiguration

```json
{
  "mcpServers": {
    "sequentialthinking": {
      "command": "docker",
      "args": [
        "run",
        "--rm",
        "-i",
        "mcp/sequentialthinking"
      ]
    }
  }
}
```

#### Lokale Konfiguration

**Methode 1 - Globale Installation**:

##### Windows
```powershell
npm i -g @modelcontextprotocol/server-sequential-thinking
```

```json
{
  "mcpServers": {
    "sequential-thinking": {
      "command": "cmd",
      "args": [
        "/c",
        "C:\\nvm4w\\nodejs\\node_modules\\@modelcontextprotocol\\server-sequential-thinking\\dist\\index.js"
      ]
    }
  }
}
```

**Methode 2 - NPX**:

##### Windows
```json
{
  "mcpServers": {
    "sequential-thinking": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@modelcontextprotocol/server-sequential-thinking"
      ]
    }
  }
}
```

##### Linux/Mac
```json
{
  "mcpServers": {
    "sequential-thinking": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-sequential-thinking"
      ]
    }
  }
}
```

### Smithery Konfiguration

**Windows**:
```json
{
  "mcpServers": {
    "server-sequential-thinking": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@smithery/cli@latest",
        "run",
        "@smithery-ai/server-sequential-thinking",
        "--config",
        "{\"maxDepth\":8,\"parallelTasks\":true,\"enableSummarization\":true,\"thoughtCategorization\":true,\"progressTracking\":true,\"dynamicAdaptation\":true,\"contextWindow\":32768}"
      ]
    }
  }
}
```

**Linux/Mac**:
```json
{
  "mcpServers": {
    "server-sequential-thinking": {
      "command": "npx",
      "args": [
        "-y",
        "@smithery/cli@latest",
        "run",
        "@smithery-ai/server-sequential-thinking",
        "--config",
        "{\"maxDepth\":8,\"parallelTasks\":true,\"enableSummarization\":true,\"thoughtCategorization\":true,\"progressTracking\":true,\"dynamicAdaptation\":true,\"contextWindow\":32768}"
      ]
    }
  }
}
```

## 🚀 Verwendung

Der Sequential Thinking Server bietet folgende Hauptfunktion:

```
Tool: mcp_server_sequential_thinking_sequentialthinking
Parameter:
  - thought: Der aktuelle Gedankenschritt
  - nextThoughtNeeded: Boolean, ob ein weiterer Gedankenschritt nötig ist
  - thoughtNumber: Aktuelle Nummer in der Gedankensequenz
  - totalThoughts: Geschätzte Gesamtzahl an benötigten Gedanken
  - isRevision: (Optional) Boolean, ob dieser Gedanke eine Revision ist
  - revisesThought: (Optional) Welcher Gedanke revidiert wird
  - branchFromThought: (Optional) Ausgangspunkt für Gedankenverzweigung
  - branchId: (Optional) Kennung für den aktuellen Zweig
  - needsMoreThoughts: (Optional) Ob mehr Gedanken benötigt werden
```

## 💡 Anwendungsfälle

Der Sequential Thinking Server ist besonders nützlich für:

- **Komplexe Problemlösung**: Strukturiertes Durcharbeiten mehrschrittiger Probleme
- **Debugging**: Schrittweise Analyse von Code, um Fehler zu finden
- **Kreatives Denken**: Entwicklung von Ideen durch iterative Verfeinerung
- **Mathematische Berechnungen**: Schrittweise Durchführung komplizierter Berechnungen
- **Argumentationsanalyse**: Entwicklung und Überprüfung von Argumentationsketten
- **Planung**: Erstellung detaillierter Pläne mit Abhängigkeiten und Alternativen
- **Entscheidungsfindung**: Systematische Bewertung von Optionen und Konsequenzen

## 🔗 Links

- [NPM Package](https://www.npmjs.com/package/@modelcontextprotocol/server-sequential-thinking)
- [Smithery AI Dokumentation](https://smithery.ai/server/@smithery-ai/server-sequential-thinking)
- [GitHub Repository](https://github.com/smithery-ai/reference-servers/tree/main/src/sequentialthinking) 