---
date: 2026-01-10
description: Erfahren Sie, wie Sie DWG‑Dateien lesen und Multileader‑DWG‑Entitäten
  mit Aspose.CAD für Java in diesem Schritt‑für‑Schritt‑Tutorial erstellen.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Wie man DWG liest und MLeader mit Aspose.CAD für Java unterstützt
url: /de/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man DWG liest und MLeader mit Aspose.CAD für Java unterstützt

## Einführung

Wenn Sie **DWG**‑Dateien **lesen** und mit **multileader DWG**‑Entitäten in einer Java‑Anwendung arbeiten müssen, sind Sie hier genau richtig. Aspose.CAD für Java bietet Ihnen eine saubere, programmatische Möglichkeit, DWG‑Zeichnungen zu öffnen, MLeader‑Objekte zu inspizieren und deren Eigenschaften zu validieren – und das alles, ohne eine vollwertige CAD‑Arbeitsstation zu benötigen. In diesem Tutorial führen wir Sie Schritt für Schritt durch den gesamten Prozess, vom Laden einer DWG‑Datei bis zum Bestätigen, dass die Multileader‑Daten dem erwarteten Stil entsprechen.

## Schnelle Antworten
- **Was bedeutet „wie man DWG liest“?** Laden der DWG mit `Image.load()` und Umwandlung in `CadImage`.
- **Kann ich multileader DWG‑Entitäten erstellen?** Ja – Sie können MLeader‑Objekte mit der CadMLeader‑API hinzufügen, bearbeiten und validieren.
- **Welche Bibliotheksversion wird benötigt?** Jede aktuelle Aspose.CAD für Java‑Version (die gezeigte API funktioniert mit den Builds 2024+).
- **Benötige ich eine Lizenz für die Entwicklung?** Eine temporäre Lizenz reicht für Tests; für die Produktion ist eine Voll‑Lizenz erforderlich.
- **Ist der Code plattformübergreifend?** Absolut – Java läuft unter Windows, Linux und macOS.

## Was bedeutet „wie man DWG liest“ mit Aspose.CAD?

Das Lesen einer DWG‑Datei bedeutet, die binäre Zeichnung in ein In‑Memory‑`CadImage`‑Objekt zu konvertieren. Sobald Sie dieses Objekt besitzen, können Sie seine Entitäten (Linien, Kreise, Text, **MLeader**‑Objekte usw.) enumerieren und deren Eigenschaften inspizieren.

## Warum MLeader‑Entitäten unterstützen?

MLeader (Multileader)‑Objekte kombinieren Führungs‑Linien mit angehängtem Text oder Blöcken und sind damit unverzichtbar für Anmerkungen in technischen Zeichnungen. Die Unterstützung ermöglicht Ihnen:

- Überprüfen, dass Anmerkungen den Unternehmensstandards entsprechen.
- Text für nachgelagerte Verarbeitung extrahieren (z. B. Stücklisten‑Erstellung).
- Programmatisch Führungs‑Stile ändern oder Blockinhalt ersetzen.

## Voraussetzungen

Bevor wir starten, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java‑Entwicklungsumgebung** – JDK 11+ und Ihre bevorzugte IDE (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD für Java** – Laden Sie das neueste JAR von dem [Download‑Link](https://releases.aspose.com/cad/java/) herunter.  

## Namespaces importieren

Fügen Sie die folgenden Importe zu Ihrer Java‑Klasse hinzu, damit Sie mit DWG‑Entitäten und Rasterisierungsoptionen arbeiten können:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Wie man DWG‑Dateien mit Aspose.CAD für Java liest

### Schritt 1: Laden der DWG‑Datei und Erhalten eines `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Schritt 2: Validieren, dass die Zeichnung MLeader‑Entitäten enthält

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Schritt 3: MLeader‑Stil und Grundattribute überprüfen

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Schritt 4: Zugriff auf die MLeader‑Kontextdaten (das Herz des Multileaders)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Schritt 5: Kontext‑Ebene Attribute validieren

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Schritt 6: Arbeiten mit dem MLeader‑Knoten und seiner Führungs‑Linie

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Schritt 7: Zusätzliche MLeader‑Knoten‑Attribute validieren

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Schritt 8: Text‑bezogene Eigenschaften prüfen

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Schritt 9: Weitere MLeader‑Attribute zur Vollständigkeit überprüfen

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| `ClassCastException` beim Casten der Entität | Der ausgewählte Index ist kein MLeader‑Objekt. | Überprüfen Sie `cadImage.getEntities()[i] instanceof CadMLeader` bevor Sie casten. |
| `null`‑Werte für Führungs‑Linien‑Punkte | Die Zeichnung verwendet einen benutzerdefinierten Führungsstil, der nicht vollständig unterstützt wird. | Verwenden Sie die neueste Aspose.CAD‑Version oder greifen Sie für Tests auf den Standardstil zurück. |
| Assertions‑Fehler bei numerischen Werten | Geringe Rundungsunterschiede zwischen CAD‑Versionen. | Passen Sie die Toleranz in `Assert.areEqual(..., delta)` wie in den Beispielen an. |

## Häufig gestellte Fragen

**Q: Kann ich Aspose.CAD für Java mit anderen CAD‑Formaten verwenden?**  
A: Ja, Aspose.CAD unterstützt neben DWG auch DXF, DWF, DGN und mehrere Rasterformate.

**Q: Wo finde ich detaillierte Dokumentation für Aspose.CAD für Java?**  
A: Siehe die offizielle [Dokumentation](https://reference.aspose.com/cad/java/) für API‑Details und Code‑Beispiele.

**Q: Gibt es eine kostenlose Testversion?**  
A: Absolut – Sie können eine Testversion von der [Free‑Trial](https://releases.aspose.com/)‑Seite herunterladen.

**Q: Wie erhalte ich eine temporäre Lizenz für Tests?**  
A: Holen Sie sich eine temporäre Lizenz über den [Temporary‑License‑Link](https://purchase.aspose.com/temporary-license/).

**Q: Wo kann ich die Community um Hilfe bitten?**  
A: Das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) ist der beste Ort, um Fragen zu stellen und Lösungen zu teilen.

## Fazit

Sie haben nun eine vollständige, durchgängige Anleitung, wie Sie **DWG‑Dateien lesen** und **multileader DWG‑Entitäten erstellen** mit Aspose.CAD für Java. Durch Befolgen der obigen Schritte können Sie MLeader‑Stile validieren, Anmerkungsdaten extrahieren und die DWG‑Verarbeitung in jeden Java‑basierten Workflow integrieren.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-01-10  
**Getestet mit:** Aspose.CAD 24.11 für Java  
**Autor:** Aspose