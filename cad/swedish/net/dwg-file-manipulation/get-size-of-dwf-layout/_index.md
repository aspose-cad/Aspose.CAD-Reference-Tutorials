---
date: 2026-04-06
description: Lär dig hur du konverterar DWF till JPG i C# med Aspose.CAD och upptäck
  hur du extraherar DWF‑layoutens storlek från DWG‑filer.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Arbeta med DWG-filer i C# – Hämta storlek på DWF‑layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DWF till JPG i C# – Hämta DWF‑layoutstorlek från DWG
url: /sv/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DWF till JPG i C# – Hämta DWF‑layoutstorlek från DWG

## Introduktion

Om du behöver **konvertera DWF till JPG** samtidigt som du ska ta reda på de exakta layoutmåtten, är du på rätt plats. I den här handledningen går vi igenom ett komplett, end‑to‑end‑exempel som använder Aspose.CAD för .NET för att öppna en DWG‑baserad DWF‑fil, läsa varje layouts storlek och spara layouten som en högkvalitativ JPG‑bild. I slutet vet du inte bara hur du extraherar DWF‑layoutinformation utan har också ett återanvändbart kodsnutt som du kan lägga in i vilket C#‑projekt som helst.

## Snabba svar
- **Vad betyder “convert DWF to JPG”?** Det betyder att rasterisera en vektor‑DWF‑layout till en bitmap‑JPEG‑bild.  
- **Varför läsa layoutstorlek först?** Att känna till de exakta måtten låter dig ange rätt sidodimensioner och undvika utdragen eller avklippt output.  
- **Vilket bibliotek hanterar detta?** Aspose.CAD för .NET erbjuder fullt stöd för DWG, DWF och rasterbildskonvertering.  
- **Behöver jag en licens?** En temporär licens fungerar för utvärdering; en fullständig licens krävs för produktion.  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Vad är “convert DWF to JPG” och varför är det viktigt?

Att konvertera en DWF (Design Web Format)-fil till JPG skapar en portabel bild som kan visas i webbläsare, bäddas in i rapporter eller delas med intressenter som inte har CAD‑programvara. Konverteringen ger dig också flexibiliteten att manipulera bilden (ändra storlek, komprimera, vattenstämpel) med vanliga bildbehandlingsverktyg.

## Varför extrahera DWF‑layoutstorlek?

En DWF‑fil kan innehålla flera layouter, var och en med sitt eget koordinatsystem och enheter (tum, millimeter osv.). Att extrahera layoutstorleken låter dig:

1. Bevara det ursprungliga bildförhållandet vid rasterisering.  
2. Välja rätt DPI för högupplöst output.  
3. Automatisera batch‑behandling av många layouter utan manuell justering.

## Förutsättningar

För att följa den här handledningen utan avbrott, se till att du har följande förutsättningar på plats:

- Aspose.CAD för .NET: Se till att du har Aspose.CAD för .NET installerat. Du kan ladda ner det från [Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).

Att ha biblioteket redo betyder att du kan fokusera på koden istället för att leta efter beroenden.

## Importera namnrymder

Innan vi börjar koda, importera de nödvändiga namnrymderna. Dessa tillhandahåller de klasser vi behöver för att arbeta med CAD‑filer, rasteriseringsalternativ och fil‑I/O.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Steg 1: Ställ in din miljö

Skapa ett nytt C#‑konsol‑ eller klassbiblioteksprojekt, lägg till en referens till **Aspose.CAD.dll**, och se till att projektet riktar mot en kompatibel .NET‑version.

## Steg 2: Definiera filsökvägar (hur man extraherar DWF)

Ange var din käll‑DWF‑fil finns och var de genererade JPG‑filerna ska skrivas.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** Använd `Path.Combine(MyDir, "blocks_and_tables.dwf")` för säkrare sökvägshantering på olika OS.

## Steg 3: Ladda DWF‑bilden

