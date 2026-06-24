---
date: 2026-04-13
description: Erfahren Sie, wie Sie CAD‑Layer mit Aspose.CAD für Java rasterisieren.
  Diese Schritt‑für‑Schritt‑Anleitung zeigt die konvertierung auf Ebenen‑Ebene in
  Rasterbilder.
keywords:
- java rasterize cad layer
- Aspose CAD Java
- convert CAD layer to raster
linktitle: CAD-Layer in Rasterbildformat konvertieren
second_title: Aspose.CAD Java API
title: Java CAD‑Ebene rasterisieren – Aspose CAD Tutorial
url: /de/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD Java Tutorial: CAD-Layer in Rasterbildformat konvertieren

## Einführung

Wenn Sie **java rasterize cad layer** Dateien für einfacheres Teilen, Drucken oder nachgelagerte Bildverarbeitung benötigen, sind Sie hier genau richtig. In diesem Tutorial zeigen wir, wie Aspose.CAD für Java es Ihnen ermöglicht, einzelne Ebenen einer CAD-Zeichnung auszuwählen und sie als hochwertige Rasterbilder wie JPEG, PNG oder BMP zu exportieren. Am Ende verstehen Sie, warum selektive Rasterisierung wichtig ist, wie Sie die Rasterisierungsoptionen konfigurieren und das Ergebnis mit nur wenigen Codezeilen speichern.

## Schnelle Antworten
- **Was behandelt dieses Tutorial?** Konvertierung ausgewählter CAD-Ebenen in Rasterbilder mit Aspose.CAD für Java.  
- **Welche Formate werden unterstützt?** Jedes von Aspose unterstützte Rasterformat (JPEG, PNG, BMP usw.).  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine Lizenz erforderlich.  
- **Was sind die Voraussetzungen?** Java-Entwicklungsumgebung und die Aspose.CAD Java-Bibliothek.  
- **Wie lange dauert die Implementierung?** Etwa 10–15 Minuten für eine grundlegende Konvertierung.

## Was ist “java rasterize cad layer”?

Das Rasterisieren einer CAD-Ebene bedeutet, die Vektordaten dieser spezifischen Ebene in ein pixelbasiertes Bild zu konvertieren. Dieser Vorgang bewahrt das visuelle Erscheinungsbild der Ebene, macht sie jedoch kompatibel mit jedem System, das Standard‑Bildformate anzeigen kann.

## Warum diesen Ansatz verwenden?

- **Selektiver Export** – Nur die benötigten Ebenen werden gerendert, wodurch Dateigröße und Verarbeitungszeit reduziert werden.  
- **Formatflexibilität** – Wechseln Sie `JpegOptions` zu `PngOptions`, `BmpOptions` usw., ohne die Kernlogik zu ändern.  
- **Hochwertiges Rendering** – Aspose.CAD bewahrt Linienstärken, Farben und Text exakt wie in der Original‑CAD‑Datei.  

## Voraussetzungen

Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java-Entwicklungsumgebung** – Installiertes und konfiguriertes JDK 8 oder höher.  
- **Aspose.CAD-Bibliothek** – Laden Sie die Aspose.CAD-Bibliothek für Java von dem [download link](https://releases.aspose.com/cad/java/) herunter und installieren Sie sie.  

## Namespaces importieren

In diesem Schritt importieren wir die notwendigen Klassen, um mit CAD-Dateien zu arbeiten.

### Aspose.CAD-Klassen importieren

In Ihrer Java-Quelldatei fügen Sie die erforderlichen Aspose.CAD-Importe ein:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## CAD-Layer in Rasterbildformat konvertieren

Nachfolgend finden Sie den vollständigen Schritt‑für‑Schritt‑Prozess. Jeder Schritt wird in Klartext erklärt, bevor der Codeblock folgt, sodass Sie genau wissen, was passiert.

### Schritt 1: CAD-Datei einrichten

Zuerst geben Sie den Pfad zu Ihrer CAD-Datei an und laden sie in ein `Image`‑Objekt.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Schritt 2: Rasterisierungsoptionen konfigurieren

Erstellen Sie eine Instanz von `CadRasterizationOptions`, um die Ausgabegröße und -qualität des Bildes festzulegen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### Schritt 3: CAD-Ebenen angeben

Fügen Sie die Ebenennamen hinzu, die Sie rasterisieren möchten. In diesem Beispiel exportieren wir die Standard‑Ebene `"0"`.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### Schritt 4: JPEG-Optionen einrichten

Erstellen Sie ein `JpegOptions`‑Objekt (oder andere Rasterbildoptionen) und verknüpfen Sie es mit den Rasterisierungseinstellungen.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 5: Als JPEG exportieren

Abschließend speichern Sie die rasterisierte Ebene als JPEG‑Datei.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

Wiederholen Sie die obigen Schritte für weitere Ebenen oder passen Sie die Rasterisierungsparameter (Auflösung, Hintergrundfarbe usw.) an Ihre spezifischen Anforderungen an.

## Häufige Probleme & Fehlerbehebung

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| Leeres Bild | Keine Ebenen angegeben oder falscher Ebenenname | Überprüfen Sie, ob die Ebenennamen in der CAD-Datei existieren; verwenden Sie `image.getLayers()`, um sie aufzulisten. |
| Niedrige Auflösung | Standard‑DPI ist niedrig | Setzen Sie `rasterizationOptions.setResolution(300);` (oder höher) vor dem Speichern. |
| Nicht unterstütztes CAD-Format | Verwendung einer älteren Aspose.CAD-Version | Aktualisieren Sie auf die neueste Aspose.CAD für Java-Version. |

## Häufig gestellte Fragen

**F: Kann ich Aspose.CAD für Java mit anderen Programmiersprachen verwenden?**  
**A:** Aspose.CAD unterstützt hauptsächlich Java, es gibt jedoch .NET-, C++- und weitere Sprachversionen.

**F: Wo finde ich zusätzliche Unterstützung oder Hilfe?**  
**A:** Für Fragen oder Unterstützung besuchen Sie das [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

**F: Gibt es eine kostenlose Testversion?**  
**A:** Ja, Sie können Aspose.CAD mit einer kostenlosen Testversion von [hier](https://releases.aspose.com/) erkunden.

**F: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?**  
**A:** Erwerben Sie eine temporäre Lizenz über [diesen Link](https://purchase.aspose.com/temporary-license/).

**F: Gibt es spezifische Systemanforderungen für Aspose.CAD für Java?**  
**A:** Stellen Sie sicher, dass Sie eine kompatible Java-Entwicklungsumgebung haben; siehe die Dokumentation für detaillierte Anforderungen.

---

**Letzte Aktualisierung:** 2026-04-13  
**Getestet mit:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}