---
date: 2026-08-23
description: Erfahren Sie, wie Sie ein viewport dwg c# mit Aspose.CAD erstellen. Dieser
  Leitfaden behandelt loading einer DWG-Datei, configuring rasterization, defining
  a viewport und saving des Ergebnisses als PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Rendering von DWG-Dokumenten in C#
og_description: Erfahren Sie, wie Sie ein viewport dwg c# mit Aspose.CAD in .NET erstellen.
  Dieser Schritt‑für‑Schritt‑Leitfaden zeigt loading, rasterizing, defining viewports
  und saving to PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Wie man ein viewport dwg c# mit Aspose.CAD für .NET erstellt
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Wie man ein viewport dwg c# mit Aspose.CAD für .NET erstellt
url: /de/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-Dokumente in C# rendern – Viewport dwg c# erstellen Tutorial

## Einleitung

In diesem umfassenden Tutorial lernen Sie, wie Sie **create viewport dwg c#** mit Aspose.CAD erstellen und eine DWG-Datei in PDF rendern. Ob Sie ein bestimmtes Layout extrahieren, ein druckbares Blatt erzeugen oder eine CAD-Ansicht in einen Bericht einbetten müssen, die Steuerung des Viewports gibt Ihnen präzise Rendering‑Kontrolle. Aspose.CAD unterstützt **20+ CAD formats** und kann Dateien mit Tausenden von Entitäten verarbeiten, ohne das gesamte Dokument in den Speicher zu laden, was es ideal für Hochleistungs‑.NET‑Anwendungen macht.

## Schnelle Antworten
- **Was ist der erste Schritt?** Laden Sie die DWG-Datei mit `CadImage.Load`.
- **Welche Klasse definiert den Anzeigebereich?** `Viewport` innerhalb von `CadRasterizationOptions`.
- **Kann ich in PDF ausgeben?** Ja, mittels `PdfOptions` nach der Rasterisierung.
- **Benötige ich eine Lizenz für die Produktion?** Eine kommerzielle Lizenz ist erforderlich; eine kostenlose Testversion funktioniert für die Evaluierung.
- **Wird .NET Core unterstützt?** Absolut – Aspose.CAD funktioniert mit .NET Framework, .NET Core und .NET 5/6.

## Voraussetzungen

Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie folgendes haben:

- Grundkenntnisse in C#‑Programmierung.
- Visual Studio (beliebige aktuelle Edition) installiert.
- Aspose.CAD‑Bibliothek zu Ihrem Projekt hinzugefügt. Sie können sie von der [Aspose.CAD download page](https://releases.aspose.com/cad/net/) herunterladen.
- Eine Beispiel‑DWG‑Datei, z. B. **Bottom_plate.dwg**, zum Mitverfolgen.

## Namespaces importieren

Fügen Sie die erforderlichen `using`‑Direktiven am Anfang Ihrer C#‑Datei hinzu, damit der Compiler die Aspose.CAD‑Typen finden kann.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Jetzt, da die Umgebung bereit ist, gehen wir die Implementierung Schritt für Schritt durch.

## Wie erstelle ich viewport dwg c#?

Um einen benutzerdefinierten Viewport zu erstellen, laden Sie zunächst die DWG-Datei in ein `CadImage`‑Objekt, konfigurieren dann `CadRasterizationOptions` mit dem gewünschten Layout und der Skalierung. Definieren Sie den Bereich, den Sie anzeigen möchten, erzeugen ein `CadVportTableObject` mit dem berechneten Zentrum, der Höhe und dem Seitenverhältnis, ersetzen den aktiven Viewport, setzen ggf. PDF‑Optionen und speichern schließlich das Ergebnis.

## Schritt 1: DWG-Datei laden

`CadImage.Load` lädt eine DWG-Datei in ein `CadImage`‑Objekt, das die CAD‑Zeichnung im Speicher repräsentiert.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

`CadRasterizationOptions` gibt an, wie die CAD‑Zeichnung rasterisiert wird, einschließlich Layout‑Auswahl, Skalierung und Ausgabengröße.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Schritt 3: Zeichenbereich definieren

`Point` definiert die X‑ und Y‑Koordinaten der oberen linken Ecke des zu rendernden Bereichs.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Schritt 4: Neuen Viewport erstellen

`CadVportTableObject` stellt ein Viewport‑Objekt dar, das den sichtbaren Bereich und das Seitenverhältnis der gerenderten Zeichnung steuert.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Schritt 5: Aktiven Viewport ersetzen

Die Schleife ersetzt den aktiven Viewport durch den neu erstellten, um die benutzerdefinierten Ansichtseinstellungen anzuwenden.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Schritt 6: PDF‑Optionen konfigurieren

`PdfOptions` konfiguriert PDF‑Ausgabeparameter wie Kompression und Metadaten.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 7: Gerendertes DWG als PDF speichern

`image.Save` schreibt das gerenderte Bild mit den angegebenen Formatoptionen in eine Datei.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Warum einen benutzerdefinierten Viewport beim Rendern von DWG verwenden?

Ein benutzerdefinierter Viewport ermöglicht es, ein bestimmtes Layout oder einen Bereich zu isolieren, wodurch die Dateigröße reduziert und die Rendering‑Geschwindigkeit verbessert wird. Aspose.CAD kann ein 300‑seitiges DWG in weniger als 2 Sekunden rendern, wenn ein fokussierter Viewport verwendet wird, im Vergleich zum Rendering der gesamten Zeichnung, das mehrere Sekunden länger dauern kann.

## Häufige Probleme und Lösungen

- **Leere Ausgabe** – Stellen Sie sicher, dass die Viewport‑Koordinaten innerhalb der Zeichenbereichsgrenzen liegen; verwenden Sie `CadImage.Size`, um die Grenzen zu überprüfen.
- **Fehlende Ebenen** – Setzen Sie `CadRasterizationOptions.Layouts` auf den korrekten Layout‑Namen; andernfalls kann das Standard‑Layout leer sein.
- **Leistungsverlust** – Deaktivieren Sie Anti‑Aliasing in `CadRasterizationOptions`, wenn Sie nur eine schnelle Vorschau benötigen.

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD mit anderen CAD‑Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene Formate, darunter DWG, DXF, DWF und mehr als 20 weitere CAD‑Typen.

### Q2: Ist Aspose.CAD mit .NET Core kompatibel?

A2: Ja, Aspose.CAD funktioniert mit .NET Framework, .NET Core und den neuesten .NET‑Versionen.

### Q3: Wie kann ich verschiedene Layouts in einer DWG-Datei handhaben?

A3: Geben Sie das gewünschte Layout über die `Layouts`‑Eigenschaft von `CadRasterizationOptions` vor dem Rendern an.

### Q4: Gibt es Lizenzüberlegungen bei der Verwendung von Aspose.CAD?

A4: Für Lizenzdetails besuchen Sie die [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Wo finde ich zusätzliche Unterstützung?

A5: Besuchen Sie das [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) für Community‑Hilfe und Diskussionen.

### Q6: Kann ich direkt nach PNG statt PDF rendern?

A6: Ja, ändern Sie `PdfOptions` zu `PngOptions` und rufen Sie `image.Save("output.png", pngOptions)` auf.

### Q7: Wie bette ich das gerenderte Bild in eine Windows‑Forms‑Anwendung ein?

A7: Laden Sie das gespeicherte Bild mit `Image.FromFile("output.png")` in ein `PictureBox`‑Steuerelement.

## Fazit

Sie wissen jetzt, wie Sie **create viewport dwg c#** erstellen und eine DWG-Datei mit Aspose.CAD in PDF (oder andere Rasterformate) rendern. Durch das Beherrschen der Viewport‑Manipulation erhalten Sie eine feinkörnige Kontrolle über die visuelle Ausgabe, was für die Erstellung genauer technischer Zeichnungen, Berichte oder Thumbnails unerlässlich ist. Erkunden Sie zusätzliche Rasterisierungs‑Einstellungen, experimentieren Sie mit verschiedenen Ausgabeformaten und integrieren Sie den Code in größere .NET‑Dienste oder Desktop‑Utilities.

---

**Last Updated:** 2026-08-23  
**Tested with:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Verwandte Tutorials

- [Wie man Viewport beim Konvertieren von DWG zu PDF mit Koordinaten in C# festlegt – Aspose.CAD Tutorial](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Erfahren Sie, wie Sie CAD‑Rasterisierungsoptionen festlegen – Bestimmte Layouts mit Aspose.CAD nach PDF exportieren](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Wie man DWG mit Aspose.CAD für .NET in PDF und Rasterbilder konvertiert](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}