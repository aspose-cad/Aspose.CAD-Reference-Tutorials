---
date: 2026-05-04
description: Erfahren Sie, wie Sie DXF in DWG konvertieren und die Primärschriftart
  in Java mit Aspose.CAD festlegen. Schritt‑für‑Schritt‑Anleitung für perfekte CAD‑Visualisierungen.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Schriftart in DWG ersetzen
second_title: Aspose.CAD Java API
title: DXF zu DWG konvertieren und Schriftart in DWG mit Aspose.CAD Java ändern
url: /de/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man DWG-Datei in Java lädt und Schriftart mit Aspose.CAD ersetzt

## Einleitung

Wenn Sie in Java‑Anwendungen **convert dxf to dwg** benötigen und Ihren Zeichnungen ein professionelles Aussehen verleihen möchten, ist das Ersetzen der Schriftart ein schneller Gewinn. Mit Aspose.CAD für Java können Sie den Standard‑Textstil durch jede systeminstallierte Schriftart ersetzen und sicherstellen, dass jede Anmerkung genau so erscheint, wie Sie es erwarten. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer DWG‑Datei in Java bis zur Verwendung der Methode `setPrimaryFontName`, um die Schriftart zu ändern.

## Schnelle Antworten
- **Welche Bibliothek benötige ich?** Aspose.CAD für Java.  
- **Kann ich eine DWG‑Datei in Java laden?** Ja, rufen Sie einfach `Image.load()` mit dem DWG‑Pfad auf.  
- **Welche Methode ändert die Schriftart?** `setPrimaryFontName`.  
- **Benötige ich eine Lizenz für die Produktion?** Ja, eine kommerzielle Lizenz ist erforderlich.  
- **Ist die Stapelverarbeitung möglich?** Absolut – durchlaufen Sie mehrere Dateien mit demselben Code.

## Was ist **convert dxf to dwg**?

„Convert dxf to dwg“ bezieht sich auf die Umwandlung einer DXF‑Datei (Drawing Exchange Format) in das native DWG‑Format, das von vielen CAD‑Anwendungen verwendet wird. Durch die Konvertierung können Sie eine weit verbreitete DXF‑Zeichnung in einen DWG‑Workflow einbinden und anschließend erweiterte Formatierungen – wie das Ersetzen von Schriftarten – mit Aspose.CAD anwenden.

## Warum Schriftarten in einer DWG-Datei ersetzen?

- **Konsistenz:** Gewährleistet, dass alle Mitwirkenden dieselbe Schriftart sehen, unabhängig von ihrer lokalen Schriftkonfiguration.  
- **Lesbarkeit:** Einige Standard‑CAD‑Schriften sind auf Bildschirmen schwer zu lesen; das Ersetzen durch eine klare Schrift wie Arial verbessert die Klarheit.  
- **Branding:** Passt technische Zeichnungen an die Unternehmens‑Style‑Guidelines an.  

## Häufige Anwendungsfälle

| Szenario | Warum es wichtig ist |
|----------|----------------------|
| **Batch‑Konvertierung von Legacy‑DXF‑Zeichnungen** | Sie können sie in DWG konvertieren und in einem Durchgang eine Unternehmensschriftart durchsetzen. |
| **Vorbereitung von Zeichnungen für Kundenpräsentationen** | Konsistente, gut lesbare Schriftarten lassen die Dokumente professionell wirken. |
| **Automatisierte CAD‑Pipelines** | Das Einbetten der Schriftart‑Ersetzung eliminiert manuelle Nachbearbeitungsschritte. |

## Voraussetzungen

- **Java Development Kit (JDK)** – jede aktuelle Version (8+ empfohlen).  
- **Aspose.CAD für Java** – Download von der [website](https://releases.aspose.com/cad/java/).  
- **Beispiel‑DWG/DXF‑Datei** – eine Zeichnung, die Sie ändern möchten (Sie können jede DWG‑ oder DXF‑Datei zum Testen verwenden).

## Namespaces importieren

In Ihrem Java‑Projekt importieren Sie die erforderlichen Klassen, um mit Aspose.CAD zu arbeiten. Diese Importe geben Ihnen Zugriff auf das Laden von Bildern, CAD‑spezifische Objekte und die Stilmanipulation.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Schritt‑für‑Schritt‑Anleitung zum Ersetzen der Schriftart

### Schritt 1: Laden Sie Ihre DWG-Datei (load dwg file java)

Zuerst zeigen Sie die API auf den Speicherort Ihrer DWG‑ (oder DXF‑) Datei und laden sie in ein `CadImage`‑Objekt.

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

### Schritt 3: Speichern Sie die modifizierte Zeichnung

Nachdem Sie die Schriftart aktualisiert haben, schreiben Sie die Änderungen zurück in eine neue DWG‑Datei (oder überschreiben die Originaldatei).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Die gespeicherte Datei verwendet nun die von Ihnen angegebene Schriftart, und jede Textanmerkung wird mit diesem Schriftschnitt dargestellt.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|---------|--------|
| **Schriftart nicht angewendet** | Vergewissern Sie sich, dass die Schriftart im Host‑OS installiert ist und die Schreibweise exakt übereinstimmt. |
| **`Image.load` wirft eine Ausnahme** | Stellen Sie sicher, dass der Dateipfad korrekt ist und die Datei ein unterstütztes DWG/DXF‑Format hat. |
| **Leistungsabfall bei großen Dateien** | Verarbeiten Sie Dateien in einem separaten Thread oder stapeln Sie sie, um UI‑Blockierungen zu vermeiden. |

## Häufig gestellte Fragen

**F: Wirkt die Methode `setPrimaryFontName` nur auf Textelemente?**  
A: Sie aktualisiert die primäre Schriftart für die Stiltabelle, die wiederum alle Textobjekte beeinflusst, die diesen Stil referenzieren.

**F: Kann ich eine benutzerdefinierte Schriftart verwenden, die nicht im System installiert ist?**  
A: Aspose.CAD nutzt das Schriftarten‑Register des Betriebssystems. Um eine benutzerdefinierte Schriftart zu verwenden, installieren Sie sie auf dem Rechner, auf dem der Code ausgeführt wird.

**F: Ist es möglich, die Schriftart nur für eine einzelne Ebene zu ändern?**  
A: Ja, Sie können Stile nach Ebenennamen filtern, bevor Sie `setPrimaryFontName` aufrufen.

**F: Welche Version von Aspose.CAD wird für DWG‑2022‑Dateien benötigt?**  
A: Die neueste Version (Stand 2025) unterstützt DWG 2022 vollständig. Prüfen Sie stets die Versionshinweise für die spezifische Formatunterstützung.

**F: Wie gehe ich mit Lizenzen in einer Entwicklungsumgebung um?**  
A: Verwenden Sie eine temporäre Evaluierungslizenz zum Testen. Für die Produktion betten Sie Ihre erworbene Lizenzdatei mit `License.setLicense("Aspose.Total.Java.lic");` ein.

**Zuletzt aktualisiert:** 2026-05-04  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}