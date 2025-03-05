---
title: Exportieren Sie DWG mit Aspose.CAD für Java in PDF oder Raster
linktitle: Exportieren Sie DWG in PDF oder Raster
second_title: Aspose.CAD Java API
description: Entdecken Sie den nahtlosen Prozess des Exports von DWG-Dateien in PDF oder Rasterbilder in Java mit Aspose.CAD. Diese Schritt-für-Schritt-Anleitung sorgt für Präzision und Effizienz.
type: docs
weight: 13
url: /de/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Einführung

In der dynamischen Welt des computergestützten Designs (CAD) ist ein effizienter Umgang mit Zeichnungen von entscheidender Bedeutung. Aspose.CAD für Java bietet eine leistungsstarke Lösung zum Exportieren von DWG-Dateien in PDF- oder Rasterbilder. Dieses Tutorial führt Sie durch den Prozess und stellt sicher, dass Sie das volle Potenzial von Aspose.CAD für Java nutzen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Grundlegendes Verständnis der Java-Programmierung.
-  Aspose.CAD für Java-Bibliothek installiert. Wenn nicht, laden Sie es herunter[Hier](https://releases.aspose.com/cad/java/).
- Eine DWG-Datei zu Testzwecken. Sie können die bereitgestellte Datei „Bottom_plate.dwg“ verwenden.

## Namespaces importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Namespaces, um den Prozess zu starten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Schritt 1: Laden Sie die DWG-Datei

 Laden Sie zunächst Ihre DWG-Datei mit Aspose.CAD`Image` Klasse:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Schritt 2: Bestimmen Sie den Einheitentyp

Überprüfen Sie als Nächstes den Einheitentyp der geladenen DWG-Datei:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Schritt 3: Rasterisierungsoptionen festlegen

Konfigurieren Sie basierend auf dem Einheitentyp die Rasterisierungsoptionen:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metrische Einheiten
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // imperiale Einheiten
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Schritt 4: PDF-Optionen konfigurieren

PDF-Exportoptionen einrichten:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Schritt 5: Als PDF speichern

Abschließend speichern Sie die DWG-Datei als PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Und da haben Sie es! Sie haben mit Aspose.CAD für Java erfolgreich eine DWG-Datei in PDF exportiert.

## Abschluss

Dieses Tutorial enthielt eine Schritt-für-Schritt-Anleitung zur Nutzung von Aspose.CAD für Java zum Exportieren von DWG-Dateien in PDF- oder Rasterbilder. Diese Bibliothek vereinfacht den Prozess und ermöglicht Ihnen die effiziente Bearbeitung von CAD-Zeichnungen in Ihren Java-Anwendungen.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen Java-Frameworks verwenden?

A1: Ja, Aspose.CAD für Java lässt sich nahtlos in gängige Java-Frameworks integrieren.

### F2: Ist eine temporäre Lizenz für Aspose.CAD für Java verfügbar?

 A2: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F3: Wo finde ich Unterstützung für Aspose.CAD für Java?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) um Unterstützung aus der Gemeinde.

### F4: Wie kann ich eine Lizenz für Aspose.CAD für Java erwerben?

 A4: Sie können eine Lizenz erwerben[Hier](https://purchase.aspose.com/buy).

### F5: Welche Einheiten unterstützt Aspose.CAD für Java?

A5: Aspose.CAD für Java unterstützt sowohl metrische als auch imperiale Einheiten.