---
title: Rendern von DWG-Dokumenten in C# – Aspose.CAD-Handbuch
linktitle: Rendern von DWG-Dokumenten in C#
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie DWG-Dokumente in C# mit Aspose.CAD rendern. Diese Schritt-für-Schritt-Anleitung behandelt das Importieren, Konfigurieren und Speichern anhand von Codebeispielen.
type: docs
weight: 17
url: /de/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## Einführung

Willkommen beim umfassenden Leitfaden zum Rendern von DWG-Dokumenten in C# mit Aspose.CAD. Unabhängig davon, ob Sie ein erfahrener Entwickler sind oder gerade erst mit .NET beginnen, führt Sie dieses Tutorial durch den Prozess der Nutzung von Aspose.CAD zum effizienten Rendern von DWG-Dateien. Aspose.CAD ist eine leistungsstarke API, die robuste Funktionalitäten für die Arbeit mit CAD-Dateiformaten bietet und damit eine erste Wahl für Entwickler ist, die mit DWG-Dateien arbeiten.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Grundkenntnisse der Programmiersprache C#.
- Visual Studio ist auf Ihrem Computer installiert.
-  Aspose.CAD-Bibliothek in Ihr Projekt integriert. Sie können es herunterladen unter[Hier](https://releases.aspose.com/cad/net/).
- Eine Beispiel-DWG-Datei, z. B. „Bottom_plate.dwg“, als Ergänzung zu den Beispielen.

## Namespaces importieren

Stellen Sie zunächst sicher, dass Sie die erforderlichen Namespaces am Anfang Ihres C#-Codes importieren:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Lassen Sie uns nun das bereitgestellte Beispiel in mehrere Schritte unterteilen:

## Schritt 1: Laden Sie die DWG-Datei

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Ihr Code zum Laden der DWG-Datei finden Sie hier.
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Hier können zusätzliche Rasterisierungskonfigurationen hinzugefügt werden.
```

## Schritt 3: Definieren Sie den zu zeichnenden Bereich

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Schritt 4: Erstellen Sie ein neues Ansichtsfenster

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Schritt 5: Aktives Ansichtsfenster ersetzen

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Schritt 6: PDF-Optionen konfigurieren

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 7: Speichern Sie die gerenderte DWG-Datei als PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Abschluss

Glückwunsch! Sie haben ein DWG-Dokument mit Aspose.CAD in C# erfolgreich in PDF gerendert. Entdecken Sie gerne weitere Funktionen und passen Sie den Code an Ihre spezifischen Anforderungen an.

## FAQs

### F1: Kann ich Aspose.CAD mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate, einschließlich DWG, DXF, DWF und mehr.

### F2: Ist Aspose.CAD mit .NET Core kompatibel?

A2: Ja, Aspose.CAD ist sowohl mit .NET Framework als auch .NET Core kompatibel.

### F3: Wie kann ich unterschiedliche Layouts in einer DWG-Datei verarbeiten?

 A3: Sie können das gewünschte Layout im festlegen`Layouts` Eigentum von`CadRasterizationOptions`.

### F4: Gibt es irgendwelche Lizenzaspekte für die Verwendung von Aspose.CAD?

 A4: Einzelheiten zur Lizenzierung finden Sie unter[Hier](https://purchase.aspose.com/buy).

### F5: Wo finde ich zusätzliche Unterstützung?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.