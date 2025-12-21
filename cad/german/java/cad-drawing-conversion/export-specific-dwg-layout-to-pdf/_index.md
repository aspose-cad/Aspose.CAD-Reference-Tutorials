---
date: 2025-12-21
description: Erfahren Sie, wie Sie DWG in PDF konvertieren, indem Sie ein bestimmtes
  DWG‑Layout mit Aspose.CAD für Java als PDF exportieren. Folgen Sie diesem Schritt‑für‑Schritt‑DWG‑zu‑PDF‑Tutorial,
  um Ihren CAD‑Workflow zu optimieren.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: DWG in PDF konvertieren – Layout exportieren mit Aspose.CAD für Java
url: /de/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG in PDF konvertieren – Bestimmtes Layout mit Aspose.CAD für Java exportieren

## Einführung

In der dynamischen Welt des Computer‑Aided Design (CAD) ist **DWG in PDF konvertieren** ein häufiges Bedürfnis, wenn Zeichnungen mit Kunden, Auftragnehmern oder nicht‑technischen Stakeholdern geteilt werden. Aspose.CAD für Java macht diese Konvertierung mühelos und ermöglicht es sogar, ein einzelnes Layout aus einer DWG‑Datei mit mehreren Layouts auszuwählen. In diesem Tutorial führen wir Sie Schritt für Schritt durch **den Export von DWG‑spezifischen Layouts nach PDF**, sodass Sie genau das liefern können, was Ihr Projekt benötigt, ohne zusätzliche Seiten oder manuelles Zuschneiden.

## Schnellantworten
- **Was bedeutet „DWG in PDF konvertieren“?** Es wandelt eine DWG‑Zeichnung in ein PDF‑Dokument um und bewahrt dabei Vektordaten und Layout‑Treue.  
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.CAD für Java stellt eine sofort einsatzbereite API bereit.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Ja, eine kommerzielle Lizenz ist erforderlich; eine kostenlose Testversion ist für Evaluierungen verfügbar.  
- **Kann ich ein einzelnes Layout auswählen?** Absolut – setzen Sie die Eigenschaft `Layouts` auf den gewünschten Layout‑Namen.  
- **Welche Java‑Version wird unterstützt?** Java 8 und höher sind vollständig kompatibel.

## Voraussetzungen

Bevor Sie starten, stellen Sie sicher, dass Sie Folgendes haben:

- **Java‑Entwicklungsumgebung** – JDK 8+ und Ihre bevorzugte IDE.  
- **Aspose.CAD‑Bibliothek** – Laden Sie das aktuelle JAR von der offiziellen Seite **[hier](https://releases.aspose.com/cad/java/)** herunter.  
- **DWG‑Datei** – Eine Zeichnung, die mindestens ein Layout enthält (z. B. *visualization_-_conference_room.dwg*).  

## Warum ein bestimmtes DWG‑Layout nach PDF exportieren?

Viele DWG‑Dateien enthalten mehrere Papierbereiche (Layouts). Der Export der gesamten Datei kann ein sperriges PDF mit unerwünschten Seiten erzeugen. Die Auswahl eines einzelnen Layouts:

- Reduziert die Dateigröße.  
- Lenkt die Aufmerksamkeit des Betrachters auf das relevante Zeichenblatt.  
- Entspricht den Dokumentationsstandards des Projekts.  

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Projektumgebung einrichten

Erstellen Sie ein neues Java‑Projekt (Maven, Gradle oder reines IDE‑Projekt) und fügen Sie das Aspose.CAD‑JAR Ihrem Klassenpfad hinzu. Sie können es **[hier](https://releases.aspose.com/cad/java/)** herunterladen.

### Schritt 2: Notwendige Pakete importieren

Fügen Sie die erforderlichen Aspose.CAD‑Namespaces zu Ihrer Java‑Klasse hinzu.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Schritt 3: DWG‑Datei laden

Verweisen Sie auf die DWG, die Sie konvertieren möchten, und laden Sie sie in ein `Image`‑Objekt.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Schritt 4: Rasterisierungsoptionen konfigurieren

Definieren Sie die Seitengröße und – entscheidend – das Layout, das Sie exportieren möchten.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Schritt 5: PDF‑Exportoptionen festlegen

Verknüpfen Sie die Rasterisierungseinstellungen mit dem PDF‑Exporter.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 6: DWG nach PDF exportieren

Speichern Sie das Ergebnis als PDF‑Datei. Die Ausgabe enthält nur **Layout1**, wodurch ein sauberer **DWG in PDF konvertieren** Vorgang erzielt wird.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|-------|----------------|-----|
| **Layout nicht gefunden** | Der Layout‑Name ist falsch geschrieben oder existiert nicht in der DWG. | Verwenden Sie `image.getLayoutNames()`, um verfügbare Layouts aufzulisten, und wählen Sie das richtige aus. |
| **PDF mit niedriger Auflösung** | `PageWidth`/`PageHeight` sind zu klein. | Erhöhen Sie die Abmessungen (z. B. 2000 × 2000) oder setzen Sie `rasterizationOptions.setResolution(300);`. |
| **Lizenz‑Ausnahme** | Ausführung ohne gültige Lizenz in einer Nicht‑Testumgebung. | Laden Sie Ihre Aspose.CAD‑Lizenz, bevor Sie das Bild laden: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Häufig gestellte Fragen

**F1: Kann ich Aspose.CAD für Java mit anderen Java‑basierten CAD‑Bibliotheken verwenden?**  
A: Aspose.CAD für Java ist eine eigenständige Bibliothek, kann aber mit anderen Java‑basierten Bibliotheken für erweiterte Funktionen integriert werden.

**F2: Gibt es Lizenzoptionen für Aspose.CAD?**  
A: Ja, Sie können Lizenzoptionen prüfen und Details zum Kauf **[hier](https://purchase.aspose.com/buy)** einsehen.

**F3: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD?**  
A: Besuchen Sie **[diesen Link](https://purchase.aspose.com/temporary-license/)**, um eine temporäre Lizenz anzufordern.

**F4: Wo finde ich Support für Aspose.CAD?**  
A: Für Fragen oder Unterstützung besuchen Sie das **[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19)**.

**F5: Gibt es eine kostenlose Testversion von Aspose.CAD?**  
A: Ja, Sie können eine kostenlose Testversion **[hier](https://releases.aspose.com/)** nutzen.

## Fazit

Durch Befolgen dieses **DWG‑zu‑PDF‑Tutorials** haben Sie nun eine zuverlässige Methode, **DWG in PDF zu konvertieren**, wobei Sie ein einzelnes Layout anvisieren. Dieser Ansatz spart Speicherplatz, beschleunigt den Dokumentenaustausch und hält Ihren CAD‑Workflow übersichtlich. Experimentieren Sie gern mit verschiedenen Rasterisierungs‑Einstellungen oder kombinieren Sie mehrere Layouts zu einem einzigen PDF, wenn Ihr Projekt dies erfordert.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2025-12-21  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose