# Avec Chaleur — Automatisierungsanalyse

## Projekt

Website für einen Kunden (Avec Chaleur / CYALIZED-AC), die eine Automatisierungsanalyse für Gehaltsprozesse in einem Enterprise-Unternehmen (500+ Mitarbeiter) präsentiert. Statisches HTML/CSS — kein Build-Tool, kein Framework.

## Sprache

- Alle Inhalte sind auf **Deutsch**
- Kommunikation mit dem User auf **Deutsch**

## Tech Stack

- Reines HTML + CSS (+ minimales Vanilla JS für Akkordeons/Tabs)
- Shared Stylesheet: `styles.css`
- Fonts: Cabinet Grotesk (800/700/500/400) + Instrument Serif (italic)
- Kein Build-Prozess, kein Node.js, kein Framework
- Deployment: GitHub → Netlify (manuell per `netlify deploy --prod`)

## Seiten

| Datei | Inhalt |
|---|---|
| `index.html` | Landing Page — 4 Karten zu den Unterseiten |
| `vergleich.html` | Interaktiver 3-Tab-Vergleich (Heute / Ohne Tool / Mit n8n) |
| `technische-analyse.html` | API-Realität & Tool-Stack |
| `enterprise.html` | Datenschutz, 6 Varianten (A–F), DSGVO-Grid, Vergleichstabelle |
| `eigenes-tool.html` | Desktop-App & Web-App als Alternative zu n8n |
| `styles.css` | Shared Design-System (Variablen, Reset, Nav, Typografie) |

## Design-System

- CSS-Variablen in `styles.css`: `--bg: #f0ede8`, `--green: #3a6351`, `--blue: #2d5a87`, `--red: #b5372a`, `--amber: #8a6200`, `--purple: #6b4c8a`
- Max-Width: `720px` (`.wrap`)
- Breakpoint: `560px`
- Cards, Badges, Meter-Bars, Akkordeons als wiederverwendbare Patterns
- Navigation: sticky, blur-backdrop, hamburger auf Mobile

## Deployment

- **GitHub Repo:** https://github.com/CYALIZED-AC/avec-chaleur-automate
- **Netlify Site:** https://avec-chaleur-automate.netlify.app
- **Netlify Site ID:** `908814ac-2cd1-4ebb-8327-8db196d1ab92`
- Deploy-Befehl: `npx netlify-cli deploy --prod --dir=. --site=908814ac-2cd1-4ebb-8327-8db196d1ab92`

## Alte Dateien (nicht im Git)

Die Original-Dateien liegen noch im Projektordner, sind aber nicht committed:
- `automatisierung-enterprise-optionen.html` (Original → enterprise.html)
- `gehaltsaenderung-automatisierung.html` (Original → technische-analyse.html)
- `vergleich-v6.html` (Original → vergleich.html)

## Kontext

- Der Kunde arbeitet in einem Großunternehmen mit eingeschränktem Rechner (kein USB, kein Software-Install, nur Browser)
- Hauptprozess: Gehaltsänderungen in 8 Schritten (Leapsome Review → Personio → Dokument → Freigabe → Upload → Ablage)
- APIs: Leapsome Content API + SCIM, Personio v1 + v2 (Compensations, Documents)
- n8n ist im Enterprise-Kontext schwer umsetzbar (IT-Freigabe, DPIA)
- Eigenes Tool (Desktop-App portable .exe oder Web-App auf Vercel) als Alternative vorgeschlagen
