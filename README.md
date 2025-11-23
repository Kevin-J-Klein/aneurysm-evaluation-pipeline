# README: PipelineV2

## Übersicht

Dieses Notebook (`PipelineV2.ipynb`) beschreibt eine modulare Auswertungs-Pipeline, die verschiedene Schritte von der Datenkonfiguration über das Preprocessing bis hin zur Inferenz und Evaluation umfasst. Die Pipeline ist so aufgebaut, dass sie auf einem lokalen Rechner ausgeführt werden kann.

---

## 1. Konfiguration

Zu Beginn des Notebooks werden die grundlegenden Einstellungen und Pfade definiert. Diese beinhalten:

* Parameter für die Verarbeitung und Auswertung
* Pfade für Zwischenergebnisse und Endresultate

**Hinweis:** Stelle sicher, dass alle Verzeichnisse existieren oder im Notebook automatisch erstellt werden können.

---

## 2. Preprocessing (optional)

Der Preprocessing-Teil dient zur Vorbereitung der Daten für die spätere Inferenz. Dazu können Schritte wie:

* Datenbereinigung
* Normalisierung oder Transformation
* Aufteilung in Trainings- und Testsets
  gehören.

Dieser Abschnitt **kann übersprungen werden**, wenn die Daten bereits vorverarbeitet vorliegen.

---

## 3. Inference

Im Inferenz-Abschnitt wird:

1. Der Ziel-Ordner für die Resultate erstellt.
2. Alle nötigen Dateien und Pfade für die Modellvorhersage vorbereitet.

Die eigentliche **Inferenz wird extern auf dem Cluster ausgeführt**. Das Notebook dient nur der Vorbereitung der Eingabedaten und Struktur.

Nach Abschluss der externen Inferenz sollen die generierten Resultate (prediction masks) in den vorgesehenen Ergebnisordner kopiert werden, sodass sie für die anschließende Evaluation verfügbar sind.

---

## 4. Evaluation

Der Evaluationsabschnitt wertet die Ergebnisse der Inferenz aus. 

