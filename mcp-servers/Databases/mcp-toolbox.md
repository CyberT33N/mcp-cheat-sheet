# MCP Toolbox for Databases

[googleapis/genai-toolbox](https://github.com/googleapis/genai-toolbox/tree/main?utm_source=tldrdata)

MCP Toolbox for Databases ist ein Open-Source-MCP-Server für Datenbanken. Er ermöglicht die einfachere, schnellere und sicherere Entwicklung von Tools, indem er Komplexitäten wie Connection Pooling, Authentifizierung und mehr übernimmt.

> **Hinweis:**
> 
> MCP Toolbox for Databases befindet sich derzeit in der Beta-Phase und kann vor der ersten stabilen Version (v1.0) Breaking Changes erfahren.
> 
> Diese Lösung wurde ursprünglich als "Gen AI Toolbox for Databases" bezeichnet, da die anfängliche Entwicklung vor MCP stattfand, wurde aber umbenannt, um mit der kürzlich hinzugefügten MCP-Kompatibilität zu übereinstimmen.

## Warum Toolbox?

Toolbox hilft Ihnen, Gen AI-Tools zu erstellen, mit denen Ihre Agenten auf Daten in Ihrer Datenbank zugreifen können. Toolbox bietet:

- **Vereinfachte Entwicklung:** Integrieren Sie Tools in Ihren Agenten in weniger als 10 Codezeilen, verwenden Sie Tools zwischen mehreren Agenten oder Frameworks wieder und stellen Sie neue Versionen von Tools einfacher bereit.
- **Bessere Leistung:** Best Practices wie Connection Pooling, Authentifizierung und mehr.
- **Verbesserte Sicherheit:** Integrierte Authentifizierung für sichereren Zugriff auf Ihre Daten
- **End-to-End-Beobachtbarkeit:** Vorgefertigte Metriken und Tracing mit integrierter Unterstützung für OpenTelemetry.

## Allgemeine Architektur

Toolbox liegt zwischen dem Orchestrierungsframework Ihrer Anwendung und Ihrer Datenbank und bietet eine Steuerungsebene, die zur Änderung, Verteilung oder Aufrufen von Tools verwendet wird. Es vereinfacht die Verwaltung Ihrer Tools, indem es Ihnen einen zentralen Ort zur Speicherung und Aktualisierung von Tools bietet, sodass Sie Tools zwischen Agenten und Anwendungen teilen und diese Tools aktualisieren können, ohne unbedingt Ihre Anwendung neu bereitstellen zu müssen.

## Erste Schritte

### Installation des Servers

Für die neueste Version überprüfen Sie die Releases-Seite und verwenden Sie die folgenden Anweisungen für Ihr Betriebssystem und Ihre CPU-Architektur.

**Binärdatei:**

Um Toolbox als Binärdatei zu installieren:

```bash
# siehe Releases-Seite für andere Versionen
export VERSION=0.5.0
curl -O https://storage.googleapis.com/genai-toolbox/v$VERSION/linux/amd64/toolbox
chmod +x toolbox
```

**Container-Image:**

**Aus Quellcode kompilieren:**

### Ausführen des Servers

Konfigurieren Sie eine tools.yaml, um Ihre Tools zu definieren, und führen Sie dann toolbox aus, um den Server zu starten:

```bash
./toolbox --tools-file "tools.yaml"
```

Sie können toolbox help für eine vollständige Liste von Flags verwenden! Um den Server zu stoppen, senden Sie ein Terminierungssignal (Strg+C auf den meisten Plattformen).

Für detailliertere Dokumentation zur Bereitstellung in verschiedenen Umgebungen, schauen Sie sich die Ressourcen im How-to-Abschnitt an.

### Integration in Ihre Anwendung

Sobald Ihr Server läuft, können Sie die Tools in Ihre Anwendung laden. Sehen Sie unten die Liste der Client-SDKs für die Verwendung verschiedener Frameworks:

**Core:**

Installieren Sie das Toolbox Core SDK:

```bash
pip install toolbox-core
```

Tools laden:

```python
from toolbox_core import ToolboxClient

# URL aktualisieren, um auf Ihren Server zu zeigen
client = ToolboxClient("http://127.0.0.1:5000")

# diese Tools können an Ihre Anwendung übergeben werden! 
tools = await client.load_toolset("toolset_name")
```

Für detailliertere Anweisungen zur Verwendung des Toolbox Core SDK siehe die README des Projekts.

**LangChain / LangGraph:**

**LlamaIndex:**

## Konfiguration

Die Hauptmethode zur Konfiguration von Toolbox ist über die tools.yaml-Datei. Wenn Sie mehrere Dateien haben, können Sie Toolbox mit dem Flag --tools-file tools.yaml mitteilen, welche geladen werden soll.

Detailliertere Referenzdokumentation zu allen Ressourcentypen finden Sie in den Ressourcen.

### Quellen

Der sources-Abschnitt Ihrer tools.yaml definiert, auf welche Datenquellen Ihre Toolbox zugreifen soll. Die meisten Tools haben mindestens eine Quelle, gegen die sie ausgeführt werden.

```yaml
sources:
  my-pg-source:
    kind: postgres
    host: 127.0.0.1
    port: 5432
    database: toolbox_db
    user: toolbox_user
    password: my-password
```

Für weitere Details zur Konfiguration verschiedener Arten von Quellen, siehe die Quellen.

### Tools

Der tools-Abschnitt einer tools.yaml definiert die Aktionen, die ein Agent ausführen kann: welche Art von Tool es ist, welche Quelle(n) es beeinflusst, welche Parameter es verwendet usw.

```yaml
tools:
  search-hotels-by-name:
    kind: postgres-sql
    source: my-pg-source
    description: Suche nach Hotels basierend auf dem Namen.
    parameters:
      - name: name
        type: string
        description: Der Name des Hotels.
    statement: SELECT * FROM hotels WHERE name ILIKE '%' || $1 || '%';
```

Für weitere Details zur Konfiguration verschiedener Arten von Tools, siehe die Tools.

### Toolsets

Der toolsets-Abschnitt Ihrer tools.yaml ermöglicht es Ihnen, Gruppen von Tools zu definieren, die Sie zusammen laden möchten. Dies kann nützlich sein, um verschiedene Gruppen basierend auf Agent oder Anwendung zu definieren.

```yaml
toolsets:
    my_first_toolset:
        - my_first_tool
        - my_second_tool
    my_second_toolset:
        - my_second_tool
        - my_third_tool
```

Sie können Toolsets nach Namen laden:

```python
# Dies lädt alle Tools
all_tools = client.load_toolset()

# Dies lädt nur die Tools, die in 'my_second_toolset' aufgelistet sind
my_second_toolset = client.load_toolset("my_second_toolset")
```

## Versionierung

Dieses Projekt verwendet semantische Versionierung, einschließlich einer MAJOR.MINOR.PATCH-Versionsnummer, die wie folgt erhöht wird:

- **MAJOR-Version** wenn wir inkompatible API-Änderungen vornehmen
- **MINOR-Version** wenn wir Funktionalität in einer rückwärtskompatiblen Weise hinzufügen
- **PATCH-Version** wenn wir rückwärtskompatible Bugfixes vornehmen

Die öffentliche API, auf die sich dies bezieht, ist das CLI, das mit Toolbox verknüpft ist, die Interaktionen mit offiziellen SDKs und die Definitionen in der tools.yaml-Datei.