# KYRO Launcher

Electron + Vite + React + TypeScript launcher for Minecraft Java 1.21.1 with Fabric Loader 0.16.10.

## Requirements
- Windows 10/11 x64
- Node.js 20+ (Node 22 recommended)
- Java 21 x64 installed

## Development
```powershell
npm install
npx concurrently -k "vite --host 127.0.0.1" "wait-on http://127.0.0.1:5173 && npm run build:electron && electron ."
```

## Build installer
```powershell
npm run package
```
The NSIS installer is written to `release/`.

## First launch
1. Enter an offline username in Account.
2. Configure memory and Java in Settings.
3. Click INSTALL CLIENT. The launcher downloads Minecraft 1.21.1 and installs Fabric Loader 0.16.10.
4. Click PLAY NOW.

Game directory: `%APPDATA%\\.kyro`.

Offline mode is a local profile and does not authenticate a Microsoft account or verify game ownership. Java 21 x64 must be installed separately. Network access is required to download Minecraft and Fabric. Test installation and launch on a clean Windows machine before public distribution. Minecraft is a trademark of Mojang Studios; KYRO is independent and unaffiliated.
