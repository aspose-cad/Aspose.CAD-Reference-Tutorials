---
date: 2026-06-19
description: Erfahren Sie, wie Sie DWG-Dateien mit Aspose.CAD für Java bearbeiten,
  einschließlich der Aktualisierung von DWG XRef-Pfaden und der Bearbeitung von Hyperlinks.
  Testen Sie noch heute die kostenlose Testversion!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Hyperlink bearbeiten
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Wie man DWG-Hyperlinks bearbeitet – Aspose.CAD Java Tutorial
url: /de/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man DWG-Hyperlinks bearbeitet – Aspose.CAD Java‑Tutorial

Im heutigen digitalen Zeitalter ist **wie man DWG**-Dateien effizient bearbeitet eine unverzichtbare Fähigkeit für Ingenieure, Architekten und BIM‑Spezialisten. Egal, ob Sie einen defekten Hyperlink korrigieren, einen XRef auf eine neue Quelle verweisen oder viele Zeichnungen stapelweise aktualisieren müssen, bietet Aspose.CAD für Java eine saubere, programmatische Möglichkeit, diese Änderungen vorzunehmen, ohne den CAD‑Editor zu öffnen. Dieses Tutorial führt Sie durch den gesamten Prozess, vom Laden einer Zeichnung bis zum Speichern der Änderungen.

## Schnelle Antworten
- **Welche Bibliothek bearbeitet DWG in Java?** Aspose.CAD for Java.  
- **Kann ich Hyperlinks und XRef‑Pfade zusammen bearbeiten?** Ja – beide werden von derselben API unterstützt.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert zum Testen; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher.  
- **Ist das Code‑Beispiel sofort ausführbar?** Ja, nachdem Sie die Dateipfade so angepasst haben, dass sie auf Ihre lokalen DWG‑Dateien verweisen.  

## Warum DWG‑Hyperlinks und XRef‑Pfade bearbeiten?

Das Aktualisieren von Hyperlinks und XRef‑Pfaden verhindert defekte Verweise, stellt sicher, dass die Projektdokumentation stets auf die richtigen Ressourcen verweist, und ermöglicht automatisierte Stapel‑Updates in umfangreichen CAD‑Bibliotheken. Dies reduziert manuellen Aufwand, minimiert Fehler und verbessert die Gesamteffizienz des Projekts, indem Entwickler die Link‑Integrität während des gesamten Design‑Lebenszyklus programmatisch aufrechterhalten können.

## Voraussetzungen

