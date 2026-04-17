---
date: 2026-03-05
description: Erfahren Sie, wie Sie DWG nach PDF exportieren, versteckte Linien aktivieren
  und DWG mit Aspose.CAD für Java in PDF konvertieren – in diesem Schritt‑für‑Schritt‑Tutorial.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: DWG in PDF mit versteckten Linien exportieren – Aspose.CAD für Java
url: /de/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG nach PDF mit versteckten Linien exportieren – Aspose.CAD für Java

## Einführung

In diesem Tutorial lernen Sie, wie Sie **DWG nach PDF** exportieren und dabei versteckte Linien mit Aspose.CAD für Java beibehalten. Egal, ob Sie **DWG zu PDF konvertieren**, einen **DWG‑zu‑PDF‑Tutorial‑Stil‑Leitfaden** erstellen oder einfach **DWG als PDF** mit Unterstützung für versteckte Linien speichern möchten, wir führen Sie durch jeden Schritt. Am Ende haben Sie eine einsatzbereite Lösung, die Sie in jedes Java‑Projekt einbinden können.

## Schnellantworten
- **Was behandelt dieses Tutorial?** Aktivierung der versteckten Linien‑Darstellung beim Export von DWG nach PDF mit Aspose.CAD für Java.  
- **Welche primäre Operation wird ausgeführt?** `export dwg to pdf`.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für Tests; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Was sind die Voraussetzungen?** Java‑Entwicklungsumgebung, Aspose.CAD für Java‑Bibliothek und DWG‑Dateien.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für eine Grundkonfiguration.

## Was ist „export dwg to pdf“?
Das Exportieren einer DWG‑Datei nach PDF konvertiert die vektorbasierte CAD‑Zeichnung in ein portables Dokumentenformat, wobei Ebenen, Linientypen und optional die Darstellung versteckter Linien erhalten bleiben. Das erleichtert das Teilen von CAD‑Entwürfen mit Interessenten, die keine CAD‑Software besitzen.

## Wie man versteckte Linien beim Export von DWG nach PDF aktiviert
Versteckte Linien werden über die Layout‑Einstellung in den Rasterisierungsoptionen gesteuert. Durch die Auswahl des **Model**‑Layouts weist Aspose.CAD den Renderer an, versteckte Kanten als unsichtbar zu behandeln, wodurch Sie eine saubere 2‑D‑Darstellung eines 3‑D‑Modells erhalten.

## Warum versteckte Linien beim Export aktivieren?
Versteckte Linien bieten eine klarere visuelle Darstellung komplexer 3‑D‑Modelle auf einer 2‑D‑Seite, indem nur sichtbare Kanten hervorgehoben werden. Das verbessert die Lesbarkeit und ist häufig für technische Dokumentationen erforderlich.

## Voraussetzungen

1. **Aspose.CAD für Java** – Laden Sie die Bibliothek von der offiziellen Seite [hier](https://releases.aspose.com/cad/java/) herunter.  
2. **DWG‑Dateien** – Legen Sie die Quell‑DWG‑Zeichnungen in einem bekannten Verzeichnis ab.  
3. **Java‑Entwicklungsumgebung** – JDK 8+ und Ihre bevorzugte IDE (Eclipse, IntelliJ usw.).  

Jetzt, wo Sie eingerichtet sind, tauchen wir in den Code ein.

## Namespaces importieren

Importieren Sie die notwendigen Klassen, um mit CAD‑Bildern und PDF‑Optionen arbeiten zu können.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Schritt 1: Projekt einrichten

Erstellen Sie ein Java‑Projekt und fügen Sie die Aspose.CAD‑JAR zu Ihrem Build‑Pfad hinzu. Definieren Sie anschließend das Verzeichnis, das Ihre DWG‑Dateien enthält.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro‑Tipp:** Verwenden Sie einen absoluten Pfad oder konfigurieren Sie einen relativen Pfad basierend auf dem Ressourcen‑Ordner Ihres Projekts.

## Schritt 2: DWG‑Datei laden

Laden Sie die Quell‑DWG‑Datei in ein `CadImage`‑Objekt, damit Sie sie manipulieren können.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Schritt 3: Rasterisierungsoptionen konfigurieren

Wählen Sie die Ebenen aus, die Sie einbeziehen möchten, und setzen Sie die Seitengröße so, dass sie dem Original entspricht. Hier aktivieren wir die Darstellung versteckter Linien, indem wir das Layout festlegen.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Schritt 4: PDF‑Optionen festlegen

Weisen Sie Aspose.CAD an, die Vektordaten in ein PDF zu rasterisieren, wobei das „Model“‑Layout verwendet wird, um versteckte Linien verborgen zu lassen.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 5: Ergebnis speichern

Exportieren Sie schließlich das DWG als PDF‑Datei. Die versteckten Linien werden gemäß dem festgelegten Layout berücksichtigt.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Häufiges Problem:** Wenn das Layout nicht auf `"Model"` gesetzt wird, erscheinen alle Linien (einschließlich versteckter) im PDF durchgängig.

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Wie zu beheben |
|---------|-------------------|----------------|
| PDF zeigt alle Linien durchgängig | Layout nicht auf **Model** gesetzt | Stellen Sie sicher, dass `rasterizationOptions.setLayouts(new String[] { "Model" });` vor dem Speichern aufgerufen wird. |
| Fehlende Ebenen in der Ausgabe | Ungültige Ebenennamen | Prüfen Sie die Ebenennamen in der DWG‑Datei und stimmen Sie sie exakt mit der `list` ab. |
| Out‑of‑memory‑Fehler bei großen Dateien | Große Rasterisierungsgröße | Reduzieren Sie die Seitengröße oder verarbeiten Sie die Zeichnung nach Möglichkeit in Teilen. |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?
A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate wie DWG, DXF, DWF und mehr.

### Q2: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?
A2: Ja, Sie finden die kostenlose Testversion [hier](https://releases.aspose.com/).

### Q3: Wie erhalte ich Support für Aspose.CAD für Java?
A3: Besuchen Sie das Aspose.CAD‑Forum [hier](https://forum.aspose.com/c/cad/19) für Community‑Support.

### Q4: Wo finde ich detaillierte Dokumentation für Aspose.CAD für Java?
A4: Siehe die Dokumentation [hier](https://reference.aspose.com/cad/java/).

### Q5: Kann ich eine temporäre Lizenz für Aspose.CAD für Java erwerben?
A5: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q6: Funktioniert diese Methode auch für die Konvertierung von DWG nach PDF in einer headless Server‑Umgebung?
A6: Absolut. Da der Code ausschließlich die Aspose.CAD‑API nutzt, läuft er ohne UI‑Abhängigkeiten und ist ideal für serverseitige Automatisierung.

## Fazit

Sie haben nun eine vollständige, produktionsreife Methode, um **DWG nach PDF** mit Unterstützung für versteckte Linien mithilfe von Aspose.CAD für Java zu exportieren. Dieser Ansatz lässt sich in Batch‑Verarbeitungstools, Web‑Services oder Desktop‑Anwendungen integrieren, um die CAD‑zu‑PDF‑Konvertierung zu automatisieren.

---

**Zuletzt aktualisiert:** 2026-03-05  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}