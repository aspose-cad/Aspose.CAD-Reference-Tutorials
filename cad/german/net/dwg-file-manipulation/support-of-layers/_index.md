---
date: 2026-04-09
description: Erfahren Sie, wie Sie DWG‑Ebenen exportieren, DWG‑Bilder konvertieren
  und DWG‑JPEGs mit C# und Aspose.CAD für .NET speichern. Schritt‑für‑Schritt‑Anleitung
  für effiziente CAD‑Dateimanipulation.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Umgang mit Ebenen in DWG‑Dateien mit C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG‑Ebenen mit C# exportieren – Aspose.CAD‑Tutorial
url: /de/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-Layer mit C# exportieren – Aspose.CAD Tutorial

## Einführung

In diesem umfassenden Leitfaden lernen Sie **wie man DWG-Layer exportiert** mit C# und der Aspose.CAD-Bibliothek. Egal, ob Sie **DWG-Bilder** konvertieren, **DWG-Layer‑Sichtbarkeit** steuern oder einfach **DWG‑JPEG**‑Dateien speichern müssen, die nachfolgenden Schritte zeigen Ihnen genau, wie Sie dies effizient erledigen. Am Ende des Tutorials haben Sie ein sofort ausführbares Snippet, das einen bestimmten Layer isoliert und als hochqualitatives JPEG rendert.

## Schnelle Antworten
- **Was bedeutet “export dwg layers”?** Es bedeutet, ausgewählte Layer einer DWG-Datei in ein Bildformat wie JPEG oder PNG zu rasterisieren.  
- **Welche Bibliothek ist am besten für diese Aufgabe?** Aspose.CAD für .NET bietet vollständige Unterstützung, ohne dass AutoCAD erforderlich ist.  
- **Kann ich mehrere Layer gleichzeitig exportieren?** Ja – übergeben Sie ein Array von Layer‑Namen an die Rasterisierungsoptionen.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Eine kommerzielle Lizenz ist erforderlich; eine kostenlose Testversion steht zur Evaluierung bereit.  
- **Welche Ausgabeformate werden unterstützt?** JPEG, PNG, BMP, TIFF und mehrere andere über die ImageOptions‑Klassen.

## Was bedeutet das Exportieren von DWG-Layern?
Das Exportieren von DWG-Layern bedeutet, die Vektordaten, die zu einem oder mehreren Layern in einer DWG-Zeichnung gehören, in ein Bitmap‑Bild zu rasterisieren. Dies ist nützlich, wenn Sie einen Blick auf einen bestimmten Teil einer Zeichnung teilen möchten, ohne die gesamte CAD‑Datei preiszugeben.

## Warum die DWG-Layer‑Sichtbarkeit steuern?
Die Steuerung der Layer‑Sichtbarkeit ermöglicht es Ihnen:

