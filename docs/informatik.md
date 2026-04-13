---
layout: default
title: Informatik
nav_order: 4
---

# Informatik

Programme für den Informatikunterricht. Alle Programme werden im Rahmen des BYOD-Konzepts auf dem persönlichen Gerät der Schülerinnen installiert.

## Ansprechpersonen

| Programm | Ansprechperson |
|---|---|
| VS Code, Python, pip, Git, Anaconda, Jupyter Notebook, SQLite, Filius | Cyril Blum |

---

## VS Code

Visual Studio Code (VS Code) ist die Entwicklungsumgebung für den Informatikunterricht.

### macOS

```bash
brew install --cask visual-studio-code
```

### Windows

```powershell
winget install -e --id Microsoft.VisualStudioCode --scope machine --silent --accept-package-agreements --accept-source-agreements
```

---

## Python und pip

Python ist die Programmiersprache des Informatikunterrichts. pip (Paketmanager für Python) wird automatisch mitinstalliert.

### macOS

```bash
brew install python3
```

### Windows

```powershell
winget install -e --id Python.Python.3.13 --scope machine --silent --accept-package-agreements --accept-source-agreements
```

---

## Git

Git ist ein Versionskontrollsystem zur Nachverfolgung von Änderungen in Programmierprojekten.

### macOS

```bash
brew install git
```

### Windows

```powershell
winget install -e --id Git.Git --scope machine --silent --accept-package-agreements --accept-source-agreements
```

---

## Anaconda (inkl. Jupyter Notebook)

Anaconda ist eine Python-Distribution für wissenschaftliches Rechnen und Data Science. Sie enthält unter anderem Jupyter Notebook.

### macOS

```bash
brew install --cask anaconda
```

Nach der Installation die PATH-Variable anpassen – Hinweise werden im Terminal angezeigt.

### Windows

```powershell
winget install -e --id Anaconda.Anaconda3 --scope machine --silent --accept-package-agreements --accept-source-agreements
```

---

## SQLite

SQLite ist ein leichtgewichtiges, serverloses Datenbanksystem. Es wird automatisch mit Python mitgeliefert.

### macOS

SQLite ist auf macOS bereits vorinstalliert. Für die Kommandozeile:

```bash
brew install sqlite
```

### Windows

SQLite ist im Python-Paket enthalten und damit bereits verfügbar. Für die eigenständige SQLite-Shell kann die ausführbare Datei manuell unter [sqlite.org/download.html](https://www.sqlite.org/download.html) heruntergeladen werden (keine Installation nötig – ZIP entpacken und `sqlite3.exe` verwenden).

---

## Filius

Filius ist eine Netzwerksimulationssoftware für den Unterricht. Sie ermöglicht das Erstellen und Testen von Netzwerken.

### macOS

Filius ist nicht über Homebrew verfügbar. Download unter:

[lernsoftware-filius.de](https://www.lernsoftware-filius.de)

Die macOS-Version herunterladen und installieren.

### Windows

Filius ist nicht über winget verfügbar. Download unter:

[lernsoftware-filius.de](https://www.lernsoftware-filius.de)

Die Windows-Version herunterladen und installieren.
