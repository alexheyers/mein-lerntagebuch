# Tag 4 — 02.06.2026

## Was habe ich gelernt?

Deployment ist kein Hexenwerk mehr. Heute habe ich zum ersten Mal die **Vercel CLI** installiert, mich eingeloggt und verstanden, wie der Weg vom lokalen Code zur Live-URL aussieht. Dazu: GitHub-Account aufgeräumt (neuer Username `alexheyers`, SSH-Zugang eingerichtet).

Außerdem ein tiefes Three.js-Learning: 3D-Szenen müssen auf **jede Bildschirmgröße** reagieren — was auf meinem Monitor perfekt aussieht, kann auf einem anderen abgeschnitten sein.

## Welches Problem hatte ich?

Auf meiner cinematic Homepage laufen Headlines als Three.js-Partikel-Animationen. Problem: Bei bestimmten Fenster-Seitenverhältnissen wurden **Wörter am Rand abgeschnitten** (Bleed). "STRUKTUR" wurde zu "TRUKTU". Peinlich für eine Bewerbungsseite.

## Wie habe ich es gelöst?

Eine Funktion `fitCamZ()` gebaut (bzw. bauen lassen und verstanden), die den Kamera-Abstand dynamisch berechnet:

```js
// Kamera-Z so skalieren, dass die gemessene halbe
// Wortbreite (o.hw) immer ins Sichtfeld passt —
// abhängig vom aktuellen Seitenverhältnis (aspect)
function fitCamZ(o, aspect) { /* ... */ }
```

Der Kern-Gedanke: Nicht das Wort verkleinern, sondern die Kamera zurückfahren, bis das ganze Wort im Bild ist. Die Messung (`o.hw` = halbe Wortbreite) kommt aus der Szene selbst, nicht aus einer Schätzung.

**Merksatz des Tages:** Teste responsive Verhalten, bevor du deployst — dein Bildschirm ist nicht der Maßstab.
