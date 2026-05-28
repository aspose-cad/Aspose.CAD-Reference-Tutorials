---
date: 2026-03-02
description: Erfahren Sie, wie Sie mit Aspise.CAD für .NET ein einzelnes PDF mit verschiedenen
  Layouts erstellen – CAD in PDF konvertieren, DWG nach PDF exportieren und CAD effizient
  als PDF speichern.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Wie man ein einzelnes PDF mit verschiedenen Layouts erstellt – Aspose.CAD‑Leitfaden
url: /de/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein einzelnes PDF mit verschiedenen Layouts erstellt – Aspose.CAD Leitfaden

## Einleitung

Wenn Sie **einzelne PDF**‑Dateien erstellen müssen, die mehrere CAD‑Layouts enthalten, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie Schritt für Schritt durch die genauen Schritte, die erforderlich sind, um CAD‑Zeichnungen in ein PDF‑Dokument zu konvertieren und dabei mehrere Layouts zu verarbeiten. Sie werden sehen, wie Aspose.CAD für .NET das **convert CAD to PDF**, **export DWG to PDF**, und **save CAD as PDF** mit nur wenigen Zeilen C#‑Code erleichtert.

## Schnelle Antworten
- **Worum geht es in diesem Tutorial?** Generierung eines PDFs, das mehrere CAD‑Layouts enthält.  
- **Welche Bibliothek wird verwendet?** Aspose.CAD für .NET.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Unterstützte CAD‑Formate?** DWG, DXF, DGN und viele weitere.  
- **Typische Implementierungszeit?** Etwa 10‑15 Minuten für eine grundlegende Konvertierung.

## Was bedeutet “einzelnes PDF erstellen” im CAD‑Kontext?

Ein einzelnes PDF zu erstellen bedeutet, eine CAD‑Quelldatei, die mehrere Layout‑Definitionen (Papierbereiche) enthalten kann, zu nehmen und jedes Layout zu separaten Seiten eines einzigen PDF‑Dokuments zusammenzuführen. Dies ist besonders nützlich für Architekturpläne, technische Schemata oder jede Situation, in der ein Kunde ein konsolidiertes PDF‑Paket erwartet.

## Warum Aspose.CAD für diese Aufgabe verwenden?

- **Keine externen Abhängigkeiten** – reines .NET, keine AutoCAD‑Installation erforderlich.  
- **Vollständige Kontrolle über die Rasterisierung** – Sie können Seitengröße, DPI und benutzerdefinierte Layout‑Abmessungen festlegen.  
- **Hoch‑präzises Rendering** – Vektordaten werden, wo möglich, beibehalten, was ein klares Ergebnis gewährleistet.  
- **Batch‑fähig** – derselbe Code kann in einer Schleife platziert werden, um viele Zeichnungen automatisch zu verarbeiten.

## Voraussetzungen

