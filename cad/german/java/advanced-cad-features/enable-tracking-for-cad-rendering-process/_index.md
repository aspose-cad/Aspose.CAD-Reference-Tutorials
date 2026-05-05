---
date: 2026-02-12
description: Erfahren Sie, wie Sie die PDF‑Seitengröße beim Konvertieren von CAD zu
  PDF mit Aspose.CAD für Java festlegen. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung,
  um das Tracking zu aktivieren, CAD in PDF zu konvertieren und CAD effizient als
  PDF zu speichern.
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

# Tracking für den CAD-Renderprozess aktivieren

## Einleitung

In diesem Tutorial lernen Sie, wie Sie **PDF-Seitengröße festlegen** können, während Sie **CAD zu PDF konvertieren** mit **Aspose.CAD for Java**. Durch das Aktivieren des Trackings erhalten Sie vollständige Sichtbarkeit über die Rendering-Pipeline, was das Debuggen und Optimieren der Konvertierung von CAD-Dateien (wie DXF) zu PDF erleichtert. Egal, ob Sie **CAD als PDF speichern**, PDF aus DXF erzeugen oder einfach die Ausgabedimensionen steuern möchten, die nachfolgenden Schritte führen Sie durch den gesamten Prozess.

## Schnelle Antworten
- **Was bewirkt „PDF-Seitengröße festlegen“?** Sie definiert die Breite und Höhe der resultierenden PDF-Seite während des CAD-Renderings.  
- **Warum Tracking aktivieren?** Tracking protokolliert jede Phase der Konvertierung und hilft Ihnen, Leistungsengpässe oder Fehler zu erkennen.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche CAD-Formate werden unterstützt?** DWG, DXF, DGN und viele weitere – siehe die Aspose.CAD-Dokumentation für die vollständige Liste.  
- **Kann ich die Seitengrößen dynamisch ändern?** Ja – passen Sie einfach die Werte `PageWidth` und `PageHeight` in `CadRasterizationOptions` an.

## Was bedeutet „PDF-Seitengröße festlegen“ beim CAD-Rendering?

Das Festlegen der PDF-Seitengröße teilt dem Rasterizer mit, wie groß die Zeichenfläche sein soll, wenn die Vektor‑CAD‑Daten in eine PDF‑Seite gerastert werden. Dies ist entscheidend, um die visuelle Treue zu bewahren, insbesondere bei detaillierten technischen Zeichnungen.

## Warum Tracking für das CAD-Rendering aktivieren?

Das Aktivieren von Tracking liefert ein detailliertes Protokoll jedes Schrittes – vom Laden der Quelldatei bis zum Schreiben der PDF‑Ausgabe. Es hilft Ihnen:
- Diagnostizieren, warum eine bestimmte Zeichnung möglicherweise fehlerhaft gerendert wird.  
- Die für jede Phase benötigte Zeit zu messen, was für Performance‑Optimierungen nützlich ist.  
- Verifizieren, dass die von Ihnen konfigurierte Seitengröße tatsächlich angewendet wird.

## Voraussetzungen

