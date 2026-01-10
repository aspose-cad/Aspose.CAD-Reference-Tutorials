---
date: 2026-01-10
description: Lär dig hur du exporterar dgn till dwg och konverterar MicroStation DGN
  till AutoCAD DWG med Aspose.CAD för Java. Steg‑för‑steg‑guide.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Exportera DGN till DWG med Aspose.CAD för Java
url: /sv/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DGN till DWG med Aspose.CAD för Java

## Introduktion

I den här handledningen kommer du att lära dig hur du **export dgn to dwg** och bäddar in en MicroStation DGN‑design i en AutoCAD DWG‑fil med hjälp av Aspose.CAD‑biblioteket för Java. Oavsett om du migrerar äldre MicroStation‑ritningar eller behöver kombinera DGN‑underlays med DWG‑layouter, guidar den här guiden dig genom varje steg — från att konfigurera miljön till att generera en PDF‑förhandsgranskning av den slutgiltiga DWG‑filen.

## Snabba svar
- **Vad uppnår “export dgn to dwg”?** Det bäddar in ett DGN‑underlay i en DWG, vilket möjliggör sömlös visning i AutoCAD.
- **Vilket format kan jag exportera resultatet till för snabb förhandsgranskning?** Du kan **export cad file to pdf** med `PdfOptions`.
- **Behöver jag en licens för att köra koden?** En tillfällig eller betald Aspose.CAD‑licens krävs för produktionsanvändning.
- **Vilken Java‑version stöds?** Java 8 eller senare fungerar med den senaste Aspose.CAD för Java‑utgåvan.
- **Finns det en gratis provversion?** Ja – ladda ner en provversion från Aspose‑webbplatsen.

## Vad är “export dgn to dwg”?
Export av DGN till DWG innebär att konvertera eller bädda in en MicroStation DGN‑design som ett underlay i en AutoCAD DWG‑ritning. Detta gör det möjligt för CAD‑proffs att utnyttja befintliga DGN‑tillgångar utan att återskapa geometri från grunden.

## Varför konvertera MicroStation DGN till AutoCAD DWG?
- **Samarbete:** Team som använder AutoCAD kan visa och redigera DGN‑innehåll direkt.
- **Standardisering:** DWG är det de‑facto‑formatet för många efterföljande arbetsflöden (t.ex. PDF‑generering, 3D‑rendering).
- **Bevarande:** Behåller original‑DGN‑referenser intakta, vilket minskar dataförlust.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:
1. **Aspose.CAD Library:** Ladda ner och installera Aspose.CAD‑biblioteket för Java. Du kan hitta biblioteket [here](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Se till att du har Java installerat på ditt system.
3. **Integrated Development Environment (IDE):** Välj en Java‑IDE som Eclipse eller IntelliJ för en smidigare utvecklingsupplevelse.

## Importera paket

I ditt Java‑projekt importerar du de nödvändiga Aspose.CAD‑paketen för att möjliggöra CAD‑filmanipulation. Här är ett exempel:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Steg 1: Ange filsökvägar

Definiera in- och utdatafilernas sökvägar för DWG‑filen. Uppdatera variablerna `dataDir`, `fileName` och `outPath` enligt dina behov.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Steg 2: Skapa PdfOptions‑instans

Skapa en instans av klassen `PdfOptions`, eftersom vi **exporterar CAD‑filen till PDF** för snabb verifiering.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Steg 3: Läs in DWG‑fil

Läs in den befintliga DWG‑filen som en bild och konvertera den till typen `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Steg 4: Iterera genom enheter

Gå igenom varje enhet i DWG‑filen och kontrollera om den är en bilddefinition. Om så är fallet, hämta den externa referensen till objektet.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Steg 5: Definiera rasteriseringsalternativ

Definiera inställningar för objektet `CadRasterizationOptions`, inklusive sidbredd, höjd, layouter och bakgrundsfärg.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Steg 6: Ställ in vektor‑rasteriseringsalternativ

Ställ in vektor‑rasteriseringsalternativen för exporten.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Steg 7: Exportera DWG till PDF

Slutligen exporterar du DWG till PDF genom att anropa metoden `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|----------|
| **Ingen DGN‑underlay visas** | DWG‑filen innehåller inte en `DGNUNDERLAY`‑entity. | Verifiera att käll‑DWG‑filen inkluderar en DGN‑referens. |
| **PDF är tom** | Rasteriseringsalternativen är satta till nollstorlek eller fel layout. | Se till att `setPageWidth`/`setPageHeight` är positiva och att `setLayouts` matchar DWG‑layoutens namn. |
| **Licensundantag** | Kör utan en giltig Aspose.CAD‑licens. | Applicera en tillfällig eller köpt licens innan du anropar några API‑metoder. |

## Vanliga frågor

### Q1: Var kan jag hitta dokumentationen för Aspose.CAD för Java?

A1: Dokumentationen finns [here](https://reference.aspose.com/cad/java/).

### Q2: Hur kan jag ladda ner Aspose.CAD‑biblioteket för Java?

A2: Du kan ladda ner biblioteket från [this link](https://releases.aspose.com/cad/java/).

### Q3: Finns det en gratis provversion för Aspose.CAD för Java?

A3: Ja, du kan hitta den gratis provversionen [here](https://releases.aspose.com/).

### Q4: Var kan jag få en tillfällig licens för Aspose.CAD för Java?

A4: Skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

### Q5: Behöver du hjälp eller har du frågor?

A5: Besök Aspose.CAD‑community‑support‑forum [here](https://forum.aspose.com/c/cad/19).

### Q6: Kan jag konvertera den resulterande PDF‑filen tillbaka till DWG?

A6: PDF‑filen är en raster‑förhandsgranskning; konvertering tillbaka till DWG kräver ett separat reverse‑engineering‑verktyg.

### Q7: Fungerar detta tillvägagångssätt med andra CAD‑format som DWF eller DXF?

A7: Ja, Aspose.CAD stöder många format; du behöver bara justera filändelserna och rasteriseringsinställningarna därefter.

**Senast uppdaterad:** 2026-01-10  
**Testad med:** Aspose.CAD for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}