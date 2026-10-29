# Projekt Phantome – Compliance Escape Room

Ein Escape Room im Browser mit Story. Freitag, 16:58 Uhr: Senior-Analyst Weber ist verschwunden, ihr seid in seinem Büro eingeschlossen, und um 17:50 Uhr verlassen 3,8 Mio. Euro automatisch die Bank. Untersucht den Raum (Telefon, Kaffeetasse, Aktenschrank, Pinnwand, Papierkorb, Laptop), löst drei Fälle – Sanktionen, Geldwäsche, Fraud – und setzt aus den Codefragmenten den Not-Stopp-Code zusammen.

<details><summary>Lösung für Spielleitung</summary>

1. Anrufbeantworter abhören → Schlüssel unter der Kaffeetasse.
2. Aktenschrank: Viktor Marin, Listen-ID SAN-8839 → A = 7.
3. Papierkorb + Pinnwand → Laptop-Passwort `weber2604`.
4. Kontoanalyse: alle Bareinzahlungen und Überweisungen an Nova Trade Ltd. (6 Buchungen) → B = 6.
5. Posteingang: Domain, Druck/Geheimhaltung/Vier-Augen-Umgehung, MRZ-Prüfung → C = 3.
6. Not-Stopp-Terminal: Reihenfolge WER → WIE → WOMIT = **763**, dann „Not-Stopp bestätigen, dokumentieren, eskalieren, verifizieren“.
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
