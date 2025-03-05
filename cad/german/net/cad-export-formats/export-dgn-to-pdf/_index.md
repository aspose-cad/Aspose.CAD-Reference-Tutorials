---
title: Exportieren Sie DGN als PDF in Aspose.CAD für .NET
linktitle: DGN in PDF exportieren
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie DGN-Dateien mit Aspose.CAD für .NET mühelos in PDF exportieren. Eine Schritt-für-Schritt-Anleitung für die nahtlose Bearbeitung von CAD-Dateien.
type: docs
weight: 12
url: /de/net/cad-export-formats/export-dgn-to-pdf/
---
## Einführung

In der Welt der .NET-Entwicklung ist Aspose.CAD eine leistungsstarke Bibliothek, die die Bearbeitung und Konvertierung von CAD-Dateien erleichtert. Eine häufige Aufgabe für Entwickler ist das Exportieren von DGN-Dateien in das PDF-Format. In diesem Tutorial führen wir den Prozess Schritt für Schritt durch, indem wir Aspose.CAD für .NET verwenden.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Folgendes vorhanden ist:

- Grundkenntnisse in C# und dem .NET Framework.
-  Aspose.CAD für .NET-Bibliothek installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/net/).
- Eine Beispiel-DGN-Datei, zum Beispiel „Nikon_D90_Camera.dgn“ für dieses Tutorial.

## Namespaces importieren

Beginnen Sie in Ihrem C#-Projekt mit dem Importieren der erforderlichen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DGN-Datei laden

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Ihr Code hier...
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Schritt 3: PDF-Optionen erstellen

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 4: Als PDF speichern

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Abschluss

Glückwunsch! Sie haben mit Aspose.CAD für .NET erfolgreich eine DGN-Datei in PDF exportiert. In diesem Tutorial wurden die wesentlichen Schritte behandelt, vom Laden der DGN-Datei über die Konfiguration der Rasterisierungsoptionen bis hin zum Speichern der Ausgabe als PDF.

## FAQs

### F1: Kann ich Aspose.CAD für .NET ohne CAD-Vorkenntnisse verwenden?

A1: Auf jeden Fall! Aspose.CAD vereinfacht komplexe CAD-Aufgaben und macht es für Entwickler mit unterschiedlichem Hintergrund zugänglich.

### F2: Wo finde ich weitere Beispiele und Dokumentation für Aspose.CAD?

 A2: Entdecken Sie die[Dokumentation](https://reference.aspose.com/cad/net/) Ausführliche Anleitungen und Beispiele finden Sie hier.

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD?

A3: Ja, Sie können eine kostenlose Testversion erhalten[Hier](https://releases.aspose.com/).

### F4: Wie kann ich temporäre Lizenzen für Aspose.CAD erhalten?

 A4: Besorgen Sie sich temporäre Lizenzen[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Benötigen Sie Hilfe oder haben Sie Fragen?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft.