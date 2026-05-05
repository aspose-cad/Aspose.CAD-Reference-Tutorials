---
date: 2026-02-15
description: Erfahren Sie, wie Sie eine benutzerdefinierte Seitengröße festlegen und
  ein PDF aus CAD mit Aspose.CAD für Java erstellen. Dieser Schritt‑für‑Schritt‑Leitfaden
  behandelt den Export von CAD nach PDF mit automatischer Layout‑Skalierung.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Benutzerdefinierte Seitengröße festlegen – PDF aus CAD mit automatischer Layout‑Skalierung
url: /de/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Benutzerdefinierte Seitengröße festlegen – PDF aus CAD mit automatischer Layout‑Skalierung erstellen

## Einführung

Wenn Sie **benutzerdefinierte Seitengröße** festlegen müssen, während Sie **PDF aus CAD**‑Dateien schnell und mit perfekter Skalierung erstellen, bietet Aspose.CAD für Java die passende Lösung. Auto Layout Scaling passt die Layout‑Abmessungen automatisch an, sodass das resultierende PDF genau wie beabsichtigt aussieht, unabhängig von der ursprünglichen CAD‑Seitengröße. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer DXF‑Datei bis zum Exportieren eines PDFs – und zeigen dabei die **export CAD to PDF**‑Funktionen der Bibliothek sowie die Möglichkeit, **DWG zu PDF** zu **konvertieren** oder bei Bedarf die **PDF‑Auflösung zu erhöhen**.

## Schnellantworten
- **Was macht Auto Layout Scaling?** Es ändert automatisch die Größe von CAD‑Layouts, sodass sie beim Rasterisieren in die Ziel‑Seitenabmessungen passen.
- **Welche Formate kann ich konvertieren?** Jedes von Aspose.CAD unterstützte Format (z. B. DXF, DWG, DWF) kann in PDF konvertiert werden.
- **Benötige ich eine Lizenz für die Produktion?** Ja, für den Einsatz außerhalb der Evaluierung ist eine kommerzielle Lizenz erforderlich.
- **Wie lange dauert die Konvertierung?** In der Regel unter einer Sekunde für Standarddateien auf moderner Hardware.
- **Kann ich die Seitengröße ändern?** Ja, Sie können benutzerdefinierte Seitenabmessungen über `CadRasterizationOptions` festlegen.

## Was bedeutet „PDF aus CAD erstellen“?

Ein PDF aus CAD zu erstellen bedeutet, eine vektorbasierte Konstruktionszeichnung (DXF, DWG usw.) zu rasterisieren und in ein PDF‑Dokument zu überführen. Das PDF bewahrt die visuelle Treue der Originalzeichnung und ist auf jeder Plattform leicht anzeigbar.

## Warum Auto Layout Scaling verwenden?

- **Konsistente Ausgabe:** Stellt sicher, dass alle Layouts die PDF‑Seite ausfüllen, ohne manuelle Größenberechnungen.
- **Zeitersparnis:** Entfernt die Notwendigkeit, Skalierungsfaktoren für jede Zeichnung manuell anzupassen.
- **Hohe Qualität:** Bewahrt Linienstärken und geometrische Genauigkeit während der Konvertierung.
- **Flexibilität:** Funktioniert für **convert dxf to pdf**, **convert dwg to pdf** und sogar, wenn Sie die **PDF‑Auflösung erhöhen** müssen, um druckfertige Dateien zu erzeugen.

## Voraussetzungen

