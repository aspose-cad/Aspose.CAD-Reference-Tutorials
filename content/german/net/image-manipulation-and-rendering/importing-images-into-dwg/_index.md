---
title: Importieren von Bildern in DWG-Dateien mit C# – Aspose.CAD-Handbuch
linktitle: Importieren von Bildern in DWG-Dateien mit C#
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie Bilder mit C# mit Aspose.CAD für .NET in DWG-Dateien importieren. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 11
url: /de/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## Einführung

Im Bereich des computergestützten Designs (CAD) ist das Einbinden von Bildern in DWG-Dateien eine häufige und entscheidende Aufgabe. Aspose.CAD für .NET bietet leistungsstarke Tools zur Optimierung dieses Prozesses und macht ihn für C#-Entwickler zugänglich. In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie Bilder in DWG-Dateien importieren.

## Voraussetzungen

Bevor Sie in den Leitfaden eintauchen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Grundkenntnisse der C#-Programmierung.
-  Aspose.CAD für .NET installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/net/).
- Eine Entwicklungsumgebung eingerichtet.

## Namespaces importieren

Stellen Sie sicher, dass Sie die erforderlichen Namespaces in Ihr C#-Projekt aufnehmen:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt 1: Richten Sie Ihr Dokumentenverzeichnis ein

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: Laden Sie die DWG-Datei

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Schritt 3: Definieren Sie die Bildeigenschaften

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Schritt 4: Einfügepunkt und Vektoren festlegen

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Schritt 5: Erstellen und konfigurieren Sie das Rasterbild

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Schritt 6: Bild zur DWG-Datei hinzufügen

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Schritt 7: Als PDF speichern

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Abschluss

Die Integration von Bildern in DWG-Dateien mit C# und Aspose.CAD für .NET ist ein nahtloser Prozess, der es Entwicklern ermöglicht, ihre CAD-Projekte mühelos mit visuellen Elementen zu erweitern.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen Programmiersprachen verwenden?

A1: Aspose.CAD ist in erster Linie für .NET konzipiert, Aspose bietet jedoch Bibliotheken für verschiedene Programmiersprachen.

### F2: Ist eine kostenlose Testversion für Aspose.CAD für .NET verfügbar?

 A2: Ja, Sie können eine kostenlose Testversion ausprobieren[Hier](https://releases.aspose.com/).

### F3: Wo finde ich eine ausführliche Dokumentation zu Aspose.CAD?

 A3: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/cad/net/).

### F4: Wie kann ich eine temporäre Lizenz für Aspose.CAD für .NET erhalten?

 A4: Besuchen[dieser Link](https://purchase.aspose.com/temporary-license/) um eine befristete Lizenz zu erhalten.

### F5: Gibt es Community-Foren für Aspose.CAD-Unterstützung?

 A5: Ja, Sie können Unterstützung suchen und sich in der Community engagieren[Hier](https://forum.aspose.com/c/cad/19).