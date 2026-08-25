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

Falls `assets/` noch fehlt: den GitHub-Action-Workflow **asset-bridge** einmal
manuell ausführen (Actions → asset-bridge → Run workflow). Er lädt die drei
Dateien aus der Higgsfield-Medienbibliothek und committet sie. Danach kann
`.github/workflows/asset-bridge.yml` gelöscht werden.

## Lokale Vorschau

```
python3 -m http.server 8080
```

Dann http://localhost:8080 im Browser öffnen. (Direktes Doppelklicken von
`index.html` zeigt bewusst den statischen Hero, weil Browser `fetch` auf
file://-URLs blockieren.)

Telefone und Reduced-Motion-Nutzer bekommen einen gestalteten statischen Hero
statt des Scroll-Videos. Die Visuals sind KI-generiert.
