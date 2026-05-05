---
date: 2026-01-22
description: Lär dig hur du skapar PDF från CAD-ritningar, konverterar DWG till PDF
  och anpassar PDF-sidstorlek med Aspose.CAD för Java.
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Hur man skapar PDF från CAD-ritningar med Aspose.CAD för Java
url: /sv/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Så skapar du PDF från CAD-ritningar med Aspose.CAD för Java

## Introduktion

I den här handledningen kommer du att upptäcka **hur man skapar PDF från CAD**-ritningar med hjälp av Aspose.CAD-biblioteket för Java. Oavsett om du behöver **konvertera DWG till PDF**, exportera en komplex CAD-fil eller använda en **anpassad PDF-sidstorlek**, så kommer stegen nedan att guida dig genom en ren, programmerbar lösning. Låt oss gå igenom processen tillsammans, så att du kan generera en enda PDF som innehåller flera layout‑sidor — allt med bara några rader Java‑kod.

## Snabba svar
- **Vad gör Aspose.CAD?** Det låter Java‑utvecklare ladda, manipulera och exportera CAD‑ritningar till format som PDF.
- **Kan jag exportera flera layouter till en PDF?** Ja, genom att anpassa layout‑sidstorlekar innan du sparar.
- **Vilka CAD‑format stöds?** DWG, DXF, DWF, DGN och många fler.
- **Behöver jag en licens för produktion?** En tillfällig licens fungerar för testning; en full licens krävs för kommersiell användning.
- **Vilken version av Java krävs?** Java 8 eller senare.

## Vad är “skapasarbete.

## Var?
- **Inga externa beroenden** – ren Java, inga inhemska DLL‑filer.
- **Fin‑granulär kontroll** över rasteriseringsalternativ såsom DPI, sidstorlek och layout‑val.
- **Batch‑bearbetning** – hantera många ritningar i ett enda körning.
- **Noggrann konvertering** – bevarar linjebredder, färger och lager.

## Förutsättningar

Innan vi börjar, se till att du har följande:

- **Java‑miljö** – JDK 8 eller nyare installerat.
- **Aspose.CAD‑bibliotek** – Ladda ner och installera Aspose.CAD‑biblioteket för Java från [download link](https://releases.aspose.com/cad/java/).
- **Dokumentkatalog** – En mapp som innehåller DWG‑ (eller andra CAD‑) ritningarna du vill konvertera.

## Importera paket

I ditt Java‑projekt, importera de nödvändiga klasserna:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Steg‑för‑steg‑guide

### Steg 1: Ladda CAD‑ritning

Först, ladda käll‑CAD‑filen (t.ex. en DWG) i ett `CadImage`‑objekt. Detta är startpunkten för alla **export CAD till PDF**‑operationer.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Steg 2: Konfigurera rasteriseringsalternativ

Definiera hur CAD‑data ska rasteriseras. Här sätter vi en grundläggande sidbredd och -höjd som kommer att användas för layouter som inte har en anpassad storlek.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Steg 3: Anpassa layout‑sidstorlekar

Om du behöver en **anpassad PDF‑sidstorlek**, lägg till poster för varje layout du vill ha med i den slutliga PDF‑filen. Detta låter dig **konvertera DWG till PDF** med olika dimensioner per layout.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Steg 4: Ställ in PDF‑alternativ

Kombinera rasteriseringsinställningarna med PDF‑specifika alternativ. `VectorRasterizationOptions`‑egenskapen talar om för Aspose.CAD att använda de layout‑storlekar vi just definierade.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 5: Spara som PDF

Slutligen, exportera CAD‑ritningen till en enda PDF‑fil som innehåller alla angivna layouter. Detta steg **sparar CAD som PDF** i ett enda anrop.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Proffstips:** Återanvänd samma `PdfOptions`‑objekt om du behöver exportera flera ritningar i en batch – det minskar overhead för objekt‑skapande.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Tomma sidor i utdata‑PDF** | Verifiera att layout‑namnen (`"ANSI C Plot"`, `"8.5 x 11 Plot"`) exakt matchar de som definierats i CAD‑filen. |
| **Lågupplöst utdata** | Öka DPI genom att anropa `rasterizationOptions.setResolution(300);` innan du sparar. |
| **Licens inte tillämpad** | Läs in din tillfälliga eller fullständiga licens innan några Aspose.CAD‑anrop: `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för Java med andra Java‑bibliotek?

A1: Ja, Aspose.CAD för Java är designat för att sömlöst integreras med andra Java‑bibliotek och erbjuder omfattande funktionalitet.

### Q2: Finns det en provversion tillgänglig?

A2: Absolut! Du kan komma åt en gratis provversion [here](https://releases.aspose.com/).

### Q3: Var kan jag hitta ytterligare support?

A3: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

### Q4: Hur får jag en tillfällig licens?

A4: Du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

### Q5: Var kan jag köpa fullversionen?

A5: Köp fullversionen av Aspose.CAD för Java [here](https://purchase.aspose.com/buy).

**Senast uppdaterad:** 2026-01-22  
**Testad med:** Aspose.CAD for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}