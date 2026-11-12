# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack
Statisches HTML/CSS, kein Build-Schritt. `src/` ist ein Klon der Squarespace-Seite www.cyan-it.de (Squarespace-Markup, CSS und JS lokal unter `src/assets/`). Bestätigt vom Nutzer.

## Users
- B2B-Kunden: Entscheider im Mittelstand und in der Industrie (Logistik, Bau, Relocation), die eine individuelle digitale Lösung suchen, entweder als Gesamtprojekt oder als punktuelle Unterstützung.
- Bewerber:innen: Azubis (Fachinformatiker Anwendungsentwicklung/Systemintegration, duales Studium Wirtschaftsinformatik), Werkstudent:innen, Praktikant:innen und erfahrene Entwickler:innen, die den Arbeitgeber in Ruderting prüfen.

Blog-Leser (DevOps, Observability, Architektur) sind ein Nebenpublikum, nicht als Hauptzielgruppe bestätigt.

## Product Purpose
Website der Cyan IT GmbH (Ruderting, Niederbayern, rund 30 Mitarbeitende). Sie soll Kunden zu einem Gespräch führen und Bewerber:innen zur Bewerbung. Der Klon in `src/` dient dem Relaunch: Ablösung von Squarespace durch eine selbst gehostete Seite.

## Positioning
Entwicklung maßgeschneiderter Software (ERP, branchenspezifische Cloud-Anwendungen, Datenanalyse/Big Data/IoT, DevOps) auf Augenhöhe mit den Kunden: "Wir sehen die Welt mit Ihren Augen, aber durch unsere Brille." Beleg dafür sind langjährige Kundenprojekte statt Standardprodukten.

## Operating Context
Leistungen: Softwareentwicklung, Softwarearchitektur, Qualitätssicherung, Anforderungsmanagement, Octopus Deploy/DevOps. Inhalte sind deutschsprachig (de-DE). Kontakt- und Bewerbungsformulare sowie ein Blog (inkl. RSS) gehören zum Funktionsumfang der Live-Seite; im Klon laufen sie nicht.

## Capabilities and Constraints
- Der Klon ist ein statischer Snapshot; Formulare, Warenkorb (`cart.html`) und Squarespace-Laufzeitskripte funktionieren offline nicht. 184 Verweise laden weiter von Squarespace-CDNs.
- Duplikate ohne Entscheidung: `home.html` vs. `index.html`, `leistungen.html` vs. `leistungen-1.html`, `blog.html` vs. `blog/`.
- Offen: Ersatz für Formulare, Hosting-Ziel, Umgang mit Squarespace-Laufzeit-JS.
- Rechtliche Seiten (Impressum, Datenschutz in drei Varianten) müssen erhalten bleiben.

## Brand Commitments
Name "Cyan IT" / "cyan.it", Selbstbezeichnung "Cyantists". Werte laut `unsere-werte.html`: Innovation, Qualität, Fairness/Vielfalt, Lernen, Verantwortung, Team, Transparenz, Individualität, Freude. Tonalität: ehrlich, freundlich, unaufgeregt, effektiv ("Menschen, die ehrlich gute Arbeit machen"). Logos unter `src/assets/images/` (u. a. weißes Logo ohne Claim).

## Evidence on Hand
- Vier Case Studies mit PDFs (`src/assets/documents/`): metron eging (Custom ERP), Liebherr-MCCtec Nenzing (Datenanalyse), ICUnet.Group (SaaS IND, German Innovation Award 2022), aigner business solutions (docu-safe).
- Kundenzitate auf der Startseite (metron eging, Liebherr-MCCtec, ICUnet.Group, aigner).
- Mitarbeiterzitate und Benefits im Jobs-Bereich; Auszeichnungen/Badges (Familienpakt, Charta der Vielfalt, Top-Unternehmen) als Bilder vorhanden.
- Nicht erfinden: Kennzahlen, weitere Kunden, Preise, Zertifizierungen jenseits des Vorhandenen.

## Product Principles
- Vertrauen vor Verkauf: Belege (Case Studies, Zitate) stehen vor Versprechen.
- Zwei Zielgruppen, ein Auftritt: Kunden- und Karrierepfad bleiben klar getrennt auffindbar.
- Inhalte und Tonalität der Live-Seite bleiben Wahrheit; Änderungen an Aussagen nur nach Rückfrage.
- Menschlich und unaufgeregt statt Agentur-Pathos.

## Accessibility & Inclusion
Keine produktspezifische Vorgabe bestätigt. Deutschsprachiges Publikum; Diversity ist ein Markenwert (gendergerechte Sprache wie "Mitarbeiter:innen" beibehalten).
