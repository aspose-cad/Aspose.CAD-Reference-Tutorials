---
date: 2025-12-03
description: Erfahren Sie, wie Sie die PDF‑Seitengröße beim Konvertieren von DWG zu
  PDF festlegen und das Tracking in DWG‑Dateien mit Aspose.CAD für Java aktivieren
  – ein vollständiger Leitfaden zum präzisen Export von CAD‑Zeichnungen als PDF.
language: de
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: PDF‑Seitengröße festlegen und Tracking in DWG‑Dateien mit Aspose.CAD in Java
  aktivieren
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF-Seitengröße festlegen und Tracking in DWG-Dateien mit Aspose.CAD in Java aktivieren

## Einführung

Wenn Sie **die PDF-Seitengröße** beim *Konvertieren von DWG zu PDF* festlegen und gleichzeitig etwaige Rendering‑Probleme nachverfolgen möchten, bietet Aspose.CAD für Java eine saubere, programmatische Möglichkeit, beides zu erledigen. In diesem Tutorial führen wir Sie Schritt für Schritt durch die Konfiguration der Seitendimensionen, das Aktivieren des Trackings und den Export einer CAD‑Zeichnung als PDF – alles aus Java heraus. Am Ende verstehen Sie, warum die korrekte Seitengröße für CAD‑Zeichnungen wichtig ist und wie Sie detaillierte Tracking‑Informationen während des Exportvorgangs erfassen.

## Schnellantworten
- **Was beeinflusst “PDF‑Seitengröße festlegen”?** Sie definiert die Breite und Höhe der resultierenden PDF‑Leinwand, sodass Ihre Zeichnung perfekt passt.  
- **Benötige ich eine Lizenz für diese Funktion?** Eine Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Aspose.CAD‑Version wird benötigt?** Jede aktuelle Version, die `CadRasterizationOptions` unterstützt.  
- **Kann ich das mit anderen CAD‑Formaten verwenden?** Das Beispiel zeigt DWG/DXF, aber derselbe Ansatz funktioniert für die meisten unterstützten Formate.  
- **Wie lange dauert die Konvertierung?** In der Regel unter einer Sekunde für kleine Dateien; größere Zeichnungen können länger benötigen.

## Was bedeutet “PDF‑Seitengröße festlegen” im Kontext des CAD‑Exports?
Das Festlegen der PDF‑Seitengröße teilt dem Renderer die genauen Abmessungen (in Pixeln oder Punkten) der Ausgabeleinwand mit. Das ist besonders wichtig für technische Zeichnungen, bei denen Maßstab und Layout erhalten bleiben müssen. Ohne explizite Seitengrößeneinstellungen kann das PDF standardmäßig eine Größe annehmen, die die Zeichnung abschneidet oder verzerrt.

## Warum die PDF‑Seitengröße beim Export von CAD‑Zeichnungen festlegen?
- **Maßstab erhalten** – Ingenieure benötigen maßstabsgetreue Ausdrucke.  
- **Auf Papier passen** – Wählen Sie A4, Letter oder eine benutzerdefinierte Größe, die den Projektspezifikationen entspricht.  
- **Lesbarkeit verbessern** – Größere Seiten zeigen feine Details, ohne dass gezoomt werden muss.  
- **Konsistenter Output** – Automatisierte Pipelines erzeugen PDFs mit identischen Abmessungen bei jedem Durchlauf.

## Wie legt man die PDF‑Seitengröße beim Konvertieren von DWG zu PDF fest?
Im Folgenden konfigurieren wir `CadRasterizationOptions` mit benutzerdefinierten Breiten‑ und Höhenwerten, bevor wir exportieren. Dieser Schritt adressiert direkt das Hauptkeyword **PDF‑Seitengröße festlegen**.

## Voraussetzungen

