---
date: 2026-07-04
description: Lär dig hur du ställer in PDF-sidstorlek och exporterar PDF från 3D CAD‑bilder
  med Aspose.CAD för .NET – en steg‑för‑steg‑guide för att konvertera DWG till PDF
  och spara CAD som PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Exportera 3D-bilder till PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ställ in PDF-sidstorlek – Exportera 3D-bilder till PDF med Aspose.CAD
url: /sv/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera 3D‑bilder till PDF - Aspose.CAD‑handledning

## Introduktion

Om du behöver **ange PDF‑sidstorlek** när du konverterar en 3‑D‑CAD‑ritning till PDF, har du kommit till rätt ställe. Denna handledning visar dig steg för steg hur du laddar en CAD‑fil, konfigurerar rasteriseringsalternativ — inklusive anpassade sidmått — och genererar en högkvalitativ PDF med Aspose.CAD för .NET. I slutet kommer du att kunna **exportera PDF från CAD**, **spara CAD som PDF**, och kontrollera varje layout‑detalj utan att installera AutoCAD.

## Snabba svar

- **Vad betyder “export PDF from CAD”?** Det konverterar en CAD‑ritning (DWG, DXF, DGN, etc.) till en PDF som kan öppnas på vilken enhet som helst.  
- **Vilket bibliotek utför konverteringen?** Aspose.CAD för .NET tillhandahåller rasterisering och PDF‑export utan externa beroenden.  
- **Behöver jag en licens?** En tillfällig eller fullständig licens krävs för produktion; en gratis provversion finns tillgänglig.  
- **Kan jag ange anpassade sidmått?** Ja—använd `PageWidth` och `PageHeight` i `RasterizationOptions`.  
- **Kommer 3‑D‑geometri att bevaras?** 3‑D‑entiteterna rasteriseras; aktivera `TypeOfEntities.Entities3D` för full 3‑D‑stöd.  

## Vad betyder “export PDF” i CAD‑sammanhang?

Att exportera PDF från CAD innebär att ta en CAD‑ritning (DWG, DXF, DGN, etc.) och konvertera den till en PDF‑fil som kan innehålla vektorgrafik, rasteriserade 3‑D‑vyer och exakt sidlayoutinformation, vilket gör det enkelt att dela med någon som inte har CAD‑programvara.

## Varför använda Aspose.CAD för att exportera PDF?

Aspose.CAD låter dig **ange PDF‑sidstorlek** och exportera PDF‑filer helt i hanterad .NET‑kod. Det stöder över 50 CAD‑format, bearbetar filer upp till 2 GB utan att ladda hela dokumentet i minnet, och bevarar linjebredder, färger samt valfri 3‑D‑entitetsrendering med en rasteriserings‑DPI på upp till 1200. Biblioteket körs på Windows, Linux och macOS, så de genererade PDF‑filerna fungerar på vilken plattform som helst.

## Förutsättningar

- **Aspose.CAD for .NET** installerat. Ladda ner det från [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- En mapp som innehåller CAD‑filerna du vill konvertera (t.ex. `C:\CAD\`).  
- .NET 6.0 eller senare (eller .NET Framework 4.7.2).  

## Importera namnrymder

`using`‑satser importerar de Aspose.CAD‑namnrymder som behövs för att arbeta med rasteriserings‑ och PDF‑alternativ.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Steg‑för‑steg‑guide

### Hur man anger PDF‑sidstorlek när man exporterar CAD till PDF?

Läs in din CAD‑fil, konfigurera sidmåtten i `RasterizationOptions`, koppla dessa alternativ till en `PdfOptions`‑instans och anropa `Save`. Detta fyrastegsflöde ger dig full kontroll över utdata‑storlek och kvalitet samtidigt som koden förblir koncis.

### Steg 1: Läs in CAD‑bilden

`Image`‑klassen representerar en CAD‑ritning som laddats in i minnet, redo för rasterisering.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Steg 2: Konfigurera rasteriseringsalternativ (Spara CAD som PDF)

`RasterizationOptions`‑klassen definierar hur CAD‑data rasteriseras, inklusive sidstorlek, DPI och huruvida 3‑D‑entiteter renderas.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Steg 3: Ange PDF‑alternativ (Skapa PDF från CAD)

`PdfOptions`‑klassen innehåller inställningarna för utdataformatet och länkar rasteriseringsalternativen till PDF‑generering.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Steg 4: Spara som PDF (Generera PDF från 3D‑modell)

`Save`‑metoden på `Image`‑objektet skriver det rasteriserade innehållet till den angivna PDF‑filen och skapar ett färdigt dokument att dela.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|--------|-----|
| **Utdata‑PDF är tom** | Fel layout‑namn eller saknad `Model`‑layout. | Verifiera att `rasterizationOptions.Layouts` matchar en layout som finns i CAD‑filen. |
| **Låg upplösning** | Standard‑DPI för rasterisering är låg. | Ställ in `rasterizationOptions.Resolution = 300;` innan du sparar. |
| **3‑D‑entiteter visas inte** | `TypeOfEntities` är kommenterad. | Avkommentera `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Licensundantag** | Använder en provversion utan licens. | Applicera en tillfällig eller permanent licens via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med alla CAD‑filformat?**  
A: Ja, Aspose.CAD stöder mer än 50 in‑ och utdataformat, inklusive DWG, DXF, DGN, STL och IFC, vilket säkerställer flexibilitet för alla projekt.

**Q: Kan jag anpassa sidmåtten när jag exporterar till PDF?**  
A: Absolut. Ställ in `PageWidth` och `PageHeight` i `RasterizationOptions` till valfri storlek i punkter, tum eller millimeter innan du anropar `Save`.

**Q: Finns tillfälliga licenser tillgängliga för Aspose.CAD?**  
A: Ja, du kan skaffa tillfälliga licenser för Aspose.CAD genom att besöka [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag hitta ytterligare support eller community‑diskussioner?**  
A: Gå till [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) för expert‑hjälp och peer‑to‑peer‑råd.

**Q: Finns det en gratis provversion av Aspose.CAD?**  
A: Ja, du kan utforska funktionerna i Aspose.CAD genom att gå till [free trial](https://releases.aspose.com/).

## Slutsats

Du har nu en komplett, produktionsklar metod för att **ange PDF‑sidstorlek** och **exportera PDF från 3D‑CAD‑bilder** med Aspose.CAD för .NET. Genom att justera rasteriseringsalternativen kan du finjustera upplösning, sidlayout och 3‑D‑entitetsrendering för att möta alla dokumentationskrav. Experimentera med olika DPI‑inställningar och sidmått för att uppnå den perfekta balansen mellan filstorlek och visuell kvalitet.

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Exportera specifika layouter till PDF - Aspose.CAD‑guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exportera DWG till PDF eller rasterbilder - Aspose.CAD‑guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportera DGN till PDF i Aspose.CAD för .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Senast uppdaterad:** 2026-07-04  
**Testat med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose