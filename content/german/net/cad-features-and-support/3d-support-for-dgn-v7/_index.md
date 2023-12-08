---
title: 3D-Unterstützung für DGN V7 in Aspose.CAD für .NET
linktitle: 3D-Unterstützung für DGN V7
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die Leistungsfähigkeit der 3D-Unterstützung für DGN V7-Dateien in Aspose.CAD für .NET. Befolgen Sie unsere Schritt-für-Schritt-Anleitung, um CAD-Dateien mühelos zu integrieren und zu bearbeiten.
type: docs
weight: 10
url: /de/net/cad-features-and-support/3d-support-for-dgn-v7/
---
## Einführung

In der dynamischen Welt der Softwareentwicklung ist die Fähigkeit zur nahtlosen Integration und Bearbeitung von 3D-Daten von entscheidender Bedeutung. Aspose.CAD für .NET bietet Entwicklern eine Reihe robuster Tools für den effizienten Umgang mit CAD-Dateien. In diesem Tutorial befassen wir uns mit den Feinheiten der Aktivierung der 3D-Unterstützung für DGN V7-Dateien mithilfe von Aspose.CAD für .NET.

## Voraussetzungen

Stellen Sie vor Beginn dieser Reise sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass die Bibliothek installiert ist. Sie können es hier herunterladen[Aspose.CAD für .NET-Downloadseite](https://releases.aspose.com/cad/net/).

- Gültige DGN-Datei: Bereiten Sie eine gültige DGN-Datei vor, die Sie mithilfe des bereitgestellten Codeausschnitts verarbeiten möchten. Sie können Ihr eigenes verwenden oder zu Testzwecken eines herunterladen.

- .NET-Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein, um den bereitgestellten Code auszuführen. Wenn Sie noch keines haben, können Sie den Installationsanweisungen auf der folgen[.NET-Dokumentation](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr .NET-Projekt:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Lassen Sie uns nun den bereitgestellten Codeausschnitt in eine Schritt-für-Schritt-Anleitung aufschlüsseln.

## Schritt 1: Richten Sie die Umgebung ein

Definieren Sie Ihr Dokumentverzeichnis und den Pfad zur DGN-Datei:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

## Schritt 2: Laden Sie die DGN-Datei

 Laden Sie die DGN-Datei als`DgnImage` mit Aspose.CAD`Image.Load` Methode:

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Codeausschnitt wird fortgesetzt...
}
```

## Schritt 3: Exportoptionen konfigurieren

Richten Sie die Exportoptionen ein und geben Sie die Einstellungen für die Vektorrasterung an:

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Exportieren Sie bestimmte Ansichten
    }
};
```

## Schritt 4: Speichern Sie das Ergebnis

 Nutzen Sie die`Save` Methode zum Exportieren der DGN-Datei in ein Rasterbild:

```csharp
string outFile = "Your Output Directory"; // Geben Sie das Ausgabeverzeichnis an
dgnImage.Save(outFile, options);
```

## Abschluss

Glückwunsch! Sie haben die 3D-Unterstützung für DGN V7-Dateien mit Aspose.CAD für .NET erfolgreich aktiviert. Dieses Tutorial bietet eine klare Roadmap, die Sie durch jeden Schritt führt, um eine reibungslose Implementierung sicherzustellen.

## FAQs

### F1: Kann ich mit diesem Ansatz mehrere DGN-Dateien gleichzeitig verarbeiten?

A1: Ja, Sie können den Code ändern, um mehrere Dateien innerhalb einer Schleife oder als Teil eines Stapelverarbeitungssystems zu verarbeiten.

### F2: Welche anderen Exportformate werden von Aspose.CAD für .NET unterstützt?

 A2: Aspose.CAD für .NET unterstützt verschiedene Exportformate, darunter PDF, PNG, JPG und mehr. Siehe die[Dokumentation](https://reference.aspose.com/cad/net/) für Details.

### F3: Ist Aspose.CAD für .NET mit den neuesten .NET Core-Versionen kompatibel?

A3: Ja, Aspose.CAD für .NET ist so konzipiert, dass es mit den neuesten .NET Core-Versionen kompatibel ist. Stellen Sie sicher, dass in Ihrer Umgebung die entsprechende Version installiert ist.

### F4: Kann ich die Exporteinstellungen weiter an meine spezifischen Anforderungen anpassen?

 A4: Auf jeden Fall! Der bereitgestellte Code bietet einen Ausgangspunkt. Weitere Optionen und Konfigurationen finden Sie im[Aspose.CAD-Dokumentation](https://reference.aspose.com/cad/net/).

### F5: Wo kann ich Hilfe suchen oder meine Erfahrungen mit Aspose.CAD für .NET teilen?

A5: Treten Sie der Aspose.CAD-Community bei[Forum](https://forum.aspose.com/c/cad/19) um mit anderen Entwicklern zu interagieren und Unterstützung zu suchen.