1. **Aspose.CAD für Java Bibliothek** – laden Sie die neueste Version von der [download page](https://releases.aspose.com/cad/java/) herunter.  
2. **Ressourcen‑Verzeichnis** – erstellen Sie einen Ordner auf Ihrem Rechner, um CAD‑Dateien zu speichern; ersetzen Sie `"Your Document Directory"` im Code durch diesen Pfad.  
3. **Beispiel‑CAD‑Datei** – für diese Anleitung verwenden wir `conic_pyramid.dxf`, die im Aspose‑Beispieldatensatz enthalten ist.

## Namespaces importieren

Zuerst importieren wir die erforderlichen Klassen. Dadurch erhalten wir Zugriff auf Bild‑Laden, Rasterisierung und PDF‑Export‑Funktionen.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Wie man benutzerdefinierte Seitengröße für PDF aus CAD festlegt

Bevor wir in den Schritt‑für‑Schritt‑Code eintauchen, sollten wir verstehen, warum das Festlegen einer benutzerdefinierten Seitengröße wichtig ist. Wenn Sie **benutzerdefinierte Seitengröße** festlegen, bestimmen Sie die physischen Abmessungen des resultierenden PDFs (z. B. A4, Letter oder eine eigens definierte Größe). Das ist entscheidend für ingenieurtechnische Workflows, bei denen Zeichnungen den Blatt‑Standards entsprechen müssen oder wenn das PDF in größere Dokumente eingebettet werden soll.

### Schritt 1: CAD‑Datei laden

Das Laden der Quelldatei ist der erste Schritt beim **how to export CAD** in ein PDF‑Dokument.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Schritt 2: Rasterisierungsoptionen erstellen

Definieren Sie die Ziel‑Seitenabmessungen. Sie können diesen Block auch nutzen, um **CAD‑Seitengröße** manuell festzulegen, falls Sie ein benutzerdefiniertes Layout bevorzugen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Schritt 3: Auto Layout Scaling aktivieren

Aktivieren Sie die automatische Skalierungsfunktion. Dies ist der Kern von **how to set scaling** für eine CAD‑zu‑PDF‑Konvertierung.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Schritt 4: PDF‑Optionen erstellen

Verknüpfen Sie die Rasterisierungseinstellungen mit den PDF‑Export‑Optionen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Schritt 5: In PDF exportieren

Speichern Sie schließlich das gerenderte Bild als PDF‑Datei. Dieser Schritt schließt den **convert dxf to pdf**‑Workflow ab.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Wiederholen Sie die obigen Schritte für alle weiteren CAD‑Dateien, die Sie verarbeiten möchten, egal ob es sich um **DWG**, **DWF** oder andere unterstützte Formate handelt.

## Häufige Anwendungsfälle

| Szenario | Warum eine benutzerdefinierte Seitengröße setzen? |
|----------|---------------------------------------------------|
| **Einreichung von Bauzeichnungen** | Passt das PDF an die standardisierten Blattgrößen A1/A2 an, die von Aufsichtsbehörden gefordert werden. |
| **Einbettung in technische Handbücher** | Stellt sicher, dass die Zeichnung in das vordefinierte Layout des Handbuchs passt, ohne zusätzliche Skalierung. |
| **Hochauflösender Druck** | Ermöglicht das Erhöhen der DPI (z. B. `rasterizationOptions.setResolution(300)`) bei gleichbleibenden Seitenabmessungen. |

## Häufige Probleme & Fehlerbehebung

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| Leeres PDF | Rasterisierungsoptionen nicht gesetzt oder falscher Dateipfad | Prüfen Sie den Pfad von `srcFile` und stellen Sie sicher, dass `setPageWidth/Height` nicht null ist |
| Verzerrte Skalierung | `setAutomaticLayoutsScaling` bleibt auf `false` | Aktivieren Sie die automatische Skalierung oder berechnen Sie den Skalierungsfaktor manuell |
| Fehlende Ebenen | Quell‑DXF enthält nicht unterstützte Entitäten | Prüfen Sie die Release‑Notes von Aspose.CAD für unterstützte Entitätstypen |

## Häufig gestellte Fragen

**Q: Ist Aspose.CAD für Java mit allen CAD‑Dateiformaten kompatibel?**  
A: Aspose.CAD für Java unterstützt verschiedene CAD‑Formate, darunter DWG, DXF und DWF.

**Q: Kann ich die Skalierungsoptionen weiter anpassen?**  
A: Ja, die Klasse `CadRasterizationOptions` bietet Eigenschaften zur Feinabstimmung von Skalierung, DPI und anderen Rasterisierungseinstellungen.

**Q: Wo finde ich weitere Dokumentation zu Aspose.CAD für Java?**  
A: Siehe die [documentation](https://reference.aspose.com/cad/java/) für detaillierte Informationen und Beispiele.

**Q: Gibt es eine kostenlose Testversion von Aspose.CAD für Java?**  
A: Ja, Sie können eine [free trial](https://releases.aspose.com/) nutzen, um die Funktionen von Aspose.CAD für Java zu testen.

**Q: Wie kann ich Unterstützung erhalten oder mich an Diskussionen über Aspose.CAD für Java beteiligen?**  
A: Besuchen Sie das [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), um mit der Community in Kontakt zu treten und Unterstützung zu erhalten.

**Weitere häufige Fragen**

**Q: Wie konvertiere ich eine DWG‑Datei zu PDF anstelle von DXF?**  
A: Der gleiche Code funktioniert; ändern Sie einfach die Dateierweiterung in `srcFile` zu `.dwg`.

**Q: Kann ich eine benutzerdefinierte DPI für hochauflösende PDFs festlegen?**  
A: Ja, verwenden Sie `rasterizationOptions.setResolution(300);` (oder jede gewünschte DPI).

**Q: Ist es möglich, Schriftarten im erzeugten PDF einzubetten?**  
A: Aspose.CAD rasterisiert die Zeichnung, sodass Schriftarten als Vektoren gerendert werden; ein separates Einbetten von Schriftarten ist nicht erforderlich.

## Fazit

Durch Befolgen dieser Anleitung wissen Sie jetzt, wie Sie **benutzerdefinierte Seitengröße** festlegen und **PDF aus CAD**‑Dateien mit Aspose.CAD für Java und automatischer Layout‑Skalierung erstellen. Der Prozess optimiert den **export CAD to PDF**‑Workflow, sorgt für konsistente Skalierung und spart wertvolle Entwicklungszeit. Experimentieren Sie gern mit verschiedenen Seitengrößen, Auflösungen und CAD‑Formaten, um Ihre Projektanforderungen zu erfüllen – sei es beim **Konvertieren von DWG zu PDF**, **Erhöhen der PDF‑Auflösung** oder beim Aufbau eines **java CAD to PDF**‑Batch‑Processors.

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD für Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}