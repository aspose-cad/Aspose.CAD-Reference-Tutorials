---
date: 2025-12-01
description: Erfahren Sie, wie Sie die PDF‑Seitengröße festlegen, DWG in PDF konvertieren
  und die Nachverfolgung von DWG‑Änderungen mit Aspose.CAD für Java aktivieren.
language: de
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: PDF‑Seitengröße festlegen und DWG mit Aspose.CAD Java verfolgen
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF‑Seitengröße festlegen und DWG mit Aspose.CAD Java nachverfolgen

## Einführung

Bei der Zusammenarbeit an CAD-Projekten müssen Sie häufig **PDF‑Seitengröße festlegen**, um ein konsistentes Layout zu erhalten, **DWG in PDF konvertieren** und jede Änderung an der Zeichnung nachverfolgen. Aspose.CAD für Java macht all das in einem einzigen, optimierten Workflow möglich. In diesem Tutorial gehen wir die genauen Schritte durch, um **PDF‑Seitengröße festzulegen**, **DWG‑Änderungen zu verfolgen** und die Zeichnung als PDF zu exportieren – alles mit Java.

## Schnelle Antworten
- **Wie lege ich die PDF‑Seitengröße fest?** Verwenden Sie `CadRasterizationOptions.setPageWidth()` und `setPageHeight()` vor dem Export.  
- **Kann ich Änderungen beim Export nachverfolgen?** Ja – implementieren Sie einen benutzerdefinierten `CadRenderHandler`, um die Tracking‑Ergebnisse zu erfassen.  
- **Welche Methode konvertiert DWG zu PDF?** Rufen Sie `image.save(stream, pdfOptions)` nach der Konfiguration der Optionen auf.  
- **Was sind die wichtigsten Voraussetzungen?** JDK, Aspose.CAD für Java und ein Ordner mit DWG/DXF‑Dateien.  
- **Ist für den Produktionseinsatz eine Lizenz erforderlich?** Ja, eine gültige Aspose.CAD‑Lizenz wird für den Einsatz außerhalb der Testphase benötigt.

## Was bedeutet „PDF‑Seitengröße festlegen“ im Kontext des DWG‑Exports?

Das Festlegen der PDF‑Seitengröße bestimmt die Abmessungen der resultierenden PDF‑Leinwand (Breite × Höhe in Pixel). Dies ist wichtig, wenn die exportierte Zeichnung auf ein bestimmtes Papierformat oder Bildschirmlayout passen soll, sodass alle Elemente genau dort erscheinen, wo Sie sie erwarten.

## Warum Tracking beim Export von DWG‑Dateien aktivieren?

Tracking (oder Änderungsverfolgung) protokolliert alle Rendering‑Probleme, fehlenden Schriftarten oder nicht unterstützten Entitäten, die während der Konvertierung auftreten. Durch das Erfassen dieser Informationen können Sie:
- Schnell Probleme identifizieren, die vor der finalen Auslieferung behoben werden müssen.
- Klare Rückmeldungen an Teammitglieder geben, was geändert oder weggelassen wurde.
- Einen Prüfpfad für stark regulierte Branchen aufrechterhalten.

## Voraussetzungen

