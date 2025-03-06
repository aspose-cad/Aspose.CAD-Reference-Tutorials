---
title: Unterstützung für DGN V7 in Aspose.CAD für .NET
linktitle: Unterstützung für DGN V7
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die nahtlose Unterstützung von Aspose.CAD für .NET für DGN V7. Konvertieren Sie DGN-Dateien mühelos mit der Schritt-für-Schritt-Anleitung in Rasterbilder.
weight: 19
url: /de/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterstützung für DGN V7 in Aspose.CAD für .NET

## Einführung

Im Bereich der .NET-Entwicklung zeichnet sich Aspose.CAD als leistungsstarke Bibliothek für die Verarbeitung von CAD-Dateien (Computer-Aided Design) aus. Dieses Tutorial befasst sich mit einer spezifischen Funktion von Aspose.CAD für .NET – der Unterstützung für DGN V7-Dateien. DGN, die Abkürzung für Design, ist ein weit verbreitetes Dateiformat im CAD-Bereich. Aspose.CAD vereinfacht die Arbeit mit DGN V7-Dateien und bietet Entwicklern ein nahtloses Erlebnis.

## Voraussetzungen

Bevor wir uns mit der Implementierung befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass die Aspose.CAD-Bibliothek installiert ist. Sie können es hier herunterladen[Webseite](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Richten Sie eine funktionierende .NET-Entwicklungsumgebung ein, einschließlich Visual Studio oder einer anderen bevorzugten IDE.

Nachdem wir nun die Voraussetzungen geklärt haben, wollen wir untersuchen, wie wir die Unterstützung für DGN V7 in Aspose.CAD für .NET nutzen können.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces, um auf die Funktionalität von Aspose.CAD zuzugreifen:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DGN-Datei laden

 Beginnen Sie mit dem Laden einer vorhandenen DGN-Datei als`CadImage` Ersetzen`"Your Document Directory"` Und`"Nikon_D90_Camera.dgn"` mit dem entsprechenden Verzeichnispfad und Dateinamen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Code für weitere Schritte finden Sie hier...
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

 Ein ... kreieren`CadRasterizationOptions` Objekt zum Definieren und Festlegen verschiedener Eigenschaften im Zusammenhang mit der Rasterung.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Schritt 3: Legen Sie die Optionen für die Vektorrasterung fest

 Ein ... kreieren`JpegOptions` Objekt, da wir beabsichtigen, die DGN-Datei in JPEG zu konvertieren. Weisen Sie das zuvor erstellte zu`CadRasterizationOptions` Einspruch dagegen erheben.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Schritt 4: Speichern Sie das gerasterte Bild

 Ruf den`Save` Methode der`CadImage` Klassenobjekt zum Exportieren der DGN-Datei in ein Rasterbild, in diesem Fall ein JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Nachdem diese Schritte abgeschlossen sind, wurde die DGN-Datei erfolgreich in ein Rasterbild exportiert.

## Abschluss

In diesem Tutorial haben wir die nahtlose Unterstützung für DGN V7 in Aspose.CAD für .NET untersucht. Durch Befolgen der Schritt-für-Schritt-Anleitung können Entwickler DGN-Dateien mühelos in Rasterbilder konvertieren und so die Funktionen ihrer .NET-Anwendungen erweitern.

## FAQs

### F1: Ist Aspose.CAD mit den neuesten DGN V7-Spezifikationen kompatibel?

A1: Ja, Aspose.CAD ist für die nahtlose Verarbeitung von DGN V7-Dateien konzipiert und gewährleistet die Kompatibilität mit den neuesten Spezifikationen.

### F2: Kann ich die Rasterungsoptionen für die DGN-Dateikonvertierung anpassen?

 A2: Absolut. Das Tutorial zeigt, wie man erstellt und konfiguriert`CadRasterizationOptions` um den Konvertierungsprozess anzupassen.

### F3: Gibt es neben JPEG noch andere unterstützte Ausgabeformate?

A3: Ja, Aspose.CAD unterstützt verschiedene Ausgabeformate. Eine umfassende Liste finden Sie in der Dokumentation.

### F4: Wie kann ich Unterstützung für Aspose.CAD-bezogene Anfragen erhalten?

 A4: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F5: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?

 A5: Ja, Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
