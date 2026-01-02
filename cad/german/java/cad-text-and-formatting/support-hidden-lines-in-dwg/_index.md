---
date: 2026-01-02
description: Erfahren Sie, wie Sie DWG als PDF exportieren, versteckte Linien aktivieren
  und DWG mit Aspose.CAD für Java in PDF konvertieren – in diesem Schritt‑für‑Schritt‑Tutorial.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: DWG als PDF mit versteckten Linien exportieren – Aspose.CAD für Java
url: /de/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG als PDF mit verdeckten Linien exportieren – Aspose.CAD für Java

## Introduction

In diesem Tutorial lernen Sie, wie Sie **DWG als PDF exportieren** und dabei versteckte Linien mit Aspose.CAD für Java beibehalten. Ob Sie **DWG in PDF konvertieren**, einen **DWG‑zu‑PDF‑Tutorial‑Stil‑Leitfaden** erstellen oder einfach **DWG als PDF speichern** mit Unterstützung für versteckte Linien benötigen, wir führen Sie durch jeden Schritt. Am Ende haben Sie eine einsatzbereite Lösung, die Sie in jedes Java‑Projekt einbinden können.

## Quick Answers
- **Worum geht es in diesem Tutorial?** Aktivieren der versteckten Liniendarstellung beim Export von DWG nach PDF mit Aspose.CAD für Java.  
- **Welche Hauptoperation wird ausgeführt?** `export dwg as pdf`.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Was sind die Voraussetzungen?** Java-Entwicklungsumgebung, Aspose.CAD für Java Bibliothek und DWG‑Dateien.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für eine Grundkonfiguration.

## What is “export dwg as pdf”?

Das Exportieren einer DWG‑Datei nach PDF konvertiert die vektorbasierte CAD‑Zeichnung in ein Portable Document Format, wobei Ebenen, Linientypen und optional die Darstellung versteckter Linien beibehalten werden. Dadurch lässt sich das CAD‑Design leicht mit Stakeholdern teilen, die keine CAD‑Software besitzen.

## Why enable hidden lines when exporting?

Versteckte Linien bieten eine klarere visuelle Darstellung komplexer 3D‑Modelle auf einer 2‑D‑Seite, indem nur sichtbare Kanten hervorgehoben werden. Dies verbessert die Lesbarkeit und ist häufig für technische Dokumentationen erforderlich.

## Prerequisites

1. **Aspose.CAD für Java** – Laden Sie die Bibliothek von der offiziellen Seite [hier](https://releases.aspose.com/cad/java/) herunter.  
2. **DWG‑Dateien** – Haben Sie die Quell‑DWG‑Zeichnungen in einem bekannten Verzeichnis gespeichert.  
3. **Java‑Entwicklungsumgebung** – JDK 8+ und Ihre bevorzugte IDE (Eclipse, IntelliJ usw.).  

Jetzt, da Sie eingerichtet sind, tauchen wir in den Code ein.

## Import Namespaces

Beginnen Sie damit, die erforderlichen Klassen zu importieren, damit Sie mit CAD‑Bildern und PDF‑Optionen arbeiten können.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

Erstellen Sie ein Java‑Projekt und fügen Sie das Aspose.CAD‑JAR zu Ihrem Build‑Pfad hinzu. Definieren Sie anschließend das Verzeichnis, das Ihre DWG‑Dateien enthält.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro‑Tipp:** Verwenden Sie einen absoluten Pfad oder konfigurieren Sie einen relativen Pfad basierend auf dem Ressourcen‑Ordner Ihres Projekts.

## Step 2: Load DWG File

Laden Sie die Quell‑DWG‑Datei in ein `CadImage`‑Objekt, damit Sie sie manipulieren können.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

Wählen Sie die Ebenen aus, die Sie einbeziehen möchten, und stellen Sie die Seitengröße so ein, dass sie dem Originalzeichnung entspricht. Hier aktivieren wir die Darstellung versteckter Linien, indem wir das Layout festlegen.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

Weisen Sie Aspose.CAD an, die Vektordaten in ein PDF zu rasterisieren, wobei das Layout „Model“ verwendet wird, um versteckte Linien verborgen zu halten.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

Exportieren Sie schließlich die DWG‑Datei als PDF. Die versteckten Linien werden gemäß dem von Ihnen festgelegten Layout berücksichtigt.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Häufiger Fehler:** Wenn Sie vergessen, das Layout auf `"Model"` zu setzen, erscheinen alle Linien (einschließlich versteckter) im PDF durchgehend.

## Conclusion

Sie haben nun eine vollständige, produktionsreife Methode, um **DWG als PDF** mit Unterstützung für versteckte Linien mithilfe von Aspose.CAD für Java zu **exportieren**. Dieser Ansatz kann in Batch‑Verarbeitungstools, Web‑Services oder Desktop‑Anwendungen integriert werden, um die CAD‑zu‑PDF‑Konvertierung zu automatisieren.

## Frequently Asked Questions

### Q1: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?
A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate wie DWG, DXF, DWF und mehr.

### Q2: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?
A2: Ja, Sie finden die kostenlose Testversion [hier](https://releases.aspose.com/).

### Q3: Wie erhalte ich Support für Aspose.CAD für Java?
A3: Besuchen Sie das Aspose.CAD‑Forum [hier](https://forum.aspose.com/c/cad/19) für Community‑Support.

### Q4: Wo finde ich ausführliche Dokumentation für Aspose.CAD für Java?
A4: Siehe die Dokumentation [hier](https://reference.aspose.com/cad/java/).

### Q5: Kann ich eine temporäre Lizenz für Aspose.CAD für Java erwerben?
A5: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q6: Funktioniert diese Methode auch für die Konvertierung von DWG zu PDF in einer headless Server‑Umgebung?
A6: Absolut. Da der Code ausschließlich die Aspose.CAD‑API verwendet, läuft er ohne UI‑Abhängigkeiten und ist ideal für serverseitige Automatisierung.

---

**Zuletzt aktualisiert:** 2026-01-02  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}