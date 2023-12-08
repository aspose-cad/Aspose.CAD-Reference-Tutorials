---
title: Farben in CAD-Dateien rendern – Aspose.CAD-Handbuch
linktitle: Farben in CAD-Dateien rendern
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Master-CAD-Datei-Rendering in .NET mit Aspose.CAD. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für lebendige Farben.
type: docs
weight: 10
url: /de/net/conversion-and-export/rendering-colors-in-cad-files/
---
## Einführung

Stehen Sie vor der Herausforderung, Farben in CAD-Dateien mithilfe von .NET wiederzugeben? Suchen Sie nicht weiter! In dieser umfassenden Anleitung führen wir Sie mithilfe der leistungsstarken Aspose.CAD-Bibliothek Schritt für Schritt durch den Prozess. Am Ende dieses Tutorials verfügen Sie über das nötige Wissen, um Farben in Ihren CAD-Dateien mühelos wiederzugeben.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek herunter und installieren Sie sie[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Stellen Sie sicher, dass Sie eine .NET-Entwicklungsumgebung eingerichtet haben.

- CAD-Datei: Halten Sie eine Beispiel-CAD-Datei zum Testen bereit. Für dieses Tutorial können Sie „test1.dwg“ verwenden.

## Namespaces importieren

Importieren Sie in Ihrem .NET-Projekt die erforderlichen Namespaces, um auf die Aspose.CAD-Funktionen zuzugreifen. Fügen Sie am Anfang Ihres Codes die folgenden Zeilen hinzu:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Schritt 1: Richten Sie Ihr Projekt ein

Erstellen Sie ein neues .NET-Projekt und richten Sie die erforderlichen Verzeichnisse ein. Stellen Sie sicher, dass in Ihrem Projekt auf die Aspose.CAD-Bibliothek verwiesen wird.

## Schritt 2: Dateipfade definieren

Geben Sie die Pfade für Ihre Eingabe-CAD-Datei und die Ausgabe-PNG-Datei an. Aktualisieren Sie die folgenden Zeilen in Ihrem Code:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## Schritt 3: CAD-Datei laden

Verwenden Sie den folgenden Code, um die CAD-Datei zu öffnen und zu laden:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## Schritt 4: Rasterisierungsoptionen konfigurieren

Konfigurieren Sie die Rasterisierungsoptionen, um den Rendervorgang anzupassen. Aktualisieren Sie die folgenden Zeilen:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## Schritt 5: Speichern Sie das gerenderte Bild

Speichern Sie das gerenderte Bild mit den angegebenen Optionen:

```csharp
document.Save(output, saveOptions);
```

## Abschluss

Glückwunsch! Sie haben mit Aspose.CAD für .NET erfolgreich Farben in CAD-Dateien gerendert. Diese Schritt-für-Schritt-Anleitung hat Ihnen die Fähigkeiten vermittelt, Ihre CAD-Rendering-Fähigkeiten zu verbessern.

## FAQs

### F1: Kann ich Aspose.CAD kostenlos nutzen?

 A1: Aspose.CAD bietet eine kostenlose Testversion an[Hier](https://releases.aspose.com/)Sie können die Funktionen erkunden, bevor Sie einen Kauf tätigen.

### F2: Wo finde ich eine ausführliche Dokumentation zu Aspose.CAD?

 A2: Sehen Sie sich die Dokumentation an[Hier](https://reference.aspose.com/cad/net/) Ausführliche Informationen zu den Funktionen von Aspose.CAD finden Sie hier.

### F3: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD?

 A3: Besorgen Sie sich eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/) zu Testzwecken.

### F4: Benötigen Sie Hilfe oder haben Sie Fragen?

 A4: Besuchen Sie die Aspose.CAD-Community[Forum](https://forum.aspose.com/c/cad/19) für Unterstützung und Diskussionen.

### F5: Wo kann ich die Aspose.CAD-Bibliothek kaufen?

 A5: Kaufen Sie Aspose.CAD[Hier](https://purchase.aspose.com/buy) um sein volles Potenzial auszuschöpfen.