---
date: 2026-02-17
description: Erfahren Sie, wie die Java‑CAD‑Bibliothek Aspose.CAD für Java DWG schnell
  und präzise in PDF oder Rasterbilder exportieren kann.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: DWG in PDF oder Raster exportieren mit der Java‑CAD‑Bibliothek Aspose.CAD für
  Java
url: /de/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

Let's craft final output.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG nach PDF oder Raster mit der java cad library Aspose.CAD für Java

## Einführung

In der dynamischen Welt des computerunterstützten Designs (CAD) ist ein effizientes Handling von Zeichnungen entscheidend. Mit der **java cad library** **Aspose.CAD for Java** können Sie **export dwg to pdf** — oder Rasterbilder — in nur wenigen Codezeilen. Dieses Tutorial führt Sie durch den gesamten Prozess, vom Laden einer DWG-Datei bis zur Erzeugung eines hochwertigen PDFs, und zeigt, warum Aspose.CAD Java die bevorzugte Bibliothek für CAD-Konvertierungsaufgaben ist.

## Schnelle Antworten
- **Was behandelt dieses Tutorial?** Exportieren von DWG-Dateien nach PDF oder Rasterbildern mit Aspose.CAD für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose temporäre Lizenz steht für die Evaluierung zur Verfügung; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Jede Java 8+ Runtime funktioniert mit der neuesten Aspose.CAD Java API.  
- **Kann ich DWG in andere Bildformate konvertieren?** Ja – dieselben Rasterisierungsoptionen ermöglichen die Ausgabe als PNG, JPEG, BMP usw.  
- **Wie lange dauert die Konvertierung?** In der Regel unter einer Sekunde für Standardzeichnungen; größere Dateien können einige Sekunden benötigen.

## Warum ist die java cad library die beste Wahl für DWG‑Konvertierung?

- **Pure Java‑Implementierung** – keine nativen DLLs oder externen Tools.  
- **Genaues Einheiten‑Handling** – metrische und imperiale Einheiten werden automatisch erkannt.  
- **Hochwertige Rasterausgabe** – fein abgestimmte DPI‑ und Seitengrößen‑Kontrolle.  
- **Vollständige PDF‑Unterstützung** – vektorbasierte PDF‑Erstellung ohne zusätzliche Abhängigkeiten.  
- **Flexibles Lizenzmodell** – starten Sie mit einer **temporary license aspose** für Tests und upgraden Sie, wenn Sie live gehen.

## Was bedeutet „export dwg to pdf“?

Das Exportieren von DWG nach PDF bedeutet, eine native AutoCAD‑Zeichnung in ein portables, geräteunabhängiges PDF‑Dokument zu konvertieren. Das resultierende PDF bewahrt Vektordaten, Ebenen und Skalierung und ist ideal zum Teilen, Drucken oder Archivieren.

## Warum Aspose.CAD Java für diese Konvertierung verwenden?

Weil die **java cad library** alles von der Einheitenkonvertierung bis zur Rasterisierung intern verarbeitet, vermeiden Sie die Komplexität von Drittanbieter‑Tools und erhalten konsistente Ergebnisse über alle Plattformen hinweg.

## Voraussetzungen

Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie:

