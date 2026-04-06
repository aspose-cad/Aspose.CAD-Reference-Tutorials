---
date: 2026-04-06
description: Lernen Sie, wie Sie DWF in C# mit Aspose.CAD in JPG konvertieren und
  erfahren Sie, wie Sie die DWF‑Layoutgröße aus DWG‑Dateien extrahieren.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Arbeiten mit DWG-Dateien in C# – Größe des DWF-Layouts ermitteln
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWF in JPG konvertieren in C# – DWF‑Layoutgröße aus DWG erhalten
url: /de/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWF in JPG konvertieren in C# – DWF-Layoutgröße aus DWG erhalten

## Einleitung

Wenn Sie **DWF in JPG konvertieren** müssen und gleichzeitig die genauen Layout‑Abmessungen ermitteln wollen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch ein vollständiges End‑to‑End‑Beispiel, das Aspose.CAD für .NET verwendet, um eine aus DWG abgeleitete DWF‑Datei zu öffnen, die Größe jedes Layouts auszulesen und das Layout als hochqualitatives JPG‑Bild zu speichern. Am Ende wissen Sie nicht nur, wie Sie DWF‑Layout‑Informationen extrahieren, sondern erhalten auch ein wiederverwendbares Code‑Snippet, das Sie in jedes C#‑Projekt einbinden können.

## Schnelle Antworten
- **Was bedeutet „convert DWF to JPG“?** Es bedeutet, ein Vektor‑DWF‑Layout in ein Bitmap‑JPEG‑Bild zu rasterisieren.  
- **Warum zuerst die Layoutgröße auslesen?** Das Wissen um die genauen Ausmaße ermöglicht das Festlegen der korrekten Seitengrößen und verhindert gestreckte oder abgeschnittene Ausgaben.  
- **Welche Bibliothek übernimmt das?** Aspose.CAD für .NET bietet vollständige Unterstützung für DWG, DWF und die Umwandlung in Rasterbilder.  
- **Benötige ich eine Lizenz?** Eine temporäre Lizenz funktioniert für die Evaluierung; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Was bedeutet „convert DWF to JPG“ und warum ist das wichtig?

Das Konvertieren einer DWF‑Datei (Design Web Format) in JPG erzeugt ein portables Bild, das in Browsern angezeigt, in Berichte eingebettet oder mit Interessenten geteilt werden kann, die keine CAD‑Software besitzen. Die Umwandlung bietet zudem die Flexibilität, das Bild (Größe ändern, komprimieren, Wasserzeichen hinzufügen) mit gängigen Bildverarbeitungs‑Tools zu bearbeiten.

## Warum DWF-Layoutgröße extrahieren?

Eine DWF‑Datei kann mehrere Layouts enthalten, von denen jedes ein eigenes Koordinatensystem und eigene Einheiten (Zoll, Millimeter usw.) hat. Das Extrahieren der Layoutgröße ermöglicht Ihnen:

1. Das ursprüngliche Seitenverhältnis beim Rasterisieren beizubehalten.  
2. Die richtige DPI für hochauflösende Ausgaben zu wählen.  
3. Die Stapelverarbeitung vieler Layouts zu automatisieren, ohne manuelle Anpassungen.

## Voraussetzungen

Um diesem Tutorial reibungslos zu folgen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.CAD für .NET: Vergewissern Sie sich, dass Aspose.CAD für .NET installiert ist. Sie können es von der [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) herunterladen.

Wenn die Bibliothek bereitsteht, können Sie sich auf den Code konzentrieren, anstatt nach Abhängigkeiten zu suchen.

## Namespaces importieren

Bevor wir mit dem Codieren beginnen, importieren Sie die erforderlichen Namespaces. Diese stellen die Klassen bereit, die wir für die Arbeit mit CAD‑Dateien, Rasterisierungsoptionen und Datei‑I/O benötigen.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Schritt 1: Umgebung einrichten

Erstellen Sie ein neues C#‑Konsolen‑ oder Klassenbibliotheks‑Projekt, fügen Sie einen Verweis auf **Aspose.CAD.dll** hinzu und stellen Sie sicher, dass das Projekt eine kompatible .NET‑Version anvisiert.

## Schritt 2: Dateipfade definieren (wie DWF extrahieren)

Geben Sie an, wo sich Ihre Quell‑DWF‑Datei befindet und wohin die erzeugten JPG‑Dateien geschrieben werden sollen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro‑Tipp:** Verwenden Sie `Path.Combine(MyDir, "blocks_and_tables.dwf")` für eine sicherere Pfadbehandlung auf verschiedenen Betriebssystemen.

## Schritt 3: DWF-Bild laden

