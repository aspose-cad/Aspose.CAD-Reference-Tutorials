---
title: Unterstützte DGN-Elemente in Aspose.CAD für .NET
linktitle: Unterstützte DGN-Elemente
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die leistungsstarken Funktionen von Aspose.CAD für .NET für die Verarbeitung von DGN-Dateien. Befolgen Sie unsere Schritt-für-Schritt-Anleitung, um nahtlos mit 2D- und 3D-Elementen zu arbeiten.
type: docs
weight: 18
url: /de/net/cad-features-and-support/supported-dgn-elements/
---
## Einführung

Sind Sie ein .NET-Entwickler und möchten nahtlos mit DGN-Dateien arbeiten? Aspose.CAD für .NET bietet eine robuste Lösung für die effiziente Verarbeitung von DGN-Dateien. In diesem Tutorial befassen wir uns mit den unterstützten DGN-Elementen und führen Sie durch den Prozess der Arbeit mit Aspose.CAD für .NET.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Grundkenntnisse der .NET-Programmierung.
- Visual Studio ist auf Ihrem Computer installiert.
-  Aspose.CAD für .NET-Bibliothek, die Sie herunterladen können[Hier](https://releases.aspose.com/cad/net/).

## Namespaces importieren

Um Ihr Projekt anzukurbeln, importieren Sie die erforderlichen Namespaces in Ihre .NET-Anwendung. Dieser Schritt stellt sicher, dass Sie Zugriff auf die von Aspose.CAD für .NET bereitgestellten Funktionen haben.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Schritt 1: Laden Sie die DGN-Datei

Laden Sie zunächst eine vorhandene DGN-Datei als CadImage in Ihre .NET-Anwendung.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Ihr Code hier
}
```

## Schritt 2: Durchlaufen Sie DGN-Elemente

Durchlaufen Sie die DGN-Elemente mithilfe einer foreach-Schleife. Aspose.CAD für .NET bietet eine Vielzahl von DGN-Elementtypen, mit denen Sie arbeiten können.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Ihr Code hier
}
```

## Schritt 3: Behandeln Sie zuvor unterstützte Entitäten

Behandeln Sie die zuvor unterstützten 2D-Elemente, die jetzt auch für 3D unterstützt werden.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Zusätzliche Fälle
        {
            // Ihr Code hier
            break;
        }
}
```

## Schritt 4: Behandeln Sie unterstützte 3D-Elemente

Behandeln Sie die unterstützten 3D-Elemente, die von Aspose.CAD für .NET bereitgestellt werden.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Ihr Code hier
            break;
        }
}
```

## Schritt 5: Exportieren und speichern

Exportieren Sie abschließend die geänderte DGN-Datei in ein Rasterbild und speichern Sie es im angegebenen Verzeichnis.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Abschluss

In diesem Tutorial haben wir die Möglichkeiten von Aspose.CAD für .NET bei der Handhabung und Bearbeitung von DGN-Dateien untersucht. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie effizient mit unterstützten DGN-Elementen arbeiten, unabhängig davon, ob es sich um 2D- oder 3D-Elemente handelt. Aspose.CAD für .NET ermöglicht Ihnen die nahtlose Integration der DGN-Dateiverarbeitung in Ihre .NET-Anwendungen.

## FAQs

### F1: Wo finde ich die Dokumentation für Aspose.CAD für .NET?

 A1: Sie finden die Dokumentation[Hier](https://reference.aspose.com/cad/net/).

### F2: Wie lade ich Aspose.CAD für .NET herunter?

 A2: Sie können die Bibliothek herunterladen[Hier](https://releases.aspose.com/cad/net/).

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?

 A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wo kann ich temporäre Lizenzen für Aspose.CAD für .NET erhalten?

 A4: Temporäre Lizenzen sind verfügbar[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Benötigen Sie Hilfe oder haben Sie Fragen?

 A5: Besuchen Sie die Aspose.CAD für .NET-Community[Hilfeforum](https://forum.aspose.com/c/cad/19).