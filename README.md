# Taktiktreppe

Schach-Trainer als Web-App: 31 Eröffnungskurse (Lernen, Wiederholen mit Wiederholungs-Rhythmus, Drill, Zeit, Puzzles, Arena), Analyse der eigenen Chess.com-Partien mit Fehler-Training und Eröffnungsvorschlägen, Taktik-Puzzles in 7 Elo-Stufen und Trainingspartien gegen 7 Bots.

Die Chess.com-Anbindung nutzt die öffentliche Schnittstelle (api.chess.com/pub) mit dem Benutzernamen. Die Analyse läuft im Browser.

## Stockfish

Die Partie-Analyse nutzt [Stockfish](https://github.com/official-stockfish/Stockfish) 19 als WebAssembly-Build von [stockfish.js](https://github.com/nmrugg/stockfish.js) (Variante „lite, single-threaded“, Dateien im Ordner `sf/`). Stockfish steht unter der GNU General Public License v3, siehe `sf/Copying.txt`; der Quellcode ist unter den beiden Links verfügbar. Die Engine läuft als eigenständiges Programm in einem Web Worker und wird über das UCI-Protokoll angesprochen. Ist sie nicht verfügbar, nimmt die App ihre eingebaute Engine.

Die App ist passwortgeschützt: `index.html` enthält sie nur verschlüsselt (AES-GCM, Schlüssel per PBKDF2 aus dem Passwort).
