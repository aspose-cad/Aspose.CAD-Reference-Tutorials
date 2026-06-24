---
date: 2026-03-16
description: Lernen Sie, wie Sie DWG mit Aspose.CAD für .NET in PDF oder Rasterbilder
  konvertieren. Dieses Schritt‑für‑Schritt‑CAD‑zu‑PDF‑Tutorial behandelt das Exportieren
  von DWG in Bildformate wie PNG und zeigt, wie Sie DWG effizient in Bilddateien exportieren.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Wie man DWG in PDF und Rasterbilder mit Aspose.CAD für .NET konvertiert
url: /de/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von DWG zu PDF oder Rasterbildern – Aspose.CAD Leitfaden

## Einführung

Wenn Sie **DWG zu PDF** (oder zu Rasterformaten wie PNG) direkt aus einer .NET‑Anwendung konvertieren müssen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie Schritt für Schritt durch die erforderlichen Vorgänge, um Aspose.CAD für .NET für die Konvertierung zu nutzen, erklären, warum die Bibliothek eine solide Wahl ist, und zeigen Ihnen, wie Sie sowohl PDF‑ als auch Bildausgaben mit nur wenigen Codezeilen handhaben können.

## Schnelle Antworten
- **Welche Bibliothek übernimmt die DWG‑Konvertierung?** Aspose.CAD for .NET  
- **Kann ich DWG sowohl nach PNG als auch nach PDF exportieren?** Ja – dieselben Rasterisierungsoptionen funktionieren für beide Formate.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert zum Testen; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Wird die Einheitenumrechnung automatisch durchgeführt?** Sie können das Einheitssystem manuell festlegen (metrisch oder imperial), wie im Code gezeigt.

## Was bedeutet „DWG zu PDF konvertieren“?
DWG zu PDF zu konvertieren bedeutet, eine CAD‑Zeichnung (DWG) zu rendern und in ein portables, nur‑lesbares Dokument (PDF) zu überführen. Das ist nützlich, um Designs mit Stakeholdern zu teilen, die keine CAD‑Software besitzen, druckbare Dokumentationen zu erstellen oder Zeichnungen in einem universell lesbaren Format zu archivieren.

## Warum Aspose.CAD für diese Konvertierung verwenden?
- **Keine externen Abhängigkeiten** – die Bibliothek arbeitet vollständig im verwalteten Code.  
- **Hohe Treue** – behält Ebenen, Linienstärken und Layout‑Informationen bei.  
- **Eingebaute Rasteroptionen** – ermöglichen den Export nach PNG, JPEG, BMP usw. mit einem einzigen Konfigurationsobjekt.  
- **Plattformübergreifend** – funktioniert unter Windows, Linux und macOS mit .NET Core.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass Sie Folgendes bereit haben:

- Grundlegendes Verständnis von .NET‑Programmierung.  
- Aspose.CAD for .NET Bibliothek installiert. Falls nicht, laden Sie sie [hier](https://releases.aspose.com/cad/net/) herunter.  
- Ihre bevorzugte integrierte Entwicklungsumgebung (IDE) für .NET‑Entwicklung eingerichtet.

## Namespaces importieren

Lassen Sie uns beginnen, indem wir die notwendigen Namespaces in Ihrem .NET‑Projekt importieren. Dadurch haben Sie Zugriff auf die Aspose.CAD‑Funktionalität in Ihrem Code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: DWG‑Datei laden

Laden Sie zunächst die DWG‑Datei, die Sie konvertieren möchten. Ersetzen Sie `"Your Document Directory"` durch den Pfad zu Ihrer DWG‑Datei.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Schritt 2: PDF‑Export einrichten (Wie man DWG zu PDF exportiert)

Jetzt konfigurieren wir die PDF‑Export‑Einstellungen. Dieses Beispiel zeigt, wie das Layout festgelegt und Einheitenumrechnungen gehandhabt werden.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Schritt 3: Export nach PDF

Führen Sie den Export nach PDF mit den konfigurierten Einstellungen aus.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Schritt 4: Export zu Rasterbildern (DWG zu Bild exportieren)

Erweitern Sie die Funktionalität, um zu Rasterbildern wie PNG zu exportieren.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Wie zu beheben |
|---------|-------------------|----------------|
| **Leere Seiten im PDF** | Layout nicht korrekt angegeben | Stellen Sie sicher, dass `rasterizationOptions.Layouts` den korrekten Layoutnamen enthält (z. B. `"Model"`). |
| **Falsche Abmessungen** | DPI- oder Seitengrößenabweichung | Passen Sie `PageHeight`, `PageWidth` und DPI‑Werte in `CadRasterizationOptions` an. |
| **Einheiten erscheinen falsch** | Einheitenumrechnung nicht definiert | Verwenden Sie `DefineUnitSystem`, um `currentUnitIsMetric` und `currentUnitCoefficient` basierend auf `cadImage.UnitType` festzulegen. |
| **Lizenzausnahme** | Einschränkungen der Testversion | Wenden Sie eine temporäre oder permanente Lizenz an, bevor Sie `Image.Load` aufrufen. |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für .NET in meinen kommerziellen Projekten verwenden?
A1: Ja, das können Sie. Besuchen Sie [purchase.aspose.com/buy](https://purchase.aspose.com/buy) für Lizenzdetails.

### Q2: Gibt es eine kostenlose Testversion?
A2: Natürlich! Holen Sie sich Ihre kostenlose Testversion [hier](https://releases.aspose.com/).

### Q3: Wie kann ich Support für Aspose.CAD für .NET erhalten?
A3: Gehen Sie zum [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

### Q4: Kann ich eine temporäre Lizenz für Testzwecke erhalten?
A4: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q5: Wo finde ich die ausführliche Dokumentation?
A5: Die Dokumentation ist verfügbar unter [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Wie speichere ich CAD als PNG mit hoher Qualität?
A6: Setzen Sie `PageHeight` und `PageWidth` auf die gewünschten Pixelabmessungen und wählen Sie einen DPI von 300 oder höher in `CadRasterizationOptions`.

### Q7: Was ist der beste Weg, **DWG zu konvertieren**, wenn die Quelldatei mehrere Layouts enthält?
A7: Füllen Sie `rasterizationOptions.Layouts` mit allen Layoutnamen, die Sie exportieren möchten, und iterieren Sie dann über jedes Layout und rufen Sie `Save` für jedes Ausgabeformat auf.

---

**Zuletzt aktualisiert:** 2026-03-16  
**Getestet mit:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}