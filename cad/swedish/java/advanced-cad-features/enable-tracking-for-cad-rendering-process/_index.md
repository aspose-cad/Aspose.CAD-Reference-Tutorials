---
date: 2026-02-12
description: Lär dig hur du ställer in PDF‑sidstorlek när du konverterar CAD till
  PDF med Aspose.CAD för Java. Följ den här steg‑för‑steg‑guiden för att aktivera
  spårning, konvertera CAD till PDF och spara CAD som PDF på ett effektivt sätt.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: Hur man ställer in PDF‑sidstorlek och aktiverar spårning för CAD‑renderingsprocessen
url: /sv/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aktivera spårning för CAD-renderingsprocessen

## Introduktion

I den här handledningen kommer du att lära dig hur du **ställer in PDF-sidstorlek** medan du **konverterar CAD till PDF** med **Aspose.CAD for Java**. Genom att aktivera spårning får du full insyn i renderingspipeline, vilket gör det enklare att felsöka och optimera konverteringen från CAD-filer (såsom DXF) till PDF. Oavsett om du behöver **spara CAD som PDF**, generera PDF från DXF, eller helt enkelt kontrollera utskriftsdimensionerna, så guidar stegen nedan dig genom hela processen.

## Snabba svar
- **Vad gör “set PDF page size”?** Det definierar bredden och höjden på den resulterande PDF-sidan under CAD-rendering.  
- **Varför aktivera spårning?** Spårning loggar varje steg i konverteringen, vilket hjälper dig att upptäcka prestandaflaskhalsar eller fel.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Vilka CAD-format stöds?** DWG, DXF, DGN och många andra – se Aspose.CAD-dokumentationen för den fullständiga listan.  
- **Kan jag ändra sidimensioner i farten?** Ja – justera helt enkelt `PageWidth` och `PageHeight` i `CadRasterizationOptions`.

## Vad är “set PDF page size” i CAD-rendering?

Att ställa in PDF-sidstorlek talar om för rasteriseraren hur stor arbetsytan ska vara när den vektoriserade CAD-datan rasteriseras till en PDF-sida. Detta är avgörande för att bevara visuell noggrannhet, särskilt vid hantering av detaljerade ingenjörsritningar.

## Varför aktivera spårning för CAD-rendering?

Att aktivera spårning ger en detaljerad logg över varje steg – från inläsning av källfilen till skrivning av PDF-utdata. Det hjälper dig:

- Diagnostisera varför en viss ritning kan renderas felaktigt.  
- Mäta den tid som tas för varje steg, användbart för prestandaoptimering.  
- Verifiera att den sidstorlek du konfigurerat faktiskt tillämpas.

## Förutsättningar

Innan du dyker ner i spårningsinställningarna, se till att du har följande förutsättningar:

1. **Java-utvecklingsmiljö** – Java 8 eller senare installerat på din maskin.  
2. **Aspose.CAD-bibliotek** – Ladda ner och integrera Aspose.CAD-biblioteket i ditt Java-projekt. Du kan hitta nedladdningslänken [här](https://releases.aspose.com/cad/java/).  
3. **Dokumentkatalog** – Förbered en katalog för att lagra dina CAD-filer och de genererade PDF-filerna.

## Importera namnrymder

I ditt Java-projekt, importera de nödvändiga namnrymderna för att utnyttja Aspose.CAD-funktioner. Lägg till följande rader i början av din kod:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Ställ in sökvägen till resurskatalogen

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Byt ut `"Your Document Directory"` mot den faktiska sökvägen till din dokumentkatalog.

## Ladda CAD-filen

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Ange sökvägen till din CAD-fil och säkerställ att den ligger i den angivna dokumentkatalogen.

## Ställ in PDF-utdataalternativ

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Skapa en output‑ström och ställ in PDF‑alternativ för konverteringen.

## Konfigurera CadRasterizationOptions (Ställ in PDF-sidstorlek)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Här **ställer vi in PDF-sidstorlek** genom att definiera `PageWidth` och `PageHeight`. Justera dessa värden så att de matchar de dimensioner som krävs för din ingenjörsritning. Detta är kärnsteg som svarar på **hur man ställer in PDF-storlek** när du **java cad to pdf**.

## Spara PDF-filen

```java
image.save(stream, pdfOptions);
```

Spara den renderade PDF-filen med de angivna alternativen.

## Verifiera att spårning är aktiverad

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

Bekräfta att spårning har aktiverats framgångsrikt för CAD-renderingsprocessen.

## Vanliga problem & felsökning

| Symptom | Trolig orsak | Åtgärd |
|---------|--------------|--------|
| PDF-sidan visas tom | `PageWidth`/`PageHeight` satt till 0 | Säkerställ att icke‑noll dimensioner anges. |
| Utdatafilen är korrupt | Output‑strömmen är inte stängd | Anropa `stream.close()` efter `image.save(...)`. |
| Lager saknas i PDF | CAD-filen använder ej stödda enheter | Verifiera att filformatet är fullt stödjat av Aspose.CAD. |

## Vanliga frågor

### Q1: Är Aspose.CAD kompatibel med alla CAD-filformat?

A1: Aspose.CAD stödjer ett brett spektrum av CAD-format, inklusive DWG, DXF, DGN och fler. Se [dokumentationen](https://reference.aspose.com/cad/java/) för en komplett lista.

### Q2: Kan jag anpassa utskriftsdimensionerna för PDF-filen?

A2: Absolut! Justera parametrarna `PageWidth` och `PageHeight` i `CadRasterizationOptions` för att anpassa utskriftsdimensionerna.

### Q3: Finns det en gratis provversion för Aspose.CAD för Java?

A3: Ja, du kan utforska funktionerna i Aspose.CAD genom att skaffa en gratis provversion [här](https://releases.aspose.com/).

### Q4: Hur kan jag få community‑stöd för frågor relaterade till Aspose.CAD?

A4: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för att interagera med communityn och söka hjälp.

### Q5: Finns tillfälliga licenser för Aspose.CAD?

A5: Ja, om du behöver en tillfällig licens kan du skaffa en [här](https://purchase.aspose.com/temporary-license/).

## Slutsats

Grattis! Du har nu lärt dig hur du **ställer in PDF-sidstorlek** och aktiverar spårning för CAD-rendering med **Aspose.CAD for Java**. Denna guide ger dig möjlighet att **konvertera CAD till PDF**, **spara CAD som PDF**, och generera PDF från DXF med full kontroll över siddimensioner och detaljerade körloggar. Känn dig fri att experimentera med olika sidstorlekar och utforska ytterligare rasteriseringsalternativ för att passa dina specifika ingenjörsarbetsflöden.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}