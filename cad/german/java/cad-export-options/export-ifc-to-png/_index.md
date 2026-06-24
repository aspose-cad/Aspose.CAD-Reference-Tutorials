---
date: 2026-02-20
description: Konvertieren Sie IFC mühelos in PNG mit Aspose.CAD für Java. Folgen Sie
  unserem Schritt‑für‑Schritt‑Tutorial.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Wie man IFC mit Aspose.CAD für Java in PNG konvertiert
url: /de/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export IFC to PNG mit Aspose.CAD für Java

## Einführung

Willkommen zu diesem Schritt‑für‑Schritt‑Tutorial über **wie man IFC zu PNG konvertiert** mit Aspose.CAD für Java. Egal, ob Sie eine BIM‑zu‑Bild‑Pipeline erstellen oder schnelle visuelle Vorschauen von IFC‑Modellen benötigen, führt Sie dieser Leitfaden durch jedes Detail, sodass Sie **IFC zu PNG** zuverlässig in Ihren Java‑Anwendungen konvertieren können.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.CAD für Java  
- **Kann ich IFC zu PNG in wenigen Codezeilen konvertieren?** Ja – der Kernprozess passt in weniger als 20 Zeilen.  
- **Benötige ich eine Lizenz für die Produktion?** Eine temporäre Lizenz funktioniert für Tests; eine Voll‑Lizenz ist für den kommerziellen Einsatz erforderlich.  
- **Ist die Ausgabe skalierbar?** Die Rasterisierungsoptionen ermöglichen das Festlegen beliebiger Pixel‑Abmessungen.  
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher.

## Was bedeutet „convert IFC to PNG“?
Das Konvertieren von IFC (Industry Foundation Classes) zu PNG bedeutet, die 3‑D‑Gebäudemodell‑Daten in ein 2‑D‑Bitmap‑Bild zu rasterisieren. Dies ist nützlich, um Thumbnails zu erzeugen, Modelle in Berichte einzubetten oder web‑fertige Visualisierungen zu erstellen, ohne einen vollständigen CAD‑Viewer zu benötigen.

## Warum Aspose.CAD für Java verwenden?
- **Voll‑funktions‑** Unterstützung für viele CAD‑Formate, einschließlich IFC.  
- **Keine externen Abhängigkeiten** – reines Java, einfach zu integrieren.  
- **Fein‑granulare Kontrolle** über die Rasterisierung (Auflösung, Hintergrund, Linienstärke).  
- **Plattform‑übergreifend** – funktioniert unter Windows, Linux und macOS.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD Bibliothek** – laden Sie die Aspose.CAD Bibliothek für Java von dem [Download‑Link](https://releases.aspose.com/cad/java/) herunter und installieren Sie sie.  
- **Dokumenten‑Verzeichnis** – ein Ordner auf Ihrem System, der die IFC‑Datei enthält, die Sie konvertieren möchten.

## Namespaces importieren

Importieren Sie in Ihrem Java‑Projekt die erforderlichen Klassen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Laden der IFC‑Datei
Zuerst geben Sie den Ordner an, in dem sich Ihre IFC‑Datei befindet, und laden sie.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Warum das wichtig ist:** Das Laden der Datei als `IfcImage` gibt Ihnen später Zugriff auf CAD‑spezifische Rasterisierungsoptionen.

### Schritt 2: Vektor‑ (Rasterisierungs‑)Optionen festlegen
Definieren Sie die Ausgabedimensionen und weitere vektorbezogene Einstellungen.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Sie können `PageWidth` und `PageHeight` anpassen, um die endgültige PNG‑Auflösung zu steuern, was wichtig ist, wenn Sie **PNG‑java‑Dateien** für hochqualitative Drucke speichern.

### Schritt 3: PNG‑Optionen konfigurieren
Verknüpfen Sie die Rasterisierungsoptionen mit dem PNG‑Exporter.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Schritt 4: Bild als PNG speichern
Schreiben Sie schließlich das rasterisierte Bild auf die Festplatte.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Nach diesem Schritt haben Sie **IFC zu PNG** erfolgreich konvertiert und können das resultierende `example.png` überall dort verwenden, wo Sie ein Rasterbild benötigen.

## Häufige Anwendungsfälle
- **Thumbnails generieren** für BIM‑Modelle in Web‑Portalen.  
- **Grundriss‑Schnappschüsse** in PDF‑Berichte einbetten.  
- **Automatisierte Batch‑Konvertierung** großer IFC‑Bibliotheken für die Archivierung.

## Fehlersuche & Tipps
- **Speicherprobleme:** Beim Konvertieren sehr großer IFC‑Dateien erhöhen Sie den JVM‑Heap (`-Xmx2g` oder höher).  
- **Fehlende Texturen:** Stellen Sie sicher, dass die IFC‑Datei externe Ressourcen referenziert, die von `dataDir` aus erreichbar sind.  
- **Pro‑Tipp:** Verwenden Sie `vectorOptions.setBackgroundColor(Color.getWhite())`, wenn Sie einen weißen Hintergrund anstelle des standardmäßigen transparenten PNG benötigen.

## FAQ's

### Q1: Ist Aspose.CAD mit allen Versionen von IFC‑Dateien kompatibel?
A1: Aspose.CAD unterstützt verschiedene Versionen von IFC‑Dateien. Weitere Details finden Sie in der [Dokumentation](https://reference.aspose.com/cad/java/).

### Q2: Kann ich die Rasterisierungsoptionen weiter anpassen?
A2: Absolut! Erkunden Sie die [Dokumentation](https://reference.aspose.com/cad/java/) für erweiterte Anpassungsoptionen.

### Q3: Gibt es eine Testversion?
A3: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Wie bekomme ich eine temporäre Lizenz für Aspose.CAD?
A4: Eine temporäre Lizenz erhalten Sie über [diesen Link](https://purchase.aspose.com/temporary-license/).

### Q5: Wo kann ich Hilfe erhalten oder Themen diskutieren?
A5: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

## Häufig gestellte Fragen

**F: Kann ich diesen Ansatz verwenden, um andere CAD‑Formate zu PNG zu konvertieren?**  
A: Ja, Aspose.CAD unterstützt viele Formate (DWG, DXF, DGN usw.). Ändern Sie einfach die Dateierweiterung und casten Sie zur entsprechenden Bildklasse.

**F: Kann ich eine benutzerdefinierte DPI festlegen?**  
A: Sie können die DPI indirekt steuern, indem Sie `PageWidth`/`PageHeight` im Verhältnis zur gewünschten physischen Größe anpassen.

**F: Ist die PNG‑Ausgabe verlustfrei?**  
A: PNG ist ein verlustfreies Format, sodass das rasterisierte Bild die volle visuelle Treue der Vektordaten beibehält.

## Fazit

Sie haben nun gelernt, wie Sie **IFC zu PNG** effizient mit Aspose.CAD für Java konvertieren. Durch Befolgen dieser Schritte können Sie die IFC‑zu‑PNG‑Konvertierung in jeden Java‑basierten Workflow integrieren, sei es ein Desktop‑Tool, ein serverseitiger Dienst oder eine Cloud‑Funktion.

---

**Zuletzt aktualisiert:** 2026-02-20  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}