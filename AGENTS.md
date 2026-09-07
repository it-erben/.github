# Arbeitsregeln

Ton, Schreibweise und Commit-Regeln stehen in der Nutzer-Konfiguration
(`~/.claude/CLAUDE.md`, Abschnitte "Schreibweise in deutschen Texten" und
"Arbeitsregeln in Repos"). Hier steht nur, was in diesem Repo dazukommt oder
abweicht.

## Vor dem Abschluss

- `pre-commit run --all-files` laufen lassen und alle Befunde beheben.

## Aufbau dieses Repos

Dieses Repo ist das Organisationsprofil von `it-erben` auf GitHub.

- `profile/README.md` erscheint auf github.com/it-erben. Sie nennt die Kurse
  und den Lizenzhinweis auf CC BY-NC-SA 4.0.
- `default.json` ist die geteilte Renovate-Konfiguration. Die anderen
  Repositories binden sie über `extends: ["local>it-erben/.github"]` ein.
- `renovate.json` schaltet Renovate für dieses Repository ab. Es hat keine
  Abhängigkeiten, ohne die Datei entstünde ein Onboarding-Pull-Request.
- `README.md` beschreibt beides für den Blick ins Repository selbst.

Kein Kursmaterial, keine Folien, keine Labs. Inhalte gehören in das Repo des
jeweiligen Kurses.

## Fallstricke dieses Repos

- **`profile/README.md` ist öffentlich sichtbar.** Sie ist die Startseite der
  Organisation. Keine internen Notizen, keine Kundennamen, keine Preise.
- **Der Lizenzabschnitt ist rechtlich relevant.** Die Nennung von
  CC BY-NC-SA 4.0 und der Vorbehalt für abweichende Vereinbarungen mit
  Auftraggebern bleiben, solange sie nicht ausdrücklich geändert werden
  sollen. Dieselbe Lizenz steht im `footer` der Foliensätze mehrerer
  Kursrepos; eine Änderung hier zieht dort nach.
- **Eine Änderung an `default.json` wirkt sofort auf alle Repositories.**
  Renovate liest den Preset bei jedem Lauf frisch, ohne Version dazwischen.
- **Es gibt keine Pipeline.** Nichts wird gebaut, nichts wird released. Der
  Scope einer Commit-Nachricht routet hier nichts.
- **`.pre-commit-config.yaml` ist nicht versioniert.** Sie liegt lokal und
  bringt markdownlint-cli2, yamllint und lychee mit. Dieselben Hooks wie in
  den Kursrepos.
