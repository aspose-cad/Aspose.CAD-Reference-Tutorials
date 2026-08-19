---
date: 2026-03-21
description: Leer hoe u PDF maakt van DWG en DGN exporteert als onderdeel van DWG
  met Aspose.CAD voor .NET. Deze gids laat ook zien hoe u DWG naar PDF converteert
  en PDF‑opties instelt.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF maken van DWG en DGN exporteren als onderdeel van DWG – Aspose.CAD voor
  .NET
url: /nl/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak PDF van DWG en Exporteer DGN als onderdeel van DWG – Aspose.CAD voor .NET

## Inleiding

Als je **PDF wilt maken van DWG**‑bestanden en tegelijkertijd een DGN‑ontwerp als onderdeel van de DWG wilt insluiten, maakt Aspose.CAD voor .NET dit eenvoudig. In deze tutorial lopen we het volledige werkproces door: een DWG laden, de ingesloten DGN‑underlay vinden, rasterisatie‑opties configureren en uiteindelijk het resultaat exporteren naar een PDF‑document. Of je nu een batch‑conversietool, een rapportage‑engine of een CAD‑BIM‑integratieservice bouwt, de onderstaande stappen geven je een solide, productie‑klare basis.

## Snelle antwoorden
- **Welke bibliotheek verwerkt DWG → PDF-conversie?** Aspose.CAD voor .NET  
- **Kan ik een DGN‑underlay exporteren tijdens het maken van de PDF?** Ja – de underlay wordt benaderd via `CadDgnUnderlay`.  
- **Welke methode stelt PDF‑opties in?** `PdfOptions` samen met `CadRasterizationOptions`.  
- **Heb ik een licentie nodig voor commercieel gebruik?** Ja, een geldige Aspose.CAD‑licentie is vereist.  
- **Ondersteunde .NET‑versies?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Wat betekent “PDF maken van DWG”?

Een PDF maken van een DWG‑bestand houdt in dat de vectortekening wordt gerenderd naar een raster‑ of vector‑gebaseerd PDF‑document. Dit proces is nuttig voor het delen van tekeningen met belanghebbenden die geen CAD‑software hebben, voor archivering of voor het genereren van afdrukbare rapporten. Aspose.CAD vereenvoudigt de taak door het zware werk van het parseren van DWG‑entiteiten af te handelen en biedt fijne controle over de output via `PdfOptions`.

## Waarom DGN exporteren als onderdeel van een DWG?

Een DGN‑underlay vertegenwoordigt vaak referentie‑geometrie uit MicroStation‑projecten. Door de DGN samen met de DWG te exporteren behoud je de oorspronkelijke ontwerp‑context, zodat downstream‑gebruikers de volledige tekeningsset zien. Dit is vooral waardevol in multidisciplinaire projecten waar zowel DWG‑ als DGN‑bestanden naast elkaar bestaan.

## Vereisten

- **Aspose.CAD voor .NET** – download het [hier](https://releases.aspose.com/cad/net/).  
- **Ontwikkelomgeving** – Visual Studio (een recente versie) of je favoriete .NET‑IDE.  
- **Basiskennis van C#** – je moet vertrouwd zijn met C#‑syntaxis en .NET‑projectstructuur.

## Namespaces importeren

Voeg de benodigde `using`‑directieven toe aan de bovenkant van je C#‑bronbestand:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stapsgewijze handleiding

### Stap 1: Bestands‑paden definiëren

Stel het invoer‑DWG‑bestand en de naam van de uitvoer‑PDF in.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Stap 2: `PdfOptions`‑instantie maken (pdf‑opties instellen)

`PdfOptions` laat je bepalen hoe de PDF wordt gegenereerd, zoals paginagrootte, compressie en metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Stap 3: Het DWG‑bestand laden

Laad de DWG als een `CadImage` zodat je de entiteiten kunt inspecteren.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Stap 4: Door entiteiten itereren

Loop door elke entiteit in de tekening om de DGN‑underlay te vinden.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Stap 5: Entiteitstype controleren (hoe DGN exporteren)

Identificeer of de huidige entiteit een DGN‑underlay is.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Stap 6: Underlay‑pad ophalen

Haal het pad van de externe referentie van het DGN‑bestand op.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Stap 7: Rasterisatie‑opties definiëren (dwg naar pdf converteren)

Configureer hoe de DWG wordt gerasterd voordat deze in de PDF wordt geplaatst.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Stap 8: DWG naar PDF exporteren

Sla tenslotte het gerenderde beeld op als een PDF‑bestand.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **`Image.Load` geeft “File not found”** | Onjuist pad of ontbrekend bestand. | Gebruik een absoluut pad of zorg dat de DWG naar de output‑map wordt gekopieerd. |
| **Underlay‑pad is leeg** | DGN‑underlay niet ingesloten of referentie verbroken. | Controleer of de DWG daadwerkelijk een DGN‑underlay bevat en of het externe DGN‑bestand toegankelijk is. |
| **PDF‑output is leeg** | Rasterisatie‑opties ingesteld op nulgrootte. | Pas `PageWidth`/`PageHeight` aan of stel `NoScaling = false` in. |
| **Licentie‑exception** | Er wordt geen geldige Aspose.CAD‑licentie gebruikt. | Pas de licentie toe vóór het laden van de afbeelding: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD voor .NET gebruiken in mijn commerciële projecten?
A1: Ja, dat kan. Bezoek [hier](https://purchase.aspose.com/buy) voor licentie‑opties.

### Q2: Zijn er beperkingen qua grootte van DWG‑bestanden die ik kan verwerken?
A2: Aspose.CAD ondersteunt het verwerken van grote DWG‑bestanden, maar hardware‑beperkingen kunnen van toepassing zijn.

### Q3: Is er een proefversie beschikbaar?
A3: Ja, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q4: Hoe kan ik tijdelijke licenties verkrijgen?
A4: Tijdelijke licenties zijn beschikbaar [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Waar kan ik hulp zoeken als ik tegen problemen aanloop?
A5: Bezoek het Aspose.CAD‑forum [hier](https://forum.aspose.com/c/cad/19) voor ondersteuning.

**Q: Hoe stel ik extra PDF‑metadata in (auteur, titel, enz.)?**  
A: Gebruik de `exportOptions.Metadata`‑eigenschappen vóór het aanroepen van `Save`.

**Q: Kan ik meerdere layouts exporteren naar afzonderlijke PDF‑pagina’s?**  
A: Ja – stel `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**Q: Ondersteunt Aspose.CAD het converteren van DWG naar andere beeldformaten?**  
A: Absoluut. Je kunt exporteren naar PNG, JPEG, SVG en meer door de overeenkomstige `Image.Save`‑overloads te gebruiken.

---

**Laatst bijgewerkt:** 2026-03-21  
**Getest met:** Aspose.CAD 24.11 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}