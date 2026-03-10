# Changelog

Alle nennenswerten Änderungen an diesem Projekt werden in dieser Datei dokumentiert.

Das Format ist an [Keep a Changelog](https://keepachangelog.com/de/1.0.0/) angelehnt.

## [Unreleased]

### Delivery modalities UI

**Was**: Neue Ansicht / Komponente zur übersichtlichen Darstellung der Liefermodalitäten

**Warum**: Die Liefermodalitäten (die bisher nur im Standorte-Interface gepflegt werden) werden jetzt strukturiert extrahiert und dem Benutzer sofort sichtbar gemacht. Dadurch sieht man auf einen Blick:

- Erkannte Anlieferzeiten (Wochentage + Samstag)
- Möglichkeit der Samstagsanlieferung (Ja/Nein)
- Nachtanlieferung (Ja/Nein bzw. Nur Nacht / Keine)
- Wichtige Hinweise & Warnungen (z. B. nur Gebrauchtfahrzeuge)

Diese extrahierten Informationen sollen später den **Load Builder** deutlich effizienter und fehlerresistenter machen.

**Wie es aussieht**:

#### 1. Extrahierte / erkannte Werte (Read-only-Ansicht)

![Erkannte Liefermodalitäten – Zusammengefasste Ansicht](https://private-user-images.githubusercontent.com/258/558087360-2ee17ef3-2b04-4ba8-943d-fc280deefc52.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzMxNDM3MzAsIm5iZiI6MTc3MzE0MzQzMCwicGF0aCI6Ii8yNTgvNTU4MDg3MzYwLTJlZTE3ZWYzLTJiMDQtNGJhOC05NDNkLWZjMjgwZGVlZmM1Mi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwMzEwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDMxMFQxMTUwMzBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hZjJlMzBiYjFkYTNmZjgwYWQ1NmU0YmY3YzVhNjEyZmU4NGVhMTA4YjFhOTUyZDhiZjZhNDM5YTIxNjA5OTdhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.Y1QWzABvr5BjY8n7qXknGWIzHtfrrnsfKF7M54r6qpQ) 
<!-- Alternativ: ./screenshots/2026-03-10_erkannt-liefermodalitaeten.png -->

- Anlieferzeiten: Mo–Do 08:00–17:00; Fr 08:00–15:00; Sa 08:00–11:00
- Nachtanlieferung: Keine
- Samstagsanlieferung: Ja
- Zusätzliche Warnung: **NUR GEBRAUCHT-Fahrzeuge**

#### 2. Bearbeitungsansicht (Standort → Bearbeiten)

![Standort-Bearbeitung – Anlieferzeiten und Hinweise](screenshots/standort-bearbeiten-anlieferzeiten.png)
<!-- Alternativ: ./screenshots/2026-03-10_standort-bearbeiten-delivery-settings.png -->

- Flexible Zeiträume (mehrere Blöcke möglich, z. B. Mo–Fr + Sa separat)
- Nachtanlieferung als Auswahl (Nur Nacht / Keine / …)
- Freitext für Anlieferhinweise (z. B. „Nach dem Tor links!")
- Benachrichtigungs-E-Mails (optional)

**Nächste Schritte / Offen**:

- Automatische Validierung der eingegebenen Zeiten gegen die extrahierten Werte
- Integration in den Load Builder (voraussichtlich Q2 2026)
- Optional: visuelle Wochenkalender-Darstellung der Zeiten
