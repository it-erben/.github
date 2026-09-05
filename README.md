# .github

Organisationsprofil von [it-erben](https://github.com/it-erben) auf GitHub.

`profile/README.md` erscheint auf der Startseite der Organisation und trägt
den Kurskatalog samt Lizenzhinweis.

`default.json` ist die geteilte Renovate-Konfiguration. Repositories binden
sie so ein:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>it-erben/.github"]
}
```
