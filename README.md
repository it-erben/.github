# .github

Organisationsprofil von [it-erben](https://github.com/it-erben) auf GitHub.

`profile/README.md` erscheint auf der Startseite der Organisation und trägt
den Kurskatalog samt Lizenzhinweis.

`default.json` ist die geteilte Renovate-Konfiguration. Sie aktualisiert
ausschließlich GitHub-Actions-Abhängigkeiten und merged Anhebungen von
`it-erben/ci` ohne Zutun. Das Dependency Dashboard ist aus, weil in allen
Repositories die Issues abgeschaltet sind. Repositories binden die
Konfiguration so ein:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>it-erben/.github"]
}
```
