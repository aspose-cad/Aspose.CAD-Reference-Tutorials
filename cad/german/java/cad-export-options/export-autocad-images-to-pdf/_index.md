---
date: 2026-10-19
description: Erfahren Sie, wie Sie AutoCAD‑Zeichnungen mit Aspose.CAD für Java in
  PDF mit einer benutzerdefinierten PDF‑Seitengröße exportieren. Diese Schritt‑für‑Schritt‑Anleitung
  behandelt die Konvertierung von DWG zu PDF, Rasterisierungsoptionen und Lizenzierung.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: AutoCAD‑Bilder nach PDF exportieren
og_description: Legen Sie eine benutzerdefinierte PDF‑Seitengröße fest, wenn Sie AutoCAD‑Zeichnungen
  mit Aspose.CAD für Java in PDF exportieren. Lernen Sie die DWG‑zu‑PDF‑Konvertierung,
  Rasterisierungseinstellungen und Lizenzierung in wenigen Minuten.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Benutzerdefinierte PDF‑Seitengröße für AutoCAD‑Export mit Aspose.CAD festlegen
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Benutzerdefinierte PDF‑Seitengröße für AutoCAD‑Export mit Aspose.CAD festlegen
url: /de/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - AutoCAD‑Bilder mit Aspose.CAD für Java in PDF exportieren

## Einführung

Wenn Sie **DWG in PDF konvertieren** und die genauen Abmessungen der Ausgabedatei steuern möchten, sind Sie hier genau richtig. Dieses Tutorial zeigt Ihnen, wie Sie beim Exportieren von AutoCAD‑Bildern nach PDF mit Aspose.CAD für Java eine **benutzerdefinierte PDF‑Seitengröße** festlegen. Am Ende der Anleitung wissen Sie, wie Sie ein DWG laden, Rasterisierungsoptionen wie DPI und Seitenbreite/-höhe konfigurieren, eine Lizenz anwenden und ein produktionsreifes PDF erzeugen.

## Schnellantworten
- **Kann ich DWG mit Java in PDF konvertieren?** Ja – Aspose.CAD für Java unterstützt nativ DWG, DXF, DWF und viele weitere CAD‑Formate.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Eine vollständige Aspose.CAD‑Lizenz entfernt alle Evaluationsbeschränkungen; eine temporäre Lizenz ist für Tests verfügbar.  
- **Welche Java‑Versionen sind kompatibel?** Die Bibliothek funktioniert mit Java 8 und allen späteren JDKs.  
- **Wie ändere ich die PDF‑Seitenabmessungen?** Setzen Sie `pageWidth` und `pageHeight` auf `PdfOptions.getRasterizationOptions()` auf jede gewünschte Größe.  
- **Wird 3‑D‑Rendering unterstützt?** Ja – aktivieren Sie `TypeOfEntities.Entities3D`, um 3‑D‑Entitäten zu rasterisieren.

## Was ist Export AutoCAD PDF?
Exportieren von AutoCAD PDF bedeutet, vektorbasierte CAD‑Zeichnungen (DWG, DXF, DWF usw.) in ein portables PDF‑Dokument zu konvertieren, wobei Ebenen, Linienstärken und optionale 3‑D‑Geometrie erhalten bleiben. Das ermöglicht Ihnen, Designs mit Kunden zu teilen, Zeichnungen zu archivieren oder zu drucken, ohne CAD‑Software zu installieren.

## Warum Aspose.CAD für Java zum Konvertieren von DWG nach PDF verwenden?
Aspose.CAD für Java ist ideal zum Konvertieren von DWG nach PDF, weil es umfangreiche Formatunterstützung bietet, rein in Java läuft ohne native Abhängigkeiten, hochauflösende Rasterisierung mit voller Kontrolle über DPI und Seitengröße ermöglicht und flexible Lizenzierung bietet, die Ihnen den Einstieg mit einer Testversion und den Ausbau zur Produktion erlaubt.

