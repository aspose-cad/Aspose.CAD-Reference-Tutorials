---
date: 2025-12-22
description: Erfahren Sie, wie Sie CAD‑Zeichnungen exportieren und DWG in BMP in Java
  mit Aspose.CAD konvertieren. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung für
  eine effiziente CAD‑Dateiverarbeitung.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Wie man CAD‑Zeichnung mit Aspose.CAD für Java in BMP exportiert
url: /de/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man CAD‑Zeichnung in BMP mit Aspose.CAD für Java exportiert

## Einführung

Wenn Sie nach einer klaren, zuverlässigen Methode suchen, **CAD‑Dateien** aus Java zu **exportieren**, sind Sie hier genau richtig. Mit Aspose.CAD für Java können Sie nicht nur die Zeichengrößen automatisch anpassen, sondern auch **DWG in BMP** mit nur wenigen Codezeilen konvertieren. Dieses Tutorial führt Sie durch den gesamten Prozess, von der Einrichtung Ihrer Umgebung bis zur Erstellung eines BMP‑Bildes, das das ursprüngliche CAD‑Layout beibehält.

## Schnelle Antworten
- **Was bedeutet „how to export cad“?** Es bezieht sich auf die Konvertierung von CAD‑Dateien (DWG, DXF usw.) in ein anderes Format wie BMP, PNG oder PDF.  
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.CAD für Java bietet eine einfache API für diese Aufgabe.  
- **Benötige ich eine Lizenz?** Eine temporäre Lizenz funktioniert für Tests; für die Produktion ist eine Voll‑Lizenz erforderlich.  
- **Kann ich mehrere Layouts gleichzeitig exportieren?** Ja – durch Setzen der `Layouts`‑Eigenschaft können Sie festlegen, welche Layouts gerendert werden sollen.  
- **Ist BMP das einzige Ausgabeformat?** Nein – Sie können auch nach PNG, JPEG, TIFF und mehr exportieren.

## Was bedeutet „how to export cad“ mit Aspose.CAD?
Das Exportieren von CAD bedeutet, eine native CAD‑Zeichnung (z. B. eine DWG‑Datei) zu nehmen und sie in ein Rasterbild oder ein anderes Vektorformat zu rendern. Aspose.CAD übernimmt dabei die gesamte Schwerarbeit: das Parsen der CAD‑Struktur, das Rasterisieren von Vektor‑Entitäten und das Schreiben des Ergebnisses in das von Ihnen gewählte Bildformat.

## Warum Aspose.CAD für Java zum **convert DWG to BMP** verwenden?
- **Keine externen Abhängigkeiten** – reines Java, keine nativen DLLs.  
- **Vollständige Unterstützung für DWG, DXF, DGN und andere Formate**.  
- **Feinkörnige Kontrolle** über Rasterisierungsoptionen wie Layout‑Auswahl, Skalierung und Hintergrundfarbe.  
- **Hohe Leistung** geeignet für Batch‑Verarbeitung auf Servern.

## Voraussetzungen

1. **Java Development Kit** – laden Sie es [hier](https://www.java.com/en/download/) herunter.  
2. **Aspose.CAD für Java Bibliothek** – erhalten Sie das neueste JAR [hier](https://releases.aspose.com/cad/java/).  
3. **Beispiel‑CAD‑Datei** – eine DWG‑Datei (z. B. `sample.dwg`) im Dokumenten‑Verzeichnis Ihres Projekts.

## Namespaces importieren

In Ihrer Java‑Anwendung fügen Sie die notwendigen Namespaces hinzu, um die Aspose.CAD‑Funktionalität zu nutzen. Hier ein Beispiel:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nun zerlegen wir den Prozess des **how to export cad** in handhabbare Schritte.

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: CAD‑Zeichnung laden

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Wir laden die Quell‑DWG‑Datei in ein `Image`‑Objekt, das als Einstiegspunkt für alle nachfolgenden Vorgänge dient.

### Schritt 2: `BmpOptions` erstellen

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` enthält die Rasterisierungseinstellungen, die speziell für die BMP‑Ausgabe gelten.

### Schritt 3: Rasterisierungseinstellungen konfigurieren

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Hier verknüpfen wir die Rasterisierungsoptionen mit den BMP‑Optionen, sodass wir steuern können, wie die CAD‑Entitäten gerendert werden.

### Schritt 4: Layout(s) zum Export festlegen

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Die Eigenschaft `Layouts` teilt Aspose.CAD mit, welche Zeichen‑Layouts einbezogen werden sollen. In den meisten Fällen ist `"Model"` das primäre Layout, das Sie konvertieren möchten.

### Schritt 5: Export im BMP‑Format

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Durch Aufrufen von `save` mit den konfigurierten `BmpOptions` wird die BMP‑Datei auf die Festplatte geschrieben. Damit ist der **convert DWG to BMP**‑Arbeitsablauf abgeschlossen.

## Häufige Probleme und Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| Ausgabe‑Bild ist leer | Falscher Layout‑Name oder fehlendes Layout | Stellen Sie sicher, dass der Layout‑Name mit der CAD‑Datei übereinstimmt (z. B. `"Model"`). |
| Niedrige Auflösung | Standard‑DPI ist niedrig | Setzen Sie `cadRasterizationOptions.setResolution(300);` vor dem Speichern. |
| Out‑of‑Memory‑Fehler bei großen Dateien | Große Zeichnungen benötigen mehr Heap | Erhöhen Sie die JVM‑Heap‑Größe (`-Xmx2g`) oder verarbeiten Sie Seiten einzeln. |

## Häufig gestellte Fragen

**F: Ist Aspose.CAD mit verschiedenen CAD‑Dateiformaten kompatibel?**  
A: Ja, Aspose.CAD unterstützt DWG, DXF, DGN und viele weitere Formate.

**F: Kann ich Aspose.CAD für kommerzielle Projekte verwenden?**  
A: Absolut. Kaufen Sie eine Lizenz [hier](https://purchase.aspose.com/buy) für den Produktionseinsatz.

**F: Wie erhalte ich eine temporäre Lizenz für Tests?**  
A: Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**F: Wo finde ich Community‑Support?**  
A: Treten Sie dem Aspose.CAD‑Community‑Forum bei unter [forum](https://forum.aspose.com/c/cad/19).

**F: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?**  
A: Ja, laden Sie die kostenlose Testversion [hier](https://releases.aspose.com/) herunter.

## Fazit

In diesem Leitfaden haben wir gezeigt, wie man **CAD‑Dateien** aus Java **exportiert** und **DWG in BMP** mit Aspose.CAD konvertiert. Wenn Sie die oben genannten fünf Schritte befolgen, können Sie die CAD‑zu‑Bild‑Konvertierung in jede Java‑Anwendung integrieren, sei es ein Desktop‑Tool, ein Web‑Service oder eine Batch‑Verarbeitungspipeline. Erkunden Sie weitere Ausgabeformate (PNG, JPEG, PDF), indem Sie die Options‑Klasse austauschen, und nutzen Sie das umfangreiche Funktionsspektrum von Aspose.CAD, um all Ihre CAD‑Manipulationsanforderungen zu erfüllen.

---

**Zuletzt aktualisiert:** 2025-12-22  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}