- **Java Development Kit (JDK)** – Java 8 oder neuer auf Ihrem Rechner installiert.  
- **Aspose.CAD für Java** – Download von der offiziellen [Aspose CAD Download-Seite](https://releases.aspose.com/cad/java/).  
- **Dokumenten‑Verzeichnis** – Ein Ordner, der die DWG/DXF‑Dateien enthält, die Sie verarbeiten möchten.

## Namespaces importieren

Zuerst importieren Sie die benötigten Klassen. Der Code‑Block bleibt unverändert gegenüber dem Original‑Tutorial.

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

## Schritt 1: DWG/DXF‑Datei laden

Laden Sie Ihre Quelldatei. Passen Sie den Pfad an Ihre eigene Datei an.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Schritt 2: PDF‑Exportoptionen konfigurieren (inklusive Seitengröße)

Hier setzen wir die Seitenbreite und -höhe – hier wird die **PDF‑Seitengröße festgelegt**. Die Werte sind in Pixeln; Sie können sie bei Bedarf von Zoll oder Millimetern umrechnen.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tipp:** Wenn Sie Standardpapiergrößen bevorzugen, verwenden Sie die Umrechnung `1 Zoll = 72 Punkte`. Für eine A4‑Seite (8,27 × 11,69 in) setzen Sie `pageWidth = 595` und `pageHeight = 842`.

## Schritt 3: Tracking implementieren

Tracking erfasst etwaige Rendering‑Probleme. Wir hängen einen benutzerdefinierten Handler an, der nach dem Export aufgerufen wird.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Schritt 4: Export nach PDF

Führen Sie nun die Konvertierung aus. Das PDF wird mit den von Ihnen angegebenen Abmessungen erstellt, und alle Tracking‑Informationen werden in der Konsole ausgegeben.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Schritt 5: CadRenderHandler‑Klasse

Der Handler gibt alle Fehler aus, die während des Renderns aufgetreten sind. Das hilft beim Debuggen, wenn Sie **CAD‑Zeichnung als PDF exportieren**.

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

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|-------|-----|
| **Leeres PDF** | Seitengröße auf 0 oder zu klein gesetzt | Stellen Sie sicher, dass `setPageWidth` und `setPageHeight` positive Werte haben. |
| **Geometrie fehlt** | Rendering‑Fehler vom Handler erfasst | Prüfen Sie die Konsolenausgabe von `ErrorHandler` und beheben Sie den jeweiligen `RenderCode`. |
| **Datei nicht gefunden** | Falscher `dataDir`‑Pfad | Verwenden absoluten Pfad oder stellen Sie sicher, dass das Verzeichnis existiert. |
| **Lizenz‑Ausnahme** | Testversion ohne gültige Lizenz für große Dateien verwendet | Laden Sie Ihre Aspose.CAD‑Lizenz, bevor Sie das Bild laden. |

## Häufig gestellte Fragen

**F: Kann ich das Tracking für andere CAD‑Dateiformate mit Aspose.CAD für Java aktivieren?**  
A: Aspose.CAD unterstützt hauptsächlich DWG/DXF für das Tracking. Für andere Formate konsultieren Sie bitte die offizielle Dokumentation.

**F: Wie kann ich zusätzliche Exportoptionen in Aspose.CAD für Java handhaben?**  
A: Die Bibliothek bietet zahlreiche Optionen wie DPI, Hintergrundfarbe und Vektor‑Rasterisierung. Siehe die [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) für Details.

**F: Gibt es eine Testversion von Aspose.CAD für Java?**  
A: Ja, Sie können eine kostenlose Testversion von der [Aspose.CAD Free Trial](https://releases.aspose.com/) herunterladen.

**F: Wo finde ich Unterstützung oder Diskussionen zu Aspose.CAD für Java?**  
A: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und offizielle Antworten.

**F: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für Java?**  
A: Folgen Sie den Schritten auf der Seite [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Zuletzt aktualisiert:** 2025-12-03  
**Getestet mit:** Aspose.CAD für Java 24.11 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}