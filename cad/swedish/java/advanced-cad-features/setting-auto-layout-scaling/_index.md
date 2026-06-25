---
date: 2026-02-15
description: Lär dig hur du ställer in anpassad sidstorlek och skapar PDF från CAD
  med Aspose.CAD för Java. Denna steg‑för‑steg‑guide täcker export av CAD till PDF
  med automatisk layoutskalning.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Ställ in anpassad sidstorlek – PDF från CAD med automatisk layoutskalning
url: /sv/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ange anpassad sidstorlek – Skapa PDF från CAD med automatisk layoutskalning

## Introduktion

Om du behöver **set custom page size** medan du **create PDF from CAD**‑filer snabbt och med perfekt skalning, har Aspose.CAD för Java dig täckt. Auto Layout Scaling justerar automatiskt layoutens dimensioner så att den resulterande PDF‑filen ser exakt ut som avsett, oavsett den ursprungliga CAD‑sidstorleken. I den här handledningen går vi igenom hela processen – från att läsa in en DXF‑fil till att exportera en PDF – samtidigt som vi framhäver **export CAD to PDF**‑funktionerna i biblioteket och visar hur du också kan **convert DWG to PDF** eller **increase PDF resolution** vid behov.

## Snabba svar
- **Vad gör Auto Layout Scaling?** Den automatiskt ändrar storlek på CAD‑layouter så att de passar målsidans dimensioner vid rasterisering.
- **Vilka format kan jag konvertera?** Alla format som stöds av Aspose.CAD (t.ex. DXF, DWG, DWF) kan konverteras till PDF.
- **Behöver jag en licens för produktion?** Ja, en kommersiell licens krävs för icke‑utvärderingsbruk.
- **Hur lång tid tar konverteringen?** Vanligtvis under en sekund för standardfiler på modern hårdvara.
- **Kan jag ändra sidstorleken?** Ja, du kan ange anpassade sidmått via `CadRasterizationOptions`.

## Vad betyder “skapa PDF från CAD”?

Att skapa en PDF från CAD innebär att ta en vektorbaserad ingenjörsritning (DXF, DWG osv.) och rasterisera den till ett PDF‑dokument. PDF‑filen behåller den visuella troheten i den ursprungliga ritningen samtidigt som den kan visas på i stort sett alla plattformar.

## Varför använda Auto Layout Scaling?

- **Konsistent resultat:** Garanti för att alla layouter fyller PDF‑sidan utan manuella storleksberäkningar.
- **Tidsbesparande:** Eliminerar behovet av att manuellt justera skalningsfaktorer för varje ritning.
- **Hög kvalitet:** Bevarar linjebredd och geometrisk noggrannhet under konverteringen.
- **Flexibilitet:** Fungerar för **convert dxf to pdf**, **convert dwg to pdf**, och även när du behöver **increase PDF resolution** för utskriftsklara filer.

## Förutsättningar

