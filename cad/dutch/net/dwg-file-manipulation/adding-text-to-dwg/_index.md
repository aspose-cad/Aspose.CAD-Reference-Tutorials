---
date: 2026-04-06
description: Leer hoe je DWG naar PDF kunt converteren en aangepaste tekst kunt toevoegen
  met C# en Aspose.CAD. Deze stapsgewijze handleiding behandelt het genereren van
  PDF vanuit DWG, het invoegen van een textelement en het wijzigen van het DWG-tekstlettertype.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Tekst toevoegen aan DWG-bestanden in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG converteren naar PDF en tekst toevoegen in C# – Aspose.CAD‑handleiding
url: /nl/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG naar PDF converteren en tekst toevoegen in C# – Aspose.CAD Tutorial

## Inleiding

In de snel veranderende wereld van CAD- en .NET-ontwikkeling is **DWG naar PDF converteren** terwijl je aangepaste annotaties invoegt een veelvoorkomende eis. Of je nu afdrukbare tekeningen voor klanten moet genereren of dynamische notities direct in een DWG wilt insluiten, Aspose.CAD maakt het werk eenvoudig. In deze tutorial leer je hoe je **DWG naar PDF kunt converteren**, **een textelement kunt toevoegen**, en zelfs **het DWG-tekstlettertype kunt wijzigen** met C#.

## Snelle antwoorden
- **Welke bibliotheek is het beste voor DWG‑naar‑PDF conversie?** Aspose.CAD voor .NET  
- **Kan ik aangepaste tekst toevoegen tijdens het converteren?** Ja – maak een `CadText`-entity aan en voeg deze toe vóór het opslaan.  
- **Heb ik een licentie nodig voor productiegebruik?** Een commerciële licentie is vereist; een gratis proefversie is beschikbaar.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Is het mogelijk om het tekstlettertype te wijzigen?** Ja, pas de `CadText`-eigenschappen aan, zoals `StyleType` en `TextHeight`.

## Wat is “DWG naar PDF converteren”?

Een DWG‑bestand naar PDF converteren verandert een vector‑gebaseerde CAD-tekening in een breed deelbaar, apparaat‑onafhankelijk document. De PDF behoudt de oorspronkelijke geometrie en lagen, terwijl je annotaties, tekst of andere metadata kunt insluiten. Aspose.CAD verwerkt de rasterisatie en vectorweergave automatisch, zodat je geen externe CAD‑software op de server nodig hebt.

## Waarom tekst toevoegen aan een DWG vóór conversie?

Tekst direct in de DWG insluiten geeft je volledige controle over plaatsing, opmaak en laagtoewijzing. Wanneer het bestand later naar PDF wordt geconverteerd, verschijnt de tekst precies op de positie die je hebt ingesteld, waardoor het ontwerpintentie behouden blijft en nabewerking in een PDF‑editor overbodig wordt.

## Voorvereisten