- Grundkenntnisse in Java‑Programmierung.  
- Aspose.CAD für Java installiert haben. Wenn Sie es noch nicht heruntergeladen haben, erhalten Sie es **[hier](https://releases.aspose.com/cad/java/)**.  
- Eine DWG‑Datei zum Testen – das Beispiel **Bottom_plate.dwg** wird in diesem Leitfaden verwendet.

## Namespaces importieren

In Ihrem Java‑Projekt importieren Sie die notwendigen Klassen, um die Konvertierung zu starten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: DWG‑Datei laden

Laden Sie Ihre DWG‑Zeichnung mit der `Image`‑Klasse. Dadurch entsteht eine In‑Memory‑Repräsentation, mit der Aspose.CAD arbeiten kann.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Schritt 2: Einheitstyp bestimmen

Zu wissen, ob die Zeichnung metrische oder imperiale Einheiten verwendet, ist für die korrekte Skalierung entscheidend. Die Hilfsmethode `IsMetric` (Implementierung aus Platzgründen weggelassen) liefert einen booleschen Wert.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Schritt 3: Rasterisierungsoptionen festlegen

Abhängig vom Einheitssystem konfigurieren Sie Seitengröße, Skalierung und den Ziel‑Einheitstyp. Diese Optionen bestimmen, wie das DWG rasterisiert wird, bevor es in ein PDF eingebettet wird.

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

### Schritt 4: PDF‑Optionen konfigurieren (pdf options cad)

Erzeugen Sie eine `PdfOptions`‑Instanz und hängen Sie die Rasterisierungs‑Einstellungen an. Damit teilt Aspose.CAD mit, wie der rasterisierte Inhalt in das finale PDF eingebettet werden soll.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Schritt 5: Als PDF speichern

Exportieren Sie schließlich die Zeichnung in eine PDF‑Datei. Die `save`‑Methode erhält den Ausgabepfad und die konfigurierten `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Wenn der Code abgeschlossen ist, finden Sie **Saved.pdf** in Ihrem `DWGDrawings`‑Ordner, bereit für Verteilung oder Archivierung.

## Wie man DWG‑Rasterbilder mit der java cad library konvertiert

Falls Sie Rasterbilder statt eines PDFs benötigen, ersetzen Sie einfach `PdfOptions` durch die entsprechenden Raster‑Bildoptionen (z. B. `PngOptions`, `JpegOptions`). Die gleiche `CadRasterizationOptions`‑Instanz kann wiederverwendet werden, sodass Sie **convert dwg raster** Dateien mit minimalen Code‑Änderungen konvertieren können.

## Wie man PDF‑DWG mit pdf options cad erzeugt

Das obige Beispiel erzeugt bereits **pdf dwg** Ausgabe. Durch Anpassen von `pdfOptions` – zum Beispiel `pdfOptions.setCompress(true)` – können Sie die PDF‑Größe und -Qualität steuern. Das demonstriert die Flexibilität der **pdf options cad** API.

## Häufige Probleme & Tipps

- **Falsche Seitengröße** – Überprüfen Sie die Logik zur Einheitenumrechnung; falsche Koeffizienten können übergroße Seiten erzeugen.  
- **Fehlende Schriftarten oder Linienstärken** – Stellen Sie sicher, dass die DWG alle externen Ressourcen referenziert, bevor Sie konvertieren.  
- **Performance bei großen Zeichnungen** – Erhöhen Sie den `DPI`‑Wert in `CadRasterizationOptions` nur, wenn höhere Qualität nötig ist; ein niedrigerer DPI beschleunigt die Verarbeitung.  
- **Lizenzfragen** – Für die Evaluierung können Sie eine **temporary license aspose** nutzen; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.

## Häufig gestellte Fragen

**F: Kann ich Aspose.CAD für Java mit anderen Java‑Frameworks verwenden?**  
A: Ja, Aspose.CAD für Java lässt sich nahtlos in gängige Java‑Frameworks wie Spring, Jakarta EE und Android integrieren.

**F: Gibt es eine temporäre Lizenz für Aspose.CAD für Java?**  
A: Ja, Sie können eine temporäre Lizenz **[hier](https://purchase.aspose.com/temporary-license/)** erhalten.

**F: Wo finde ich Support für Aspose.CAD für Java?**  
A: Besuchen Sie das **[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19)** für Hilfe von der Community und den Aspose‑Entwicklern.

**F: Wie kann ich eine Lizenz für Aspose.CAD für Java erwerben?**  
A: Sie können eine Lizenz **[hier](https://purchase.aspose.com/buy)** erwerben.

**F: Welche Einheiten unterstützt Aspose.CAD für Java?**  
A: Aspose.CAD für Java unterstützt sowohl metrische als auch imperiale Einheiten und erkennt das Einheitensystem der Zeichnung automatisch.

**F: Kann ich DWG in andere Bildformate (z. B. PNG, JPEG) mit derselben API konvertieren?**  
A: Absolut. Ersetzen Sie `PdfOptions` durch die entsprechenden Raster‑Bildoptionen (z. B. `PngOptions`) und verwenden Sie dieselben `CadRasterizationOptions`.

## Fazit

Dieses Tutorial hat gezeigt, wie man **export dwg to pdf** und Rasterbilder mit der **java cad library** Aspose.CAD für Java exportiert. Durch Befolgen der Schritt‑für‑Schritt‑Anleitung können Sie zuverlässige CAD‑Konvertierung in jede Java‑Anwendung integrieren, egal ob Sie PDFs für Dokumentation oder Rasterbilder für die Webanzeige benötigen.

---

**Zuletzt aktualisiert:** 2026-02-17  
**Getestet mit:** Aspose.CAD für Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}