Laden Sie die DWF‑Datei in ein `Aspose.CAD.Image`‑Objekt. Wir casten es zu `DwfImage`, weil wir Zugriff auf seiten­spezifische Eigenschaften benötigen.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Schritt 4: Durch Seiten iterieren

Eine DWF kann mehrere Seiten (Layouts) enthalten. Durchlaufen Sie jede, damit wir sie einzeln verarbeiten können.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Schritt 5: Layout-Informationen abrufen

Innerhalb der Schleife holen Sie den Layout‑Namen ab. Dieser Name wird sowohl für das Logging als auch für die Benennung der Ausgabedatei JPG verwendet.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Schritt 6: JPG-Optionen einrichten

Erzeugen Sie eine Instanz von `JpegOptions` und konfigurieren Sie die Rasterisierungsoptionen. Die Eigenschaft `Layouts` gibt Aspose.CAD an, welches Layout gerendert werden soll.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Schritt 7: Seitengröße bestimmen (dwg in jpg konvertieren)

Berechnen Sie die Breite und Höhe des Layouts in seinen nativen Einheiten. Diese Information ist entscheidend, um die Raster‑Seitengröße korrekt festzulegen.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Schritt 8: Seitenabmessungen festlegen

Wandeln Sie die nativen Einheiten (Zoll oder Millimeter) mit den von Aspose.CAD bereitgestellten Hilfsmethoden in Pixel um. Wenn der Einheitentyp keiner dieser ist, greifen wir auf die Rohwerte zurück.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Schritt 9: JPG-Datei speichern

Schließlich binden Sie die Rasterisierungsoptionen an die JPEG‑Optionen und speichern das Bild auf dem Datenträger.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Wenn die Schleife beendet ist, haben Sie für jedes Layout eine JPG‑Datei, die exakt den ursprünglichen DWF‑Abmessungen entspricht.

## Häufige Probleme und Lösungen

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| Leere JPG‑Ausgabe | `options.Layouts` nicht korrekt gesetzt | Stellen Sie sicher, dass der Layout‑Name mit `page.Name` übereinstimmt. |
| Verzerrtes Bild | Falsche DPI‑Umrechnung | Verwenden Sie `CommonHelper.DPI = 300` (oder Ihre Ziel‑DPI) vor der Umwandlung. |
| Datei nicht gefunden | Falscher `MyDir`‑Pfad | Verwenden Sie absolute Pfade oder `Path.Combine`. |
| Lizenz‑Ausnahme | Keine Lizenz angewendet | Laden Sie eine temporäre oder permanente Lizenz, bevor Sie `Image.Load` aufrufen. |

## Häufig gestellte Fragen

### Q1: Ist Aspose.CAD mit den neuesten DWG‑Dateiformaten kompatibel?

A1: Aspose.CAD unterstützt verschiedene DWG‑Dateiformate, einschließlich der neuesten Versionen. Weitere Details zur Kompatibilität finden Sie in der [documentation](https://reference.aspose.com/cad/net/).

### Q2: Kann ich Aspose.CAD sowohl für kommerzielle als auch für private Projekte nutzen?

A2: Ja, Aspose.CAD bietet flexible Lizenzierungsoptionen für kommerzielle und private Nutzung. Besuchen Sie die [purchase page](https://purchase.aspose.com/buy) für weitere Details.

### Q3: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

A3: Sie können eine temporäre Lizenz von [here](https://purchase.aspose.com/temporary-license/) für Evaluierungszwecke erhalten.

### Q4: Wo finde ich Support für Aspose.CAD?

A4: Bei Fragen oder Unterstützung besuchen Sie das [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Gibt es eine kostenlose Testversion für Aspose.CAD?

A5: Ja, Sie können eine kostenlose Testversion von Aspose.CAD [here](https://releases.aspose.com/) erhalten.

### Q6: Wie konvertiere ich eine DWG‑Datei direkt in JPG, ohne zuerst DWF zu extrahieren?

A6: Sie können die DWG‑Datei mit `Aspose.CAD.Image.Load` laden und denselben Rasterisierungs‑Workflow verwenden; setzen Sie einfach `options.Layouts` auf die gewünschten Layout‑Namen aus der DWG.

### Q7: Erhält die Konvertierung die Vektor‑Qualität?

A7: Nach der Rasterisierung zu JPG ist das Bild bitmap‑basiert, sodass die Vektor‑Skalierbarkeit verloren geht. Für verlustfreie Skalierung sollten Sie stattdessen den Export nach PNG oder SVG in Betracht ziehen.

---

**Zuletzt aktualisiert:** 2026-04-06  
**Getestet mit:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}