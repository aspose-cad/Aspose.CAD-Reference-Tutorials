---
date: 2026-10-19
description: Erfahren Sie, wie Sie PNG-Thumbnails von IFC-Dateien mit Aspose.CAD für
  Java in nur wenigen Codezeilen erstellen.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exportieren von IFC nach PNG
og_description: Erstellen Sie mühelos PNG-Thumbnails von IFC-Dateien mit Aspose.CAD
  für Java. Diese Schritt‑für‑Schritt‑Anleitung zeigt, wie Sie IFC‑Modelle laden,
  rasterisieren und als hochwertige PNG‑Bilder speichern.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: PNG-Thumbnails von IFC mit Aspose.CAD für Java erstellen
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Wie man PNG-Thumbnails von IFC mit Aspose.CAD für Java erstellt
url: /de/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC nach PNG exportieren mit Aspose.CAD für Java

## Einführung

In diesem Tutorial lernen Sie, wie Sie mit Aspose.CAD für Java **PNG‑Thumbnail‑IFC**‑Dateien erstellen. Egal, ob Sie schnelle Vorschaubilder für ein BIM‑Portal benötigen, Thumbnails für ein Dokumenten‑Management‑System erzeugen oder Stapelkonvertierungen automatisieren möchten – die nachfolgenden Schritte ermöglichen es Ihnen, ein 3‑D‑IFC‑Modell in ein gestochen scharfes 2‑D‑PNG‑Bild zu rasterisieren, und das mit nur wenigen Zeilen Java‑Code.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.CAD für Java.  
- **Kann ich ein PNG‑Thumbnail‑IFC in wenigen Codezeilen erstellen?** Ja – der gesamte Workflow passt in weniger als 20 Zeilen.  
- **Benötige ich eine Lizenz für die Produktion?** Eine temporäre Lizenz reicht für Tests; für den kommerziellen Einsatz ist eine Voll‑Lizenz erforderlich.  
- **Ist die Ausgabe skalierbar?** Sie können beliebige Pixel‑Abmessungen festlegen, sodass das PNG auf jede gewünschte Größe skaliert.  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher.

## Was bedeutet „IFC nach PNG konvertieren“?
Das Konvertieren von IFC (Industry Foundation Classes) nach PNG bedeutet, das 3‑D‑Gebäudemodell in ein 2‑D‑Bitmap‑Bild zu rasterisieren. Dieser Vorgang erzeugt ein visuelles Thumbnail, das in Browsern, Berichten oder mobilen Apps angezeigt werden kann, ohne dass ein vollständiger CAD‑Viewer erforderlich ist.

## Warum Aspose.CAD für Java verwenden?
Aspose.CAD unterstützt **über 30 CAD‑ und BIM‑Formate**, darunter IFC, DWG, DXF und DGN, und kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Die Bibliothek ist reines Java, hat **keine externen Abhängigkeiten** und läuft auf Windows, Linux und macOS, was sie ideal für serverseitige Bildgenerierung macht.  
Sie bietet hochperformante Rasterisierung, umfangreiche Formatunterstützung und eine einfache Integration in Java‑Anwendungen.

## Voraussetzungen

- **Aspose.CAD‑Bibliothek** – Laden Sie das neueste JAR von dem [download link](https://releases.aspose.com/cad/java/) herunter.  
- **Java Development Kit** – JDK 8 oder neuer, auf Ihrem Rechner installiert.  
- **IFC‑Quelldatei** – Platzieren Sie die Datei in einem Ordner, den Sie in Ihrem Code referenzieren können.

## Namespaces importieren

Das Paket `com.aspose.cad` stellt alle benötigten Klassen bereit. `CadImage` ist der Einstiegspunkt zum Laden von CAD‑Dateien, während `PngOptions` die Rasterisierungseinstellungen konfiguriert.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Wie erstelle ich ein PNG‑Thumbnail‑IFC in Java?

Laden Sie die IFC‑Datei, definieren Sie die Rasterisierungsoptionen und speichern Sie das Ergebnis als PNG‑Bild – das ist der komplette Konvertierungs‑Workflow. Die folgenden Abschnitte zerlegen jeden Schritt, sodass Sie die Code‑Snippets in Ihr Projekt kopieren und sofort ausführen können.

### Schritt 1: IFC‑Datei laden
Zuerst geben Sie den Ordner an, in dem sich Ihre IFC‑Datei befindet, und laden sie mit `CadImage.load`.  
`CadImage.load` liest eine CAD‑Datei und gibt ein Bildobjekt zurück, das rasterisiert werden kann.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Warum das wichtig ist:** Das Laden der Datei als `CadImage` verschafft Ihnen Zugriff auf Vektor‑zu‑Raster‑Konvertierungsoptionen, die Auflösung, Hintergrundfarbe und Linienstärke steuern.

### Schritt 2: Rasterisierungsoptionen festlegen
Definieren Sie die Ausgabedimensionen und weitere vektorbezogene Einstellungen über `VectorRasterizationOptions`.  
`VectorRasterizationOptions` ermöglicht die Angabe von Ausgabegröße, Hintergrundfarbe und anderen Rasterisierungsparametern.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Passen Sie `PageWidth` und `PageHeight` an, um die endgültige PNG‑Auflösung zu steuern, was wichtig ist, wenn Sie **PNG‑java**‑Dateien für hochwertige Drucke oder Web‑Thumbnails speichern.

### Schritt 3: PNG‑Optionen konfigurieren
Verknüpfen Sie die Rasterisierungsoptionen mit dem PNG‑Exporter, indem Sie eine Instanz von `PngOptions` erstellen.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Schritt 4: Bild als PNG speichern
Schließlich schreiben Sie das rasterisierte Bild mit der `save`‑Methode auf die Festplatte.  
`save` speichert das rasterisierte Bild im angegebenen Dateipfad im gewählten Format.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Nach diesem Schritt haben Sie erfolgreich ein **PNG‑Thumbnail‑IFC** erstellt und können das resultierende `example.png` überall dort verwenden, wo Sie ein Rasterbild benötigen.

## Häufige Anwendungsfälle
- **Thumbnails generieren** für BIM‑Modelle in Web‑Portalen.  
- **Einbetten von Grundriss‑Schnappschüssen** in PDF‑ oder Word‑Berichte.  
- **Automatisierte Stapelkonvertierung** großer IFC‑Bibliotheken für Archivierungs‑ oder Migrationsprojekte.

## Fehlerbehebung & Tipps
- **Speicherprobleme:** Bei sehr großen IFC‑Dateien erhöhen Sie den JVM‑Heap (`-Xmx2g` oder höher).  
- **Fehlende Texturen:** Stellen Sie sicher, dass die externen Ressourcen der IFC‑Datei vom `dataDir` aus erreichbar sind.  
- **Pro‑Tipp:** Verwenden Sie `vectorOptions.setBackgroundColor(Color.getWhite())`, wenn Sie einen weißen Hintergrund anstelle des standardmäßig transparenten PNG bevorzugen.

## Häufig gestellte Fragen

### Q1: Ist Aspose.CAD mit allen Versionen von IFC‑Dateien kompatibel?
A1: Aspose.CAD unterstützt verschiedene IFC‑Versionen. Weitere Details zur Kompatibilität finden Sie in der [documentation](https://reference.aspose.com/cad/java/).

### Q2: Kann ich die Rasterisierungsoptionen weiter anpassen?
A2: Auf jeden Fall! Erkunden Sie die [documentation](https://reference.aspose.com/cad/java/) für erweiterte Einstellungen wie DPI‑Steuerung, Anti‑Aliasing und Linienstärke.

### Q3: Gibt es eine Testversion?
A3: Ja, Sie können die kostenlose Testversion von der [Aspose.CAD free trial](https://releases.aspose.com/) herunterladen.

### Q4: Wie kann ich eine temporäre Lizenz für Tests erhalten?
A4: Holen Sie sich eine temporäre Lizenz von der [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: Wo kann ich Fragen stellen oder Probleme melden?
A5: Treten Sie der Community im [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) bei, um Unterstützung von Aspose‑Ingenieuren und anderen Entwicklern zu erhalten.

## Frequently asked questions

**Q: Kann ich diesen Ansatz verwenden, um andere CAD‑Formate nach PNG zu konvertieren?**  
A: Ja, Aspose.CAD unterstützt viele Formate (DWG, DXF, DGN usw.). Ändern Sie einfach die Dateierweiterung und laden Sie die entsprechende Bildklasse.

**Q: Ermöglicht die Bibliothek das Festlegen einer benutzerdefinierten DPI?**  
A: Die DPI wird indirekt über `PageWidth`/`PageHeight` gesteuert. Passen Sie diese Werte relativ zur gewünschten physischen Größe an, um die erforderliche DPI zu erreichen.

**Q: Ist die PNG‑Ausgabe verlustfrei?**  
A: PNG ist ein verlustfreies Format, sodass das rasterisierte Bild die volle visuelle Treue der ursprünglichen Vektordaten beibehält.

## Fazit

Sie haben nun eine vollständige, produktionsreife Methode, um **PNG‑Thumbnail‑IFC**‑Dateien mit Aspose.CAD für Java zu erstellen. Integrieren Sie diese Schritte in Desktop‑Tools, serverseitige Dienste oder Cloud‑Funktionen, um BIM‑Visualisierungspipelines zu automatisieren und End‑Benutzern schnelle, hochwertige Thumbnails bereitzustellen.

---

**Zuletzt aktualisiert:** 2026-10-19  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose

## Verwandte Tutorials

- [Wie man STL nach PNG mit Aspose.CAD für Java konvertiert](/cad/java/cad-export-options/export-stl-to-png/)
- [DWG nach PNG konvertieren – CAD als PNG speichern mit Aspose.CAD für Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [DWG nach PDF exportieren in Java – PDF‑Seitengröße mit Aspose.CAD festlegen](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}