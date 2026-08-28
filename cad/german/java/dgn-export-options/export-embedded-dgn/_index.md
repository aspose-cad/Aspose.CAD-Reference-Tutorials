---
date: 2026-06-14
description: Erfahren Sie, wie Sie CAD nach PDF exportieren und DGN in PDF konvertieren
  mit Aspose.CAD for Java. Schritt‑für‑Schritt‑Anleitung für Java‑Entwickler.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Export eingebettetes DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Export CAD nach PDF – Export eingebettetes DGN mit Aspose.CAD for Java
url: /de/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD nach PDF – Eingebettetes DGN exportieren mit Aspose.CAD für Java

## Einleitung

In diesem Tutorial erfahren Sie **wie man CAD nach PDF exportiert**, indem Sie eine eingebettete DGN‑Datei in ein hochwertiges PDF‑Dokument mit Aspose.CAD für Java konvertieren. Aspose.CAD ist eine robuste Bibliothek, die Java‑Entwicklern die volle Kontrolle über die CAD‑Dateimanipulation gibt, egal ob Sie **DGN nach PDF konvertieren**, **DWG nach PDF konvertieren** oder CAD‑Zeichnungen einfach in andere Formate rendern möchten. Folgen Sie der nachstehenden Schritt‑für‑Schritt‑Anleitung, und Sie können diese Fähigkeit in wenigen Minuten in Ihre Anwendungen integrieren.

## Schnelle Antworten
- **Was bedeutet „Export CAD nach PDF“?** Es konvertiert CAD‑Zeichnungen (DWG, DGN usw.) in PDF‑Dateien, wobei die Vektorqualität erhalten bleibt.  
- **Welche Bibliothek wird verwendet?** Aspose.CAD for Java.  
- **Benötige ich eine Lizenz?** Eine Lizenz ist für die Produktion erforderlich; ein kostenloser Testzeitraum ist verfügbar.  
- **Was sind die wichtigsten Voraussetzungen?** Java‑Entwicklungsumgebung und das Aspose.CAD for Java JAR.  
- **Kann ich die Ausgabe anpassen?** Ja – Sie können Layouts auswählen, Rasterisierungsoptionen festlegen und PDF‑Einstellungen steuern.

## Was ist „Export CAD nach PDF“?

Export CAD nach PDF konvertiert eine native CAD‑Zeichnung (DWG, DGN usw.) in eine PDF‑Datei, die die ursprüngliche Vektorgeometrie, Ebenen und das Layout beibehält, sodass jeder das Design ohne CAD‑Software ansehen, drucken oder teilen kann. Diese Transformation erzeugt ein plattformunabhängiges Dokument, das bei jedem Zoom‑Level identisch aussieht und sich ideal für Zusammenarbeit und Archivierung eignet.

## Warum Aspose.CAD für Java zum Konvertieren von DGN nach PDF verwenden?

Aspose.CAD for Java bietet eine reine Java‑Lösung, die den Bedarf an externen CAD‑Tools eliminiert, exakte Vektortreue in den resultierenden PDFs sicherstellt und umfangreiche Konfigurationsoptionen wie Layout‑Auswahl, DPI‑Steuerung und Schriftart‑Einbettung bietet, wodurch es sowohl für einfache als auch für unternehmensweite Konvertierungsaufgaben ideal ist.

