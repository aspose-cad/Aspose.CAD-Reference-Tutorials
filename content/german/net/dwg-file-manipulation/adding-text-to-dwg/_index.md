---
title: Text zu DWG-Dateien in C# hinzufügen – Aspose.CAD-Tutorial
linktitle: Text zu DWG-Dateien in C# hinzufügen
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie mit C# und Aspose.CAD Text zu DWG-Dateien hinzufügen. Befolgen Sie diese Schritt-für-Schritt-Anleitung für eine nahtlose Integration. Umfassende Anleitungen finden Sie in der Aspose.CAD-Dokumentation.
type: docs
weight: 14
url: /de/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Einführung

Im dynamischen Bereich des computergestützten Designs (CAD) und der .NET-Entwicklung sticht Aspose.CAD als leistungsstarkes Werkzeug zur Bearbeitung von DWG-Dateien hervor. Das Hinzufügen von Text zu DWG-Dateien ist eine häufige Anforderung. In diesem Tutorial erfahren Sie, wie Sie dies mit C# und Aspose.CAD erreichen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Folgendes vorhanden ist:

-  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek von herunter und installieren Sie sie[Download-Link](https://releases.aspose.com/cad/net/).

-  Dokumentenverzeichnis: Richten Sie ein Verzeichnis für Ihre Dokumente ein und notieren Sie den Pfad als`MyDir`.

Lassen Sie uns nun den Prozess in überschaubare Schritte unterteilen.

## Namespaces importieren

Fügen Sie in Ihren C#-Code die erforderlichen Namespaces ein, um auf Aspose.CAD-Funktionen zuzugreifen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: DWG-Datei laden

 Laden Sie die DWG-Datei in eine`Image` Objekt mithilfe der Aspose.CAD-Bibliothek.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Ihr Code für die nachfolgenden Schritte finden Sie hier
}
```

## Schritt 2: CadText-Objekt erstellen

 Instanziieren Sie a`CadText` Objekt, das den Text darstellt, den Sie der DWG-Datei hinzufügen möchten.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## Schritt 3: Text zur DWG hinzufügen

 Fügen Sie das erstellte hinzu`CadText` Objekt mit Aspose.CAD in die DWG-Datei einfügen.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Schritt 4: PDF-Optionen konfigurieren

Konfigurieren Sie PDF-Optionen zum Speichern der geänderten DWG-Datei als PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Schritt 5: Als PDF speichern

Speichern Sie die geänderte DWG-Datei als PDF mit dem hinzugefügten Text.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Jetzt haben Sie mit C# und Aspose.CAD erfolgreich Text zu einer DWG-Datei hinzugefügt. Entdecken Sie gerne weitere Features und Funktionalitäten von Aspose.CAD für Ihre CAD-Manipulationsanforderungen.

## Abschluss

In diesem Tutorial haben wir die wesentlichen Schritte zum Hinzufügen von Text zu DWG-Dateien mit C# und Aspose.CAD behandelt. Diese leistungsstarke Kombination eröffnet Möglichkeiten für die dynamische und individuelle Erstellung von CAD-Dokumenten.

## FAQs

### F1: Ist Aspose.CAD mit allen Versionen von DWG-Dateien kompatibel?

A1: Aspose.CAD unterstützt eine Vielzahl von DWG-Dateiversionen und gewährleistet so die Kompatibilität mit verschiedenen CAD-Softwareprogrammen.

### F2: Kann ich mit Aspose.CAD mehrere Textelemente zu einer einzelnen DWG-Datei hinzufügen?

A2: Ja, Sie können einer DWG-Datei mehrere Textelemente hinzufügen, indem Sie den im Tutorial beschriebenen Vorgang wiederholen.

### F3: Wie kann ich die Schriftart und den Textstil in Aspose.CAD ändern?

 A3: Um die Schriftart und den Textstil zu ändern, passen Sie die Eigenschaften an`CadText` Objekt, bevor Sie es der DWG-Datei hinzufügen.

### F4: Gibt es lizenzrechtliche Überlegungen für die Verwendung von Aspose.CAD in einem kommerziellen Projekt?

 A4: Ja, stellen Sie die Einhaltung der Aspose.CAD-Lizenzbedingungen sicher. Beziehen auf[Aspose.CAD-Kauf](https://purchase.aspose.com/buy) für Details.

### F5: Wo kann ich Hilfe suchen oder Aspose.CAD-bezogene Fragen besprechen?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19)um mit der Community in Kontakt zu treten und Unterstützung zu erhalten.