---
date: 2026-01-12
description: Erfahren Sie, wie Sie CAD in PDF exportieren und dabei die automatische
  Codepage-Erkennung in DWG-Dateien mit Aspose.CAD für Java überschreiben. Unterstützt
  die Kodierung und fehlerhafte CIF/MIF.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: CAD nach PDF exportieren – Automatische Codepage-Erkennung in DWG‑Dateien mit
  Java überschreiben
url: /de/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD nach PDF exportieren – Automatische Codepage-Erkennung in DWG-Dateien mit Java überschreiben

## Einleitung

In diesem umfassenden Leitfaden erfahren Sie **wie Sie CAD nach PDF exportieren** und dabei die automatische Codepage-Erkennung überschreiben, die Text in DWG-Dateien beschädigen kann. Aspose.CAD für Java bietet Ihnen eine feinkörnige Kontrolle über die Kodierung, sodass Sie fehlerhafte CIF/MIF-Daten wiederherstellen und zuverlässige PDF-Ausgaben erzeugen können. Egal, ob Sie einen Batch-Konverter erstellen oder die CAD-Verarbeitung in eine größere Java-Anwendung integrieren, die nachfolgenden Schritte führen Sie durch den gesamten Arbeitsablauf.

## Schnelle Antworten
- **Was bedeutet „override code page“?** Es zwingt Aspose.CAD, eine bestimmte Zeichenkodierung zu verwenden, anstatt zu raten.
- **Kann ich DWG direkt nach PDF exportieren?** Ja – nach dem Festlegen der korrekten Codepage können Sie das CAD‑Bild als PDF speichern.
- **Welche Kodierung funktioniert für japanischen Text?** `CodePages.Japanese` und `MifCodePages.Japanese` sind die richtigen Optionen.
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Eine kommerzielle Lizenz ist erforderlich; eine temporäre Lizenz ist für Tests verfügbar.
- **Welche Version von Aspose.CAD wird benötigt?** Jede aktuelle Version, die `LoadOptions` und `PdfOptions` unterstützt.

## Was bedeutet „CAD nach PDF exportieren“?
Das Exportieren von CAD nach PDF konvertiert vektorbasierte CAD‑Zeichnungen in ein weit verbreitetes, festes Layout‑Dokumentformat. Das resultierende PDF bewahrt Linien, Ebenen und Text, während die Zeichnung leicht zu teilen, zu drucken oder in andere Anwendungen einzubetten ist.

## Warum die automatische Codepage-Erkennung überschreiben?
DWG‑Dateien speichern Text häufig mit veralteten Codepages. Die Auto‑Erkennung von Aspose.CAD kann diese Bytes missinterpretieren, was zu fehlerhaften Zeichen führt. Durch die manuelle Angabe der Codepage stellen Sie sicher, dass der Text im exportierten PDF exakt wie beabsichtigt erscheint, insbesondere bei nicht‑lateinischen Schriften wie Japanisch, Kyrillisch oder Arabisch.

## Voraussetzungen
- **Java-Entwicklungsumgebung** – JDK 8+ und Ihre bevorzugte IDE.
- **Aspose.CAD für Java** – Laden Sie die Bibliothek von der offiziellen Seite [hier](https://releases.aspose.com/cad/java/).
- **DWG-Beispieldatei** – Verwenden Sie die bereitgestellte `SimpleEntities.dwg` oder jede DWG, die Sie konvertieren möchten.

## Pakete importieren
In Ihrem Java‑Projekt importieren Sie die erforderlichen Aspose.CAD‑Klassen:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Java‑Projekt einrichten
Erstellen Sie ein neues Maven‑ oder Gradle‑Projekt und fügen Sie das Aspose.CAD‑JAR dem Klassenpfad hinzu. Dieser Schritt stellt sicher, dass die IDE die importierten Klassen auflösen kann.

### Schritt 2: DWG‑Datei mit einer angegebenen Codepage laden
Teilen Sie Aspose.CAD mit, welche Kodierung verwendet werden soll und ob versucht werden soll, fehlerhafte CIF/MIF‑Daten wiederherzustellen.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Schritt 3: CAD‑Bild nach PDF exportieren
Mit der korrekt angewendeten Codepage können Sie die Zeichnung sicher exportieren. Das `PdfOptions`‑Objekt ermöglicht Ihnen, die PDF‑Ausgabe (Kompression, Rasterung usw.) fein abzustimmen.

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Schritt 4: Erfolg überprüfen
Eine einfache Konsolennachricht bestätigt, dass der Vorgang ohne Ausnahmen abgeschlossen wurde.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Sie können diese Schritte für mehrere DWG‑Dateien wiederholen und dabei den Quellpfad sowie den Ausgabename nach Bedarf anpassen.

## Häufige Probleme & Lösungen
- **Garbage‑Zeichen erscheinen weiterhin:** Überprüfen Sie, ob `specifiedEncoding` mit der ursprünglichen Codepage der DWG übereinstimmt. Verwenden Sie bei Bedarf ein anderes `CodePages`‑Enum.
- **`NullPointerException` bei `cadImage.save`:** Stellen Sie sicher, dass die DWG‑Datei korrekt geladen wird; prüfen Sie Pfad und Dateiberechtigungen.
- **PDF‑Größe ist groß:** Aktivieren Sie die Kompression in `PdfOptions` (z. B. `pdfOptions.setCompress(true)`).

## Häufig gestellte Fragen

**Q1: Ist Aspose.CAD mit allen Versionen von DWG‑Dateien kompatibel?**  
A1: Aspose.CAD unterstützt eine breite Palette von DWG‑Versionen, einschließlich AutoCAD 2018 und früheren Releases.

**Q2: Kann ich Aspose.CAD für kommerzielle Projekte verwenden?**  
A2: Ja, für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich. Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erhalten.

**Q3: Gibt es Einschränkungen in der kostenlosen Testversion?**  
A3: Die Testversion hat Größen‑ und Funktionsbeschränkungen; konsultieren Sie die offizielle Dokumentation für Details.

**Q4: Wie kann ich Support für Aspose.CAD erhalten?**  
A4: Besuchen Sie die Community‑[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Unterstützung und Diskussionen.

**Q5: Gibt es eine temporäre Lizenz für Testzwecke?**  
A5: Ja, eine temporäre Lizenz kann [hier](https://purchase.aspose.com/temporary-license/) angefordert werden.

**Zuletzt aktualisiert:** 2026-01-12  
**Getestet mit:** Aspose.CAD für Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}