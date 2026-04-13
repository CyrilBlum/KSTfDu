---
layout: default
title: Informatik
nav_order: 3
---

# Informatik

Programme für den Informatikunterricht. Alle Programme werden im Rahmen des BYOD-Konzepts auf dem persönlichen Gerät der Schülerinnen installiert.

## Ansprechpersonen

| Programm | Ansprechperson |
|---|---|
| VS Code, Python, pip, Git, Anaconda, Jupyter Notebook, SQLite, Filius | Cyril Blum |

---

## Homebrew (nur macOS – Voraussetzung)

Homebrew ist der Paketmanager für macOS und wird für alle folgenden Installationen benötigt. Falls noch nicht installiert:

Öffne ein Terminal (*Cmd + Leertaste → "Terminal"*) und führe aus:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Folge danach den Hinweisen zur PATH-Konfiguration, die im Terminal angezeigt werden.

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

SQLite ist ein leichtgewichtiges, serverloses Datenbanksystem. Es wird automatisch mit Python mitgeliefert und ist auf macOS vorinstalliert.

### macOS

SQLite ist auf macOS bereits vorinstalliert. Für die Kommandozeile:

```bash
brew install sqlite
```

### Windows

SQLite ist im Python-Paket enthalten. Für die eigenständige SQLite-Shell: Download unter [sqlite.org/download.html](https://www.sqlite.org/download.html).

---

## Filius

Filius ist eine Netzwerksimulationssoftware für den Unterricht. Sie ermöglicht das Erstellen und Testen von Netzwerken.

### macOS und Windows

Filius ist nicht über Homebrew oder winget verfügbar. Download unter:

[lernsoftware-filius.de](https://www.lernsoftware-filius.de)

Dort die aktuelle Version für das jeweilige Betriebssystem herunterladen und installieren.
