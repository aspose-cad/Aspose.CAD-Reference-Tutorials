---
title: Exportieren Sie DGN als Teil von DWG in Aspose.CAD für .NET
linktitle: Exportieren Sie DGN als Teil von DWG
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie DGN als Teil von DWG in Aspose.CAD für .NET exportieren. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 11
url: /de/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Einführung

In der Welt der .NET-Entwicklung sticht Aspose.CAD als leistungsstarke Bibliothek für die Arbeit mit CAD-Dateien (Computer-Aided Design) hervor. Dieses Tutorial führt Sie durch den Prozess des Exportierens einer DGN-Datei (Design) als Teil einer DWG-Datei (Zeichnung) mit Aspose.CAD für .NET. Unabhängig davon, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, hilft Ihnen diese Schritt-für-Schritt-Anleitung dabei, die Funktionen von Aspose.CAD zu nutzen, um diese spezielle Aufgabe effizient zu lösen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass Sie die Aspose.CAD-Bibliothek für .NET installiert haben. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Richten Sie Ihre bevorzugte .NET-Entwicklungsumgebung ein, z. B. Visual Studio.

- Grundkenntnisse in C#: Machen Sie sich mit der Programmiersprache C# vertraut.

## Namespaces importieren

Fügen Sie in Ihr C#-Projekt die erforderlichen Namespaces ein, um auf die Aspose.CAD-Funktionalität zuzugreifen. Fügen Sie am Anfang Ihrer Codedatei die folgenden using-Anweisungen hinzu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Lassen Sie uns nun den bereitgestellten Code in mehrere Schritte aufteilen:

## Schritt 1: Dateipfade definieren

```csharp
//Eingabe- und Ausgabedateipfade
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Schritt 2: Erstellen Sie eine PdfOptions-Instanz

```csharp
// Erstellen Sie eine Instanz der PdfOptions-Klasse zum Exportieren von DWG in PDF
PdfOptions exportOptions = new PdfOptions();
```

## Schritt 3: DWG-Datei laden

```csharp
// Laden Sie die vorhandene DWG-Datei als Bild und konvertieren Sie sie in den CadImage-Typ
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Schritt 4: Durch Entitäten iterieren

```csharp
// Durchlaufen Sie jedes Element in der DWG-Datei
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Schritt 5: Überprüfen Sie den Entitätstyp

```csharp
// Überprüfen Sie, ob es sich bei der Entität um eine Bilddefinition handelt
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Schritt 6: Holen Sie sich den Unterlagepfad

```csharp
// Wenn es sich um eine Bilddefinition handelt, rufen Sie den externen Verweis auf das Objekt ab
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Schritt 7: Rasterisierungsoptionen definieren

```csharp
// Definieren Sie Einstellungen für das CadRasterizationOptions-Objekt
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Schritt 8: DWG in PDF exportieren

```csharp
// Exportieren Sie die DWG-Datei in eine PDF-Datei, indem Sie die Save-Methode aufrufen
cadImage.Save(outPath, exportOptions);
```

## Abschluss

Glückwunsch! Sie haben den Prozess des Exportierens einer DGN-Datei als Teil einer DWG-Datei mit Aspose.CAD für .NET erfolgreich durchlaufen. Dieses Tutorial hat Ihnen die grundlegenden Schritte und Codeausschnitte vermittelt, um diese spezielle Aufgabe nahtlos zu erledigen.

## FAQs

### F1: Kann ich Aspose.CAD für .NET in meinen kommerziellen Projekten verwenden?
 A1: Ja, das können Sie. Besuchen[Hier](https://purchase.aspose.com/buy) um Lizenzoptionen zu erkunden.

### F2: Gibt es Einschränkungen hinsichtlich der Größe der DWG-Dateien, die ich verarbeiten kann?
A2: Aspose.CAD unterstützt die Verarbeitung großer DWG-Dateien, es können jedoch Hardwareeinschränkungen gelten.

### F3: Gibt es eine Testversion?
A3: Ja, Sie können eine kostenlose Testversion erhalten[Hier](https://releases.aspose.com/).

### F4: Wie kann ich temporäre Lizenzen erhalten?
 A4: Es können temporäre Lizenzen erworben werden[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich Hilfe suchen, wenn ich auf Probleme stoße?
 A5: Sie können das Aspose.CAD-Forum besuchen[Hier](https://forum.aspose.com/c/cad/19) zur Unterstützung.