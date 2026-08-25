# Luginbühl Consulting

Cinematische One-Page-Website für Prozessanalysen und Optimierungen.

**Konzept:** Ein Knoten aus Lichtfäden löst sich beim Scrollen in eine klare Linie auf.
Der Scroll steuert das Hero-Video (Scrub), darunter folgt die eigentliche Seite:
Pains, Leistungen, Vorgehen mit Halte-Interaktion, Über mich, Kompetenzen, FAQ, Kontakt.

## Struktur

- `index.html` – komplette Seite (HTML, CSS, Vanilla-JS, kein Build-Schritt)
- `assets/hero-scrub.mp4` – Scrub-Video (Keyframe-Intervall 8 für sauberes Seeking)
- `assets/hero-poster.jpg` – Erstes Frame (Poster)
- `assets/hero-ending.jpg` – Letztes Frame (statischer Hero, Kontakt-Hintergrund)

## Lokale Vorschau

```
python3 -m http.server 8080
```

Dann http://localhost:8080 im Browser öffnen. (Direktes Doppelklicken von
`index.html` zeigt bewusst den statischen Hero, weil Browser `fetch` auf
file://-URLs blockieren.)

Telefone und Reduced-Motion-Nutzer bekommen einen gestalteten statischen Hero
statt des Scroll-Videos. Die Visuals sind KI-generiert.
