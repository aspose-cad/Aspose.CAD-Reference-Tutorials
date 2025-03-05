---
title: Unterstützung von 3D für DGN V7 in Aspose.CAD für .NET
linktitle: Unterstützung von 3D für DGN V7
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Nutzen Sie die Leistungsfähigkeit der 3D-Unterstützung für DGN V7 in Aspose.CAD für .NET. Folgen Sie unserer Schritt-für-Schritt-Anleitung.
type: docs
weight: 20
url: /de/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## Einführung

Willkommen zu unserem umfassenden Tutorial zur Nutzung der 3D-Unterstützung für DGN V7 in Aspose.CAD für .NET! Aspose.CAD ist eine leistungsstarke Bibliothek, die Entwicklern die nahtlose Arbeit mit CAD-Dateien in ihren .NET-Anwendungen ermöglicht. In diesem Tutorial erläutern wir die Schritte zur Nutzung der 3D-Unterstützung für DGN V7 und vermitteln Ihnen das Wissen, um Ihre CAD-bezogenen Projekte zu verbessern.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass Aspose.CAD für .NET installiert ist. Wenn nicht, können Sie es hier herunterladen[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Richten Sie eine geeignete Entwicklungsumgebung wie Visual Studio für die .NET-Anwendungsentwicklung ein.

- Beispiel-DGN-Datei: Halten Sie eine Beispiel-DGN-Datei zum Testen bereit. Sie können die bereitgestellte Beispieldatei „Nikon_D90_Camera.dgn“ verwenden.

Beginnen wir nun mit den Schritten zum Erreichen der 3D-Unterstützung für DGN V7 mit Aspose.CAD für .NET!

## Namespaces importieren

Beginnen Sie in Ihrer .NET-Anwendung mit dem Importieren der erforderlichen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: Richten Sie Ihr Dokumentenverzeichnis ein

 Stellen Sie sicher, dass in Ihrem Projekt ein Dokumentenverzeichnis eingerichtet ist. Ersetzen`"Your Document Directory"` mit dem tatsächlichen Pfad zu Ihrem Dokumentverzeichnis.

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: Laden Sie die DGN-Datei

Laden Sie die vorhandene DGN-Datei als CadImage mit dem folgenden Code:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Hier kommt Ihr Code zur weiteren Verarbeitung
}
```

## Schritt 3: PDF-Exportoptionen konfigurieren

Richten Sie Optionen für den Export in PDF ein und legen Sie Optionen für die Vektorrasterung fest, z. B. Seitenabmessungen, automatische Layoutskalierung, Hintergrundfarbe und zu exportierende Layouts.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Exportieren Sie nur bestimmte Ansichten
    }
};
```

## Schritt 4: Speichern Sie das Rasterbild

Speichern Sie die DGN-Datei als Rasterbild mit den konfigurierten Optionen.

```csharp
dgnImage.Save(outFile, options);
```

## Abschluss

Glückwunsch! Sie haben Aspose.CAD für .NET erfolgreich verwendet, um eine DGN-Datei mit 3D-Unterstützung in ein Rasterbild zu exportieren. Dieses Tutorial hat Sie mit den wesentlichen Schritten ausgestattet, um diese Funktionalität in Ihre CAD-Projekte zu integrieren.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Dateiformate, einschließlich DWG und DXF.

### F2: Wie kann ich mit Ausnahmen umgehen, wenn ich mit Aspose.CAD arbeite?

A2: Binden Sie Ihren Code in einen Try-Catch-Block ein, wie im bereitgestellten Beispiel gezeigt, um Ausnahmen ordnungsgemäß zu behandeln.

### F3: Ist Aspose.CAD für kommerzielle Projekte geeignet?

 A3: Auf jeden Fall! Sie können Aspose.CAD für .NET erwerben[Hier](https://purchase.aspose.com/buy).

### F4: Kann ich Aspose.CAD für .NET vor dem Kauf testen?

A4: Auf jeden Fall! Entdecken Sie die kostenlose Testversion[Hier](https://releases.aspose.com/).

### F5: Wo finde ich Community-Unterstützung für Aspose.CAD für .NET?

 A5: Besuchen Sie das Community-Forum[Hier](https://forum.aspose.com/c/cad/19).