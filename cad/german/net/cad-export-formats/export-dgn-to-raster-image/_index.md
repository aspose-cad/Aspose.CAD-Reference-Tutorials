---
date: 2026-03-24
description: Erfahren Sie, wie Sie DGN in PNG konvertieren und CAD als JPEG speichern
  können, mit Aspose.CAD für .NET – ein kurzer Leitfaden zur CAD‑zu‑Bild‑Konvertierung.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Wie man DGN in PNG mit Aspose.CAD für .NET konvertiert
url: /de/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN in PNG konvertieren mit Aspose.CAD für .NET

In der modernen .NET‑Entwicklung ist **convert dgn to png** ein häufiges Anliegen, wenn Sie CAD‑Zeichnungen im Web anzeigen oder in Berichten einbetten müssen. Aspose.CAD für .NET macht diese Konvertierung unkompliziert und ermöglicht es Ihnen, eine DGN‑Datei mit nur wenigen Codezeilen in ein hochqualitatives Rasterbild zu verwandeln. In diesem Leitfaden führen wir Sie durch den gesamten Prozess – von der Projekt‑Einrichtung bis zum Speichern der finalen PNG‑ (oder JPEG‑) Datei.

## Quick Answers
- **Kann ich DGN mit Aspose.CAD nach PNG konvertieren?** Ja – konfigurieren Sie einfach die Rasterisierungsoptionen und wählen Sie PNG oder JPEG als Ausgabe.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Für den Einsatz außerhalb der Testphase ist eine gültige Aspose.CAD‑Lizenz erforderlich.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Welche Bildformate stehen zur Verfügung?** PNG, JPEG, BMP, GIF, TIFF und weitere.  
- **Ist Ausnahmebehandlung notwendig?** Auf jeden Fall – wickeln Sie die Konvertierung in try/catch ein, um Zugriffsprobleme zu behandeln.

## Was bedeutet „convert dgn to png“?
Das Konvertieren einer DGN‑ (MicroStation‑) Datei in PNG bedeutet, Vektor‑CAD‑Daten in ein pixelbasiertes Bild zu rasterisieren. Das ist nützlich für die Erstellung von Vorschaubildern, das Einbetten von Zeichnungen in HTML‑E‑Mails oder das Erzeugen von Thumbnails für Dokumenten‑Management‑Systeme.

## Warum Aspose.CAD für die CAD‑zu‑Bild‑Konvertierung verwenden?
- **Keine externen Abhängigkeiten** – funktioniert rein in verwaltetem Code.  
- **Hohe Treue** – bewahrt Linienstärken, Ebenen und Farben.  
- **Flexible Ausgabe** – wechseln Sie zwischen PNG, JPEG, BMP usw., indem Sie nur eine Option ändern.  
- **Leistungsoptimiert** – die Rasterisierung ist selbst bei großen Zeichnungen schnell.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie:

- **Aspose.CAD für .NET** in Ihrem Projekt installiert haben. Sie können es von der [Website](https://reference.aspose.com/cad/net/) herunterladen.  
- Eine Beispiel‑DGN‑Datei (z. B. `Nikon_D90_Camera.dgn`) in einem bekannten Verzeichnis abgelegt haben.

## Namespaces importieren

Fügen Sie zunächst die benötigten `using`‑Anweisungen hinzu, damit Sie auf die Aspose.CAD‑Klassen zugreifen können.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DGN‑Datei laden

Laden Sie die Quell‑DGN in ein `CadImage`‑Objekt. Dieses Objekt repräsentiert die CAD‑Zeichnung im Speicher und dient als Quelle für die Rasterisierung.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Schritt 2: Rasterisierungsoptionen definieren

Konfigurieren Sie, wie die CAD‑Zeichnung rasterisiert werden soll. Hier können Sie Bildgröße, Skalierung und Hintergrundfarbe festlegen.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Schritt 3: Ausgabeformat wählen (PNG oder JPEG)

Obwohl das Tutorial auf PNG fokussiert, können Sie auch **save cad as jpeg** verwenden. Erzeugen Sie das passende Image‑Options‑Objekt und verknüpfen Sie die Rasterisierungseinstellungen.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro‑Tipp:** Um eine PNG‑Datei zu erzeugen, ersetzen Sie `new JpegOptions()` durch `new PngOptions()`.

## Schritt 4: Rasterbild speichern

Rufen Sie schließlich `Save` auf der `CadImage`‑Instanz auf, geben Sie den gewünschten Dateinamen und das konfigurierte Options‑Objekt an.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Wenn Sie zu `PngOptions` gewechselt haben, wird die Datei als `ExportDGNToRasterImage_out.png` gespeichert.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|-------|-----|
| **Leeres Ausgabebild** | `NoScaling` falsch gesetzt oder Layout nicht ausgewählt | `AutomaticLayoutsScaling = true` setzen oder das gewünschte Layout angeben. |
| **Out‑of‑memory bei großen Dateien** | Große DGN wird ohne Streaming geladen | `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })` verwenden. |
| **Nicht unterstützte DGN‑Version** | Ältere MicroStation‑Versionen | Sicherstellen, dass Sie die neueste Aspose.CAD‑Version verwenden, die Legacy‑Formate unterstützt. |

## Häufig gestellte Fragen

**F: Kann ich DGN‑Dateien in andere Formate als JPEG exportieren?**  
A: Ja, Aspose.CAD für .NET unterstützt PNG, BMP, GIF, TIFF und weitere – einfach die Options‑Klasse austauschen (z. B. `new PngOptions()`).

**F: Wie sollte ich Ausnahmen während der Konvertierung behandeln?**  
A: Wickeln Sie den Konvertierungscode in einen `try/catch`‑Block und loggen Sie `Aspose.CAD.CadException` für detaillierte Fehlermeldungen.

**F: Gibt es eine Testversion von Aspose.CAD für .NET?**  
A: Ja, Sie können das Produkt mit einer kostenlosen Testversion ausprobieren. Weitere Informationen finden Sie [hier](https://releases.aspose.com/).

**F: Wo finde ich Unterstützung oder Diskussionen zu Aspose.CAD für .NET?**  
A: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

**F: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für .NET?**  
A: Unter [diesem Link](https://purchase.aspose.com/temporary-license/) können Sie eine temporäre Lizenz für Ihre Entwicklungsbedürfnisse erwerben.

## Fazit

Sie haben nun gelernt, wie Sie **convert dgn to png** (oder JPEG) mit Aspose.CAD für .NET durchführen. Durch Anpassen der Rasterisierungsoptionen und Austausch der Image‑Options‑Klasse können Sie die Ausgabe an jede Projektanforderung anpassen. Experimentieren Sie gern mit verschiedenen Seitengrößen, DPI‑Einstellungen und Dateiformaten, um das perfekte Rasterbild für Ihre Anwendung zu erhalten.

---

**Zuletzt aktualisiert:** 2026-03-24  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}