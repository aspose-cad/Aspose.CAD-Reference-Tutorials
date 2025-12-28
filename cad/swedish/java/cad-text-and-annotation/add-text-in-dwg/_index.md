---
date: 2025-12-28
description: Lär dig hur du skapar PDF från DWG, sparar DWG som PDF och lägger till
  text i DWG-ritningar med Aspose.CAD för Java – steg‑för‑steg‑guide.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Skapa PDF från DWG och lägg till text med Aspose.CAD för Java
url: /sv/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PDF från DWG och lägg till text med Aspose.CAD för Java

## Introduktion

Om du behöver **create PDF from DWG**-filer samtidigt som du infogar anpassad text, är du på rätt plats. I den här handledningen går vi igenom hela processen — laddar en DWG-ritning, lägger till en textannotation och sparar slutligen resultatet som en PDF med Aspose.CAD för Java. I slutet kommer du att förstå hur du **save DWG as PDF**, anpassar texthöjd och även lägger till grundläggande annotationer.

## Snabba svar
- **Kan jag konvertera DWG till PDF i Java?** Ja, Aspose.CAD för Java tillhandahåller ett enkelt API.  
- **Behöver jag en licens för produktionsanvändning?** En kommersiell licens krävs; en gratis provversion finns tillgänglig.  
- **Vilken metod lägger till text i en DWG?** Använd `CadText`-objektet och lägg till det i modellutrymmet.  
- **Kan jag ange texthöjden?** Absolut — använd `setTextHeight()` på `CadText`-instansen.  
- **Är utdata vektorbaserad?** När rasteriseringsalternativen är inställda på `UseObjectColor` behåller PDF:en högkvalitativ vektordata.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för Java-biblioteket: Ladda ner och installera biblioteket från [Aspose.CAD for Java-sidan](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Se till att du har den senaste JDK:n installerad på ditt system.
- DWG-ritning: Förbered en DWG-ritningsfil där du vill lägga till text.

## Importera namnrymder

I din Java-kod, importera de nödvändiga namnrymderna för Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nu ska vi bryta ner kodsnutten som tillhandahålls i flera steg:

## Steg 1: Ställ in dokumentkatalog och DWG-filväg

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Steg 2: Ladda DWG-bild

```java
Image image = Image.load(dwgPathToFile);
```

## Steg 3: Skapa CadText-objekt (Lägg till text i DWG)

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

## Steg 4: Lägg till text i CadImage (Infoga annotation)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Steg 5: Ställ in PDF-alternativ (Förbered för att skapa PDF från DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Steg 6: Konfigurera CadRasterizationOptions (Styr PDF-rendering)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Steg 7: Spara den modifierade DWG som PDF (dwg till pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Genom att följa dessa steg kommer du att kunna **create PDF from DWG**, lägga till anpassad text och styra texthöjden — allt med bara några rader Java-kod.

## Varför lägga till text i DWG och konvertera till PDF?

Att lägga till text direkt i en DWG-fil är användbart för:

- **Märka upp designer** med anteckningar eller delnummer.
- **Skapa utskrivbar dokumentation** där PDF:en fungerar som ett skrivskyddat, allmänt stödd format.
- **Automatisera batchbearbetning** av stora CAD-bibliotek utan manuell redigering.

## Vanliga problem och tips

- **Texten visas inte?** Verifiera att X/Y-koordinaterna ligger inom ritningens omfång och att lagret är synligt.
- **Fel texthöjd?** Justera `setTextHeight()`; värdet är i ritningens enhetssystem.
- **PDF ser rasteriserad ut?** Se till att `CadDrawTypeMode.UseObjectColor` är inställt för att behålla vektorinformation.
- **Prestanda på stora filer?** Öka `pageHeight`/`pageWidth` endast vid behov; större värden förbrukar mer minne.

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med alla versioner av DWG-filer?**  
A: Aspose.CAD stöder olika versioner av DWG-filer, vilket säkerställer kompatibilitet med ett brett spektrum av CAD-programvara.

**Q: Kan jag anpassa teckensnittet och formateringen av den tillagda texten?**  
A: Ja, du kan anpassa teckensnitt, stil och andra formateringsalternativ för texten som läggs till i DWG-filer med Aspose.CAD.

**Q: Finns det en gratis provversion av Aspose.CAD för Java?**  
A: Ja, du kan utforska funktionerna i Aspose.CAD genom att skaffa en gratis provversion från [här](https://releases.aspose.com/).

**Q: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för Java?**  
A: Se dokumentationen [här](https://reference.aspose.com/cad/java/) för djupgående information och exempel.

**Q: Hur kan jag få support eller hjälp med Aspose.CAD?**  
A: Besök [Aspose.CAD-forumet](https://forum.aspose.com/c/cad/19) för att få hjälp och ansluta till communityn.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}