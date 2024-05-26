# Benutzerhandbuch Präanalysetool

Willkommen zum Benutzerhandbuch zum QGIS-Plug-in **Präanalysetool**.

Das Plug-in ermöglicht es, interaktiv ein geodätisches Netz zu planen und eine Präanalyse zu berechnen. Berechnen Sie die Lage- und Höhengenauigkeit, Zuverlässigkeit, sowie die relative Genauigkeit und die relative Zuverlässigkeit zwischen zwei Neupunkten. Das Plug-in ist bisher auf terrestrische Messungen und hart gelagerte Netze beschränkt.

Klicken  Sie auf die Bilder, um diese zu vergrössern!

## 1. Installationsanleitung {#install}

Das Plug-in wurde mit der QGIS-Version 3.34 (LTR) getestet. Bei Verwendung einer anderen QGIS-Version kann die Funktionstüchtigkeit nicht garantiert werden.

### 1.1. QGIS installieren

Installieren Sie die Version 3.34 (LTR) von QGIS. [Link](https://download.qgis.org/downloads/QGIS-OSGeo4W-3.34.4-1.msi)

### 1.2. Erweiterung installieren

Das Plug-in wurde bisher nicht in der Plug-in-Cloud von QGIS veröffentlicht. Daher muss es als .zip-Datei installiert werden. Falls Sie diese Datei nicht besitzen, könne Sie diese beim Institut Geomatik der Fachhochschule anfragen: [geomatik-studieren.ch](https://geomatik-studieren.ch)

- Navigieren Sie zu _Erweiterungen_ → _Erweiterungen verwalten und installieren..._ (Abbildung 1)
 [![Erweiterungen installieren](./images/install/install_add_plugin.png)](./images/install/install_add_plugin.png)
_Abbildung 1: Erweiterungen installieren_

- Es öffnet sich ein neues Fenster. Klicken Sie hier auf _Aus ZIP installieren_ (Abbildung 2)
[![Aus ZIP installieren](./images/install/install_from_zip.png)](./images/install/install_from_zip.png)
_Abbildung 2: Aus ZIP installieren_

- Klicken Sie auf den Knopf _..._ in Abbildung 3 und wählen die .zip-Datei aus. Klicken Sie anschliessend auf _Erweiterung installieren_
[![Erweiterung installieren](./images/install/install_install_plugin.png)](./images/install/install_install_plugin.png)
_Abbildung 3: Erweiterung auswählen und installieren_

- Falls eine Fehlermeldung auftaucht, prüfen Sie ob Sie die richtige Version von QGIS verwenden und ob sich nicht bereits ein Plug-in mit demselben Namen um _plugin_-Verzeichnis von QGIS befindet.

- Wenn keine Fehlermeldung aufgetreten ist, sollte die Erweiterung in der _Plug-in-Leiste_ (Abbildung 4) auftauchen
[![Plug-in erfolgreich installiert](./images/install/install_installed.png)](./images/install/install_installed.png)
_Abbildung 4: Plug-in erfolgreich installiert_

Sie können die Erweiterung nun mit Klick auf das Icon starten. Viel Spass mit der Präanalyse!

## Hilfe {#Help}
Bei geöffnetem Plug-in kann jederzeit die Hilfe geöffnet werden. Klicken Sie dazu auf den Knopf unten Links im Plug-in-Fenster (Abbildung 5) oder drücken Sie die Taste _F1_.
[![Hilfe öffnen](./images/help/help.jpg)](./images/help/help.jpg)
_Abbildung 5: Hilfe öffnen_

## Projekt eröffnen {#openProject}

In der Startmaske des Plug-ins muss ein Projekt gewählt werden. Klicken Sie auf die drei Punkte und wählen Sie einen Ordner aus. In diesem Ordner wird - falls noch nicht vorhanden - die Projektstruktur aufgebaut. Wenn die Projektstruktur bereits im Ordner vorhanden ist, wird diese vom Plug-in eingelesen und dargestellt. Wenn Sie die Web-Version der Anleitung verwenden, sehen Sie in Abbildung 7 den Arbeitsablauf der Projekterstellung. Wenn Sie die PDF-Version der Anleitung verwenden, sehen Sie in Abbildung 7 die Ausgangslage der Projekterstellung.

<video controls autoplay loop muted style="max-width: 100%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);">
<source src="./videos/1_openProject.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

_Abbildung 6: Projekt öffnen_

Die Projektstruktur setzt sich aus sechs Ordnern zusammen. Die nachfolgende Abbildung zeigt das Baumdiagramm des Projektes und den Inhalt der Ordner.

| Struktur             | Beschreibung        |
|----------------------|----------------------|
| 📂 **Demo**          | Hauptverzeichnis     |
| ├── 📂 **bin**       | Ordner für Temporäre Dateien         |
| ├── 📂 **instruments** | Instrumente         |
| ├── 📂 **layers**    | Layer-Verzeichnis    |
| ├── 📂 **properties** | Definition der relativen Analysen       |
| ├── 📂 **raster**     | Rasterdaten         |
| └── 📂 **results**    | Ergebnisse          |

## Grundlagen {#fundamental_data}

Im Register Grundlagen werden die Grundlagedaten des Projektes bezogen. Es stehen folgende Optionen zu Verfügung (konsultieren Sie Abbildung 7):

- _Textfile:_ importieren Sie ihre eigenen Punkte als _.txt_-Datei. Die Datei muss durch Semikolon getrennt sein und eine Punktnummer, Ostkoordinate, Nordkoordinate und Höhe für jeden Punkt enthalten.
- _Perimeter zeichnen:_ Der Perimeter ist die Grundlage für den bezug der öffentlichen Geodaten (Fixpunkte und Oberflächenmodell). Der Klick auf den Knopf _Perimeter zeichnen_ aktiviert das Zeichnen in der Zeichenoberfläche von QGIS. Beim ersten Klick in der Zeichenoberfläche wird die erste Ecke einer Bounding-Box aktiviert. Mit dem zweiten Klick wird die Bounding-Box abgeschlossen. Anschliessend werden die Koordinaten und die Fläche des Perimeters berechnet und unterhalb des Knopfes in der Benutzeroberfläche des Plug-ins dargestellt.
- _Fixpunkte (©swisstopo):_ Wenn ein Perimeter definiert wurde, können Sie mit Klick auf den Knopf _Fixpunkte (©swisstopo)_ alle Fixpunkte (LFP1-3 & HFP 1-3) von swisstopo herunterladen.
- _SwissSURFACE3D laden (©swisstopo):_ Wenn ein Perimeter definitert wurde, können Sie mit Klick auf den Knopf _SwissSURFACE3D laden (©swisstopo)_ das Oberflächenmodell der Schweiz _SwissSURFACE3D_ im definierten Perimeter laden. Beachten Sie, dass der Bezug des Oberflächenmodells je nach Ausdehnung des Perimeters und Leistungsfähigkeit Ihres Computers lange dauern kann.
- _Import Höhenmodell (.tif):_ Mit dieser Funktion können Sie ihre eigene Rasterdatei in das Projekt laden. Beachten Sie, dass Sie nur eine Rasterdatei pro Projekt besitzen können. Die älteren Dateien werden jedes Mal überschrieben.
- _Import Orthophoto (©swisstopo):_ Diese Funktion bezieht das Luftbild der Schweiz als WMS-Dienst. Das Luftbild kann bei der Netzdefinition und der Orientierung währed derer helfen. 

[![Grundlagen laden](./images/plugin/fundamental_data.png)](./images/plugin/fundamental_data.png)
_Abbildung 7: Bezug von Grundlagedaten_

## Stochastisches Modell {#stochMod}

Im Register Stoch. Modell (Stochastisches Modell) in Abbildung 8 wird das stochastische Modell der Präanalyse definiert. Für die Netzdefinition (nächstes Register) müssen Instrumente erstellt werden. Die Erstellung der Instrumente wird (in der Web-Version in Abbildung 8) demonstriert. In diesem Register stehen folgende Möglichkeiten zur Verfügung:

### Lage und Höhe

- _Instrument hinzufügen:_ Fügen Sie ein neues Instrument mit Name, Winkelgenauigkeit [mgon], Distanzgenauigkeit [mm], Distanzgenauigkeit [ppm] hinzu.
- _Instrument bearbeiten:_ Wählen Sie in der Liste ein Instrument aus und klicken Sie auf _Instrument bearbeiten:. Sie können alle Eigenschaften des Instrumentes bearbeiten.
- _Instrument löschen:_ Wählen Sie in der Liste ein Instrument aus und klicken Sie auf _Instrument löschen_. Das Instrument wird gelöscht. Sie müssen mindestens ein anderes Instrument in der Liste haben. Beim Löschen müssen Sie ein eratzinstrument auswählen.
- _Default Instrumente laden:_ Mit Klick auf den Knopf _Default Instrumente laden_ werden die Instrumente der Fachhochschule Nordwestschweiz (MS60 und SX12) mit den Genauigkeiten geladen.
### Höhe

Anders als in LTOP werden die Genauigkeiten für die Höhe nicht für gegenseitige Beobachtungen, sonder für einseitige Beobachtungen eingegeben!

- _Sigma Refraktion:_ Geben Sie die Genauigkeit der Refraktion ein. Diese wirkt sich auf die Genauigkeit der Höhe aus.
- _Sigma Instrumentenhöhe [mm]:_ Geben Sie die Genauigkeit der Instrumentenhöhe ein.
- _Sigma Signalhöhe [mm]:_ Geben Sie die Genauigkeit der Signalhöhe ein.

<video controls autoplay loop muted style="max-width: 100%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);">
<source src="./videos/2_stochMod.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

_Abbildung 8: Definition stochatisches Modell_

## Netzdefinition {#networkDef}

In diesem Register wird die Netzdefinition erstellt. Voraussetzung ist, dass Sie den Perimeter erstellt und Instrumente mit ihren Genauigkeiten definiert haben. Wenn Sie die Web-Version des Benutzerhandbuches verwenden, zeigt die Abbildung 9 den Arbeitsablauf der Netzdefinition. Verwenden Sie die PDF-Verion des Benutzerhandbuches, zeigt die Abbildung 9 die Ausgangslage für die Netzdefinition. Für die Netzdefinition stehen Ihnen folgende Optionen zur Verfügung:

### Knoten

- _Knoten erfassen:_
  - ☒ _Aus Grundlagedaten:_ Wenn die Option _Aus Grundlagedaten_ aktiviert ist, können importierte Fixpunkte verwendet werden. Klicken Sie dafür auf einen Fixpunkt. Die Punknummer, die Koordinaten und die Punkthöhe werden automatisch übernommen. Wählen Sie aus, ob es sich um einen Festpunkt oder um einen Neupunkt handelt.
  - ☐ _Aus Grundlagedaten:_ Wenn die Option _Aus Grundlagedaten_ deaktiviert ist,  können Punkte frei digitalisiert werden. Die Koordinaten werden von der Position der Maus übernommen. Die Höhe wird über eine API der swisstopo übernommen. Die Punktnummer müssen Sie selbst vergeben. Achten Sie darauf, dass jede Punktnummer nur einmal vorkommt. Wählen Sie aus, ob es sich um einen Festpunkt oder um einen Neupunkt handelt.
- _Knoten bearbeiten:_ Diese Optio erlaubt das Bearbeiten der Punkteigenschaften.
- _Konten löschen:_ Verwenden  sie diesen Knopf, um Knoten zu löschen. Messungen und die dazugehörigen Sichtbarkeitsanalysen, welche an diesem Punkt angehängt sind, werden ebenfalls gelöscht.
- _Punkthöhen von Raster:_ Wenn eine Rasterdatei vorhanden ist, können die Punkthöhen vom Raster abgegriffen werden.  **Achtung:** Diese Option überschreibt alle bestehenden  Punkthöhen.

### Beobachtungen

- _Messung erfassen:_ Erfassen Sie eine Beobachtung und führen Sie die Sichtbarkeitsanalyse (Schema der Sichtbarkeitsanalyse in Abbildung 10) durch. Wählen Sie Start und Zielpunkt der Beobachtung aus. Klicken Sie dazu auf vorher digitalisierte Netzpunkte. Anschliessend geben Sie an, welche Elemente der Beobachtung gemessen werden (Winkel, Distanz, beide). Wählen Sie, ob die Beobachtung gegenseitig oder einseitig erfolgt, wie oft die Messung getätigt wird und welches Instrument die Messungen durchführt.
  - _Sichtbarkeitsanalyse DEM:_ Die Sichtbarkeitsanalyse wird auf dem Geländemodell durchgeführt. Dazu wird nicht das importierte Raster verwendet, sondern eine API der swisstopo. Die Erdkrümmung wird kompensiert.
  - _Sichtbarkeitsanalyse DEM:_ Die Sichtbarkeitsanalyse wird auf dem importierten Raster durchgeführt. Die Erdkrümmung wird kompensiert.
  - _Sichtbarkeitsanalyse keine:_ Es wird keine Sichtbarkeitsanalyse durchgeführt. (am schnellsten)
- _Messung bearbeiten:_ bearbeiten Sie die Messanordnung, die Anzahl Messungen und das verwendete Instrument.
- _Messung löschen:_ löschen Sie gezeichnete Messungen. Die Sichtbarkeitsanalyse wird ebenfalls gelöscht.

<video controls autoplay loop muted style="max-width: 100%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);">
<source src="./videos/3_NetDef.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

_Abbildung 9: Netzdefinition_

[![Schema Sichtbarkeitsanalyse](./images/visibility/schema_visibility.png)](./images/visibility/schema_visibility.png)

_Abbildung 10: Schema Sichtbarkeitsanalyse_

## Qualität und Zuverlässigkeit {#QualRel}

In der Registerkarte _Qualität / Zuverlässigkeit_ können Sie die Einstellungen bezüglich der Zuverlässigkeit und der Analyse der relativen Genauigkeit und Zuverlässigkeit machen. Wenn Sie die Web-Version des Benutzerhandbuches verwenden, zeigt die Abbildung 11 den Arbeitsablauf im Register _Qualität / Zuverlässigkeit_. Verwenden Sie die PDF-Verion des Benutzerhandbuches, zeigt die Abbildung 11 die Ausgangslage im Register _Qualität / Zuverlässigkeit_. Ihnen stehen folgende Optionen zur Verfügung:
