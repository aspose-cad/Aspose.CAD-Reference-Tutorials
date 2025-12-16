---
date: 2025-12-16
description: Erfahren Sie, wie Sie CAD mit Aspose.CAD für Java in PNG konvertieren,
  einschließlich des Exports von DWG in ein Bild, des Speicherns von CAD als PNG und
  der Optionen für CAD zu Rasterbild.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Wie man CAD in PNG mit Aspose.CAD für Java konvertiert
url: /de/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# So konvertieren Sie CAD in PNG mit Aspose.CAD für Java

In modernen Ingenieur‑Workflows müssen Sie häufig **CAD in PNG konvertieren**, damit Zeichnungen in Browsern angezeigt, in Dokumente eingebettet oder mit Stakeholdern geteilt werden können, die keine CAD‑Software besitzen. Dieses Tutorial führt Sie durch den gesamten Prozess – vom Laden einer CAD‑Datei bis zum Export eines hochqualitativen PNG‑Rasterbildes – mithilfe der leistungsstarken Aspose.CAD‑Bibliothek für Java.

## Schnelle Antworten
- **Was ist der Hauptzweck?** CAD‑Zeichnungen in PNG‑Rasterbilder konvertieren.  
- **Welche Bibliothek wird verwendet?** Aspose.CAD für Java.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Kann ich die Bildgröße anpassen?** Ja, verwenden Sie `CadRasterizationOptions`, um Breite und Höhe festzulegen.  
- **Unterstützte CAD‑Formate?** DWG, DXF, DWF und viele weitere.

## Was bedeutet „CAD in PNG konvertieren“?
Das Konvertieren von CAD zu PNG bedeutet, vektorbasierte CAD‑Inhalte (DWG, DXF usw.) in ein pixelbasiertes Bildformat zu rasterisieren. PNG behält Transparenz und verlustfreie Qualität bei, wodurch es ideal für Web‑Vorschauen, Dokumentation und Berichte ist.

## Warum CAD in PNG konvertieren (CAD zu Rasterbild)?
- **Universelle Ansicht:** PNG funktioniert auf jedem Gerät ohne spezielle CAD‑Betrachter.  
- **Schnelles Laden:** Rasterbilder werden sofort in Webseiten geladen.  
- **Einfache Einbettung:** PNGs in PDFs, Word‑Dokumente oder Präsentationen einfügen.  
- **Konsistentes Aussehen:** Linienbreiten, Farben und Ebenen exakt wie im Entwurf beibehalten.

## Voraussetzungen
Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java‑Entwicklungsumgebung** – JDK 8 oder neuer installiert und konfiguriert.  
2. **Aspose.CAD‑Bibliothek** – Bibliothek herunterladen und dem Projekt hinzufügen. Sie finden die Bibliothek **[hier](https://releases.aspose.com/cad/java/)**.

## Namespaces importieren
Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu, damit Sie mit Aspose.CAD‑Objekten arbeiten können.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Schritt‑für‑Schritt‑Anleitung zum Konvertieren von CAD in PNG

### Schritt 1: CAD‑Zeichnung laden
Laden Sie zunächst die Quell‑CAD‑Datei (DXF, DWG usw.) mit `Image.load()`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **Pro‑Tipp:** Bewahren Sie Ihre CAD‑Dateien in einem eigenen Ordner (z. B. `CADConversion`) auf, um Pfadprobleme zu vermeiden.

### Schritt 2: Rasterisierungsoptionen festlegen (DWG in Bild exportieren)
Definieren Sie die Ausgabe‑Bildgröße und weitere Rastereinstellungen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

Sie können hier bei Bedarf auch Hintergrundfarbe, Linienrender‑Modus und DPI steuern.

### Schritt 3: Bildoptionen erstellen (CAD als PNG speichern)
Erzeugen Sie eine `PpngOptions`‑Instanz und verknüpfen Sie die Rasterisierungs‑Einstellungen.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 4: Rasterbild speichern (CAD‑Datei zu PNG)
Schreiben Sie schließlich die PNG‑Datei auf die Festplatte.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Die resultierende Datei `conic_pyramid_raster_image_out.png` ist eine hochauflösende PNG‑Darstellung Ihrer ursprünglichen CAD‑Zeichnung.

### Wiederholen für andere Dateien
Ändern Sie einfach `srcFile`, sodass er auf eine andere CAD‑Datei zeigt, und führen Sie dieselben Schritte aus. Der gleiche Code funktioniert für DWG, DWF und andere unterstützte Formate.

## Häufige Probleme & Lösungen
| Problem | Lösung |
|---------|--------|
| **Leeres PNG‑Ergebnis** | Vergewissern Sie sich, dass die Quell‑CAD‑Datei korrekt geladen wird (`Image.load()` sollte keine Ausnahme werfen). |
| **Falsche Abmessungen** | Passen Sie `PageWidth` / `PageHeight` an oder setzen Sie DPI über `rasterizationOptions.setResolution(...)`. |
| **Fehlende Ebenen** | Stellen Sie sicher, dass die Ebenen der CAD‑Datei nicht ausgeblendet sind; verwenden Sie `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`. |
| **Lizenzfehler** | Verwenden Sie eine gültige Aspose.CAD‑Lizenzdatei (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## Häufig gestellte Fragen

**Q1: Ist Aspose.CAD mit allen CAD‑Formaten kompatibel?**  
A1: Aspose.CAD unterstützt eine breite Palette von CAD‑Formaten, darunter DWG, DXF, DWF und weitere. Die vollständige Liste finden Sie in der **[Dokumentation](https://reference.aspose.com/cad/java/)**.

**Q2: Kann ich die Rasterisierungsoptionen für meine spezifischen Anforderungen anpassen?**  
A2: Ja, Aspose.CAD bietet Flexibilität beim Festlegen der Rasterisierungsoptionen, sodass Sie die Ausgabe nach Ihren Bedürfnissen (Größe, DPI, Hintergrundfarbe usw.) anpassen können.

**Q3: Wo finde ich Support für Fragen zu Aspose.CAD?**  
A3: Besuchen Sie das **[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19)**, um Unterstützung zu erhalten und sich mit der Community auszutauschen.

**Q4: Gibt es eine kostenlose Testversion von Aspose.CAD für Java?**  
A4: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion **[hier](https://releases.aspose.com/)** ausprobieren.

**Q5: Wie kann ich Aspose.CAD für Java erwerben?**  
A5: Um Aspose.CAD für Java zu kaufen, besuchen Sie die **[Kaufseite](https://purchase.aspose.com/buy)**.

**Letzte Aktualisierung:** 2025-12-16  
**Getestet mit:** Aspose.CAD für Java 24.11 (zum Zeitpunkt der Erstellung aktuell)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}