---
date: 2025-12-10
description: Erfahren Sie, wie Sie mit Aspose.CAD für Java und Auto Layout Scaling
  PDFs aus CAD erstellen. Diese Schritt‑für‑Schritt‑Anleitung zeigt Ihnen, wie Sie
  CAD effizient und zuverlässig in PDF exportieren.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: PDF aus CAD erstellen – Automatisches Layout‑Skalieren mit Aspose.CAD Java
url: /de/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF aus CAD erstellen – Auto Layout Scaling mit Aspose.CAD Java

## Einleitung

Wenn Sie **PDF aus CAD** Dateien schnell und mit perfekter Skalierung erstellen müssen, bietet Aspose.CAD für Java die passende Lösung. Auto Layout Scaling passt die Layout‑Abmessungen automatisch an, sodass das resultierende PDF genau wie beabsichtigt aussieht, unabhängig von der ursprünglichen CAD‑Seitengröße. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer DXF‑Datei bis zum Exportieren eines PDFs – und heben dabei die **export CAD to PDF**‑Funktionen der Bibliothek hervor.

## Schnelle Antworten
- **Was macht Auto Layout Scaling?** Es verkleinert/erweitert CAD‑Layouts automatisch, um die Zielseitengröße beim Rasterisieren zu füllen.
- **Welche Formate kann ich konvertieren?** Jedes von Aspose.CAD unterstützte Format (z. B. DXF, DWG, DWF) kann in PDF konvertiert werden.
- **Benötige ich eine Lizenz für die Produktion?** Ja, für den nicht‑evaluativen Einsatz ist eine kommerzielle Lizenz erforderlich.
- **Wie lange dauert die Konvertierung?** In der Regel weniger als eine Sekunde für Standarddateien auf moderner Hardware.
- **Kann ich die Seitengröße ändern?** Ja, Sie können benutzerdefinierte Seitengrößen über `CadRasterizationOptions` festlegen.

## Was bedeutet „PDF aus CAD erstellen“?
Ein PDF aus CAD zu erstellen bedeutet, eine vektorbasierte Konstruktionszeichnung (DXF, DWG usw.) zu nehmen und sie in ein PDF‑Dokument zu rasterisieren. Das PDF bewahrt die visuelle Treue der Originalzeichnung und kann auf jeder Plattform problemlos angezeigt werden.

## Warum Auto Layout Scaling verwenden?
- **Konsistentes Ergebnis:** Gewährleistet, dass alle Layouts die PDF‑Sefüllen, ohne manuelle Größenberechnungen.
- **Zeitersparnis:** Entfernt die Notwendigkeit, Skalierungsfaktoren für jede Zeichnung manuell anzupassen.
- **Hohe Qualität:** Bewahrt Linienstärken und geometrische Genauigkeit während der Konvertierung.

## Voraussetzungen

