---
date: 2026-03-26
description: Erfahren Sie, wie Sie mit Aspose.CAD für .NET PDFs aus CAD erstellen
  und DXF in PDF konvertieren. Passen Sie die Stiftoptionen an, um beeindruckende
  Visualisierungen in PDF, PNG, BMP und mehr zu erzielen.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF aus CAD mit benutzerdefinierten Stiftoptionen erstellen – Aspose.CAD für
  .NET
url: /de/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verbessern Sie den CAD-Export mit benutzerdefinierten Stiftoptionen in Aspose.CAD für .NET

## Einführung

Wenn Sie **PDF aus CAD**-Dateien schnell und mit voller visueller Kontrolle erstellen müssen, bietet Ihnen Aspose.CAD für .NET genau das. Durch die Nutzung der Pen‑Support‑Funktion der Bibliothek können Sie Start‑ und End‑Caps, Linienverbindungen und andere Zeichenattribute definieren und PDFs erzeugen, die exakt so aussehen, wie Sie es wünschen. Dieses Tutorial führt Sie durch den gesamten Prozess – vom Laden einer DXF‑Datei bis zum Export eines fertigen PDFs – und zeigt zudem, wie dieselben Einstellungen wiederverwendet werden können, wenn Sie **CAD nach PNG exportieren** oder **CAD‑Bild rasterisieren** für andere Formate.

## Schnelle Antworten
- **Was bedeutet “create PDF from CAD”?** Es konvertiert vektorbasierte CAD‑Zeichnungen (z. B. DXF) in ein PDF‑Dokument, wobei Geometrie und Stil erhalten bleiben.  
- **Welche Formate unterstützen Stiftoptionen?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF und WMF.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert zum Testen; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich Linien‑Caps für andere Formate ändern?** Ja – Stiftoptionen gelten für jedes von Aspose.CAD unterstützte Rasterisierungsziel.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Was ist Pen‑Support beim CAD‑Export?

Pen‑Support ermöglicht es Ihnen, anzupassen, wie Linien gezeichnet werden, wenn eine CAD‑Zeichnung rasterisiert oder vektor‑rasterisiert wird. Sie können Eigenschaften wie `StartCap`, `EndCap`, `LineJoin` und `DashStyle` festlegen. Diese Einstellungen beeinflussen das endgültige Aussehen des exportierten Bildes oder PDFs und geben Ihnen eine feinkörnige Kontrolle über die visuelle Qualität.

## Warum benutzerdefinierte Stiftoptionen verwenden, wenn Sie **PDF aus CAD** erstellen?

- **Konsistentes Branding** – passen Sie Unternehmenslinienstile in allen Dokumenten an.  
- **Verbesserte Lesbarkeit** – dickere Caps und Verbindungen machen technische Zeichnungen auf dem Bildschirm und im Druck klarer.  
- **Cross‑Format‑Flexibilität** – dieselbe Stiftkonfiguration funktioniert für PNG, BMP und andere Rasterformate und spart Ihnen Zeit.

## Voraussetzungen

- Aspose.CAD für .NET installiert (Download von der [release page](https://releases.aspose.com/cad/net/)).  
- Grundkenntnisse von DXF (Drawing Exchange Format).  
- Vertrautheit mit C#‑Programmierung.

## Namespaces importieren

Um zu beginnen, stellen Sie sicher, dass Sie die erforderlichen Namespaces in Ihrem C#‑Projekt importieren:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Schritt 1: Richten Sie Ihr Dokumentenverzeichnis ein

Definieren Sie den Ordner, der die Quell‑CAD‑Datei enthält:

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das CAD‑Bild

Laden Sie die CAD‑Zeichnung (z. B. eine DXF‑Datei) in ein `Aspose.CAD.Image`‑Objekt:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Schritt 3: Rasterisierungsoptionen konfigurieren

Erstellen Sie Rasterisierungs‑ und PDF‑Optionsobjekte. Diese Objekte ermöglichen es Ihnen, zu steuern, wie die CAD‑Daten in ein Rasterbild oder eine PDF‑Seite umgewandelt werden:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Schritt 4: Stiftoptionen anpassen

Hier passen Sie den **Stift** an, der die Linien zeichnet. Sie können die Start‑ und End‑Caps auf `Flat`, `Round`, `Square` usw. setzen. Dies ist der Kern von “how to export CAD” mit dem gewünschten visuellen Stil:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Pro‑Tipp:* Experimentieren Sie mit `LineCap.Round` für glattere Linienenden, wenn Sie **CAD nach PNG exportieren**.

## Schritt 5: Vektor‑Rasterisierungsoptionen anwenden

Binden Sie die Rasterisierungseinstellungen an die PDF‑Optionen, damit der Exportprozess weiß, welche Stiftkonfiguration verwendet werden soll:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 6: Exportiertes PDF speichern

Erzeugen Sie schließlich die PDF‑Datei. Dieser Schritt **erstellt PDF aus CAD** mit den angewendeten benutzerdefinierten Stift‑Einstellungen:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

Sie können die `PdfOptions` durch `PngOptions`, `BmpOptions` usw. ersetzen, um **CAD nach PNG** oder andere Rasterformate zu exportieren, während Sie dieselbe Stiftkonfiguration beibehalten.

## Häufige Anwendungsfälle

- **Technische Dokumentation** – präzise Linienstile in Engineering‑PDFs einbetten.  
- **Automatisierte Berichtserstellung** – viele DXF‑Dateien stapelweise in PDFs mit einem einzigen Stiftprofil verarbeiten.  
- **Web‑Services** – stellen Sie eine API bereit, die hochgeladene DXF‑Dateien on‑the‑fly in PDFs konvertiert und dabei ein konsistentes Styling gewährleistet.

## Fehlerbehebung & häufige Stolperfallen

| Issue | Reason | Solution |
|-------|--------|----------|
| Exportierte Linien erscheinen dicker als erwartet | DPI ist höher als beabsichtigt | Setzen Sie `rasterizationOptions.PageWidth` / `PageHeight` oder passen Sie `Resolution` an. |
| Stiftoptionen werden für PNG‑Ausgabe ignoriert | Verwendung von `ImageOptions` anstelle von `VectorRasterizationOptions` | Stellen Sie sicher, dass Sie `rasterizationOptions.PenOptions` vor dem Speichern zuweisen. |
| PDF‑Datei ist leer | Quell‑DXF‑Pfad ist falsch oder die Datei ist beschädigt | Überprüfen Sie `sourceFilePath` und stellen Sie sicher, dass das DXF ohne Ausnahmen geladen wird. |

## FAQ's

### Q1: Kann ich diese Stiftoptionen für andere Bildformate außer PDF verwenden?

A1: Ja, die Stiftoptionen können auf verschiedene Bildformate wie PNG, BMP, GIF, JPEG und mehr angewendet werden.

### Q2: Wo finde ich zusätzliche Dokumentation für Aspose.CAD für .NET?

A2: Siehe die [documentation](https://reference.aspose.com/cad/net/) für umfassende Informationen und Beispiele.

### Q3: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?

A3: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Wie kann ich temporäre Lizenzen für Aspose.CAD für .NET erhalten?

A4: Besuchen Sie die [temporary license page](https://purchase.aspose.com/temporary-license/) für temporäre Lizenzierungsoptionen.

### Q5: Wo kann ich Community‑Support für Aspose.CAD für .NET erhalten?

A5: Treten Sie mit der Community im [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) in Kontakt.

## Zusätzliche häufig gestellte Fragen

**Q: Wie konvertiere ich programmgesteuert DXF zu PDF?**  
A: Laden Sie das DXF mit `Image.Load`, konfigurieren Sie `CadRasterizationOptions` und `PdfOptions` und rufen Sie dann `Save` wie in den obigen Schritten gezeigt auf.

**Q: Kann ich ein CAD‑Bild rasterisieren, ohne ein PDF zu erstellen?**  
A: Ja – verwenden Sie `PngOptions`, `BmpOptions` oder eine andere Rasterformat‑Klasse und weisen Sie dieselben `rasterizationOptions` zu, um eine hochwertige Rasterisierung zu erreichen.

**Q: Ist es möglich, die Linienbreite beim Erstellen eines PDFs aus CAD zu ändern?**  
A: Passen Sie `rasterizationOptions.CustomLineWidth` an oder ändern Sie die Eigenschaft `PenOptions.Width` vor dem Speichern.

**Q: Unterstützt die Bibliothek 3D‑DXF‑Dateien?**  
A: Aspose.CAD konzentriert sich auf 2D‑Vektordaten; 3D‑Entitäten werden bei der Rasterisierung ignoriert.

**Q: Welche Version von Aspose.CAD wird für diese Funktionen benötigt?**  
A: Pen‑Support ist seit Version 20.9 verfügbar; jede neuere Version funktioniert.

---

**Zuletzt aktualisiert:** 2026-03-26  
**Getestet mit:** Aspose.CAD für .NET 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}