# Benutzerhandbuch Präanalysetool

Willkommen zum Benutzerhandbuch zum QGIS-Plug-in **Präanalysetool**.

Das Plug-in ermöglicht es, interaktiv ein geodätisches Netz zu planen und eine Präanalyse zu berechnen. Berechnen Sie die Lage- und Höhengenauigkeit, Zuverlässigkeit, sowie die relative Genauigkeit und die relative Zuverlässigkeit zwischen zwei Neupunkten. Das Plug-in ist bisher auf terrestrische Messungen und hart gelagerte Netze beschränkt.

## Installationsanleitung {#install}

Das Plug-in wurde mit der QGIS-Version 3.34 (LTR) getestet. Bei Verwendung einer anderen QGIS-Version kann die Funktionstüchtigkeit nicht garantiert werden.

### 1. QGIS installieren

Installieren Sie die Version 3.34 (LTR) von QGIS. [Link](https://download.qgis.org/downloads/QGIS-OSGeo4W-3.34.4-1.msi)

### 2. Erweiterung installieren

Das Plug-in wurde bisher nicht in der Plug-in-Cloud von QGIS veröffentlicht. Daher muss es als .zip-Datei installiert werden. Falls Sie diese Datei nicht besitzen, könne Sie diese beim Institut Geomatik der Fachhochschule anfragen: [geomatik-studieren.ch](https://geomatik-studieren.ch)

### {#Abbildung1}

1. Navigieren Sie zu _Erweiterungen_ → _Erweiterungen verwalten und installieren..._ ([Abbildung 1](https://fabianruefenacht.github.io/praeanalyse_tool_docs/#Abbildung1))
 ![Erweiterungen installieren](./images/install/install_add_plugin.png)
_Abbildung 1: Erweiterungen installieren_

### {#Abbildung2}

2. Es öffnet sich ein neues Fenster. Klicken Sie hier auf _Aus ZIP installieren_
![Aus ZIP installieren](./images/install/install_from_zip.png)

### {#Abbildung3}

3. Klicken Sie auf den Knopf _..._ und wählen die .zip-Datei aus. Klicken Sie anschliessend auf _Erweiterung installieren_
![Erweiterung installieren](./images/install/install_install_plugin.png)

4. Falls eine Fehlermeldung auftaucht, prüfen Sie ob Sie die richtige Version von QGIS verwenden und ob sich nicht bereits ein Plug-in mit demselben Namen um _plugin_-Verzeichnis von QGIS befindet.

### {#Abbildung4}

5. Wenn keine Fehlermeldung aufgetreten ist, sollte die Erweiterung in der _Plug-in-Leiste_ auftauchen
![Plug-in erfolgreich installiert](./images/install/install_installed.png)

Sie können die Erweiterung nun mit Klick auf das Icon starten. Viel Spass mit der Präanalyse!

## Projekt eröffnen {#openProject}

In der Startmaske des Plug-ins muss ein Projekt gewählt werden. Klicken Sie auf die drei Punkte und wählen Sie einen Ordner aus. In diesem Ordner wird - falls noch nicht vorhanden - die Projektstruktur aufgebaut. Wenn die Projektstruktur bereits im Ordner vorhanden ist, wird diese vom Plug-in eingelesen und dargestellt.

Die Projektstruktur setzt sich aus sechs Ordnern zusammen. Die nachfolgende Abbildung zeigt das Baumdiagramm des Projektes und den Inhalt der Ordner.
