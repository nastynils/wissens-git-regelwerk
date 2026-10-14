# Wissens-Git: verdichtetes Teamwissen statt Textablage

Stand: 14.10.2026 · Wiederverwendbare Vorlage für neue Wissens-Repositories.

**Leitgedanke:** Speichere, was die nächste gute Entscheidung erleichtert – nicht alles, was während der Arbeit entstanden ist. So wenig wie möglich, so viel wie für Verständnis, Anwendung und Überprüfung nötig.

## Startbefehl für einen KI-Agenten

Diesen Auftrag zusammen mit dieser Datei im gewünschten Repository verwenden. Es ist ein Prompt, kein installierter Slash-Befehl:

```text
Richte dieses Repository als schlanke, gemeinsame Wissensbasis nach WISSENS-GIT-REGELWERK.md ein bzw. pflege es danach. Prüfe zuerst vorhandene Regeln, Struktur, Git-Stand und thematisch verwandtes Wissen. Bewahre bestehende Konventionen; lege keine parallele Wissensstruktur an. In einem neuen Repo erstelle nur einen kurzen Agenteneinstieg und einen Index; weitere Dateien nur für tatsächlich vorhandenes Wissen. Übernimm ausschließlich belegte, wiederverwendbare Erkenntnisse, Entscheidungen mit Warum und erprobte Vorgehensweisen. Keine Rohchats, Volltranskripte, Daten-Dumps oder Tätigkeitsprotokolle. Ergänze bestehende Aussagen statt sie zu duplizieren. Erhalte Quellen, Geltungsbereich und Unsicherheit. Prüfe den Beitrag und berichte knapp: Wissensgewinn, geänderte Dateien, Prüfungen und Teilungsstatus. Kein Push, Merge oder externe Veröffentlichung ohne entsprechenden Auftrag.
```

## 1. Was ins Repository gehört

Übernimm einen Beitrag nur, wenn er eine spätere Frage beantwortet, eine Entscheidung verbessert oder einen wiederkehrenden Fehler verhindert:

- **Erkenntnis:** belegter Befund mit Geltungsbereich und praktischer Konsequenz.
- **Entscheidung:** was gilt, warum, welche Alternative verworfen wurde und wann neu zu prüfen ist.
- **Vorgehen:** tatsächlich erprobtes Rezept mit Voraussetzungen, Prüfung und bekannten Grenzen.
- **Orientierung:** Zuständigkeiten, Schnittstellen und Quellenorte, soweit für die Zusammenarbeit erforderlich.

**Warum:** Das Repository ist ein gemeinsames Arbeitsgedächtnis, kein Nachweis, wie beschäftigt ein Agent war. „Keine neue Erkenntnis“ ist ein vollwertiges Ergebnis.

Nicht aufnehmen: komplette Chats, Transkripte, E-Mail-Ketten, Terminalausgaben, tägliche Agentenberichte, unbearbeitete Recherchetexte, redundante Zusammenfassungen und fertige Arbeitsprodukte ohne zusätzlichen Wissenswert. Diese bleiben im zuständigen Quellsystem oder Arbeitsprojekt.

**Belege nicht wegkürzen:** Entscheidende Messwerte, Einschränkungen, Gegenbelege und kurze Originalzitate dürfen bleiben. Rohdaten standardmäßig nur referenzieren; eine kleine, unverzichtbare und datenschutzkonforme Reproduktionsprobe nur begründet aufnehmen. Umfangreiche Exporte bleiben außerhalb des Wissens-Gits. Vorhandene Archive nicht ungefragt löschen oder migrieren.

**Warum:** Verdichtung darf weder Nachprüfbarkeit zerstören noch das Repo in ein Datenlager verwandeln.

## 2. Erst finden, dann schreiben

1. Regeln und Index lesen, dann nach Thema, Synonymen und betroffenen Entscheidungen suchen. Nur relevante Dateien nachladen. **Warum:** Ein Index spart Kontext nur, wenn nicht trotzdem das gesamte Repo eingelesen wird.
2. Gleiche Aussage, keine neue Evidenz: nichts anlegen. Neue Evidenz: Quelle und echtes Prüfdatum ergänzen. Teilkorrektur: bestehende Passage ändern. Eigenständiges Thema: neue kompakte Datei. **Warum:** Wissenszuwachs ist wichtiger als Dateizuwachs.
3. Eine Aussage hat einen kanonischen Ort. Andere Abteilungen und Projekte verlinken dorthin. **Warum:** Kopierte Regeln entwickeln widersprüchliche Versionen.
4. Nicht jeden Einzelfehler zur globalen Regel machen. Nur wiederkehrende oder folgenreiche Fehler verallgemeinern, mit Ursache, Schutzregel und Geltungsbereich. **Warum:** Eine Sammlung von Sonderfällen wird selbst zum Kontextproblem.

