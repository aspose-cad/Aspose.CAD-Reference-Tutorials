---
title: Umgang mit Ebenen in DWG-Dateien mit C# – Aspose.CAD-Tutorial
linktitle: Umgang mit Ebenen in DWG-Dateien mit C#
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie Ebenen in DWG-Dateien mit C# mit Aspose.CAD für .NET verarbeiten. Schritt-für-Schritt-Anleitung für die effiziente Bearbeitung von CAD-Dateien.
type: docs
weight: 11
url: /de/net/dwg-file-manipulation/support-of-layers/
---
## Einführung

Willkommen zu unserem ausführlichen Tutorial zum Umgang mit Ebenen in DWG-Dateien mithilfe von C# mit Aspose.CAD für .NET. Aspose.CAD ist eine leistungsstarke Bibliothek, die Entwicklern die nahtlose Arbeit mit CAD-Dateiformaten ermöglicht. In diesem Tutorial führen wir Sie Schritt für Schritt durch den Umgang mit Ebenen in DWG-Dateien.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Grundkenntnisse der Programmiersprache C#.
- Visual Studio ist auf Ihrem Computer installiert.
-  Aspose.CAD für .NET-Bibliothek, die Sie von der herunterladen können[Aspose.CAD-Website](https://releases.aspose.com/cad/net/).

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr C#-Projekt. Diese Namespaces stellen die für die Arbeit mit CAD-Dateien erforderliche Funktionalität bereit.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Schritt 1: Laden Sie die DWG-Datei

Laden Sie zunächst die DWG-Datei mithilfe der Aspose.CAD-Bibliothek in Ihre C#-Anwendung.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Ihr Code für die nachfolgenden Schritte finden Sie hier
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

 Erstellen Sie eine Instanz von`CadRasterizationOptions` und legen Sie seine Eigenschaften fest, um zu definieren, wie die DWG-Datei gerastert werden soll.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Schritt 3: Ebenen angeben

Fügen Sie die gewünschten Ebenen zu den Rasterisierungsoptionen hinzu. In diesem Beispiel haben wir „LayerA“ hinzugefügt.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Schritt 4: Bildexportoptionen konfigurieren

 Erstellen Sie die erforderlichen Bildexportoptionen. Hier verwenden wir`JpegOptions` zum Exportieren in JPEG.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 5: Speichern Sie das exportierte Bild

Geben Sie den Ausgabepfad an und speichern Sie die gerasterte DWG-Datei als JPEG.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Jetzt haben Sie erfolgreich Ebenen in einer DWG-Datei mit C# mit Aspose.CAD für .NET verarbeitet.

## Abschluss

In diesem Tutorial haben wir den Prozess der Verarbeitung von Ebenen in DWG-Dateien mithilfe von C# und der Aspose.CAD-Bibliothek durchlaufen. Wenn Sie diese Schritte befolgen, können Sie effizient mit CAD-Dateien in Ihren .NET-Anwendungen arbeiten.

## FAQs

### F1: Kann ich mehrere Ebenen gleichzeitig bearbeiten?

 A1: Ja, das können Sie. Fügen Sie einfach die Ebenennamen hinzu`rasterizationOptions.Layers` Array.

### F2: Ist eine Testversion von Aspose.CAD verfügbar?

 A2: Ja, Sie können eine kostenlose Testversion von erhalten[Hier](https://releases.aspose.com/).

### F3: Wo finde ich die Dokumentation?

 A3: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/cad/net/).

### F4: Wie erhalte ich Unterstützung für Aspose.CAD?

 A4: Sie können auf der Website Unterstützung suchen[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).

### F5: Welche Lizenzoptionen gibt es für Aspose.CAD?

 A5: Sie können sich über Lizenzoptionen und Kaufdetails informieren[Hier](https://purchase.aspose.com/buy).