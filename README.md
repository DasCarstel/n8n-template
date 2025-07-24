# 🚀 n8n Template Collection

Eine Sammlung nützlicher n8n-Workflows für die Automatisierung alltäglicher Aufgaben.

## 📋 Verfügbare Templates

### 1. Notion-To-Do Synchronisation
**Datei:** `Notion-To-Do.json`

Automatisiert die Synchronisation zwischen Notion-Datenbanken und Microsoft To-Do Listen.

#### ✨ Features:
- 🕐 **Planbare Ausführung** - Konfigurierbare Zeitplanung (Mo, Mi, Fr)
- 📝 **Bidirektionale Synchronisation** - Zwischen Notion und Microsoft To-Do
- ⚙️ **Anpassbare Task-Details** - Zeit, Emoji und Name konfigurierbar
- 🔄 **Automatische Statusaktualisierung** - Erledigt-Status wird synchronisiert
- 🛡️ **Robuste Fehlerbehandlung** - 3-5 Versuche mit intelligenten Wartezeiten
- ⏰ **Erinnerungen** - 30 Minuten vor Fälligkeit

#### 🎯 Workflow-Ablauf:
1. **⏰ Schedule Trigger** - Startet zu konfigurierten Zeiten
2. **⚙️ Task-Konfiguration** - Setzt Zeit, Emoji und Namen
3. **📝 Notion Task erstellen** - Erstellt Aufgabe in Notion-Datenbank
4. **⏳ Wartezeit** - 7 Tage bis zur Task-Erstellung
5. **📋 Microsoft To-Do Task erstellen** - Erstellt parallele Aufgabe
6. **🔄 Status-Synchronisation** - Überwacht und synchronisiert Änderungen

## 🔧 Installation & Setup

### Voraussetzungen:
- n8n Installation (Cloud oder Self-hosted)
- Notion Account mit API-Zugang
- Microsoft To-Do Account
- OAuth-Verbindungen konfiguriert

### Setup-Schritte:

1. **Template importieren**
   ```
   - n8n öffnen
   - "Import from File" wählen  
   - JSON-Datei hochladen
   ```

2. **Credentials konfigurieren**
   - Notion API Credentials einrichten
   - Microsoft To-Do OAuth2 konfigurieren

3. **Template anpassen**
   - Notion-Datenbank ID anpassen
   - Microsoft To-Do Liste ID setzen
   - Zeitplan und Task-Details konfigurieren

## ⚙️ Konfiguration

### Notion-To-Do Template:

#### 🔧 Zu konfigurierende Bereiche:

1. **⏰ Schedule Trigger**
   ```json
   "triggerAtDay": [1, 3, 5]  // Mo, Mi, Fr
   ```

2. **⚙️ Task Details**
   ```json
   "Uhrzeit": 19,      // 19:00 Uhr
   "Emoji": "🚲",      // Task-Icon
   "Name": "Sport"     // Task-Name
   ```

3. **📝 Notion Datenbank**
   ```json
   "databaseId": "YOUR_NOTION_DATABASE_ID"
   ```

4. **📋 Microsoft To-Do Liste**
   ```json
   "taskListId": "YOUR_TODO_LIST_ID"
   ```

5. **Credentials**
   - Notion API Token
   - Microsoft To-Do OAuth2

## 🛡️ Fehlerbehandlung

Alle Templates sind mit robuster Fehlerbehandlung ausgestattet:

- **🔄 Automatische Wiederholung** bei Fehlern
- **⏱️ Intelligente Wartezeiten** zwischen Versuchen
- **📊 Verschiedene Retry-Strategien**:
  - Standard-Operationen: 3 Versuche, 2s Wartezeit
  - API-intensive Operationen: 5 Versuche, 5s Wartezeit
- **🔀 Workflow-Fortsetzung** auch bei Einzelfehlern

## 📚 Verwendung

### Notion-To-Do Workflow:

1. **Erste Einrichtung:**
   - Template importieren
   - Credentials konfigurieren
   - Datenbank/Listen-IDs setzen
   - Task-Details anpassen

2. **Aktivierung:**
   - Workflow aktivieren
   - Ersten Test-Lauf durchführen
   - Zeitplan überprüfen

3. **Überwachung:**
   - Execution-Log überprüfen
   - Synchronisation validieren
   - Bei Bedarf anpassen

## 🔍 Troubleshooting

### Häufige Probleme:

1. **Credential-Fehler**
   ```
   - API-Keys überprüfen
   - OAuth-Tokens erneuern
   - Berechtigungen kontrollieren
   ```

2. **Datenbank-Zugriff**
   ```
   - Notion-Datenbank ID korrekt?
   - Zugriffsberechtigung vorhanden?
   - Feldnamen richtig geschrieben?
   ```

3. **To-Do Listen-Fehler**
   ```
   - Microsoft To-Do Listen-ID korrekt?
   - OAuth-Berechtigung aktiv?
   - Account-Verbindung ok?
   ```

## 🤝 Beitragen

Weitere Templates sind willkommen! 

### Template-Struktur:
- **Beschreibende Namen** mit Emojis
- **Robuste Fehlerbehandlung** implementiert
- **Konfigurierbare Parameter** dokumentiert
- **README-Dokumentation** aktualisiert

## 📄 Lizenz

Diese Templates stehen unter der MIT-Lizenz zur freien Verfügung.

## 🏷️ Tags

`n8n` `automation` `notion` `microsoft-todo` `workflow` `productivity` `templates`

---

**💡 Tipp:** Starten Sie mit dem Notion-To-Do Template und passen Sie es an Ihre Bedürfnisse an. Weitere Templates folgen!
