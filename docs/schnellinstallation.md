---
layout: default
title: Schnellinstallation
nav_order: 2
---

# Schnellinstallation

Diese Seite bündelt die wichtigsten Installationsschritte in je **einem Block für macOS** und **einem Block für Windows**.

> **Hinweis:** Einige Programme sind nicht zuverlässig über `brew` oder `winget` verfügbar und müssen manuell installiert werden (siehe unten).

---

## macOS (Homebrew)

Öffne Terminal und führe den gesamten Block aus:

```bash
echo "========================================"
echo " Schnellinstallation – macOS"
echo "========================================"
echo ""

# Homebrew prüfen
if ! command -v brew >/dev/null 2>&1; then
  echo "❌ Homebrew fehlt. Bitte zuerst installieren: https://brew.sh"
  exit 1
fi

brew update

# Formulas
formulas=(
  git
  python@3.13
)

# Casks
casks=(
  safe-exam-browser
  visual-studio-code
  anaconda
  ape
  fiji
  cellprofiler
  mega
  prism
  musescore
  blender
  adobe-creative-cloud
)

ok=0
fail=0

install_formula () {
  local pkg="$1"
  if brew list "$pkg" >/dev/null 2>&1; then
    echo "✅ $pkg bereits installiert"
    ok=$((ok + 1))
  elif brew install "$pkg"; then
    echo "✅ $pkg installiert"
    ok=$((ok + 1))
  else
    echo "❌ $pkg fehlgeschlagen"
    fail=$((fail + 1))
  fi
}

install_cask () {
  local pkg="$1"
  if brew list --cask "$pkg" >/dev/null 2>&1; then
    echo "✅ $pkg bereits installiert"
    ok=$((ok + 1))
  elif brew install --cask "$pkg"; then
    echo "✅ $pkg installiert"
    ok=$((ok + 1))
  else
    echo "❌ $pkg fehlgeschlagen"
    fail=$((fail + 1))
  fi
}

echo "--- Formulas ---"
for p in "${formulas[@]}"; do install_formula "$p"; done

echo ""
echo "--- Casks ---"
for p in "${casks[@]}"; do install_cask "$p"; done

echo ""
echo "Versuche GeoGebra..."
if brew install --cask geogebra-classic >/dev/null 2>&1 || brew install --cask geogebra >/dev/null 2>&1; then
  echo "✅ GeoGebra installiert"
  ok=$((ok + 1))
else
  echo "❌ GeoGebra nicht via brew installiert (ggf. manuell)"
  fail=$((fail + 1))
fi

echo ""
echo "========================================"
echo " Ergebnis: $ok ✅  erfolgreich, $fail ❌  fehlgeschlagen"
echo "========================================"
```

### Manuell (macOS)

Folgende Programme ggf. manuell installieren (je nach Fach / Lizenz):

- Microsoft 365
- Filius
- ApE
- CellProfiler
- MEGA
- GraphPad Prism
- Matlab
- Ableton
- GarageBand / Logic Pro (App Store)
- Dorico Pro

---

## Windows (winget)

Öffne **PowerShell als Administrator** und führe den gesamten Block aus:

```powershell
Write-Host "========================================" -ForegroundColor Cyan
Write-Host " Schnellinstallation – Windows"         -ForegroundColor Cyan
Write-Host "========================================" -ForegroundColor Cyan
Write-Host ""

$apps = @(
  "ETHZurich.SafeExamBrowser",
  "Microsoft.VisualStudioCode",
  "Python.Python.3.13",
  "Git.Git",
  "GeoGebra.GeoGebra.Classic.6",
  "Musescore.Musescore",
  "BlenderFoundation.Blender",
  "Adobe.CreativeCloud"
)

$ok = 0
$fail = 0

foreach ($id in $apps) {
  Write-Host "Installiere $id ..."
  winget install --id $id -e --accept-package-agreements --accept-source-agreements
  if ($LASTEXITCODE -eq 0) {
    Write-Host "✅ $id" -ForegroundColor Green
    $ok++
  } else {
    Write-Host "❌ $id" -ForegroundColor Red
    $fail++
  }
}

Write-Host ""
Write-Host "========================================" -ForegroundColor Cyan
Write-Host " Ergebnis: $ok ✅  erfolgreich, $fail ❌  fehlgeschlagen" -ForegroundColor Cyan
Write-Host "========================================" -ForegroundColor Cyan
```

### Manuell (Windows)

Folgende Programme ggf. manuell installieren (je nach Fach / Lizenz):

- Microsoft 365
- Filius
- Fiji (ImageJ)
- ApE
- CellProfiler
- MEGA
- GraphPad Prism
- Matlab
- Ableton
- GarageBand / Logic Pro (nur macOS)
- Dorico Pro