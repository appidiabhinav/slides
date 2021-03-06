# VS Code

## VS Code

<https://code.visualstudio.com>

Open-Source-Entwicklungsumgebung

Unabhängig vom eigentlichen Visual Studio

## VS Code: Ordner öffnen

ganzen Ordner öffnen mit _File_ - _Open Folder_

## VS Code: Datei-Explorer, Split Editor

## VS Code: Terminal

Öffnen und Schließen der Ansicht via _Strg_ + _Ö_

zusätzliches Terminal via Symbol _+_

übernimmt das aktuell geöffnete Verzeichnis

## VS Code - Konfiguration

Via _File - Preferences - Settings_

Eingeteilt in _User Settings_ und _Workspace Settings_

## VS Code - Konfigurationsmöglichkeiten

Empfehlungen:

- Accept Suggestion on Commit Character (Autovervollständigung ohne _Enter_): _deaktivieren_
- Tab Size: _2_ oder _4_

Weitere Möglichkeiten:

- Auto Save
- Format on Save
- Word Wrap
- EOL
- Workbench: Color Theme

## VS Code - Befehle

_F1_ oder _Ctrl_ + _Shift_ + _P_: Befehlspalette

- durchsuchbar
- zeigt Kurzbefehle an

Beispiele für Befehle:

- _Find_
- _Search: Find in Files_
- _Format Document_
- _Toggle line comment_ / _Toggle block comment_
- _Go to definition_ / _Peek definition_ (nur für bestimmte Dateitypen)
- _Rename symbol_ (nur für bestimmte Dateitypen)

## VS Code - Mehrere Textcursor

- _Ctrl_ + _F2_: Mehrere Textcursor setzen
- _Alt_ + Mausklick: Mehrere Textcursor setzen

# VS Code für JavaScript

## VS Code - Extensions für JavaScript

Extensions-Sidebar öffnen: fünftes Symbol auf der linken Seite

mögliche Extensions:

- Prettier (Code-Formatierung)
- ESLint (Linter)

## Prettier

- automatische Code-Formatierung nach strikten Regeln
- für JavaScript, HTML, CSS
- Tastenkürzel: _Alt_ + _Shift_ + _F_

## Prettier

Konfiguration:

z.B. über _.prettierrc.json_:

```json
{
  "singleQuote": true,
  "arrowParens": "always"
}
```

## ESLint

Linter mit mehr Funktionalität als der Standard-Linter von VS Code

## Debugging von JavaScript

Möglichkeiten:

- ein node.js debug Terminal starten; JS Code von dort ausführen
- eine JavaScript-Datei im Debugger von node.js starten (konfiguriert via _launch.json_)
- mit dem Debugger eines Browsers verbinden (konfiguriert via _launch.json_)

aufrufbar mittels des _Run_-Tabs in der Sidebar

## Debugger-Konfiguration

Debugger wird via _.vscode/launch.json_ konfiguriert

Erstellen einer Konfigurationsdatei: In der _Run_-Sidebar, wähle _create a launch.json file_

## Debugging mit node.js

Beispiel eines _launch.json_-Eintrages für node.js:

```json
{
  "name": "Launch Node.js Program",
  "type": "node",
  "request": "launch",
  "skipFiles": ["<node_internals>/**"],
  "program": "${workspaceFolder}/index.js"
}
```

## Debugging im Browser

Beispiele für _launch.json_-Einträge zum Debugging in Browsern:

```json
{
  "name": "Launch Chrome",
  "type": "pwa-chrome",
  "request": "launch",
  "url": "http://localhost:8080",
  "webRoot": "${workspaceFolder}"
}
```

```json
{
  "name": "Launch Edge for React",
  "type": "pwa-msedge",
  "request": "launch",
  "url": "http://localhost:3000"
}
```

# VS Code für Python

## VS Code für Python

**Python-Extension**

Installation:

- Extensions-Sidebar öffnen: fünftes Symbol auf der linken Seite
- Installation der _Python_-Extension

Konfiguration:

- Befehlspalette öffnen (F1)
- Suchen nach "Python: select interpreter"
- Enter
- warten...
- gewünschte Python-Version auswählen

## VS Code - Ausführen von Python-Programmen

grünes Play-Symbol zur Editoransicht

oder

_Debug_ - _Start Without Debugging (Ctrl + F5)_

## VS Code - PyLint

um Fehler in VS Code angezeigt zu bekommen: Installation des Python-Pakets _pylint_

```bash
pip install pylint
```
