---
layout: default
title: Alle Fächer
parent: Fachschaften
nav_order: 1
---

# Alle Fächer

Diese Programme werden in allen Fächern benötigt und müssen von allen Schülerinnen installiert werden.

## Ansprechpersonen

| Programm | Ansprechperson |
|---|---|
| SafeExamBrowser | Cyril Blum (IT) |
| Microsoft 365 | IT |

---

## SafeExamBrowser

SafeExamBrowser ist ein gesicherter Prüfungsbrowser, der während digitalen Prüfungen den Zugriff auf das Internet und andere Programme sperrt.


### macOS

Öffne ein **Terminal**, indem du die Spotlight-Suche mit Cmd + Leertaste öffnest, Terminal eingibst und mit Enter bestätigst. 

![Terminal unter macOS öffnen](assets/images/Terminal.png)

Führe danach folgenden Befehl aus:

```bash
brew install --cask safe-exam-browser
```

### Windows

Öffne **PowerShell** als Administrator:

![PowerShell unter Windows als Administrator](assets/images/PowerShell.png)

Führe danach folgenden Befehl aus:



```powershell
winget install -e --id ETHZurich.SafeExamBrowser --scope machine --silent --accept-package-agreements --accept-source-agreements
```

---

## Microsoft 365

Microsoft 365 (Word, Excel, PowerPoint, Teams usw.) steht als Webanwendung unter [office.com](https://www.office.com) zur Verfügung und kann zusätzlich lokal installiert werden.

- **Webzugang:** [office.com](https://www.office.com) – Login mit der schulischen E-Mail-Adresse

### macOS

```bash
brew install --cask microsoft-office
```

Danach müssen Sie sich mit der schulischen E-Mail-Adresse anmelden, um die Lizenz zu aktivieren.

### Windows

```powershell
winget install -e --id Microsoft.Office --scope machine --silent --accept-package-agreements --accept-source-agreements
```

Danach müssen Sie sich mit der schulischen E-Mail-Adresse anmelden, um die Lizenz zu aktivieren.
