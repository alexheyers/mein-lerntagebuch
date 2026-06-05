# Tag 7 — 05.06.2026

## Was habe ich gelernt?

Zwei Dinge:

1. **UX-Entscheidungen brauchen Nutzer-Feedback, keine Entwickler-Logik.** An meiner 3D-System-Map (eine Three.js-"Galaxie" meiner gesamten Infrastruktur mit 48 n8n-Workflow-Satelliten) habe ich das Zoom-Verhalten umgebaut.
2. **Der Git-Workflow, den dieses Repo selbst demonstriert:** Branch anlegen, Änderungen committen, Pull Request öffnen, mergen. Heute zum ersten Mal komplett selbst durchgezogen.

## Welches Problem hatte ich?

Das Mausrad-Zoom in der 3D-Karte war unbrauchbar: Beim Scrollen über die Seite zoomte man versehentlich in die Szene hinein und verlor die Orientierung. Außerdem wirkten die flachen Icons in der 3D-Welt wie Fremdkörper.

## Wie habe ich es gelöst?

1. **Zoom:** Mausrad-Zoom deaktiviert, stattdessen explizite **+/− Buttons**. Weniger "modern", aber vorhersagbar. Der Nutzer entscheidet bewusst, wann er zoomt.
2. **Icons:** Von flachen Sprites auf **3D-Bubbles** umgestellt — jetzt fügen sie sich in die räumliche Szene ein.
3. **Git:** Dieses Lerntagebuch als Übung aufgesetzt — 7 Commits auf `main`, dann ein Feature-Branch für den Wochenrückblick, Pull Request auf GitHub geöffnet und gemergt. Der Aha-Moment: Ein PR ist kein Bürokratie-Ritual, sondern ein **Review-Checkpoint** — selbst wenn man ihn (wie ich) an sich selbst stellt.

**Merksatz des Tages:** Vorhersagbar schlägt beeindruckend — in der UX wie im Git-Workflow.

---

*Woche 1 geschafft. Der Rückblick kommt per Pull Request.* 🎯
