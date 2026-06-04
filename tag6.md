# Tag 6 — 04.06.2026

## Was habe ich gelernt?

Design und Inhalt sind trennbar — und genau das macht schnelles Experimentieren möglich. Heute habe ich für zwei Homepages (myflowmotion + AI-Adoption-Studio) jeweils **drei komplett verschiedene Design-Welten** bauen lassen: eine Sketch-Variante, eine 80er-Jahre-"Memphis"-Variante und eine Claude-Stil-Fusion. Der Content blieb in allen drei Versionen identisch.

## Welches Problem hatte ich?

Ein unerwartetes technisches: Die Sub-Agenten, die die Design-Varianten parallel bauen sollten, **durften keine Dateien schreiben** (Schreibrechte verweigert in ihrer Sandbox). Drei Agenten, drei fertige Designs — und keiner konnte sein Ergebnis speichern.

## Wie habe ich es gelöst?

Architektur-Umbau im Workflow: Die Agenten geben ihr fertiges HTML **als Rückgabewert** zurück, und der Haupt-Prozess (der Schreibrechte hat) schreibt die Dateien auf die Festplatte.

```
Vorher:  Agent baut → Agent schreibt Datei ❌
Nachher: Agent baut → gibt HTML zurück → Hauptprozess schreibt ✅
```

Das ist ein Muster, das ich mir merke: Wenn ein Teilprozess etwas nicht darf, lass ihn das Ergebnis liefern und die privilegierte Ebene die Aktion ausführen. Gilt in der KI-Orchestrierung genauso wie in klassischer Software-Architektur (Separation of Concerns).

**Merksatz des Tages:** Drei Varianten parallel kosten kaum mehr als eine — aber die Auswahl macht das Ergebnis doppelt so gut.
