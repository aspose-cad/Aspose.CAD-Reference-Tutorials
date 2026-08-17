---
date: 2026-02-20
description: Erfahren Sie, wie Sie AutoCAD‑PDF mit Aspose.CAD für Java exportieren.
  Diese Schritt‑für‑Schritt‑Anleitung zeigt Ihnen, wie Sie **DWG in PDF konvertieren**,
  **CAD als PDF speichern** und die Lizenzierung handhaben.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: DWG in PDF konvertieren – AutoCAD‑Bilder mit Aspose.CAD für Java in PDF exportieren
url: /de/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - AutoCAD-Bilder nach PDF exportieren mit Aspose.CAD für Java

## Einleitung

Suchen Sie nach einer Möglichkeit, **DWG in PDF** mit Java zu konvertieren? Dann sind Sie hier genau richtig! In diesem Tutorial führen wir Sie durch die Konvertierung von AutoCAD-Bildern zu PDF mit Aspose.CAD für Java, einer leistungsstarken Bibliothek, die den **DWG‑zu‑PDF‑Konvertierungsprozess** mühelos macht. Am Ende verstehen Sie, wie Sie **CAD als PDF speichern**, benutzerdefinierte Rasterisierungs‑Einstellungen anwenden und eine Aspose.CAD‑Lizenz für den Produktionseinsatz verwenden.

## Schnelle Antworten
- **Kann ich DWG mit Java in PDF konvertieren?** Ja, Aspose.CAD für Java verarbeitet DWG, DXF und viele andere Formate.  
- **Benötige ich eine Lizenz?** Eine **Aspose CAD‑Lizenz** ist für uneingeschränkte Nutzung erforderlich; eine temporäre Lizenz steht für Evaluierungszwecke zur Verfügung.  
- **Welche Java‑Version wird unterstützt?** Java 8+ (die Bibliothek ist mit allen modernen JDKs kompatibel).  
- **Kann ich die PDF‑Seitengröße anpassen?** Absolut – passen Sie `pageWidth` und `pageHeight` in den Rasterisierungsoptionen an.  
- **Ist 3‑D‑Rasterisierung möglich?** Ja, aktivieren Sie `TypeOfEntities.Entities3D` für vollständiges 3‑D‑Rendering.

## Was ist **export autocad pdf**?
Das Exportieren von AutoCAD PDF bedeutet, vektorbasierte CAD‑Zeichnungen (DWG, DXF, DWF usw.) in ein portables PDF‑Dokument zu konvertieren, wobei Ebenen, Linienstärken und optional 3‑D‑Geometrie erhalten bleiben. Dies ist nützlich, um Designs mit Kunden zu teilen, zu archivieren oder zu drucken, ohne CAD‑Software zu benötigen.

## Warum DWG mit Aspose.CAD für Java in PDF konvertieren?
- **Vollständige Formatunterstützung** – funktioniert mit DWG, DXF, DWF und vielen weiteren.  
- **Keine externen Abhängigkeiten** – reine Java‑Bibliothek, keine nativen DLLs.  
- **Hochwertige Rasterisierung** – Kontrolle über DPI, Seitengröße und Layout, sodass Sie **die PDF‑Seitengröße** an die Anforderungen Ihres Projekts anpassen können.  
- **Lizenzflexibilität** – beginnen Sie mit einer kostenlosen Testversion und wechseln Sie dann zu einer permanenten **Aspose CAD‑Lizenz**.  

## Voraussetzungen

Bevor Sie starten, stellen Sie sicher, dass Sie Folgendes haben:

- **Java Development Environment** – JDK 8 oder höher installiert.  
- **Aspose.CAD for Java Library** – herunterladen von dem [Download-Link](https://releases.aspose.com/cad/java/).  
- **Document Directory** – ein Ordner auf Ihrem Rechner, in dem die Quell‑CAD‑Dateien und die erzeugten PDFs abgelegt werden.

## Namespaces importieren

In Ihrem Java‑Projekt importieren Sie die notwendigen Klassen, um mit Aspose.CAD zu arbeiten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Jetzt gehen wir den Code Schritt für Schritt durch.

## Wie man DWG mit Aspose.CAD für Java in PDF konvertiert

### Schritt 1: Pfad zum Ressourcenverzeichnis festlegen

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Profi‑Tipp:** Ersetzen Sie `"Your Document Directory"` durch den absoluten Pfad zu dem Ordner, den Sie in den Voraussetzungen erstellt haben.

### Schritt 2: CAD‑Bild laden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Warum das wichtig ist:** Das Laden der CAD‑Datei in ein `Image`‑Objekt gibt Ihnen vollen Zugriff auf die Rasterisierungs‑Engine von Aspose.CAD.

### Schritt 3: Rasterisierungsoptionen festlegen

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Passen Sie `pageWidth` und `pageHeight` an, um **die PDF‑Seitengröße** anzupassen.  
- Entkommentieren Sie die Zeile `setTypeOfEntities`, wenn Sie **java convert cad pdf** für 3‑D‑Entitäten benötigen.  
- Der Aufruf `setLayouts` wählt aus, welches Layout (Model, Layout1 usw.) gerendert werden soll.

### Schritt 4: PDF‑Optionen konfigurieren

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Dies verknüpft die Rasterisierungseinstellungen mit der PDF‑Ausgabe und stellt sicher, dass die Vektordaten korrekt konvertiert werden.

### Schritt 5: PDF speichern

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Die resultierende Datei, `Export3DImagestoPDF_out_.pdf`, ist eine **save cad as pdf**‑Darstellung Ihrer ursprünglichen AutoCAD‑Zeichnung.

## Häufige Probleme & Lösungen

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| Leere PDF-Ausgabe | Rasterisierungsoptionen nicht gesetzt oder Layout stimmt nicht überein | Stellen Sie sicher, dass `setLayouts` dem Layoutnamen in Ihrer CAD‑Datei entspricht. |
| Bild mit niedriger Auflösung | `pageWidth`/`pageHeight` zu klein | Erhöhen Sie die Abmessungen oder setzen Sie eine höhere DPI über `rasterizationOptions.setResolution(...)`. |
| Lizenzausnahme | Keine gültige Lizenz angewendet | Wenden Sie eine **Aspose CAD‑Lizenz** an oder verwenden Sie eine temporäre Lizenz für Tests. |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?
A1: Ja, Aspose.CAD unterstützt eine Vielzahl von Formaten, darunter DWG, DWF, DGN und mehr, und bietet Ihnen Flexibilität in Ihren Projekten.

### Q2: Wie kann ich eine temporäre Lizenz für Aspose.CAD für Java erhalten?
A2: Besuchen Sie [hier](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz für die Evaluierung zu erhalten.

### Q3: Gibt es Layout‑Optionen für die Rasterisierung?
A3: Ja, Sie können Layouts (z. B. `"Model"`, `"Layout1"`) über die Methode `setLayouts` anpassen, um zu steuern, welche Ansicht gerendert wird.

### Q4: Kann ich die Größe der Ausgabedatei PDF anpassen?
A4: Absolut! Passen Sie die Parameter `pageWidth` und `pageHeight` in den Rasterisierungsoptionen an, um die gewünschten Abmessungen zu erreichen.

### Q5: Wo kann ich Hilfe erhalten oder Probleme im Zusammenhang mit Aspose.CAD für Java diskutieren?
A5: Besuchen Sie das [Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für dedizierten Support und Community‑Diskussionen.

---

**Zuletzt aktualisiert:** 2026-02-20  
**Getestet mit:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}