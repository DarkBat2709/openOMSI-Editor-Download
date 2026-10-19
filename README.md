# openOMSI Editor — In-game map editor by DarkBat2709

**[English](#english) · [Deutsch](#deutsch)**

Free, experimental community map editor for openOMSI: edit roads, splines, AI traffic paths, terrain and scenery directly in the game. Requires original OMSI 2 content.

Kostenloser, experimenteller Community-Karteneditor für openOMSI: Straßen, Splines, KI-Fahrwege, Gelände und Objekte direkt im Spiel bearbeiten. Originale OMSI-2-Inhalte werden benötigt.

**[Downloads](https://github.com/DarkBat2709/openOMSI-Editor/releases/tag/v0.8.8-pre)** · **[Video](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.0-pre/openOMSI-Editor-Vorstellung-DE.mp4)** · **[English guide](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-Quick-Guide-EN.pdf)** · **[Deutsche Anleitung](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-Kurzanleitung.pdf)**

## English

### What is openOMSI Editor?

**openOMSI Editor by DarkBat2709** is a free community fork of [openOMSI](https://github.com/openOMSI-org/openOMSI) with extended in-game map-building tools. It combines driving and map editing in the same application. It is an independent community project, not an official openOMSI release.

**Current editor release: 0.8.8-pre**, based on **openOMSI 0.3.33**. Information updated: **19 October 2026**.

### New in 0.8.8-pre

- Movable spline dimensions window for length, radius, curve angle, gradient and absolute start height.
- Live mouse preview before placement, updated as dimensions change; camera movement remains available outside text inputs.
- Edit existing splines numerically and with ordinary tools across existing tile boundaries.
- Four-step roundabout builder: Circle, Approaches, Islands and Finish.
- Per-approach splitter islands with configurable shape, length, width, ring distance and height, including rounded, teardrop and rounded-wedge shapes.
- Concrete kerbs for central and splitter islands; island-aware paths and markings.
- Independently configurable 1–4 ring lanes and approach lanes, with matching AI paths.
- Improved roundabout endpoint connectivity, complete driving curves, exit planning, lookahead and conflict detection to reduce unnecessary repeated laps.
- Free AI path drawing as a chain of sections, with three form handles plus start/end per section; existing endpoint connection mode remains available.
- Editable connection preview, remove-last-point and clear-preview controls. Add before saving, then reload to update traffic.
- Fixed reloading of deleted and reshaped grouped roundabout paths: deleted curves no longer return as short fragments.
- Updated German and English PDF guides, 39 pages each, including new screenshots and the original introduction.

Engine base remains **openOMSI 0.3.33**. Map/aerial-image overlays and automatically generated crossings, signs and traffic lights are not included. AI connections do not generate traffic-light control. Back up maps before updating; save, reload and check traffic after editing.

This project uses the AGPL-3.0-only licence. Exact source and build instructions are linked below.

### Building tools introduced in 0.8.4-pre

Build asphalt and separate markings together, fit a marking to a complete selected road chain, and support terrain across the full road width. Roundabouts now offer outer edge lines, dashed entrance openings and adjustable line insets. Both German and English PDF guides include updated screenshots and instructions. These tools remain included in 0.8.8-pre.

### What can I build and edit?

- Place, move, rotate, copy and delete scenery objects and road splines.
- Connect roads, create junctions and roundabouts.
- Create and edit AI traffic paths, shape curves and add turning connections.
- Shape and paint terrain; create maps and tiles.
- Adjust road heights and gradients for bridges and tunnels, use a work plane and hide terrain while editing. Decks, walls and portals use catalogue assets.
- Use movable editor windows and German or English controls.
- Edit during a driving session and reload the map with the bus and onboard passengers preserved within the limits described in the guides.

### Does official openOMSI already include an editor?

Yes. The official [object editor](https://github.com/openOMSI-org/openOMSI/blob/main/docs/USER_GUIDE.md#object-editor) supports changes to existing scenery objects. Its documentation excludes splines, terrain and adding new objects. DarkBat2709's openOMSI Editor extends map editing with the tools listed above. The projects share the openOMSI foundation; this fork builds on the work of its contributors.

### Download and requirements

- **[Windows x64 portable ZIP](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-windows-x64.zip)** · [SHA256 checksum](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-windows-x64.zip.sha256)

For Windows: extract all files to a new writable folder, double-click `start-editor.cmd`, and configure your original OMSI 2 installation in the launcher. No Python, Rust or administrator rights are required. See `START-HERE.txt` in the ZIP. The package is unsigned; settings and logs may be shared with an existing openOMSI installation.

Ready-to-run **0.8.8-pre packages are available for Linux x64 and Windows x64**. The Linux package requires **glibc 2.39 or newer**. It was built on Linux Mint 22.3. An original OMSI 2 installation with its content is required. OMSI 2, third-party maps and mods are not included.

- **[Linux x64 editor package](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-linux-x64.tar.gz)**
- **[SHA256 checksum](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-linux-x64.tar.gz.sha256)**
- **[English operating guide (PDF)](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-Quick-Guide-EN.pdf)**
- **[German operating guide (PDF)](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-Kurzanleitung.pdf)**

On Linux, extract the archive to a separate folder and run:

```bash
bash start-editor.sh "/path/to/openOMSI-content"
```

Set up the original OMSI 2 installation as described in the guide. Back up your maps before editing. The editor bundles its own engine; updating a separate openOMSI game installation does not update this editor package. GitHub's automatic “Source code” downloads contain source files, not the ready-to-run editor.

Linux and Windows CI builds and automated tests passed for the released source. The Windows ZIP and starter passed clean-extraction self-tests. Fresh Windows VM installation and gameplay testing are still pending.

### Demonstration

The video shows version 0.8.0-pre. Version 0.8.8-pre groups the controls into separate toolboxes; the updated PDF guides show the current layout.

[Watch or download the demonstration video (MP4)](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.0-pre/openOMSI-Editor-Vorstellung-DE.mp4): **3:25 minutes, Full HD, German captions, no audio**. It shows passenger boarding, connecting a road gap, editing AI paths, shaping the landscape and continuing the journey.

## Deutsch

### Was ist der openOMSI Editor?

Der **openOMSI Editor von DarkBat2709** ist ein kostenloser Community-Fork von [openOMSI](https://github.com/openOMSI-org/openOMSI) mit erweiterten Werkzeugen für den Kartenbau direkt im Spiel. Busfahren und Kartenbearbeitung finden im selben Programm statt. Es handelt sich um ein eigenständiges Community-Projekt, keine offizielle openOMSI-Veröffentlichung.

**Aktuelle Editor-Version: 0.8.8-pre**, auf Basis von **openOMSI 0.3.33**. Stand dieser Informationen: **19. Oktober 2026**.

### Neu in 0.8.8-pre

- **Spline-Maße:** Neues verschiebbares Fenster für Länge, Radius, Kurvenwinkel, Steigung und absolute Starthöhe.
- **Spline-Vorschau:** Neue Splines vor dem Platzieren an der Maus ansehen. Geänderte Maße aktualisieren die Vorschau; ein Klick setzt den Spline. Kamerabewegung bleibt außerhalb von Texteingaben verfügbar.
- **Vorhandene Splines bearbeiten:** Maße direkt ändern und danach mit den normalen Werkzeugen weiterarbeiten. Platzieren und Bearbeiten funktionieren auch über vorhandene Kachelgrenzen hinweg.
- **Kreisverkehr-Baukasten:** Bedienung in vier zusammenhängenden Schritten: Kreisform, Zufahrten, Inseln und Ausstattung.
- **Verkehrsinseln je Zufahrt:** Einzeln ein-/ausschalten; Form, Länge, Breite, Abstand zum Ring und Höhe einstellen. Abgerundete Inseln, Tropfen und abgerundete Keile mit Vorlageneinstellung.
- **Bordsteine und Markierungen:** Betonbordsteine an Kreis- und Verkehrsinseln; Fahrwege und Markierungen berücksichtigen die Inselgeometrie.
- **Mehrspurige Kreisverkehre:** 1 bis 4 Spuren auf der Kreisfahrbahn und separat einstellbare Spuranzahl je Zufahrt. KI-Wege passen sich an.
- **KI-Verkehr im Kreisverkehr:** Genauer verbundene Fahrwegenden, zusammenhängende Fahrkurven und geplante Ausfahrten verbessern Fahrverhalten, Vorausschau und Konflikterkennung. Unnötiges mehrfaches Kreisen wurde reduziert.
- **Freie KI-Verbindungen:** Neue Wege abschnittsweise auf der geladenen Fläche zeichnen, ohne zuerst zwei bestehende Anschlüsse wählen zu müssen. Jeder Abschnitt hat drei Formpunkte zusätzlich zu Start und Ende.
- **Verbindungsvorschau:** Formpunkte und Endpunkte ziehen, letzten Abschnitt entfernen oder Vorschau leeren. Erst Hinzufügen übernimmt die Verbindung; anschließend speichern und neu laden.
- **Speichern und Neuladen korrigiert:** Gelöschte Kreisverkehr-Fahrkurven erscheinen nicht mehr als kurze Reststücke. Gespeicherte Formänderungen werden auf die vollständige Fahrkurve angewendet.
- **Anleitungen:** Deutsche und englische PDF mit aktuellen Bildern, neuen KI-Anleitungen, geordneten Kapiteln und wiederhergestellter ursprünglicher Einleitung; jeweils 39 Seiten.

Die openOMSI-Basis bleibt **0.3.33**. Landkarten-/Luftbild-Unterlagen sowie automatisch erzeugte Fußgängerüberwege, Schilder und Ampeln sind noch nicht enthalten. KI-Verbindungen erzeugen keine automatische Ampelsteuerung. Karten vor dem Update sichern und nach Änderungen speichern, neu laden und den Verkehr prüfen.

Das Projekt verwendet die AGPL-3.0-only-Lizenz. Quellstand und Bauanleitung sind unten verlinkt.

### Bauwerkzeuge aus 0.8.4-pre

Asphalt und separate Markierungen gemeinsam formen und weiterbauen; Markierungen an ganze ausgewählte Straßenketten anpassen; Gelände unter der vollständigen Straßenbreite stützen. Kreisverkehre bieten Außenrandlinien, gestrichelte Zufahrten und einstellbare Linienabstände. Beide PDF-Anleitungen enthalten neue Bilder und aktuelle Bedienhinweise. Diese Werkzeuge bleiben in 0.8.8-pre enthalten.

### Was kann ich bauen und bearbeiten?

- Landschaftsobjekte und Straßensplines platzieren, verschieben, drehen, kopieren und löschen.
- Straßen verbinden sowie Kreuzungen und Kreisverkehre erstellen.
- KI-Fahrwege erstellen und bearbeiten, Kurven formen und Abbiegeverbindungen ergänzen.
- Gelände formen und texturieren sowie Karten und Tiles anlegen.
- Straßenhöhen und Steigungen für Brücken und Tunnel einstellen, eine Arbeitsebene verwenden und das Gelände beim Bearbeiten ausblenden. Bauteile, Wände und Portale stammen aus dem Katalog.
- Verschiebbare Editorfenster und deutsche oder englische Bedienung nutzen.
- Während einer Fahrt bauen und die Karte mit Übernahme des Busses und der Fahrgäste im Bus neu laden; Umfang und Grenzen stehen in den Anleitungen.

### Hat das offizielle openOMSI bereits einen Editor?

Ja. Der offizielle [Objekteditor](https://github.com/openOMSI-org/openOMSI/blob/main/docs/USER_GUIDE.md#object-editor) ermöglicht Änderungen an vorhandenen Landschaftsobjekten. Seine Dokumentation schließt Splines, Gelände und das Hinzufügen neuer Objekte aus. Der openOMSI Editor von DarkBat2709 ergänzt die oben beschriebenen Kartenbauwerkzeuge. Dieser Fork baut auf der Arbeit der openOMSI-Mitwirkenden auf.

### Download und Voraussetzungen

- **[Windows x64: portables ZIP](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-windows-x64.zip)** · [SHA256-Prüfsumme](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-windows-x64.zip.sha256)

Unter Windows: Alle Dateien in einen neuen beschreibbaren Ordner entpacken, `start-editor.cmd` doppelt anklicken und im Launcher die originale OMSI-2-Installation einrichten. Python, Rust und Administratorrechte sind nicht erforderlich. Siehe `START-HERE.txt` im ZIP. Das Paket ist nicht signiert; Einstellungen und Logs können mit einer vorhandenen openOMSI-Installation geteilt werden.

Fertige Pakete von **0.8.8-pre stehen für Linux x64 und Windows x64 bereit**. Das Linux-Paket benötigt **glibc 2.39 oder neuer**. Es wurde auf Linux Mint 22.3 gebaut. Eine originale OMSI-2-Installation mit ihren Inhalten wird benötigt. OMSI 2, fremde Karten und Mods sind nicht im Paket enthalten.

- **[Linux-x64-Editorpaket](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-linux-x64.tar.gz)**
- **[SHA256-Prüfsumme](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-0.8.8-pre-linux-x64.tar.gz.sha256)**
- **[Englische Bedienungsanleitung (PDF)](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-Quick-Guide-EN.pdf)**
- **[Deutsche Bedienungsanleitung (PDF)](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.8-pre/openOMSI-Editor-Kurzanleitung.pdf)**

Unter Linux das Archiv in einen eigenen Ordner entpacken und starten:

```bash
bash start-editor.sh "/Pfad/zum/openOMSI-Inhaltsordner"
```

Die originale OMSI-2-Installation gemäß Anleitung einrichten. Karten vor dem Bearbeiten sichern. Der Editor enthält seine eigene Engine; ein Update einer separaten openOMSI-Spielinstallation aktualisiert das Editorpaket nicht. Die automatisch von GitHub angebotenen „Source code“-Archive enthalten Quellcode und sind nicht das startfertige Editorpaket.

Die automatischen Builds und Tests für Linux und Windows sind für den veröffentlichten Quellstand bestanden. Das Windows-ZIP und die Startdatei haben Selbsttests nach frischem Entpacken bestanden. Tests einer frischen Windows-VM-Installation und des Spielbetriebs stehen noch aus.

### Vorstellungsvideo

Das Video zeigt Version 0.8.0-pre. In 0.8.8-pre sind die Bedienelemente in getrennten Werkzeugboxen angeordnet; die aktualisierten PDF-Anleitungen zeigen die aktuelle Oberfläche.

[Vorstellung ansehen oder herunterladen (MP4)](https://github.com/DarkBat2709/openOMSI-Editor/releases/download/v0.8.0-pre/openOMSI-Editor-Vorstellung-DE.mp4): **3:25 Minuten, Full HD, deutsche Einblendungen, ohne Ton**. Zu sehen sind das Aufnehmen von Fahrgästen, das Schließen einer Straßenlücke, das Bearbeiten von KI-Fahrwegen und Landschaft sowie die anschließende Weiterfahrt.

## Source code and feedback / Quellcode und Rückmeldungen

- [Release source / Quellstand beider Pakete: v0.8.8-pre](https://github.com/DarkBat2709/openOMSI-Editor/tree/v0.8.8-pre)
- [All releases / Alle Veröffentlichungen](https://github.com/DarkBat2709/openOMSI-Editor/releases)
- [Report a bug / Fehler melden](https://github.com/DarkBat2709/openOMSI-Editor/issues)

For bug reports, include the editor version, steps to reproduce the problem and a relevant log excerpt.
Bitte bei Fehlerberichten die Editor-Version, Schritte zum Nachstellen und einen passenden Logauszug angeben.

This repository provides downloads and project information. Development takes place in the [editor repository](https://github.com/DarkBat2709/openOMSI-Editor).

Dieses Repository bietet Downloads und Projektinformationen. Die Entwicklung erfolgt im [Editor-Repository](https://github.com/DarkBat2709/openOMSI-Editor).