- **Aspose.CAD Library** – download deze via de [download link](https://releases.aspose.com/cad/net/).  
- **Een werkende .NET-omgeving** (Visual Studio 2022, .NET 6, of een andere compatibele versie).  
- **Een map voor je testbestanden** – we zullen er gedurende de gids naar verwijzen als `MyDir`.

Laten we nu stap voor stap het proces doorlopen.

## Namespaces importeren

Voeg de benodigde `using`-statements toe zodat je toegang hebt tot de Aspose.CAD‑klassen.

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

## Stap 1: Laad het DWG‑bestand

Laad je bron‑DWG‑bestand in een `Image`‑object. Dit object geeft je toegang tot de onderliggende CAD‑entiteiten.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Stap 2: Maak een CadText‑object (Tekstelement invoegen)

De `CadText`‑klasse vertegenwoordigt een enkele regel tekst in een DWG. Hier stellen we de stijl, waarde, kleur, laag en positie in. Pas `StyleType` of `TextHeight` aan om **het DWG‑tekstlettertype te wijzigen**.

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

## Stap 3: Voeg het textelement toe aan de Model Space

De DWG‑modelruimte bevat de meeste tekenelementen. Door onze `CadText` toe te voegen aan het `*Model_Space`‑blok, wordt de tekst onderdeel van de tekening.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Stap 4: PDF‑opties configureren (PDF genereren vanuit DWG)

Stel rasterisatie‑opties in die bepalen hoe de DWG wordt gerenderd naar een PDF. Je kunt paginagrootte, teken‑type en lay‑out aanpassen.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Stap 5: Sla de gewijzigde DWG op als PDF

Exporteer tenslotte de gewijzigde tekening. De resulterende PDF bevat de nieuw ingevoegde tekst.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro tip:** Als je een PDF met hogere resolutie nodig hebt, verhoog dan `PageHeight` en `PageWidth` proportioneel.

## Veelvoorkomende problemen & oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| Tekst verschijnt niet in de PDF | Verkeerde laag of kleur‑ID | Zorg ervoor dat `LayerName` bestaat en `ColorId` is ingesteld op een zichtbare kleur (bijv. 7 voor wit). |
| Tekst staat op de verkeerde plaats | Onjuiste uitlijningscoördinaten | Controleer de waarden van `FirstAlignment.X/Y` ten opzichte van de eenheden van de tekening. |
| PDF is leeg | Rasterisatie‑opties niet ingesteld | Stel `DrawType` in op `UseObjectColor` of `UseObjectLineWeight`. |

## Veelgestelde vragen (bestaand)

### Q1: Is Aspose.CAD compatibel met alle versies van DWG‑bestanden?

A1: Aspose.CAD ondersteunt een breed scala aan DWG‑bestandversies, waardoor compatibiliteit met diverse CAD‑software gegarandeerd is.

### Q2: Kan ik meerdere textelementen toevoegen aan één DWG‑bestand met Aspose.CAD?

A2: Ja, je kunt meerdere textelementen toevoegen aan een DWG‑bestand door het proces uit de tutorial te herhalen.

### Q3: Hoe kan ik het tekstlettertype en de stijl wijzigen in Aspose.CAD?

A3: Om het tekstlettertype en de stijl te wijzigen, pas je de eigenschappen van het `CadText`‑object aan voordat je het aan het DWG‑bestand toevoegt.

### Q4: Zijn er licentie‑overwegingen bij het gebruik van Aspose.CAD in een commercieel project?

A5: Ja, zorg voor naleving van de licentievoorwaarden van Aspose.CAD. Zie [Aspose.CAD Purchase](https://purchase.aspose.com/buy) voor details.

### Q5: Waar kan ik hulp zoeken of discussiëren over Aspose.CAD‑gerelateerde vragen?

A5: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) om contact te maken met de community en ondersteuning te krijgen.

## Aanvullende veelgestelde vragen

**Q: Hoe genereer ik een PDF vanuit DWG zonder tekst toe te voegen?**  
A: Sla de stap van het maken van `CadText` over en configureer direct `PdfOptions` voordat je `image.Save(...)` aanroept.

**Q: Kan ik de tekstkleur programmatically wijzigen?**  
A: Ja, stel `cadText.ColorId` in op een specifiek ACI‑kleurnummer (bijv. 1 voor rood).

**Q: Is het mogelijk om meerregelige tekst in te voegen?**  
A: Gebruik `CadMText` voor meerregelige tekstblokken; de aanpak is vergelijkbaar met `CadText`.

**Q: Ondersteunt Aspose.CAD batch‑conversie van meerdere DWG‑bestanden?**  
A: Zeker – loop door een map met DWG‑bestanden, pas dezelfde stappen toe en sla elk op als PDF.

## Conclusie

Je hebt nu een volledige, productie‑klare workflow om **DWG naar PDF te converteren**, **aangepaste tekst toe te voegen**, en **de weergave van tekst aan te passen** met C# en Aspose.CAD. Deze techniek is ideaal voor geautomatiseerde tekeningsgeneratie, rapportage‑pijplijnen, of elke situatie waarin je CAD‑bestanden direct wilt verrijken.

---

**Laatste update:** 2026-04-06  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}