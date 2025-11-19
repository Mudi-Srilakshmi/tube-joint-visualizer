# Packaging (Windows) — Tube Joint Visualizer (2D)

## 1. Install dependencies
Run this command in the project folder:

npm install --save-dev electron@^28.0.0 electron-builder@^24.0.0

If your network is slow or blocks downloads, use:

npm install --save-dev electron electron-builder --fetch-retries=5 --fetch-retry-mintimeout=2000

## 2. Run the app inside Electron (development)
You can preview your app in a desktop window:

npx electron .

## 3. Build Windows EXE installer
Run:

npm run build:win

After this finishes, the installer/EXE will be created in:

dist/
(e.g., dist/Tube-Joint-Visualizer Setup 1.0.0.exe)

## 4. Troubleshooting
- If you get EPERM errors, run PowerShell or VS Code as Administrator.
- If build fails, install NSIS (required by electron-builder):
  https://nsis.sourceforge.io/Download
- If downloads fail, retry with extra flags:
  npm install --save-dev electron electron-builder --fetch-retries=5
