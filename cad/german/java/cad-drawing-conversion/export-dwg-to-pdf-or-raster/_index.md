---
date: 2025-12-18
description: Erkunden Sie, wie Sie DWG in PDF oder Rasterbilder in Java mit Aspose.CAD
  exportieren. Dieser Schritt‑für‑Schritt‑Leitfaden gewährleistet Präzision, Effizienz
  und eine einfache Konvertierung von DWG‑Dateien.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: DWG in PDF oder Raster exportieren mit Aspose.CAD für Java
url: /de/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG nach PDF oder Raster exportieren mit Aspose.CAD für Java

## Einleitung

Im dynamischen Umfeld des computerunterstützten Designs (CAD) ist ein effizientes Handling von Zeichnungen entscheidend. Mit **Aspose.CAD for Java** können Sie **export dwg to pdf** — oder Rasterbilder — in nur wenigen Codezeilen durchführen. Dieses Tutorial führt Sie durch den gesamten Prozess, vom Laden einer DWG‑Datei bis zur Erstellung eines hochwertigen PDFs, und zeigt, warum Aspose.CAD Java die bevorzugte Bibliothek für CAD‑Konvertierungsaufgaben ist.

## Schnelle Antworten
- **Was behandelt dieses Tutorial?** Export von DWG‑Dateien zu PDF oder Rasterbildern mit Aspose.CAD für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose temporäre Lizenz steht für die Evaluierung zur Verfügung; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Jede Java 8+ Laufzeit funktioniert mit der neuesten Aspose.CAD Java API.  
- **Kann ich DWG in andere Bildformate konvertieren?** Ja – dieselben Rasterisierungsoptionen ermöglichen die Ausgabe von PNG, JPEG, BMP usw.  
- **Wie lange dauert die Konvertierung?** In der Regel weniger als eine Sekunde für Standardzeichnungen; größere Dateien können einige Sekunden benötigen.

## Was bedeutet „export dwg to pdf“?
Das Exportieren von DWG nach PDF bedeutet, eine native AutoCAD‑Zeichnung in ein portables, geräteunabhängiges PDF‑Dokument zu konvertieren. Das resultierende PDF bewahrt Vektordaten, Ebenen und Skalierung und ist damit ideal zum Teilen, Drucken oder Archivieren.

## Warum Aspose.CAD Java für diese Konvertierung verwenden?
- **Keine externen Abhängigkeiten** – reines Java, keine nativen DLLs.  
- **Präzise Einheitenverarbeitung** – berücksichtigt automatisch metrische oder imperiale Einheiten.  
- **Hochwertige Rasterausgabe** – fein abgestimmte DPI‑ und Seitengrößensteuerung.  
- **Vollständige PDF‑Unterstützung** – vektor‑erhaltende PDF‑Erstellung ohne zusätzliche Bibliotheken.

## Voraussetzungen

Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie:

- Grundkenntnisse in der Java‑Programmierung besitzen.  
- Die Aspose.CAD for Java‑Bibliothek installiert haben. Wenn Sie sie noch nicht heruntergeladen haben, erhalten Sie sie **[hier](https://releases.aspose.com/cad/java/)**.  
- Eine DWG‑Datei zum Testen – das Beispiel **Bottom_plate.dwg** wird in diesem Leitfaden verwendet.

## Namespaces importieren

Importieren Sie in Ihrem Java‑Projekt die erforderlichen Klassen, um die Konvertierung zu starten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: DWG‑Datei laden

Laden Sie zunächst Ihre DWG‑Zeichnung mit der Klasse `Image`. Dadurch wird eine In‑Memory‑Repräsentation erstellt, mit der Aspose.CAD arbeiten kann.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Schritt 2: Einheitstyp bestimmen

Das Verständnis, ob die Zeichnung metrische oder imperiale Einheiten verwendet, ist für die korrekte Skalierung entscheidend. Die Hilfsmethode `IsMetric` (Implementierung aus Gründen der Kürze weggelassen) liefert einen booleschen Wert.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Schritt 3: Rasterisierungsoptionen festlegen

Basierend auf dem Einheitssystem konfigurieren Sie Seitengröße, Skalierung und den Ziel‑Einheitstyp. Diese Optionen bestimmen, wie das DWG rasterisiert wird, bevor es in ein PDF eingebettet wird.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Schritt 4: PDF‑Optionen konfigurieren

Erstellen Sie eine Instanz von `PdfOptions` und fügen Sie die Rasterisierungseinstellungen hinzu. Dadurch wird Aspose.CAD mitgeteilt, wie der rasterisierte Inhalt in das endgültige PDF eingebettet werden soll.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Schritt 5: Als PDF speichern

Exportieren Sie schließlich die Zeichnung in eine PDF‑Datei. Die Methode `save` erhält den Ausgabepfad und die konfigurierten `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Wenn der Code abgeschlossen ist, finden Sie **Saved.pdf** in Ihrem Ordner `DWGDrawings`, bereit für die Verteilung oder Archivierung.

## Häufige Probleme & Tipps

- **Falsche Seitengröße** – Überprüfen Sie die Logik der Einheitumrechnung; nicht passende Koeffizienten können zu übergroßen Seiten führen.  
- **Fehlende Schriftarten oder Linienstärken** – Stellen Sie sicher, dass das DWG vor der Konvertierung auf externe Ressourcen verweist.  
- **Leistung bei großen Zeichnungen** – Erhöhen Sie die `DPI`‑Einstellung in `CadRasterizationOptions` nur, wenn höhere Qualität erforderlich ist; ein niedrigeres DPI beschleunigt die Verarbeitung.

## Häufig gestellte Fragen

**Q: Kann ich Aspose.CAD für Java mit anderen Java‑Frameworks verwenden?**  
A: Ja, Aspose.CAD für Java lässt sich nahtlos in gängige Java‑Frameworks wie Spring, Jakarta EE und Android integrieren.

**Q: Ist eine temporäre Lizenz für Aspose.CAD für Java verfügbar?**  
A: Ja, Sie können eine temporäre Lizenz **[hier](https://purchase.aspose.com/temporary-license/)** erhalten.

**Q: Wo finde ich Unterstützung für Aspose.CAD für Java?**  
A: Besuchen Sie das **[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19)** für Unterstützung durch die Community und Aspose‑Ingenieure.

**Q: Wie kann ich eine Lizenz für Aspose.CAD für Java erwerben?**  
A: Sie können eine Lizenz **[hier](https://purchase.aspose.com/buy)** erwerben.

**Q: Welche Einheiten unterstützt Aspose.CAD für Java?**  
A: Aspose.CAD für Java unterstützt sowohl metrische als auch imperiale Einheiten und erkennt das Einheitssystem der Zeichnung automatisch.

**Q: Kann ich DWG mit derselben API in andere Bildformate (z. B. PNG, JPEG) konvertieren?**  
A: Absolut. Ersetzen Sie `PdfOptions` durch die entsprechenden Rasterbildoptionen (z. B. `PngOptions`) und verwenden Sie dieselben `CadRasterizationOptions` erneut.

## Fazit

Dieses Tutorial zeigte, wie man **export dwg to pdf** und Rasterbilder mit Aspose.CAD für Java durchführt. Durch Befolgen der Schritt‑für‑Schritt‑Anleitung können Sie zuverlässige CAD‑Konvertierung in jede Java‑Anwendung integrieren, egal ob Sie PDFs für Dokumentation oder Rasterbilder für die Webanzeige benötigen.

---

**Letzte Aktualisierung:** 2025-12-18  
**Getestet mit:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}