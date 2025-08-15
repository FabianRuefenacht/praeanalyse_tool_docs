# Netzdefinition

In diesem Register wird die Netzdefinition erstellt. Sämtliche Punkte und Beobachtungen können mit dieser Maske digitalisiert werden. Abbildung 1 zeigt die Registerkarte ```Netzdefinition```.

<img src="../imgs/network/network.png" width="500" /><br/>
<small>_Abbildung 1: Netzdefinition._</small>

---

## Netzpunkte

Netzpunkte sind die Punkte, die für die Netzberechnung von Interesse sind – namentlich die Neupunkte sowie die Referenz- bzw. Lagerungspunkte des Netzes.

### Knoten erfassen

Ein Klick auf den Knopf ```Knoten erfassen``` aktiviert das Digitalisieren von Netzpunkten in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Klicken Sie an der gewünschten Position in der QGIS-Zeichenoberfläche.
- Bestätigen Sie das Pop-up.
- Der neue Punkt wird gezeichnet.

### Aus Grundlagedaten

Der Bereich ```Aus Grundlagedaten``` wechselt das Werkzeug zur Punkterfassung. Nun können Punkte, die zuvor importiert oder über den WFS heruntergeladen wurden, ausgewählt werden (vgl. [Grundlagedaten laden](../load_data)).

- Selektieren Sie einen Punkt aus dem Layer ```imported points```.
- Bestätigen Sie das Pop-up.
- Der neue Punkt wird gezeichnet.

### Knoten bearbeiten

Ein Klick auf den Knopf ```Knoten bearbeiten``` aktiviert die Bearbeitung von Netzpunkten in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie einen Punkt aus dem Layer ```reference_points```.
- Geben Sie die gewünschten Änderungen ein und bestätigen Sie.
- Der Punkt wird aktualisiert.

### Knoten löschen

Ein Klick auf den Knopf ```Knoten löschen``` aktiviert das Löschen von Netzpunkten in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

**Achtung:** Wenn Sie einenen Punkt löschen, an welchem noch Beobachtungen hängen, werden diese Beobachtungen ebenfalls gelöscht.

- Selektieren Sie einen Punkt aus dem Layer ```reference_points```.
- Bestätigen Sie die Löschung.
- Der Punkt wird entfernt.

---

## TS-Beobachtungen

In diesem Abschnitt des Registers ```Netzdefinition``` können Tachymeter-Beobachtungen oder ähnliche Messungen erstellt, bearbeitet und gelöscht werden.

### TS-Beobachtungen erfassen

Ein Klick auf den Knopf ```TS-Beobachtungen erfassen``` aktiviert das Digitalisieren von TS-Beobachtungen in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie den ersten Punkt der Beobachtung aus dem Layer ```reference_points```.
- Bei jeder Mausbewegung wird das **RubberBand** aktualisiert, bis Sie den zweiten Punkt aus dem Layer ```reference_points``` wählen.
- Je nach Einstellung wird eine Sichtbarkeitsanalyse durchgeführt.
- Es erscheint ein Pop-up zur Konfiguration der Beobachtung.
- Nach der Bestätigung wird die Beobachtung in der QGIS-Zeichenoberfläche dargestellt.

### Sichtbarkeitsanalyse

Abhängig von den gewählten Einstellungen kann eine Sichtbarkeitsanalyse durchgeführt werden. Folgende Optionen stehen zur Verfügung:

- **DEM (Swisstopo-API):** Entlang der Beobachtung wird ein Höhenprofil auf Basis des **Geländemodells** SwissALTI3D abgefragt und mit der Beobachtungshöhe verglichen. Dies erfolgt über eine API von Swisstopo ([COGIS o.J.](https://api3.geo.admin.ch/services/sdiservices.html#profile)).
- **DSM (geladenes Höhenmodell):** Entlang der Beobachtung wird ein Höhenprofil auf Basis des geladenen Höhenmodells abgefragt und mit der Beobachtungshöhe verglichen. Diese Berechnung erfolgt lokal auf dem Computer.
- **Keine:** Es wird **keine** Sichtbarkeitsanalyse durchgeführt. Diese Option eignet sich für Computer mit geringer Rechenleistung oder bei sehr langen Visuren.

### TS-Beobachtungen bearbeiten

Ein Klick auf den Knopf ```TS-Beobachtungen bearbeiten``` aktiviert die Bearbeitung von TS-Beobachtungen in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie eine Beobachtung aus dem Layer ```ts_observations```.
- Es erscheint ein Pop-up zur Konfiguration der Beobachtung.
- Nach der Bestätigung wird die Beobachtung in der QGIS-Zeichenoberfläche aktualisiert.

### TS-Beobachtungen löschen

Ein Klick auf den Knopf ```TS-Beobachtungen löschen``` aktiviert das Löschen von TS-Beobachtungen in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie eine Beobachtung aus dem Layer ```ts_observations```.
- Es erscheint ein Pop-up zur Bestätigung der Löschung.
- Nach der Bestätigung wird die Beobachtung entfernt.

---

## GNSS-Beobachtungen

In diesem Abschnitt des Registers ```Netzdefinition``` können GNSS-Beobachtungen oder ähnliche Messungen erstellt, bearbeitet und gelöscht werden.

### GNSS-Beobachtungen erfassen

Ein Klick auf den Knopf ```GNSS-Beobachtungen erfassen``` aktiviert das Digitalisieren von GNSS-Beobachtungen in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie den Punkt der Beobachtung aus dem Layer ```reference_points```.
- Es erscheint ein Pop-up zur Konfiguration der Beobachtung.
- Nach der Bestätigung wird die Beobachtung in der QGIS-Zeichenoberfläche dargestellt.

*Konfiguration der GNSS-Beobachtungen:* Bei der Erfassung von GNSS-Beobachtungen (siehe Abb. 2) können Sie sämtliche Sessionen direkt in einer Maske erfassen. Klicken Sie hierzu auf den Button ```Zeile hinzufügen``` und wählen Sie aus dem Dropdown in der rechten Spalte das Instrument/die Session aus. Fehlerhaft erfasste Sessionen können über den Button ```Zeile löschen``` entfernt werden.

<img src="../imgs/network/GNSS-Obs.png" width="500" /><br/>
<small>_Abbildung 2: Erfassen einer GNSS-Beobachtung._</small>

### GNSS-Beobachtungen bearbeiten

Ein Klick auf den Knopf ```GNSS-Beobachtungen bearbeiten``` aktiviert die Bearbeitung von GNSS-Beobachtungen in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie eine Beobachtung aus dem Layer ```gnss_observations```.
- Es erscheint ein Pop-up zur Konfiguration der Beobachtung.
- Nach der Bestätigung wird die Beobachtung in der QGIS-Zeichenoberfläche aktualisiert.

### GNSS-Beobachtungen löschen

Ein Klick auf den Knopf ```GNSS-Beobachtungen löschen``` aktiviert das Löschen von GNSS-Beobachtungen in der QGIS-Zeichenoberfläche. Ein weiterer Klick auf den Knopf deaktiviert das Tool.

- Selektieren Sie eine Beobachtung aus dem Layer ```gnss_observations```.
- Es erscheint ein Pop-up zur Bestätigung der Löschung.
- Nach der Bestätigung wird die Beobachtung entfernt.

---

## Nivellierungs-Beobachtungen

Die Knöpfe in diesem Bereich haben derzeit keine Funktion.

---

## Kreisel-Beobachtungen

Die Knöpfe in diesem Bereich haben derzeit keine Funktion.
