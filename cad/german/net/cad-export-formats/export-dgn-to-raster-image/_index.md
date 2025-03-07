---
title: Exportieren Sie DGN in ein Rasterbild in Aspose.CAD für .NET
linktitle: Exportieren Sie DGN in ein Rasterbild
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Konvertieren Sie DGN mühelos in Rasterbilder mit Aspose.CAD für .NET. Entdecken Sie die Schritt-für-Schritt-Anleitung und nutzen Sie die Leistungsfähigkeit von .NET bei der Bearbeitung von CAD-Dateien.
weight: 13
url: /de/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren Sie DGN in ein Rasterbild in Aspose.CAD für .NET

## Einführung

Im dynamischen Bereich der .NET-Entwicklung erweist sich Aspose.CAD als leistungsstarkes Werkzeug für den Umgang mit CAD-Dateien (Computer-Aided Design). Dieses Tutorial befasst sich mit dem Prozess des Exportierens von DGN-Dateien in Rasterbilder mit Aspose.CAD für .NET. Wenn Sie Ihre DGN-Dateien nahtlos in optisch ansprechende Rasterbilder umwandeln möchten, sind Sie hier richtig.

## Voraussetzungen

Bevor wir uns auf diese Reise begeben, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass die Aspose.CAD-Bibliothek in Ihrem .NET-Projekt installiert ist. Die Bibliothek und die entsprechende Dokumentation finden Sie unter[Webseite](https://reference.aspose.com/cad/net/).

- Beispiel-DGN-Datei: Halten Sie eine DGN-Datei zur Konvertierung bereit. In unserem Beispiel verwenden wir „Nikon_D90_Camera.dgn“.

Kommen wir nun zur Schritt-für-Schritt-Anleitung.

## Namespaces importieren

Beginnen Sie in Ihrem .NET-Projekt mit dem Importieren der erforderlichen Namespaces für Aspose.CAD. Dieser Schritt ermöglicht Ihnen den Zugriff auf die Klassen und Methoden, die für die Konvertierung von DGN-Bildern in Rasterbilder erforderlich sind.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DGN-Datei laden

 Laden Sie zunächst die DGN-Datei in ein`CadImage` Objekt. Dies stellt eine Grundlage für spätere Operationen dar.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Hier kommt Ihr Code zur weiteren Verarbeitung
}
```

## Schritt 2: Rasterisierungsoptionen definieren

 Ein ... kreieren`CadRasterizationOptions` Objekt und legen Sie verschiedene Eigenschaften fest, um den Rasterungsprozess entsprechend Ihren Anforderungen anzupassen.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Schritt 3: JpegOptions-Objekt erstellen

 Da wir die DGN-Datei in JPEG konvertieren möchten, erstellen Sie eine`JpegOptions` Objekt und weisen Sie das zuvor definierte zu`CadRasterizationOptions` dazu.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 4: Speichern Sie das Rasterbild

 Nutzen Sie die`Save` Methode der`CadImage` Klasse, um die DGN-Datei in ein Rasterbild im gewünschten Format zu exportieren, in diesem Fall ein JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Abschluss

Glückwunsch! Sie haben die Schritte zum Exportieren einer DGN-Datei in ein Rasterbild mit Aspose.CAD für .NET erfolgreich durchlaufen. Dieses Tutorial hat Ihnen das notwendige Wissen vermittelt, um diese Funktionalität mühelos in Ihre .NET-Projekte zu integrieren.

## FAQs

### F1: Kann ich DGN-Dateien in andere Formate als JPEG exportieren?

A1: Ja, Aspose.CAD für .NET unterstützt verschiedene Ausgabeformate. Sie können die Optionen in Schritt 3 entsprechend ändern.

### F2 Wie kann ich Ausnahmen während des Konvertierungsprozesses behandeln?

A2: Stellen Sie sicher, dass Sie über eine ordnungsgemäße Ausnahmebehandlung verfügen, wie im bereitgestellten Code gezeigt, um potenzielle Probleme zu beheben.

### F3: Gibt es eine Testversion für Aspose.CAD für .NET?

 A3: Ja, Sie können das Produkt mit einer kostenlosen Testversion erkunden. Besuchen[Hier](https://releases.aspose.com/) für mehr Informationen.

### F4: Wo kann ich Hilfe suchen oder Probleme im Zusammenhang mit Aspose.CAD für .NET besprechen?

 A4: Gehen Sie rüber zum[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F5: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für .NET?

 A5: Besuchen[dieser Link](https://purchase.aspose.com/temporary-license/)um eine temporäre Lizenz für Ihre Entwicklungsanforderungen zu erwerben.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
