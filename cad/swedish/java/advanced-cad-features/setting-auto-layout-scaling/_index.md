---
date: 2025-12-10
description: Lär dig hur du skapar PDF från CAD med Aspose.CAD för Java och Auto Layout
  Scaling. Denna steg‑för‑steg‑guide visar dig hur du exporterar CAD till PDF på ett
  effektivt och pålitligt sätt.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Skapa PDF från CAD – Automatisk layoutskalning med Aspose.CAD Java
url: /sv/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PDF från CAD – Automatisk layoutskalning med Aspose.CAD Java

## Introduction

Om du behöver **skapa PDF från CAD**‑filer snabbt och med perfekt skalning, så har Aspose.CAD för Java dig täckt. Auto Layout Scaling justerar automatiskt layoutens dimensioner så att den resulterande PDF‑filen ser exakt ut som avsett, oavsett den ursprungliga CAD‑sidans storlek. I den här handledningen går vi igenom hela processen—från att ladda en DXF‑fil till att exportera en PDF—och lyfter fram **export CAD till PDF**‑funktionerna i biblioteket.

## Quick Answers
- **Vad gör Auto Layout Scaling?** Den ändrar automatiskt storleken på CAD‑layouter så att de passar mål sidans dimensioner vid rasterisering.
- **Vilka format kan jag konvertera?** Alla format som stöds av Aspose.CAD (t.ex. DXF, DWG, DWF) kan konverteras till PDF.
- **Behöver jag en licens för produktion?** Ja, en kommersiell licens krävs för icke‑utvärderingsbruk.
- **Hur lång tid tar konverteringen?** Vanligtvis under en sekund för standardfiler på modern hårdvara.
- **Kan jag ändra sidstorleken?** Ja, du kan ange anpassade sidmått via `CadRasterizationOptions`.

## What is “create PDF from CAD”?

Att skapa en PDF från CAD innebär att ta en vektorbaserad ingenjörsritning (DXF, DWG, etc.) och rasterisera den till ett PDF‑dokument. PDF‑filen behåller den visuella kvaliteten från den ursprungliga ritningen samtidigt som den kan visas på vilken plattform som helst.

## Why use Auto Layout Scaling?
- **Konsistent resultat:** Garanti för att alla layouter fyller PDF‑sidan utan manuella storleksberäkningar.
- **Tidsbesparande:** Eliminerar behovet av att manuellt justera skalningsfaktorer för varje ritning.
- **Hög kvalitet:** Behåller linjebredd och geometrisk noggrannhet under konverteringen.

## Prerequisites

1. **Aspose.CAD for Java Library** – ladda ner den senaste versionen från [download page](https://releases.aspose.com/cad/java/).  
2. **Resurskatalog** – skapa en mapp på din maskin för att lagra CAD‑filer; ersätt `"Your Document Directory"` i koden med den sökvägen.  
3. **Exempel‑CAD‑fil** – för den här guiden använder vi `conic_pyramid.dxf`, som ingår i Aspose‑exempeldatasettet.

## Import Namespaces

First, import the required classes. This gives us access to image loading, rasterization, and PDF export features.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step 1: Load the CAD File

Loading the source file is the first step in **how to export CAD** to a PDF document.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Step 2: Create Rasterization Options

Define the target page dimensions. You can also use this block to **set CAD page size** manually if you prefer a custom layout.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Step 3: Set Auto Layout Scaling

Enable the automatic scaling feature. This is the core of **how to set scaling** for a CAD‑to‑PDF conversion.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Step 4: Create PDF Options

Link the rasterization settings to the PDF export options.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Export to PDF

Finally, save the rendered image as a PDF file. This step completes the **convert DXF to PDF** workflow.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Repeat the steps above for any additional CAD files you need to process.

## Common Issues & Troubleshooting

| Symtom | Trolig orsak | Åtgärd |
|--------|--------------|--------|
| Tom PDF-utmatning | Rasteriseringsalternativ är inte inställda eller felaktig filsökväg | Verifiera `srcFile`‑sökvägen och säkerställ att `setPageWidth/Height` är icke‑noll |
| Förvrängd skalning | `setAutomaticLayoutsScaling` left as `false` | Aktivera automatisk skalning eller beräkna skalningsfaktorn manuellt |
| Saknade lager | Käll‑DXF innehåller ej stödda enheter | Kontrollera Aspose.CAD:s release‑anteckningar för vilka enhetstyper som stöds |

## FAQ's

### Q1: Är Aspose.CAD för Java kompatibel med alla CAD‑filformat?

A1: Aspose.CAD för Java stöder olika CAD‑format, inklusive DWG, DXF och DWF.

### Q2: Kan jag anpassa skalningsalternativen ytterligare?

A2: Ja, `CadRasterizationOptions`‑klassen erbjuder olika egenskaper för finjustering av skalning och andra inställningar.

### Q3: Var kan jag hitta ytterligare dokumentation för Aspose.CAD för Java?

A3: Se [documentation](https://reference.aspose.com/cad/java/) för djupgående information och exempel.

### Q4: Finns det en gratis provversion av Aspose.CAD för Java?

A4: Ja, du kan utforska en [free trial](https://releases.aspose.com/) för att uppleva funktionerna i Aspose.CAD för Java.

### Q5: Hur kan jag få hjälp eller delta i diskussioner om Aspose.CAD för Java?

A5: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för att ansluta till communityn och söka support.

**Additional Common Questions**

**Q: Hur konverterar jag en DWG‑fil till PDF istället för DXF?**  
A: Samma kod fungerar; byt bara filändelsen i `srcFile` till `.dwg`.

**Q: Kan jag ange en anpassad DPI för högupplösta PDF‑filer?**  
A: Ja, använd `rasterizationOptions.setResolution(300);` (eller någon annan DPI du behöver).

**Q: Är det möjligt att bädda in teckensnitt i den genererade PDF‑filen?**  
A: Aspose.CAD rasteriserar ritningen, så teckensnitt renderas som vektorer; separat inbäddning av teckensnitt krävs inte.

## Conclusion

Genom att följa den här guiden vet du nu hur du **skapar PDF från CAD**‑filer med Aspose.CAD för Java och Automatisk layoutskalning. Processen förenklar **export CAD till PDF**‑arbetsflödet, säkerställer konsekvent skalning och sparar värdefull utvecklingstid. Känn dig fri att experimentera med olika sidstorlekar, upplösningar och CAD‑format för att passa ditt projekts behov.

---

**Last Updated:** -12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}