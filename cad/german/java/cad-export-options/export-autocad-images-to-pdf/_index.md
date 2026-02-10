---
date: 2025-12-19
description: Erfahren Sie, wie Sie PDF aus AutoCAD mit Aspose.CAD für Java exportieren.
  Diese Schritt‑für‑Schritt‑Anleitung zeigt Ihnen, wie Sie DWG in PDF konvertieren,
  CAD als PDF speichern und die Lizenzierung handhaben.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Export AutoCAD PDF – AutoCAD‑Bilder in PDF exportieren mit Aspose.CAD für Java‑Tutorial
url: /de/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD-PDF exportieren – AutoCAD-Bilder nach PDF exportieren mit Aspose.CAD für Java

## Einführung

Suchen Sie nach einer nahtlosen Möglichkeit, **AutoCAD PDF** mit Java zu exportieren? Suchen Sie nicht weiter! In diesem Tutorial führen wir Sie durch die Konvertierung von AutoCAD-Bildern zu PDF mit Aspose.CAD für Java, einer leistungsstarken Bibliothek, die den **convert DWG to PDF**-Prozess mühelos macht. Am Ende verstehen Sie, wie Sie **CAD als PDF speichern** anwenden, benutzerdefinierte Rasterisierungs-Einstellungen festlegen und eine Aspose.CAD-Lizenz für den Produktionseinsatz verwenden.

## Schnelle Antworten
- **Kann ich DWG mit Java in PDF konvertieren?** Ja, Aspose.CAD für Java verarbeitet DWG, DXF und viele andere Formate.
- **Benötige ich eine Lizenz?** Für die unbegrenzte Nutzung ist eine **Aspose CAD-Lizenz** erforderlich; Zur Evaluierung steht eine temporäre Lizenz zur Verfügung.
- **Welche Java-Version wird unterstützt?** Java 8+ (die Bibliothek ist mit allen modernen JDKs kompatibel).

- **Kann ich die PDF-Seitengröße anpassen?** Selbstverständlich – passen Sie `pageWidth` und `pageHeight` in den Rasterisierungsoptionen an.

- **Ist 3D-Rasterisierung möglich?** Ja, aktivieren Sie `TypeOfEntities.Entities3D` für vollständiges 3D-Rendering.


## Was ist **AutoCAD-PDF exportieren**?
AutoCAD-PDF zu exportieren bedeutet, vektorbasierte CAD-Zeichnungen (DWG, DXF, DWF usw.) in ein portables PDF-Dokument zu konvertieren, wobei Ebenen, Linienstärken und optional die 3D-Geometrie erhalten bleiben. Dies ist nützlich, um Entwürfe mit Kunden zu teilen, zu archivieren oder ohne CAD-Software zu drucken.


## Warum Aspose.CAD für Java zum **Exportieren von AutoCAD-PDFs** verwenden?


**Vollständige Formatunterstützung** – funktioniert mit DWG, DXF, DWF und vielen weiteren Formaten.
- **Keine externen Abhängigkeiten** – reine Java-Bibliothek, keine nativen DLLs.
- **Hochwertige Rasterisierung** – Kontrolle über DPI, Seitengröße und Layout.
- **Flexible Lizenz** – Starten Sie mit einer kostenlosen Testversion und upgraden Sie anschließend auf eine dauerhafte **Aspose CAD-Lizenz**.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java-Entwicklungsumgebung** – JDK 8 oder höher installiert.
- **Aspose.CAD für Java-Bibliothek** – Download über den [Download-Link](https://releases.aspose.com/cad/java/).
- **Dokumentverzeichnis** – ein Ordner auf Ihrem Rechner, in dem die CAD-Quelldateien und die generierten PDFs gespeichert werden.

## Namespaces importieren

Importieren Sie in Ihrem Java-Projekt die notwendigen Klassen, um mit Aspose.CAD zu arbeiten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Gehen wir den Code nun Schritt für Schritt durch.

## Schritt-für-Schritt-Anleitung

### Schritt 1: Ressourcenverzeichnispfad festlegen

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Profi-Tipp:** Ersetzen Sie „Ihr Dokumentenverzeichnis“ durch den absoluten Pfad zu dem Ordner, den Sie in den Voraussetzungen erstellt haben.

### Schritt 2: CAD-Bild laden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Warum das wichtig ist:** Durch das Laden der CAD-Datei in ein `Image`-Objekt erhalten Sie vollen Zugriff auf die Rasterisierungs-Engine von Aspose.CAD.

### Schritt 3: Rasterisierungsoptionen festlegen

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Passen Sie `pageWidth` und `pageHeight` an, um die Größe der Ausgabedatei (PDF) zu ändern.
- Entfernen Sie die Kommentarzeichen vor der Zeile `setTypeOfEntities`, wenn Sie **Java-Konvertierung von CAD-Dateien in PDF** für 3D-Objekte benötigen.
- Mit dem Aufruf von `setLayouts` wählen Sie das zu rendernde Layout (Modell, Layout1 usw.) aus.

### Schritt 4: PDF-Optionen konfigurieren

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Hiermit werden die Rasterisierungseinstellungen mit der PDF-Ausgabe verknüpft, um sicherzustellen, dass die Vektordaten korrekt konvertiert werden.

### Schritt 5: PDF speichern

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Die resultierende Datei `Export3DImagestoPDF_out_.pdf` ist eine **als PDF gespeicherte** Darstellung Ihrer ursprünglichen AutoCAD-Zeichnung.

## Häufige Probleme & Lösungen

| Symptom | Wahrscheinliche Ursache | Lösung |

|---------|--------------------------|--------|

| Leere PDF-Ausgabe | Rasterisierungsoptionen nicht festgelegt oder Layout stimmt nicht überein | Überprüfen Sie, ob `setLayouts` mit dem Layoutnamen in Ihrer CAD-Datei übereinstimmt. |

| Niedrig aufgelöstes Bild | `pageWidth`/`pageHeight` zu klein | Vergrößern Sie die Abmessungen oder legen Sie eine höhere DPI-Zahl über `rasterizationOptions.setResolution(...)` fest. |

| Lizenzausnahme | Keine gültige Lizenz angewendet | Wenden Sie eine **Aspose CAD-Lizenz** an oder verwenden Sie eine temporäre Lizenz zum Testen. |

## Häufig gestellte Fragen

### F1: Kann ich Aspose.CAD für Java mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt eine Vielzahl von Formaten, darunter DWG, DWF, DGN und mehr, und bietet Ihnen so maximale Flexibilität für Ihre Projekte.

### F2: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für Java?

A2: Besuchen Sie [hier](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz für Testzwecke zu erhalten.

### F3: Gibt es Layoutoptionen für die Rasterisierung?

A3: Ja, Sie können Layouts (z. B. `"Model"`, `"Layout1"`) über die Methode `setLayouts` anpassen, um die gerenderte Ansicht festzulegen.

### F4: Kann ich die Größe der Ausgabedatei (PDF) anpassen?

A4: Selbstverständlich! Passen Sie die Parameter `pageWidth` und `pageHeight` in den Rasterisierungsoptionen an Ihre gewünschten Abmessungen an.

### F5: Wo kann ich Hilfe zu Aspose.CAD für Java erhalten oder Probleme besprechen?

A5: Besuchen Sie das [Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für gezielte Unterstützung und Diskussionen in der Community.

---

**Letzte Aktualisierung:** 19.12.2025
**Getestet mit:** Aspose.CAD für Java 24.10
**Autor:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}