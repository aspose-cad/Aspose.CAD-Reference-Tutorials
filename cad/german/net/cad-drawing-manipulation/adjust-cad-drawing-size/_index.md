---
date: 2026-03-19
description: Erfahren Sie, wie Sie CAD‑Zeichnungen in .NET mit Aspose.CAD skalieren,
  einschließlich der Skalierung von CAD‑Zeichnungseinheiten und der Anpassung der
  Layoutgröße. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Wie man CAD‑Zeichnungen mit Aspose.CAD für .NET skaliert
url: /de/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man CAD-Zeichnungen mit Aspose.CAD für .NET in der Größe ändert

## Introduction

Wenn Sie **CAD-Dateien** direkt aus Ihrer .NET-Anwendung **skalieren** müssen, sind Sie hier genau richtig. In diesem Tutorial zeigen wir Ihnen, wie Sie CAD‑Einheitseinstellungen ändern, die Abmessungen einer CAD‑Zeichnung skalieren und die CAD‑Größe programmgesteuert mit Aspose.CAD für .NET anpassen. Am Ende des Leitfadens verfügen Sie über eine solide, produktionsreife Lösung zum Ändern der Größe jedes unterstützten CAD‑Formats.

## Quick Answers
- **Welche Bibliothek wird benötigt?** Aspose.CAD für .NET  
- **Kann ich den Einheitstyp ändern?** Ja – setzen Sie `UnitType` in `CadRasterizationOptions`  
- **Wird für die Produktion eine Lizenz benötigt?** Eine gültige Aspose.CAD‑Lizenz ist für die Nutzung außerhalb der Testphase erforderlich  
- **In welches Bildformat exportiert das Beispiel?** BMP (aber jedes unterstützte Rasterformat funktioniert)  
- **Wie viele Codezeilen?** Weniger als 30 Zeilen für eine vollständige Größenänderung  

## What is “how to resize CAD” in practice?
Das Ändern der Größe einer CAD‑Zeichnung bedeutet, die Vektordaten in ein Rasterbild bei einem bestimmten Maßstab oder einer bestimmten Einheit (z. B. Zentimeter, Zoll) zu konvertieren. Dies ist nützlich, wenn Sie Zeichnungen in Berichte einbetten, Miniaturansichten erzeugen oder CAD‑Grafiken in Webseiten integrieren müssen.

## Why adjust CAD size with Aspose.CAD?
- **Keine externe CAD‑Software** – alles läuft innerhalb Ihres .NET‑Codes.  
- **Feinkörnige Kontrolle** über Einheiten, Layouts und Rasterisierungsoptionen.  
- **Cross‑Format‑Unterstützung** – derselbe Code funktioniert für DWG, DXF, DWF und weitere.  

