---
date: 2026-03-29
description: Erfahren Sie, wie Sie CAD‑Rasterisierungsoptionen konfigurieren und DGN
  mit 3D‑Unterstützung in PDF exportieren, indem Sie Aspose.CAD für .NET verwenden.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD‑Rasterisierungsoptionen für DGN V7 3D konfigurieren
url: /de/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD-Rasterisierungsoptionen für DGN V7 3D konfigurieren

## Einführung

In diesem umfassenden Tutorial lernen Sie **wie Sie CAD-Rasterisierungsoptionen konfigurieren** um eine 3‑D DGN V7-Datei mit Aspose.CAD für .NET in PDF zu exportieren. Egal, ob Sie einen CAD‑Viewer, ein Reporting‑Tool oder eine automatisierte Konvertierungspipeline erstellen, das Beherrschen dieser Einstellungen gibt Ihnen präzise Kontrolle über Seitengröße, Layout‑Skalierung, Hintergrundfarben und die spezifischen Ansichten, die Sie rendern möchten. Lassen Sie uns den Prozess Schritt für Schritt durchgehen.

## Schnelle Antworten
- **Was bedeutet „configure CAD rasterization options“?**  
  Es bezieht sich auf das Festlegen von Eigenschaften wie Seitendimensionen, Skalierung, Hintergrundfarbe und Layoutauswahl, bevor eine CAD‑Datei in ein Rasterformat (z. B. PDF) konvertiert wird.
- **Wie exportiere ich DGN mit 3‑D‑Unterstützung nach PDF?**  
  Laden Sie das DGN mit `DgnImage`, definieren Sie `PdfOptions` + `CadRasterizationOptions` und rufen Sie anschließend `Save` auf.
- **Benötige ich eine Lizenz für den Produktionseinsatz?**  
  Ja – eine kommerzielle Lizenz ist für die Bereitstellung erforderlich; ein kostenloser Testzeitraum ist verfügbar.
- **Welche .NET‑Versionen werden unterstützt?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Kann ich bestimmte Ansichten zum Export auswählen?**  
  Absolut – setzen Sie das `Layouts`‑Array in den Rasterisierungsoptionen.

## Was bedeutet „configure CAD rasterization options“?

Das Konfigurieren von CAD‑Rasterisierungsoptionen bedeutet, anzupassen, wie eine CAD‑Zeichnung rasterisiert wird (von Vektor in Bitmap oder PDF umgewandelt). Durch das Anpassen dieser Einstellungen steuern Sie die visuelle Ausgabe, die Leistung und die Dateigröße des resultierenden Dokuments.

## Warum Aspose.CAD für den 3‑D DGN V7‑Export verwenden?

- **Vollständige .NET‑Integration** – keine COM‑ oder nativen DLLs erforderlich.  
- **Unterstützt 3‑D‑Geometrie** – behält Tiefeninformationen beim Rendern nach PDF bei.  
- **Fein abgestimmte Kontrolle** – wählen Sie exakte Layouts, Skalierung und Hintergrundfarben.  
- **Plattformübergreifend** – funktioniert unter Windows, Linux und macOS mit .NET Core.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD for .NET** – laden Sie es von [hier](https://releases.aspose.com/cad/net/) herunter.  
- **Visual Studio** oder ein kompatibles .NET‑IDE.  
- **Eine Beispiel‑DGN‑Datei** – für diese Anleitung verwenden wir `Nikon_D90_Camera.dgn` (im Aspose‑Beispielpaket enthalten).  

Jetzt, da alles bereit ist, tauchen wir in den Code ein.

## Namespaces importieren

In Ihrem .NET‑Projekt importieren Sie die erforderlichen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: Dokumentverzeichnis einrichten

Erstellen Sie eine Variable, die auf den Ordner verweist, in dem Ihre Quell‑DGN‑Datei und die Ausgabedateien gespeichert werden.

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: DGN‑Datei laden

Laden Sie die DGN‑Datei als `DgnImage`. Dieses Objekt gibt Ihnen Zugriff auf die CAD‑Daten und die Rasterisierungspipeline.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Schritt 3: PDF‑Exportoptionen konfigurieren (CAD‑Rasterisierungsoptionen konfigurieren)

Hier **konfigurieren wir CAD‑Rasterisierungsoptionen**, die bestimmen, wie das 3‑D‑Modell nach PDF gerendert wird. Sie können die Seitengröße anpassen, die automatische Layout‑Skalierung aktivieren, eine Hintergrundfarbe festlegen und die genauen Layouts (Ansichten) auswählen, die Sie exportieren möchten.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Schritt 4: Rasterbild speichern

Abschließend exportieren Sie das DGN mit den gerade konfigurierten Optionen in eine PDF‑Datei.

```csharp
dgnImage.Save(outFile, options);
```

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Leere PDF‑Ausgabe** | Stellen Sie sicher, dass das `Layouts`‑Array die korrekten Ansicht‑Bezeichner enthält, die in der DGN‑Datei vorhanden sind. |
| **Falsche Farben** | Vergewissern Sie sich, dass `BackgroundColor` auf den gewünschten Wert gesetzt ist; verwenden Sie `Color.White` für einen hellen Hintergrund. |
| **Leistungsengpass bei großen Dateien** | Aktivieren Sie `AutomaticLayoutsScaling` und erwägen Sie, `PageWidth/PageHeight` zu reduzieren, um eine kleinere Rasterauflösung zu erhalten. |
| **Lizenzausnahme** | Installieren Sie eine gültige Aspose.CAD‑Lizenz, bevor Sie das Bild laden, um Wasserzeichen der Testversion zu vermeiden. |

## Häufig gestellte Fragen

**F: Kann ich Aspose.CAD für .NET mit anderen CAD‑Dateiformaten verwenden?**  
A: Ja, Aspose.CAD unterstützt DWG, DXF, DWF, DGN und viele weitere Formate.

**F: Wie kann ich Ausnahmen beim Arbeiten mit Aspose.CAD behandeln?**  
A: Umgeben Sie Ihren Code mit einem `try‑catch`‑Block und prüfen Sie `Aspose.CAD.CADException` für detaillierte Fehlerinformationen.

**F: Ist Aspose.CAD für kommerzielle Projekte geeignet?**  
A: Absolut. Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben.

**F: Kann ich Aspose.CAD für .NET vor dem Kauf testen?**  
A: Ja, ein kostenloser Testzeitraum ist [hier](https://releases.aspose.com/) verfügbar.

**F: Wo finde ich Community‑Support für Aspose.CAD?**  
A: Treten Sie dem Diskussionsforum [hier](https://forum.aspose.com/c/cad/19) bei.

---

**Zuletzt aktualisiert:** 2026-03-29  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}