---
date: 2026-10-19
description: Lär dig hur du skapar PNG‑miniaturebild‑filer för IFC med Aspose.CAD
  for Java på bara några rader kod.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exportera IFC till PNG
og_description: Skapa PNG‑miniaturebild‑filer för IFC enkelt med Aspose.CAD for Java.
  Denna steg‑för‑steg‑guide visar hur du laddar, rasterize, och sparar IFC‑modeller
  som högkvalitativa PNG‑bilder.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Skapa PNG‑miniaturebild för IFC med Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Hur man skapar PNG‑miniaturebild för IFC med Aspose.CAD for Java
url: /sv/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera IFC till PNG med Aspose.CAD för Java

## Introduktion

I den här handledningen kommer du att lära dig hur du **skapar PNG‑miniatyr‑IFC**‑filer med Aspose.CAD för Java. Oavsett om du behöver snabba förhandsgranskningar för en BIM‑portal, generera miniatyrbilder för ett dokumenthanteringssystem eller automatisera batch‑konverteringar, låter stegen nedan dig rasterisera en 3‑D‑IFC‑modell till en skarp 2‑D‑PNG‑bild med bara några rader Java‑kod.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.CAD for Java.  
- **Kan jag skapa en PNG‑miniatyr‑IFC med några rader kod?** Ja – hela arbetsflödet ryms på under 20 rader.  
- **Behöver jag en licens för produktion?** En tillfällig licens fungerar för testning; en full licens krävs för kommersiell distribution.  
- **Är utdata skalbara?** Du kan ange valfri pixelstorlek, så PNG‑en skalar till vilken storlek du behöver.  
- **Vilken Java‑version stöds?** Java 8 eller högre.

## Vad är “convert IFC to PNG”?
Att konvertera IFC (Industry Foundation Classes) till PNG betyder att rasterisera den 3‑D‑byggnadsmodellen till en 2‑D‑bitmap‑bild. Denna process skapar en visuell miniatyr som kan visas i webbläsare, rapporter eller mobilappar utan att kräva en fullständig CAD‑visare.

## Varför använda Aspose.CAD för Java?
Aspose.CAD stöder **30+ CAD‑ och BIM‑format**, inklusive IFC, DWG, DXF och DGN, och kan bearbeta filer upp till **2 GB** utan att ladda hela dokumentet i minnet. Biblioteket är rent Java, har **inga externa beroenden**, och körs på Windows, Linux och macOS, vilket gör det idealiskt för server‑sidig bildgenerering.  
Det erbjuder högpresterande rasterisering, omfattande formatstöd och enkel integration i Java‑applikationer.

## Förutsättningar

