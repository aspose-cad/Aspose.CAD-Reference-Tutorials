---
date: 2025-12-18
description: Erfahren Sie, wie Sie DWG mit Aspose.CAD für Java in PNG und andere Rasterbildformate
  konvertieren. Exportieren Sie CAD als PNG mit hochwertigen Ergebnissen.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: DWG in PNG und andere Rasterformate mit Aspose.CAD für Java konvertieren
url: /de/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG in PNG und andere Rasterformate konvertieren mit Aspose.CAD für Java

## Einleitung

Das Konvertieren von DWG in PNG (oder andere Rasterbildformate) ist ein häufiges Bedürfnis, wenn Sie CAD‑Zeichnungen mit Teamkollegen teilen müssen, die keinen CAD‑Viewer haben, Designs in Dokumentationen einbetten oder Miniaturansichten für Webgalerien erzeugen wollen. Aspose.CAD für Java macht diese Konvertierung unkompliziert, egal ob Sie mit einer kompletten Zeichnungsdatei oder nur einem bestimmten Layout arbeiten. In diesem Tutorial führen wir Sie durch die genauen Schritte, um **ein CAD‑Layout in ein Rasterbild zu konvertieren** – dieselbe Technik, die Sie anwenden können, um PNG, JPEG, TIFF oder PDF auszugeben.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet DWG zu PNG?** Aspose.CAD für Java  
- **Welche Formate können exportiert werden?** PNG, JPEG, TIFF, PDF, BMP und mehr  
- **Benötige ich eine Lizenz für Tests?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine Lizenz erforderlich  
- **Kann ich ein bestimmtes Layout auswählen?** Ja, verwenden Sie `setLayouts`, um „Model“, „Layout1“ usw. anzusprechen.  
- **Ist eine hochauflösende Ausgabe möglich?** Absolut – passen Sie `setPageWidth` und `setPageHeight` an, um die DPI zu steuern  

## Was bedeutet „convert dwg to png“?

Der Ausdruck „convert dwg to png“ beschreibt den Vorgang, eine vektorbasierte DWG‑Datei (das native Format vieler CAD‑Anwendungen) in ein pixelbasiertes PNG‑Bild zu rasterisieren. Rasterbilder eignen sich ideal für die Anzeige im Web, das Teilen per E‑Mail und die Integration in Nicht‑CAD‑Software.

## Warum CAD als PNG (oder andere Rasterformate) exportieren?

- **Universelle Kompatibilität:** PNG und JPEG werden von praktisch jedem Bildbetrachter und Browser unterstützt.  
- **Schnelles Laden:** Rasterbilder laden sofort im Vergleich zum Öffnen einer großen DWG‑Datei.  
- **Einfache Einbettung:** PNGs direkt in Word, PowerPoint oder HTML einfügen, ohne zusätzliche Plugins.  
- **Konsistentes Erscheinungsbild:** Sie steuern Auflösung, Hintergrund und Layout, sodass jeder Beteiligte dieselbe Darstellung sieht.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java-Entwicklungsumgebung** – JDK 8 oder neuer installiert und konfiguriert.  
2. **Aspose.CAD für Java** – Laden Sie das neueste JAR von der [Aspose.CAD für Java Dokumentation](https://reference.aspose.com/cad/java/) herunter.

## Namespaces importieren

Zuerst importieren Sie die Klassen, die Sie benötigen. Diese Importe geben Ihnen Zugriff auf das Laden von Bildern, Rasterisierungsoptionen und die TIFF/PNG‑Ausgabe‑Einstellungen.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro‑Tipp:** Wenn Sie stattdessen nach PNG exportieren möchten, ersetzen Sie `TiffOptions` durch `PngOptions` (zu finden in `com.aspose.cad.imageoptions.PngOptions`).

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Ressourcenverzeichnis einrichten

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ersetzen Sie `"Your Document Directory"` durch den absoluten Pfad, in dem Ihre CAD‑Dateien liegen.

### Schritt 2: CAD‑Datei laden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Sie können jedes unterstützte Format laden (DWG, DXF, DGN usw.). Dies ist der **how to convert cad**‑Teil – zeigen Sie einfach auf die Datei und lassen Sie Aspose das Parsen übernehmen.

### Schritt 3: Rasterisierungsoptionen konfigurieren

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` steuern die Ausgaberesolution (größere Werte = höhere DPI).  
- `setLayouts` ermöglicht es Ihnen, **convert cad to raster** für bestimmte Layouts auszuführen; lassen Sie es weg, um die gesamte Zeichnung zu rasterisieren.

### Schritt 4: Bildoptionen festlegen

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Wenn Sie PNG bevorzugen, instanziieren Sie `PngOptions` anstelle von `TiffOptions`. Hier erfolgt das **export cad as png**.

### Schritt 5: Ergebnisbild speichern

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Ändern Sie die Dateierweiterung zu `.png` (und das Options‑Objekt zu `PngOptions`), um **CAD als JPEG/PNG zu speichern**.

> **Häufiges Problem:** Wenn die Dateierweiterung nicht zur Options‑Klasse passt, führt das zu einer `UnsupportedFormatException`. Halten Sie sie stets synchron.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|---------|--------|
| **Leeres Ausgabebild** | Stellen Sie sicher, dass die Layout‑Namen in `setLayouts` exakt mit denen in der Quell‑CAD‑Datei übereinstimmen. |
| **Niedrigauflösendes PNG** | Erhöhen Sie `setPageWidth` / `setPageHeight` oder setzen Sie `setResolution` in den Rasterisierungsoptionen. |
| **Nicht unterstützte DWG‑Version** | Stellen Sie sicher, dass Sie die neueste Aspose.CAD‑Version verwenden; ältere Versionen unterstützen möglicherweise neuere DWG‑Versionen nicht. |
| **Speicherfehler bei großen Dateien** | Verarbeiten Sie Seiten einzeln oder erhöhen Sie den JVM‑Heap (`-Xmx2g`). |

## Häufig gestellte Fragen

**F: Ist Aspose.CAD mit verschiedenen CAD‑Dateiformaten kompatibel?**  
A: Ja, es unterstützt DWG, DXF, DGN und viele weitere.

**F: Kann ich die Auflösung des Ausgaberasterbildes anpassen?**  
A: Absolut. Passen Sie `setPageWidth`, `setPageHeight` oder `setResolution` in `CadRasterizationOptions` an.

**F: Wie kann ich mehrere CAD‑Layouts in einem Durchlauf konvertieren?**  
A: Übergeben Sie ein Array mit allen Layout‑Namen an `setLayouts`, z. B. `new String[]{"Model","Layout1","Layout2"}`.

**F: Gibt es neben TIFF weitere unterstützte Ausgabeformate?**  
A: Ja – PNG, JPEG, BMP, PDF und weitere sind über die jeweiligen `*Options`‑Klassen verfügbar.

**F: Wo kann ich Hilfe erhalten oder meine Erfahrungen mit Aspose.CAD teilen?**  
A: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und offizielle Unterstützung.

## Fazit

Wenn Sie diese Schritte befolgen, können Sie **DWG in PNG konvertieren**, **CAD als PNG exportieren**, **CAD als JPEG speichern** oder jedes andere benötigte Rasterformat erzeugen. Aspose.CAD für Java übernimmt die schwere Arbeit, sodass Sie sich darauf konzentrieren können, hochwertige Bilder in Ihre Anwendungen, Dokumentationen oder Webportale zu integrieren.

---

**Zuletzt aktualisiert:** 2025-12-18  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}