## 3. Klein beginnen, bei Bedarf gliedern

Bestehende Strukturen respektieren. Für ein leeres Repository genügen zunächst:

- `AGENTS.md`: kurze Arbeitsregeln und Verweis auf dieses Regelwerk und den Index.
- `INDEX.md`: Zweck, Grenzen und Lesepfade „Frage → zuständiges Dokument“.
- Themendateien erst beim ersten echten Beitrag.

Bei wachsendem Bestand nach Informationsbedarf trennen: Referenzen, Anleitungen, Analysen, Entscheidungen. Initiativen nur führen, wenn dieses Repo deren vereinbarter Statusort ist; sonst das zuständige Ticket verlinken. Keine leeren Ordner oder zweite Aufgabenverwaltung auf Vorrat.

**Warum:** Navigation soll Leser unterstützen, nicht eine Organisationsschablone erfüllen. Fachwissen gehört in Themendokumente, nicht vollständig in automatisch geladene Agentenregeln.

**Arbeitsrichtwerte, keine wissenschaftlichen Grenzwerte:** Agenteneinstieg möglichst unter 100 Zeilen; Index als kompakte Wegweisung; normaler Wissensbeitrag etwa 150–500 Wörter. Längere Dokumente sind erlaubt, wenn der zusätzliche Inhalt eine konkrete Frage beantwortet. Dann Kurzfassung voranstellen und Details nur bei Bedarf laden. Niemals wichtige Bedingungen für ein Wortlimit streichen.

Werkzeugspezifische Startdateien verweisen auf denselben Regelbestand, statt ihn zu kopieren. Den tatsächlichen Ladeweg in einer frischen Sitzung prüfen; nicht voraussetzen, dass jeder Agent jede Datei automatisch liest.

## 4. Minimalformat eines Wissensbeitrags

Vorhandene Metadatenschemata weiterverwenden. Ohne Schema genügt diese Vorlage; Platzhalter vor Aufnahme ersetzen:

```markdown
# Aussagekräftiger Titel
Status: Entwurf | gültig | ersetzt
Evidenz: belegt | teilweise belegt | Hypothese
Geltungsbereich: betroffene Systeme / Zielgruppe / Zeitraum
Verantwortlich: bestätigte Person oder Rolle; sonst „ungeklärt“
Zuletzt an Quelle geprüft: Datum oder „noch nicht geprüft“
Erneut prüfen bei: konkretem Auslöser oder begründetem Termin

## Kernaussage
Was wissen oder entscheiden wir? Wenige Sätze.

## Warum und Konsequenz
Wodurch begründet? Was soll künftig anders gemacht werden?

## Belege und Grenzen
Quelle mit Fundstelle und Datenstand; bei Auswertungen Methode/Filter.
Unsicherheit, Gegenbelege und nicht abgedeckte Fälle.
```

**Warum:** Quelle, Aussage und Handlung bleiben verbunden. Metadaten sind kein Selbstzweck; mehr Felder nur, wenn Suche, Prüfung oder Zusammenarbeit sie tatsächlich brauchen.

Beobachtung, Interpretation, Vorschlag und freigegebene Entscheidung ausdrücklich unterscheiden. Ein abgeschlossenes Projekt beweist keine Wirksamkeit. Ein neues Dokument ist nicht automatisch richtiger als ein altes.

## 5. Abteilungsübergreifend nutzbar schreiben

- Gemeinsames Problem und praktische Konsequenz erklären; Fachbegriffe kurz erläutern oder verlinken. **Warum:** Ein Befund aus Technik oder Analyse soll auch Redaktion, Video und Vertrieb helfen.
- Nur belegte Zuständigkeiten nennen. Bei Unklarheit eine Rolle als Vorschlag kennzeichnen, keine Person oder Frist erfinden. **Warum:** Eine Agentenannahme darf kein Mitarbeiterauftrag werden.
- Aufgaben nur aus einem tatsächlichen Auftrag ableiten. Bestehende Tickets verlinken statt hier zu duplizieren. **Warum:** Wissen und Arbeitsfreigabe sind verschieden.
- Vertrauliches weder direkt noch durch verräterische Links weitergeben. Nur für die Repo-Zielgruppe freigegebene Zusammenfassungen übernehmen; Quellzugriff nicht mit Weitergaberecht verwechseln. **Warum:** Gemeinsames Wissen muss die Vertraulichkeitsgrenze jeder Quelle respektieren.

## 6. Aktualität ohne Geschichtsmüll