- **Keine externen Abhängigkeiten** – funktioniert rein in Java auf jedem Betriebssystem.  
- **Erhält Vektordaten** – PDFs bleiben bei jedem Zoom‑Level scharf.  
- **Fein abgestimmte Kontrolle** – wählen Sie spezifische Layouts, setzen Sie die Rasterisierungs‑DPI und betten Sie Schriftarten ein.  
- **Unternehmens‑bereit** – unterstützt Dateien bis zu **2 GB**, Stapelverarbeitung von Tausenden von Zeichnungen und flexible Lizenzierung.  

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java Development Environment** – JDK 8 oder höher installiert und konfiguriert.  
- **Aspose.CAD for Java** – laden Sie das neueste JAR von [here](https://releases.aspose.com/cad/java/) herunter.  

## Pakete importieren

Die `import`‑Anweisungen bringen die erforderlichen Aspose.CAD‑Klassen in den Gültigkeitsbereich.  
`Image` ist die Kernklasse, die jede rasterisierbare CAD‑Datei repräsentiert, während `PdfOptions` und `RasterizationOptions` Ihnen ermöglichen, die PDF‑Ausgabe fein abzustimmen.  
`CadRasterizationOptions` legt Rasterisierungsparameter wie DPI, Seitengröße und Layout für das CAD‑Rendering fest.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Wie exportiere ich CAD nach PDF mit Aspose.CAD für Java?

Der Prozess beginnt mit dem Laden der DWG‑Datei, die das eingebettete DGN enthält, anschließend werden Rasterisierungsparameter festgelegt, um Auflösung und Layout der Ausgabe zu definieren, diese Parameter einem PdfOptions‑Objekt zugeordnet und schließlich die Save‑Methode aufgerufen, um das PDF zu erzeugen. Dieser Ansatz gewährleistet hochwertige, vektor‑erhaltende Ergebnisse mit minimalem Code.

Im Folgenden finden Sie eine klare, nummerierte Schritt‑für‑Schritt‑Anleitung, die genau zeigt, wie Sie eine eingebettete DGN‑Datei (innerhalb einer DWG gespeichert) in ein PDF konvertieren.

### Schritt 1: Eingabe‑ und Ausgabepfade festlegen

Definieren Sie das Verzeichnis, das Ihre Quelldatei enthält, und geben Sie die DWG an, die das eingebettete DGN enthält.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Schritt 2: DWG‑Datei laden

`Image` lädt die DWG und erkennt automatisch alle eingebetteten DGN‑Daten, die dann weiterverarbeitet werden können.

```java
Image objImage = Image.load(fileName);
```

### Schritt 3: Rasterisierungsoptionen konfigurieren

Wählen Sie aus, welche Layout(s) Sie in das PDF aufnehmen möchten. In diesem Beispiel exportieren wir nur das **Model**‑Layout, das die gängigste Ansicht für Konstruktionszeichnungen ist.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Schritt 4: PDF‑Optionen konfigurieren

Binden Sie die Rasterisierungseinstellungen an die PDF‑Export‑Optionen, sodass das endgültige Dokument das gewählte Layout und die DPI berücksichtigt.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 5: PDF‑Datei speichern

Schreiben Sie schließlich das PDF mithilfe der konfigurierten Optionen auf die Festplatte. Die `save`‑Methode schreibt das konfigurierte Bild im Ziel‑Dateiformat auf die Festplatte.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG nach PDF konvertieren – ein zusätzlicher Hinweis

Wenn Ihre Quelldatei ein reines DWG (ohne eingebettetes DGN) ist, können Sie denselben Code wiederverwenden – ändern Sie einfach den `fileName`, sodass er auf das DWG zeigt, das Sie konvertieren möchten. Die Rasterisierungs‑ und PDF‑Optionen bleiben identisch und bieten Ihnen einen konsistenten **convert DWG to PDF**‑Workflow.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|--------|----------|
| **Leere PDF‑Ausgabe** | Layout‑Name stimmt nicht überein | Stellen Sie sicher, dass der an `setLayouts` übergebene Layout‑Name exakt dem Layout in der Quelldatei entspricht (Groß‑/Kleinschreibung beachten). |
| **Lizenz‑Ausnahme** | Verwendung der Testversion ohne Lizenz | Wenden Sie eine gültige Aspose.CAD‑Lizenz an, bevor Sie das Bild laden (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Datei nicht gefunden** | Falscher `dataDir`‑Pfad | Verwenden Sie einen absoluten Pfad oder stellen Sie sicher, dass der relative Pfad korrekt zum Arbeitsverzeichnis des Projekts ist. |
| **Grafiken mit niedriger Auflösung** | Standard‑Rasterisierungs‑DPI ist niedrig | Setzen Sie `rasterizationOptions.setResolution(300)` oder passen Sie `setPageWidth/Height` an, um die DPI zu erhöhen. |

## Häufig gestellte Fragen

**Q: Kann ich Aspose.CAD für Java in einem kommerziellen Projekt verwenden?**  
A: Ja, Aspose.CAD für Java ist eine kommerzielle Bibliothek. Sie können eine Lizenz von [here](https://purchase.aspose.com/buy) erhalten.

**Q: Gibt es eine kostenlose Testversion?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.CAD für Java [here](https://releases.aspose.com/) erhalten.

**Q: Wie kann ich Support für Aspose.CAD für Java erhalten?**  
A: Sie können Unterstützung von der Aspose.CAD‑Community im [forum](https://forum.aspose.com/c/cad/19) erhalten.

**Q: Was, wenn ich eine temporäre Lizenz benötige?**  
A: Sie können eine temporäre Lizenz [here](https://purchase.aspose.com/temporary-license/) erhalten.

**Q: Wo finde ich die offizielle Dokumentation?**  
A: Die Dokumentation ist verfügbar [here](https://reference.aspose.com/cad/java/).

## Fazit

Sie haben nun gelernt, wie man **CAD nach PDF exportiert**, speziell wie man **DGN nach PDF** und sogar **DWG nach PDF** mit Aspose.CAD für Java konvertiert. Durch Befolgen der obigen Schritte können Sie nahtlose CAD‑zu‑PDF‑Konvertierung in jede Java‑basierte Lösung integrieren und Ihren Benutzern hochwertige PDFs bereitstellen, ohne zusätzliche CAD‑Software zu benötigen.

---

**Zuletzt aktualisiert:** 2026-06-14  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Export DGN nach DWG mit Aspose.CAD für Java – Tutorial](/cad/java/dgn-export-options/)
- [Müheloser DGN‑zu‑AutoCAD‑PDF‑Export mit Aspose.CAD für Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg nach pdf java – CAD nach PDF exportieren mit Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}