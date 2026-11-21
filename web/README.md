# Th3inspector Studio integration

This repository now includes a browser-based JavaScript/userscript workbench in `web/`.

## Legacy CLI preserved
The existing Perl CLI, install/update scripts, config assets, and license remain at the repository root and are not replaced by the web application. The legacy CLI contains 19 Perl subroutines and the original menu/flag interface described in the root README.

## Studio
- Bilingual English/Bangla interface.
- Userscript/JavaScript library: import, search (within current list), enable/disable, edit, export and JSON backup/restore.
- JavaScript editor with syntax validation.
- Sandboxed developer console with log/info/warn/error/table capture.
- App-origin network monitor (not cross-tab interception).
- Browser, storage, service worker and performance diagnostics.
- Integration directory for GitHub, Vercel and userscript managers.
- Mobile-responsive single-page interface; no build step.

## Run locally
From the repository root:
```sh
cd web
python -m http.server 8080
```
Open http://127.0.0.1:8080.

## Userscripts
Install Tampermonkey or Violentmonkey in a supported browser, then import a `.user.js` file from the Studio library. The sandbox console does not inject code into other tabs. Full browser DevTools remain browser-native.

## Vercel
The Vercel project root is `web`; it is a static site and requires no build command or environment variables.
