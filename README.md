# MaxxiCharge Einstellungen für ioBroker

Dieses Skript ermöglicht die einfache Verwaltung der MaxxiCharge-CCU über ioBroker ab Version 0.42. Es erstellt automatisch die benötigten Datenpunkte und sendet Änderungen direkt an die CCU, um die Konfiguration zu aktualisieren.

## Voraussetzungen

- **ioBroker** ist installiert und läuft.
- Der **JavaScript-Adapter** in ioBroker ist aktiv.
- im Javascript-Adapter unter Einstellung **NPM-Module** muss **axios** eintragen sein.

## Installation

1. **JavaScript-Adapter überprüfen**
   - Öffne ioBroker.
   - Gehe zu **Adapter** und stelle sicher, dass der **JavaScript-Adapter** installiert und aktiv ist.

2. **Skript hinzufügen**
   - Öffne den **JavaScript-Editor** unter **Skripte**.
   - Erstelle ein neues Skript (Typ `JavaScript`).
   - Kopiere den Inhalt des Skripts aus **MaxxiCharge_SetSettings.txt** in den Editor.

3. **Konfiguration anpassen**
   - Passe die IP-Adresse oder den Hostnamen der MaxxiCharge-CCU im Skript an:

     ```javascript
     const config = {
         IP: "maxxi.local", // Ersetze durch die IP-Adresse oder maxxi.local
         namespace: "javascript.0.MaxxiChargeSettings", // Namespace für die Datenpunkte
     };
     ```

4. **Skript starten**
   - Speichere das Skript und aktiviere es.
   - Das Skript erstellt automatisch alle relevanten Datenpunkte unter `javascript.0.MaxxiChargeSettings`.

## Nutzung

- **Werte ändern:**
  - Öffne den **Objekte-Tab** in ioBroker.
  - Navigiere zu `javascript.0.MaxxiChargeSettings`.
  - Ändere die gewünschten Werte direkt in den Datenpunkten.
  - Das Skript validiert die Eingaben und sendet Änderungen automatisch an die MaxxiCharge-CCU.


## Hinweise

- Wenn `maxxi.local` nicht funktioniert, verwende die direkte IP-Adresse der CCU.
- Stelle sicher, dass die MaxxiCharge-CCU und ioBroker im selben Netzwerk sind.

---
