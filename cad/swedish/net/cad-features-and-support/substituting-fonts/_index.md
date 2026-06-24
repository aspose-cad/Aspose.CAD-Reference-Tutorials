---
date: 2026-03-29
description: Lär dig hur du snabbt ersätter teckensnitt i Aspose.CAD för .NET. Denna
  steg‑för‑steg‑guide visar dig hur du ställer in primärt teckensnittsnamn och anpassar
  CAD-ritningar effektivt.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man ersätter teckensnitt i Aspose.CAD för .NET
url: /sv/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ersätter teckensnitt i Aspose.CAD för .NET

## Introduktion

I CAD‑utveckling med .NET är **kunskapen om hur man ersätter teckensnitt** en viktig färdighet som kan förbättra den visuella kvaliteten på dina ritningar avsevärt. Aspose.CAD för .NET erbjuder ett enkelt API som låter dig **ange primärt teckensnittsnamn** för vilken stil som helst, vilket gör global eller selektiv teckensnittsbyte enkelt. I den här handledningen går vi igenom hela processen – från att ladda en ritning till att byta teckensnitt antingen globalt eller efter specifikt stilnamn.

## Snabba svar
- **Vad är huvudklassen för CAD-manipulation?** `Aspose.CAD.Image` (eller dess avledda `CadImage`).
- **Vilken egenskap ändrar teckensnittet?** `PrimaryFontName` på `CadStyleTableObject`.
- **Kan jag ersätta teckensnitt för alla stilar på en gång?** Ja, iterera genom `cadImage.Styles` och sätt egenskapen.
- **Behöver jag en licens för produktion?** En giltig Aspose.CAD‑licens krävs för icke‑testanvändning.
- **Stödda .NET‑versioner?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Vad är teckensnittssubstitution i CAD?
Teckensnittssubstitution innebär att ersätta det ursprungliga typsnittet som används i en CAD‑ritning med ett annat som finns tillgängligt på mål‑systemet. Detta är särskilt användbart när det ursprungliga teckensnittet saknas, när du behöver en enhetlig företagsstil, eller när du förbereder ritningar för utskrift på enheter som bara stöder ett begränsat urval av teckensnitt.

## Varför ersätta teckensnitt med Aspose.CAD?
- **Inga externa beroenden** – biblioteket hanterar teckensnittsmappning internt.
- **Fungerar med många format** – DXF, DWG, DGN och fler.
- **Programmerbar kontroll** – automatisera processen för batch‑konverteringar eller CI‑pipelines.
- **Bevarar ritningsgeometri** – endast den visuella representationen av text ändras.

## Förutsättningar

- Grundläggande kunskap om .NET‑programmering.
- Aspose.CAD för .NET installerat. Om du ännu inte har installerat det, ladda ner det [here](https://releases.aspose.com/cad/net/).
- En CAD‑ritningsfil (DXF, DWG, etc.) att experimentera med.

## Importera namnrymder

Innan du börjar, importera de nödvändiga namnrymderna för att få åtkomst till Aspose.CAD‑funktionaliteten i din .NET‑applikation.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Steg 1: Ladda CAD-ritning

Börja med att ladda CAD‑ritningen i en instans av `CadImage`. Se till att du anger rätt sökväg till din dokumentkatalog.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Steg 2: Iterera över stilar

Iterera sedan över stilarna i CAD‑ritningen med en `foreach`‑loop. Detta låter dig komma åt och manipulera enskilda teckensnittsstilar.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Hur man anger primärt teckensnittsnamn för teckensnittssubstitution

`PrimaryFontName`‑egenskapen på varje `CadStyleTableObject` styr vilket teckensnitt som används när ritningen renderas. Genom att sätta denna egenskap ersätter du effektivt det ursprungliga teckensnittet.

### Steg 3: Ersätt teckensnitt globalt

För att ersätta teckensnitt för **alla** stilar, sätt `PrimaryFontName`‑egenskapen för varje stil till önskat teckensnittsnamn, till exempel `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Steg 4: Ersätt teckensnitt efter stilnamn

Om du bara behöver ersätta teckensnittet för en specifik stil (t.ex. stilen med namnet `"Roman"`), lägg till en villkorskontroll inuti loopen.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Vanliga problem och felsökning

| Problem | Orsak | Lösning |
|-------|-------|-----|
| Teckensnittet ändras inte efter att koden körts | Ritningen är cachad eller öppnad i skrivskyddat läge | Se till att du sparar bilden efter ändring (`cadImage.Save(...)`) eller läser in filen på nytt för att verifiera. |
| Önskat teckensnitt finns inte på systemet | Teckensnittet är inte installerat på maskinen som kör koden | Installera det nödvändiga TrueType/OpenType‑teckensnittet eller bädda in det i applikationens resurser. |
| Texten visas förvrängd | Fel kodning eller saknar Unicode‑stöd | Använd ett teckensnitt som stödjer den erforderliga teckenuppsättningen (t.ex. Arial Unicode MS). |

## Vanliga frågor

**Q: Kan jag återställa teckensnittsändringar i Aspose.CAD för .NET?**  
A: Ja, du kan återställa genom att ladda om den ursprungliga CAD‑ritningen eller genom att behålla en backup‑kopia innan du gör ändringar.

**Q: Finns det andra teckensnittsegenskaper jag kan ändra?**  
A: Absolut. Förutom `PrimaryFontName` kan du arbeta med `SecondaryFontName`, `FontFamily` och andra stilrelaterade attribut för avancerad anpassning.

**Q: Är Aspose.CAD kompatibel med olika CAD‑format?**  
A: Ja, Aspose.CAD stödjer ett brett sortiment av format såsom DXF, DWG, DGN, DWF och fler, vilket ger dig flexibilitet över projekt.

**Q: Kan jag automatisera teckensnittssubstitution i batchbearbetning?**  
A: Självklart. Packa in laddnings‑ och substitutionslogiken i en loop som itererar över en mapp med CAD‑filer, eller integrera den i en CI/CD‑pipeline.

**Q: Var kan jag hitta ytterligare support för Aspose.CAD för .NET?**  
A: För ytterligare support och community‑diskussioner, besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD for .NET (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}