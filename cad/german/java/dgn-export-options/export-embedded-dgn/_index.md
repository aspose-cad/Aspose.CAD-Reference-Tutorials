---
date: 2026-01-07
description: Erfahren Sie, wie Sie CAD in PDF exportieren und DGN in PDF konvertieren
  mit Aspose.CAD für Java. Schritt‑für‑Schritt‑Anleitung für Java‑Entwickler.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CAD nach PDF exportieren – Eingebettetes DGN mit Aspose.CAD für Java exportieren
url: /de/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD nach PDF exportieren – Eingebettetes DGN mit Aspose.CAD für Java exportieren

## Einführung

In diesem Tutorial erfahren Sie **wie man CAD nach PDF exportiert**, indem Sie eine eingebettete DGN‑Datei in ein hochqualitatives PDF‑Dokument mit Aspose.CAD für Java konvertieren. Aspose.CAD ist eine robuste Bibliothek, die Java‑Entwicklern die volle Kontrolle über die CAD‑Dateimanipulation gibt, egal ob Sie **DGN nach PDF konvertieren**, **DWG nach PDF konvertieren** oder CAD‑Zeichnungen einfach in anderen Formaten rendern möchten. Folgen Sie der nachstehenden Schritt‑für‑Schritt‑Anleitung, und Sie können diese Fähigkeit in wenigen Minuten in Ihre Anwendungen integrieren.

## Schnelle Antworten
- **Was bedeutet „CAD nach PDF exportieren“?** Es konvertiert CAD‑Zeichnungen (DWG, DGN usw.) in PDF‑Dateien und bewahrt dabei die Vektorqualität.  
- **Welche Bibliothek wird verwendet?** Aspose.CAD für Java.  
- **Benötige ich eine Lizenz?** Für den Produktionseinsatz ist eine Lizenz erforderlich; ein kostenloser Test ist verfügbar.  
- **Was sind die wichtigsten Voraussetzungen?** Java‑Entwicklungsumgebung und das Aspose.CAD für Java‑JAR.  
- **Kann ich die Ausgabe anpassen?** Ja – Sie können Layouts auswählen, Rasterisierungsoptionen festlegen und PDF‑Einstellungen steuern.

## Was bedeutet „CAD nach PDF exportieren“?
Das Exportieren von CAD nach PDF bedeutet, dass eine native CAD‑Datei (wie DWG oder DGN) genommen und ein PDF‑Dokument erzeugt wird, das die ursprüngliche Geometrie getreu wiedergeben kann. Das PDF kann auf jeder Plattform angezeigt werden, ohne dass CAD‑Software nötig ist, was es ideal zum Teilen, Drucken oder Archivieren macht.

