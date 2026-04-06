---
date: 2026-04-06
description: Lär dig hur du konverterar DWG till PDF och lägger till anpassad text
  med C# och Aspose.CAD. Denna steg‑för‑steg‑guide täcker generering av PDF från DWG,
  infogning av ett textelement och ändring av DWG‑textens teckensnitt.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Lägga till text i DWG-filer i C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DWG till PDF och lägg till text i C# – Aspose.CAD-handledning
url: /sv/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DWG till PDF och lägg till text i C# – Aspose.CAD-handledning

## Introduktion

I den snabbt föränderliga världen av CAD och .NET‑utveckling är **konvertering av DWG till PDF** samtidigt som man infogar anpassade annotationer ett vanligt krav. Oavsett om du behöver skapa utskrivbara ritningar för kunder eller bädda in dynamiska anteckningar direkt i en DWG, gör Aspose.CAD jobbet enkelt. I den här handledningen kommer du att lära dig hur du **konverterar DWG till PDF**, **lägger till en textelement** och till och med **ändrar DWG‑textens teckensnitt** med C#.

## Snabba svar

- **Vilket bibliotek är bäst för DWG‑till‑PDF‑konvertering?** Aspose.CAD för .NET  
- **Kan jag lägga till anpassad text under konverteringen?** Ja – skapa ett `CadText`‑objekt och lägg till det innan du sparar.  
- **Behöver jag en licens för produktionsanvändning?** En kommersiell licens krävs; en gratis provversion finns tillgänglig.  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Är det möjligt att ändra textens teckensnitt?** Ja, justera `CadText`‑egenskaper som `StyleType` och `TextHeight`.  

## Vad är “konvertera dwg till pdf”?

Att konvertera en DWG‑fil till PDF omvandlar en vektorbaserad CAD‑ritning till ett brett delbart, enhetsoberoende dokument. PDF‑filen behåller den ursprungliga geometrin och lagren, samtidigt som du kan bädda in annotationer, text eller annan metadata. Aspose.CAD hanterar rasterisering och vektorrendering automatiskt, så du behöver ingen tredjeparts‑CAD‑programvara på servern.

## Varför lägga till text i en DWG före konvertering?

Att bädda in text direkt i DWG ger dig full kontroll över placering, stil och lagertilldelning. När filen senare konverteras till PDF visas texten exakt där du placerade den, vilket bevarar designintentionen och eliminerar behovet av efterbearbetning i en PDF‑redigerare.

## Förutsättningar

- **Aspose.CAD Library** – ladda ner den från [download link](https://releases.aspose.com/cad/net/).  
- **En fungerande .NET‑miljö** (Visual Studio 2022, .NET 6, eller någon kompatibel version).  
- **En mapp för dina testfiler** – vi kommer att referera till den som `MyDir` genom hela guiden.

Låt oss nu gå igenom processen steg för steg.

## Importera namnrymder

Lägg till de nödvändiga `using`‑satserna så att du kan komma åt Aspose.CAD‑klasser.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Ladda DWG‑filen

Ladda din käll‑DWG‑fil i ett `Image`‑objekt. Detta objekt ger dig åtkomst till de underliggande CAD‑entiteterna.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Steg 2: Skapa ett CadText‑objekt (Infoga textelement)

`CadText`‑klassen representerar en enstaka textrad i en DWG. Här sätter vi dess stil, värde, färg, lager och position. Justera `StyleType` eller `TextHeight` för att **ändra DWG‑textens teckensnitt**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Steg 3: Lägg till textelementet i modellutrymmet

DWG‑modellutrymmet innehåller de flesta ritningselement. Genom att lägga till vår `CadText` i `*Model_Space`‑blocket blir texten en del av ritningen.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Steg 4: Konfigurera PDF‑alternativ (Generera PDF från DWG)

Ställ in rasteriseringsalternativ som styr hur DWG renderas till en PDF. Du kan justera sidstorlek, rittyp och layout.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Steg 5: Spara den modifierade DWG‑filen som PDF

Slutligen exporterar du den modifierade ritningen. Den resulterande PDF‑filen innehåller den nyinfogade texten.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Proffstips:** Om du behöver en PDF med högre upplösning, öka `PageHeight` och `PageWidth` proportionellt.

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|-------|--------|-----|
| Text visas inte i PDF | Fel lager eller färg‑ID | Se till att `LayerName` finns och att `ColorId` är satt till en synlig färg (t.ex. 7 för vit). |
| Text är felplacerad | Felaktiga justeringskoordinater | Verifiera `FirstAlignment.X/Y`‑värden i förhållande till ritningens enheter. |
| PDF är tom | Rasteriseringsalternativ har inte ställts in | Ställ in `DrawType` till `UseObjectColor` eller `UseObjectLineWeight`. |

## Vanliga frågor (existerande)

### Q1: Är Aspose.CAD kompatibel med alla versioner av DWG‑filer?

A1: Aspose.CAD stöder ett brett spektrum av DWG‑filversioner, vilket säkerställer kompatibilitet med olika CAD‑program.

### Q2: Kan jag lägga till flera textelement i en enda DWG‑fil med Aspose.CAD?

A2: Ja, du kan lägga till flera textelement i en DWG‑fil genom att upprepa processen som beskrivs i handledningen.

### Q3: Hur kan jag ändra textens teckensnitt och stil i Aspose.CAD?

A3: För att ändra textens teckensnitt och stil, justera egenskaperna för `CadText`‑objektet innan du lägger till det i DWG‑filen.

### Q4: Finns det några licensaspekter att beakta vid användning av Aspose.CAD i ett kommersiellt projekt?

A5: Ja, säkerställ att du följer Aspose.CAD‑licensvillkoren. Se [Aspose.CAD Purchase](https://purchase.aspose.com/buy) för detaljer.

### Q5: Var kan jag få hjälp eller diskutera frågor relaterade till Aspose.CAD?

A5: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för att komma i kontakt med communityn och få support.

## Ytterligare vanliga frågor

**Q: Hur genererar jag PDF från DWG utan att lägga till text?**  
A: Hoppa över steget för att skapa `CadText` och konfigurera direkt `PdfOptions` innan du anropar `image.Save(...)`.

**Q: Kan jag ändra textfärgen programatiskt?**  
A: Ja, sätt `cadText.ColorId` till ett specifikt ACI‑färgsnummer (t.ex. 1 för röd).

**Q: Är det möjligt att infoga flerradig text?**  
A: Använd `CadMText` för flerradiga textblock; tillvägagångssättet är liknande `CadText`.

**Q: Stöder Aspose.CAD batch‑konvertering av flera DWG‑filer?**  
A: Absolut – loopa igenom en katalog med DWG‑filer, tillämpa samma steg och spara varje som PDF.

## Slutsats

Du har nu ett komplett, produktionsklart arbetsflöde för att **konvertera DWG till PDF**, **lägga till anpassad text** och **anpassa textens utseende** med C# och Aspose.CAD. Denna teknik är idealisk för automatiserad ritningsgenerering, rapporteringspipelines eller alla scenarier där du behöver berika CAD‑filer i realtid.

---

**Senast uppdaterad:** 2026-04-06  
**Testad med:** Aspose.CAD 24.11 for .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}