---
date: 2026-03-02
description: Entfesseln Sie das Potenzial von Aspose.CAD für Java. Exportieren Sie
  mühelos OLE‑Objekte und **speichern Sie CAD als PNG**. Laden Sie jetzt herunter
  für eine nahtlose CAD‑Datenverwaltung.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD als PNG speichern – OLE‑Objekte mit Aspose.CAD für Java exportieren
url: /de/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD als PNG speichern – OLE‑Objekte mit Aspose.CAD für Java exportieren

## Einführung

In der dynamischen Welt des Computer‑Aided Design (CAD) ist das effiziente Verwalten und Extrahieren von OLE (Object Linking and Embedding)‑Objekten – und die Möglichkeit, **CAD als PNG zu speichern** – entscheidend für nachgelagerte Workflows wie Reporting, Web‑Vorschau oder Archivierung. Aspose.CAD für Java bietet eine leistungsstarke, code‑first‑Lösung, mit der Sie sowohl OLE‑Objekte exportieren als auch CAD‑Zeichnungen mit nur wenigen Codezeilen in hochwertige PNG‑Bilder konvertieren können.

## Schnellantworten
- **Was macht Aspose.CAD?** Es liest, manipuliert und konvertiert CAD‑Dateien (DWG, DXF, DGN usw.), ohne dass native CAD‑Software erforderlich ist.  
- **Kann ich CAD als PNG speichern?** Ja – verwenden Sie `PngOptions` zusammen mit `CadRasterizationOptions`, um ein beliebiges Layout zu rasterisieren.  
- **Wie exportiere ich OLE‑Objekte?** Laden Sie die CAD‑Datei mit `Image.load` und speichern Sie jedes OLE‑enthaltende Layout als PNG.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion ist verfügbar; eine kommerzielle Lizenz entfernt die Evaluationsbeschränkungen.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher wird vollständig unterstützt.

## Was bedeutet **CAD als PNG speichern**?
CAD als PNG zu speichern bedeutet, vektorbasierte CAD‑Zeichnungen in ein pixelbasiertes PNG‑Bild zu rasterisieren. Diese Konvertierung ist nützlich, wenn Sie ein leichtgewichtiges, universell anzeigbares Format für Webseiten, mobile Apps oder Dokumentationen benötigen.

## Warum Aspose.CAD für Java zum **Konvertieren von CAD zu PNG** verwenden?
- **Keine CAD‑Installation nötig** – die Bibliothek arbeitet vollständig in Java.  
- **Erhält Layout‑Treue** – Sie können bestimmte Layouts auswählen, DPI steuern und die Linienqualität beibehalten.  
- **Batch‑Verarbeitung** – iterieren Sie über mehrere Dateien mit einer einfachen Schleife.  
- **Export von OLE‑Objekten** – OLE‑Inhalte, die in DWG/DXF‑Dateien eingebettet sind, werden automatisch in die PNG‑Ausgabe gerendert.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- **Java‑Umgebung** – Vergewissern Sie sich, dass eine Java‑Entwicklungsumgebung auf Ihrem Rechner eingerichtet ist.  
- **Aspose.CAD für Java** – Laden Sie die Aspose.CAD‑Bibliothek für Java herunter und installieren Sie sie. Die Bibliothek finden Sie unter dem [Download‑Link](https://releases.aspose.com/cad/java/).  
- **CAD‑Dateien** – Bereiten Sie die CAD‑Dateien vor, die OLE‑Objekte enthalten und die Sie exportieren möchten.

## Namespaces importieren

Um zu beginnen, importieren Sie die erforderlichen Namespaces in Ihr Java‑Projekt. Diese Namespaces stellen die wesentlichen Klassen und Funktionalitäten bereit, die für die Arbeit mit CAD‑Dateien mittels Aspose.CAD nötig sind.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nun zerlegen wir den Vorgang des Exports von OLE‑Objekten aus CAD in mehrere Schritte:

## Wie man **CAD als PNG speichert** und OLE‑Objekte exportiert

### Schritt 1: Dokumentverzeichnis festlegen

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Ersetzen Sie `"Your Document Directory"` durch den Pfad zu dem Verzeichnis, das Ihre CAD‑Dateien enthält.

### Schritt 2: CAD‑Dateinamen definieren

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Geben Sie die Namen der CAD‑Dateien an, die Sie im `files`‑Array verarbeiten möchten.

### Schritt 3: PNG‑Exportoptionen festlegen

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurieren Sie die PNG‑Exportoptionen, einschließlich Vektor‑Rasterisierung und Layout‑Einstellungen. Diese Optionen ermöglichen es Ihnen, **CAD zu PNG zu konvertieren** mit der gewünschten Qualität.

### Schritt 4: Durch CAD‑Dateien iterieren

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iterieren Sie über jede angegebene CAD‑Datei, laden Sie sie mit Aspose.CAD und speichern Sie die OLE‑Objekte als PNG‑Bilder. Diese Schleife demonstriert eine einfache Methode, **DWG zu PNG** massenhaft zu konvertieren.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| **Leeres PNG‑Ergebnis** | Layout‑Name stimmt nicht überein | Prüfen Sie, ob der Layout‑Name (`"Layout1"`) im Quell‑DWG vorhanden ist. |
| **Fehlende OLE‑Grafiken** | OLE‑Objekte befinden sich in einem anderen Layout | Binden Sie alle relevanten Layouts in `rasterizationOptions.setLayouts(...)` ein. |
| **Out‑of‑Memory‑Fehler bei großen Dateien** | Hohe DPI‑Einstellungen | Reduzieren Sie die DPI über `rasterizationOptions.setResolution(...)` oder verarbeiten Sie die Dateien einzeln. |

## Häufig gestellte Fragen

**F: Ist Aspose.CAD mit allen CAD‑Dateiformaten kompatibel?**  
A: Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF und DGN. Die vollständige Liste finden Sie in der [Dokumentation](https://reference.aspose.com/cad/java/).

**F: Kann ich die Exporteinstellungen für OLE‑Objekte anpassen?**  
A: Ja, Aspose.CAD bietet umfangreiche Optionen zur Anpassung der Exporteinstellungen, sodass Sie die Ausgabe an Ihre spezifischen Anforderungen anpassen können.

**F: Gibt es eine kostenlose Testversion von Aspose.CAD?**  
A: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion von [hier](https://releases.aspose.com/) ausprobieren.

**F: Wo finde ich Community‑Support für Aspose.CAD?**  
A: Treten Sie der Aspose.CAD‑Community im [Forum](https://forum.aspose.com/c/cad/19) bei, um Hilfe zu erhalten und Erfahrungen auszutauschen.

**F: Wie kann ich eine Lizenz für Aspose.CAD erwerben?**  
A: Besuchen Sie die [Kaufseite](https://purchase.aspose.com/buy), um eine Lizenz zu erhalten, die Ihren Entwicklungsbedürfnissen entspricht.

## Fazit

Mit diesen einfachen, aber leistungsstarken Schritten können Sie nahtlos **CAD als PNG speichern**, während Sie OLE‑Objekte aus CAD‑Dateien mit Aspose.CAD für Java exportieren. Dieses vielseitige Werkzeug befähigt Entwickler, CAD‑Daten effizient zu verwalten und eröffnet neue Möglichkeiten in der CAD‑Anwendungsentwicklung sowie in nachgelagerten bildbasierten Workflows.

---

**Zuletzt aktualisiert:** 2026-03-02  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}