## Warum Aspose.CAD für Java zum Konvertieren von DGN nach PDF verwenden?
- **Keine externen Abhängigkeiten** – funktioniert rein in Java.  
- **Erhält Vektordaten** – PDFs bleiben bei jeder Vergrößerung scharf.  
- **Feinkörnige Kontrolle** – wählen Sie bestimmte Layouts, setzen Sie die Rasterisierungs‑DPI und betten Sie Schriftarten ein.  
- **Unternehmensbereit** – unterstützt große Dateien, Batch‑Verarbeitung und Lizenzoptionen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java‑Entwicklungsumgebung** – JDK 8 oder höher installiert und konfiguriert.  
- **Aspose.CAD für Java** – laden Sie das neueste JAR von [hier](https://releases.aspose.com/cad/java/) herunter.  

## Pakete importieren

Um loszulegen, müssen Sie die erforderlichen Klassen in Ihrem Java‑Projekt importieren. Fügen Sie die folgenden Import‑Anweisungen zu Ihrer Quelldatei hinzu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Wie exportiere ich DGN nach PDF mit Aspose.CAD für Java?

Im Folgenden finden Sie eine klare, nummerierte Anleitung, die genau zeigt, wie Sie eine eingebettete DGN‑Datei (innerhalb einer DWG) in ein PDF konvertieren.

### Schritt 1: Eingabe‑ und Ausgabepfade festlegen

Definieren Sie das Verzeichnis, das Ihre Quelldatei enthält, und geben Sie die DWG an, die das eingebettete DGN enthält.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Schritt 2: DWG‑Datei laden

Laden Sie die DWG‑Datei in ein `Image`‑Objekt. Aspose.CAD erkennt automatisch eingebettete DGN‑Daten.

```java
Image objImage = Image.load(fileName);
```

### Schritt 3: Rasterisierungsoptionen konfigurieren

Wählen Sie aus, welche Layout(s) Sie in das PDF aufnehmen möchten. In diesem Beispiel exportieren wir nur das **Model**‑Layout.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Schritt 4: PDF‑Optionen konfigurieren

Binden Sie die Rasterisierungseinstellungen in die PDF‑Export‑Optionen ein.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 5: PDF‑Datei speichern

Schreiben Sie schließlich das PDF mit den konfigurierten Optionen auf die Festplatte.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG nach PDF konvertieren – ein zusätzlicher Hinweis

Wenn Ihre Quelldatei eine reine DWG ist (ohne eingebettetes DGN), können Sie denselben Code wiederverwenden – ändern Sie einfach den `fileName`, sodass er auf die DWG verweist, die Sie konvertieren möchten. Die Rasterisierungs‑ und PDF‑Optionen bleiben identisch, sodass Sie einen konsistenten **DWG nach PDF konvertieren**‑Workflow erhalten.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| **Leeres PDF‑Ergebnis** | Layout‑Name stimmt nicht überein | Stellen Sie sicher, dass der an `setLayouts` übergebene Layout‑Name exakt dem Layout in der Quelldatei entspricht (Groß‑/Kleinschreibung beachten). |
| **Lizenz‑Ausnahme** | Verwendung der Testversion ohne Lizenz | Wenden Sie eine gültige Aspose.CAD‑Lizenz an, bevor Sie das Bild laden (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Datei nicht gefunden** | Falscher `dataDir`‑Pfad | Verwenden Sie einen absoluten Pfad oder stellen Sie sicher, dass der relative Pfad korrekt zum Arbeitsverzeichnis des Projekts ist. |
| **Grafiken mit niedriger Auflösung** | Standard‑Rasterisierungs‑DPI ist niedrig | Setzen Sie `rasterizationOptions.setPageWidth/Height` oder `setResolution`, um die DPI zu erhöhen. |

## Häufig gestellte Fragen

**Q: Ist die Nutzung von Aspose.CAD für Java in einem kommerziellen Projekt erlaubt?**  
A: Ja, Aspose.CAD für Java ist eine kommerzielle Bibliothek. Sie können eine Lizenz von [hier](https://purchase.aspose.com/buy) erhalten.

**Q: Gibt es eine kostenlose Testversion?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.CAD für Java [hier](https://releases.aspose.com/) erhalten.

**Q: Wie kann ich Support für Aspose.CAD für Java erhalten?**  
A: Sie können Unterstützung von der Aspose.CAD‑Community im [Forum](https://forum.aspose.com/c/cad/19) erhalten.

**Q: Was, wenn ich eine temporäre Lizenz benötige?**  
A: Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**Q: Wo finde ich die Dokumentation?**  
A: Die Dokumentation ist [hier](https://reference.aspose.com/cad/java/) verfügbar.

## Fazit

Sie haben nun gelernt, **wie man CAD nach PDF exportiert**, insbesondere **wie man DGN nach PDF konvertiert** und sogar **wie man DWG nach PDF konvertiert** mit Aspose.CAD für Java. Durch Befolgen der obigen Schritte können Sie nahtlose CAD‑zu‑PDF‑Konvertierung in jede Java‑basierte Lösung integrieren und Ihren Benutzern hochwertige PDFs bereitstellen, ohne zusätzliche CAD‑Software zu benötigen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-01-07  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose