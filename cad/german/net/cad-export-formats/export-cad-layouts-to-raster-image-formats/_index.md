---
date: 2026-03-21
description: Erfahren Sie, wie Sie DXF in PNG und andere Rasterformate mit Aspose.CAD
  für .NET konvertieren. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung für einen
  nahtlosen CAD‑Layer‑Export.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DXF in PNG mit Aspose.CAD für .NET konvertieren
url: /de/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von CAD-Layouts in Rasterbildformate mit Aspose.CAD für .NET

## Einführung

Möchten Sie effizient **convert dxf to png** und andere Rasterbildformate mit Aspose.CAD für .NET konvertieren? Diese Schritt‑für‑Schritt‑Anleitung führt Sie durch den Prozess, liefert detaillierte Anweisungen und Code‑Snippets, um die Aufgabe reibungslos zu erledigen. Egal, ob Sie ein erfahrener Entwickler oder ein Neuling bei Aspose.CAD sind, dieses Tutorial richtet sich an alle Erfahrungsstufen.

### Schnelle Antworten
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.CAD for .NET  
- **Welches primäre Format wird standardmäßig unterstützt?** JPEG, PNG, BMP und TIFF Rasterbilder  
- **Kann ich bestimmte CAD‑Layer exportieren?** Ja – verwenden Sie `CadRasterizationOptions.Layers`, um einzelne Layer anzusprechen  
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.CAD‑Lizenz ist für die Nutzung außerhalb der Testversion erforderlich  
- **Unterstützte .NET‑Versionen?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Was ist **convert dxf to png**?

Das Konvertieren einer DXF‑Datei (Drawing Exchange Format) in PNG bedeutet, vektorbasierte CAD‑Daten in ein pixelbasiertes Bild zu rasterisieren. Dies ist nützlich, wenn Sie CAD‑Zeichnungen in Webseiten, Berichte oder jede Umgebung einbetten müssen, die nur Rastergrafiken unterstützt.

## Warum CAD‑Layer separat exportieren?

Der einzelne Export von CAD‑Layern gibt Ihnen eine feinkörnige Kontrolle über die visuelle Ausgabe, reduziert die Dateigröße jedes Bildes und ermöglicht das Anwenden von layer‑spezifischen Stilen oder Nachbearbeitungen. Dies ist besonders praktisch bei großen technischen Zeichnungen, bei denen nur ein Teil der Layer für ein bestimmtes Publikum relevant ist.

## Voraussetzungen