- **Java Development Kit (JDK)** – jede aktuelle Version (8 +).  
- **Aspose.CAD für Java** – herunterladen von der offiziellen [Aspose CAD Download‑Seite](https://releases.aspose.com/cad/java/).  
- **Dokumentenverzeichnis** – ein Ordner, der die DWG/DXF‑Dateien enthält, die Sie verarbeiten möchten.

## Namespaces importieren

Beginnen Sie mit dem Import der erforderlichen Aspose.CAD‑Klassen und der Standard‑Java‑I/O‑Klassen.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Schritt 1: DWG‑ (oder DXF‑)Datei laden

Laden Sie Ihre Quellzeichnung in ein `Image`‑Objekt. Passen Sie den Pfad an, damit er auf Ihr eigenes Verzeichnis zeigt.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Schritt 2: PDF‑Exportoptionen konfigurieren (einschließlich Seitengröße)

Hier setzen wir die PDF‑Optionen und legen explizit die **PDF‑Seitengröße** auf 800 × 600 Pixel fest. Hier wird das Haupt‑Keyword angewendet.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Schritt 3: Tracking implementieren

Erstellen Sie einen benutzerdefinierten Fehler‑Handler, der während des Konvertierungsprozesses Tracking‑Informationen erhält.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Schritt 4: Export nach PDF

Mit den konfigurierten Optionen und dem Tracking‑Handler exportieren Sie die Zeichnung. Dieser Schritt **konvertiert DWG zu PDF** (bzw. DXF zu PDF in unserem Beispiel).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Schritt 5: CadRenderHandler‑Klasse – Erfassung von Tracking‑Ergebnissen

Die Klasse `ErrorHandler` erweitert `CadRenderHandler` und gibt alle Rendering‑Probleme aus, die beim **Tracking von Änderungen an DWG‑Dateien** aufgetreten sind.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Häufige Probleme & deren Lösung

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **Fehlende Schriftarten** | CAD‑Datei verweist auf Schriftarten, die auf dem Server nicht installiert sind. | Installieren Sie die erforderlichen Schriftarten oder betten Sie sie in die Quellzeichnung ein. |
| **Nicht unterstützte Entitäten** | Bestimmte DWG‑Entitäten werden von Aspose.CAD noch nicht unterstützt. | Nutzen Sie die Tracking‑Ausgabe, um sie zu identifizieren und die Zeichnung zu vereinfachen. |
| **Falsche Seitengröße** | `setPageWidth/Height` wurde vor dem Export nicht aufgerufen. | Stellen Sie sicher, dass die Seitengröße in `CadRasterizationOptions` wie oben gezeigt gesetzt ist. |

## Häufig gestellte Fragen

### F1: Kann ich das Tracking für andere CAD‑Dateiformate mit Aspose.CAD für Java aktivieren?

A1: Aspose.CAD unterstützt das Tracking hauptsächlich für DWG/DXF‑Dateien. Für andere Formate konsultieren Sie bitte die offizielle Dokumentation, um zu sehen, welche Funktionen verfügbar sind.

### F2: Wie kann ich zusätzliche Exportoptionen in Aspose.CAD für Java handhaben?

A2: Die Bibliothek bietet viele Optionen wie DPI, Hintergrundfarbe und Vektor‑Rasterisierung. Erkunden Sie diese in der [Aspose.CAD Java Dokumentation](https://reference.aspose.com/cad/java/).

### F3: Gibt es eine Testversion von Aspose.CAD für Java?

A3: Ja, Sie können eine kostenlose Testversion von der [Aspose.CAD Free Trial](https://releases.aspose.com/) herunterladen.

### F4: Wo kann ich Hilfe erhalten oder Probleme im Zusammenhang mit Aspose.CAD für Java diskutieren?

A4: Das Community‑Forum unter dem [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) ist ein guter Ort, um Fragen zu stellen und Erfahrungen zu teilen.

### F5: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für Java?

A5: Folgen Sie den Schritten auf der Seite [Temporary License](https://purchase.aspose.com/temporary-license/), um eine zeitlich begrenzte Lizenz für Evaluationszwecke anzufordern.

### F6: Kann ich **DWG zu PDF konvertieren**, während die Ebenen erhalten bleiben?

A6: Ja. Durch die Konfiguration von `CadRasterizationOptions` können Sie Ebeneninformationen im resultierenden PDF erhalten.

### F7: Was ist der beste Weg, **DWG als PDF zu exportieren** mit benutzerdefinierten Seitendimensionen?

A7: Legen Sie die gewünschte Breite und Höhe mit `setPageWidth` und `setPageHeight` fest, bevor Sie `image.save()` aufrufen – genau wie in Schritt 2 gezeigt.

## Fazit

Wenn Sie die obigen Schritte befolgen, können Sie **PDF‑Seitengröße festlegen**, **DWG zu PDF konvertieren** und **Änderungen in DWG‑Dateien nachverfolgen** mit Aspose.CAD für Java. Dieser Workflow gibt Ihnen die volle Kontrolle über das Ausgabe‑Layout und liefert wertvolle Diagnosen, die Ihre CAD‑Zusammenarbeit reibungslos und fehlerfrei halten. Erkunden Sie gerne weitere Rendering‑Optionen und integrieren Sie diesen Code in größere Automatisierungspipelines.

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}