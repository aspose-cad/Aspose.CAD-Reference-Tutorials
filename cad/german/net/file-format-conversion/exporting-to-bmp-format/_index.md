---
title: Exportieren in das BMP-Format – Aspose.CAD-Tutorial
linktitle: Exportieren in das BMP-Format
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die nahtlose Welt des 3D-Bildexports in BMP mit Aspose.CAD für .NET. Folgen Sie unserem Tutorial für ein problemloses Erlebnis.
weight: 11
url: /de/net/file-format-conversion/exporting-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren in das BMP-Format – Aspose.CAD-Tutorial

## Einführung

In der dynamischen Welt der Softwareentwicklung sticht Aspose.CAD für .NET als leistungsstarkes Werkzeug für den Umgang mit CAD-Dateien (Computer-Aided Design) hervor. Wenn Sie CAD-Bilder in das weit verbreitete BMP-Format exportieren möchten, ist dieses Tutorial Ihr Leitfaden. In dieser Schritt-für-Schritt-Anleitung erkunden wir den Prozess des Exportierens von 3D-Bildern nach BMP mit Aspose.CAD für .NET. Lass uns eintauchen!

## Voraussetzungen

Bevor wir mit diesem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Laden Sie die Aspose.CAD-Bibliothek herunter und installieren Sie sie[Hier](https://releases.aspose.com/cad/net/).
- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein.
- CAD-Datei: Halten Sie eine CAD-Datei für den Export bereit. Für dieses Beispiel verwenden wir „18-12-11 9644 – site.dwf“.

## Namespaces importieren

Stellen Sie in Ihrem .NET-Projekt sicher, dass Sie die erforderlichen Namespaces importieren:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: Laden Sie das CAD-Bild

Laden Sie zunächst das CAD-Bild in Ihr Projekt. Ersetzen Sie „Ihr Dokumentverzeichnis“ durch den tatsächlichen Verzeichnispfad.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Hier finden Sie Ihren Code zum Laden des Bildes
}
```

## Schritt 2: Konfigurieren Sie die BMP-Exportoptionen

Richten Sie die BMP-Exportoptionen ein, einschließlich Vektor-Rasterisierungsoptionen für CAD-Dateien.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Schritt 3: Export nach BMP

Führen Sie den Exportvorgang aus und geben Sie dabei den Ausgabepfad für die BMP-Datei an.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Abschluss

Glückwunsch! Sie haben mit Aspose.CAD für .NET erfolgreich ein 3D-Bild in BMP exportiert. Dieses Tutorial bietet einen Einblick in die Vielseitigkeit von Aspose.CAD und macht komplexe Aufgaben zu einem Kinderspiel.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit jedem CAD-Dateiformat verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Dateiformate und bietet so Flexibilität bei Ihren Projekten.

### F2: Ist zu Testzwecken eine temporäre Lizenz verfügbar?

 A2: Auf jeden Fall! Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/) zur Auswertung.

### F3: Wo finde ich eine umfassende Dokumentation für Aspose.CAD?

 A3: Sehen Sie sich die Dokumentation an[Hier](https://reference.aspose.com/cad/net/) Ausführliche Informationen und Beispiele finden Sie hier.

### F4: Wie kann ich Unterstützung suchen oder mit der Community in Kontakt treten?

 A4: Besuchen Sie das Aspose.CAD-Forum[Hier](https://forum.aspose.com/c/cad/19) um Fragen zu stellen und mit der Community in Kontakt zu treten.

### F5: Kann ich Aspose.CAD für .NET kaufen?

 A5: Ja, Sie können Aspose.CAD erwerben[Hier](https://purchase.aspose.com/buy) um das volle Potenzial für Ihre Projekte auszuschöpfen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
