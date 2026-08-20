---
date: 2026-04-03
description: Lär dig hur du ställer in viewport och konverterar DWG till PDF i C#
  med Aspose.CAD. Denna DWG‑till‑PDF-handledning visar exakt export med koordinater.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Konvertera DWG till PDF med koordinater i C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man ställer in viewport vid konvertering av DWG till PDF med koordinater
  i C# – Aspose.CAD-handledning
url: /sv/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DWG till PDF med koordinater i C# - Aspose.CAD-handledning

## Introduktion

Välkommen till denna omfattande handledning om **how to set viewport** medan du konverterar DWG-filer till PDF med angivna koordinater med hjälp av Aspose.CAD för .NET. Genom att kontrollera viewport får du pixelperfekta PDF-filer som exakt matchar det område du behöver – perfekt för konstruktionsritningar, planritningsförhandsvisningar eller någon BIM-arbetsflöde.

## Snabba svar
- **Vad betyder “set viewport”?** Det definierar det synliga området och skalningen av CAD-ritningen under rasterisering.  
- **Vilket bibliotek hanterar konverteringen?** Aspose.CAD för .NET.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Stödda plattformar?** Windows, Linux och macOS med .NET 5/6/7 eller .NET Framework 4.6+.  
- **Typisk implementeringstid?** Ungefär 10‑15 minuter för en grundläggande konvertering.

## Förutsättningar

**Innan vi börjar, se till att du har följande förutsättningar:**

- **Aspose.CAD Library** – Ladda ner och installera Aspose.CAD-biblioteket för .NET. Du kan hitta biblioteket [här](https://releases.aspose.com/cad/net/).
- **Utvecklingsmiljö** – Visual Studio, Rider eller någon IDE som stödjer .NET-utveckling.
- **DWG-fil** – Ha en DWG-fil redo för konvertering. Du kan använda den medföljande exempel-filen eller din egen DWG-fil.

## Hur man ställer in viewport för exakt PDF-export

Att ställa in viewport är kärnsteg som låter dig definiera exakt det område av ritningen du vill rendera. I koden nedan skapar vi ett nytt `CadVportTableObject`, placerar det med den övre‑vänstra koordinaten och beräknar bredd, höjd och bildförhållande. Detta är **how to set viewport**-implementeringen som driver resten av konverteringen.

## Importera namnrymder

I ditt C#-projekt, importera de nödvändiga namnrymderna:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Låt oss gå igenom koden steg för steg för bättre förståelse:

## Steg 1: Definiera dokumentkatalogen

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Ange sökvägen till käll‑DWG‑filen

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Steg 3: Ladda DWG-fil och konfigurera rasteriseringsalternativ

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Steg 4: Definiera koordinater och viewport  

Här **ställer vi faktiskt in viewport** (how to set viewport) genom att ange det övre‑vänstra hörnet, bredd och höjd på det område du vill exportera.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Steg 5: Tillämpa viewport‑inställningar

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Steg 6: Konfigurera PDF‑alternativ och export  

Nu knyter vi ihop allt och **konverterar DWG till PDF** med hjälp av rasteriseringsalternativen vi just förberedde.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Steg 7: Visa framgångsmeddelande

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Vanliga användningsfall

- **Konstruktionsdokumentation** – Generera utskrivbara PDF-filer av specifika planritningssektioner.  
- **BIM‑koordinering** – Exportera endast det intresseområde för krockdetektion.  
- **Kundpresentationer** – Tillhandahåll en ren PDF av ett valt rum eller en elevation utan att avslöja hela ritningen.

## Slutsats

Grattis! Du har framgångsrikt **konverterat DWG till PDF** med exakta koordinater och lärt dig **how to set viewport** med Aspose.CAD för .NET. Denna **dwg to pdf tutorial** visar hur man **skapar pdf från dwg** och **exporterar dwg som pdf c#** samtidigt som du behåller full kontroll över utskriftsområdet.

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD med andra CAD‑filformat?

A1: Ja, Aspose.CAD stödjer olika CAD-format, inklusive DWG, DXF, DWF och fler.

### Q2: Hur kan jag hantera fel under konverteringsprocessen?

A2: Implementera felhanteringsmekanismer med try‑catch‑block för att fånga och hantera undantag.

### Q3: Är Aspose.CAD lämplig för både Windows- och Linux-miljöer?

A3: Ja, Aspose.CAD är kompatibel med både Windows- och Linux-plattformar.

### Q4: Kan jag anpassa PDF-utdata ytterligare?

A4: Absolut! Utforska de omfattande alternativ som Aspose.CAD erbjuder för att skräddarsy PDF-utdata efter dina specifika krav.

### Q5: Var kan jag hitta ytterligare support eller community‑diskussioner?

A5: Besök [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

## Ytterligare vanliga frågor

**Q: Fungerar detta tillvägagångssätt med stora DWG-filer (hundratals MB)?**  
**A:** Ja. Rasteriseringen utförs sida‑för‑sida, och du kan justera `rasterizationOptions` (t.ex. `Resolution`) för att balansera kvalitet och minnesanvändning.

**Q: Kan jag exportera flera viewports till separata PDF‑sidor?**  
**A:** Du kan loopa igenom `cadImage.ViewPorts`, sätta varje som aktiv och anropa `Save` för varje sida, sedan slå ihop PDF-filer med Aspose.PDF.

**Q: Är det möjligt att lägga till ett vattenmärke i den genererade PDF‑filen?**  
**A:** Efter att PDF-filen sparats kan du öppna den igen med Aspose.PDF och applicera ett text‑ eller bildvattenmärke innan du levererar den till användaren.

---

**Senast uppdaterad:** 2026-04-03  
**Testad med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}