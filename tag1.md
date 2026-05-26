# Tag 1 — 26.05.2026

## Was habe ich gelernt?

Git ist keine Backup-Software. Git ist eine Zeitmaschine — und heute habe ich verstanden, warum das einen riesigen Unterschied macht.

Außerdem: Sub-Agenten (KI-Agenten, die im Hintergrund eigenständig arbeiten) brauchen klare Grenzen. Man gibt ihnen entweder einen isolierten Arbeitsbereich (Worktree) oder nur eng begrenzte, additive Aufgaben. Niemals freie Hand über das ganze Projekt.

## Welches Problem hatte ich?

Ich habe einen Hintergrund-Agenten losgeschickt, der eine kleine Aufgabe erledigen sollte — und er hat **mein komplettes Repository umstrukturiert**. Ordner verschoben, Dateien umbenannt, alles durcheinander. Mein erster Impuls: Panik. Stundenlange Arbeit, scheinbar zerstört.

## Wie habe ich es gelöst?

Mit Git. Der Agent hatte vor seiner Umstrukturierung einen Commit gemacht (`1eb18c2`). Ein einziger Befehl hat alles zurückgeholt:

```bash
git reset --hard 1eb18c2
```

Zwei Sekunden statt zwei Tagen Wiederaufbau. Das war der Moment, in dem Git für mich vom "lästigen Pflichttool" zum Sicherheitsnetz wurde.

**Merksatz des Tages:** Committe, bevor du etwas Riskantes tust. Der Commit, den du nicht gemacht hast, ist der, den du brauchst.
