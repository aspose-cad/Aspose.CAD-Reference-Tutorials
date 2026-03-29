---
date: 2026-03-29
description: Lär dig hur du konverterar DGN till JPEG med Aspose.CAD för .NET, som
  ger fullt stöd för DGN V7 och gör det enkelt att konvertera CAD till rasterbilder.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DGN till JPEG med Aspose.CAD för .NET – V7‑stöd
url: /sv/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DGN till JPEG med Aspose.CAD för .NET – V7-stöd

## Introduktion

I den här handledningen kommer du att lära dig hur du **konverterar DGN till JPEG** med Aspose.CAD för .NET, och utnyttjar bibliotekets fullständiga DGN V7-stöd. Att konvertera DGN-filer till rasterbilder såsom JPEG är ett vanligt krav när du behöver bädda in CAD-ritningar i webbsidor, mobilappar eller rapporteringsverktyg. Aspose.CAD låter dig också **konvertera CAD till raster**-format effektivt, vilket ger dig flexibilitet i hur du presenterar designdata.

## Snabba svar
- **Vad täcker handledningen?** Konvertera en DGN V7-fil till en JPEG-rasterbild med Aspose.CAD för .NET.  
- **Vilken biblioteksversion krävs?** Alla nyligen släppta Aspose.CAD för .NET-versioner som inkluderar DGN V7-stöd.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Kan jag ändra utdata storlek?** Ja – rasteriseringsalternativ låter dig ange sidbredd, höjd och skalning.  
- **Är JPEG det enda utdataformatet?** Nej – Aspose.CAD stödjer många rasterformat (PNG, BMP, TIFF, etc.).

## Vad är DGN V7?
DGN (Design) är ett filformat som ursprungligen skapades av Bentley Systems för MicroStation. Version 7 lägger till rikare geometri och metadata, vilket gör det till ett populärt val för civil‑ingenjörs- och infrastrukturprojekt. Aspose.CAD för .NET kan läsa DGN V7-filer direkt och exponera deras innehåll som `CadImage`‑objekt som du kan rasterisera eller konvertera till andra format.

## Varför konvertera DGN till JPEG?
- **Web‑klar:** JPEG‑bilder är lätta och visas omedelbart i webbläsare utan att kräva speciella tillägg.  
- **Plattformsoberoende:** JPEG kan visas på vilken enhet som helst, vilket gör det idealiskt för att dela CAD-ritningar med icke‑tekniska intressenter.  
- **Förenklade arbetsflöden:** Att konvertera till ett rasterformat eliminerar behovet av CAD‑specifika visare i efterföljande processer.

## Förutsättningar

Innan vi dyker in i implementeringen, se till att du har följande:

- **Aspose.CAD för .NET** – ladda ner det från [webbplatsen](https://releases.aspose.com/cad/net/).  
- **Utvecklingsmiljö** – Visual Studio (eller någon IDE som stödjer .NET).  

Att ha dessa redo gör att du kan följa stegen utan avbrott.

## Importera namnrymder

Börja med att importera namnrymderna som krävs för CadImage‑hantering och rasterisering.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda DGN‑filen

Läs in käll‑DGN‑filen i ett `CadImage`‑objekt. Ersätt platshållar‑sökvägen med mappen som innehåller din DGN‑fil.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Steg 2: Konfigurera rasteriseringsalternativ

Definiera hur DGN‑ritningen ska rasteriseras. Du kan kontrollera utdata‑dimensioner och skalningsbeteende.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Steg 3: Ställ in vektor‑rasteriseringsalternativ

Skapa ett `JpegOptions`‑objekt (eller någon annan rasterformat‑alternativ) och fäst rasteriseringsinställningarna.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Steg 4: Spara den rasteriserade bilden

Slutligen, exportera DGN‑ritningen till en JPEG‑fil med hjälp av `Save`‑metoden.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

När koden körs framgångsrikt kommer du att hitta en JPEG‑representation av den ursprungliga DGN V7‑ritningen i den angivna mappen.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Filen hittades inte** | Verifiera att `MyDir` slutar med en sökvägsavgränsare (`\\` eller `/`) och att filnamnet är korrekt. |
| **Tom bild** | Se till att `NoScaling` är korrekt inställt; sätt den till `false` om du vill att ritningen fyller sidan. |
| **Ej stödda enheter** | Aspose.CAD stödjer de flesta DGN‑enheter, men mycket gamla eller anpassade objekt kan ignoreras. Kontrollera konverteringsloggen för varningar. |

## Vanliga frågor

### Q1: Är Aspose.CAD kompatibel med de senaste DGN V7-specifikationerna?
**A:** Ja, Aspose.CAD stödjer fullt ut DGN V7 och hanterar både geometri och metadata enligt de senaste standarderna.

### Q2: Kan jag anpassa rasteriseringsalternativen för DGN‑filkonvertering?
**A:** Absolut. Klassen `CadRasterizationOptions` låter dig justera sidstorlek, skalning, linjebredd, bakgrundsfärg och mer.

### Q3: Finns det andra stödjade utdataformat förutom JPEG?
**A:** Ja, Aspose.CAD kan exportera till PNG, BMP, TIFF och flera andra rasterformat. Använd helt enkelt motsvarande `*Options`‑klass (t.ex. `PngOptions`).

### Q4: Hur kan jag få hjälp med frågor relaterade till Aspose.CAD?
**A:** Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för community‑stöd och officiella svar.

### Q5: Finns det en gratis provversion av Aspose.CAD för .NET?
**A:** Ja, du kan ladda ner en provversion från [här](https://releases.aspose.com/).

---

**Senast uppdaterad:** 2026-03-29  
**Testat med:** Aspose.CAD 24.12 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}