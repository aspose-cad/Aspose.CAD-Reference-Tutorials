---
date: 2026-06-09
description: Lär dig hur du konverterar DXF till WMF med Aspose.CAD för Java, inklusive
  en gratis provperiod, stöd för Java 8+ och valfri PDF-export. Steg‑för‑steg‑guide
  med kodexempel.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Exportera DXF till WMF-format med Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konvertera DXF till WMF med Aspose.CAD i Java
url: /sv/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DXF till WMF med Aspose.CAD i Java

## Introduktion

I den här handledningen kommer du att upptäcka hur du **konverterar DXF till WMF** med Aspose.CAD för Java. Oavsett om du behöver bädda in CAD‑ritningar i en Windows‑baserad rapport, skapa lätta vektorgrafik för Office‑dokument, eller automatisera batch‑konverteringar, är konvertering av DXF till WMF ett vanligt krav i ingenjörs‑ och rapporteringsprocesser. Vi går igenom hur du laddar en DXF‑ritning, konfigurerar rasteriseringsalternativ, sparar resultatet som WMF och eventuellt exporterar samma ritning till PDF.

## Snabba svar
- **Kan jag konvertera DXF till WMF med en gratis provperiod?** Ja – Aspose erbjuder en fullt funktionell 30‑dagars provperiod.  
- **Vilken Java‑version krävs?** Java 8 eller senare.  
- **Behöver jag en licens för att köra koden?** En licens krävs för produktion; provperioden fungerar för utveckling och testning.  
- **Är konverteringen förlustfri?** Vektordata bevaras; rasteriseringsalternativen låter dig styra upplösning.  
- **Kan jag också exportera samma ritning till PDF?** Absolut – se steget “Export till PDF” nedan.

## Vad betyder “konvertera DXF till WMF”?

Att konvertera DXF till WMF innebär att ta en Drawing Exchange Format (DXF)‑fil – ett allmänt använt CAD‑format – och omvandla den till en Windows Metafile (WMF). WMF är ett vektorbildformat som integreras smidigt med Microsoft Office, Windows‑applikationer och många rapporteringsverktyg.

## Varför använda Aspose.CAD för Java?

Aspose.CAD för Java erbjuder en ren‑Java‑motor utan inhemska DLL‑beroenden som konverterar CAD‑filer med **över 99 % vektorfidelitet**, och bevarar lager, färger, linjestilar och skraffermönster. Den stöder **50+ in‑ och utdataformat** – inklusive DXF, DWG, DGN, PDF, PNG, SVG och WMF – samtidigt som du kan finjustera sidstorlek, DPI och bakgrundsfärg via inbyggda rasteriseringsalternativ. Samma API hanterar även PDF-, PNG‑ och SVG‑export, vilket eliminerar behovet av flera bibliotek.

### Viktiga fördelar
- **Inga externa beroenden** – ren Java, fungerar på alla OS som kör Java.  
- **Hög‑fidelitets rendering** – behåller linjebredd, färg och skrafferdetaljer.  
- **Inbyggd rasterisering** – kontroll över siddimensioner, upplösning och bakgrund.  
- **All‑i‑ett‑konvertering** – samma klasser exporterar till WMF, PDF, PNG, SVG osv.

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.CAD för Java** integrerat i ditt projekt. Ladda ner det från den officiella sidan: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Dokumentkatalog** där dina DXF‑filer lagras (t.ex. `Your Document Directory/DXFDrawings/`).  

## Importera namnrymder

Följande import‑satser tar in de Aspose.CAD‑klasser som behövs för att ladda, rasterisera och spara CAD‑filer.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Steg‑för‑steg‑guide

### Hur konverterar jag DXF till WMF i Java?