- Saubere visuelle Assets für Präsentationen oder Dokumentationen zu erstellen.  
- Die Dateigröße zu reduzieren, indem nur die benötigte Geometrie exportiert wird.  
- Proprietäre Design‑Details zu schützen, indem vertrauliche Layer ausgeblendet werden.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- Grundkenntnisse der Programmiersprache C#.  
- Visual Studio auf Ihrem Rechner installiert.  
- Die Aspose.CAD für .NET‑Bibliothek, die Sie von der [Aspose.CAD-Website](https://releases.aspose.com/cad/net/) herunterladen können.

## Namespaces importieren

Um zu beginnen, importieren Sie die Namespaces, die Ihnen Zugriff auf Rasterisierungs‑ und Bild‑Export‑Funktionen geben.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Schritt 1: DWG-Datei laden

Laden Sie die Quell‑DWG‑ (oder DWF‑)Datei in ein `Image`‑Objekt. Dieses Objekt repräsentiert die gesamte Zeichnung im Speicher.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Warum das wichtig ist:* Das einmalige Laden der Datei ermöglicht es Ihnen, dieselbe `image`‑Instanz für beliebig viele layer‑spezifische Exporte wiederzuverwenden, was die Leistung verbessert.

## Schritt 2: Rasterisierungsoptionen konfigurieren

Erzeugen Sie eine `CadRasterizationOptions`‑Instanz, um Aspose.CAD mitzuteilen, wie die Zeichnung gerendert werden soll. Hier setzen wir eine hohe Auflösung (1600 × 1600), um sicherzustellen, dass das exportierte JPEG scharf ist.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Bei Bedarf können Sie auch die Hintergrundfarbe, die Linienstärken‑Skalierung oder Anti‑Aliasing‑Einstellungen anpassen.

## Schritt 3: Layer festlegen (DWG‑Layer‑Sichtbarkeit)

Fügen Sie die Layer hinzu, für die Sie **DWG-Layer exportieren** möchten. In diesem Beispiel exportieren wir nur „LayerA“. Um mehrere Layer zu exportieren, listen Sie sie einfach im Array auf.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Pro‑Tipp:* Verwenden Sie den genauen Layer‑Namen, wie er in der Zeichnung erscheint; Layer‑Namen sind case‑sensitive.

## Schritt 4: Bild‑Exportoptionen konfigurieren

Wählen Sie das Bildformat, das Sie erstellen möchten. Wir verwenden `JpegOptions`, weil JPEG ein gutes Gleichgewicht zwischen Qualität und Dateigröße bietet, was ideal ist, wenn Sie **DWG‑JPEG**‑Dateien für die Web‑Vorschau speichern müssen.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Falls Sie **DWG‑Bilder** in PNG oder TIFF konvertieren müssen, ersetzen Sie `JpegOptions` durch die entsprechende Options‑Klasse.

## Schritt 5: Exportiertes Bild speichern

Definieren Sie den Ausgabepfad und rufen Sie `Save` auf. Die Rasterisierungs‑Engine berücksichtigt die von Ihnen bereitgestellte Layer‑Liste, sodass nur „LayerA“ im finalen JPEG erscheint.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Nachdem diese Zeile ausgeführt wurde, finden Sie `for_layers_test.jpg` in Ihrem Dokumenten‑Verzeichnis, das nur den ausgewählten Layer enthält.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|------------|
| **Layer‑Name nicht gefunden** | Überprüfen Sie die genaue Schreibweise und Groß‑/Kleinschreibung des Layers in der ursprünglichen DWG. Verwenden Sie einen CAD‑Viewer, um die Layer‑Namen aufzulisten. |
| **Leeres Ausgabebild** | Stellen Sie sicher, dass die Rasterisierungsoptionen einen nicht‑transparenten Hintergrund haben und dass die ausgewählten Layer tatsächlich Geometrie enthalten. |
| **Ausgabe mit niedriger Auflösung** | Erhöhen Sie `PageWidth` und `PageHeight` oder setzen Sie `Resolution` in `CadRasterizationOptions`. |
| **Nicht unterstützte DWG‑Version** | Aktualisieren Sie auf die neueste Aspose.CAD‑Version; sie fügt Unterstützung für neuere AutoCAD‑Versionen hinzu. |

## Häufig gestellte Fragen

### Q1: Kann ich mehrere Layer gleichzeitig verarbeiten?
A1: Ja, das können Sie. Fügen Sie einfach die Layer‑Namen dem Array `rasterizationOptions.Layers` hinzu.

### Q2: Ist eine Testversion von Aspose.CAD verfügbar?
A2: Ja, Sie können eine kostenlose Testversion von [hier](https://releases.aspose.com/) erhalten.

### Q3: Wo finde ich die Dokumentation?
A3: Die Dokumentation ist [hier](https://reference.aspose.com/cad/net/) verfügbar.

### Q4: Wie erhalte ich Support für Aspose.CAD?
A4: Sie können Support im [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) erhalten.

### Q5: Welche Lizenzierungsoptionen gibt es für Aspose.CAD?
A5: Sie können Lizenzoptionen und Kaufdetails [hier](https://purchase.aspose.com/buy) einsehen.

**Zusätzliche Fragen & Antworten**

**Q: Kann ich die Zeichnung statt JPEG als PNG exportieren?**  
A: Absolut. Ersetzen Sie `JpegOptions` durch `PngOptions` und passen Sie die Dateierweiterung entsprechend an.

**Q: Bewahrt die Bibliothek Linienstile und Farben?**  
A: Ja. Alle Vektoreigenschaften werden während der Rasterisierung getreu wiedergegeben.

---

**Zuletzt aktualisiert:** 2026-04-09  
**Getestet mit:** Aspose.CAD für .NET (neueste Version)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}