---
date: 2025-12-28
description: Erfahren Sie, wie Sie mit Aspose.CAD für Java PDFs aus DWG erstellen,
  DWG als PDF speichern und Text zu DWG‑Zeichnungen hinzufügen – Schritt‑für‑Schritt‑Anleitung.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: PDF aus DWG erstellen und Text mit Aspose.CAD für Java hinzufügen
url: /de/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF aus DWG erstellen und Text hinzufügen mit Aspose.CAD for Java

## Einführung

Wenn Sie **PDF aus DWG**‑Dateien erstellen und gleichzeitig benutzerdefinierten Text einfügen müssen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch den gesamten Prozess – Laden einer DWG‑Zeichnung, Hinzufügen einer Textannotation und schließlich das Speichern des Ergebnisses als PDF mit Aspose.CAD for Java. Am Ende verstehen Sie, wie Sie **DWG als PDF speichern**, die Texthöhe anpassen und sogar grundlegende Anmerkungen hinzufügen können.

## Schnelle Antworten
- **Kann ich DWG in Java zu PDF konvertieren?** Ja, Aspose.CAD for Java bietet eine unkomplizierte API.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Eine kommerzielle Lizenz ist erforderlich; ein kostenloser Test ist verfügbar.  
- **Welche Methode fügt Text zu einem DWG hinzu?** Verwenden Sie das `CadText`‑Objekt und fügen Sie es dem Model Space hinzu.  
- **Kann ich die Texthöhe festlegen?** Natürlich—verwenden Sie `setTextHeight()` beim `CadText`‑Objekt.  
- **Ist die Ausgabe vektor‑basiert?** Wenn die Rasterisierungsoptionen auf `UseObjectColor` gesetzt sind, behält das PDF hochqualitative Vektordaten bei.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:

- Aspose.CAD for Java Library: Laden Sie die Bibliothek von der [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/) herunter und installieren Sie sie.  
- Java Development Kit (JDK): Stellen Sie sicher, dass das neueste JDK auf Ihrem System installiert ist.  
- DWG-Zeichnung: Bereiten Sie eine DWG‑Zeichnungsdatei vor, in die Sie Text einfügen möchten.

## Namespaces importieren

In Ihrem Java‑Code importieren Sie die notwendigen Namespaces für Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Jetzt zerlegen wir das bereitgestellte Code‑Snippet in mehrere Schritte:

## Schritt 1: Dokumentverzeichnis und DWG-Dateipfad einrichten

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Schritt 2: DWG-Bild laden

```java
Image image = Image.load(dwgPathToFile);
```

## Schritt 3: CadText-Objekt erstellen (Text zu DWG hinzufügen)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Schritt 4: Text zu CadImage hinzufügen (Annotation einfügen)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Schritt 5: PDF-Optionen einrichten (Vorbereitung zur Erstellung von PDF aus DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Schritt 6: CadRasterizationOptions konfigurieren (PDF-Rendering steuern)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Schritt 7: Modifiziertes DWG als PDF speichern (dwg zu pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Durch das Befolgen dieser Schritte können Sie **PDF aus DWG** erstellen, benutzerdefinierten Text hinzufügen und die Texthöhe steuern – alles mit nur wenigen Zeilen Java‑Code.

## Warum Text zu DWG hinzufügen und in PDF konvertieren?

Das direkte Hinzufügen von Text zu einer DWG‑Datei ist nützlich für:

- **Markieren von Designs** mit Notizen oder Teilenummern.  
- **Erstellen druckbarer Dokumentation**, bei der das PDF als schreibgeschütztes, weit verbreitetes Format dient.  
- **Automatisierung der Stapelverarbeitung** großer CAD‑Bibliotheken ohne manuelle Bearbeitung.

## Häufige Probleme & Tipps

- **Text erscheint nicht?** Überprüfen Sie, ob die X/Y‑Koordinaten innerhalb der Zeichenbereichsgrenzen liegen und die Ebene sichtbar ist.  
- **Falsche Texthöhe?** Passen Sie `setTextHeight()` an; der Wert ist im Einheitensystem der Zeichnung.  
- **PDF sieht rasterisiert aus?** Stellen Sie sicher, dass `CadDrawTypeMode.UseObjectColor` gesetzt ist, um Vektorinformationen zu erhalten.  
- **Leistung bei großen Dateien?** Erhöhen Sie `pageHeight`/`pageWidth` nur bei Bedarf; größere Werte verbrauchen mehr Speicher.

## Häufig gestellte Fragen

**Q: Ist Aspose.CAD mit allen Versionen von DWG‑Dateien kompatibel?**  
A: Aspose.CAD unterstützt verschiedene Versionen von DWG‑Dateien und gewährleistet damit die Kompatibilität mit einer breiten Palette von CAD‑Software.

**Q: Kann ich die Schriftart und Formatierung des hinzugefügten Textes anpassen?**  
A: Ja, Sie können Schriftart, Stil und weitere Formatierungsoptionen für den zu DWG‑Dateien hinzugefügten Text mit Aspose.CAD anpassen.

**Q: Gibt es eine kostenlose Testversion für Aspose.CAD for Java?**  
A: Ja, Sie können die Funktionen von Aspose.CAD erkunden, indem Sie eine kostenlose Testversion von [hier](https://releases.aspose.com/) erhalten.

**Q: Wo finde ich detaillierte Dokumentation für Aspose.CAD for Java?**  
A: Die Dokumentation finden Sie [hier](https://reference.aspose.com/cad/java/) für ausführliche Informationen und Beispiele.

**Q: Wie kann ich Support erhalten oder Hilfe zu Aspose.CAD bekommen?**  
A: Besuchen Sie das [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), um Unterstützung zu erhalten und sich mit der Community zu vernetzen.

---

**Zuletzt aktualisiert:** 2025-12-28  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}