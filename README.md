# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story, der fast vollständig auf einem nachgebauten PC spielt. Freitag, 15:40 Uhr: Senior-Analyst Matthias Weber war an etwas Großem dran und ist verschwunden. Um 16:30 Uhr startet der Buchungslauf – und mit ihm eine Zahlung über 3,8 Mio. Euro an eine Firma auf der Sanktionsliste.

Der rote Faden sind Webers Notizen: Notiz 1 ist offen und nennt den ersten Schritt. Jede richtig abgeschlossene Prüfung (EmbargoCheck, AML-Monitor, FraudDesk) erzeugt eine Vorgangsnummer, die die nächste Notiz entsperrt. Notiz 4 enthält den Freigabecode für den Compliance-Stopp im ZV-Cockpit.

<details><summary>Lösung für Spielleitung</summary>

1. Notizen → Notiz 1 lesen.
2. EmbargoCheck: SAN-4417 Northbridge S.A. (Name, Adresse und Land passen) → Vorgang **3108** → öffnet Notiz 2.
3. AML-Monitor, Alert A-2291: alle Bareinzahlungen und Überweisungen an Nova Trade Ltd. markieren (6 Buchungen) → Vorgang **2604** → öffnet Notiz 3.
4. FraudDesk: Nordlicht IT und Stadtwerke West weiterbearbeiten, Mira Energie ablehnen → Vorgang **7190** → öffnet Notiz 4.
5. ZV-Cockpit → PHANTOME → Freigabecode **762**, dann „Compliance-Stopp bestätigen, dokumentieren, eskalieren, prüfen“.
</details>

## Lokal testen
1. `index.html` doppelklicken oder in einem aktuellen Browser öffnen.
2. Teamname eingeben und spielen.

## Kostenlos mit GitHub Pages veröffentlichen
1. Bei GitHub anmelden und ein neues Repository erstellen, z. B. `projekt-phantome`.
2. Repository auf **Public** stellen, sofern das mit den internen Vorgaben vereinbar ist. GitHub Pages ist je nach GitHub-Plan und Repository-Einstellungen verfügbar.
3. `index.html` hochladen und committen.
4. Im Repository **Settings → Pages** öffnen.
5. Bei **Build and deployment** als Quelle **Deploy from a branch** wählen.
6. Branch `main` und Ordner `/ (root)` auswählen, dann speichern.
7. Nach der Veröffentlichung die angezeigte Pages-URL öffnen.

## Hinweise
- Die Anwendung ist eine statische Website. Spiellogik und Lösungen liegen im Browsercode und sind daher nicht manipulationssicher.
- Das Spiel speichert keine Teamdaten auf einem Server. Der Ergebnisbutton kopiert eine Zusammenfassung in die Zwischenablage.
- Keine echten Kunden-, Konto-, Verdachts- oder Sanktionsdaten verwenden.
- Vor einer Veröffentlichung oder Nutzung im Bankumfeld die internen Vorgaben zu IT, Datenschutz, Informationssicherheit und externem Hosting prüfen.
- Alle Namen, Unternehmen, Listeneinträge und Transaktionsdaten im Beispiel sind fiktiv.
- Die Falllogik ist ein didaktischer Prototyp, keine verbindliche Rechts- oder Compliance-Anweisung.
