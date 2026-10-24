# Produktions-Workflow Stefania

Stand: 24.10.2026, nach dem Videotest an Reel 001.

## 1. Stills (immer zuerst)
- Erzeugung in Artlist mit **Nano Banana Pro I2I, 4K** (Identity-Edits).
- Ausgangsbild immer der Master: `character/reference/00_master.png`.
- Auto immer aus `character/car/car_v1.png`, Kamera aus `character/props/`.
- STEF-Fingertattoo: nie dem Modell überlassen, siehe `character/props/STEF_METHOD.md`.
- Der Nutzer gibt die Stills frei, **bevor** ein Video gerendert wird.

## 2. Video: Omni statt Kling (Test Reel 001, 24.10.2026)
- **Kling v3 Pro** (1080, ca. 100 Credits/s): verliert die Identität bei Kopfdrehungen
  und frontalen Gesichtern (Gesicht driftet, Mund öffnet sich). Nur für Rückansichten brauchbar.
- **Artlist Omni 1.1** (1080p, 250 Credits/s; 5 s = 1.250, 6 s = 1.500): hält das Gesicht,
  Mund bleibt zu, scharf, echte Drehungen. Urteil des Nutzers: klar besser.
  → **Standard für alle Videos mit sichtbarem Gesicht.**
- Modi: „Interpolation – 1080p“ (Start- + Endframe), „Start Frame only – 1080p“ (ein Bild).
- Format immer **9:16**.
- Omni hat keine Audio-Einstellung, bettet aber eine stumme AAC-Spur ein.
- Bekannte kleine Omni-Fehler, immer prüfen und ggf. retuschieren:
  - Spiegelungen können ein anderes Gesicht zeigen.
  - Zusätzliche Requisiten tauchen auf (z. B. ein Hocker).
  - Kamera-Schriftzug kann sich verändern („XTD“ statt „X-T5“).

## 3. Prompt-Bausteine (an jeden Video-Prompt anhängen)
```
Mouth closed, no talking, no lip movement, no text. Preserve her face, facial
proportions, hair, tattoos (including finger tattoos and the thin vertical line on
the throat), outfit, camera and car exactly. Hyperrealistic skin with visible pores
and natural imperfections, no airbrushed skin. Shot on 35mm analog film
(Kodak Vision3 500T), organic film grain.
```

## 4. Lieferung
- Rohclips einzeln, **ungegradet**, jede Szene separat.
- Der Nutzer gradet selbst (Lightroom/Photoshop), schneidet in CapCut und legt dort den Ton an.
- Keine Rohschnitte, außer ausdrücklich gewünscht.
- Lokales Grading-Skript (`filmlook.py`, „Scorsese warm“) nur als Option.

## 5. Kosten
- Immer zuerst die Kosten nennen; der Nutzer gibt Credits ausdrücklich frei.
- Artlist verlangt vor jeder Generierung einen confirmCost-Schritt.

## 6. Dateien
```
content/reels/<nr>_<name>/
  shotN.png        Stills (Varianten: _fixed, _final_vN …)
  SELECTION.md     freigegebene Shots
  caption.md       Bildunterschrift
  video/           Videos
    artlist_omni/  Omni-Renders
```
- Dateien im Git müssen unter **100 MB** bleiben.
