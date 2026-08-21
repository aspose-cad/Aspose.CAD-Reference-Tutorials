---
date: 2026-05-04
description: Erfahren Sie, wie Sie CAD‑PDF‑Dateien konvertieren, indem Sie DGN mit
  Aspose.CAD für Java in AutoCAD‑PDF exportieren. Schritt‑für‑Schritt‑Anleitung mit
  anpassbarer PDF‑Größe und Optionen.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Exportieren von DGN im AutoCAD-Format als PDF
second_title: Aspose.CAD Java API
title: CAD-PDF konvertieren – mühelose DGN‑zu‑AutoCAD‑PDF‑Export mit Aspose.CAD für
  Java
url: /de/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD PDF konvertieren: Mühelose DGN‑zu‑AutoCAD‑PDF‑Export mit Aspose.CAD für Java

## Einführung

Wenn Sie **CAD PDF**‑Dateien direkt aus DGN‑Quellen konvertieren müssen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie Schritt für Schritt durch die Verwendung von Aspose.CAD für Java, um DGN‑Dateien in ein AutoCAD‑kompatibles PDF zu exportieren. Sie sehen, wie Sie benutzerdefinierte Seitengrößen festlegen, bestimmte Layouts auswählen und die PDF‑Ausgabe feinabstimmen – alles mit klaren, schrittweisen Code‑Beispielen, die Sie in Ihr eigenes Projekt übernehmen können.

## Schnelle Antworten
- **Was bedeutet „convert CAD PDF“?** Es bezeichnet die Umwandlung von CAD‑Quelldateien (wie DGN) in ein PDF, das Vektordaten und Layout‑Treue bewahrt.  
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.CAD für Java bietet dafür eine zuverlässige, lizenz‑freie Testversion.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich die PDF‑Größe anpassen?** Ja – die `CadRasterizationOptions` ermöglichen das Festlegen von Seitenbreite, -höhe und Skalierung.  
- **Wie viele Code‑Zeilen werden benötigt?** Weniger als 20 Zeilen Java‑Code zum Laden, Konfigurieren und Speichern des PDFs.

## Was bedeutet „convert CAD PDF“?
„CAD PDF konvertieren“ bedeutet, eine native CAD‑Zeichnung (z. B. DGN) zu nehmen und ein PDF zu erzeugen, das die ursprünglichen Vektorgrafiken, Ebenen und Layout‑Informationen beibehält. Das resultierende PDF kann auf jedem Gerät angezeigt werden, ohne dass CAD‑Software nötig ist – ideal zum Teilen, Drucken oder Archivieren.

## Warum Aspose.CAD für Java zum Konvertieren von CAD PDF verwenden?
- **Umfassende Formatunterstützung** – DGN, DWG, DXF und viele weitere.  
- **Keine externen Abhängigkeiten** – reines Java, keine nativen DLLs.  
- **Fein abgestimmte Kontrolle** – Sie können wählen, welche Layouts exportiert werden, benutzerdefinierte Seitengrößen festlegen und die Rasterisierungsqualität steuern.  
- **Skalierbar für Batch‑Jobs** – Laden und speichern Sie Dutzende von Dateien in einer Schleife mit minimalem Aufwand.

