---
date: 2026-02-20
description: Lär dig hur du exporterar AutoCAD PDF med Aspose.CAD för Java. Denna
  steg‑för‑steg‑guide visar dig hur du **konverterar DWG till PDF**, **sparar CAD
  som PDF** och hanterar licensiering.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Konvertera DWG till PDF – Exportera AutoCAD‑bilder till PDF med Aspose.CAD
  för Java
url: /sv/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

CAD Images to PDF with Aspose.CAD for Java" -> "Exportera AutoCAD PDF - Exportera AutoCAD-bilder till PDF med Aspose.CAD för Java". Keep "Export AutoCAD PDF" maybe keep as is? We'll translate.

Make sure to keep markdown formatting.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera AutoCAD PDF - Exportera AutoCAD‑bilder till PDF med Aspose.CAD för Java

## Introduktion

Letar du efter ett sätt att **konvertera DWG till PDF** med Java? Sök inte längre! I den här handledningen går vi igenom hur du konverterar AutoCAD‑bilder till PDF med Aspose.CAD för Java, ett kraftfullt bibliotek som gör **konverteringen från DWG till PDF** enkel. I slutet kommer du att förstå hur du **sparar CAD som PDF**, använder anpassade rasteriseringsinställningar och arbetar med en Aspose.CAD‑licens för produktionsbruk.

## Snabba svar
- **Kan jag konvertera DWG till PDF med Java?** Ja, Aspose.CAD för Java hanterar DWG, DXF och många andra format.  
- **Behöver jag en licens?** En **Aspose CAD‑licens** krävs för obegränsad användning; en tillfällig licens finns tillgänglig för utvärdering.  
- **Vilken Java‑version stöds?** Java 8+ (biblioteket är kompatibelt med alla moderna JDK).  
- **Kan jag anpassa PDF‑sidstorlek?** Absolut – justera `pageWidth` och `pageHeight` i rasteriseringsalternativen.  
- **Är 3‑D‑rasterisering möjlig?** Ja, aktivera `TypeOfEntities.Entities3D` för full 3‑D‑rendering.

## Vad är **export autocad pdf**?
Att exportera AutoCAD PDF innebär att konvertera vektorbaserade CAD‑ritningar (DWG, DXF, DWF osv.) till ett portabelt PDF‑dokument samtidigt som lager, linjebredder och eventuellt 3‑D‑geometri bevaras. Detta är användbart för att dela design med kunder, arkivera eller skriva ut utan att behöva CAD‑programvara.

## Varför konvertera DWG till PDF med Aspose.CAD för Java?
- **Fullt formatstöd** – fungerar med DWG, DXF, DWF och många fler.  
- **Inga externa beroenden** – rent Java‑bibliotek, inga inhemska DLL‑filer.  
- **Högkvalitativ rasterisering** – kontroll över DPI, sidstorlek och layout, så att du kan **anpassa PDF‑sidstorlek** efter projektets krav.  
- **Licensflexibilitet** – börja med en gratis provperiod och uppgradera sedan till en permanent **Aspose CAD‑licens**.  

## Förutsättningar

Innan du dyker ner, se till att du har:

- **Java‑utvecklingsmiljö** – JDK 8 eller senare installerad.  
- **Aspose.CAD för Java‑bibliotek** – ladda ner från [download link](https://releases.aspose.com/cad/java/).  
- **Dokumentkatalog** – en mapp på din maskin där käll‑CAD‑filerna och de genererade PDF‑filerna ska ligga.

## Importera namnrymder

I ditt Java‑projekt importerar du de nödvändiga klasserna för att arbeta med Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Låt oss nu gå igenom koden steg för steg.

## Så konverterar du DWG till PDF med Aspose.CAD för Java

### Steg 1: Ange sökvägen till resurskatalogen

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Proffstips:** Ersätt `"Your Document Directory"` med den absoluta sökvägen till den mapp du skapade i förutsättningarna.

### Steg 2: Ladda CAD‑bilden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Varför detta är viktigt:** Att ladda CAD‑filen i ett `Image`‑objekt ger dig full åtkomst till Aspose.CAD:s rasteriseringsmotor.

### Steg 3: Ställ in rasteriseringsalternativ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Justera `pageWidth` och `pageHeight` för att **anpassa PDF‑sidstorlek**.  
- Avkommentera raden `setTypeOfEntities` om du behöver **java convert cad pdf** för 3‑D‑entiteter.  
- Anropet `setLayouts` väljer vilken layout (Model, Layout1 osv.) som ska renderas.

### Steg 4: Konfigurera PDF‑alternativ

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Detta kopplar rasteriseringsinställningarna till PDF‑utdata och säkerställer att vektordatan konverteras korrekt.

### Steg 5: Spara PDF‑filen

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Den resulterande filen, `Export3DImagestoPDF_out_.pdf`, är en **save cad as pdf**‑representation av din ursprungliga AutoCAD‑ritning.

## Vanliga problem & lösningar

| Symptom | Trolig orsak | Åtgärd |
|---------|--------------|--------|
| Tom PDF‑utdata | Rasteriseringsalternativ ej satta eller fel layout | Kontrollera att `setLayouts` matchar layoutnamnet i din CAD‑fil. |
| Lågupplöst bild | `pageWidth`/`pageHeight` för små | Öka dimensionerna eller sätt ett högre DPI‑värde via `rasterizationOptions.setResolution(...)`. |
| Licensundantag | Ingen giltig licens tillämpad | Använd en **Aspose CAD‑licens** eller en tillfällig licens för testning. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?
A1: Ja, Aspose.CAD stödjer ett brett spektrum av format inklusive DWG, DWF, DGN och fler, vilket ger dig flexibilitet i dina projekt.

### Q2: Hur får jag en tillfällig licens för Aspose.CAD för Java?
A2: Besök [here](https://purchase.aspose.com/temporary-license/) för att skaffa en tillfällig licens för utvärdering.

### Q3: Finns det layoutalternativ för rasterisering?
A3: Ja, du kan anpassa layouter (t.ex. `"Model"`, `"Layout1"`) via metoden `setLayouts` för att styra vilken vy som renderas.

### Q4: Kan jag anpassa storleken på den genererade PDF‑filen?
A4: Absolut! Justera parametrarna `pageWidth` och `pageHeight` i rasteriseringsalternativen för att passa dina önskade dimensioner.

### Q5: Var kan jag få hjälp eller diskutera problem relaterade till Aspose.CAD för Java?
A5: Gå till [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för dedikerad support och community‑diskussioner.

---

**Senast uppdaterad:** 2026-02-20  
**Testad med:** Aspose.CAD för Java 24.10  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}