Bevor Sie in das Tutorial einsteigen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD for .NET Library** – laden Sie sie von der [Aspose.CAD website](https://releases.aspose.com/cad/net/) herunter.  
- **CAD‑Zeichnungsdatei** – eine DXF‑Datei (z. B. `conic_pyramid.dxf`), die Sie in Rasterformate konvertieren möchten.  

## Namespaces importieren

Importieren Sie in Ihrem .NET‑Projekt die erforderlichen Namespaces, um die Funktionen von Aspose.CAD zu nutzen. Fügen Sie die folgenden Namespaces am Anfang Ihres Codes ein:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Wie man **convert dxf to png** – Schritt‑für‑Schritt‑Anleitung

### Schritt 1: CAD‑Zeichnung laden

Laden Sie zunächst die DXF‑Datei in ein `Image`‑Objekt. Dieses Objekt repräsentiert die gesamte CAD‑Zeichnung im Speicher.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Schritt 2: `CadRasterizationOptions` erstellen

Konfigurieren Sie die Rasterisierungseinstellungen wie Ausgabedimensionen und Auflösung. Diese Optionen steuern, wie die Vektordaten rasterisiert werden.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Schritt 3: Layer angeben (CAD‑Layer exportieren)

Wenn Sie nur einen bestimmten Layer benötigen, geben Sie hier dessen Namen an. Dies demonstriert das einzelne **export cad layers**.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Schritt 4: Bildformat wählen – CAD als PNG (oder JPEG) speichern

Erstellen Sie ein options‑Objekt, das spezifisch für das Bildformat ist. Ersetzen Sie `JpegOptions` durch `PngOptions`, wenn Sie **save cad as png** möchten.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro‑Tipp:** Um PNG‑Dateien zu erzeugen, instanziieren Sie einfach `new PngOptions()` anstelle von `JpegOptions`.

### Schritt 5: Export im JPEG‑ (oder PNG‑)Format

Speichern Sie schließlich das rasterisierte Bild auf dem Datenträger. Die Dateierweiterung bestimmt das Ausgabeformat.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Wenn Sie `JpegOptions` durch `PngOptions` ersetzen, wird derselbe Code **convert dxf to png** und erzeugt eine `.png`‑Datei.

### Zusätzlicher Schritt: Alle Layer konvertieren

Wenn Sie **convert cad to raster** für jeden Layer in der Zeichnung benötigen, rufen Sie die untenstehende Hilfsmethode auf. Sie iteriert über alle Layer und speichert jeden als separates Bild.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Hinweis:* Die Implementierung von `ConvertAllLayersToRasterImageFormats` ist Teil der vollständigen Aspose.CAD‑Beispielsammlung und demonstriert die Stapelverarbeitung von Layern.

## Häufige Probleme & Fehlersuche

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| Leeres oder weißes Bild | Rasterisierungsoptionen nicht gesetzt (z. B. `PageWidth`/`PageHeight` = 0) | Stellen Sie sicher, dass `PageWidth` und `PageHeight` positive Werte haben |
| Fehlende Layer | Falscher Layer‑Name im `Layers`‑Array | Überprüfen Sie den genauen Layer‑Namen in der CAD‑Datei (Groß‑/Kleinschreibung beachten) |
| Niedrige PNG‑Qualität | Standard‑DPI ist niedrig | Setzen Sie `rasterizationOptions.Resolution = 300;` für höhere Qualität |

## Häufig gestellte Fragen (Original)

### Q1: Kann ich andere Bildformate für den Export verwenden?

A1: Ja, das können Sie. Ersetzen Sie einfach `JpegOptions` durch die Optionen des gewünschten Formats, z. B. `PngOptions` oder `BmpOptions`.

### Q2: Gibt es eine Testversion?

A2: Ja, Sie können die Funktionalität von Aspose.CAD erkunden, indem Sie die Testversion [hier](https://releases.aspose.com/) herunterladen.

### Q3: Wie kann ich Support für Aspose.CAD erhalten?

A3: Besuchen Sie das Aspose.CAD‑[Forum](https://forum.aspose.com/c/cad/19) für Community‑Support oder erwägen Sie den Kauf einer Lizenz für dedizierten Support.

### Q4: Gibt es temporäre Lizenzen?

A4: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q5: Wo finde ich die Dokumentation?

A5: Siehe die ausführliche Dokumentation [hier](https://reference.aspose.com/cad/net/).

## Zusätzliche FAQ

**Q: Kann ich alle Layer mit einem Befehl exportieren?**  
A: Ja, verwenden Sie die oben gezeigte Methode `ConvertAllLayersToRasterImageFormats`.

**Q: Unterstützt Aspose.CAD Vektorformate wie SVG?**  
A: Es richtet sich hauptsächlich auf Rasterformate, aber Sie können nach PDF exportieren, das Vektordaten beibehält.

**Q: Wie kann ich die Hintergrundfarbe des exportierten PNG steuern?**  
A: Setzen Sie `rasterizationOptions.BackgroundColor` auf die gewünschte `Color`, bevor Sie speichern.

**Q: Ist es möglich, ein einzelnes Layout statt der gesamten Zeichnung zu exportieren?**  
A: Ja, konfigurieren Sie `rasterizationOptions.Layouts`, um die gewünschten Layout‑Namen anzugeben, die Sie rasterisieren möchten.

## Fazit

Sie haben nun gelernt, wie man **convert dxf to png**, **export cad layers** und **save cad as png** oder JPEG mit Aspose.CAD für .NET durchführt. Durch Anpassen von `CadRasterizationOptions` und dem Austausch der Bildformat‑Optionen können Sie die Konvertierung an praktisch jede gewünschte Rasterausgabe anpassen. Erkunden Sie die weiteren Formatoptionen in der Aspose.CAD‑API, um Ihren CAD‑zu‑Raster‑Workflow zu erweitern.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}