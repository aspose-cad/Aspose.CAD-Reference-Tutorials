---
date: 2026-01-04
description: Erfahren Sie, wie Sie **CAD als PNG speichern** und mühelos OLE‑Objekte
  aus CAD‑Dateien mit Aspose.CAD für Java exportieren. Schnelle Einrichtung, vollständiges
  Codebeispiel und Tipps zu bewährten Verfahren.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD als PNG speichern und OLE‑Objekte mit Aspose.CAD für Java exportieren
url: /de/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD als PNG speichern und OLE‑Objekte mit Aspose.CAD für Java exportieren

## Einführung

In der schnelllebigen Welt des Computer‑Aided Design (CAD) kann das **Speichern von CAD als PNG** und das Extrahieren eingebetteter OLE‑Objekte (Object Linking and Embedding) Ihren Arbeitsablauf erheblich vereinfachen. Egal, ob Sie ein Batch‑Konvertierungstool bauen, Thumbnails für ein Web‑Portal erzeugen oder einfach OLE‑Inhalte archivieren möchten – Aspose.CAD für Java bietet Ihnen eine saubere, programmatische Möglichkeit dazu. In diesem Tutorial führen wir Sie durch den gesamten Prozess, von der Projekt‑Einrichtung bis zum Export jedes OLE‑Objekts als PNG‑Bild.

## Schnellantworten
- **Kann ich OLE‑Objekte direkt nach PNG exportieren?** Ja – Aspose.CAD lädt die CAD‑Datei und ermöglicht das Rasterisieren jedes Layouts nach PNG.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher.  
- **Benötige ich eine Lizenz für dieses Feature?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Werden Vektordaten erhalten bleiben?** Die PNG‑Rasterisierung bewahrt die visuelle Treue, das Ergebnis ist jedoch ein Rasterbild, kein Vektor.  
- **Wird Batch‑Verarbeitung unterstützt?** Absolut – iterieren Sie über ein Array von Dateien wie im Code‑Beispiel gezeigt.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java Development Kit (JDK)** – Java 8+ installiert und konfiguriert.  
- **Aspose.CAD für Java** – Laden Sie die neueste Bibliothek vom [Download‑Link](https://releases.aspose.com/cad/java/) herunter.  
- **CAD‑Quelldateien** – Beliebige DWG/DXF/DGN‑Dateien, die OLE‑Objekte enthalten, die Sie exportieren möchten.

## Namespaces importieren

Um mit CAD‑Dateien zu arbeiten, müssen Sie die Kernklassen von Aspose.CAD importieren. Belassen Sie den Import‑Block exakt wie gezeigt – er stellt die Klassen bereit, die später im Tutorial verwendet werden.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Wie man CAD als PNG speichert

Im Folgenden finden Sie eine kompakte, schrittweise Anleitung, die **zeigt, wie OLE‑Objekte exportiert und CAD als PNG gespeichert** wird. Jeder Schritt enthält eine kurze Erklärung gefolgt vom genauen Code, den Sie in Ihr Projekt übernehmen können.

### Schritt 1: Dokumentverzeichnis festlegen

Definieren Sie den Ordner, der Ihre CAD‑Zeichnungen enthält. Ersetzen Sie den Platzhalter durch den tatsächlichen Pfad auf Ihrem Rechner.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Schritt 2: CAD‑Dateinamen definieren

Listen Sie jede CAD‑Datei auf, die Sie verarbeiten möchten. Sie können beliebig viele Einträge hinzufügen.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Schritt 3: PNG‑Exportoptionen festlegen

Konfigurieren Sie die Rasterisierungseinstellungen. Hier richten wir uns auf ein bestimmtes Layout (`Layout1`) und verwenden die Standard‑PNG‑Optionen.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Schritt 4: Durch CAD‑Dateien iterieren und als PNG speichern

Laden Sie jede CAD‑Datei, rasterisieren Sie die OLE‑Objekte und schreiben Sie die resultierende PNG‑Datei. Das Suffix `_out.png` hilft Ihnen, die erzeugten Bilder zu identifizieren.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **`Image.load` wirft `FileNotFoundException`** | Der Pfad `dataDir` ist falsch oder der Dateiname enthält einen Tippfehler. | Überprüfen Sie den Verzeichnis‑String und stellen Sie sicher, dass die Dateinamen exakt übereinstimmen, inklusive Leerzeichen. |
| **Ausgabe‑PNG ist leer** | Der Layout‑Name existiert nicht in der Quell‑CAD‑Datei. | Verwenden Sie `cadImage.getLayouts()`, um verfügbare Layouts aufzulisten, und aktualisieren Sie `rasterizationOptions.setLayouts(...)`. |
| **Große CAD‑Dateien verursachen OutOfMemoryError** | Das Rasterisieren hochauflösender Bilder verbraucht viel Heap‑Speicher. | Erhöhen Sie den JVM‑Heap (`-Xmx2g`) oder reduzieren Sie die Rasterisierungsauflösung via `rasterizationOptions.setResolution(...)`. |

## FAQ's

### Q1: Ist Aspose.CAD mit allen CAD‑Dateiformaten kompatibel?

A1: Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF und DGN. Die vollständige Liste finden Sie in der [Dokumentation](https://reference.aspose.com/cad/java/).

### Q2: Kann ich die Exporteinstellungen für OLE‑Objekte anpassen?

A2: Ja, Aspose.CAD bietet umfangreiche Optionen zur Anpassung der Exporteinstellungen, sodass Sie die Ausgabe an Ihre spezifischen Anforderungen anpassen können.

### Q3: Gibt es eine kostenlose Testversion von Aspose.CAD?

A3: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion von [hier](https://releases.aspose.com/) ausprobieren.

### Q4: Wo finde ich Community‑Support für Aspose.CAD?

A4: Treten Sie der Aspose.CAD‑Community im [Forum](https://forum.aspose.com/c/cad/19) bei, um Hilfe zu erhalten und Erfahrungen auszutauschen.

### Q5: Wie kann ich eine Lizenz für Aspose.CAD erwerben?

A5: Besuchen Sie die [Kaufseite](https://purchase.aspose.com/buy), um eine Lizenz zu erhalten, die Ihren Entwicklungsanforderungen entspricht.

## Fazit

Durch Befolgen dieser fünf einfachen Schritte können Sie **CAD als PNG speichern** und jedes eingebettete OLE‑Objekt mit nur wenigen Zeilen Java‑Code extrahieren. Dieser Ansatz eignet sich ideal für Batch‑Konvertierungen, automatisierte Berichte oder jede Situation, in der Sie Rasterbilder von CAD‑Inhalten benötigen, ohne manuell zu exportieren. Experimentieren Sie gern mit verschiedenen Rasterisierungsoptionen, um Qualität und Performance Ihren Bedürfnissen anzupassen.

---

**Zuletzt aktualisiert:** 2026-01-04  
**Getestet mit:** Aspose.CAD für Java 24.12 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}