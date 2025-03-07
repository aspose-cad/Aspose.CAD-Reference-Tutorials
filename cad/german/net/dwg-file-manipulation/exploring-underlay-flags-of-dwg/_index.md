---
title: Unterlageflaggen von DWG-Dateien erkunden – Aspose.CAD-Tutorial
linktitle: Erkunden der Underlay-Flags von DWG-Dateien
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Nutzen Sie die Leistungsfähigkeit von Aspose.CAD für .NET beim Erkunden von DWG-Dateiunterlage-Flags. Folgen Sie unserer Schritt-für-Schritt-Anleitung.
weight: 13
url: /de/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterlageflaggen von DWG-Dateien erkunden – Aspose.CAD-Tutorial

## Einführung

Wenn Sie in die komplizierte Welt der CAD-Dateien, insbesondere DWG-Dateien, eintauchen und die Geheimnisse der Underlay-Flags lüften möchten, sind Sie hier richtig. Dieses Tutorial führt Sie durch den Prozess der Untersuchung von Underlay-Flags in DWG-Dateien mithilfe der leistungsstarken Bibliothek Aspose.CAD für .NET.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Ein grundlegendes Verständnis der C#- und .NET-Programmierung.
-  Aspose.CAD für .NET-Bibliothek installiert. Wenn nicht, können Sie es herunterladen[Hier](https://releases.aspose.com/cad/net/).
- Eine DWG-Datei zum Testen. Sie können die im Tutorial bereitgestellte Beispieldatei „BlockRefDgn.dwg“ verwenden.

## Namespaces importieren

Um zu beginnen, müssen Sie die erforderlichen Namespaces importieren. Hier ist ein Ausschnitt, der Ihnen helfen soll:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Schritt 1: DWG-Datei laden und in CadImage konvertieren

Laden Sie zunächst die vorhandene DWG-Datei und konvertieren Sie sie in ein CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Laden Sie die DWG-Datei und konvertieren Sie sie in CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Hier finden Sie Ihren Code für die weiteren Schritte
}
```

## Schritt 2: Durch Entitäten iterieren

Als nächstes durchlaufen Sie jedes Element in der DWG-Datei:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Hier finden Sie Ihren Code für die weiteren Schritte
}
```

## Schritt 3: Überprüfen Sie den CadDgnUnderlay-Typ

Überprüfen Sie, ob die Entität vom Typ CadDgnUnderlay ist:

```csharp
if (entity is CadDgnUnderlay)
{
    // Hier finden Sie Ihren Code für die weiteren Schritte
}
```

## Schritt 4: Greifen Sie auf die Underlay-Flags zu

Greifen Sie auf verschiedene Underlay-Flags zu und extrahieren Sie relevante Informationen:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Abschluss

Glückwunsch! Sie haben die Underlay-Flags von DWG-Dateien mit Aspose.CAD für .NET erfolgreich untersucht. Dieses Tutorial vermittelt Ihnen das Wissen, durch Entitäten zu navigieren und wichtige Informationen über Unterlagen zu extrahieren.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen CAD-Dateiformaten verwenden?

A1: Aspose.CAD unterstützt verschiedene CAD-Formate, einschließlich DWG, DXF, DGN und mehr. Die vollständige Liste finden Sie in der Dokumentation.

### F2: Ist eine temporäre Lizenz für Aspose.CAD für .NET verfügbar?

 A2: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F3: Wo finde ich Unterstützung für Aspose.CAD für .NET?

 A3: Besuchen Sie das Support-Forum[Hier](https://forum.aspose.com/c/cad/19) zur Hilfe.

### F4: Wie kaufe ich Aspose.CAD für .NET?

A4: Kaufen Sie die Bibliothek[Hier](https://purchase.aspose.com/buy).

### F5: Gibt es eine kostenlose Testversion?

 A5: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