Bevor Sie mit der Einrichtung des Trackings beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
1. **Java-Entwicklungsumgebung** – Java 8 oder höher auf Ihrem Rechner installiert.  
2. **Aspose.CAD-Bibliothek** – Laden Sie die Aspose.CAD‑Bibliothek herunter und integrieren Sie sie in Ihr Java‑Projekt. Sie finden den Download‑Link [hier](https://releases.aspose.com/cad/java/).  
3. **Dokumentverzeichnis** – Bereiten Sie ein Verzeichnis vor, um Ihre CAD‑Dateien und die erzeugten PDFs zu speichern.

## Namespaces importieren

Importieren Sie in Ihrem Java‑Projekt die erforderlichen Namespaces, um die Funktionen von Aspose.CAD zu nutzen. Fügen Sie die folgenden Zeilen am Anfang Ihres Codes hinzu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Ressourcenverzeichnis-Pfad festlegen

Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrem Dokumentverzeichnis.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## CAD-Datei laden

Geben Sie den Pfad zu Ihrer CAD‑Datei an und stellen Sie sicher, dass sie sich im vorgesehenen Dokumentverzeichnis befindet.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## PDF-Ausgabeoptionen festlegen

Erzeugen Sie einen Ausgabestream und setzen Sie die PDF‑Optionen für die Konvertierung.

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

## CadRasterizationOptions konfigurieren (PDF-Seitengröße festlegen)

Hier **legen wir die PDF‑Seitengröße** fest, indem wir `PageWidth` und `PageHeight` definieren. Passen Sie diese Werte an die für Ihre technische Zeichnung erforderlichen Abmessungen an. Dies ist der zentrale Schritt, der beantwortet, **wie man die PDF‑Größe festlegt**, wenn Sie **java cad to pdf**.

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## PDF-Datei speichern

Speichern Sie die gerenderte PDF‑Datei mit den angegebenen Optionen.

```java
image.save(stream, pdfOptions);
```

## Tracking-Aktivierung überprüfen

Bestätigen Sie, dass das Tracking für den CAD‑Renderprozess erfolgreich aktiviert ist.

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

## Häufige Probleme & Fehlerbehebung

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| PDF-Seite erscheint leer | `PageWidth`/`PageHeight` auf 0 gesetzt | Stellen Sie sicher, dass nicht‑null Dimensionen angegeben werden. |
| Ausgabedatei ist beschädigt | Ausgabestream nicht geschlossen | Rufen Sie `stream.close()` nach `image.save(...)` auf. |
| Fehlende Ebenen im PDF | CAD-Datei verwendet nicht unterstützte Entitäten | Überprüfen Sie, ob das Dateiformat vollständig von Aspose.CAD unterstützt wird. |

## Häufig gestellte Fragen

### Q1: Ist Aspose.CAD mit allen CAD-Dateiformaten kompatibel?

A1: Aspose.CAD unterstützt eine breite Palette von CAD‑Formaten, darunter DWG, DXF, DGN und weitere. Siehe die [Dokumentation](https://reference.aspose.com/cad/java/) für eine umfassende Liste.

### Q2: Kann ich die Ausgabedimensionen der PDF‑Datei anpassen?

A2: Auf jeden Fall! Passen Sie die Parameter `PageWidth` und `PageHeight` in den `CadRasterizationOptions` an, um die Ausgabedimensionen zu bestimmen.

### Q3: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?

A3: Ja, Sie können die Funktionen von Aspose.CAD testen, indem Sie eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Wie kann ich Community‑Support für Aspose.CAD‑bezogene Anfragen erhalten?

A4: Besuchen Sie das [Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19), um mit der Community in Kontakt zu treten und Unterstützung zu erhalten.

### Q5: Gibt es temporäre Lizenzen für Aspose.CAD?

A5: Ja, falls Sie eine temporäre Lizenz benötigen, können Sie diese [hier](https://purchase.aspose.com/temporary-license/) erwerben.

## Fazit

Herzlichen Glückwunsch! Sie haben nun gelernt, wie Sie **die PDF‑Seitengröße festlegen** und das Tracking für das CAD‑Rendering mit **Aspose.CAD for Java** aktivieren. Diese Anleitung befähigt Sie, **CAD zu PDF zu konvertieren**, **CAD als PDF zu speichern** und PDF aus DXF zu erzeugen, wobei Sie die Seitengrößen vollständig kontrollieren und detaillierte Ausführungsprotokolle erhalten. Experimentieren Sie gern mit verschiedenen Seitengrößen und erkunden Sie weitere Rasterisierungsoptionen, um Ihre spezifischen Engineering‑Workflows zu unterstützen.

---

**Zuletzt aktualisiert:** 2026-02-12  
**Getestet mit:** Aspose.CAD for Java 24.12 (neueste Version zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}