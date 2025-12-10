---
date: 2025-12-07
description: Erfahren Sie, wie Sie die PDF‑Seitengröße beim Konvertieren von CAD zu
  PDF mit Aspose.CAD für Java festlegen. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung,
  um die Nachverfolgung zu aktivieren, CAD in PDF zu konvertieren und CAD effizient
  als PDF zu speichern.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: Wie man die PDF‑Seitengröße festlegt und das Tracking für den CAD‑Renderprozess
  aktiviert
url: /de/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aktivieren des Trackings für den CAD‑Renderprozess

## Einführung

In diesem Tutorial lernen Sie, wie Sie **die PDF‑Seitengröße festlegen**, während Sie **CAD nach PDF konvertieren** mithilfe von **Aspose.CAD for Java**. Durch das Aktivieren des Trackings erhalten Sie vollständige Transparenz über die Rendering‑Pipeline, was das Debuggen und Optimieren der Konvertierung von CAD‑Dateien (wie DXF) nach PDF erleichtert. Egal, ob Sie **CAD als PDF speichern**, PDF aus DXF erzeugen oder einfach die Ausgabedimensionen steuern möchten – die nachfolgenden Schritte führen Sie durch den gesamten Prozess.

## Schnellantworten
- **Was bewirkt „set PDF page size“?** Sie definiert die Breite und Höhe der resultierenden PDF‑Seite während des CAD‑Renderings.  
- **Warum Tracking aktivieren?** Tracking protokolliert jede Phase der Konvertierung und hilft, Leistungsengpässe oder Fehler zu erkennen.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche CAD‑Formate werden unterstützt?** DWG, DXF, DGN und viele weitere – siehe die Aspose.CAD‑Dokumentation für die vollständige Liste.  
- **Kann ich die Seitengröße zur Laufzeit ändern?** Ja – passen Sie einfach die Werte `PageWidth` und `PageHeight` in `CadRasterizationOptions` an.

## Was bedeutet „set PDF page size“ beim CAD‑Rendering?

Das Festlegen der PDF‑Seitengröße teilt dem Rasterizer mit, wie groß die Zeichenfläche sein soll, wenn die Vektor‑CAD‑Daten in eine PDF‑Seite gerastert werden. Dies ist entscheidend, um die visuelle Treue zu bewahren, insbesondere bei detaillierten technischen Zeichnungen.

## Warum Tracking für das CAD‑Rendering aktivieren?

Durch das Aktivieren des Trackings erhalten Sie ein detailliertes Protokoll jedes Schrittes – vom Laden der Quelldatei bis zum Schreiben der PDF‑Ausgabe. Es hilft Ihnen:

- Zu diagnostizieren, warum eine bestimmte Zeichnung möglicherweise fehlerhaft gerendert wird.  
- Die für jede Phase benötigte Zeit zu messen, was für Performance‑Optimierungen nützlich ist.  
- Zu überprüfen, ob die konfigurierte Seitengröße tatsächlich angewendet wurde.

## Voraussetzungen

Bevor Sie mit der Einrichtung des Trackings beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

