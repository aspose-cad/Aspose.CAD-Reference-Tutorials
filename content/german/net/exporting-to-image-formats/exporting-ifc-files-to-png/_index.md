---
title: IFC-Dateien nach PNG exportieren – Aspose.CAD-Tutorial
linktitle: IFC-Dateien nach PNG exportieren
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie Aspose.CAD für .NET, eine robuste Lösung für die nahtlose Konvertierung von IFC in PNG. Jetzt herunterladen für eine effiziente CAD-Dateiverarbeitung.
type: docs
weight: 10
url: /de/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---
## Einführung

In der dynamischen Welt des computergestützten Designs (CAD) ist eine effiziente Dateikonvertierung von entscheidender Bedeutung. Aspose.CAD für .NET erweist sich als leistungsstarkes Tool, das nahtlose Funktionen zum Exportieren von IFC-Dateien (Industry Foundation Classes) in das PNG-Format bietet. Dieses Schritt-für-Schritt-Tutorial führt Sie durch den Prozess und sorgt für ein reibungsloses Erlebnis mit Aspose.CAD.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### 1. Aspose.CAD-Installation

 Stellen Sie sicher, dass Aspose.CAD für .NET installiert ist. Sie können es von der Release-Seite herunterladen[Hier](https://releases.aspose.com/cad/net/).

### 2. Dokumentenverzeichnis

 Erstellen Sie ein bestimmtes Verzeichnis für Ihre Dokumente. Im bereitgestellten Beispiel ist die Variable`MyDir` stellt das Dokumentenverzeichnis dar.

## Namespaces importieren

Nachdem Sie nun die Voraussetzungen eingerichtet haben, importieren wir die erforderlichen Namespaces in Ihre .NET-Anwendung, um die Aspose.CAD-Funktionen zu nutzen.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Schritt 1: IFC-Datei laden

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 In diesem Schritt initialisieren wir Aspose.CAD`IfcImage` Objekt und laden Sie die IFC-Datei hinein.

## Schritt 2: Rasterisierungsoptionen festlegen

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definieren Sie Rasterisierungsoptionen, um die Seitenbreite und -höhe für die PNG-Ausgabe zu konfigurieren.

## Schritt 3: PNG-Optionen festlegen

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Erstellen Sie PNG-Optionen und verknüpfen Sie die zuvor definierten Rasterisierungsoptionen.

## Schritt 4: Geben Sie den Ausgabepfad an

```csharp
    // Legen Sie auch den Ausgabepfad fest
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definieren Sie den Ausgabepfad für die PNG-Datei und stellen Sie sicher, dass sie denselben Namen wie die Quelldatei mit der Erweiterung „.png“ hat. Speichern Sie abschließend das konvertierte Bild.

## Abschluss

Mit diesen einfachen Schritten haben Sie mit Aspose.CAD für .NET erfolgreich eine IFC-Datei nach PNG exportiert. Dieses vielseitige Tool vereinfacht den CAD-Konvertierungsprozess und macht ihn für Entwickler und Ingenieure zugänglich.

## FAQs

### F1: Kann ich Aspose.CAD für .NET unter macOS oder Linux verwenden?

A1: Nein, Aspose.CAD für .NET wurde speziell für Windows-Umgebungen entwickelt.

### F2: Ist zu Testzwecken eine temporäre Lizenz verfügbar?

 A2: Ja, Sie können eine temporäre Lizenz erhalten von[Hier](https://purchase.aspose.com/temporary-license/) zur Auswertung.

### F3: Wie kann ich Unterstützung für Aspose.CAD erhalten?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F4: Wo finde ich eine umfassende Dokumentation?

 A4: Siehe[Aspose.CAD-Dokumentation](https://reference.aspose.com/cad/net/) Ausführliche Informationen und Beispiele finden Sie hier.

### F5: Was passiert, wenn während der Installation Probleme auftreten?

 A5: Überprüfen Sie die Dokumentation oder bitten Sie um Hilfe[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).