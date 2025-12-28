---
date: 2025-12-28
description: Erfahren Sie, wie Sie DWG‑Dateien in Java‑Projekten laden und den primären
  Schriftartnamen mit Aspose.CAD für Java festlegen. Schritt‑für‑Schritt‑Anleitung
  für perfekte CAD‑Visualisierungen.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Wie man eine DWG-Datei in Java lädt und die Schriftart mit Aspose.CAD ersetzt
url: /de/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man DWG‑Datei in Java lädt und Schriftart mit Aspose.CAD ersetzt

## Einführung

Wenn Sie **DWG‑Dateien in Java** laden müssen und Ihren Zeichnungen ein professionelles Aussehen verleihen wollen, ist das Ersetzen der Schriftart ein schneller Gewinn. Mit Aspose.CAD für Java können Sie den Standard‑Textstil durch jede im System installierte Schriftart ersetzen, sodass jede Anmerkung genau so erscheint, wie Sie es erwarten. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer DWG‑Datei in Java bis zur Verwendung der Methode `setPrimaryFontName`, um die Schriftart zu ändern.

## Schnelle Antworten
- **Welche Bibliothek benötige ich?** Aspose.CAD for Java.
- **Kann ich eine DWG‑Datei in Java laden?** Ja, rufen Sie einfach `Image.load()` mit dem DWG‑Pfad auf.
- **Welche Methode ändert die Schriftart?** `setPrimaryFontName`.
- **Benötige ich eine Lizenz für die Produktion?** Ja, eine kommerzielle Lizenz ist erforderlich.
- **Ist Batch‑Verarbeitung möglich?** Absolut – iterieren Sie über mehrere Dateien mit demselben Code.

## Was bedeutet „DWG‑Datei in Java laden“?

Das Laden einer DWG‑Datei in einer Java‑Umgebung bedeutet, die binären CAD‑Daten in ein `Image`‑Objekt zu lesen, das Aspose.CAD manipulieren kann. Sobald die Datei geladen ist, haben Sie vollen programmatischen Zugriff auf Ebenen, Stile und Textelemente.

## Warum Schriftarten in einer DWG‑Datei ersetzen?

- **Konsistenz:** Gewährleistet, dass alle Mitarbeitenden dieselbe Schriftart sehen, unabhängig von ihrer lokalen Schriftkonfiguration.  
- **Lesbarkeit:** Einige Standard‑CAD‑Schriften sind auf Bildschirmen schwer lesbar; das Austauschen gegen eine klare Schrift wie Arial verbessert die Klarheit.  
- **Branding:** Passt technische Zeichnungen an die Unternehmens‑Styleguidelines an.

## Voraussetzungen

- **Java Development Kit (JDK)** – jede aktuelle Version (empfohlen 8+).  
- **Aspose.CAD for Java** – Download von der [Website](https://releases.aspose.com/cad/java/).  
- **Beispiel‑DWG‑Datei** – eine Zeichnung, die Sie ändern möchten (Sie können jede DWG‑ oder DXF‑Datei zum Testen verwenden).

## Namensräume importieren

Importieren Sie in Ihrem Java‑Projekt die erforderlichen Klassen, um mit Aspose.CAD zu arbeiten. Diese Importe geben Ihnen Zugriff auf das Laden von Bildern, CAD‑spezifische Objekte und die Stilmanipulation.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Schritt‑für‑Schritt‑Anleitung zum Ersetzen der Schriftart

### Schritt 1: Laden Sie Ihre DWG‑Datei (DWG‑Datei in Java laden)

Zuerst zeigen Sie der API auf den Speicherort Ihrer DWG‑ (oder DXF‑) Datei und laden sie in ein `CadImage`‑Objekt.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro‑Tipp:** Wenn Sie direkt mit DWG‑Dateien arbeiten, ersetzen Sie die Erweiterung `.dxf` durch `.dwg` in der Variable `srcFile`.

### Schritt 2: Durchlaufen Sie die Stiltabelle und setzen Sie den primären Schriftartnamen

Jede CAD‑Zeichnung enthält eine Sammlung von Stilobjekten. Durchlaufen Sie diese und verwenden Sie die Methode `setPrimaryFontName` (der API‑Aufruf, der **den primären Schriftartnamen setzt**), um die Schriftart zu ersetzen.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Sie können `"Arial"` durch jede Schriftart ersetzen, die auf dem ausführenden Rechner installiert ist.

### Schritt 3: Speichern Sie die geänderte Zeichnung

Nachdem die Schriftart aktualisiert wurde, schreiben Sie die Änderungen zurück in eine neue DWG‑Datei (oder überschreiben die Originaldatei).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Die gespeicherte Datei verwendet nun die von Ihnen angegebene Schriftart, und jede Textanmerkung wird mit diesem Schriftschnitt dargestellt.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Schriftart nicht angewendet** | Stellen Sie sicher, dass die Schriftart auf dem Host‑OS installiert ist und die Schreibweise exakt übereinstimmt. |
| **`Image.load` wirft eine Ausnahme** | Stellen Sie sicher, dass der Dateipfad korrekt ist und die Datei ein unterstütztes DWG/DXF‑Format hat. |
| **Leistungsabfall bei großen Dateien** | Verarbeiten Sie Dateien in einem separaten Thread oder stapeln Sie sie, um UI‑Blockierungen zu vermeiden. |

## FAQ's

### Q1: Kann ich Schriftart‑Ersetzungen in meiner DWG‑Datei rückgängig machen?

A1: Ja, Sie können Schriftart‑Ersetzungen rückgängig machen, indem Sie die ursprüngliche DWG‑Datei erneut laden oder die Undo‑Funktion Ihrer CAD‑Software verwenden.

### Q2: Gibt es Einschränkungen bei Schriftart‑Ersetzungen in Aspose.CAD für Java?

A2: Die Möglichkeiten zur Schriftart‑Ersetzung hängen von den im System verfügbaren Schriftarten ab. Stellen Sie sicher, dass die gewünschte Schriftart zugänglich ist, oder erwägen Sie, sie in die DWG‑Datei einzubetten.

### Q3: Wie kann ich während der Ersetzung die Schriftgröße anpassen?

A3: Schriftgrößen können angepasst werden, indem Sie auf die Stileigenschaften in Aspose.CAD zugreifen und die Schriftgröße entsprechend ändern.

### Q4: Kann ich die Schriftart‑Ersetzung in einem Batch‑Prozess automatisieren?

A4: Ja, Aspose.CAD für Java unterstützt Batch‑Verarbeitung. Sie können Schriftart‑Ersetzungen über mehrere DWG‑Dateien hinweg mittels Skripting oder Programmierung automatisieren.

### Q5: Ist Aspose.CAD für Java mit den neuesten CAD‑Dateiformaten kompatibel?

A5: Ja, Aspose.CAD für Java wird regelmäßig aktualisiert, um die neuesten CAD‑Dateiformate zu unterstützen und die Kompatibilität mit Industriestandards sicherzustellen.

## Häufig gestellte Fragen

**F: Wirkt die Methode `setPrimaryFontName` nur auf Textelemente?**  
A: Sie aktualisiert die primäre Schriftart für die Stiltabelle, was wiederum alle Textelemente beeinflusst, die diesen Stil referenzieren.

**F: Kann ich eine benutzerdefinierte Schriftart verwenden, die nicht im System installiert ist?**  
A: Aspose.CAD nutzt das Schriftarten‑Register des Betriebssystems. Um eine benutzerdefinierte Schriftart zu verwenden, installieren Sie sie auf dem Rechner, auf dem der Code ausgeführt wird.

**F: Ist es möglich, die Schriftart nur für eine einzelne Ebene zu ändern?**  
A: Ja, Sie können Stile nach Ebenennamen filtern, bevor Sie `setPrimaryFontName` aufrufen.

**F: Welche Version von Aspose.CAD wird für DWG‑2022‑Dateien benötigt?**  
A: Die neueste Version (Stand 2025) unterstützt DWG 2022 vollständig. Prüfen Sie stets die Versionshinweise für spezifische Formatunterstützung.

**F: Wie gehe ich mit Lizenzierung in einer Entwicklungsumgebung um?**  
A: Verwenden Sie eine temporäre Evaluationslizenz zum Testen. Für die Produktion betten Sie Ihre erworbene Lizenzdatei mit `License.setLicense("Aspose.Total.Java.lic");` ein.

---

**Zuletzt aktualisiert:** 2025-12-28  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}