Ladda DWF‑filen i ett `Aspose.CAD.Image`‑objekt. Vi kastar det till `DwfImage` eftersom vi behöver åtkomst till sid‑specifika egenskaper.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Steg 4: Iterera genom sidor

En DWF kan innehålla flera sidor (layouter). Loop igenom varje sida så att vi kan bearbeta dem individuellt.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Steg 5: Hämta layoutinformation

Inuti loopen, hämta layoutnamnet. Detta namn används både för loggning och för att namnge den resulterande JPG‑filen.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Steg 6: Ställ in JPG‑alternativ

Skapa en `JpegOptions`‑instans och konfigurera rasteriseringsalternativen. `Layouts`‑egenskapen talar om för Aspose.CAD vilken layout som ska renderas.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Steg 7: Bestäm sidstorlek (konvertera dwg till jpg)

Beräkna bredd och höjd på layouten i dess ursprungliga enheter. Denna information är avgörande för att korrekt ställa in raster‑sidstorlek.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Steg 8: Ställ in sidimensioner

Konvertera de ursprungliga enheterna (tum eller millimeter) till pixlar med hjälp av hjälpfunktionerna som tillhandahålls av Aspose.CAD. Om enhetstypen är annan, faller vi tillbaka på att använda de råa värdena.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Steg 9: Spara JPG‑filen

Till sist bindes rasteriseringsalternativen till JPEG‑alternativen och bilden sparas till **disk**.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

När loopen är klar har du en JPG‑fil för varje layout, varje fil har exakt samma storlek som den ursprungliga DWF‑dimensionen.

## Vanliga problem och lösningar

| Symtom | Trolig orsak | Åtgärd |
|---------|--------------|-----|
| Tom JPG‑output | `options.Layouts` är inte korrekt inställd | Verifiera att layoutnamnet matchar `page.Name`. |
| Förvrängd bild | Fel DPI‑konvertering | Använd `CommonHelper.DPI = 300` (eller ditt mål‑DPI) före konvertering. |
| Filen hittades inte | Felaktig `MyDir`‑sökväg | Använd absoluta sökvägar eller `Path.Combine`. |
| Licensundantag | Ingen licens tillämpad | Läs in en temporär eller permanent licens innan du anropar `Image.Load`. |

## Vanliga frågor

### Q1: Är Aspose.CAD kompatibel med de senaste DWG‑filformaten?

A1: Aspose.CAD stöder olika DWG‑filformat, inklusive de senaste versionerna. Se [dokumentationen](https://reference.aspose.com/cad/net/) för specifika kompatibilitetsdetaljer.

### Q2: Kan jag använda Aspose.CAD för både kommersiella och personliga projekt?

A2: Ja, Aspose.CAD erbjuder flexibla licensalternativ för både kommersiell och personlig användning. Besök [köpsidan](https://purchase.aspose.com/buy) för mer information.

### Q3: Hur kan jag skaffa en temporär licens för Aspose.CAD?

A3: Du kan få en temporär licens från [här](https://purchase.aspose.com/temporary-license/) för utvärderingsändamål.

### Q4: Var kan jag hitta support för Aspose.CAD?

A4: För frågor eller hjälp, besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19).

### Q5: Finns det en gratis provversion av Aspose.CAD?

A5: Ja, du kan få åtkomst till en gratis provversion av Aspose.CAD [här](https://releases.aspose.com/).

### Q6: Hur konverterar jag en DWG‑fil direkt till JPG utan att först extrahera DWF?

A6: Du kan ladda DWG‑filen med `Aspose.CAD.Image.Load` och använda samma rasteriseringsarbetsflöde; ange bara `options.Layouts` till önskat layoutnamn/namn från DWG.

### Q7: Bevarar konverteringen vektor‑kvaliteten?

A7: När den rasteriseras till JPG blir bilden bitmap‑baserad, så vektorskala förloras. För förlustfri skalning, överväg att exportera till PNG eller SVG istället.

**Senast uppdaterad:** 2026-04-06  
**Testad med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}