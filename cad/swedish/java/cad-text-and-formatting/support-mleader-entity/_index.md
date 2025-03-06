---
title: Stöd MLeader Entity för DWG-format med Aspose.CAD för Java
linktitle: Stöd MLeader Entity för DWG-format med Java
second_title: Aspose.CAD Java API
description: Lås upp kraften i Aspose.CAD för Java med vår steg-för-steg handledning om att stödja MLeader-enheter i DWG-format.
weight: 12
url: /sv/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stöd MLeader Entity för DWG-format med Aspose.CAD för Java

## Introduktion

Inom området datorstödd design (CAD) med Java är det en värdefull färdighet att förstå och implementera stöd för MLeader-enheter i DWG-format. Aspose.CAD för Java tillhandahåller en robust lösning för sådana uppgifter, och erbjuder en uppsättning kraftfulla verktyg och funktioner. Denna handledning guidar dig genom processen att stödja MLeader-enheter i DWG-filer med Java med Aspose.CAD.

## Förutsättningar

Innan vi går in i handledningen, se till att du har följande förutsättningar på plats:

1. Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på ditt system.

2.  Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket för Java från[nedladdningslänk](https://releases.aspose.com/cad/java/).

## Importera namnområden

Importera de nödvändiga namnrymden i ditt Java-projekt för att effektivt utnyttja funktionerna i Aspose.CAD. Inkludera följande rader i din kod:

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

Låt oss nu dela upp koden i en steg-för-steg-guide för att stödja MLeader-enheter för DWG-format med Java med Aspose.CAD.

## 1. Ladda DWG-fil och få åtkomst till CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Validera MLeader Entities

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Verifiera MLeader-stil och attribut

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Få åtkomst till MLeader-kontextdata

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Validera kontextattribut

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Åtkomst till MLeader Node och Leader Line

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

## 7. Validera ytterligare MLeader-attribut

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Validera textattribut

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Ytterligare MLeader-attribut

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Slutsats

Grattis! Du har framgångsrikt navigerat igenom den omfattande guiden om att stödja MLeader-enheter för DWG-format med Java och Aspose.CAD. Denna förmåga öppnar dörrar till avancerade CAD-manipulationer och förbättrar din Java-utvecklingsverktygssats.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra CAD-format?

S1: Ja, Aspose.CAD stöder olika CAD-format utöver DWG, vilket ger mångsidighet i dina projekt.

### F2: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för Java?

 A2: Se[dokumentation](https://reference.aspose.com/cad/java/) för djupgående insikter i Aspose.CAD:s möjligheter.

### F3: Finns det en gratis provperiod?

 S3: Ja, utforska funktionerna på egen hand med[gratis provperiod](https://releases.aspose.com/).

### F4: Hur kan jag få tillfällig licens för Aspose.CAD?

A4: Skaffa en tillfällig licens genom[den här länken](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag söka stöd och hjälp från samhället?

A5: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) att få kontakt med samhället och få hjälp.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
