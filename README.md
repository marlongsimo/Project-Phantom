# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story, der fast vollständig auf einem nachgebauten PC spielt. Freitag, 15:40 Uhr: Senior-Analyst Matthias Weber war an etwas Großem dran und ist verschwunden. Um 16:30 Uhr startet der Buchungslauf – und mit ihm eine Zahlung über 3,8 Mio. Euro an eine Firma auf der Sanktionsliste.

Der rote Faden sind Webers Notizen: Notiz 1 ist offen und nennt den ersten Schritt. Jede richtig abgeschlossene Prüfung (EmbargoCheck, AML-Monitor, FraudDesk) erzeugt eine Vorgangsnummer, die die nächste Notiz entsperrt. Notiz 4 enthält den Freigabecode für den Compliance-Stopp im ZV-Cockpit. Zum Schluss deckt das Team auf, wer im Haus geholfen hat: ein Mitarbeiter des Zahlungsverkehrs, der Weber mit einer gefälschten Vorstandsmail weggelockt und dessen entsperrten PC benutzt hat.

<details><summary>Lösung für Spielleitung</summary>

1. Notizen → Notiz 1 lesen.
2. ZV-Cockpit → Zeile PHANTOME anklicken: Empfänger Northbridge S.A., Calle 50, Torre Ámbar, Of. 1207, Panama-Stadt, Panama.
3. EmbargoCheck: „Northbridge“ suchen, Treffer öffnen und vergleichen. SAN-4417 als echten Treffer bewerten (SAN-3871 hat das gleiche Land, aber eine andere Adresse) → Vorgang **3108** → öffnet Notiz 2.
4. AML-Monitor, Alert A-2291: Kundenprofil ansehen (kein Bargeld erwartet), unter „Umsätze“ alle Bareinzahlungen und Überweisungen an Nova Trade markieren (6 Buchungen). Unter „Gegenpartei“: Nova Trade teilt die Adresse mit Northbridge S.A.; Abschluss „Vertiefte Prüfung und Meldung an den Geldwäschebeauftragten“ → Vorgang **2604** → öffnet Notiz 3.
5. FraudDesk: bei jeder Zahlung VoP-Abfrage starten und Lieferantenakte öffnen. Nordlicht IT und Stadtwerke West weiterbearbeiten, Mira Energie ablehnen → Vorgang **7190** → öffnet Notiz 4.
6. ZV-Cockpit → PHANTOME → „Compliance-Stopp setzen“: Freigabecode **762**, Vorgangsnummern 3108, 2604, 7190, Gründe „Sanktionstreffer“ und „Geldwäsche über Nova Trade“. Danach „eskalieren und über -1200 prüfen“.
7. Interner Täter: Mail → „Vorstandsmail“ → Kopfzeilen: gesendet von PC-ZV-114. Intranet: PC-ZV-114 gehört Sven Kranz (Zahlungsverkehr). Mail → Gesendet: 15:31 ging von Webers entsperrtem PC eine Mail an s.kranz, obwohl Weber laut Chat seit 15:26 weg war. Weitere Belege: Mira-Kontoänderung durch s.kranz (FraudDesk), 1. Freigabe von PHANTOME von PC-ZV-114 (ZV-Cockpit).
8. Hinweisgebersystem: Sven Kranz, die vier Belege (nicht Albers/Kuchen), „Meldung an Compliance und Revision, Beweise sichern, PC sperren, Person nicht ansprechen“.
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
