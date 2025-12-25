---
date: 2025-12-25
description: Lär dig hur du exporterar DWG till BMP med Aspose.CAD för Java. Denna
  steg‑för‑steg‑guide visar hur du justerar CAD‑ritningsstorlek och konverterar CAD
  till BMP på ett effektivt sätt.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Exportera DWG till BMP – Justera CAD‑storlek med enhetstyp (Java)
url: /sv/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DWG till BMP – Justera CAD-ritningsstorlek med enhetstyp med Aspose.CAD för Java

## Introduktion

När du behöver **exportera DWG till BMP** är det viktigt att kontrollera utskriftsstorleken och måttenheten för efterföljande bearbetning eller utskrift. I den här handledningen lär du dig hur du justerar CAD-ritningsstorlek och konverterar CAD till BMP med Aspose.CAD för Java, genom att använda egenskapen `UnitType` för att definiera måttenheten. Stegen förklaras på ett enkelt språk så att du kan följa med även om du är ny på biblioteket.

## Snabba svar
- **Vad betyder “export DWG till BMP”?** Konverterar en DWG-ritning till en BMP-rasterbild.  
- **Vilken egenskap styr utskriftsstorleken?** `CadRasterizationOptions.setUnitType()` anger enheten (t.ex. centimeter).  
- **Behöver jag en licens för att köra koden?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.  
- **Kan jag välja andra layouter?** Ja, använd `setLayouts()` för att ange modell- eller pappersutrymmeslayouter.  
- **Vilka utskriftsformat stöds?** Förutom BMP kan du exportera till PNG, JPEG, TIFF osv. genom att ändra alternativklassen.

## Vad är **export DWG till BMP**?

Att exportera DWG till BMP innebär att rasterisera en vektorbaserad DWG‑fil till en bitmap‑bild (BMP). Detta är användbart när du behöver en pixel‑perfekt representation för äldre system, bildbehandlingspipelines eller enkla visningsscenarier.

## Varför justera CAD-ritningsstorlek med **Unit Type**?

Genom att ange enhetstypen kan du kontrollera de fysiska dimensionerna på den exporterade bilden utan att manuellt beräkna skalningsfaktorer. Detta säkerställer att bitmap‑filen matchar verkliga mått (t.ex. centimeter), vilket är avgörande för ingenjörsritningar och tryckt dokumentation.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- **Java‑utvecklingsmiljö** – En fungerande JDK (8 eller senare) samt en IDE eller byggverktyg (Maven/Gradle).  
- **Aspose.CAD för Java‑bibliotek** – Ladda ner och integrera Aspose.CAD‑biblioteket i ditt Java‑projekt. Du kan hämta biblioteket [här](https://releases.aspose.com/cad/java/).

## Importera namnrymder

I din Java‑kod, inkludera de nödvändiga namnrymderna för att få åtkomst till Aspose.CAD‑funktioner. Lägg till följande imports:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nu ska vi bryta ner processen för att justera CAD-ritningsstorlek med enhetstyp i hanterbara steg:

## Steg 1: Definiera datakatalog

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ange sökvägen till katalogen där dina CAD‑filer finns.

## Steg 2: Ladda CAD‑ritning

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Ladda CAD‑ritningen med Aspose.CAD:s `Image`‑klass.

## Steg 3: Skapa BMP‑alternativ

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instansiera `BmpOptions`‑klassen för att exportera CAD‑layouten till BMP‑format.

## Steg 4: Konfigurera rasteriseringsalternativ

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Skapa en instans av `CadRasterizationOptions` och associera den med `BmpOptions` för vektor‑rasterisering.

## Steg 5: Ange enhetstyp

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Ange önskad enhetstyp för CAD‑ritningen. I detta exempel har vi satt den till **Centimeter**, vilket direkt påverkar den exporterade bildens storlek när du **justerar CAD‑ritningsstorlek**.

## Steg 6: Ange layouter

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definiera de layouter som ska beaktas under exporten. I detta fall har vi valt layouten **"Model"**, men du kan byta till pappersutrymmes‑layouter om så behövs.

## Steg 7: Exportera till BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Spara slutligen den modifierade CAD‑ritningen i BMP‑format. Detta steg slutför **export DWG till BMP**‑arbetsflödet samtidigt som de storleksjusteringar du konfigurerat bevaras.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|---------|
| **Utdata bilden är för liten** | Enhetstyp inte angiven eller standard (pixel) använd | Anropa `setUnitType()` med önskad måttenhet (t.ex. `UnitType.Centimeter`). |
| **Fel layout exporterad** | Felstavning av layoutnamn | Verifiera layoutnamn med en CAD‑visare; använd exakt sträng i `setLayouts()`. |
| **Licensundantag** | Kör utan en giltig licens i produktion | Tilldela en tillfällig eller permanent licens enligt beskrivningen i FAQ. |

## Vanliga frågor (utökad)

**Q: Kan jag använda Aspose.CAD för Java med andra programmeringsspråk?**  
A: Aspose.CAD stödjer främst Java, men det finns versioner tillgängliga för andra språk som .NET.

**Q: Finns det licensalternativ för Aspose.CAD?**  
A: Ja, du kan utforska licensalternativ och köpa Aspose.CAD [här](https://purchase.aspose.com/buy).

**Q: Finns det en gratis provversion av Aspose.CAD?**  
A: Självklart, du kan få tillgång till en gratis provversion [här](https://releases.aspose.com/).

**Q: Hur kan jag få support för Aspose.CAD för Java?**  
A: Besök Aspose.CAD‑forumet [här](https://forum.aspose.com/c/cad/19) för omfattande support.

**Q: Kan jag skaffa en tillfällig licens för Aspose.CAD?**  
A: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

---

**Senast uppdaterad:** 2025-12-25  
**Testat med:** Aspose.CAD for Java 24.10  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}