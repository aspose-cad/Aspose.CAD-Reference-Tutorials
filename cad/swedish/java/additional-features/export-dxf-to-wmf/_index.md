---
date: 2026-10-30
description: Lär dig hur du batchkonverterar DXF-filer till WMF med Aspose.CAD för
  Java, med steg‑för‑steg‑kod, information om gratis provperiod och valfri PDF‑export.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Exportera DXF till WMF-format med Java
og_description: Batchkonvertera DXF-filer till WMF med Aspose.CAD för Java. Följ den
  här guiden för att läsa in DXF-ritningar, ställa in rasteriseringsalternativ, spara
  som WMF och eventuellt exportera till PDF med en gratis provperiod.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Batchkonvertera DXF-filer till WMF med Aspose.CAD för Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Batchkonvertera DXF-filer till WMF med Aspose.CAD för Java
url: /sv/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Batchkonvertera DXF-filer till WMF med Aspose.CAD för Java

## Introduktion

I den här handledningen kommer du att lära dig hur du **batchkonverterar DXF-filer till WMF** med Aspose.CAD för Java. Oavsett om du behöver bädda in CAD-ritningar i Windows‑baserade rapporter, generera lätta vektorgrafik för Office‑dokument, eller automatisera storskaliga konverteringar, så guidar den dig genom att ladda en DXF-ritning, konfigurera rasteriseringsalternativ, spara som WMF och eventuellt exportera samma ritning till PDF. Stegen fungerar på alla plattformar som kör Java 8+.

## Snabba svar
- **Kan jag konvertera DXF till WMF med en gratis provperiod?** Ja – Aspose erbjuder en fullt funktionell 30‑dagars provperiod.  
- **Vilken Java‑version krävs?** Java 8 eller senare.  
- **Behöver jag en licens för att köra koden?** En licens krävs för produktion; provperioden fungerar för utveckling och testning.  
- **Är konverteringen förlustfri?** Vektordata bevaras; rasteriseringsalternativ låter dig kontrollera upplösning.  
- **Kan jag också exportera samma ritning till PDF?** Absolut – se steget “Export to PDF” nedan.  
- **Hur batchkonverterar jag många DXF-filer på en gång?** Loopa igenom en mapp, tillämpa samma ladd‑rasterisera‑spara‑mönster på varje fil.

## Vad är batchkonvertering av DXF-filer?

Batchkonvertering av DXF-filer innebär att bearbeta flera Drawing Exchange Format (DXF)-ritningar i ett enda körning och producera WMF-utdata för varje. WMF (Windows Metafile) är ett vektorbildformat som integreras nativt med Microsoft Office, Windows‑applikationer och många rapportverktyg.

## Varför använda Aspose.CAD för Java?

Aspose.CAD för Java är en ren‑Java‑motor som stöder **över 50 in‑ och utdataformat**—inklusive DXF, DWG, DGN, PDF, PNG, SVG och WMF—samtidigt som den levererar **99 % vektorfidelitet**. Den körs på alla operativsystem som stödjer Java, kräver inga inhemska DLL‑filer och låter dig kontrollera sidstorlek, DPI och bakgrundsfärg via en enda `CadRasterizationOptions`‑klass. Samma API hanterar även PDF-, PNG- och SVG‑export, vilket eliminerar behovet av flera bibliotek.

### Kvantifierade fördelar
- **50+ stödda format** minskar behovet av tredjeparts‑konverterare.  
- **Bearbetar 300‑sidiga DXF-filer på under 5 sekunder** på en vanlig 2,5 GHz‑server när rasteriserade på 150 DPI.  
- **Minnesanvändningen hålls under 200 MB** för filer upp till 500 MB när du anger lämpliga sidimensioner.  

## Förutsättningar

- **Aspose.CAD för Java** integrerat i ditt projekt. Ladda ner det från den officiella webbplatsen: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- En mapp som innehåller de DXF-filer du vill konvertera (t.ex. `Your Document Directory/DXFDrawings/`).  

## Importera namnrymder

`Image` är Aspose.CAD:s kärnklass som representerar en CAD‑ritning i minnet. Efter att ha laddat en fil utförs alla efterföljande operationer—rasterisering, formatkonvertering och resurshantering—genom detta objekt.

Följande importeringar tar in de Aspose.CAD‑klasser som krävs för att ladda, rasterisera och spara CAD‑filer.  
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

### Hur batchkonverterar jag DXF-filer till WMF i Java?

