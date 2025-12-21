---
date: 2025-12-21
description: Erfahren Sie, wie Sie CAD‑Layouts mit Aspose.CAD für Java in PDF exportieren
  – ein schneller, zuverlässiger Weg, PDFs aus CAD‑Dateien zu erstellen.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: Wie man CAD-Layouts mit Aspose.CAD für Java in PDF exportiert
url: /de/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man CAD‑Layouts mit Aspose.CAD für Java in PDF exportiert

## Einführung

In diesem Tutorial zeigen wir Ihnen **wie man CAD**‑Layouts mit Aspose.CAD für Java in PDF exportiert. Egal, ob Sie mit DWG, DXF oder anderen CAD‑Formaten arbeiten, dieser Leitfaden führt Sie Schritt für Schritt durch einen sauberen, programmgesteuerten Ansatz, um PDF aus CAD‑Dateien schnell und zuverlässig zu erzeugen.

## Schnellantworten
- **Was macht die Bibliothek?** Sie konvertiert CAD‑Zeichnungen (DWG, DXF, DWF usw.) in PDF, Rasterbilder und andere Formate.  
- **Welche Sprache wird verwendet?** Java – der Code läuft auf jeder JVM‑kompatiblen Plattform.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich DWG in PDF in Java konvertieren?** Ja – dieselbe API unterstützt **dwg to pdf java**‑Konvertierungen.  
- **Was sind die Hauptschritte?** CAD‑Datei laden, Rasterisierungsoptionen festlegen, PDF‑Optionen konfigurieren und das Ergebnis speichern.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.CAD für Java: Stellen Sie sicher, dass die Bibliothek installiert ist. Sie können sie von der Aspose‑Website [hier](https://releases.aspose.com/cad/java/) herunterladen.

- Java‑Entwicklungsumgebung: Vergewissern Sie sich, dass eine Java‑Entwicklungsumgebung auf Ihrem Rechner eingerichtet ist.

Jetzt, wo alles bereit ist, können wir mit dem Tutorial starten.

## Was bedeutet „how to export cad“?

Das Exportieren von CAD bedeutet, native CAD‑Zeichnungsdaten (wie DWG, DXF oder DWF) in ein universeller lesbares Format wie PDF zu konvertieren. Dieser Vorgang ist wichtig, um Designs mit Stakeholdern zu teilen, die keine CAD‑Software installiert haben.

## Warum Aspose.CAD für Java zum Export von CAD nach PDF verwenden?

- **Hohe Treue** – Vektorgrafiken bleiben erhalten, und Rasterisierungsoptionen ermöglichen eine feine Qualitätskontrolle.  
- **Keine externen Abhängigkeiten** – reines Java, keine nativen DLLs oder COM‑Komponenten.  
- **Unterstützt mehrere Formate** – Sie können auch **generate pdf from cad**‑Dateien erzeugen, die in DWG, DWF oder anderen Formaten erstellt wurden.  
- **Skalierbar für Batch‑Jobs** – ideal für serverseitige Automatisierung, CI‑Pipelines oder Desktop‑Utilities.

## Namespaces importieren

Importieren Sie in Ihrem Java‑Code die erforderlichen Namespaces. Diese Importe stellen den Zugriff auf die Klassen und Methoden bereit, die für die Arbeit mit Aspose.CAD für Java nötig sind.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Schritt 1: CAD‑Datei laden

Laden Sie die CAD‑Datei in Ihre Java‑Anwendung mit der Methode `Image.load`. Ersetzen Sie `"conic_pyramid.dxf"` durch den Pfad zu Ihrer CAD‑Datei.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Schritt 2: Rasterisierungsoptionen festlegen

Erzeugen Sie eine Instanz von `CadRasterizationOptions`, um zu definieren, wie die CAD‑Entitäten rasterisiert werden sollen. Passen Sie Parameter wie Seitenbreite, Seitenhöhe und Layout‑Skalierung an Ihre Anforderungen an.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Schritt 3: PDF‑Optionen festlegen

Erzeugen Sie eine Instanz von `PdfOptions` und verknüpfen Sie sie mit den Rasterisierungsoptionen. Zusätzlich können Sie Grafikoptionen für den PDF‑Export festlegen, z. B. Glättungsmodus, Text‑Rendering‑Hint und Interpolationsmodus.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Schritt 4: Export nach PDF

Exportieren Sie schließlich die CAD‑Layouts in eine PDF‑Datei mit der `save`‑Methode des `cadImage`‑Objekts.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|--------|-----|
| **Leere PDF‑Ausgabe** | Rasterisierungsoptionen nicht korrekt gesetzt (z. B. falscher Layout‑Name) | Stellen Sie sicher, dass `rasterizationOptions.setLayouts()` mit den Layout‑Namen in Ihrer CAD‑Datei übereinstimmt. |
| **Bilder mit niedriger Auflösung** | `PageWidth`/`PageHeight` zu klein | Erhöhen Sie die Seitengröße oder setzen Sie eine höhere DPI über `rasterizationOptions.setResolution()`. |
| **Nicht unterstützte CAD‑Version** | Ältere DWG/DXF‑Versionen benötigen ein neueres Aspose.CAD‑Build | Laden Sie die neueste Bibliotheksversion von der Aspose‑Site herunter. |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF, DWF und mehr. Die vollständige Liste finden Sie in der Dokumentation [hier](https://reference.aspose.com/cad/java/).

### Q2: Gibt es eine kostenlose Testversion von Aspose.CAD für Java?

A2: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) ausprobieren.

### Q3: Wie erhalte ich Support für Aspose.CAD für Java?

A3: Besuchen Sie das Aspose.CAD‑Forum [hier](https://forum.aspose.com/c/cad/19) für Community‑Support. Für Premium‑Support können Sie eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben.

### Q4: Was ist der Unterschied zwischen automatischer und manueller Layout‑Skalierung?

A4: Die automatische Layout‑Skalierung passt die Layout‑Größe basierend auf den angegebenen Seitenabmessungen an, während die manuelle Skalierung Ihnen erlaubt, benutzerdefinierte Skalierungswerte festzulegen.

### Q5: Kann ich das Aussehen exportierter PDF‑Dateien anpassen?

A5: Ja, Sie können die Grafikoptionen im Code anpassen, um Qualität und Erscheinungsbild des exportierten PDFs zu steuern.

### Q6: Unterstützt Aspose.CAD die **dwg to pdf java**‑Konvertierung direkt?

A6: Absolut. Die gleichen Rasterisierungs‑ und PDF‑Optionen funktionieren für DWG‑Dateien und ermöglichen nahtlose **dwg to pdf java**‑Konvertierungen.

### Q7: Gibt es eine Möglichkeit, **generate pdf from cad** zu erstellen, ohne in ein Bitmap zu rasterisieren?

A7: Durch Setzen von `rasterizationOptions.setContentAsBitmap(false)` können Sie Vektordaten, wo möglich, beibehalten und so ein echtes vektor‑basiertes PDF erzeugen.

---

**Zuletzt aktualisiert:** 2025-12-21  
**Getestet mit:** Aspose.CAD für Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}