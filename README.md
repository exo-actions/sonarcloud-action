# eXo Sonarcloud Analyse Action

Sonarcloud Analyse Maven project using Github Actions

Usage example:

```yaml
name: Sonarcloud Analyse
on:
  push:
jobs:
  sonarcloud-analyse:
    name: Sonarcloud Build
    runs-on: ubuntu-latest
    timeout-minutes: 120
    steps:
      - name: Sonarcloud Build
        uses: exo-actions/sonar-action@v1
        with:
          maven_version: "3.9.9"
          jdk_major_version: "21"
          jdk_distribution: "zulu"
          SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}
```