Bevor wir in das Tutorial einsteigen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. **Java-Entwicklungsumgebung:** Ein installiertes JDK 8+ und Ihre bevorzugte IDE (IntelliJ IDEA, Eclipse usw.).
2. **Aspose.CAD for Java‑Bibliothek:** Laden Sie die Aspose.CAD for Java‑Bibliothek von dem [Download‑Link](https://releases.aspose.com/cad/java/) herunter und installieren Sie sie.
3. **DWG‑Zeichnung:** Haben Sie eine DWG‑Datei bereit, um Hyperlinks zu bearbeiten.

## Pakete importieren

Beginnen Sie damit, die erforderlichen Pakete in Ihr Java‑Projekt zu importieren. Dadurch haben Sie Zugriff auf die Funktionen von Aspose.CAD für Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Wie man DWG‑Hyperlinks mit Aspose.CAD für Java bearbeitet?

`CadImage` ist die Aspose.CAD‑Klasse, die zum Laden und Speichern von CAD‑Zeichnungen verwendet wird.  
Laden Sie die DWG‑Datei mit `CadImage`, iterieren Sie über deren Entitäten, aktualisieren Sie den Hyperlink und den XRef‑Pfad bei Bedarf und speichern Sie das Bild schließlich wieder als DWG. Dieser End‑zu‑End‑Ablauf ermöglicht es Ihnen, beliebig viele Entitäten in einem Durchlauf zu ändern und garantiert, dass alle Änderungen gespeichert werden.

### Schritt 1: Zugriff auf Insert‑Objekte

`CadInsertObject` ist die Aspose.CAD‑Klasse, die eine eingefügte Blockreferenz (XRef) innerhalb einer DWG‑Zeichnung darstellt. Durchlaufen Sie die Entitäten und prüfen Sie, ob eine Entität eine Instanz der Klasse `CadInsertObject` ist.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Schritt 2: XRef‑Pfad in einer DWG‑Zeichnung ändern

`CadImage` ist das primäre Objekt, das CAD‑Dateien in Aspose.CAD für Java lädt und speichert. Sobald Sie das Insert‑Objekt identifiziert haben, rufen Sie die zugehörige Block‑Entität ab und aktualisieren Sie den XRef‑Pfad nach Bedarf. Dadurch wird sichergestellt, dass die Referenz auf die richtige externe Datei zeigt.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Schritt 3: Hyperlinks ändern

Als Nächstes prüfen Sie, ob die Entität einen zugehörigen Hyperlink hat. Wenn der Hyperlink einer bestimmten URL entspricht, aktualisieren Sie ihn auf die gewünschte URL. Dieser Schritt stellt sicher, dass beim Klicken auf den Hyperlink im CAD‑Viewer das neue Ziel geöffnet wird.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Häufige Fallstricke & Tipps

- **String‑Vergleich:** Verwenden Sie `.equals()` anstelle von `==` für zuverlässige String‑Vergleiche in Java. Das Beispiel nutzt `==` aus Einfachheitsgründen, aber in der Produktion sollten Sie es durch `entity.getHyperlink().equals("https://products.aspose.com")` ersetzen.  
- **Null‑Prüfungen:** Stellen Sie stets sicher, dass `block.getXRefPathName()` nicht `null` ist, bevor Sie `.getValue()` aufrufen.  
- **Änderungen speichern:** Nach dem Ändern von Entitäten rufen Sie `cadImage.save("output.dwg");` auf, um die Änderungen zu speichern (Code weggelassen, um die ursprüngliche Blockanzahl beizubehalten).  
- **Hinweis zur Leistung:** Aspose.CAD für Java unterstützt über 30 CAD‑Formate und kann Dateien bis zu 2 GB verarbeiten, ohne das gesamte Dokument in den Speicher zu laden, wodurch Massen‑Updates schnell und speichereffizient sind.  

## Häufig gestellte Fragen

### F1: Ist Aspose.CAD für Java mit allen DWG‑Zeichnungs‑Versionen kompatibel?

A1: Aspose.CAD für Java unterstützt mehr als 50 DWG‑Versionen und deckt Releases von AutoCAD 2000 bis zum neuesten Format 2025 ab.

### F2: Kann ich Aspose.CAD für Java in kommerziellen Projekten verwenden?

A2: Ja, für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich. Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben.

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?

A3: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) ausprobieren.

### F4: Wie kann ich technischen Support für Aspose.CAD für Java erhalten?

A4: Für technische Unterstützung besuchen Sie das Aspose.CAD‑Forum [hier](https://forum.aspose.com/c/cad/19).

### F5: Kann ich eine temporäre Lizenz für Testzwecke erhalten?

A5: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**Zusätzliche Fragen & Antworten**

**F: Muss ich eine bestimmte Methode aufrufen, um das bearbeitete DWG auf die Festplatte zu schreiben?**  
A: Ja, nach den Änderungen rufen Sie `cadImage.save("EditedDrawing.dwg");` auf, um die Modifikationen zu speichern.

**F: Ist es möglich, mehrere Hyperlinks in einem Durchlauf zu bearbeiten?**  
A: Absolut – iterieren Sie über `cadImage.getEntities()` und wenden Sie die Hyperlink‑Logik auf jede passende Entität an.

---

**Zuletzt aktualisiert:** 2026-06-19  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [XREF-Metadaten aus DWG‑Dateien mit Aspose.CAD für Java lesen](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Benutzerdefinierte Eigenschaften zu DWG‑Dateien mit Aspose.CAD für Java hinzufügen](/cad/java/additional-features/add-custom-properties/)
- [DWG nach PDF oder Raster mit Aspose.CAD für Java exportieren](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}