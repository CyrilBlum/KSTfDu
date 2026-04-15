---
layout: default
title: ⭐ Schnellinstallation
nav_order: 3
---

# Schnellinstallation

Diese Seite bündelt die wichtigsten Installationsschritte in je **einem Block für macOS** und **einem Block für Windows**. 
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
  python3
)

# Casks
casks=(
  safe-exam-browser
  adobe-creative-cloud
  blender
  ape
  fiji  
  cellprofiler
  mega
  prism
  visual-studio-code
  filius
  geogebra
  musescore
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
echo "========================================"
echo " Ergebnis: $ok ✅  erfolgreich, $fail ❌  fehlgeschlagen"
echo "========================================"
```

---

## Windows (winget)

Öffne **PowerShell als Administrator** und führe den gesamten Block aus:

```powershell
Write-Host "========================================" -ForegroundColor Cyan
Write-Host " Schnellinstallation – Windows"         -ForegroundColor Cyan
WriFiji.ImageJ",
  "iGEM.MEGA.12",
  "StefanFreischlad.Filius",
  "te-Host "========================================" -ForegroundColor Cyan
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