- Aspose.CAD für .NET: Stellen Sie sicher, dass Aspose.CAD für .NET installiert ist. Sie können es von [hier](https://releases.aspose.com/cad/net/) herunterladen.  
- Entwicklungsumgebung: Richten Sie eine .NET‑Entwicklungsumgebung ein und besitzen Sie Grundkenntnisse in der C#‑Programmierung.

## Namespaces importieren

In Ihrem C#‑Projekt fügen Sie die notwendigen Namespaces ein, um die Funktionalitäten von Aspose.CAD für .NET zu nutzen:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: CAD‑Bild laden

Laden Sie zunächst die Quell‑CAD‑Datei (z. B. eine DWG‑Zeichnung). Die Klasse `CadImage` gibt Ihnen Zugriff auf alle Layouts in der Datei.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Schritt 2: Rasterisierungsoptionen anpassen

Definieren Sie, wie jedes Layout rasterisiert werden soll. Sie können eine Standard‑Seitengröße festlegen und diese dann für bestimmte Layouts mit `LayoutPageSizes` überschreiben.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Pro‑Tipp:** Passen Sie die DPI (`rasterizationOptions.Resolution`) an, wenn Sie eine höher aufgelöste Ausgabe für detaillierte Zeichnungen benötigen.

### Schritt 3: PDF‑Optionen definieren

Verpacken Sie die Rasterisierungseinstellungen in ein `PdfOptions`‑Objekt. Dadurch wird Aspose.CAD angewiesen, die CAD‑Daten direkt in einen PDF‑Stream zu rendern.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Schritt 4: Als PDF speichern

Rufen Sie schließlich `Save` auf der `CadImage`‑Instanz auf, übergeben Sie den Ziel‑PDF‑Dateinamen und die vorbereiteten Optionen. Die Bibliothek erzeugt ein einzelnes PDF, das für jedes konfigurierte Layout eine Seite enthält.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Nach diesem Aufruf haben Sie ein PDF, das die Layouts „ANSI C Plot“ und „8.5 x 11 Plot“ zu einem zusammenhängenden Dokument kombiniert.

## Häufige Fallstricke & Fehlersuche

| Problem | Grund | Lösung |
|---------|-------|--------|
| Layouts missing in PDF | `LayoutPageSizes` nicht für einen Layout‑Namen definiert | Überprüfen Sie die genauen Layout‑Namen in der CAD‑Datei (Groß‑/Kleinschreibung beachten). |
| Low‑quality output | Standard‑DPI ist 96 | Setzen Sie `rasterizationOptions.Resolution = 300` (oder höher) vor dem Speichern. |
| File not found | Falscher `MyDir`‑Pfad | Verwenden Sie `Path.Combine`, um plattformunabhängige Pfade zu erstellen. |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für .NET mit anderen CAD‑Formaten verwenden?

A1: Ja, Aspose.CAD für .NET unterstützt verschiedene CAD‑Formate wie DWG, DXF, DGN und weitere.

### Q2: Gibt es eine kostenlose Testversion?

A2: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) ausprobieren.

### Q3: Wie kann ich Support für Aspose.CAD für .NET erhalten?

A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

### Q4: Wo finde ich ausführliche Dokumentation?

A4: Sie finden die Dokumentation [hier](https://reference.aspose.com/cad/net/).

### Q5: Kann ich eine Lizenz für Aspose.CAD für .NET erwerben?

A5: Ja, Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben.

**Zusätzliche Fragen & Antworten**

**Q:** Wie exportiere ich **DWG zu PDF** mit benutzerdefinierten Seitengrößen?  
**A:** Verwenden Sie `CadRasterizationOptions.LayoutPageSizes`, um jedes DWG‑Layout den gewünschten PDF‑Seitendimensionen zuzuordnen, wie in Schritt 2 gezeigt.

**Q:** Ist es möglich, **CAD als PDF** zu speichern, ohne Vektordaten zu rasterisieren?  
**A:** Aspose.CAD rasterisiert beim Erstellen von PDF immer, Sie können jedoch die DPI erhöhen, um die visuelle Treue zu bewahren.

## Fazit

In diesem Leitfaden haben wir gezeigt, wie man **einzelne PDF**‑Dateien aus CAD‑Zeichnungen mit mehreren Layouts erstellt, wobei Aspose.CAD für .NET verwendet wird. Sie verfügen nun über die Bausteine, um **CAD zu PDF** zu **konvertieren**, **DWG zu PDF** zu **exportieren** und **CAD als PDF** in einem einzigen, automatisierten Workflow **zu speichern**. Experimentieren Sie mit verschiedenen Rasterisierungs‑Einstellungen, um die Qualitätsanforderungen Ihres Projekts zu erfüllen, und integrieren Sie diesen Code bei Bedarf in größere Batch‑Verarbeitungspipelines.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-03-02  
**Getestet mit:** Aspose.CAD für .NET 24.11  
**Autor:** Aspose