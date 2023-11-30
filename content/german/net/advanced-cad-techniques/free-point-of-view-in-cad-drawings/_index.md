---
title: Kostenloser Standpunkt in CAD-Zeichnungen – Aspose.CAD-Handbuch
linktitle: Kostenloser Standpunkt in CAD-Zeichnungen
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die Freiheit der CAD-Visualisierung mit Aspose.CAD für .NET. Folgen Sie unserer Schritt-für-Schritt-Anleitung für eine einzigartige Sichtweise.
type: docs
weight: 11
url: /de/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---
Im Bereich des computergestützten Designs (CAD) ist die Erlangung einer freien Sicht auf Zeichnungen ein entscheidender Aspekt bei der Visualisierung und Präsentation komplexer Designs. Aspose.CAD für .NET bietet eine robuste Lösung, um diese Freiheit zu erreichen und Benutzern die einfache Bearbeitung und Optimierung von CAD-Zeichnungen zu ermöglichen. In dieser Schritt-für-Schritt-Anleitung untersuchen wir den Prozess, mit Aspose.CAD für .NET eine freie Sicht auf CAD-Zeichnungen zu erhalten.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Aspose.CAD-Installation
 Stellen Sie sicher, dass Aspose.CAD für .NET in Ihrer Entwicklungsumgebung installiert ist. Wenn nicht, können Sie es hier herunterladen[Aspose.CAD-Website](https://releases.aspose.com/cad/net/).

2. CAD-Zeichnungsdatei
Bereiten Sie eine CAD-Zeichnungsdatei vor, die Sie bearbeiten möchten. Für diese Anleitung verwenden wir eine Beispieldatei mit dem Namen „conic_pyramid.dxf“.

3. Entwicklungsumgebung
Richten Sie eine funktionierende .NET-Entwicklungsumgebung mit Visual Studio oder einer beliebigen bevorzugten IDE ein.

## Namespaces importieren

Importieren Sie in Ihr .NET-Projekt die erforderlichen Namespaces für die Aspose.CAD-Funktionalität. Fügen Sie am Anfang Ihrer Datei den folgenden Codeausschnitt hinzu:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## Schritt 1: Dokumentenverzeichnis definieren

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string MyDir = "Your Document Directory";
```

Stellen Sie sicher, dass Sie „Ihr Dokumentverzeichnis“ durch den tatsächlichen Pfad zu Ihrem Dokumentverzeichnis ersetzen.

## Schritt 2: Quelldatei angeben

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

Geben Sie den Pfad zu Ihrer CAD-Zeichnungsdatei an.

## Schritt 3: Ausgabepfad festlegen

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

Definieren Sie den Pfad, in dem die manipulierte CAD-Zeichnung gespeichert wird.

## Schritt 4: CAD-Bild laden

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Laden Sie die CAD-Zeichnung mit Aspose.CAD.

## Schritt 5: JPEG-Optionen konfigurieren

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

Konfigurieren Sie die Optionen zum Exportieren der CAD-Zeichnung in das JPEG-Format.

## Schritt 6: Drehwinkel einstellen

```csharp
float xAngle = 10; //Drehwinkel entlang der X-Achse
float yAngle = 30; //Drehwinkel entlang der Y-Achse
float zAngle = 40; //Drehwinkel entlang der Z-Achse
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

Geben Sie die Drehwinkel entlang der X-, Y- und Z-Achse an, um den gewünschten Blickwinkel zu erreichen.

## Schritt 7: Speichern Sie die manipulierte CAD-Zeichnung

```csharp
cadImage.Save(outPath, options);
}
```

Speichern Sie die manipulierte CAD-Zeichnung im angegebenen Ausgabepfad.

## Schritt 8: Erfolgsmeldung anzeigen

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

Informieren Sie den Benutzer über den erfolgreichen Export des 3D-Bildes.

## Abschluss

In diesem Tutorial haben wir den Prozess untersucht, wie man mit Aspose.CAD für .NET eine freie Sicht auf CAD-Zeichnungen erhält. Wenn Sie diese Schritt-für-Schritt-Anleitungen befolgen, können Sie Ihre CAD-Visualisierungsfähigkeiten verbessern und Ihre Entwürfe aus einer neuen Perspektive präsentieren.


## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD für .NET unterstützt verschiedene CAD-Dateiformate, einschließlich DWG und DXF.

### F2: Gibt es eine Testversion von Aspose.CAD?

 A2: Ja, Sie können eine kostenlose Testversion herunterladen von[Hier](https://releases.aspose.com/).

### F3: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

 A3: Sie können eine temporäre Lizenz erwerben bei[Hier](https://purchase.aspose.com/temporary-license/).

### F4: Wo finde ich zusätzliche Unterstützung für Aspose.CAD?

 A4: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F5: Kann ich die Exportoptionen für verschiedene Bildformate anpassen?

A5: Auf jeden Fall! Aspose.CAD bietet eine Reihe von Optionen zur Anpassung, sodass Sie den Exportvorgang an Ihre spezifischen Anforderungen anpassen können.