## Voraussetzungen
Bevor wir starten, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD Bibliothek** – laden Sie sie [hier](https://releases.aspose.com/cad/java/) herunter.  
- **Dokumenten‑Verzeichnis** – ein Ordner auf Ihrem Rechner, in dem die Eingabe‑DGN‑Dateien und die Ausgabe‑PDFs abgelegt werden.

## Pakete importieren

Importieren Sie in Ihrem Java‑Projekt die notwendigen Pakete, um auf die Aspose.CAD‑Funktionalitäten zuzugreifen:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nun zerlegen wir den Beispielcode in mehrere Schritte:

## Schritt 1: Dateipfade definieren (wie man DGN exportiert)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Pfad, in dem Ihre Dateien liegen.

## Schritt 2: DGN‑Bild laden

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Laden Sie die DGN‑Datei mit Aspose.CAD.

## Schritt 3: PDF‑Exportoptionen festlegen (PDF‑Größe anpassen, PDF‑Optionen setzen)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Hier definieren wir die PDF‑Exportoptionen, einschließlich Seitengröße, automatischer Skalierung und den spezifischen DGN‑Layouts (Views), die Sie in das finale PDF aufnehmen möchten.

## Schritt 4: PDF‑Datei speichern

```java
objImage.save(outFile, options);
```

Speichern Sie die exportierte PDF‑Datei. Die `save`‑Methode wendet alle Optionen an, die Sie im vorherigen Schritt konfiguriert haben.

Wiederholen Sie diese Schritte für weitere DGN‑Dateien, die Sie konvertieren möchten. Herzlichen Glückwunsch! Sie haben erfolgreich **CAD PDF konvertiert**, indem Sie DGN‑Dateien mit Aspose.CAD für Java in das AutoCAD‑PDF‑Format exportiert haben.

## Häufige Probleme und Lösungen
| Problem | Warum es passiert | Lösung |
|-------|----------------|-----|
| **Datei nicht gefunden** | Falscher `dataDir`‑Pfad | Überprüfen Sie den Ordnerpfad und stellen Sie sicher, dass die DGN‑Datei existiert. |
| **Leere Seiten im PDF** | `AutomaticLayoutsScaling` ist auf `false` gesetzt oder Layout‑IDs fehlen | Lassen Sie `setAutomaticLayoutsScaling(true)` und prüfen Sie die Layout‑Namen (`"1","2",…`). |
| **Ausgabe mit niedriger Auflösung** | Standard‑Rasterisierungs‑DPI ist zu niedrig | Verwenden Sie `vectorOptions.setResolution(300);` um die Qualität zu erhöhen (vor `setVectorRasterizationOptions` einfügen). |
| **Lizenz‑Ausnahme** | Keine gültige Lizenz im Produktionseinsatz | Laden Sie eine temporäre oder gekaufte Lizenz gemäß der Aspose‑Dokumentation. |

## Häufig gestellte Fragen (Zusätzlich)

**F: Kann ich nur ein einzelnes Layout aus einer DGN‑Datei mit mehreren Layouts exportieren?**  
A: Ja – geben Sie die gewünschten Layout‑IDs in `vectorOptions.setLayouts(new String[] { "2" });` an.

**F: Ist es möglich, Schriftarten im resultierenden PDF einzubetten?**  
A: Aspose.CAD bettet die notwendigen Schriftarten automatisch ein, wenn Vektordaten gerastert werden; Sie können das Einbetten über `PdfOptions` ebenfalls steuern.

**F: Wie verarbeite ich viele DGN‑Dateien in einem Batch?**  
A: Verpacken Sie die Schritte in eine `for`‑Schleife, die über eine Liste von Dateinamen iteriert, und verwenden Sie dieselbe `PdfOptions`‑Instanz für jede Iteration.

**F: Unterstützt die Bibliothek passwortgeschützte PDFs?**  
A: Ja – Sie können ein Passwort auf dem `PdfOptions`‑Objekt setzen via `options.setPassword("yourPassword");`.

**F: Wo finde ich weitere Beispiele?**  
A: Die offizielle Aspose.CAD‑Dokumentation und das Beispiel‑Repository enthalten viele zusätzliche Szenarien.

## FAQ's (Original)

### Q1: Ist Aspose.CAD mit allen CAD‑Dateiformaten kompatibel?

A1: Ja, Aspose.CAD unterstützt eine breite Palette von CAD‑Formaten und bietet damit Vielseitigkeit beim Umgang mit verschiedenen Dateitypen.

### Q2: Kann ich die PDF‑Export‑Einstellungen anpassen?

A2: Absolut. Wie im Tutorial gezeigt, können Sie Optionen wie Seitengröße und Layouts nach Ihren Anforderungen anpassen.

### Q3: Wo finde ich zusätzlichen Support oder Hilfe?

A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

### Q4: Gibt es eine kostenlose Testversion?

A4: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q5: Wie erhalte ich eine temporäre Lizenz?

A5: Holen Sie sich eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/).

## Fazit

In diesem Tutorial haben wir gezeigt, wie man **CAD PDF**‑Dateien mithilfe von Aspose.CAD für Java konvertiert. Mit nur wenigen Code‑Zeilen können Sie eine DGN‑Zeichnung laden, die PDF‑Exportoptionen feinjustieren und hochwertige PDFs erzeugen, die sich zum Teilen oder Archivieren eignen. Experimentieren Sie gern mit verschiedenen Seitengrößen, Layouts oder Batch‑Verarbeitung, um die Lösung an die Bedürfnisse Ihres Projekts anzupassen.

---

**Zuletzt aktualisiert:** 2026-05-04  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}