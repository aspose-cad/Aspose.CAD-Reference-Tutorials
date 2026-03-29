---
date: 2026-03-29
description: Erfahren Sie, wie Sie mit Aspose.CAD für .NET in dieser Schritt‑für‑Schritt‑Anleitung
  PDF aus CAD erstellen, die Canvas‑Größe festlegen und CAD in PDF oder TIFF exportieren.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Wie man ein PDF aus CAD erstellt: Zeichenflächengröße und Modus in Aspose.CAD
  für .NET festlegen'
url: /de/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Festlegen der Canvas-Größe und des Modus in Aspose.CAD für .NET

## Einführung

Bereit, **PDF aus CAD**-Dateien zu erstellen, während Sie die Ausgabedimensionen kontrollieren? In diesem Tutorial führen wir Sie durch das Festlegen der Canvas-Größe und des Modus, das Laden einer CAD-Datei und das Exportieren in PDF oder TIFF mit Aspose.CAD für .NET. Egal, ob Sie **DXF in PDF konvertieren**, hochauflösende Zeichnungen erzeugen oder einfach den Rasterisierungsbereich anpassen müssen, die nachfolgenden Schritte bieten Ihnen eine solide, produktionsbereite Lösung.

## Schnelle Antworten
- **Was bedeutet „PDF aus CAD erstellen“?** Konvertierung einer CAD-Zeichnung (z. B. DXF, DWG) in ein PDF-Dokument, das Vektor‑ und Rasterdetails bewahrt.  
- **Welche Option steuert die Ausgabengröße?** `CadRasterizationOptions.PageWidth` und `PageHeight` (Canvas-Größe).  
- **Kann ich auch nach TIFF exportieren?** Ja – verwenden Sie `TiffOptions` mit denselben Rasterisierungseinstellungen.  
- **Benötige ich eine Lizenz für die Produktion?** Eine kommerzielle Lizenz ist erforderlich; eine kostenlose Testversion ist verfügbar.  
- **Unterstützte .NET-Versionen?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Was bedeutet „PDF aus CAD erstellen“?
Das Erstellen eines PDFs aus CAD bedeutet, die CAD-Zeichnung in ein seitenorientiertes Format (PDF) zu rendern, das angezeigt, gedruckt oder geteilt werden kann, ohne dass CAD-Software erforderlich ist. Aspose.CAD übernimmt die schwere Arbeit und ermöglicht es Ihnen, Canvas-Größe, Skalierung und Ausgabeformat festzulegen.

## Warum die Canvas-Größe festlegen, wenn man ein PDF aus CAD erstellt?
Das Festlegen der Canvas-Größe gibt Ihnen präzise Kontrolle über Auflösung und Abmessungen des resultierenden PDF oder TIFF. Dies ist besonders nützlich, wenn:
- Vorbereitung von Zeichnungen für den Druck auf spezifischen Papiergrößen.  
- Erzeugen von Thumbnails oder hochauflösenden Bildern für die Webvorschau.  
- Sicherstellung eines konsistenten Layouts über mehrere Dokumente hinweg.

## Voraussetzungen

- Aspose.CAD Bibliothek: Laden Sie die Aspose.CAD-Bibliothek herunter und installieren Sie sie von der [Aspose.CAD-Website](https://releases.aspose.com/cad/net/).
- Entwicklungsumgebung: Stellen Sie sicher, dass Sie eine .NET-Entwicklungsumgebung auf Ihrem Rechner eingerichtet haben.
- Beispiel-CAD-Datei: Für dieses Tutorial verwenden wir eine Beispiel‑DXF‑Datei. Sie finden eine solche in der [Aspose.CAD-Dokumentation](https://reference.aspose.com/cad/net/).

## Namespaces importieren

Zuerst importieren Sie die für die CAD-Verarbeitung erforderlichen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## So erstellen Sie ein PDF aus CAD mit benutzerdefinierter Canvas-Größe

### Schritt 1: CAD-Datei laden

Wir beginnen mit dem **Laden der CAD-Datei** (z. B. einer DXF) in ein `Image`‑Objekt. Dies ist der Punkt, an dem Sie die **CAD-Datei** in den Speicher laden.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Schritt 2: CadRasterizationOptions erstellen

Erstellen Sie eine Instanz von `CadRasterizationOptions` und definieren Sie die Canvas-Größe. Die Eigenschaften `PageWidth` und `PageHeight` ermöglichen es Ihnen, die **Canvas-Größe** auf die genauen Abmessungen einzustellen, die Sie benötigen.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Schritt 3: PdfOptions erstellen (CAD nach PDF exportieren)

Verknüpfen Sie die Rasterisierungseinstellungen mit einem `PdfOptions`‑Objekt. Diese Konfiguration ermöglicht es Ihnen, **CAD nach PDF zu exportieren** mit dem von Ihnen definierten benutzerdefinierten Canvas.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Schritt 4: Export nach PDF (DXF nach PDF konvertieren)

Speichern Sie nun das Bild als PDF. Dieser Schritt **erstellt ein PDF aus CAD** mithilfe der von uns festgelegten Optionen.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Schritt 5: TiffOptions erstellen (CAD nach TIFF exportieren)

Falls Sie ebenfalls ein Rasterbild benötigen, konfigurieren Sie `TiffOptions`. Die gleichen Rasterisierungseinstellungen werden wiederverwendet, sodass der **Export von CAD nach TIFF** die Canvas-Größe berücksichtigt.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Schritt 6: Export nach TIFF

Speichern Sie schließlich die Zeichnung als TIFF‑Datei.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Häufige Probleme und Lösungen

- **Canvas erscheint abgeschnitten** – Stellen Sie sicher, dass `AutomaticLayoutsScaling` auf `true` und `NoScaling` auf `false` gesetzt ist, damit die Zeichnung an den Canvas angepasst wird.  
- **PDF mit niedriger Auflösung** – Erhöhen Sie `PageWidth`/`PageHeight` oder setzen Sie `Resolution` in `CadRasterizationOptions`.  
- **Datei nicht gefunden-Fehler** – Stellen Sie sicher, dass `MyDir` auf ein gültiges Verzeichnis zeigt und der DXF-Dateiname exakt übereinstimmt.

## Häufig gestellte Fragen

### F1: Kann ich Aspose.CAD mit anderen .NET-Bibliotheken verwenden?
A1: Ja, Aspose.CAD lässt sich nahtlos in andere .NET-Bibliotheken integrieren und bietet erweiterte Möglichkeiten zur CAD‑Manipulation.

### F2: Ist eine kostenlose Testversion für Aspose.CAD verfügbar?
A2: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion ausprobieren. Besuchen Sie [hier](https://releases.aspose.com/), um zu beginnen.

### F3: Wie kann ich Support für Aspose.CAD erhalten?
A3: Für Support und Diskussionen besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19).

### F4: Wo finde ich umfassende Dokumentation für Aspose.CAD?
A4: Konsultieren Sie die [Aspose.CAD‑Dokumentation](https://reference.aspose.com/cad/net/) für detaillierte Informationen und Beispiele.

### F5: Wie kaufe ich Aspose.CAD für .NET?
A5: Um Aspose.CAD zu erwerben, besuchen Sie die [Kaufseite](https://purchase.aspose.com/buy).

**Zusätzliche Fragen & Antworten**

**F: Kann ich eine mehrseitige CAD-Zeichnung in ein einzelnes PDF exportieren?**  
A: Ja. Setzen Sie `PageCount` in `CadRasterizationOptions` und die Bibliothek fügt die Seiten zu einem PDF zusammen.

**F: Beeinflusst die Canvas-Größe die Qualität von Vektordaten?**  
A: Vektordaten bleiben auflösungsunabhängig; die Canvas-Größe wirkt sich nur auf rasterisierte Elemente und die Bildauflösung aus.

---

**Zuletzt aktualisiert:** 2026-03-29  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}