## Prerequisites

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- Aspose.CAD für .NET Bibliothek: Laden Sie die Bibliothek von der [Aspose.CAD für .NET Download-Seite](https://releases.aspose.com/cad/net/) herunter und installieren Sie sie.  
- Beispiel‑CAD‑Zeichnung: Eine Datei wie `sample.dwg`, die im Dokumentverzeichnis Ihres Projekts abgelegt ist.  

## Import Namespaces

First, import the namespaces that give you access to Aspose.CAD’s classes.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the CAD Drawing

Laden Sie die Quelldatei in ein `Image`‑Objekt. Dieses Objekt repräsentiert die CAD‑Zeichnung im Speicher und dient als Grundlage für alle weiteren Vorgänge.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Step 2: Create BmpOptions (or any other raster format)

`BmpOptions` gibt Aspose.CAD an, wie die Vektordaten beim Speichern als Bitmap gerendert werden sollen. Sie können dies je nach gewünschtem Zielformat durch `PngOptions`, `JpegOptions` usw. ersetzen.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Step 3: Set CadRasterizationOptions

`CadRasterizationOptions` enthält die Kerneinstellungen für Skalierung, Einheitumwandlung und Layoutauswahl. Durch die Verknüpfung mit der Eigenschaft `VectorRasterizationOptions` von `BmpOptions` wird sichergestellt, dass der Rasterizer Ihre benutzerdefinierten Einstellungen verwendet.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Step 4: Set UnitType (change CAD unit)

Hier ändern wir die CAD‑Einheit von der Vorgabe zu Zentimetern. Hier kommt das Stichwort **change cad unit** zum Einsatz, und es beeinflusst direkt die endgültige Bildgröße.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Step 5: Choose Layouts (set CAD layouts)

Falls Ihre Zeichnung mehrere Layouts enthält (z. B. Model, Sheet1), geben Sie an, welche Sie rasterisieren möchten. Die Auswahl des richtigen Layouts ist entscheidend, wenn Sie **set cad layouts** für eine skalierte Ausgabe festlegen.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 6: Export to BMP (resize CAD drawing)

Speichern Sie schließlich das rasterisierte Bild. Die Ausgabedatei spiegelt die von Ihnen konfigurierten neue Größe, Einheit und Layout wider – damit ist die **resize CAD drawing**‑Operation abgeschlossen.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Sie haben nun eine BMP‑Datei, die die skalierte CAD‑Zeichnung darstellt und bereit für weitere Verarbeitung oder Anzeige ist.

## Common Issues and Solutions

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| Ausgabe ist unscharf | Standard‑DPI (dots per inch) ist zu niedrig | Setzen Sie `cadRasterizationOptions.Resolution = 300;` vor dem Speichern |
| Falsches Layout wird angezeigt | Tippfehler im Layoutnamen | Überprüfen Sie den genauen Layoutnamen mit einem CAD‑Viewer oder der `Layouts`‑Sammlung |
| Einheitumwandlung wirkt falsch | Mischung aus metrischen und imperialen Einheiten | Stellen Sie sicher, dass `UnitType` dem gewünschten Messsystem entspricht |

## FAQs

### Q1: Ist Aspose.CAD für .NET mit allen CAD‑Formaten kompatibel?

A1: Aspose.CAD für .NET unterstützt eine breite Palette von CAD‑Formaten, darunter DWG, DXF, DWF und weitere. Prüfen Sie die [Dokumentation](https://reference.aspose.com/cad/net/) für die vollständige Liste.

### Q2: Kann ich mehrere Layouts gleichzeitig skalieren?

A2: Ja, Sie können mehrere Layouts skalieren, indem Sie das `Layouts`‑Array in den `CadRasterizationOptions` anpassen.

### Q3: Wo kann ich Unterstützung für Aspose.CAD für .NET erhalten?

A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Hilfe.

### Q4: Gibt es eine kostenlose Testversion?

A4: Ja, Sie können eine [kostenlose Testversion](https://releases.aspose.com/) ausprobieren, um die Funktionen von Aspose.CAD für .NET zu bewerten.

### Q5: Wie kann ich eine temporäre Lizenz für Aspose.CAD für .NET erhalten?

A5: Eine temporäre Lizenz für Testzwecke erhalten Sie [hier](https://purchase.aspose.com/temporary-license/).

## Frequently Asked Questions

**Q: Wie skaliere ich eine CAD‑Zeichnung, ohne den Einheitstyp zu ändern?**  
A: Passen Sie die `Zoom`‑Eigenschaft von `CadRasterizationOptions` an (z. B. `cadRasterizationOptions.Zoom = 2.0;`), um die Größe zu verdoppeln und gleichzeitig die ursprüngliche Einheit beizubehalten.

**Q: Kann ich in andere Formate als BMP exportieren?**  
A: Natürlich. Ersetzen Sie `BmpOptions` durch `PngOptions`, `JpegOptions` oder eine andere unterstützte Rasterformat‑Klasse.

**Q: Ist es möglich, einen Ordner mit Zeichnungen stapelweise zu verarbeiten?**  
A: Ja. Durchlaufen Sie die Dateien in einem Verzeichnis, wenden Sie dieselbe Rasterisierungslogik an und speichern Sie jede Ausgabe unter einem eindeutigen Namen.

---

**Last Updated:** 2026-03-19  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}