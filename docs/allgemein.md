---
layout: default
title: Alle Fächer
nav_order: 3
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

```bash
brew install --cask safe-exam-browser
```

### Windows

Öffne PowerShell als Administrator und führe folgenden Befehl aus:

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
