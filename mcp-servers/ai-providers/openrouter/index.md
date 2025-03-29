# 🔌 OpenRouter MCP Server

Der OpenRouter MCP Server ermöglicht den Zugriff auf eine Vielzahl von KI-Modellen über die OpenRouter-Plattform innerhalb des Model Context Protocol (MCP) Ökosystems.

## 📋 Überblick

OpenRouter ist ein Dienst, der als Gateway zu verschiedenen KI-Modellen von Anbietern wie Anthropic, OpenAI, Mistral AI und vielen anderen fungiert. Der OpenRouter MCP Server macht diese Funktionalität für MCP-fähige Anwendungen verfügbar.

### Hauptfunktionen

- Zugriff auf eine Vielzahl von Sprachmodellen über eine einheitliche API
- Modellsuche und -filterfunktionen
- Konfigurierbare Modellparameter wie Temperatur
- Einfache Integration in MCP-Workflows
- Kostenkontrolle und Optimierung der Modellnutzung

## 🛠️ Installation

### Installation über Smithery CLI

Die einfachste Methode zur Installation ist über den Smithery CLI:

```bash
npx -y @smithery/cli@latest install @mcpserver/openrouterai --client cursor
```

### Manuelle Konfiguration

#### Lokale Konfiguration

```json
{
  "mcpServers": {
    "openrouterai": {
      "command": "npx",
      "args": ["@mcpservers/openrouterai"],
      "env": {
        "OPENROUTER_API_KEY": "xxxxxxxxxxxxxxxxxxxxxxxx"
      }
    }
  }
}
```

#### Smithery Konfiguration

**MAC/Linux**:
```json
{
  "mcpServers": {
    "openrouterai": {
      "command": "npx",
      "args": [
        "-y",
        "@smithery/cli@latest",
        "run",
        "@mcpserver/openrouterai",
        "--config",
        "{\"openrouterApiKey\":\"xxxxxxxxxxxxxxx\",\"openrouterDefaultModel\":\"\"}"
      ]
    }
  }
}
```

**Windows**:
```json
{
  "mcpServers": {
    "openrouterai": {
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@smithery/cli@latest",
        "run",
        "@mcpserver/openrouterai",
        "--config",
        "{\"openrouterApiKey\":\"xxxxxxxxxxxxxxx\",\"openrouterDefaultModel\":\"\"}"
      ]
    }
  }
}
```

## 🔑 API-Schlüssel erhalten

Um den OpenRouter MCP Server zu nutzen, benötigst du einen API-Schlüssel:

1. Erstelle ein Konto auf [OpenRouter.ai](https://openrouter.ai)
2. Navigiere zu deinen Kontoeinstellungen
3. Erstelle einen neuen API-Schlüssel
4. Füge den Schlüssel in deine MCP-Konfiguration ein

## 🚀 Verwendung

Der OpenRouter MCP Server bietet folgende Haupt-Tools:

### 1. Chat-Anfragen senden

```
Tool: mcp_openrouterai_chat_completion
Parameter:
  - messages: Array von Nachrichten mit Rollen und Inhalten
  - model: Optional, z.B. "anthropic/claude-3-sonnet-20240229"
  - temperature: Optional, 0-2
```

### 2. Modelle suchen und filtern

```
Tool: mcp_openrouterai_search_models
Parameter:
  - query: Optional, Suchbegriff
  - capabilities: Optional, Filterfunktionen (z.B. vision, json_mode)
  - provider: Optional, spezifischer Anbieter
```

### 3. Modelldetails abrufen

```
Tool: mcp_openrouterai_get_model_info
Parameter:
  - model: Modell-ID
```

### 4. Modell-ID validieren

```
Tool: mcp_openrouterai_validate_model
Parameter:
  - model: Zu validierende Modell-ID
```

## 📊 Verfügbare Modelle

OpenRouter bietet Zugriff auf eine große Auswahl an Modellen, darunter:

- Anthropic: Claude 3 (Opus, Sonnet, Haiku)
- OpenAI: GPT-4, GPT-3.5
- Mistral AI: Mistral, Mixtral
- Google: Gemini
- Viele weitere Modelle von verschiedenen Anbietern

Die verfügbaren Modelle können über die `search_models`-Funktion abgefragt werden.

## 💡 Anwendungsfälle

- **Modellvergleich:** Teste dieselbe Anfrage mit verschiedenen Modellen
- **Spezialisierte Aufgaben:** Wähle das optimale Modell für spezifische Anforderungen
- **Kostenoptimierung:** Balanciere Kosten und Leistung für unterschiedliche Anwendungsfälle
- **Redundanz:** Wechsel bei Ausfällen oder API-Limits auf alternative Modelle

## 🔗 Links

- [OpenRouter AI Server Docs](https://smithery.ai/server/@mcpserver/openrouterai)
- [GitHub OpenRouter AI](https://github.com/heltonteixeira/openrouterai)
- [OpenRouter Website](https://openrouter.ai/)
- [Claude 3.7 Sonnet auf OpenRouter](https://openrouter.ai/anthropic/claude-3.7-sonnet) 