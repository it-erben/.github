# .github

Organisationsprofil von [it-erben](https://github.com/it-erben) auf GitHub.

`profile/README.md` erscheint auf der Startseite der Organisation und trägt
den Kurskatalog samt Lizenzhinweis.

`default.json` ist die geteilte Renovate-Konfiguration. Sie aktualisiert
GitHub Actions, Maven, Gradle, npm, NuGet, pip-Requirements, Dockerfiles,
Docker Compose, Helm, Terraform und pre-commit-Hooks. Minor- und
Patch-Anhebungen außerhalb der Workflows bündelt sie je Repository in einem
Pull Request, Major-Anhebungen kommen einzeln. Anhebungen von `it-erben/ci`
merged sie ohne Zutun. Kubernetes-Manifeste und Versionsangaben in
Markdown erfasst sie nicht. Das Dependency Dashboard ist aus, weil in allen
Repositories die Issues abgeschaltet sind. Repositories binden die
Konfiguration so ein:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>it-erben/.github"]
}
```
