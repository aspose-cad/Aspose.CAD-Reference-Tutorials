---
date: 2026-03-05
description: Lär dig hur du exporterar DWG till PDF, aktiverar dolda linjer och konverterar
  DWG till PDF med Aspose.CAD för Java i den här steg‑för‑steg‑handledningen.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Exportera DWG till PDF med dolda linjer – Aspose.CAD för Java
url: /sv/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DWG till PDF med dolda linjer – Aspose.CAD för Java

## Introduktion

## Snabba svar
- **Vad täcker den här handledningen?** Aktivera rendering av dolda linjer vid export av DWG till PDF med Aspose.CAD för Java.  
- **Vilken primär operation utförs?** `export dwg to pdf`.  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Vad är förutsättningarna?** Java‑utvecklingsmiljö, Aspose.CAD för Java‑biblioteket och DWG‑filer.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för en grundläggande installation.

## Vad är “export dwg to pdf”?

Att exportera en DWG‑fil till PDF konverterar den vektorbaserade CAD‑ritningen till ett portabelt dokumentformat samtidigt som lager, linjetyper och valfri rendering av dolda linjer bevaras. Detta gör det enkelt att dela CAD‑design med intressenter som kanske inte har CAD‑programvara.

## Hur du aktiverar dolda linjer vid export av DWG till PDF

Dolda linjer styrs via layout‑inställningen i rasteriseringsalternativen. Genom att välja layouten **Model** instruerar Aspose.CAD renderaren att behandla dolda kanter som osynliga, vilket ger dig en ren 2‑D‑representation av en 3‑D‑modell.

## Varför aktivera dolda linjer vid export?

Dolda linjer ger en tydligare visuell representation av komplexa 3‑D‑modeller på en 2‑D‑sida, vilket säkerställer att endast synliga kanter betonas. Detta förbättrar läsbarheten och krävs ofta för ingenjörsdokumentation.

## Förutsättningar

1. **Aspose.CAD for Java** – ladda ner biblioteket från den officiella webbplatsen [här](https://releases.aspose.com/cad/java/).  
2. **DWG‑filer** – ha käll‑DWG‑ritningarna lagrade i en känd katalog.  
3. **Java‑utvecklingsmiljö** – JDK 8+ och din föredragna IDE (Eclipse, IntelliJ, etc.).  

Nu när du är klar, låt oss dyka ner i koden.

## Importera namnrymder

Börja med att importera de nödvändiga klasserna så att du kan arbeta med CAD‑bilder och PDF‑alternativ.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Steg 1: Ställ in ditt projekt

Skapa ett Java‑projekt och lägg till Aspose.CAD‑JAR‑filen i din byggsökväg. Definiera sedan katalogen som innehåller dina DWG‑filer.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** Använd en absolut sökväg eller konfigurera en relativ sökväg baserat på ditt projekts resurser‑mapp.

## Steg 2: Läs in DWG‑fil

Läs in käll‑DWG‑filen i ett `CadImage`‑objekt så att du kan manipulera den.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Steg 3: Konfigurera rasteriseringsalternativ

Välj de lager du vill inkludera och ställ in sidstorleken så att den matchar originalritningen. Här aktiverar vi rendering av dolda linjer genom att ange layouten.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Steg 4: Ställ in PDF‑alternativ

Berätta för Aspose.CAD att rasterisera vektordatan till en PDF, med layouten “Model” för att hålla dolda linjer dolda.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Steg 5: Spara resultatet

Slutligen, exportera DWG som en PDF‑fil. De dolda linjerna kommer att respekteras enligt den layout du har angett.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Vanligt fallgropp:** Att glömma att sätta layouten till "Model" kommer göra att alla linjer (inklusive dolda) visas som solida i PDF‑filen.

## Vanliga problem och lösningar

| Problem | Varför det händer | Hur man åtgärdar |
|---------|-------------------|------------------|
| PDF visar alla linjer som solida | Layout är inte inställd på **Model** | Se till att `rasterizationOptions.setLayouts(new String[] { "Model" });` anropas innan du sparar. |
| Saknade lager i resultatet | Felaktiga lagernamn | Verifiera lagernamnen i DWG‑filen och matcha dem exakt i `list`. |
| Minnesbristfel på stora filer | Stor rasteriseringsstorlek | Minska siddimensionerna eller bearbeta ritningen i delar om möjligt. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?
A1: Ja, Aspose.CAD stöder olika CAD‑format som DWG, DXF, DWF och fler.

### Q2: Finns det en gratis provversion tillgänglig för Aspose.CAD för Java?
A2: Ja, du kan hitta den gratis provversionen [här](https://releases.aspose.com/).

### Q3: Hur får jag support för Aspose.CAD för Java?
A3: Besök Aspose.CAD‑forumet [här](https://forum.aspose.com/c/cad/19) för gemenskapsstöd.

### Q4: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för Java?
A4: Se dokumentationen [här](https://reference.aspose.com/cad/java/).

### Q5: Kan jag köpa en tillfällig licens för Aspose.CAD för Java?
A5: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### Q6: Fungerar den här metoden också för att konvertera DWG till PDF i en huvudlös servermiljö?
A6: Absolut. Eftersom koden bara använder Aspose.CAD‑API:t kör den utan några UI‑beroenden, vilket gör den idealisk för automatisering på serversidan.

## Slutsats

Du har nu en komplett, produktionsklar metod för att **export dwg to pdf** med stöd för dolda linjer med hjälp av Aspose.CAD för Java. Detta tillvägagångssätt kan integreras i batch‑bearbetningsverktyg, webbtjänster eller skrivbordsapplikationer för att automatisera CAD‑till‑PDF‑konvertering.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}