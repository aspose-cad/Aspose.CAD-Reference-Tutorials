---
date: 2026-03-29
description: Erfahren Sie, wie Sie DGN mit Aspose.CAD für .NET in JPEG konvertieren,
  wobei vollständige Unterstützung für DGN V7 bereitgestellt wird und Sie CAD einfach
  in Rasterbilder umwandeln können.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN in JPEG konvertieren mit Aspose.CAD für .NET – V7‑Unterstützung
url: /de/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN in JPEG konvertieren mit Aspose.CAD für .NET – V7-Unterstützung

## Einführung

In diesem Tutorial lernen Sie, wie Sie **DGN in JPEG** mit Aspose.CAD für .NET konvertieren, wobei Sie die vollständige DGN V7‑Unterstützung der Bibliothek nutzen. Das Konvertieren von DGN‑Dateien in Rasterbilder wie JPEG ist ein häufiges Bedürfnis, wenn Sie CAD‑Zeichnungen in Webseiten, mobile Apps oder Reporting‑Tools einbetten müssen. Aspose.CAD ermöglicht Ihnen zudem, **CAD in Raster**‑Formate effizient zu konvertieren, was Ihnen Flexibilität bei der Darstellung von Designdaten gibt.

## Schnelle Antworten
- **Worum geht es im Tutorial?** Konvertierung einer DGN V7‑Datei in ein JPEG‑Rasterbild mit Aspose.CAD für .NET.  
- **Welche Bibliotheksversion wird benötigt?** Jede aktuelle Aspose.CAD‑Version für .NET, die DGN V7‑Unterstützung enthält.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Entwicklung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich die Ausgabengröße ändern?** Ja – Rasterisierungsoptionen ermöglichen das Festlegen von Seitenbreite, -höhe und Skalierung.  
- **Ist JPEG das einzige Ausgabeformat?** Nein – Aspose.CAD unterstützt viele Rasterformate (PNG, BMP, TIFF usw.).

## Was ist DGN V7?
DGN (Design) ist ein Dateiformat, das ursprünglich von Bentley Systems für MicroStation entwickelt wurde. Version 7 fügt umfangreichere Geometrie und Metadaten hinzu und ist daher eine beliebte Wahl für Bau‑ und Infrastrukturprojekte. Aspose.CAD für .NET kann DGN V7‑Dateien direkt lesen und deren Inhalt als `CadImage`‑Objekte bereitstellen, die Sie rasterisieren oder in andere Formate konvertieren können.

## Warum DGN in JPEG konvertieren?
- **Web‑tauglich:** JPEG‑Bilder sind leichtgewichtig und werden sofort in Browsern angezeigt, ohne dass spezielle Plugins erforderlich sind.  
- **Plattformübergreifend:** JPEG kann auf jedem Gerät angezeigt werden, was es ideal macht, CAD‑Zeichnungen mit nicht‑technischen Stakeholdern zu teilen.  
- **Vereinfachte Arbeitsabläufe:** Die Konvertierung in ein Rasterformat eliminiert die Notwendigkeit von CAD‑spezifischen Betrachtern in nachgelagerten Prozessen.

## Voraussetzungen

Bevor wir mit der Implementierung beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD für .NET** – laden Sie es von der [Website](https://releases.aspose.com/cad/net/) herunter.  
- **Entwicklungsumgebung** – Visual Studio (oder jede IDE, die .NET unterstützt).  

Wenn Sie diese bereit haben, können Sie die Schritte ohne Unterbrechungen durchführen.

## Namespaces importieren

Beginnen Sie damit, die für die Verarbeitung von CadImage und die Rasterisierung erforderlichen Namespaces zu importieren.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DGN‑Datei laden

Laden Sie die Quell‑DGN‑Datei in ein `CadImage`‑Objekt. Ersetzen Sie den Platzhalterpfad durch den Ordner, der Ihre DGN‑Datei enthält.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

Definieren Sie, wie die DGN‑Zeichnung rasterisiert werden soll. Sie können die Ausgabedimensionen und das Skalierungsverhalten steuern.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Schritt 3: Vektor‑Rasterisierungsoptionen festlegen

Erstellen Sie ein `JpegOptions`‑Objekt (oder Optionen für ein anderes Rasterformat) und fügen Sie die Rasterisierungseinstellungen hinzu.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Schritt 4: Rasterisiertes Bild speichern

Exportieren Sie schließlich die DGN‑Zeichnung mit der `Save`‑Methode in eine JPEG‑Datei.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Wenn der Code erfolgreich ausgeführt wird, finden Sie im angegebenen Ordner eine JPEG‑Darstellung der ursprünglichen DGN V7‑Zeichnung.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Datei nicht gefunden** | Stellen Sie sicher, dass `MyDir` mit einem Pfadtrennzeichen (`\\` oder `/`) endet und der Dateiname korrekt ist. |
| **Leeres Ausgabebild** | Stellen Sie sicher, dass `NoScaling` korrekt gesetzt ist; setzen Sie es auf `false`, wenn die Zeichnung die Seite ausfüllen soll. |
| **Nicht unterstützte Entitäten** | Aspose.CAD unterstützt die meisten DGN‑Entitäten, aber sehr alte oder benutzerdefinierte Objekte können ignoriert werden. Prüfen Sie das Konvertierungsprotokoll auf Warnungen. |

## Häufig gestellte Fragen

### Q1: Ist Aspose.CAD mit den neuesten DGN V7‑Spezifikationen kompatibel?
**A:** Ja, Aspose.CAD unterstützt DGN V7 vollständig und verarbeitet sowohl Geometrie als auch Metadaten gemäß den neuesten Standards.

### Q2: Kann ich die Rasterisierungsoptionen für die DGN‑Dateikonvertierung anpassen?
**A:** Absolut. Die Klasse `CadRasterizationOptions` ermöglicht das Anpassen von Seitengröße, Skalierung, Linienstärke, Hintergrundfarbe und mehr.

### Q3: Gibt es neben JPEG weitere unterstützte Ausgabeformate?
**A:** Ja, Aspose.CAD kann in PNG, BMP, TIFF und mehrere andere Rasterformate exportieren. Verwenden Sie einfach die entsprechende `*Options`‑Klasse (z. B. `PngOptions`).

### Q4: Wie kann ich Hilfe zu Aspose.CAD‑bezogenen Fragen erhalten?
**A:** Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und offizielle Antworten.

### Q5: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?
**A:** Ja, Sie können eine Testversion von [hier](https://releases.aspose.com/) herunterladen.

---

**Zuletzt aktualisiert:** 2026-03-29  
**Getestet mit:** Aspose.CAD 24.12 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}