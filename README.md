# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story, der fast vollständig auf einem nachgebauten PC spielt. Freitag, 15:40 Uhr: Senior-Analyst Matthias Weber war an etwas Großem dran und ist verschwunden. Um 16:30 Uhr startet der Buchungslauf – und mit ihm eine Zahlung über 3,8 Mio. Euro, hinter der Geldwäsche und ein Embargoverstoß stecken. Die Teams setzen sich an Webers PC (Mail, Chat, Dokumente, verschlüsselte Notizen, Papierkorb) und arbeiten mit der Prüfsoftware: EmbargoCheck, AML-Monitor, FraudDesk und ZV-Cockpit.

<details><summary>Lösung für Spielleitung</summary>

1. Chat: Weber schreibt, das Notizen-Passwort sei „das, was die vertuschen wollen“.
2. Dokumente → Konnossement: Schiff AURORA STAR, IMO 9387421, Baujahr 2006.
3. EmbargoCheck: Namenssuche ergibt keinen Treffer, die IMO-Nummer 9387421 trifft EMB-4417 „KESTREL“ (Post-it: „Namen kann man ändern. Nummern nicht.“). Bewertung: echter Treffer, eskalieren.
4. Notizen-Passwort: `KESTREL`. Die Notizen erklären, wie man den Freigabecode herleitet.
5. AML-Monitor, Alert A-2291: alle Bareinzahlungen und Überweisungen an Nova Trade Ltd. markieren (6 Buchungen).
6. FraudDesk: Nordlicht IT und Stadtwerke West weiterbearbeiten, Überweisung 2 (Mira Energie) ablehnen.
7. ZV-Cockpit → PHANTOME → Freigabecode **762** (EMB-441**7**, **6** Buchungen, Überweisung **2**), dann „Compliance-Stopp bestätigen, dokumentieren, eskalieren, verifizieren“.
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
