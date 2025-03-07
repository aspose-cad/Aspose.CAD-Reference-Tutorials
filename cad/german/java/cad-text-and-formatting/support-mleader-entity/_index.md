---
title: Unterstützen Sie MLeader Entity für das DWG-Format mit Aspose.CAD für Java
linktitle: Unterstützt MLeader Entity für das DWG-Format mit Java
second_title: Aspose.CAD Java API
description: Nutzen Sie die Leistungsfähigkeit von Aspose.CAD für Java mit unserem Schritt-für-Schritt-Tutorial zur Unterstützung von MLeader-Entitäten im DWG-Format.
weight: 12
url: /de/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterstützen Sie MLeader Entity für das DWG-Format mit Aspose.CAD für Java

## Einführung

Im Bereich des computergestützten Designs (CAD) mit Java ist das Verständnis und die Implementierung der Unterstützung für MLeader-Entitäten im DWG-Format eine wertvolle Fähigkeit. Aspose.CAD für Java bietet eine robuste Lösung für solche Aufgaben und bietet eine Reihe leistungsstarker Tools und Funktionen. Dieses Tutorial führt Sie durch den Prozess der Unterstützung von MLeader-Entitäten in DWG-Dateien mithilfe von Java mit Aspose.CAD.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System eine Java-Entwicklungsumgebung eingerichtet ist.

2.  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek für Java von herunter und installieren Sie sie[Download-Link](https://releases.aspose.com/cad/java/).

## Namespaces importieren

Importieren Sie in Ihr Java-Projekt die erforderlichen Namespaces, um die Funktionen von Aspose.CAD effektiv zu nutzen. Fügen Sie die folgenden Zeilen in Ihren Code ein:

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

Lassen Sie uns nun den Code in eine Schritt-für-Schritt-Anleitung zur Unterstützung von MLeader-Entitäten für das DWG-Format unter Verwendung von Java mit Aspose.CAD aufschlüsseln.

## 1. Laden Sie die DWG-Datei und greifen Sie auf CadImage zu

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. MLeader-Entitäten validieren

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Überprüfen Sie den MLeader-Stil und die Attribute

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Greifen Sie auf MLeader-Kontextdaten zu

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Kontextattribute validieren

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Greifen Sie auf den MLeader-Knoten und die Führungslinie zu

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

## 7. Validieren Sie zusätzliche MLeader-Attribute

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Textattribute validieren

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Zusätzliche MLeader-Attribute

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich durch die umfassende Anleitung zur Unterstützung von MLeader-Entitäten für das DWG-Format mit Java und Aspose.CAD navigiert. Diese Funktion öffnet Türen für erweiterte CAD-Manipulationen und erweitert Ihr Java-Entwicklungs-Toolkit.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen CAD-Formaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate über DWG hinaus und bietet so Vielseitigkeit bei Ihren Projekten.

### F2: Wo finde ich eine ausführliche Dokumentation für Aspose.CAD für Java?

 A2: Siehe[Dokumentation](https://reference.aspose.com/cad/java/) für detaillierte Einblicke in die Möglichkeiten von Aspose.CAD.

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, erkunden Sie die Funktionen aus erster Hand mit dem[Kostenlose Testphase](https://releases.aspose.com/).

### F4: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

A4: Besorgen Sie sich eine temporäre Lizenz über[dieser Link](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich Community-Unterstützung und Hilfe suchen?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) um mit der Community in Kontakt zu treten und Hilfe zu erhalten.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
