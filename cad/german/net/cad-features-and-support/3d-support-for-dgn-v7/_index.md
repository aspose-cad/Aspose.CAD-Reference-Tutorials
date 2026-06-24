---
date: 2026-03-24
description: Erfahren Sie, wie Sie DGN mit 3D‑Unterstützung für DGN V7 mithilfe von
  Aspose.CAD für .NET in PDF (und PNG) konvertieren – Schritt‑für‑Schritt‑Anleitung.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN in PDF konvertieren (3D‑Unterstützung) mit Aspose.CAD für .NET
url: /de/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN in PDF konvertieren (3D-Unterstützung) mit Aspose.CAD für .NET

## Einleitung

In modernen CAD‑Workflows ist es unerlässlich, **DGN in PDF** schnell konvertieren zu können und dabei 3‑D‑Geometrie beizubehalten. Egal, ob Sie Dokumentationen erstellen, Entwürfe mit Nicht‑CAD‑Stakeholdern teilen oder Projekte archivieren, Aspose.CAD für .NET bietet Ihnen eine zuverlässige Möglichkeit, DGN‑V7‑Dateien in hochwertige PDF‑ (und sogar PNG‑)Ausgaben zu verwandeln. In diesem Tutorial führen wir Sie durch die genauen Schritte, die erforderlich sind, um die 3D‑Unterstützung zu aktivieren und ein PDF aus einer DGN‑Datei zu erzeugen.

## Schnelle Antworten
- **Was behandelt das Tutorial?** Aktivierung der 3D‑Unterstützung und Konvertierung von DGN V7 zu PDF mit Aspose.CAD für .NET.  
- **Welches primäre Format wird erzeugt?** PDF (mit optionalem PNG‑Export).  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Unterstützte .NET‑Versionen?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für eine grundlegende Konvertierung.

## Was bedeutet „convert DGN to PDF“?

Die Konvertierung von DGN zu PDF bedeutet, die Vektordaten, die in einer MicroStation‑DGN‑Datei gespeichert sind, in ein portables Dokumentformat zu rendern, das auf jedem Gerät ohne spezielle CAD‑Software angezeigt werden kann. Mit dem 3‑D‑Rasterisierungs‑Engine von Aspose.CAD bewahrt die Konvertierung Layout, Farben und Tiefenhinweise und liefert eine getreue visuelle Darstellung.

## Warum Aspose.CAD für diese Konvertierung verwenden?

- **Vollständige 3‑D‑Rasterisierung** – bewahrt Tiefe und Layout‑Informationen.  
- **Keine externen Abhängigkeiten** – reine .NET‑Bibliothek, kein MicroStation erforderlich.  
- **Mehrere Ausgabeformate** – PDF, PNG, JPEG, TIFF usw. (das sekundäre Schlüsselwort *convert dgn to png* wird sofort unterstützt).  
- **Plattformübergreifend** – funktioniert unter Windows, Linux und macOS.

## Voraussetzungen

Stellen Sie vor dem Start sicher, dass Sie Folgendes haben:

- Aspose.CAD für .NET installiert. Sie können es von der [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) herunterladen.  
- Eine gültige DGN‑V7‑Datei, die Sie verarbeiten möchten.  
- Eine .NET‑Entwicklungsumgebung (Visual Studio, VS Code oder die CLI). Installationsanleitungen finden Sie in der [.NET documentation](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Namespaces importieren

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Diese Namespaces geben Ihnen Zugriff auf die Kernklassen von Aspose.CAD und Standard‑.NET‑Hilfsprogramme.

## Schritt 1: Umgebung einrichten

Definieren Sie, wo sich Ihre Quell‑DGN‑Datei befindet und wo das Ausgabe‑PDF gespeichert werden soll.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Pro Tipp:** Verwenden Sie `Path.Combine` für plattformunabhängige Pfadkonstruktion.

## Schritt 2: DGN‑Datei laden

Erstellen Sie eine `DgnImage`‑Instanz, indem Sie die Datei mit `Image.Load` laden. Dieser Schritt bereitet die CAD‑Daten für die Rasterisierung vor.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Schritt 3: Exportoptionen konfigurieren

Richten Sie `PdfOptions` zusammen mit `CadRasterizationOptions` ein. Hier steuern Sie die Seitengröße, den Hintergrund und welche Layouts (Ansichten) exportiert werden.

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
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

Wenn Sie stattdessen **convert DGN to PNG** benötigen, ersetzen Sie einfach `PdfOptions` durch `PngOptions`, während Sie die gleichen Rasterisierungseinstellungen beibehalten.

## Schritt 4: Ergebnis speichern

Schreiben Sie schließlich die gerenderte Ausgabe an den gewünschten Ort.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

Nach der Ausführung finden Sie eine PDF‑Datei (oder PNG, wenn Sie die Optionen geändert haben), die die ursprüngliche 3‑D‑DGN‑Zeichnung getreu darstellt.

## Häufige Probleme & Tipps

- **Fehlende Layouts:** Stellen Sie sicher, dass die Layout‑Namen in `Layouts` mit denen in der DGN‑Datei übereinstimmen; andernfalls werden sie ignoriert.  
- **Große Dateien:** Erhöhen Sie `PageWidth`/`PageHeight` schrittweise, um hohen Speicherverbrauch zu vermeiden.  
- **Farbgenauigkeit:** Wenn der Hintergrund dunkel erscheint, prüfen Sie, ob `BackgroundColor` auf den gewünschten Wert gesetzt ist (z. B. `Color.White`).

## Fazit

Sie haben nun gelernt, wie man **DGN in PDF** mit voller 3‑D‑Unterstützung mithilfe von Aspose.CAD für .NET konvertiert. Dieser Workflow kann in automatisierte Pipelines, Desktop‑Dienstprogramme oder Web‑Services integriert werden, um CAD‑Visualisierungen jedem Publikum bereitzustellen.

## FAQ

### Q1: Kann ich mehrere DGN‑Dateien gleichzeitig mit diesem Ansatz verarbeiten?

A1: Ja, Sie können den Code anpassen, um mehrere Dateien in einer Schleife oder als Teil eines Batch‑Verarbeitungssystems zu verarbeiten.

### Q2: Welche anderen Exportformate werden von Aspose.CAD für .NET unterstützt?

A2: Aspose.CAD für .NET unterstützt verschiedene Exportformate, darunter PDF, PNG, JPG und mehr. Weitere Details finden Sie in der [documentation](https://reference.aspose.com/cad/net/).

### Q3: Ist Aspose.CAD für .NET mit den neuesten .NET‑Core‑Versionen kompatibel?

A3: Ja, Aspose.CAD für .NET ist so konzipiert, dass es mit den neuesten .NET‑Core‑Versionen kompatibel ist. Stellen Sie sicher, dass die passende Version in Ihrer Umgebung installiert ist.

### Q4: Kann ich die Export‑Einstellungen weiter an meine spezifischen Anforderungen anpassen?

A4: Absolut! Der bereitgestellte Code bietet einen Ausgangspunkt. Sie können weitere Optionen und Konfigurationen in der [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) erkunden.

### Q5: Wo kann ich Hilfe erhalten oder meine Erfahrungen mit Aspose.CAD für .NET teilen?

A5: Treten Sie der Aspose.CAD‑Community im [forum](https://forum.aspose.com/c/cad/19) bei, um mit anderen Entwicklern zu interagieren und Unterstützung zu erhalten.

---

**Zuletzt aktualisiert:** 2026-03-24  
**Getestet mit:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}