# 🌐 Browser Tools MCP

Browser Tools MCP ist eine leistungsstarke Chrome-Erweiterung mit MCP-Server-Integration, die umfassende Browser-Automatisierungsfunktionen für KI-Assistenten bereitstellt.

## 📋 Überblick

Browser Tools MCP ermöglicht es KI-Assistenten, direkt mit dem Browser zu interagieren, Screenshots aufzunehmen, Netzwerk-Logs zu analysieren, Accessibility-Audits durchzuführen und viele weitere Browser-bezogene Aufgaben auszuführen.

### Hauptfunktionen

- **Screenshot-Erstellung** von Webseiten
- **Konsolen-Logs und Fehler** abrufen
- **Netzwerk-Logs** analysieren
- **Accessibility-Audits** durchführen
- **Performance-Audits** durchführen
- **SEO-Audits** durchführen
- **Best Practices-Audits** durchführen
- **Debugging-Modus** für Webanwendungen
- **Element-Auswahl** aus der Webseite

## ⚠️ Wichtiger Hinweis

**Diese Komponente funktioniert nicht als direkter Import mit Electron.js.** Nutze stattdessen Remote-Debugging für die Integration.

## 🛠️ Installation

Die Installation erfolgt in zwei Schritten: Zuerst die Chrome-Erweiterung, dann der MCP-Server.

### 1. Chrome-Erweiterung installieren

1. Lade die Chrome-Erweiterung von [GitHub Releases](https://github.com/AgentDeskAI/browser-tools-mcp/releases) herunter.

2. **Unpacked Erweiterung manuell laden**:
   - **Chrome öffnen**
   - **Gehe zu `chrome://extensions/`**
   - **Aktiviere den Entwicklermodus** (Schalter oben rechts)
   - **Klicke auf "Load unpacked"**
   - **Wähle den Ordner mit der `manifest.json`-Datei**
   - **Fertig!** Die Erweiterung ist jetzt aktiv.

Falls Fehler auftreten, überprüfe die Entwicklerkonsole (`F12` → "Console") für Debugging-Informationen.

### 2. MCP-Server installieren und starten

```bash
npm install -g @agentdeskai/browser-tools-mcp
npx @agentdeskai/browser-tools-server
```

**Hinweis:** Der browser-tools-server läuft auf Port 3025. Stelle sicher, dass kein anderer Prozess diesen Port verwendet.

### JSON-Konfiguration

Konfiguriere den MCP-Server in der Datei `~/.cursor/mcp.json`:

**Windows**:
```json
{
  "mcpServers": {
    "browser-tools": {
      "command": "wsl",
      "args": [
        "bash",
        "-c",
        "cmd /c npx -y @agentdeskai/browser-tools-mcp@1.2.0"
      ],
      "enabled": true
    }
  }
}
```

**MAC/Linux**:
```json
{
  "mcpServers": {
    "browser-tools": {
      "command": "npx",
      "args": [
        "-y",
        "@agentdeskai/browser-tools-mcp"
      ],
      "enabled": true
    }
  }
}
```

## 🚀 Verwendung

### Verbindung überprüfen

1. Öffne Chrome Developer Tools: Rechtsklick auf eine beliebige Seite → Inspect
2. In der Konsole werden Logs angezeigt, wenn der MCP-Client verbunden ist

### Empfohlene Einstellungen

Aktiviere in den Erweiterungseinstellungen:
- Auto-paste to Cursor
- Include Request Headers
- Include Response Headers

### Verfügbare Tools

Browser Tools MCP bietet folgende Hauptfunktionen:

```
mcp_browser_tools_getConsoleLogs - Browser-Konsolenprotokolle abrufen
mcp_browser_tools_getConsoleErrors - Browser-Konsolenfehler abrufen
mcp_browser_tools_getNetworkErrors - Netzwerkfehler abrufen
mcp_browser_tools_getNetworkLogs - Alle Netzwerkprotokolle abrufen
mcp_browser_tools_takeScreenshot - Screenshot der aktuellen Browser-Tab erstellen
mcp_browser_tools_getSelectedElement - Ausgewähltes Element aus dem Browser abrufen
mcp_browser_tools_wipeLogs - Alle Browser-Logs aus dem Speicher löschen
mcp_browser_tools_runAccessibilityAudit - Accessibility-Audit auf der aktuellen Seite durchführen
mcp_browser_tools_runPerformanceAudit - Performance-Audit auf der aktuellen Seite durchführen
mcp_browser_tools_runSEOAudit - SEO-Audit auf der aktuellen Seite durchführen
mcp_browser_tools_runNextJSAudit - NextJS-Audit durchführen
mcp_browser_tools_runDebuggerMode - Debugger-Modus zur Fehlerbehebung starten
mcp_browser_tools_runAuditMode - Audit-Modus zur Optimierung der Anwendung starten
mcp_browser_tools_runBestPracticesAudit - Best Practices-Audit durchführen
```

## 💡 Anwendungsfälle

- **Web-Debugging:** Identifiziere und behebe Fehler in Webanwendungen
- **Performance-Optimierung:** Führe Performance-Audits durch und identifiziere Engpässe
- **Accessibility-Tests:** Stelle sicher, dass Webseiten den Accessibility-Standards entsprechen
- **SEO-Optimierung:** Identifiziere und behebe SEO-Probleme
- **Netzwerk-Analyse:** Untersuche Netzwerkanfragen und -antworten

## 🔗 Links

- [Browser Tools MCP GitHub](https://github.com/AgentDeskAI/browser-tools-mcp)
- [Installationsanleitung](https://browsertools.agentdesk.ai/installation)
- [Schnellstartanleitung](https://browsertools.agentdesk.ai/quickstart) 