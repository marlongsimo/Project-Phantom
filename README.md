# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story, angesiedelt bei der fiktiven **Kreisbank Hohenbrück** (kein reales Institut). Er spielt fast vollständig auf einem nachgebauten PC. Freitag, 15:40 Uhr: Senior-Analyst Matthias Weber war an etwas Großem dran und ist verschwunden. Um 16:30 Uhr startet der Buchungslauf – und mit ihm eine Zahlung über 3,8 Mio. Euro an die Northbridge S.A. in Panama.

Der Name Northbridge steht auf keiner Sanktionsliste. Erst die Ermittlung zeigt, wem die Firma gehört: Bargeld-Weiterleitungen im AML-Monitor und eine umgeleitete Lieferantenzahlung im FraudDesk führen zu Nova Trade Ltd. – gleiche Adresse, gleicher Geschäftsführer wie Northbridge. Die Handelsregister im Browser decken die Kette auf: Northbridge und Nova Trade gehören zu 100 % der Aurelius Global Holdings, die wiederum der gelisteten Aurelius Industrial Group PJSC gehört. Mit diesem Befund wird die Muttergesellschaft im EmbargoCheck geprüft und PHANTOME im ZV-Cockpit gestoppt. Zum Schluss deckt das Team auf, wer im Haus geholfen hat: ein Mitarbeiter des Zahlungsverkehrs, der Weber mit einer gefälschten Vorstandsmail weggelockt und dessen entsperrten PC benutzt hat.

**Stufe Ermittler (aktiv):** Webers Notizen sind persönliche Arbeitsspuren ohne Arbeitsaufträge; keine Schrittanzeige, kein automatisches Protokoll, das Team führt ein eigenes Ermittlungsjournal (Registerauszüge lassen sich aus dem Browser übernehmen). Kennwörter der Notizen lassen sich jederzeit eingeben; falsche Kennwörter haben keine Folgen; an jedem Schloss gibt es einen kostenlosen Kennworthinweis. Statt Punkten zählt die Zeit: Über „Hilfe anfordern“ antwortet nach einer Bestätigung eine Fachkollegin oder ein Fachkollege per Mail mit einem Hinweis passend zum aktuellen Stand; jede Anfrage lässt die Uhr um 3 Minuten vorrücken. Am Ende steht ein Ermittlungsbericht.

**Stufe Azubi (abgeschaltet):** Der Code ist noch enthalten (`AZUBI_AKTIV = true` in `index.html`), folgt aber dem früheren Fall (Northbridge als direkter Listentreffer, Freigabecode 362). Vor einer Reaktivierung müssen Notizen, Hinweise und Ablauf an den neuen Fall angepasst werden.

<details><summary>Lösung für Spielleitung (Ermittler)</summary>

1. Notizen → Eintrag 14:52 lesen (offen). ZV-Cockpit → Zeile PHANTOME: Northbridge S.A., Calle 50, Torre Ámbar, Of. 1207, Panama-Stadt, Registernummer 155-690-1207. Notiz 15:03: **1207**.
2. EmbargoCheck „Northbridge“ → kein Treffer (Namensabgleich prüft keine Eigentümer). Ein Stopp ist erst mit abgeschlossener Sanktionsprüfung möglich.
3. AML-Monitor: Rolf Hansen, Bäckerei Sommer, Lea M. → schließen. Jonas K. → auffällig, 6 Buchungen markieren (Bareinzahlungen und Überweisungen an Nova Trade), Gegenpartei: gleiche Adresse wie Northbridge S.A., „Vertiefte Prüfung, an den Geldwäschebeauftragten“. Notiz 15:17: 9.600 + 9.700 + 4.750 = **24050**.
4. FraudDesk: je Zahlung VoP, Akte, Kontoumsätze. Nordlicht IT = Weiterbearbeiten; Mira Energie (VoP: Kontoinhaber Nova Trade Ltd., Änderung durch s.kranz ohne Rückruf) = Nicht ausführen + eskalieren; Stadtwerke West = Klären; Sparbank = Weiterbearbeiten. Notiz 15:25: 48.750 € → **487**.
5. Browser: „Northbridge“ → Register: Eigentümer nicht offengelegt (Treuhänder). „Nova Trade“ → Register: gleiche Adresse, gleicher Geschäftsführer, Eigentümerin Aurelius Global Holdings Ltd. (100 %). „Aurelius Global Holdings“ → hält 100 % an Nova Trade und – treuhänderisch über Istmo Nominees – 100 % an Northbridge; gehört zu 100 % der Aurelius Industrial Group PJSC. Die Recherche gilt als erledigt, wenn die Auszüge von Nova Trade, Holding und Muttergesellschaft geöffnet wurden. Deren Profil: ul. Zavodskaya 17, Jekaterinburg, Russland, OGRN 1156658044171. (Gesucht wird nur nach Firmennamen.)
6. EmbargoCheck „Aurelius“: SAN-4417 = echter Treffer; SAN-2207, SAN-3871, SAN-5150 = Fehlalarm; SAN-4790 = nicht eindeutig. Ergebnis: „Treffer bestätigt – PHANTOME mittelbar sanktionsbetroffen“.
7. ZV-Cockpit → „Compliance-Stopp setzen“: Prüfbefund liegt vor, Vermerk (mind. 20 Zeichen, kein Abgleich) → Musterbegründung zum Vergleich. Der Stopp wirkt sofort (PHANTOME ist aus dem Lauf genommen). Danach „eskalieren und über -1200 prüfen“ – ohne Eskalation endet das Spiel als Teilerfolg.
8. Phase 2: Kopfzeilen der Vorstandsmails → PC-ZV-114 → Intranet: Sven Kranz, Anmeldeprotokoll s.kranz 13:02–15:41; „Gesendet“ 15:31. Dazu aus Phase 1: Mira-Kontoänderung durch s.kranz (FraudDesk) und 1. Freigabe von PHANTOME über zv.batch07 an PC-ZV-114 (ZV-Cockpit). Das Hinweisgebersystem öffnet nach diesen fünf Spuren; Sven Kranz melden. Zwei Versuche.

Der Spielstand wird im Browser gespeichert; nach versehentlichem Neuladen kann das Team fortsetzen.
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
