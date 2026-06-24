---
date: 2026-05-04
description: Lär dig hur du konverterar dxf till dwg och ställer in primärt teckensnitt
  i Java med Aspose.CAD. Steg‑för‑steg‑guide för perfekta CAD‑visualiseringar.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Ersätt teckensnitt i DWG
second_title: Aspose.CAD Java API
title: Konvertera dxf till dwg och ändra teckensnitt i DWG Aspose.CAD Java
url: /sv/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man laddar DWG-fil i Java och ersätter teckensnitt med Aspose.CAD

## Introduktion

Om du behöver **convert dxf to dwg** i Java‑applikationer och ge dina ritningar ett polerat utseende, är teckensnittsbyte en snabb vinst. Med Aspose.CAD för Java kan du ersätta standardtextstilen med vilket system‑installerat teckensnitt som helst, vilket säkerställer att varje annotation visas exakt som du förväntar dig. I den här handledningen går vi igenom hela processen — från att ladda en DWG‑fil i Java till att använda metoden `setPrimaryFontName` för att ändra teckensnittet.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.CAD för Java.  
- **Kan jag ladda en DWG-fil i Java?** Ja, anropa helt enkelt `Image.load()` på DWG‑sökvägen.  
- **Vilken metod ändrar teckensnittet?** `setPrimaryFontName`.  
- **Behöver jag en licens för produktion?** Ja, en kommersiell licens krävs.  
- **Är batchbearbetning möjlig?** Absolut – loopa igenom flera filer med samma kod.

## Vad är **convert dxf to dwg**?

“Convert dxf to dwg” avser att omvandla en DXF‑fil (Drawing Exchange Format) till det inhemska DWG‑formatet som används av många CAD‑program. Konverteringen gör det möjligt att ta en brett stödjd DXF‑ritning, föra in den i ett DWG‑arbetsflöde och sedan tillämpa avancerad formatering — såsom teckensnittsbyte — med Aspose.CAD.

## Varför ersätta teckensnitt i en DWG-fil?

- **Konsistens:** Säkerställer att alla samarbetspartner ser samma teckensnitt, oavsett deras lokala teckensnittsinställning.  
- **Läsbarhet:** Vissa standard CAD‑teckensnitt är svåra att läsa på skärmar; byte till ett rent teckensnitt som Arial förbättrar tydligheten.  
- **Varumärkesprofil:** Använder tekniska ritningar i enlighet med företagets stilguider.  

## Vanliga användningsfall

| Scenario | Varför det är viktigt |
|----------|-----------------------|
| **Batchkonvertering av äldre DXF-ritningar** | Du kan konvertera dem till DWG och påtvinga ett företags teckensnitt i ett steg. |
| **Förbereda ritningar för kundpresentationer** | Konsekventa, läsbara teckensnitt får dokumenten att se professionella ut. |
| **Automatiserade CAD-pipelines** | Inbäddning av teckensnittsbyte eliminerar manuella efterbearbetningssteg. |

## Förutsättningar

- **Java Development Kit (JDK)** – någon nyare version (8+ rekommenderas).  
- **Aspose.CAD för Java** – ladda ner från [webbplatsen](https://releases.aspose.com/cad/java/).  
- **Exempel DWG/DXF-fil** – en ritning du vill modifiera (du kan använda vilken DWG‑ eller DXF‑fil som helst för testning).

## Importera namnrymder

I ditt Java‑projekt importerar du de nödvändiga klasserna för att arbeta med Aspose.CAD. Dessa importeringar ger dig tillgång till bildladdning, CAD‑specifika objekt och stilmanipulering.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Steg‑för‑steg‑guide för att ersätta teckensnittet

### Steg 1: Ladda din DWG-fil (load dwg file java)

Först pekar du API‑et på platsen för din DWG‑ (eller DXF‑) fil och laddar den i ett `CadImage`‑objekt.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Om du arbetar med DWG‑filer direkt, ersätt filändelsen `.dxf` med `.dwg` i variabeln `srcFile`.

### Steg 2: Iterera över stiltabellen och ange primärt teckensnitt

Varje CAD‑ritning innehåller en samling stilobjekt. Loopa igenom dem och använd metoden `setPrimaryFontName` (API‑anropet som **sätter primärt teckensnitt**) för att ersätta teckensnittet.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Du kan ändra `"Arial"` till vilket teckensnitt som helst som är installerat på maskinen som kör koden.

### Steg 3: Spara den modifierade ritningen

Efter att ha uppdaterat teckensnittet skriver du tillbaka ändringarna till en ny DWG‑fil (eller skriver över den ursprungliga).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Den sparade filen använder nu det teckensnitt du specificerade, och alla textannotationer kommer att renderas med den teckensnittstypen.

## Vanliga problem och lösningar

| Problem | Lösning |
|---------|---------|
| **Teckensnittet tillämpas inte** | Verifiera att teckensnittet är installerat på värd‑OS och att stavningen matchar exakt. |
| **`Image.load` kastar ett undantag** | Se till att filvägen är korrekt och att filen är i ett stödformat för DWG/DXF. |
| **Prestandaförsämring på stora filer** | Processa filer i en separat tråd eller batcha dem för att undvika UI‑blockering. |

## Vanliga frågor

**Q: Påverkar `setPrimaryFontName`‑metoden endast text‑entiteter?**  
A: Den uppdaterar det primära teckensnittet för stiltabellen, vilket i sin tur påverkar alla textelement som refererar till den stilen.

**Q: Kan jag använda ett anpassat teckensnitt som inte är installerat på systemet?**  
A: Aspose.CAD förlitar sig på operativsystemets teckensnittsregister. För att använda ett anpassat teckensnitt, installera det på maskinen som kör koden.

**Q: Är det möjligt att ändra teckensnittet endast för ett enskilt lager?**  
A: Ja, du kan filtrera stilar efter lagernamn innan du anropar `setPrimaryFontName`.

**Q: Vilken version av Aspose.CAD krävs för DWG 2022‑filer?**  
A: Den senaste releasen (från 2025) stödjer fullt ut DWG 2022. Kontrollera alltid versionsnoterna för specifikt formatstöd.

**Q: Hur hanterar jag licensiering i en utvecklingsmiljö?**  
A: Använd en tillfällig evalueringslicens för testning. För produktion, bädda in din köpta licensfil med `License.setLicense("Aspose.Total.Java.lic");`.

**Senast uppdaterad:** 2026-05-04  
**Testat med:** Aspose.CAD för Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}