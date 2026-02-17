---
date: 2026-02-17
description: Erfahren Sie, wie Sie DWG in Java mit Aspose.CAD als JPEG speichern,
  mehrere Ebenen hinzufügen und CAD‑Abmessungen für eine präzise Bildkonvertierung
  anpassen.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: DWG als JPEG mit Ebenenunterstützung in Java speichern
url: /de/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG als JPEG mit Layer‑Unterstützung in Java speichern

## Einleitung

In diesem Tutorial erfahren Sie, wie Sie **DWG als JPEG speichern** und dabei die Layer‑Unterstützung von Aspose.CAD für Java voll ausnutzen. Layer ermöglichen es, bestimmte Teile einer Zeichnung zu isolieren, sodass Sie nur das exportieren können, was Sie benötigen. Wir führen Sie Schritt für Schritt durch, von der Einrichtung der Umgebung bis zum Export eines JPEGs, das nur die von Ihnen gewählten Layer enthält.

## Schnelle Antworten
- **Was bedeutet „DWG als JPEG speichern“?** Es konvertiert eine DWG‑ (oder andere CAD‑) Zeichnung in ein Raster‑JPEG‑Bild.  
- **Kann ich nur ausgewählte Layer einbeziehen?** Ja – verwenden Sie die Methode `setLayers`, um anzugeben, welche Layer gerendert werden sollen.  
- **Wie ändere ich die Bildgröße?** Passen Sie `setPageWidth` und `setPageHeight` in `CadRasterizationOptions` an.  
- **Ist dies eine rein Java‑Lösung?** Das Beispiel verwendet Aspose.CAD für Java, aber dieselben Konzepte gelten auch für andere Sprachen.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert zum Testen; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.

## Was bedeutet „DWG als JPEG speichern“?
DWG als JPEG zu speichern bedeutet, eine vektorbasierte CAD‑Datei (DWG, DWF, DXF usw.) in ein Standard‑JPEG‑Bitmap zu rasterisieren. Dies ist nützlich, wenn Sie CAD‑Zeichnungen in Webseiten, E‑Mails oder Berichte einbetten müssen, die nur Rasterbilder unterstützen.

## Warum eine layer‑bewusste JPEG‑Konvertierung verwenden?
- **Fokus auf relevante Daten:** Exportieren Sie nur die benötigten Layer, wodurch Dateigröße und visuelle Unordnung reduziert werden.  
- **Designintention beibehalten:** Layer erhalten die logische Gruppierung von Objekten, sodass Sie dieselbe Quelldatei für verschiedene Ausgaben wiederverwenden können.  
- **Vollständige Kontrolle über Abmessungen:** Durch Anpassen der Rasterisierungsoptionen können Sie hochauflösende Bilder erzeugen, die Ihren Veröffentlichungsanforderungen entsprechen.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Aspose.CAD for Java Bibliothek** – laden Sie sie von der [Website](https://releases.aspose.com/cad/java/) herunter. Befolgen Sie die Installationsanleitung, um die JAR‑Dateien zu Ihrem Projekt‑Classpath hinzuzufügen.  
2. **Java-Entwicklungsumgebung** – ein aktuelles JDK (8 oder neuer) auf Ihrem Rechner installiert.

Jetzt, wo wir eingerichtet sind, schauen wir uns den Code an, der nötig ist, um **DWG als JPEG zu speichern** mit selektiver Layer‑Renderung.

## Namespaces importieren

Beginnen Sie damit, die erforderlichen Aspose.CAD‑Klassen und Standard‑Java‑Hilfsmittel zu importieren:

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

Erstellen Sie eine Instanz von `CadRasterizationOptions` und legen Sie die gewünschte Ausgabengröße fest. Durch Ändern dieser Werte können Sie die **CAD‑Abmessungen** für das endgültige JPEG **anpassen**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Schritt 4: Layer angeben (mehrere Layer hinzufügen)

Wenn Sie mehr als einen Layer rendern möchten, fügen Sie einfach deren Namen zur Liste hinzu. Hier beginnen wir mit einem einzelnen Layer namens „LayerA“.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro Tipp:* Um **mehrere Layer hinzuzufügen**, erweitern Sie den Aufruf `Arrays.asList`, z. B. `Arrays.asList("LayerA", "LayerB", "LayerC")`. Damit können Sie **bestimmte CAD‑Layer** für die Konvertierung **auswählen**.

### Schritt 5: JPEG‑Optionen konfigurieren (Java CAD‑Bild konvertieren)

Verknüpfen Sie die Rasterisierungseinstellungen mit dem JPEG‑Ausgabeformat.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 6: Export nach JPG (DWG als JPEG speichern)

Schließlich schreiben Sie das Bild auf die Festplatte. Dieser Schritt **speichert die CAD‑Zeichnung als JPEG**‑Datei, die nur die ausgewählten Layer enthält.

```java
image.save(outFile, jpegOptions);
```

Durch Befolgen dieser Schritte haben Sie erfolgreich **DWG als JPEG gespeichert**, wobei Sie steuern, welche Layer angezeigt werden, und die Bildabmessungen anpassen.

## Wie man DWF mit Layer‑Auswahl in JPEG konvertiert

Obwohl das Beispiel eine DWF‑Quelle verwendet, funktioniert die gleiche Rasterisierungspipeline für jedes unterstützte CAD‑Format (DWG, DXF, DGN usw.). Ändern Sie einfach die Dateierweiterung in `srcFile` und die Bibliothek führt die **Konvertierung von DWF zu JPEG** (oder ein anderes Format) automatisch aus.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Layer werden nicht angezeigt** | Stellen Sie sicher, dass die Layer‑Namen exakt mit denen im DWF‑File übereinstimmen (Groß‑/Kleinschreibung beachten). |
| **Ausgabebild ist leer** | Stellen Sie sicher, dass `setPageWidth` und `setPageHeight` groß genug für die Ausmaße der Zeichnung sind. |
| **Lizenzausnahme** | Verwenden Sie eine Testlizenz zum Testen; erhalten Sie eine Voll‑Lizenz für Produktionsumgebungen. |

## Häufig gestellte Fragen

**F: Kann ich mehrere Layer zu den Rasterisierungsoptionen hinzufügen?**  
A: Absolut. Erweitern Sie die `stringList` um zusätzliche Layer‑Namen, z. B. `Arrays.asList("LayerA", "LayerB")`.

**F: Ist Aspose.CAD mit anderen CAD‑Formaten kompatibel?**  
A: Ja, es unterstützt DWG, DXF, DWF und viele weitere Formate.

**F: Wie kann ich die Bildabmessungen der Ausgabe ändern?**  
A: Ändern Sie `setPageWidth` und `setPageHeight` in der `CadRasterizationOptions`‑Instanz.

**F: Wo kann ich eine Lizenz für Aspose.CAD erwerben?**  
A: Sie können Lizenzoptionen [hier](https://purchase.aspose.com/buy) einsehen.

**F: Wo finde ich Community‑Support?**  
A: Treten Sie der Aspose.CAD‑Community im [Forum](https://forum.aspose.com/c/cad/19) bei, um Hilfe und Diskussionen zu erhalten.

---

**Zuletzt aktualisiert:** 2026-02-17  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}