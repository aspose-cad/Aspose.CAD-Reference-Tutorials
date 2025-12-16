---
date: 2025-12-13
description: Erfahren Sie, wie Sie CAD in Java mit Aspose.CAD als JPEG speichern,
  mehrere Ebenen hinzufügen und die CAD‑Abmessungen für eine präzise Bildkonvertierung
  anpassen.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: CAD als JPEG mit Ebenenunterstützung in Java speichern
url: /de/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD als JPEG mit Ebenenunterstützung in Java speichern

## Einführung

In diesem Tutorial erfahren Sie, wie Sie **CAD als JPEG** speichern, während Sie die Ebenenunterstützung von Aspose.CAD für Java voll ausnutzen. Ebenen ermöglichen es, bestimmte Teile einer Zeichnung zu isolieren, sodass Sie nur das exportieren können, was Sie benötigen. Wir führen Sie Schritt für Schritt durch, von der Einrichtung der Umgebung bis zum Export eines JPEGs, das genau die von Ihnen ausgewählten Ebenen enthält.

## Schnelle Antworten
- **Was bedeutet „CAD als JPEG speichern“?** Es konvertiert eine CAD‑Zeichnung in ein Raster‑JPEG‑Bild.
- **Kann ich nur ausgewählte Ebenen einbeziehen?** Ja – verwenden Sie die Methode `setLayers`, um anzugeben, welche Ebenen gerendert werden sollen.
- **Wie ändere ich die Bildgröße?** Passen Sie `setPageWidth` und `setPageHeight` in `CadRasterizationOptions` an.
- **Ist dies eine rein Java‑Lösung?** Das Beispiel verwendet Aspose.CAD für Java, aber dieselben Konzepte gelten auch für andere Sprachen.
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Aspose.CAD for Java Bibliothek** – laden Sie sie von der [Website](https://releases.aspose.com/cad/java/) herunter. Befolgen Sie die Installationsanleitung, um die JAR‑Dateien zu Ihrem Projekt‑Klassenpfad hinzuzufügen.  
2. **Java-Entwicklungsumgebung** – ein aktuelles JDK (Version 8 oder neuer) auf Ihrem Rechner installiert.

Jetzt, wo wir eingerichtet sind, schauen wir uns den Code an, der nötig ist, um **CAD als JPEG** mit selektiver Ebenen‑Renderung zu speichern.

## Namespaces importieren

Beginnen Sie mit dem Import der erforderlichen Aspose.CAD‑Klassen und Standard‑Java‑Hilfsmittel:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dateipfade festlegen

Definieren Sie, wo die Quell‑DWF‑Datei liegt und wohin das Ausgabe‑JPEG geschrieben wird.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Schritt 2: DWF‑Bild laden

Verwenden Sie die Methode `Image.load` von Aspose.CAD, um die CAD‑Zeichnung zu lesen.

```java
Image image = Image.load(srcFile);
```

### Schritt 3: Rasterisierungsoptionen konfigurieren (CAD‑Abmessungen anpassen)

Erstellen Sie eine Instanz von `CadRasterizationOptions` und legen Sie die gewünschte Ausgabengröße fest. Durch Ändern dieser Werte können Sie die **CAD‑Abmessungen** für das endgültige JPEG anpassen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Schritt 4: Ebenen angeben (Mehrere Ebenen hinzufügen)

Wenn Sie mehr als eine Ebene rendern möchten, fügen Sie einfach deren Namen zur Liste hinzu. Hier beginnen wir mit einer einzelnen Ebene namens „LayerA“.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro‑Tipp:* Um **mehrere Ebenen hinzuzufügen**, erweitern Sie den Aufruf `Arrays.asList`, z. B. `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Schritt 5: JPEG‑Optionen konfigurieren (Java CAD‑Bild konvertieren)

Verknüpfen Sie die Rasterisierungseinstellungen mit dem JPEG‑Ausgabeformat.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 6: Export nach JPG (CAD als JPEG speichern)

Schließlich schreiben Sie das Bild auf die Festplatte. Dieser Schritt **speichert die CAD‑Zeichnung als JPEG**‑Datei, die nur die ausgewählten Ebenen enthält.

```java
image.save(outFile, jpegOptions);
```

Durch Befolgen dieser Schritte haben Sie erfolgreich **CAD als JPEG** gespeichert, wobei Sie steuern, welche Ebenen angezeigt werden, und die Bildabmessungen anpassen.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Ebenen werden nicht angezeigt** | Stellen Sie sicher, dass die Ebenennamen exakt mit denen in der DWF‑Datei übereinstimmen (Groß‑/Kleinschreibung beachten). |
| **Ausgabebild ist leer** | Vergewissern Sie sich, dass `setPageWidth` und `setPageHeight` groß genug für die Ausmaße der Zeichnung sind. |
| **Lizenzausnahme** | Verwenden Sie eine Testlizenz für Tests; erhalten Sie eine Voll‑Lizenz für Produktionsumgebungen. |

## Häufig gestellte Fragen

**F: Kann ich mehrere Ebenen zu den Rasterisierungsoptionen hinzufügen?**  
A: Natürlich. Erweitern Sie die `stringList` um zusätzliche Ebenennamen, z. B. `Arrays.asList("LayerA", "LayerB")`.

**F: Ist Aspose.CAD mit anderen CAD‑Formaten kompatibel?**  
A: Ja, es unterstützt DWG, DXF, DWF und viele weitere Formate.

**F: Wie kann ich die Bildabmessungen der Ausgabe ändern?**  
A: Ändern Sie `setPageWidth` und `setPageHeight` in der Instanz von `CadRasterizationOptions`.

**F: Wo kann ich eine Lizenz für Aspose.CAD erwerben?**  
A: Sie können Lizenzoptionen [hier](https://purchase.aspose.com/buy) einsehen.

**F: Wo finde ich Community‑Support?**  
A: Treten Sie der Aspose.CAD‑Community im [Forum](https://forum.aspose.com/c/cad/19) bei, um Hilfe und Diskussionen zu erhalten.

---

**Zuletzt aktualisiert:** 2025-12-13  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}