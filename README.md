# StreamRift

> **Watch together. Feel together.**

StreamRift ist eine Chrome Extension, mit der du Streaming-Inhalte perfekt synchronisiert mit Freunden und Familie schaust – egal wo ihr seid. Komplett serverlos, kein Account nötig.

---

## Installation

1. **Diesen Ordner herunterladen** (ZIP entpacken oder Ordner clonen)
2. Chrome öffnen → Adressleiste: `chrome://extensions/`
3. Oben rechts **"Entwicklermodus"** aktivieren
4. **"Entpackte Erweiterung laden"** klicken → diesen Ordner auswählen
5. StreamRift erscheint in der Chrome-Toolbar ✓

> **Hinweis:** Du musst den Schritt nicht wiederholen, wenn du Chrome neu startest. Die Extension bleibt installiert.

---

## Verwendung

### Einen Raum erstellen (Host)

1. Öffne eine Streaming-Seite (Netflix, Prime Video, Disney+, YouTube)
2. Klicke auf das **StreamRift-Symbol** in der Toolbar
3. Klicke auf **"Raum erstellen"**
4. Teile den **6-stelligen Room-Code** mit deinen Freunden
5. Starte das Video – StreamRift übernimmt die Synchronisation

### Einem Raum beitreten (Gast)

1. Öffne dieselbe Streaming-Seite und navigiere zum gleichen Inhalt
2. Klicke auf das **StreamRift-Symbol** in der Toolbar
3. Klicke auf **"Raum beitreten"**
4. Gib den **Room-Code** des Hosts ein
5. Das Video wird automatisch auf den aktuellen Stand des Hosts synchronisiert

### Sync-Verhalten

- **Host steuert alles:** Play, Pause und Sprünge werden sofort an alle Teilnehmer übertragen
- **Automatische Offset-Compensation:** Netzwerklatenzen werden automatisch ausgeglichen (Ziel: < 1 Sekunde Abweichung)
- **Neuer Peer:** Wer dem Raum beitritt, springt automatisch an die aktuelle Position des Hosts

---

## Unterstützte Plattformen

| Plattform | Status |
|-----------|--------|
| Netflix | ✅ Unterstützt |
| Amazon Prime Video | ✅ Unterstützt |
| Disney+ | ✅ Unterstützt |
| YouTube | ✅ Unterstützt |

> Jeder Teilnehmer braucht ein eigenes Abo der jeweiligen Plattform.

---

## Voraussetzungen

- **Google Chrome** (aktuell, Version 88+)
- **Eigenes Abo** bei der jeweiligen Streaming-Plattform
- Alle Teilnehmer öffnen **denselben Inhalt** auf derselben Plattform

---

## Version & Änderungen

**Aktuelle Version: v0.6.0** – 2026-03-10

### Was ist neu in v0.6.0?

deploy: Host-Transfer + Bug-Fixes deployen — v0.6.0

Enthält:
- feat: Manueller Host-Transfer (GOODBYE-Event, ArrowRightLeft-Button)
- fix: Host-ContentURL bei Peer-Join korrekt übertragen (cachedContentUrlMessage)
- fix: Zombie-Host verhindern wenn letzter Peer allein bleibt
- fix: Teilnehmerliste bei Verlassen sofort aktualisieren (GOODBYE-Event)
- fix: HOST_TRANSFER Absender verifizieren (BUG-2 Security)
- fix: Host-Badge nach Transfer sofort aktualisieren (BUG-3)

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

Den vollständigen Versionsverlauf findest du im [Entwickler-Repository](https://github.com/marcroelans/StreamRiftDev/blob/main/CHANGELOG.md).

---

## Häufige Fragen

**Warum brauche ich den Entwicklermodus?**
StreamRift ist noch nicht im Chrome Web Store verfügbar. Der Entwicklermodus erlaubt das Laden nicht verifizierter Extensions. Das ist sicher – du lädst nur diesen Ordner.

**Funktioniert das auch über VPN oder Firewalls?**
StreamRift nutzt P2P (WebRTC). In manchen Netzwerken (Firmennetze, strenge Firewalls) kann das die Verbindung erschweren. Heimnetzwerke funktionieren in der Regel problemlos.

**Werden meine Videodaten übertragen?**
Nein. StreamRift überträgt ausschließlich Sync-Events (Play, Pause, Zeitstempel). Es werden keine Videodaten übermittelt.

**Was wenn die Synchronisation nicht klappt?**
Alle Teilnehmer können das Popup schließen und neu öffnen. Der Host startet den Raum neu und teilt einen neuen Code.

---

_StreamRift – Open Source, serverlos, kostenlos._