Ladda din DXF‑fil med `Image.load("yourFile.dxf")`, konfigurera `CadRasterizationOptions` för önskad sidstorlek och DPI, och anropa sedan `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Detta tre‑stegs‑mönster utför hela konverteringen samtidigt som vektor­kvaliteten bevaras och kräver bara några få kodrader.

#### Steg 1: Ladda DXF‑ritning

Image.load läser DXF‑filen till ett Aspose.CAD Image‑objekt.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Steg 2: Konfigurera rasteriseringsalternativ

CadRasterizationOptions specificerar sidstorlek, upplösning och bakgrund för rasteriseringen av CAD‑ritningen.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Steg 3: Spara som WMF

ImageSaveOptions med SaveFormat.WMF instruerar Aspose.CAD att skriva utdata som en Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Steg 4: Frigör resurser

Genom att anropa image.close() frigörs de inhemska resurser som används av Aspose.CAD Image‑objektet.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Steg 5: Valfritt – Export till PDF

PdfOptions konfigurerar PDF‑specifika inställningar när bilden sparas som ett PDF‑dokument.  
```java
finally
{
  cadImage.dispose();
}
```

> **Proffstips:** Du kan återanvända samma `CadRasterizationOptions`‑objekt för PDF‑export genom att skicka det till en `PdfOptions`‑instans, vilket sparar några kodrader.

## Hur exporterar jag DXF till PDF med Aspose CAD Java?

Export till PDF följer samma laddnings‑ och rasteriseringssteg; ersätt helt enkelt WMF‑sparaformatet med PDF. Använd `new ImageSaveOptions(SaveFormat.Pdf)` och ange eventuellt PDF‑specifika alternativ såsom komprimeringsnivå eller författarmetadata. Denna enradskonvertering skapar en sökbar, sidnoggrann PDF som speglar den ursprungliga CAD‑layouten.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|---------|
| **`NullPointerException` on `cadImage.save`** | Variabeln `cadImage` är inte definierad (ska vara `image`). | Byt ut `cadImage` mot `image` eller döp om variabeln konsekvent. |
| **Utdata WMF är tom** | Rasteriseringssidans storlek är för liten eller bakgrundsfärgen är satt till transparent. | Öka `PageWidth`/`PageHeight` eller sätt en bakgrundsfärg via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Kör utan en giltig Aspose-licens i produktion. | Applicera licensfilen vid applikationens start: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Slutsats

Du har nu ett komplett, produktionsklart arbetsflöde för att **konvertera DXF till WMF** med Aspose.CAD för Java, med ett valfritt steg för att **exportera samma ritning till PDF**. Detta tillvägagångssätt ger dig högkvalitativ vektorutdata som integreras sömlöst med Windows‑baserade rapporterings‑ och dokumentationsverktyg, samtidigt som din kodbas förblir enkel och utan beroenden.

## Vanliga frågor

### Q1: Var kan jag hitta Aspose.CAD-dokumentationen?

A1: Du kan komma åt dokumentationen [här](https://reference.aspose.com/cad/java/).

### Q2: Hur laddar jag ner Aspose.CAD för Java?

A2: Ladda ner biblioteket [här](https://releases.aspose.com/cad/java/).

### Q3: Finns det en gratis provperiod tillgänglig?

A3: Ja, du kan få en gratis provperiod [här](https://releases.aspose.com/).

### Q4: Behöver du tillfälliga licensalternativ?

A4: Utforska tillfälliga licenser [här](https://purchase.aspose.com/temporary-license/).

### Q5: Var kan jag få support?

A5: Besök Aspose.CAD supportforum [här](https://forum.aspose.com/c/cad/19).

## Vanligt förekommande frågor

**Q: Kan jag konvertera stora DXF‑filer (hundratals MB) utan att få minnesbrist?**  
A: Ja. Ladda filen i ett try‑with‑resources‑block och frigör `Image`‑objektet omedelbart. Justera `CadRasterizationOptions.setPageWidth/Height` till en rimlig storlek för att hålla minnesanvändningen låg.

**Q: Behåller WMF‑utdata lagerinformation?**  
A: WMF är ett platt vektorformat, så lagerhierarkin plattas ut, men linjestilar, färger och skraffermönster bevaras.

**Q: Är det möjligt att ange en anpassad DPI för WMF?**  
A: Använd `rasterizationOptions.setResolution(300);` för att definiera DPI innan du sparar.

**Q: Kan jag batch‑konvertera flera DXF‑filer i ett körning?**  
A: Absolut. Loopa igenom en katalog, ladda varje fil och tillämpa samma rasteriserings‑ och sparlogik.

**Q: Vilka Java‑versioner stöds?**  
A: Aspose.CAD för Java stöder Java 8 och senare, inklusive Java 11, 17 och nyare LTS‑utgåvor.

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Relaterade handledningar

- [Skapa PDF från CAD – Exportera DXF till PDF med Aspose.CAD för Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Skapa PDF från DXF: Exportera lager med Aspose.CAD för Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Hur man konverterar DXF‑layout till JPEG‑bild med Aspose.CAD i Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}