Teilkorrekturen am kanonischen Ort vornehmen; Git bewahrt den alten Wortlaut. Bei grundlegend ersetzten Entscheidungen oder Befunden eine kurze Ersetzungsmarkierung und den Nachfolger verlinken. Historische Messwerte behalten ihren ursprünglichen Zeitraum. Den Index auf den aktuellen Einstieg richten.

Ungeklärte Widersprüche mit beiden Belegen und der konkreten offenen Frage erhalten; nicht stillschweigend glätten. Überfälliges als prüfbedürftig markieren. Prüfdatum erst nach echter Quellenprüfung ändern.

**Warum:** Historie soll nachvollziehbar bleiben, darf aber nicht als heutige Wahrheit erscheinen. Ein zusätzlicher täglicher Changelog ist nicht nötig; vorhandene Learnings-Logs enthalten kurze Verweise statt nochmals den ganzen Befund.

## 7. Sicher beitragen und ehrlich abschließen

Vor Änderungen Remote, Branch, Arbeitsbaum und aktuellen Remote-Stand prüfen. Ohne Netz die fehlende Aktualitätsprüfung nennen. Fremde Änderungen nicht überschreiben, stashen oder zurücksetzen. Parallele Agenten arbeiten in getrennten Checkouts/Worktrees.

**Warum:** Wissenspflege darf keine laufende Arbeit anderer beschädigen.

Vor Übergabe prüfen:

- Gibt es wirklich neues oder korrigiertes Wissen – und keine Dublette?
- Tragen die Quellen die Aussage einschließlich Geltungsbereich und Einschränkungen?
- Enthält jede neue Regel ihr Warum? Sind Vorschläge als solche erkennbar?
- Funktionieren Dateiverweise? Stimmen Index und gegebenenfalls Ersetzungsverweise?
- Keine Secrets, unzulässigen Personendaten, Rohtextmengen oder unnötigen Kopien?
- Bestehende Repo-Prüfungen ausgeführt und Diff geprüft? Fehlende Prüfer nicht erfinden.

Nur auftragsbezogene Dateien committen. Push und PR nur im erteilten Umfang; Merge nach geltender Freigabe. Bei inhaltlichen Änderungen prüft eine zuständige Person oder ein ausdrücklich autorisierter Review-Prozess die Bedeutung – Formatchecks allein reichen nicht. Keine kostenpflichtigen Dienste oder zusätzlichen Wissenssysteme für diesen Pflegeablauf einführen.

**Warum:** Technisch gültiges Markdown kann fachlich falsch sein. Ein lokaler Beitrag ist noch kein geteiltes Teamwissen.

Abschluss in wenigen Zeilen: **Wissensgewinn / geändert / geprüft / offen / lokal, committet, PR oder gemergt**. Nach Push oder Merge den tatsächlichen Remote-Stand verifizieren. Kein Prozessroman.

## 8. Öffentlich teilen, ohne internes Wissen offenzulegen

Dieses Regelwerk kann als allgemeine Arbeitsvorlage verwendet werden. Die Öffentlichkeit einer Vorlage ist aber keine Freigabe für die später damit erstellten Wissensbeiträge.

Vor einer Veröffentlichung jeden Beitrag auf Firmen-, Personen- und Projekthinweise prüfen – einschließlich Quellenlinks, Dateinamen, Beispielen, Kommentaren und Metadaten. Interne Repository-Adressen, Nutzernamen, Ticketnummern, Commit-IDs, Infrastrukturdetails und vertrauliche Kennzahlen nicht übernehmen. Den fachlichen Zusammenhang als allgemeines Muster erklären; ein abstrahiertes Beispiel ausdrücklich als solches kennzeichnen.

**Warum:** Auch ein nicht öffentlich erreichbarer Link kann vertrauliche Zusammenhänge verraten. Anonymisierung bedeutet mehr, als nur einen Firmennamen zu entfernen.

Interne Belege bleiben im dafür freigegebenen System. Öffentlich nur zugängliche, zur Weitergabe geeignete Quellen zitieren. Ist ein Befund ohne vertraulichen Beleg nicht öffentlich prüfbar, ihn als Empfehlung oder abstrahierte Erfahrung kennzeichnen – nicht als öffentlich nachgewiesene Tatsache. Keine Quellen erfinden, um entfernte interne Nachweise zu ersetzen.

**Warum:** Fachlicher Nutzen und ehrliche Nachprüfbarkeit müssen zusammen erhalten bleiben.

Nur die bereinigte Fassung in ein neues öffentliches Repository übernehmen, nicht versehentlich alte Dateien oder die interne Git-Historie. Bei einem bestehenden Repository auch Historie und weitere Veröffentlichungsflächen prüfen: Das Löschen im aktuellen Dateistand entfernt frühere Inhalte nicht. Rechte zur Weitergabe von Texten und Beispielen klären; für die gewünschte Nachnutzung eine passende Lizenz bewusst festlegen.