- **Aspose.CAD Library** – ladda ner den senaste JAR‑filen från [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 eller nyare installerat på din maskin.  
- **IFC source file** – placera filen i en mapp som du kan referera till från din kod.

## Importera namnrymder

`com.aspose.cad`‑paketet tillhandahåller alla klasser du behöver. `CadImage` är ingångspunkten för att ladda CAD‑filer, medan `PngOptions` konfigurerar rasteriseringsinställningarna.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Hur man skapar PNG‑miniatyr‑IFC i Java?

Ladda IFC‑filen, definiera rasteriseringsalternativ och spara resultatet som en PNG‑bild – det är hela konverteringsarbetsflödet. Följande avsnitt bryter ner varje steg, så att du kan kopiera‑klistra in kodsnuttarna i ditt projekt och köra dem omedelbart.

### Steg 1: ladda IFC‑filen
Först, peka på mappen där din IFC‑fil finns och ladda den med `CadImage.load`.  
`CadImage.load` läser en CAD‑fil och returnerar ett bildobjekt som kan rasteriseras.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Varför detta är viktigt:** Att ladda filen som en `CadImage` ger dig tillgång till vektor‑till‑raster‑konverteringsalternativ som styr upplösning, bakgrundsfärg och linjebredd.

### Steg 2: ange rasteriseringsalternativ
Definiera utdata-dimensionerna och eventuella andra vektorrelaterade inställningar via `VectorRasterizationOptions`.  
`VectorRasterizationOptions` låter dig ange utskriftsstorlek, bakgrundsfärg och andra rasteriseringsparametrar.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Justera `PageWidth` och `PageHeight` för att kontrollera den slutliga PNG‑upplösningen, vilket är viktigt när du **sparar PNG java**‑filer för högkvalitativa utskrifter eller webb‑miniatyrer.

### Steg 3: konfigurera PNG‑alternativ
Koppla rasteriseringsalternativen till PNG‑exportören genom att skapa en `PngOptions`‑instans.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Steg 4: spara bilden som PNG
Slutligen, skriv den rasteriserade bilden till disk med `save`‑metoden.  
`save` skriver den rasteriserade bilden till den angivna filsökvägen i det valda formatet.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Efter detta steg har du framgångsrikt **skapat en PNG‑miniatyr‑IFC** och kan använda den resulterande `example.png` var du än behöver en rasterbild.

## Vanliga användningsfall
- **Generera miniatyrbilder** för BIM‑modeller i webbportaler.  
- **Inbädda planritnings‑ögonblicksbilder** i PDF‑ eller Word‑rapporter.  
- **Automatiserad batch‑konvertering** av stora IFC‑bibliotek för arkiverings‑ eller migrationsprojekt.

## Felsökning & tips
- **Minnesproblem:** För mycket stora IFC‑filer, öka JVM‑heapen (`-Xmx2g` eller högre).  
- **Saknade texturer:** Säkerställ att IFC‑filens externa resurser är åtkomliga från `dataDir`.  
- **Pro‑tips:** Använd `vectorOptions.setBackgroundColor(Color.getWhite())` om du föredrar en vit bakgrund istället för den standardmässiga transparenta PNG‑en.

## Vanliga frågor

### Q1: Är Aspose.CAD kompatibel med alla versioner av IFC‑filer?
A1: Aspose.CAD stöder olika IFC‑versioner. Se [documentation](https://reference.aspose.com/cad/java/) för detaljerad kompatibilitetsinformation.

### Q2: Kan jag anpassa rasteriseringsalternativen ytterligare?
A2: Absolut! Utforska [documentation](https://reference.aspose.com/cad/java/) för avancerade inställningar såsom DPI‑kontroll, anti‑aliasing och linjetjocklek.

### Q3: Finns en provversion tillgänglig?
A3: Ja, du kan ladda ner den kostnadsfria provversionen från [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: Hur kan jag få en tillfällig licens för testning?
A4: Skaffa en tillfällig licens från [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: Var kan jag ställa frågor eller rapportera problem?
A5: Gå med i gemenskapen på [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för support från både Aspose‑ingenjörer och andra utvecklare.

## Vanligt förekommande frågor

**Q: Kan jag använda detta tillvägagångssätt för att konvertera andra CAD‑format till PNG?**  
A: Ja, Aspose.CAD stöder många format (DWG, DXF, DGN, etc.). Ändra helt enkelt filändelsen och ladda rätt bildklass.

**Q: Låter biblioteket mig ange en anpassad DPI?**  
A: DPI styrs indirekt via `PageWidth`/`PageHeight`. Justera dessa värden i förhållande till önskad fysisk storlek för att uppnå den erforderliga DPI.

**Q: Är PNG‑utdata förlustfri?**  
A: PNG är ett förlustfritt format, så den rasteriserade bilden behåller den fulla visuella integriteten från den ursprungliga vektordatan.

## Slutsats

Du har nu en komplett, produktionsklar metod för att **skapa PNG‑miniatyr‑IFC**‑filer med Aspose.CAD för Java. Integrera dessa steg i skrivbordsverktyg, server‑sidiga tjänster eller molnfunktioner för att automatisera BIM‑visualiseringspipelines och leverera snabba, högkvalitativa miniatyrer till slutanvändare.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## Relaterade handledningar

- [Hur man konverterar STL till PNG med Aspose.CAD för Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Konvertera DWG till PNG – Spara CAD som PNG med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Exportera DWG till PDF i Java – Ställ in PDF‑sidstorlek med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}