1. **Aspose.CAD für Java Bibliothek** – Laden Sie die neueste Version von der [Download‑Seite](https://releases.aspose.com/cad/java/) herunter.  
2. **Ressourcen‑Verzeichnis** – Erstellen Sie einen Ordner auf Ihrem Rechner, um CAD‑Dateien zu speichern; ersetzen Sie `"Your Document Directory"` im Code durch diesen Pfad.  
3. **Beispiel‑CAD‑Datei** – Für diese Anleitung verwenden wir `conic_pyramid.dxf`, die im Aspose‑Beispieldatensatz enthalten ist.

## Namespaces importieren

Zuerst importieren Sie die benötigten Klassen. Dadurch erhalten wir Zugriff auf Bild‑Laden, Rasterisierung und PDF‑Export‑Funktionen.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Schritt 1: CAD‑Datei laden

Das Laden der Quelldatei ist der erste Schritt beim **Exportieren von CAD** in ein PDF‑Dokument.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Schritt 2: Rasterisierungsoptionen erstellen

Definieren Sie die Zielseitengrößen. Sie können diesen Block auch verwenden, um die **CAD‑Seitengröße** manuell festzulegen, falls Sie ein benutzerdefiniertes Layout bevorzugen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Schritt 3: Auto Layout Scaling aktivieren

Aktivieren Sie die automatische Skalierungsfunktion. Dies ist das Kernstück von **wie man Skalierung einstellt** für eine CAD‑zu‑PDF‑Konvertierung.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Schritt 4: PDF‑Optionen erstellen

Verknüpfen Sie die Rasterisierungseinstellungen mit den PDF‑Export‑Optionen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 5: Exportieren nach PDF

Speichern Sie schließlich das gerenderte Bild als PDF‑Datei. Dieser Schritt schließt den **DXF‑zu‑PDF‑Konvertierungs**‑Workflow ab.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Wiederholen Sie die obigen Schritte für alle weiteren CAD‑Dateien, die Sie verarbeiten müssen.

## Häufige Probleme & Fehlersuche

| Symptom               | Wahrscheinliche Ursache                                 | Lösung                                                                                           |
|-----------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Leeres PDF‑Ausgabe    | Rasterisierungsoptionen nicht gesetzt oder Dateipfad falsch | Überprüfen Sie den Pfad `srcFile` und stellen Sie sicher, dass `setPageWidth/Height` nicht null sind |
| Verzerrte Skalierung  | `setAutomaticLayoutsScaling` bleibt auf `false`          | Aktivieren Sie die automatische Skalierung oder berechnen Sie den Skalierungsfaktor manuell      |
| Fehlende Ebenen       | Quell‑DXF enthält nicht unterstützte Entitäten           | Prüfen Sie die Aspose.CAD‑Release‑Notes für unterstützte Entitätstypen                           |

## FAQ

### Q1: Ist Aspose.CAD für Java mit allen CAD‑Dateiformaten kompatibel?
A1: Aspose.CAD für Java unterstützt verschiedene CAD‑Formate, darunter DWG, DXF und DWF.

### Q2: Kann ich die Skalierungsoptionen weiter anpassen?
A2: Ja, die Klasse `CadRasterizationOptions` bietet verschiedene Eigenschaften zur Feinabstimmung von Skalierung und anderen Einstellungen.

### Q3: Wo finde ich zusätzliche Dokumentation für Aspose.CAD für Java?
A3: Siehe die [Dokumentation](https://reference.aspose.com/cad/java/) für detaillierte Informationen und Beispiele.

### Q4: Gibt es eine kostenlose Testversion von Aspose.CAD für Java?
A4: Ja, Sie können eine [kostenlose Testversion](https://releases.aspose.com/) ausprobieren, um die Fähigkeiten von Aspose.CAD für Java zu erleben.

### Q5: Wie kann ich Unterstützung erhalten oder mich an Diskussionen über Aspose.CAD für Java beteiligen?
A5: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19), um mit der Community in Kontakt zu treten und Unterstützung zu erhalten.

**Zusätzliche häufige Fragen**

**Q: Wie konvertiere ich eine DWG‑Datei in PDF statt DXF?**  
A: Der gleiche Code funktioniert; ändern Sie einfach die Dateierweiterung in `srcFile` zu `.dwg`.

**Q: Kann ich eine benutzerdefinierte DPI für hochauflösende PDFs festlegen?**  
A: Ja, verwenden Sie `rasterizationOptions.setResolution(300);` (oder jede gewünschte DPI).

**Q: Ist es möglich, Schriftarten in das erzeugte PDF einzubetten?**  
A: Aspose.CAD rasterisiert die Zeichnung, sodass Schriftarten als Vektoren gerendert werden; ein separates Einbetten von Schriftarten ist nicht erforderlich.

## Fazit

Durch die Befolgung dieser Anleitung wissen Sie nun, wie Sie **PDF aus CAD**‑Dateien mit Aspose.CAD für Java und Auto Layout Scaling erstellen. Der Prozess optimiert den **Export CAD to PDF**‑Workflow, sorgt für konsistente Skalierung und spart Ihnen wertvolle Entwicklungszeit. Experimentieren Sie gern mit verschiedenen Seitengrößen, Auflösungen und CAD‑Formaten, um Ihren Projektanforderungen gerecht zu werden.

---

**Zuletzt aktualisiert:** 2025-12-10  
**Getestet mit:** Aspose.CAD für Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}