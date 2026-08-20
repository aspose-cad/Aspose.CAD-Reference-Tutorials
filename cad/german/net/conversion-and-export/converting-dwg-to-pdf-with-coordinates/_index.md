---
date: 2026-04-03
description: Erfahren Sie, wie Sie das Ansichtsfenster festlegen und DWG in PDF in
  C# mit Aspose.CAD konvertieren. Dieses DWG‑zu‑PDF‑Tutorial zeigt einen präzisen
  Export mit Koordinaten.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: DWG in PDF mit Koordinaten in C# konvertieren
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Wie man das Ansichtsfenster beim Konvertieren von DWG zu PDF mit Koordinaten
  in C# festlegt – Aspose.CAD‑Tutorial
url: /de/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG in PDF mit Koordinaten in C# konvertieren – Aspose.CAD‑Tutorial

## Einleitung

Willkommen zu diesem umfassenden Tutorial zum **Setzen des Viewports**, während Sie DWG‑Dateien mit angegebenen Koordinaten in PDF konvertieren, unter Verwendung von Aspose.CAD für .NET. Durch die Steuerung des Viewports erhalten Sie pixelgenaue PDFs, die exakt den benötigten Bereich wiedergeben – ideal für Baudokumentationen, Grundriss‑Vorschauen oder jeden BIM‑Workflow.

## Schnelle Antworten
- **Was bedeutet „set viewport“?** Es definiert den sichtbaren Bereich und die Skalierung der CAD‑Zeichnung während der Rasterisierung.  
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.CAD für .NET.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Unterstützte Plattformen?** Windows, Linux und macOS mit .NET 5/6/7 oder .NET Framework 4.6+.  
- **Typische Implementierungsdauer?** Etwa 10‑15 Minuten für eine grundlegende Konvertierung.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- **Aspose.CAD‑Bibliothek** – Laden Sie die Aspose.CAD‑Bibliothek für .NET herunter und installieren Sie sie. Die Bibliothek finden Sie [hier](https://releases.aspose.com/cad/net/).
- **Entwicklungsumgebung** – Visual Studio, Rider oder jede IDE, die .NET‑Entwicklung unterstützt.
- **DWG‑Datei** – Haben Sie eine DWG‑Datei bereit für die Konvertierung. Sie können die bereitgestellte Beispieldatei oder Ihre eigene DWG‑Datei verwenden.

## So setzen Sie das Viewport für präzisen PDF‑Export

Das Setzen des Viewports ist der zentrale Schritt, der es Ihnen ermöglicht, den genauen Bereich der Zeichnung zu definieren, den Sie rendern möchten. Im nachfolgenden Code erstellen wir ein neues `CadVportTableObject`, positionieren es mit der oberen linken Koordinate und berechnen Breite, Höhe sowie das Seitenverhältnis. Dies ist die **how to set viewport**‑Implementierung, die den Rest der Konvertierung steuert.

## Namespaces importieren

Importieren Sie in Ihrem C#‑Projekt die erforderlichen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Lassen Sie uns den Code Schritt für Schritt aufschlüsseln, um ein besseres Verständnis zu erhalten:

## Schritt 1: Dokumentverzeichnis festlegen

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: Quell‑DWG‑Dateipfad festlegen

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Schritt 3: DWG‑Datei laden und Rasterisierungsoptionen konfigurieren

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Schritt 4: Koordinaten und Viewport definieren  

Hier setzen wir tatsächlich **den Viewport** (how to set viewport), indem wir die obere linke Ecke, Breite und Höhe des zu exportierenden Bereichs angeben.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Schritt 5: Viewport‑Einstellungen anwenden

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Schritt 6: PDF‑Optionen konfigurieren und exportieren  

Jetzt fügen wir alles zusammen und **konvertieren DWG zu PDF** mithilfe der gerade vorbereiteten Rasterisierungsoptionen.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Schritt 7: Erfolgsmeldung anzeigen

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Häufige Anwendungsfälle

- **Bau‑Dokumentation** – Erzeugen Sie druckbare PDFs bestimmter Grundriss‑Abschnitte.  
- **BIM‑Koordination** – Exportieren Sie nur den interessierenden Bereich für die Kollisionserkennung.  
- **Kundenpräsentationen** – Stellen Sie ein sauberes PDF eines ausgewählten Raums oder einer Ansicht bereit, ohne die gesamte Zeichnung offenzulegen.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **DWG zu PDF** mit genauen Koordinaten konvertiert und gelernt, **wie man den Viewport setzt** mit Aspose.CAD für .NET. Dieses **dwg to pdf tutorial** zeigt, wie man **pdf aus dwg erstellt** und **dwg als pdf c# exportiert**, wobei Sie die volle Kontrolle über den Ausgabebereich behalten.

## FAQ

### Q1: Kann ich Aspose.CAD mit anderen CAD‑Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF, DWF und weitere.

### Q2: Wie kann ich Fehler während des Konvertierungsprozesses behandeln?

A2: Implementieren Sie Fehlerbehandlungsmechanismen mit try‑catch‑Blöcken, um Ausnahmen abzufangen und zu verwalten.

### Q3: Ist Aspose.CAD für sowohl Windows‑ als auch Linux‑Umgebungen geeignet?

A3: Ja, Aspose.CAD ist mit sowohl Windows‑ als auch Linux‑Plattformen kompatibel.

### Q4: Kann ich die PDF‑Ausgabe weiter anpassen?

A4: Natürlich! Erkunden Sie die umfangreichen Optionen von Aspose.CAD, um die PDF‑Ausgabe an Ihre spezifischen Anforderungen anzupassen.

### Q5: Wo finde ich zusätzliche Unterstützung oder Community‑Diskussionen?

A5: Besuchen Sie das [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

## Zusätzliche häufig gestellte Fragen

**Q: Funktioniert dieser Ansatz mit großen DWG‑Dateien (hunderten MB)?**  
A: Ja. Die Rasterisierung wird seitenweise durchgeführt, und Sie können `rasterizationOptions` (z. B. `Resolution`) anpassen, um Qualität und Speicherverbrauch auszubalancieren.

**Q: Kann ich mehrere Viewports in separate PDF‑Seiten exportieren?**  
A: Sie können über `cadImage.ViewPorts` iterieren, jeden als aktiv setzen und `Save` für jede Seite aufrufen, anschließend PDFs mit Aspose.PDF zusammenführen.

**Q: Ist es möglich, dem erzeugten PDF ein Wasserzeichen hinzuzufügen?**  
A: Nach dem Speichern des PDFs können Sie es mit Aspose.PDF erneut öffnen und ein Text‑ oder Bildwasserzeichen hinzufügen, bevor Sie es dem Benutzer bereitstellen.

**Zuletzt aktualisiert:** 2026-04-03  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}