---
layout: default
title: Biologie
parent: Fachschaften
nav_order: 3
---

# Biologie

Programme für den Biologieunterricht. Die meisten Programme werden im Rahmen des BYOD-Konzepts auf dem persönlichen Gerät der Schülerinnen installiert.

## Ansprechpersonen

| Programm | Ansprechperson |
|---|---|
| ApE, ImageJ / Fiji, CellProfiler, MEGA, GraphPad Prism, Plickers, Brian | Nadine Ahorn, Benjamin Volkmer |

---

## ApE – A Plasmid Editor

ApE ist ein kostenloser Plasmid-Editor für die Molekularbiologie.

### macOS

```bash
brew install --cask ape
```


### Windows

ApE ist nicht über winget verfügbar. Download unter: [jorgensen.biology.utah.edu/wayned/ape](http://jorgensen.biology.utah.edu/wayned/ape/). Nach dem Download: Das heruntergeladene `zip`-Archiv entpacken, den Ordner in `ApE` umbenennen und diesen, sowie dessen Inhalt, in `C:\Program Files\ApE` verschieben.

---

## ImageJ / Fiji

ImageJ (bzw. die erweiterte Distribution Fiji) ist ein Programm für die (semi-automatische) Bildanalyse.

### macOS

```bash
brew install --cask fiji
```

### Windows

Fiji (ImageJ) ist nicht über winget verfügbar. Download unter: [fiji.sc](https://fiji.sc). Nach dem Download: Die heruntergeladene `zip`-Datei entpacken, den Ordner in `Fiji` umbenennen und diesen, sowie dessen Inhalt, in `C:\Program Files\Fiji` verschieben.

---

## CellProfiler

CellProfiler ist eine Software für die automatische Bildanalyse von Zellen.

### macOS

```bash
brew install --cask cellprofiler
```

### Windows

CellProfiler ist nicht über winget verfügbar. Download unter: [cellprofiler.org](https://cellprofiler.org)

Die Windows-Version herunterladen und installieren.

---

## MEGA

MEGA (Molecular Evolutionary Genetics Analysis) wird für Alignments und phylogenetische Bäume verwendet.

### macOS

```bash
brew install --cask mega
```

### Windows

```powershell
winget install -e --id iGEM.MEGA.12 --scope machine --silent --accept-package-agreements --accept-source-agreements --silent
```

---

## GraphPad Prism

GraphPad Prism ist ein kostenpflichtiges Programm zur Erstellung wissenschaftlicher Grafiken und Statistiken.

### macOS


```bash
brew install --cask prism
```

Download unter: [graphpad.com](https://www.graphpad.com)

### Windows

```powershell
winget install -e --id GraphPad.Prism --scope machine --silent --accept-package-agreements --accept-source-agreements --silent
```

Die Installation erfolgt über eine institutionelle Lizenz. Für den Zugang an die Ansprechpersonen wenden.