1. **Java‑Entwicklungsumgebung** – Java 8 oder höher auf Ihrem Rechner installiert.  
2. **Aspose.CAD‑Bibliothek** – Laden Sie die Aspose.CAD‑Bibliothek herunter und binden Sie sie in Ihr Java‑Projekt ein. Den Download‑Link finden Sie [hier](https://releases.aspose.com/cad/java/).  
3. **Dokumenten‑Verzeichnis** – Legen Sie ein Verzeichnis an, in dem Sie Ihre CAD‑Dateien und die erzeugten PDFs speichern.

## Namespaces importieren

Importieren Sie in Ihrem Java‑Projekt die notwendigen Namespaces, um die Funktionen von Aspose.CAD zu nutzen. Fügen Sie die folgenden Zeilen am Anfang Ihres Codes ein:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Pfad zum Ressourcen‑Verzeichnis festlegen

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrem Dokumenten‑Verzeichnis.

## CAD‑Datei laden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Geben Sie den Pfad zu Ihrer CAD‑Datei an und stellen Sie sicher, dass sie sich im vorgesehenen Dokumenten‑Verzeichnis befindet.

## PDF‑Ausgabeoptionen festlegen

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Erzeugen Sie einen Output‑Stream und setzen Sie die PDF‑Optionen für die Konvertierung.

## CadRasterizationOptions konfigurieren (PDF‑Seitengröße festlegen)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Hier **setzen wir die PDF‑Seitengröße**, indem wir `PageWidth` und `PageHeight` definieren. Passen Sie diese Werte an die für Ihre technische Zeichnung erforderlichen Abmessungen an. Dieser Schritt beeinflusst direkt, wie der CAD‑Inhalt skaliert und im finalen PDF gerendert wird.

## PDF‑Datei speichern

```java
image.save(stream, pdfOptions);
```

Speichern Sie die gerenderte PDF‑Datei mit den angegebenen Optionen.

## Überprüfung der Tracking‑Aktivierung

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

Bestätigen Sie, dass das Tracking erfolgreich für den CAD‑Renderprozess aktiviert wurde.

## Häufige Probleme & Fehlersuche

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| PDF‑Seite erscheint leer | `PageWidth`/`PageHeight` auf 0 gesetzt | Stellen Sie sicher, dass nicht‑null Dimensionen angegeben werden. |
| Ausgabedatei ist beschädigt | Output‑Stream nicht geschlossen | Rufen Sie `stream.close()` nach `image.save(...)` auf. |
| Fehlende Ebenen im PDF | CAD‑Datei verwendet nicht unterstützte Entitäten | Prüfen Sie, ob das Dateiformat vollständig von Aspose.CAD unterstützt wird. |

## Häufig gestellte Fragen

### Q1: Ist Aspose.CAD mit allen CAD‑Dateiformaten kompatibel?

A1: Aspose.CAD unterstützt eine breite Palette von CAD‑Formaten, darunter DWG, DXF, DGN und weitere. Siehe die [Dokumentation](https://reference.aspose.com/cad/java/) für eine vollständige Liste.

### Q2: Kann ich die Ausgabedimensionen der PDF‑Datei anpassen?

A2: Absolut! Passen Sie die Parameter `PageWidth` und `PageHeight` in den `CadRasterizationOptions` an, um die Ausgabedimensionen zu steuern.

### Q3: Gibt es eine kostenlose Testversion von Aspose.CAD for Java?

A3: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) ausprobieren.

### Q4: Wie erhalte ich Community‑Support für Fragen zu Aspose.CAD?

A4: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19), um sich mit der Community auszutauschen und Unterstützung zu erhalten.

### Q5: Gibt es temporäre Lizenzen für Aspose.CAD?

A5: Ja, wenn Sie eine temporäre Lizenz benötigen, können Sie diese [hier](https://purchase.aspose.com/temporary-license/) erwerben.

## Fazit

Herzlichen Glückwunsch! Sie haben nun gelernt, wie Sie **die PDF‑Seitengröße festlegen** und das Tracking für das CAD‑Rendering mithilfe von **Aspose.CAD for Java** aktivieren. Dieser Leitfaden befähigt Sie, **CAD nach PDF zu konvertieren**, **CAD als PDF zu speichern** und PDF aus DXF zu erzeugen, wobei Sie die Seitengröße vollständig kontrollieren und detaillierte Ausführungsprotokolle erhalten. Experimentieren Sie gern mit verschiedenen Seitengrößen und erkunden Sie weitere Rasterisierungsoptionen, um Ihre spezifischen Engineering‑Workflows zu optimieren.

---

**Zuletzt aktualisiert:** 2025-12-07  
**Getestet mit:** Aspose.CAD for Java 24.12 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
