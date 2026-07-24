# INSIDER.KI — Media Manager

Upload-Werkzeug für Präsentations-Medien.
Live: **https://media.insiderki.ai**

## Was es tut

Zeigt alle Bild- und Videostellen einer Präsentation als Slots, nach Folie
gruppiert. Datei per Drag-and-Drop auf eine Kachel ziehen — sie landet im
Supabase-Bucket `workshop-assets` und wird dem Slot zugeordnet. Die
Präsentation zieht sie beim nächsten Laden automatisch.

## Backend

Supabase-Projekt `ai-governance` (`nblyvxnahkbvtatathbh`)

- `presentations` — eine Zeile pro Präsentation
- `presentation_slots` — eine Zeile pro Bild-/Videostelle
- Bucket `workshop-assets` — die Dateien selbst

## Offener Punkt

Aktuell ohne Login erreichbar (`robots.txt Disallow` + `X-Robots-Tag noindex`,
also nicht in Suchmaschinen). Wer die URL kennt, kann hochladen und löschen.
Nachrüsten: Supabase Auth davorsetzen, RLS-Policies von `anon` auf
`authenticated` umstellen.
