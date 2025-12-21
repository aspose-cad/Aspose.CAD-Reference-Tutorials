---
date: 2025-12-21
description: Konvertieren Sie IFC mühelos in PNG mit Aspose.CAD für Java. Folgen Sie
  unserer Schritt‑für‑Schritt‑Anleitung.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: IFC in PNG konvertieren mit Aspose.CAD für Java
url: /de/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC in PNG konvertieren mit Aspose.CAD für Java

## Einleitung

In diesem Tutorial lernen Sie **wie man IFC in PNG konvertiert** mit der leistungsstarken Aspose.CAD-Bibliothek für Java. Egal, ob Sie einen BIM-Viewer erstellen, Thumbnails für ein Bauportal generieren oder Dokumentationspipelines automatisieren, die Konvertierung von IFC (Industry Foundation Classes)-Dateien in Rasterbilder ist ein häufiges Anliegen. Wir gehen jeden Schritt durch, erklären die Gründe für die Einstellungen und geben Ihnen Tipps, um die besten visuellen Ergebnisse zu erzielen.

## Schnelle Antworten
- ** Bibliothek wird benötigt?** Aspose.CAD for Java (kostenlose Testversion verfügbar).  
- **Unterstützte IFC-Versionen?** Die meisten IFC 2x3- und IFC4-Dateien werden verarbeitet.  
- **Typische Konvertierungszeit?** Ein paar Sekunden für Standardmodelle; abhängig von der Dateigröße.  
- **Benötige ich eine Lizenz?** Für Produktionseinsatz ist eine temporäre Lizenz erforderlich.  
- **Kann ich die Bildgröße anpassen?** Ja – verwenden Sie `CadRasterizationOptions`, um Breite und Höhe festzulegen.

## Was bedeutet „IFC in PNG konvertieren“?
IFC in PNG zu konvertieren bedeutet, ein 3‑D-Gebäudemodell (IFC) in ein 2‑D-Bitmap-Bild (PNG) zu rasterisieren. Dieser Vorgang flacht die Geometrie ab, wendet Standard-Visualisierungen an und erzeugt ein portables Bild, das in Browsern, Berichten oder mobilen Apps angezeigt werden kann, ohne dass ein CAD-Viewer erforderlich ist.

## Warum Aspose.CAD für Java verwenden?
- **Keine externe CAD-Software** – reine Java-API, funktioniert auf jeder Plattform.  
- **Hochwertiges Rendering** – bewahrt Linienstärken, Farben und Ebenen.  
- **Vollständige Kontrolle** – Rasterisierungsoptionen ermöglichen die Definition von Auflösung, Hintergrund und mehr.  
- **Einfache Lizenzierung** – Test- und temporäre Lizenzen vereinfachen die Evaluierung.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD-Bibliothek** – herunterladen und installieren Sie sie von dem [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – Version 8 oder höher.  
- **Ein Ordner**, der die IFC-Datei enthält, die Sie konvertieren möchten.

## Namespaces importieren

Importieren Sie in Ihrem Java-Projekt die notwendigen Klassen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: IFC-Datei laden

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Hier laden wir die Quell‑IFC‑Datei in ein `IfcImage`‑Objekt. Aspose.CAD analysiert automatisch die IFC‑Struktur und bereitet sie für die Rasterisierung vor.

### Schritt 2: Vektor‑ (Rasterisierungs‑)Optionen festlegen

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` steuert, wie die 3‑D‑Geometrie abgeflacht wird. Passen Sie `PageWidth` und `PageHeight` an die gewünschte PNG‑Auflösung an. Größere Werte erzeugen detailreichere Bilder, erhöhen jedoch den Speicherverbrauch.

### Schritt 3: PNG-Export‑Einstellungen konfigurieren

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` weist Aspose.CAD an, eine PNG‑Datei auszugeben und verknüpft die im vorherigen Schritt definierten Rasterisierungs‑Einstellungen.

### Schritt 4: Bild als PNG speichern

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Die Methode `save` schreibt das rasterisierte Bild auf die Festplatte. Nach Ausführung dieser Zeile finden Sie `example.png` im selben Verzeichnis wie Ihre Quell‑IFC‑Datei.

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **Leere PNG-Ausgabe** | Rasterisierungsoptionen Breite/Höhe sind auf 0 oder sehr klein gesetzt. | Stellen Sie sicher, dass `PageWidth` und `PageHeight` positive Ganzzahlen sind (z. B. 1500). |
| **Fehlende Ebenen oder Farben** | Standardansicht kann bestimmte Ebenen ausblenden. | Verwenden Sie `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` oder passen Sie die Ebenen‑Sichtbarkeit über die API an (falls nötig). |
| **Out‑of‑Memory‑Fehler** bei riesigen IFC‑Dateien | Sehr hohe Auflösung verbraucht viel RAM. | Reduzieren Sie die Auflösung oder verarbeiten Sie das Modell in Abschnitten. |

## FAQ

### Q1: Ist Aspose.CAD mit allen Versionen von IFC‑Dateien kompatibel?

A1: Aspose.CAD unterstützt verschiedene Versionen von IFC‑Dateien. Weitere Details zur Kompatibilität finden Sie in der [documentation](https://reference.aspose.com/cad/java/).

### Q2: Kann ich die Rasterisierungsoptionen weiter anpassen?

A2: Auf jeden Fall! Erkunden Sie die [documentation](https://reference.aspose.com/cad/java/) für erweiterte Anpassungsoptionen.

### Q3: Gibt es eine Testversion?

A3: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

A4: Holen Sie sich eine temporäre Lizenz über [diesen Link](https://purchase.aspose.com/temporary-license/).

### Q5: Wo kann ich Hilfe erhalten oder Probleme diskutieren?

A5: Besuchen Sie das [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

## Häufig gestellte Fragen (Zusätzlich)

**Q: Kann ich mehrere IFC‑Dateien stapelweise konvertieren?**  
A: Ja. Packen Sie die Lade‑ und Speicherlogik in eine Schleife, die über eine Liste von Dateipfaden iteriert.

**Q: Wie ändere ich die Hintergrundfarbe des PNG?**  
A: Setzen Sie `vectorOptions.setBackgroundColor(Color.getWhite())` (oder jede `java.awt.Color`) bevor Sie `PngOptions` erstellen.

**Q: Ist es möglich, in andere Rasterformate wie JPEG oder BMP zu exportieren?**  
A: Auf jeden Fall. Ersetzen Sie `PngOptions` durch `JpegOptions` oder `BmpOptions` und passen Sie ggf. format‑spezifische Einstellungen an.

**Q: Muss ich nach der Konvertierung Ressourcen freigeben?**  
A: Rufen Sie `cadImage.dispose()` auf, wenn Sie fertig sind, um den nativen Speicher freizugeben.

---

**Zuletzt aktualisiert:** 2025-12-21  
**Getestet mit:** Aspose.CAD for Java 24.12 (zum Zeitpunkt des Schreibens aktuell)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}