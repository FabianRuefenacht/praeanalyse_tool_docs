# Grundlagedaten beziehen

Für die Planung geodätischer Netze werden Grundlagedaten wie Fixpunkte der amtlichen Vermessung benötigt. Für ein effizientes und einfaches Netzdesign sind Höheninformationen – um die Sichtbarkeit oder Abschattung von Punkten zu analysieren – sowie Referenzdaten hilfreich, um sich in der Umgebung des Netzes zurechtzufinden. Im Register ```Grundlagen``` können diese Daten importiert oder aus zentralisierten Quellen bezogen werden.

<img src="../imgs/load_data/loadData.png" width="500" /><br/>
<small>_Abbildung 1: Register Grundlagen._</small>

---

## Fixpunkte aus Textdatei laden

Der Knopf ```Textfile``` ermöglicht den Import eigener Punkte. Diese Punkte können als Referenz- oder Neupunkte im Netzdesign verwendet werden.

Der Datensatz muss folgendes Format haben:

- **Kein Header:** Die erste Zeile muss bereits Punktdaten enthalten.
- **Spaltenformat:** Punktnummer;Ost-Koordinate;Nord-Koordinate;Höhe
- **Trennzeichen:** Semikolon ```;```
- **Fehlende Höhen:** Mit ```0``` als Platzhalter ergänzen.
- **Punktnummern:** Dürfen keine Sonder- oder Leerzeichen enthalten.

---

## Perimeter zeichnen

Der Perimeter bildet die Grundlage für den Bezug öffentlicher Geodaten (Fixpunkte und Oberflächenmodell).

- Klicken Sie auf den Knopf ```Perimeter zeichnen```, um die Zeichenfunktion in QGIS zu aktivieren.
- Der erste Klick in die Zeichenoberfläche setzt die erste Ecke der Bounding-Box. Der zweite Klick schliesst die Bounding-Box.
- Während des Zeichnens wird eine provisorische Bounding-Box als **RubberBand** angezeigt.
- Nach Abschluss des Zeichnens werden die Koordinaten und die Fläche des Perimeters berechnet und in der Plugin-Oberfläche unterhalb des Knopfes angezeigt.
- **Bemerkung:** Wenn Sie einen Skyplot im Rahmen von GNSS-Messungen durchführen möchten, wählen sie den Parameter entsprechend gross.

---

## Fixpunkte (©swisstopo)

Wenn ein Perimeter definiert wurde, können Sie mit Klick auf den Knopf ```Fixpunkte (©swisstopo)``` alle Fixpunkte (LFP1-3 & HFP 1-3) von swisstopo herunterladen. Die Daten stammen aus dem WFS-Dienst von swisstopo [(geodienste.ch)](https://www.geodienste.ch/services/av/info).

**Achtung:** Diese Option ist zum aktuellen Stand (23.03.2025) noch nicht in der ganzen Schweiz verfügbar.

---

## SwissSURFACE3D laden (©swisstopo)

Das Höhenmodell kann für die Sichtbarkeitsanalyse verwendet werden. **Hinweis:** Es kann nur ein Höhenmodell geladen werden.

- Wenn ein Perimeter definiert wurde, können Sie mit Klick auf den Knopf ```SwissSURFACE3D laden (©swisstopo)``` das Oberflächenmodell der Schweiz innerhalb des definierten Perimeters laden. [(swisstopo 2024)](https://www.swisstopo.admin.ch/de/hoehenmodell-swisssurface3d-raster)
- **Wichtig:** Der Download kann je nach Perimetergrösse und Systemleistung lange dauern. Zudem ist SwissSURFACE3D aktuell nicht flächendeckend verfügbar. Falls kein Raster geladen wird, prüfen Sie die Verfügbarkeit hier: [swisstopo.admin.ch](https://www.swisstopo.admin.ch/de/hoehenmodell-swisssurface3d-raster).

---

## Höhenmodell importieren (.tif)

Das Höhenmodell kann für die Sichtbarkeitsanalyse verwendet werden. **Hinweis:** Es kann nur ein Höhenmodell geladen werden.

- Mit dieser Funktion können Sie eine eigene Rasterdatei ins Projekt laden.
- Es kann immer nur eine Rasterdatei pro Projekt gespeichert werden. Eine ältere Datei wird beim erneuten Import überschrieben.
- Verwenden Sie **nicht** den Standard-Import von QGIS. Die Rasterdatei muss einem vorgegebenen Namen folgen, um im Plugin erkannt zu werden.
- Falls mehrere Rasterdateien benötigt werden, müssen diese zuerst zu einer Datei zusammengeführt werden. [Anleitung](https://docs.qgis.org/3.40/de/docs/user_manual/processing_algs/gdal/rastermiscellaneous.html#merge)

---

## Orthophoto importieren (©swisstopo)

Diese Funktion lädt das Luftbild der Schweiz als WMS-Dienst. Das Luftbild kann bei der Orientierung während der Netzdefinition helfen.