**Warum:** Eine saubere aktuelle Datei allein macht weder die gesamte Veröffentlichung vertraulichkeitsfrei noch die Nutzungsrechte eindeutig.

## Begründung und übertragbare Erfahrungen

Dieser Abschnitt erläutert die Gestaltung; er muss nicht bei jeder Fachaufgabe in den Agentenkontext geladen werden. Die Vorlage ist eine praxisorientierte Synthese, kein wissenschaftlich validierter Standard. Identifizierende interne Belege wurden nicht in diese öffentliche Fassung übernommen. Die folgenden Muster sind abstrahierte Empfehlungen, keine Berichte über bestimmte Unternehmen oder Personen.

### Was von gemeinsamer Wissensarbeit erhalten bleiben soll

- **Kleine, überprüfbare Beiträge:** Dublettenprüfung, Quellenstand, sichtbare Ablösung und die Trennung von Projektstatus und Evidenz verhindern, dass Aktivität mit Erkenntnis verwechselt wird.
- **Wissen fließt in beide Richtungen:** Arbeitsprojekte nutzen die gemeinsame Wissensbasis; anschließend geben sie nur neue, wiederverwendbare Erkenntnisse zurück. Fertige Arbeitsprodukte bleiben im Arbeitsprojekt. Ein kurzer Verweis ersetzt eine zweite Kopie.
- **Fachübergreifende Korrekturen:** Ein technischer Befund kann bestehende Annahmen und den Status mehrerer Vorhaben verändern. Daher nicht nur eine neue Analyse hinzufügen, sondern betroffene Aussagen und Einstiege mit korrigieren. Ein Beitrag aus einer anderen Abteilung kann eine strategische Frage beantworten, ohne dass die Abteilung ihre gesamten Arbeitsdaten zentral ablegt.
- **Reproduzierbarkeit ohne Datenlager:** Rohdaten im selben Repository können Nachrechnung erleichtern, erhöhen aber Volumen und Pflegeaufwand. Diese Vorlage entscheidet sich für verlinkte Quellsysteme und nur begründete kleine Reproduktionsproben. Bestehende Archive werden dadurch nicht automatisch zur Migration freigegeben.
- **Navigation muss der Realität entsprechen:** Ein ordentlich formulierter Index ist nutzlos, wenn verlinkte Dateien nicht existieren. Linkziele tatsächlich prüfen; geplante Dokumente nicht als vorhandenes Wissen darstellen.
- **Quellen und Ableitungen trennen:** Eine Zusammenfassung ersetzt nicht ihre Quelle. Fundstellen und Datenstand erhalten; technische Implementierungen oder Modellkonfigurationen eines Quellprojekts nicht ungeprüft als allgemeine Regel übernehmen.
- **Prüfumfang ehrlich benennen:** Eine Dokumentstichprobe ist keine Vollprüfung. Ein aktueller Git-Stand beweist keine fachliche Aktualität. Lokale Sichtung, Abgleich mit dem Remote und Prüfung an der Originalquelle sind unterschiedliche Prüfungen.

### Öffentliche Grundlagen

- **AGENTS.md:** Ein vorhersehbarer Ort für Agentenanweisungen ergänzt die menschenorientierte Projektdokumentation.[1] Diese Vorlage nutzt ihn als kurzen Einstieg, nicht als Sammelbehälter für sämtliches Fachwissen.
- **Context Engineering:** Anthropic empfiehlt den kleinsten hinreichenden Kontext, bedarfsgerechtes Nachladen und aussagekräftige Verdichtung statt maximaler Textmenge.[2] Daraus folgt hier: kurze Orientierung, gezielte Auswahl und Details nur nach Bedarf.
- **Diátaxis:** Dokumentationsformen werden nach Leserbedarf unterschieden, insbesondere Tutorials, Anleitungen, Referenzen und Erklärungen.[3] Daraus folgt keine Pflicht, in jedem kleinen Wissens-Repository sofort alle Kategorien anzulegen.

Die Umfangsrichtwerte in Abschnitt 3 sind praktische Konventionen dieser Vorlage, keine wissenschaftlichen Schwellenwerte oder Vorgaben der verlinkten Quellen. Die öffentlichen Grundlagen wurden am 14.10.2026 abgerufen. Ein Vergleich der Produktivität verschiedener Wissenssysteme oder ein universeller Wirksamkeitsnachweis wurde nicht durchgeführt.

## Sources

[1] https://agents.md
[2] https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
[3] https://diataxis.fr