1. **Aspose.CAD for Java Library** – ladda ner den senaste versionen från [download page](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – skapa en mapp på din maskin för att lagra CAD‑filer; ersätt `"Your Document Directory"` i koden med den sökvägen.  
3. **Sample CAD File** – för den här guiden använder vi `conic_pyramid.dxf`, som ingår i Aspose‑exempeldatasettet.

## Importera namnrymder

Först importerar du de nödvändiga klasserna. Detta ger oss åtkomst till bildladdning, rasterisering och PDF‑exportfunktioner.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hur man anger anpassad sidstorlek för PDF från CAD

Innan vi dyker ner i steg‑för‑steg‑koden, låt oss förstå varför det är viktigt att ange en anpassad sidstorlek. När du **set custom page size** styr du de fysiska dimensionerna på den resulterande PDF‑filen (t.ex. A4, Letter eller en skräddarsydd storlek). Detta är avgörande för ingenjörsarbetsflöden där ritningar måste matcha bladstandarder eller när du behöver bädda in PDF‑filen i större dokument.

### Steg 1: Läs in CAD‑filen

Att läsa in källfilen är det första steget i **how to export CAD** till ett PDF‑dokument.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Steg 2: Skapa rasteriseringsalternativ

Definiera målsidans dimensioner. Du kan också använda detta block för att **set CAD page size** manuellt om du föredrar en anpassad layout.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Steg 3: Aktivera Auto Layout Scaling

Aktivera den automatiska skalningsfunktionen. Detta är kärnan i **how to set scaling** för en CAD‑till‑PDF‑konvertering.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Steg 4: Skapa PDF‑alternativ

Koppla rasteriseringsinställningarna till PDF‑exportalternativen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 5: Exportera till PDF

Slutligen sparar du den renderade bilden som en PDF‑fil. Detta steg slutför **convert dxf to pdf**‑arbetsflödet.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Upprepa stegen ovan för alla ytterligare CAD‑filer du behöver bearbeta, oavsett om de är **DWG**, **DWF** eller andra stödda format.

## Vanliga användningsfall

| Scenario | Varför ange en anpassad sidstorlek? |
|----------|--------------------------------------|
| **Inlämning av byggritning** | Justera PDF‑filen till standard A1/A2‑bladstorlekar som krävs av myndigheter. |
| **Inbäddning i tekniska manualer** | Säkerställer att ritningen passar den fördefinierade layouten i manualen utan extra skalning. |
| **Utskrift med hög upplösning** | Gör det möjligt att öka DPI (t.ex. `rasterizationOptions.setResolution(300)`) samtidigt som sidmåtten förblir konsekventa. |

## Vanliga problem & felsökning

| Symptom | Trolig orsak | Åtgärd |
|---------|--------------|--------|
| Tom PDF‑utdata | Rasteriseringsalternativ är inte inställda eller felaktig filsökväg | Verifiera `srcFile`‑sökvägen och säkerställ att `setPageWidth/Height` är icke‑noll |
| Förvrängd skalning | `setAutomaticLayoutsScaling` lämnad som `false` | Aktivera automatisk skalning eller beräkna skalningsfaktorn manuellt |
| Saknade lager | Käll‑DXF innehåller ej stödda enheter | Kontrollera Aspose.CAD‑versionsanteckningarna för vilka enhetstyper som stöds |

## Vanliga frågor

**Q: Är Aspose.CAD för Java kompatibel med alla CAD‑filformat?**  
A: Aspose.CAD för Java stöder olika CAD‑format, inklusive DWG, DXF och DWF.

**Q: Kan jag anpassa skalningsalternativen ytterligare?**  
A: Ja, klassen `CadRasterizationOptions` erbjuder egenskaper för finjustering av skalning, DPI och andra rasteriseringsinställningar.

**Q: Var kan jag hitta ytterligare dokumentation för Aspose.CAD för Java?**  
A: Se [documentation](https://reference.aspose.com/cad/java/) för djupgående information och exempel.

**Q: Finns det en gratis provversion av Aspose.CAD för Java?**  
A: Ja, du kan prova en [free trial](https://releases.aspose.com/) för att uppleva funktionerna i Aspose.CAD för Java.

**Q: Hur kan jag få hjälp eller delta i diskussioner om Aspose.CAD för Java?**  
A: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för att komma i kontakt med communityn och söka support.

### Ytterligare vanliga frågor

**Q: Hur konverterar jag en DWG‑fil till PDF istället för DXF?**  
A: Samma kod fungerar; ändra bara filändelsen i `srcFile` till `.dwg`.

**Q: Kan jag ange en anpassad DPI för PDF‑filer med högre upplösning?**  
A: Ja, använd `rasterizationOptions.setResolution(300);` (eller någon annan DPI du behöver).

**Q: Är det möjligt att bädda in typsnitt i den genererade PDF‑filen?**  
A: Aspose.CAD rasteriserar ritningen, så typsnitt renderas som vektorer; separat inbäddning av typsnitt krävs inte.

## Slutsats

Genom att följa den här guiden vet du nu hur du **set custom page size** och **create PDF from CAD**‑filer med Aspose.CAD för Java och Auto Layout Scaling. Processen förenklar **export CAD to PDF**‑arbetsflödet, säkerställer konsekvent skalning och sparar värdefull utvecklingstid. Känn dig fri att experimentera med olika sidstorlekar, upplösningar och CAD‑format för att passa ditt projekts behov, oavsett om du **converting DWG to PDF**, **increasing PDF resolution**, eller bygger en **java CAD to PDF**‑batch‑processor.

---

**Senast uppdaterad:** 2026-02-15  
**Testat med:** Aspose.CAD for Java 24.12 (latest)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}