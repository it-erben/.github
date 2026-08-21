# Arbeitsregeln

## Ton

- Knapp. Sag, was zu sagen ist, dann Schluss. Kein Vorgeplänkel, keine
  Zusammenfassung des gerade Getanen, kein „gute Frage“, kein Wiederholen der
  Aufgabe.
- Keine Füll-Adjektive (robust, nahtlos, mächtig, umfassend, produktionsreif).
  Knapp sagen, was der Code tut, nicht wie gut er ist. Nicht paraphrasieren, was
  die nächsten Zeilen tun. Stattdessen das WARUM und WIE erklären, wenn das dem
  Verständnis wirklich hilft.
- Docs und READMEs: was es ist, wie man es nutzt, was es bereitstellt. Sonst
  nichts.
- Commit-Nachrichten: conventional-commit, Imperativ, möglichst einzeilig. Den
  Scope richtig wählen — Release-Tooling routet unter Umständen darüber. Breaking
  Changes bekommen ein `!` (`feat(api)!: …`) oder einen `BREAKING CHANGE:`-Footer.
  Betreffzeile ≤ 72 Zeichen, Imperativ („add“, „fix“, nicht „added“, „fixes“).
  Body auf 72 Zeichen umbrechen.
- Kleine, fokussierte Commits bevorzugen. Release-Tooling leitet Versionssprünge
  und Changelog oft aus den Commit-Betreffzeilen ab.
- Keine Ticket-Nummern in Code, Commits oder Docs.
- Kommentare erklären das *Warum*, nicht das *Was*. Code-Kommentare benennen die
  Absicht oder eine Einschränkung, die der Code nicht zeigen kann. Kommentare
  löschen, die den Code nur wiederholen.
- Kommentare und Docs immer als Ganzes betrachten. Nie nur anhängen. Im Kontext
  prüfen und auf den faktischen Stand bringen. Im Zweifel im Code recherchieren.
  Veraltete und aus dem Kontext gefallene Verweise entfernen, ebenso frühere
  Beobachtungen, Schilderungen von Situationen, die zu einer früheren Änderung
  führten, Maschinennamen oder -adressen sowie jede Vermutung über die
  nachgelagerte Nutzung dieses Repos und seiner Artefakte — abgesehen von
  gültigen, aktuellen Beispielen.
- Auf ein anderes Repository oder Projekt nur verweisen, wenn dessen Zustand der
  unmittelbare Grund für die Änderung ist (ein Dependency-Bump, ein eingespielter
  Fix, ein an eine veröffentlichte Version gebundener API-Vertrag). Kontext für
  Reviewer, Dank oder Querverweise gehören in den PR-Thread oder ein Issue, nicht
  in den Commit.
- Deklarative Fakten schreiben. Keine Personalpronomen („ich“, „wir“, „du“).
  Keine Leseransprache: kein „beachte, dass…“, „wie man sieht…“, „wir haben uns
  entschieden…“, „das sollte helfen…“. Hier gilt die Regel ohne Ausnahme —
  dieses Repo enthält kein Lehrmaterial.
- Nicht erzählen. Keine Historie, was zuerst versucht wurde, was scheiterte oder
  welche Alternativen erwogen wurden.
- Keine Füll-Verben ohne Konkretes. „Aufräumen“, „verbessern“, „refactoren“
  allein sagen nichts; entweder die tatsächliche Änderung benennen oder die Zeile
  weglassen.
- Keine Checklisten, keine „Summary“-/„Test plan“-Abschnitte, keine
  Marketing-Sprache, keine Emojis.

## Vor dem Abschluss

- Lint, Tests und Build des Projekts für alles Berührte ausführen.
- `pre-commit run --all-files` laufen lassen und alle Befunde beheben.
- Nicht „fertig“ behaupten, ohne die Prüfung ausgeführt zu haben. Belege vor
  Behauptungen.
- Alle TODO-Marker entfernen, die du in deiner Sitzung hinzugefügt hast, und
  nacharbeiten — oder dem Nutzer sagen, dass ein Follow-up nötig ist. Alle Marker
  und Verweise auf deine eigene Aufgabenliste oder historische Arbeitsschritte
  (P2, P3a, Item 1, Task A usw.) samt ihrer Erzählung entfernen. Wenn wirklich
  etwas offen bleibt, dem Nutzer außerhalb von Code, Docs, Markdown, Kommentaren,
  PR-Beschreibungen, Commit-Nachrichten oder allem anderen in diesem Repo und
  seiner angeschlossenen Pipeline Bescheid geben.

## Aufbau dieses Repos

Dieses Repo trägt genau eine versionierte Datei: `README.md`. GitLab zeigt sie
als Beschreibung der Gruppe `it-erben/gfu` an. Sie nennt, wofür die Gruppe da
ist, und den Lizenzhinweis auf CC BY-NC-SA 4.0.

Kein Kursmaterial, keine Folien, keine Labs. Inhalte gehören in das Repo des
jeweiligen Kurses.

## Fallstricke dieses Repos

- **Die `README.md` ist öffentlich sichtbar.** Sie ist die Landeseite der
  GFU-Gruppe. Keine internen Notizen, keine Kundennamen, keine Preise.
- **Der Lizenzabschnitt ist rechtlich relevant.** Die Nennung von
  CC BY-NC-SA 4.0 und der Vorbehalt für abweichende Vereinbarungen mit
  Auftraggebern bleiben, solange sie nicht ausdrücklich geändert werden
  sollen. Dieselbe Lizenz steht im `footer` der Foliensätze mehrerer
  Kursrepos; eine Änderung hier zieht dort nach.
- **Es gibt keine `.gitlab-ci.yml`.** Nichts wird gebaut, nichts wird
  released. Der Scope einer Commit-Nachricht routet hier nichts.
- **`.pre-commit-config.yaml` ist nicht versioniert.** Sie liegt lokal und
  bringt markdownlint-cli2, yamllint und lychee mit — dieselben Hooks wie in
  den Kursrepos.
