# Roo MCP Server Transports: STDIO & SSE

Das Model Context Protocol (MCP) nutzt zwei Haupt-Transportmechanismen für die Kommunikation zwischen Roo Code und MCP-Servern: **STDIO** und **SSE**.

## STDIO (Standard Input/Output) Transport

*   **Funktionsweise:**
    *   Läuft **lokal** auf derselben Maschine wie Roo Code.
    *   Roo Code startet den MCP-Server als Kindprozess.
    *   Kommunikation über Standard-Input (STDIN) und Standard-Output (STDOUT) des Prozesses.
    *   Nachrichten sind JSON-RPC 2.0, durch Newline (`\n`) getrennt.
    *   **Client (Roo) `->` STDIN (Server)**
    *   **Server `->` STDOUT (Client)**
*   **Eigenschaften:**
    *   **Lokal:** Gleiche Maschine.
    *   **Performance:** Sehr geringe Latenz, kein Netzwerk-Overhead.
    *   **Einfachheit:** Direkte Prozesskommunikation.
    *   **Beziehung:** Eins-zu-eins (ein Roo-Client pro Server-Instanz).
    *   **Sicherheit:** Inhärent sicherer, da keine Netzwerkexposition.
*   **Wann verwenden?**
    *   Lokale Integrationen und Tools.
    *   Sicherheitssensitive Operationen.
    *   Sehr geringe Latenzanforderungen.
    *   Szenarien mit einem einzelnen Client.
    *   Kommandozeilen-Tools oder IDE-Erweiterungen.
*   **Beispiel (SDK):**
    ```javascript
    // Server-Seite
    import { Server } from '@modelcontextprotocol/sdk/server/index.js';
    import { StdioServerTransport } from '@modelcontextprotocol/sdk/server/stdio.js';

    const server = new Server({name: 'local-server', version: '1.0.0'});
    // Tools registrieren...
    const transport = new StdioServerTransport(server);
    transport.listen();
    ```

## SSE (Server-Sent Events) Transport

*   **Funktionsweise:**
    *   Läuft auf einem **(entfernten) Server** und kommuniziert über HTTP/HTTPS.
    *   Client (Roo) verbindet sich mit dem SSE-Endpunkt des Servers via `HTTP GET`.
    *   Dies etabliert eine persistente Verbindung für Server-zu-Client Events.
    *   Für Client-zu-Server Kommunikation macht der Client `HTTP POST` Anfragen an einen separaten Endpunkt.
    *   **Zwei Kanäle:**
        1.  **Event Stream (GET):** `Server -> Client` (persistente Updates)
        2.  **Message Endpoint (POST):** `Client -> Server` (Anfragen)
*   **Eigenschaften:**
    *   **Remote-Zugriff:** Kann auf anderer Maschine als Roo Code gehostet werden.
    *   **Skalierbarkeit:** Kann mehrere Client-Verbindungen gleichzeitig bedienen.
    *   **Protokoll:** Standard HTTP/HTTPS.
    *   **Persistenz:** Dauerhafte Verbindung für Server-zu-Client Nachrichten.
    *   **Authentifizierung:** Standard HTTP-Authentifizierungsmechanismen nutzbar.
*   **Wann verwenden?**
    *   Remote-Zugriff über Netzwerke.
    *   Szenarien mit mehreren Clients.
    *   Öffentliche Dienste.
    *   Zentralisierte Tools für viele Benutzer.
    *   Integration mit Web-Services.
*   **Beispiel (SDK mit Express):**
    ```javascript
    // Server-Seite (z.B. mit Express.js)
    import { Server } from '@modelcontextprotocol/sdk/server/index.js';
    import { SSEServerTransport } from '@modelcontextprotocol/sdk/server/sse.js';
    import express from 'express';

    const app = express();
    const server = new Server({name: 'remote-server', version: '1.0.0'});
    // Tools registrieren...
    const transport = new SSEServerTransport(server);
    app.use('/mcp', transport.requestHandler()); // Stellt /events und /message Endpunkte bereit
    app.listen(3000);
    ```

## Bereitstellungsaspekte: Lokal (STDIO) vs. Gehostet (SSE)

| Aspekt                 | STDIO (Lokal)                               | SSE (Gehostet)                                  |
| :--------------------- | :------------------------------------------ | :---------------------------------------------- |
| **Installation**       | Auf jeder Benutzer-Maschine                 | Einmalig auf dem Server                           |
| **Verteilung**         | Installationspakete für OS                  | Ein Deployment bedient viele Clients            |
| **Updates**            | Jede Instanz einzeln aktualisieren          | Zentralisierte Updates für alle                 |
| **Ressourcen**         | Lokale CPU, Speicher, Festplatte            | Server-Ressourcen                               |
| **Zugriffskontrolle**  | Lokale Dateisystemberechtigungen            | Authentifizierungs-/Autorisierungssysteme       |
| **Integration (lokal)**| Einfach mit lokalen Ressourcen             | Komplexer für benutzerspezifische Ressourcen      |
| **Ausführung**         | Startet/Stoppt mit Roo (Kindprozess)        | Läuft als unabhängiger Dienst (oft kontinuierlich) |
| **Abhängigkeiten**     | Auf Benutzer-Maschine installieren          | Auf dem Server verwalten                          |

*   **Hybride Ansätze:** Möglich (z.B. lokaler STDIO-Server als Proxy zu Remote-SSE-Diensten).

## Entscheidungshilfe: STDIO vs. SSE

| Kriterium            | STDIO                               | SSE                                         |
| :------------------- | :---------------------------------- | :------------------------------------------ |
| **Standort**         | Nur lokal                           | Lokal oder entfernt                         |
| **Clients**          | Einzelner Client                    | Mehrere Clients                             |
| **Performance**      | Geringere Latenz                    | Höhere Latenz (Netzwerk-Overhead)           |
| **Setup-Komplexität**| Einfacher                           | Komplexer (benötigt HTTP-Server)            |
| **Sicherheit**       | Inhärent sicherer                   | Benötigt explizite Sicherheitsmaßnahmen     |
| **Netzwerkzugriff**  | Nicht benötigt                      | Erforderlich                                |
| **Skalierbarkeit**   | Limitiert auf lokale Maschine       | Kann über Netzwerk verteilt werden            |
| **Deployment**       | Pro-Benutzer Installation           | Zentralisierte Installation                 |
| **Updates**          | Verteilte Updates                   | Zentralisierte Updates                      |
| **Ressourcennutzung**| Nutzt Client-Ressourcen             | Nutzt Server-Ressourcen                     |
| **Abhängigkeiten**   | Client-seitige Abhängigkeiten       | Server-seitige Abhängigkeiten               |
