---
date: 2026-06-29
description: Erfahren Sie, wie Sie ein PDF aus DWG erstellen und das PDF-Layout mit
  Aspose.CAD für Java anpassen. Einfache Integration für Java-Entwickler.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: Einzel-PDF mit verschiedenen Layouts
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: PDF aus DWG mit Aspose.CAD für Java erstellen
url: /de/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF aus DWG mit Aspose.CAD für Java erstellen

## Einführung

In diesem Tutorial **erstellen Sie PDF aus DWG**-Dateien und wenden mehrere Seitenformat‑Layouts mit Aspose.CAD für Java an. Egal, ob Sie Baupläne, technische Schemata oder marketing‑fertige PDFs erzeugen müssen, die nachfolgenden Schritte zeigen Ihnen, wie Sie CAD‑Zeichnungen in PDF konvertieren, die Abmessungen jedes Layouts anpassen und ein einzelnes, mehrseitiges Dokument erzeugen – alles ohne Ihre Java‑Umgebung zu verlassen.

## Schnelle Antworten
- **Worum geht es in diesem Tutorial?** Konvertierung einer DWG‑Zeichnung in ein einzelnes PDF mit mehreren Seitenformaten.  
- **Welche Bibliothek wird benötigt?** Aspose.CAD für Java (neueste Version).  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich andere Formate exportieren?** Ja – die API unterstützt ebenfalls den Export nach PNG, JPEG und SVG.  
- **Reicht Java 8 aus?** Die Bibliothek funktioniert mit Java 8 und neueren Laufzeiten.

## Was bedeutet „PDF aus DWG erstellen“?

**Create PDF from DWG** bedeutet, eine native AutoCAD‑DWG‑Datei in ein PDF‑Dokument zu konvertieren, wobei Vektortreue, Ebenen und Linienstärken erhalten bleiben und eine Layout‑Anpassung ermöglicht wird. Aspose.CAD führt diese Konvertierung vollständig im Speicher durch, sodass keine externe CAD‑Software nötig ist und das resultierende PDF direkt bearbeitet oder gedruckt werden kann.

## Warum PDF‑Layout aus DWG anpassen?

Aspose.CAD unterstützt **30+ CAD‑Formate** und kann PDFs bis zu **500 MB** erzeugen, ohne die gesamte Datei in den Speicher zu laden. Durch die Definition individueller Seitengrößen für jedes Layout können Sie druckbare Blätter erzeugen, die ISO-, ANSI‑ oder benutzerdefinierte Abmessungen exakt treffen – ein quantifizierbarer Nutzen, der Zeit spart und manuelle Nachbearbeitung eliminiert.

## Voraussetzungen

Bevor wir diese Reise beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
- Java‑Umgebung: Vergewissern Sie sich, dass Java auf Ihrem Rechner installiert ist.  
- Aspose.CAD‑Bibliothek: Laden Sie die Aspose.CAD‑Bibliothek für Java von dem [download link](https://releases.aspose.com/cad/java/) herunter und installieren Sie sie.  
- Dokumenten‑Verzeichnis: Richten Sie ein Verzeichnis für Ihre DWG‑Zeichnungen ein.

## Pakete importieren

Die Klasse `CadImage` ist das Kernobjekt von Aspose.CAD, das eine CAD‑Zeichnung im Speicher repräsentiert. Importieren Sie die erforderlichen Namespaces, bevor Sie beginnen:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Schritt 1: CAD‑Zeichnung laden

`CadImage` lädt die DWG‑Datei und stellt Zugriff auf die Vektordaten bereit. Laden Sie Ihre CAD‑Zeichnung in ein `CadImage`‑Objekt:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

`RasterizationOptions` definiert, wie die CAD‑Vektoren rasterisiert werden, bevor sie in das PDF eingefügt werden. Richten Sie die Rasterisierungsoptionen für das CAD‑Bild ein:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Schritt 3: Layout‑Seitengrößen anpassen

`PdfOptions` ermöglicht es Ihnen, jedem Layout innerhalb der DWG unterschiedliche Seitenabmessungen zuzuweisen. Definieren Sie benutzerdefinierte Größen für mehrere Layouts in der CAD‑Zeichnung:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Schritt 4: PDF‑Optionen festlegen

`PdfOptions` ist der Container, der Rasterisierungs‑Einstellungen und Layout‑Definitionen kombiniert. Konfigurieren Sie die PDF‑Optionen und integrieren Sie die Rasterisierungs‑Einstellungen:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 5: Als PDF speichern

`PdfSaveOptions` finalisiert die Konvertierung und schreibt die Ausgabedatei. Speichern Sie das verarbeitete CAD‑Bild als PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Herzlichen Glückwunsch! Sie haben erfolgreich **PDF aus DWG erstellen** mit unterschiedlichen Seitenformaten mithilfe von Aspose.CAD für Java.

## Häufige Probleme und Lösungen

- **Leere Seiten im Ausgabepdf** – Stellen Sie sicher, dass die `PageSize`‑Werte den tatsächlichen Layout‑Abmessungen in der DWG‑Datei entsprechen.  
- **Memory‑out‑Fehler bei großen Zeichnungen** – Verwenden Sie `CadImage.load(..., LoadOptions)` mit `LoadOptions.setLoadMode(LoadMode.Memory)`, um die Datei zu streamen, anstatt sie vollständig zu laden.  
- **Falsche Skalierung** – Passen Sie `RasterizationOptions.setPageWidth` und `setPageHeight` an, um die gewünschte DPI (dots per inch) zu erreichen.

## Häufig gestellte Fragen

**Q: Kann ich Aspose.CAD für Java mit anderen Java‑Bibliotheken verwenden?**  
A: Ja, Aspose.CAD für Java lässt sich nahtlos in Bibliotheken wie Apache POI, Jackson oder Spring Boot integrieren.

**Q: Gibt es eine Testversion?**  
A: Absolut! Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

**Q: Wo finde ich zusätzlichen Support?**  
A: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

**Q: Wie erhalte ich eine temporäre Lizenz?**  
A: Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**Q: Wo kann ich die Vollversion kaufen?**  
A: Kaufen Sie die Vollversion von Aspose.CAD für Java [hier](https://purchase.aspose.com/buy).

---

**Zuletzt aktualisiert:** 2026-06-29  
**Getestet mit:** Aspose.CAD für Java 24.10  
**Autor:** Aspose

## Verwandte Tutorials

- [DWG nach PDF oder Raster exportieren mit Aspose.CAD für Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [CAD‑Layouts nach PDF exportieren mit Aspose.CAD für Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Bestimmtes DWG‑Layout nach PDF exportieren mit Aspose.CAD für Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}