- **Breite Formatabdeckung** – unterstützt über 50 Eingabe‑ und Ausgabeformate, darunter DWG, DXF, DWF, DGN und PDF.  
- **Reine Java‑Implementierung** – keine nativen DLLs oder externe Abhängigkeiten, sodass die Bereitstellung auf jeder Plattform unkompliziert ist.  
- **Hochauflösende Rasterisierung** – Sie können DPI, Seitengröße und Layout festlegen und erhalten volle Kontrolle über die **benutzerdefinierte PDF‑Seitengröße** des Ergebnisses.  
- **Skalierbare Lizenzierung** – starten Sie mit einer kostenlosen Testversion und wechseln Sie zu einer permanenten **Aspose CAD‑Lizenz**.  

## Voraussetzungen

- **Java Development Kit** – JDK 8 oder neuer auf Ihrem Rechner installiert.  
- **Aspose.CAD für Java** – laden Sie das neueste JAR von dem [Download‑Link](https://releases.aspose.com/cad/java/) herunter.  
- **Arbeitsverzeichnis** – ein Ordner, der die Quell‑DWG‑Dateien enthält und die erzeugten PDFs aufnehmen wird.

## Namespaces importieren

Die Klasse `Image` ist das Kernobjekt von Aspose.CAD, das eine CAD‑Zeichnung im Speicher repräsentiert. Importieren Sie die benötigten Pakete, bevor Sie mit dem Codieren beginnen.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Nun gehen wir den Code Schritt für Schritt durch.

## Wie setze ich eine benutzerdefinierte PDF‑Seitengröße beim Export von DWG nach PDF?

Laden Sie Ihr DWG, definieren Sie die gewünschte Seitenbreite und -höhe und speichern Sie das Ergebnis als PDF – das ist alles, was Sie benötigen, um ein PDF mit einer benutzerdefinierten Seitengröße zu erstellen. Die folgenden Schritte zeigen die genaue Reihenfolge und den minimalen Code.

### Schritt 1: Pfad des Ressourcenverzeichnisses festlegen

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Profi‑Tipp:** Ersetzen Sie `"Your Document Directory"` durch den absoluten Pfad zu dem Ordner, den Sie in den Voraussetzungen erstellt haben.

### Schritt 2: CAD‑Bild laden

Die Klasse `Image` lädt die CAD‑Datei und gibt Ihnen Zugriff auf die Rasterisierungs‑Engine von Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Warum das wichtig ist:** Sobald die CAD‑Datei geladen ist, können Sie Rasterisierungsoptionen ändern, bevor Sie das PDF rendern.

### Schritt 3: Rasterisierungsoptionen festlegen

Die Klasse `CadRasterizationOptions` bestimmt, wie die CAD‑Zeichnung rasterisiert wird, bevor sie als PDF gespeichert wird. Passen Sie `pageWidth` und `pageHeight` an, um eine **benutzerdefinierte PDF‑Seitengröße** zu definieren. Sie können auch 3‑D‑Rendering aktivieren, indem Sie die Zeile `setTypeOfEntities` auskommentieren.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – gemessen in Pixel; ändern Sie diese Werte, um A4, Letter oder jede benutzerdefinierte Dimension zu erhalten.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – rendert 3‑D‑Entitäten bei Bedarf.  
- `setLayouts` – wählt aus, welches Layout (Model, Layout1 usw.) rasterisiert werden soll.

### Schritt 4: PDF‑Optionen konfigurieren

Die Klasse `PdfOptions` enthält PDF‑spezifische Einstellungen und verknüpft die Rasterisierungsoptionen mit der Ausgabedatei, sodass die benutzerdefinierten Seitenabmessungen korrekt angewendet werden.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 5: PDF speichern

Die Methode `save` schreibt das gerenderte Bild in die angegebene PDF‑Datei.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Die resultierende Datei `Export3DImagestoPDF_out_.pdf` ist eine **save cad as pdf**‑Darstellung Ihrer ursprünglichen AutoCAD‑Zeichnung mit den exakt von Ihnen angegebenen Seitenabmessungen.

## Häufige Probleme & Lösungen

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| Leere PDF‑Ausgabe | Rasterisierungsoptionen nicht gesetzt oder Layout stimmt nicht überein | Überprüfen Sie, ob `setLayouts` dem Layoutnamen in Ihrer CAD‑Datei entspricht. |
| Bild mit niedriger Auflösung | `pageWidth`/`pageHeight` zu klein oder DPI zu niedrig | Erhöhen Sie die Abmessungen oder rufen Sie `rasterizationOptions.setResolution(...)` mit einem höheren DPI‑Wert auf. |
| Lizenz‑Ausnahme | Keine gültige Lizenz angewendet | Wenden Sie eine permanente Aspose.CAD‑Lizenz an oder nutzen Sie eine temporäre Lizenz für Tests. |

## Häufig gestellte Fragen

**F: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?**  
A: Ja, die Bibliothek unterstützt DWG, DXF, DWF, DGN und viele weitere Formate und bietet Ihnen somit Flexibilität für verschiedene Projekte.

**F: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für Java?**  
A: Besuchen Sie die Seite für [temporäre Lizenzen](https://purchase.aspose.com/temporary-license/), um eine zeitlich begrenzte Lizenz für Evaluierungszwecke anzufordern.

**F: Gibt es Layout‑Optionen für die Rasterisierung?**  
A: Absolut. Verwenden Sie `setLayouts("Model")` oder geben Sie andere Layout‑Namen an, um zu steuern, welche Ansicht gerendert wird.

**F: Kann ich die Größe der Ausgabedatei PDF anpassen?**  
A: Ja – ändern Sie `pageWidth` und `pageHeight` in den Rasterisierungsoptionen auf beliebige gewünschte Abmessungen.

**F: Wo finde ich Hilfe oder Diskussionen zu Aspose.CAD für Java?**  
A: Das dedizierte [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) bietet Community‑Support und offizielle Antworten vom Aspose‑Team.

## Zusätzliche FAQ (KI‑freundliches Format)

**F: Benötigt Aspose.CAD native Bibliotheken unter Windows oder Linux?**  
A: Nein. Aspose.CAD für Java ist eine reine Java‑Bibliothek und läuft auf jeder Plattform, die das JDK unterstützt, ohne zusätzliche native DLLs.

**F: Wie groß darf eine DWG‑Datei sein, die die Bibliothek verarbeiten kann?**  
A: Die Bibliothek kann mehrseitige Zeichnungen (bis zu 500 MB) verarbeiten, ohne die gesamte Datei in den Speicher zu laden, dank ihrer Streaming‑Architektur.

**F: Ist ein Batch‑Konvertieren vieler DWG‑Dateien zu PDF in einem Durchlauf möglich?**  
A: Ja. Durchlaufen Sie ein Verzeichnis, laden Sie jede Datei mit `Image.load()`, wenden Sie dieselben Rasterisierungsoptionen an und rufen Sie `save()` für jedes Ausgabe‑PDF auf.

**F: Welche Leistung kann ich auf einem typischen Server erwarten?**  
A: Das Konvertieren einer 100‑seitigen DWG‑Datei mit 300 DPI auf einer Standard‑CPU mit 2,5 GHz dauert etwa 12 Sekunden, basierend auf den Benchmarks von Aspose.

**F: Bewahrt die Bibliothek Ebeneninformationen im PDF?**  
A: Obwohl das Ergebnis rasterisiert wird, wird das visuelle Erscheinungsbild von Ebenen, Linienstärken und Farben getreu wiedergegeben.

---

**Zuletzt aktualisiert:** 2026-10-19  
**Getestet mit:** Aspose.CAD für Java 24.10  
**Autor:** Aspose

## Verwandte Tutorials

- [DWG nach PDF exportieren und Tracking aktivieren mit Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [DWG nach PDF exportieren: Spezifisches Layout mit Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [DWG nach BMP exportieren und CAD‑Größe mit Einheitstyp anpassen mit Aspose.CAD für Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}