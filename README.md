# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story, angesiedelt bei der fiktiven **Kreisbank Hohenbrück** (kein reales Institut). Er spielt fast vollständig auf einem nachgebauten PC. Freitag, 15:40 Uhr: Senior-Analyst Matthias Weber war an etwas Großem dran und ist verschwunden. Um 16:30 Uhr startet der Buchungslauf – und mit ihm eine Zahlung über 3,8 Mio. Euro an eine Firma auf der Sanktionsliste.

Der rote Faden sind Webers Notizen: Notiz 1 ist offen und nennt den ersten Schritt. Jede weitere Notiz ist mit einem Rätsel gesperrt, dessen Antwort nur kennt, wer die vorherige Prüfung (EmbargoCheck, AML-Monitor, FraudDesk) wirklich gelöst hat. Auch Webers Freigabecode für den Compliance-Stopp im ZV-Cockpit muss aus den drei Fällen hergeleitet werden. Zum Schluss deckt das Team auf, wer im Haus geholfen hat: ein Mitarbeiter des Zahlungsverkehrs, der Weber mit einer gefälschten Vorstandsmail weggelockt und dessen entsperrten PC benutzt hat.

**Zwei Schwierigkeitsstufen:** *Azubi* – Webers Notizen führen Schritt für Schritt, die Seitenleiste zeigt den nächsten Schritt und den Fortschritt. *Ermittler* – Webers Notizen sind persönliche Beobachtungen, ohne Schrittanzeige und automatisches Protokoll; das Team führt ein eigenes Ermittlungsjournal (freie Notizen ohne Vorgaben), Hinweise kosten mehr. Die Fachrätsel sind in beiden Stufen identisch.

<details><summary>Lösung für Spielleitung</summary>

1. Notizen → Webers ersten Eintrag (14:52) lesen.
2. ZV-Cockpit → Zeile PHANTOME anklicken: Northbridge S.A., Calle 50, Torre Ámbar, Of. 1207, Panama-Stadt, Panama, Registernummer 155-690-1207.
3. EmbargoCheck: „Northbridge“ suchen und alle fünf Treffer bewerten: SAN-4417 = echter Treffer; SAN-2207, SAN-3871, SAN-5150 = Fehlalarm; SAN-4790 (keine Adresse/Registernummer) = nicht eindeutig. Abschluss: „Zahlung nicht ausführen, dokumentieren, eskalieren“. Notiz 15:03 öffnet erst danach, Code **4417**.
4. AML-Monitor: Alle vier Alerts bewerten. Rolf Hansen (Ferienwohnung, Vertrag), Bäckerei Sommer (Tageslosung) und Lea M. (Autoverkauf mit Kaufvertrag, Kauf bei Autohaus Krämer) sind erklärt → schließen. Jonas K. → auffällig: Kundenprofil (kein Bargeld erwartet, Filialvermerk „Geschenk der Großmutter“), alle Bareinzahlungen und Überweisungen an Nova Trade markieren (6 Buchungen). Gegenpartei: gleiche Adresse wie Northbridge S.A.; Abschluss „Vertiefte Prüfung, an den Geldwäschebeauftragten“. Webers Notiz 15:17: 9.600 + 9.700 + 4.750 = **24050**.
5. FraudDesk: bei jeder Zahlung VoP-Abfrage, Akte und Kontoumsätze (öffnen sich als eigenes Fenster, 14 Buchungen, darin die relevanten suchen). Nordlicht IT = Weiterbearbeiten; Mira Energie (Umsätze: bisher deutsche IBAN) = Nicht ausführen + eskalieren; Stadtwerke West (ähnliche Übereinstimmung, Umsätze zeigen nur Lastschriften) = Klären; Sparbank (Bankname statt Kontoinhaber, Umsätze: gleiche IBAN mit eigenem Namen) = Weiterbearbeiten. Notiz 15:25: **1021**.
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
