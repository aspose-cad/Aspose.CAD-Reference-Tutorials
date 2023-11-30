---
title: Anpassen der CAD-Zeichnungsgröße in Aspose.CAD für .NET
linktitle: Anpassen der CAD-Zeichnungsgröße
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie mit Aspose.CAD mühelos CAD-Zeichnungsgrößen in .NET anpassen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Größenänderung.
type: docs
weight: 10
url: /de/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Einführung

Möchten Sie die Größe von CAD-Zeichnungen in Ihren .NET-Anwendungen nahtlos anpassen? Aspose.CAD für .NET bietet eine robuste Lösung, mit der Sie die Größenänderung von CAD-Zeichnungen mühelos durchführen können. In diesem Tutorial führen wir Sie durch den Prozess und schlüsseln jeden Schritt auf, um sicherzustellen, dass Sie die Feinheiten der Größenänderung von CAD-Zeichnungen mit Aspose.CAD verstehen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.CAD für .NET-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.CAD für .NET-Downloadseite](https://releases.aspose.com/cad/net/).
- Beispiel-CAD-Zeichnung: Stellen Sie sicher, dass Sie eine Beispiel-CAD-Zeichnungsdatei (z. B. „sample.dwg“) in Ihrem Dokumentverzeichnis haben.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihre .NET-Anwendung. Dieser Schritt ist entscheidend für den Zugriff auf die von Aspose.CAD für .NET bereitgestellten Funktionen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: CAD-Zeichnung laden

Laden Sie zunächst die CAD-Zeichnung in eine Instanz der Aspose.CAD.Image-Klasse. Stellen Sie sicher, dass Sie den richtigen Dateipfad für Ihre Beispielzeichnung haben.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Laden Sie eine CAD-Zeichnung in eine Instanz von Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Ihr Code hier...
}
```

## Schritt 2: Erstellen Sie BmpOptions

Erstellen Sie eine Instanz der BmpOptions-Klasse, die für die Angabe von Optionen beim Speichern der CAD-Zeichnung als BMP-Datei verantwortlich ist.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Schritt 3: CadRasterizationOptions festlegen

Instanziieren Sie die CadRasterizationOptions-Klasse und konfigurieren Sie ihre Eigenschaften für die Vektorrasterung.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Schritt 4: Legen Sie die UnitType-Eigenschaft fest

Legen Sie die UnitType-Eigenschaft von CadRasterizationOptions fest, um den Einheitentyp für die Größenänderung anzugeben. In diesem Beispiel ist es auf Zentimeter eingestellt.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Schritt 5: Legen Sie die Layouts-Eigenschaft fest

Geben Sie die Layouts an, die Sie in die Zeichnung mit geänderter Größe einbeziehen möchten, indem Sie die Eigenschaft „Layouts“ festlegen.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Schritt 6: Export nach BMP

Speichern Sie abschließend das geänderte Layout mit der Save-Methode als BMP-Datei.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Jetzt haben Sie die Größe Ihrer CAD-Zeichnung mit Aspose.CAD für .NET erfolgreich angepasst!

## Abschluss

In diesem Tutorial haben wir den Prozess der Größenänderung von CAD-Zeichnungen in .NET mithilfe von Aspose.CAD durchlaufen. Wenn Sie diese Schritte befolgen, können Sie diese Funktionalität nahtlos in Ihre Anwendungen integrieren und so für ein reibungsloses Benutzererlebnis sorgen.

## FAQs

### F1: Ist Aspose.CAD für .NET mit allen CAD-Formaten kompatibel?

 A1: Aspose.CAD für .NET unterstützt eine Vielzahl von CAD-Formaten, einschließlich DWG, DXF, DWF und mehr. Überprüf den[Dokumentation](https://reference.aspose.com/cad/net/) für die vollständige Liste.

### F2: Kann ich die Größe mehrerer Layouts gleichzeitig ändern?

A2: Ja, Sie können die Größe mehrerer Layouts ändern, indem Sie das Layout-Array in den CadRasterizationOptions anpassen.

### F3: Wo erhalte ich Unterstützung für Aspose.CAD für .NET?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung und Unterstützung der Gemeinschaft.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können a erkunden[Kostenlose Testphase](https://releases.aspose.com/) um die Funktionen von Aspose.CAD für .NET zu bewerten.

### F5: Wie kann ich eine temporäre Lizenz für Aspose.CAD für .NET erhalten?

 A5: Besorgen Sie sich zu Testzwecken eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).