# 🔌 DeepLucid3D UCPF Server

Der DeepLucid3D UCPF Server ist eine leistungsstarke Implementierung des Unified Cognitive Processing Framework (UCPF), die über das Model Context Protocol (MCP) bereitgestellt wird.

## 📋 Überblick

Das UCPF (Unified Cognitive Processing Framework) ist ein kognitives Framework, das AI-gestützte Problemlösungen, kreative Analysen und strukturiertes Denken ermöglicht.

### Funktionsweise

1. **Kognitive Zustandsanalyse**  
   - Erkennt den aktuellen Denkzustand (z. B. Unsicherheit, kreative Klarheit)
   
2. **Wissensdimensionen zuordnen**  
   - Unterteilt Wissen in bekannte, unbekannte und unzugängliche Bereiche

3. **Rekursive Selbstbefragung**  
   - Stellt Annahmen infrage, erkennt Denkfehler

4. **Kreative Perspektivengenerierung**  
   - Erzeugt neue Sichtweisen und Metaphern

5. **Problemanalyse & -lösung**  
   - Zerlegt komplexe Probleme und setzt sie mit neuem Verständnis zusammen

## 🛠️ Installation

### Installation über Smithery CLI

Die einfachste Methode zur Installation ist über den Smithery CLI:

```bash
npx -y @smithery/cli@latest install @MushroomFleet/deeplucid3d-mcp --client cursor
```

### Manuelle Konfiguration

#### Lokale Konfiguration

```json
{
  "mcpServers": {
    "ucpf": {
      "command": "node",
      "args": ["/home/UserName/Projects/mcp/server/prompting/DeepLucid3D-MCP/build/index.js"],
      "env": {},
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

#### Smithery Konfiguration

**MAC/Linux**:
```json
{
  "mcpServers": {
    "deeplucid3d-mcp": {
        "command": "npx",
        "args": [
          "-y",
          "@smithery/cli@latest",
          "run",
          "@MushroomFleet/deeplucid3d-mcp",
          "--config",
          "{\"defaultRenderer\":\"threejs\",\"shaderDebug\":true}"
        ]
    }
  }
}
```

**Windows**:
```json
{
  "mcpServers": {
       "deeplucid3d-mcp": {
        "command": "cmd",
        "args": [
          "/c",
          "npx",
          "-y",
          "@smithery/cli@latest",
          "run",
          "@MushroomFleet/deeplucid3d-mcp",
          "--config",
          "{\"defaultRenderer\":\"threejs\",\"shaderDebug\":true}"
        ]
    }
  }
}
```

## 🚀 Verwendung

Der DeepLucid3D UCPF Server bietet folgende Haupt-Tools:

### 1. Problem analysieren

Verwenden Sie die `analyze_problem`-Funktion, um komplexe Probleme zu zerlegen und zu analysieren:

```
Tool: mcp_ucpf_analyze_problem
Parameter:
  - problem: "Beschreibung des zu analysierenden Problems"
  - detailed: true/false (Optional für detailliertere Analyse)
```

### 2. Kreative Lösungen generieren

Mit der `creative_exploration`-Funktion können neue Perspektiven und Lösungsansätze generiert werden:

```
Tool: mcp_ucpf_creative_exploration
Parameter:
  - topic: "Das zu erkundende Thema"
  - perspective_count: 3 (Optional, Anzahl der Perspektiven)
  - include_metaphors: true/false (Optional)
```

### 3. Sitzungsstatus verwalten

Die `manage_state`-Funktion ermöglicht es, den Status der UCPF-Sitzung zu kontrollieren:

```
Tool: mcp_ucpf_manage_state
Parameter:
  - action: "enable", "disable", "reset" oder "status"
  - session_id: "Optional für spezifische Sitzungen"
```

## 💡 Vorteile

- **Strukturierte Problemlösung:** Zerlegt komplexe Probleme in handhabbare Komponenten
- **Kreative Erweiterung:** Generiert neue Perspektiven und Metaphern 
- **Kognitive Selbstreflexion:** Identifiziert Denkfehler und blinde Flecken
- **Wissensorganisation:** Hilft bei der Strukturierung und Integration von Wissen

## 🔗 Links

- [GitHub Repository](https://github.com/MushroomFleet/DeepLucid3D-MCP)
- [Smithery.ai Server](https://smithery.ai/server/@MushroomFleet/deeplucid3d-mcp)