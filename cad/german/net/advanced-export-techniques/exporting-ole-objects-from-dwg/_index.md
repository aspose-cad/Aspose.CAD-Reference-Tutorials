---
title: Exportieren von OLE-Objekten aus DWG-Dateien – Aspose.CAD-Tutorial
linktitle: Exportieren von OLE-Objekten aus DWG-Dateien
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die Schritt-für-Schritt-Anleitung zum Exportieren von OLE-Objekten aus DWG-Dateien mit Aspose.CAD für .NET. Verbessern Sie mühelos Ihre Fähigkeiten im Umgang mit CAD-Dateien.
weight: 12
url: /de/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von OLE-Objekten aus DWG-Dateien – Aspose.CAD-Tutorial

## Einführung

Möchten Sie OLE-Objekte problemlos aus DWG-Dateien extrahieren? Aspose.CAD für .NET ist hier, um den Prozess für Sie zu optimieren. In diesem Tutorial führen wir Sie Schritt für Schritt durch den Export von OLE-Objekten, um sicherzustellen, dass Sie diese leistungsstarke .NET-Bibliothek optimal nutzen. 

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Bibliothek installiert haben. Sie können es hier herunterladen[Aspose.CAD für .NET-Downloadseite](https://releases.aspose.com/cad/net/).

-  Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre DWG-Dateien gespeichert werden. Ersetzen`"Your Document Directory"` im bereitgestellten Codeausschnitt mit dem tatsächlichen Pfad.

## Namespaces importieren

In Ihrem .NET-Projekt müssen Sie die erforderlichen Namespaces importieren, um die Funktionalitäten von Aspose.CAD nutzen zu können. Verwenden Sie den folgenden Codeausschnitt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt 1: Legen Sie das Dokumentverzeichnis fest

```csharp
string MyDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` mit dem Pfad, in dem sich Ihre DWG-Dateien befinden.

## Schritt 2: DWG-Dateien angeben

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Listen Sie die DWG-Dateien, die Sie verarbeiten möchten, im Array auf.

## Schritt 3: Exportoptionen konfigurieren

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Passen Sie die Exportoptionen entsprechend Ihren Anforderungen an. In diesem Beispiel konfigurieren wir den PNG-Export mit einem angegebenen Layout.

## Schritt 4: Dateien durchlaufen und exportieren

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Durchlaufen Sie die angegebenen DWG-Dateien, laden Sie jede einzelne und speichern Sie die exportierte PNG-Datei mit den definierten Optionen.

## Abschluss

Glückwunsch! Sie haben mit Aspose.CAD für .NET erfolgreich OLE-Objekte aus DWG-Dateien exportiert. Diese leistungsstarke Bibliothek vereinfacht komplexe Aufgaben und sorgt für Effizienz und Flexibilität bei der Bearbeitung von CAD-Dateien.

## FAQs

### F1: Ist Aspose.CAD für .NET sowohl für Junior- als auch Senior-CAD-Dateien geeignet?

A1: Ja, Aspose.CAD für .NET ist vielseitig und kann eine breite Palette von CAD-Dateien verarbeiten, einschließlich Junior- und Senior-Varianten.

### F2: Kann ich Exportoptionen für verschiedene Layouts anpassen?

A2: Auf jeden Fall! Wie im Tutorial gezeigt, können Sie Exportoptionen, einschließlich Layouts, an Ihre spezifischen Anforderungen anpassen.

### F3: Wo finde ich eine ausführliche Dokumentation zu Aspose.CAD für .NET?

 A3: Entdecken Sie die[Aspose.CAD für .NET-Dokumentation](https://reference.aspose.com/cad/net/) für ausführliche Informationen und Beispiele.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können die Funktionen von Aspose.CAD für .NET mit einer kostenlosen Testversion erleben. Besuchen[dieser Link](https://releases.aspose.com/) um loszulegen.

### F5: Wie kann ich Unterstützung erhalten oder mit der Community in Kontakt treten?

 A5: Für Unterstützung und Community-Engagement besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
