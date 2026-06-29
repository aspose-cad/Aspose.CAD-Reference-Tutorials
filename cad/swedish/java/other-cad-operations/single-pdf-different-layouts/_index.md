---
date: 2026-06-29
description: Lär dig hur du skapar PDF från DWG och anpassar PDF-layout med Aspose.CAD
  för Java. Enkelt att integrera för Java‑utvecklare.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: En PDF med olika layouter
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Skapa PDF från DWG med Aspose.CAD för Java
url: /sv/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PDF från DWG med Aspose.CAD för Java

## Introduktion

## Snabba svar
- **Vad täcker handledningen?** Konvertera en DWG-ritning till en enda PDF med flera sidstorlekar.  
- **Vilket bibliotek krävs?** Aspose.CAD för Java (senaste versionen).  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Kan jag exportera andra format?** Ja – API:et stöder även export till PNG, JPEG och SVG.  
- **Är Java 8 tillräckligt?** Biblioteket fungerar med Java 8 och nyare runtime-miljöer.

## Vad betyder “create pdf from dwg”?

**Create PDF from DWG** betyder att konvertera en native AutoCAD DWG-fil till ett PDF-dokument samtidigt som vektorfidelitet, lager och linjebredder bevaras, och möjliggör layoutanpassning. Aspose.CAD utför denna konvertering helt i minnet, så ingen extern CAD-programvara behövs, och den resulterande PDF-filen kan redigeras eller skrivas ut direkt.

## Varför anpassa PDF‑layout från DWG?

Aspose.CAD stöder **30+ CAD-format** och kan generera PDF-filer upp till **500 MB** utan att ladda hela filen i minnet. Genom att definiera individuella sidstorlekar för varje layout kan du skapa utskrivbara blad som matchar ISO-, ANSI- eller anpassade dimensioner – en kvantifierad fördel som sparar tid och eliminerar manuell efterbehandling.

## Förutsättningar

Innan vi påbörjar denna resa, se till att du har följande förutsättningar på plats:
- Java-miljö: Se till att du har Java installerat på din maskin.  
- Aspose.CAD-bibliotek: Ladda ner och installera Aspose.CAD-biblioteket för Java från [download link](https://releases.aspose.com/cad/java/).  
- Dokumentkatalog: Skapa en katalog för dina DWG-ritningar.

## Importera paket

Klassen `CadImage` är Aspose.CAD:s kärnobjekt som representerar en CAD-ritning i minnet. Importera de nödvändiga namnutrymmena innan du börjar:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Steg 1: Ladda CAD‑ritning

`CadImage` laddar DWG-filen och ger åtkomst till dess vektordata. Börja med att ladda din CAD-ritning i ett `CadImage`‑objekt:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Steg 2: Konfigurera rasteriseringsalternativ

`RasterizationOptions` definierar hur CAD-vektorer rasteriseras innan de placeras i PDF:en. Ställ in rasteriseringsalternativen för CAD‑bilden:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Steg 3: Anpassa layoutsidestorlekar

`PdfOptions` låter dig tilldela olika sidmått till varje layout i DWG-filen. Definiera anpassade storlekar för flera layouter i CAD‑ritningen:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Steg 4: Ställ in PDF‑alternativ

`PdfOptions` är behållaren som kombinerar rasteriseringsinställningar och layoutdefinitioner. Konfigurera PDF‑alternativen och inkludera rasteriseringsinställningarna:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Steg 5: Spara som PDF

`PdfSaveOptions` slutför konverteringen och skriver utdatafilen. Spara den bearbetade CAD‑bilden som en PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Grattis! Du har framgångsrikt **create pdf from dwg** med olika sidstorlekar med hjälp av Aspose.CAD för Java.

## Vanliga problem och lösningar

- **Tomma sidor i den genererade PDF‑filen** – Se till att `PageSize`‑värdena matchar de faktiska layoutdimensionerna i DWG-filen.  
- **Memory‑out‑fel på stora ritningar** – Använd `CadImage.load(..., LoadOptions)` med `LoadOptions.setLoadMode(LoadMode.Memory)` för att strömma filen istället för att ladda den helt.  
- **Felaktig skalning** – Justera `RasterizationOptions.setPageWidth` och `setPageHeight` så att de matchar önskad DPI (dots per inch).

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java med andra Java‑bibliotek?**  
A: Ja, Aspose.CAD för Java integreras sömlöst med bibliotek som Apache POI, Jackson eller Spring Boot.

**Q: Finns det en provversion tillgänglig?**  
A: Absolut! Du kan komma åt en gratis provversion [här](https://releases.aspose.com/).

**Q: Var kan jag hitta ytterligare support?**  
A: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

**Q: Hur får jag en tillfällig licens?**  
A: Du kan få en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag köpa fullversionen?**  
A: Köp fullversionen av Aspose.CAD för Java [här](https://purchase.aspose.com/buy).

---

**Senast uppdaterad:** 2026-06-29  
**Testad med:** Aspose.CAD för Java 24.10  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera DWG till PDF eller raster med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Exportera CAD‑layouter till PDF med Aspose.CAD för Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Exportera specifik DWG‑layout till PDF med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}