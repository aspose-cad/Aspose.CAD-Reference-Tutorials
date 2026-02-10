---
date: 2025-12-19
description: Lär dig hur du exporterar AutoCAD PDF med Aspose.CAD för Java. Denna
  steg‑för‑steg‑guide visar hur du konverterar DWG till PDF, sparar CAD som PDF och
  hanterar licensiering.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Exportera AutoCAD PDF – Exportera AutoCAD‑bilder till PDF med Aspose.CAD för
  Java‑handledning
url: /sv/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera AutoCAD PDF - Exportera AutoCAD-bilder till PDF med Aspose.CAD för Java

## Introduktion

Vill du smidigt **exportera AutoCAD PDF** med Java? Leta inte längre! I den här handledningen guidar vi dig genom hur du konverterar AutoCAD-bilder till PDF med Aspose.CAD för Java, ett kraftfullt bibliotek som gör **konverteringen av DWG till PDF** enkel. I slutet kommer du att förstå hur du **sparar CAD som PDF**, tillämpar anpassade rasteriseringsinställningar och arbetar med en Aspose.CAD-licens för produktionsbruk.

## Snabba svar
- **Kan jag konvertera DWG till PDF med Java?** Ja, Aspose.CAD för Java hanterar DWG, DXF och många andra format.
- **Behöver jag en licens?** En **Aspose CAD-licens** krävs för obegränsad användning; en tillfällig licens finns tillgänglig för utvärdering.
- **Vilken Java-version stöds?** Java8+ (biblioteket är kompatibelt med alla moderna JDK:er).
- **Kan jag anpassa PDF-sidstorleken?** Absolut – justera `pageWidth` och `pageHeight` i rasteriseringsalternativen.
- **Är 3D-rasterisering möjlig?** Ja, aktivera `TypeOfEntities.Entities3D` för fullständig 3D-rendering.

## Vad är **exportera autocad pdf**?
Att exportera AutoCAD PDF innebär att konvertera vektorbaserade CAD-ritningar (DWG, DXF, DWF, etc.) till ett portabelt PDF-dokument samtidigt som lager, linjetjocklekar och eventuellt 3D-geometri bevaras. Detta är användbart för att dela design med kunder, arkivera eller skriva ut utan att kräva CAD-programvara.

## Varför använda Aspose.CAD för Java för att **exportera autocad pdf**?

- **Fullständigt formatstöd** – fungerar med DWG, DXF, DWF och många fler.
- **Inga externa beroenden** – rent Java-bibliotek, inga inbyggda DLL-filer.
- **Högkvalitativ rasterisering** – kontroll över DPI, sidstorlek och layout.
- **Licensflexibilitet** – börja med en gratis provperiod och uppgradera sedan till en permanent **Aspose CAD-licens**.

## Förutsättningar

Innan du börjar, se till att du har:

- **Java Development Environment** – JDK8 eller senare installerat.
- **Aspose.CAD for Java Library** – ladda ner från [nedladdningslänken](https://releases.aspose.com/cad/java/).
- **Dokumentkatalog** – en mapp på din dator där käll-CAD-filerna och de genererade PDF-filerna kommer att finnas.

## Importera namnrymder

Importera de nödvändiga klasserna i ditt Java-projekt för att arbeta med Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Nu ska vi gå igenom koden steg för steg.

## Steg-för-steg-guide

### Steg 1: Ange sökvägen till resurskatalogen

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Proffstips:** Ersätt `"Din dokumentkatalog"` med den absoluta sökvägen till mappen du skapade i förutsättningarna.

### Steg 2: Ladda CAD-bilden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Varför detta är viktigt:** Att ladda CAD-filen till ett `Image`-objekt ger dig fullständig åtkomst till Aspose.CADs rasteriseringsmotor.

### Steg 3: Ange rasteriseringsalternativ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Justera `pageWidth` och `pageHeight` för att ändra storleken på utdata-PDF-filen.
- Avkommentera raden `setTypeOfEntities` om du behöver **java convert cad pdf** för 3D-enheter.
- Anropet `setLayouts` väljer vilken layout (Modell, Layout1, etc.) som ska renderas.

### Steg 4: Konfigurera PDF-alternativ

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Detta kopplar rasterinställningarna till PDF-utdata, vilket säkerställer att vektordata konverteras korrekt.

### Steg 5: Spara PDF-filen

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Den resulterande filen, `Export3DImagestoPDF_out_.pdf`, är en **spara CAD som PDF**-representation av din ursprungliga AutoCAD-ritning.

## Vanliga problem och lösningar

| Symtom | Trolig orsak | Åtgärd |
|---------|--------------|-----|
| Tom PDF-utdata | Rasteriseringsalternativ är inte inställda eller layouten stämmer inte överens | Verifiera att `setLayouts` matchar layoutnamnet i din CAD-fil. |
| Lågupplöst bild | `pageWidth`/`pageHeight` är för liten | Öka måtten eller ange en högre DPI via `rasterizationOptions.setResolution(...)`. |
| Licensundantag | Ingen giltig licens tillämpad | Använd en **Aspose CAD-licens** eller använd en tillfällig licens för testning. |

## Vanliga frågor

### F1: Kan jag använda Aspose.CAD för Java med andra CAD-filformat?
A1: Ja, Aspose.CAD stöder ett brett utbud av format, inklusive DWG, DWF, DGN med flera, vilket ger dig flexibilitet i dina projekt.

### F2: Hur kan jag få en tillfällig licens för Aspose.CAD för Java?
A2: Besök [här](https://purchase.aspose.com/temporary-license/) för att få en tillfällig licens för utvärdering.

### F3: Finns det några layoutalternativ för rasterisering?
A3: Ja, du kan anpassa layouter (t.ex. `"Model"`, `"Layout1"`) genom metoden `setLayouts` för att kontrollera vilken vy som renderas.

### F4: Kan jag anpassa storleken på PDF-filen som visas?
A4: Absolut! Justera parametrarna `pageWidth` och `pageHeight` i rasteriseringsalternativen så att de passar dina önskade dimensioner.

### F5: Var kan jag söka hjälp eller diskutera problem relaterade till Aspose.CAD för Java?
A5: Gå till [Aspose.CAD-forumet](https://forum.aspose.com/c/cad/19) för dedikerad support och diskussioner i gemenskapen.

--

**Senast uppdaterad:** 2025-12-19
**Testad med:** Aspose.CAD för Java 24.10
**Författare:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}