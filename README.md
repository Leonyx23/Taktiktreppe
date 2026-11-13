# Taktiktreppe

Schach-Trainer als Web-App: 22 Eröffnungskurse (Lernen, Wiederholen mit Wiederholungs-Rhythmus, Drill, Zeit, Puzzles, Arena), Analyse der eigenen Chess.com-Partien mit Fehler-Training und Eröffnungsvorschlägen, Taktik-Puzzles in 7 Elo-Stufen und Trainingspartien gegen 7 Bots.

Die Chess.com-Anbindung nutzt die öffentliche Schnittstelle (api.chess.com/pub) mit dem Benutzernamen. Die Analyse läuft im Browser.

Die App ist passwortgeschützt: `index.html` enthält sie nur verschlüsselt (AES-GCM, Schlüssel per PBKDF2 aus dem Passwort).
