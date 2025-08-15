# Präanalysetool 2.5D

<img src="./imgs/icon.png" width="500" />

## Planung und Präanalyse von geodätischen Netzen

| | |
|---|---|
| **Erstellt von:** | Fabian Rüfenacht |
| **Erstellt am:** | 27. Mai 2024 |
| **Version:** | v0.1.1-beta |
| **Letzte Überarbeitung:** | 15. August 2025 |

Das vorliegende Dokument erläutert das QGIS-Plugin _Präanalysetool_.

---

## Versionskontrolle

Sämtliche Veränderungen werden unter den entsprechenden Versionen aufgelistet. Die oberste Version ist die neueste.

### v0.1.1-beta

| Änderung | Bezeichnung | Bemerkung |
|---|---|---|
| **NEU** | Export Netzkonfiguration in LTOP-Formate | Unterstützt den Export von .KOO & .MES Files |
| **NEU** | Netzkonfiguration GNSS | GNSS-Messungen können nun in die Netzkonfiguration übernommen werden. Wird bei Berechnung nicht berücksichtigt. |


### v0.1.0-beta

| Änderung | Bezeichnung | Bemerkung |
|---|---|---|
| **ÄNDERUNG** | Bezug öffentlicher Geodaten | - |
| **ÄNDERUNG** | Datenspeicherung | Die Daten werden nun in einer SQLite-Datenbank persistiert |
| **ÄNDERUNG** | Sichtbarkeitsanalyse | Optimierung der Performance |
| **ÄNDERUNG** | Code | Umstrukturierung der Code-Basis zur effizienteren Weiterentwicklung |
| **ÄNDERUNG** | Design der relativen Genauigkeits- und Zuverlässigkeitsindikatoren | Relative Indikatoren werden neu beim und nach dem Digitalisieren in der Zeichnung dargestellt. |

### v0.0.1-BTh

| Änderung | Bezeichnung |
|---|---|
| **NEU** | Bezug öffentlicher Geodaten |
| **NEU** | Tachymetrische Messungen |
| **NEU** | Zeichnen der Netzgeometrie |
| **NEU** | Sichtbarkeitsanalyse |
| **NEU** | Hart gelagerte Netze |
| **NEU** | Eingabe von Zuverlässigkeitsparametern |
| **NEU** | Berechnung Genauigkeit Lage & Höhe |
| **NEU** | Berechnung Zuverlässigkeitsindikatoren |
| **NEU** | Berechnung relativer Genauigkeits- und Zuverlässigkeitsindikatoren |
| **NEU** | Erstellung Berechnungsprotokoll |
| **NEU** | Darstellung der Resultate in der QGIS-Zeichnung |

