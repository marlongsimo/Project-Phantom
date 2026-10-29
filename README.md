# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story, der fast vollständig auf einem nachgebauten PC spielt. Freitag, 15:40 Uhr: Senior-Analyst Matthias Weber war an etwas Großem dran und ist verschwunden. Um 16:30 Uhr startet der Buchungslauf – und mit ihm eine Zahlung über 3,8 Mio. Euro an eine Firma auf der Sanktionsliste.

Der rote Faden sind Webers Notizen: Notiz 1 ist offen und nennt den ersten Schritt. Jede weitere Notiz ist mit einem Rätsel gesperrt, dessen Antwort nur kennt, wer die vorherige Prüfung (EmbargoCheck, AML-Monitor, FraudDesk) wirklich gelöst hat. Auch Webers Freigabecode für den Compliance-Stopp im ZV-Cockpit muss aus den drei Fällen hergeleitet werden. Zum Schluss deckt das Team auf, wer im Haus geholfen hat: ein Mitarbeiter des Zahlungsverkehrs, der Weber mit einer gefälschten Vorstandsmail weggelockt und dessen entsperrten PC benutzt hat.

<details><summary>Lösung für Spielleitung</summary>

1. Notizen → Notiz 1 lesen.
2. ZV-Cockpit → Zeile PHANTOME anklicken: Northbridge S.A., Calle 50, Torre Ámbar, Of. 1207, Panama-Stadt, Panama, Registernummer 155-690-1207.
3. EmbargoCheck: „Northbridge“ suchen und alle fünf Treffer bewerten: SAN-4417 = echter Treffer; SAN-2207, SAN-3871, SAN-5150 = Fehlalarm; SAN-4790 (keine Adresse/Registernummer) = nicht eindeutig. Abschluss: „Zahlung nicht ausführen, dokumentieren, eskalieren“. Notiz 2 öffnet erst danach, Code **4417**.
4. AML-Monitor, Alert A-2291: Kundenprofil ansehen (kein Bargeld erwartet, Filialvermerk „Geschenk der Großmutter“), alle Bareinzahlungen und Überweisungen an Nova Trade markieren (6 Buchungen). Gegenpartei: gleiche Adresse wie Northbridge S.A.; Abschluss „Vertiefte Prüfung, an den Geldwäschebeauftragten“. Notiz 3: 9.600 + 9.700 + 4.750 = **24050**.
5. FraudDesk: bei jeder Zahlung VoP-Abfrage und Lieferantenakte. Nordlicht IT = Weiterbearbeiten, Mira Energie = Nicht ausführen + eskalieren, Stadtwerke West (ähnliche Übereinstimmung, keine Erklärung in der Akte) = Klären. Notiz 4: **102**.
6. ZV-Cockpit → PHANTOME → „Compliance-Stopp setzen“: Freigabecode **362** (3 Fehlalarme, 6 Muster-Buchungen, Überweisung 2 nicht ausgeführt), Grund „Sanktionstreffer“ (trägt den Stopp allein, +100), ergänzend „Geldwäsche über Nova Trade“ (+150 bei beiden). Danach „eskalieren und über -1200 prüfen“.
7. Interner Täter: Kopfzeilen der Vorstandsmails → PC-ZV-114 → Intranet: Sven Kranz. Weitere Spuren: „Gesendet“ 15:31, Mira-Kontoänderung durch s.kranz, 1. Freigabe von PC-ZV-114.
8. Hinweisgebersystem: öffnet erst, wenn Kopfzeilen, Intranet-Zuordnung und „Gesendet“-Mail ausgewertet sind. Dann Sven Kranz auswählen. Zwei Versuche; nach dem zweiten falschen Verdacht ist das Spiel verloren.

Punkte: +250 pro Prüfung, −20 pro Fehlversuch, Hinweise −25 (Denkanstoß) / −50 (konkret), Zeitbonus höchstens 100. Der Spielstand wird im Browser gespeichert; nach versehentlichem Neuladen kann das Team fortsetzen.
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