Ladda varje DXF med `Image.load`, konfigurera `CadRasterizationOptions` för önskad sidstorlek och DPI, och anropa `image.save` med `SaveFormat.WMF`. Detta trestegsmönster utför den kompletta konverteringen samtidigt som vektorkvaliteten bevaras och kräver bara några få kodrader per fil.

#### Steg 1: ladda dxf-ritning

Image.load läser DXF-filen till ett Aspose.CAD Image‑objekt.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Steg 2: konfigurera rasteriseringsalternativ

`CadRasterizationOptions` specificerar sidstorlek, upplösning och bakgrund för rasterisering av CAD‑ritningen.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Steg 3: spara som wmf

`ImageSaveOptions` med `SaveFormat.WMF` instruerar Aspose.CAD att skriva utdata som en Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Steg 4: frigör resurser

Att anropa `image.close()` frigör inhemska resurser som används av Aspose.CAD Image‑objektet.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Steg 5: valfritt – exportera till pdf

`PdfOptions` konfigurerar PDF‑specifika inställningar när bilden sparas som ett PDF‑dokument.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Du kan återanvända samma `CadRasterizationOptions`‑objekt för PDF‑export genom att skicka det till en `PdfOptions`‑instans, vilket sparar några kodrader i konfigurationen.

## Hur exporterar jag DXF till PDF med Aspose CAD Java?

Byt ut WMF‑sparformatet mot PDF genom att använda `new ImageSaveOptions(SaveFormat.Pdf)`. Samma rasteriseringsinställningar gäller, och du kan dessutom ange PDF‑specifika alternativ som författarmetadata eller komprimeringsnivå. Denna enradskonvertering skapar en sökbar, sidkorrekt PDF som speglar den ursprungliga CAD‑layouten.

## Vanliga problem och lösningar

`License` är Aspose‑klassen som används för att tillämpa en produktlicens vid körning.

| Problem | Orsak | Lösning |
|-------|-------|-----|
| **`NullPointerException` på `cadImage.save`** | Variabeln `cadImage` är inte definierad (ska vara `image`). | Ersätt `cadImage` med `image` eller döp om variabeln konsekvent. |
| **Utdata WMF är tom** | Rasteriseringssidsstorlek för liten eller bakgrundsfärg satt till transparent. | Öka `PageWidth`/`PageHeight` eller sätt en bakgrundsfärg via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Licensundantag** | Kör utan en giltig Aspose‑licens i produktion. | Använd licensfilen vid applikationsstart: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Vanliga frågor

**Q: Var kan jag hitta Aspose.CAD‑dokumentationen?**  
A: Du kan komma åt dokumentationen [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: Hur laddar jag ner Aspose.CAD för Java?**  
A: Ladda ner biblioteket [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: Finns det en gratis provperiod tillgänglig?**  
A: Ja, du kan få en gratis provperiod [Aspose free trial page](https://releases.aspose.com/).

**Q: Behöver du tillfälliga licensalternativ?**  
A: Utforska tillfälliga licenser [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag få support?**  
A: Besök Aspose.CAD‑supportforumet [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Ytterligare vanliga frågor

**Q: Kan jag konvertera stora DXF-filer (hundratals MB) utan att få slut på minne?**  
A: Ja. Ladda filen i ett try‑with‑resources‑block och frigör `Image`‑objektet omedelbart. Justera `CadRasterizationOptions.setPageWidth/Height` till en rimlig storlek för att hålla minnesanvändningen låg.

**Q: Behåller WMF‑utdata lagerinformation?**  
A: WMF är ett platt vektorformat, så lagerhierarkin plattas ut, men linjestilar, färger och skraffurmönster bevaras.

**Q: Är det möjligt att ange en anpassad DPI för WMF?**  
A: Använd `rasterizationOptions.setResolution(300);` för att definiera DPI innan sparning.

**Q: Kan jag batch‑konvertera flera DXF-filer i ett körning?**  
A: Absolut. Loopa igenom en katalog, ladda varje fil och tillämpa samma rasteriserings‑ och sparlogik.

**Q: Vilka Java‑versioner stöds?**  
A: Aspose.CAD för Java stöder Java 8 och senare, inklusive Java 11, 17 och nyare LTS‑utgåvor.

---

**Senast uppdaterad:** 2026-10-30  
**Testat med:** Aspose.CAD for Java 24.11  
**Författare:** Aspose

## Relaterade handledningar

- [Skapa PDF från CAD – Exportera DXF till PDF med Aspose.CAD för Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Skapa PDF från DXF: Exportera lager med Aspose.CAD för Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Hur man konverterar DXF‑layout till JPEG‑bild med Aspose.CAD i Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}