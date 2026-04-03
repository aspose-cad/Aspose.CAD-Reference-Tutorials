---
date: 2026-04-03
description: Leer hoe je een viewport instelt en DWG naar PDF converteert in C# met
  behulp van Aspose.CAD. Deze DWG-naar-PDF‑tutorial toont een nauwkeurige export met
  coördinaten.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: DWG converteren naar PDF met coördinaten in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hoe een viewport instellen bij het converteren van DWG naar PDF met coördinaten
  in C# - Aspose.CAD‑tutorial
url: /nl/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG naar PDF converteren met coördinaten in C# - Aspose.CAD Tutorial

## Introductie

Welkom bij deze uitgebreide tutorial over **how to set viewport** tijdens het converteren van DWG‑bestanden naar PDF met gespecificeerde coördinaten met behulp van Aspose.CAD voor .NET. Door de viewport te regelen krijg je pixel‑perfecte PDF's die precies overeenkomen met het gebied dat je nodig hebt—perfect voor constructietekeningen, plattegrond‑voorbeelden, of elke BIM‑workflow.

## Snelle antwoorden
- **What does “set viewport” mean?** Het definieert het zichtbare gebied en de schaal van de CAD-tekening tijdens rasterisatie.  
- **Which library handles the conversion?** Aspose.CAD for .NET.  
- **Do I need a license?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie.  
- **Supported platforms?** Windows, Linux en macOS met .NET 5/6/7 of .NET Framework 4.6+.  
- **Typical implementation time?** Ongeveer 10‑15 minuten voor een basisconversie.

## Voorvereisten

Voordat we beginnen, zorg ervoor dat je de volgende voorwaarden hebt:

- **Aspose.CAD Library** – Download en installeer de Aspose.CAD‑bibliotheek voor .NET. Je kunt de bibliotheek [hier](https://releases.aspose.com/cad/net/) vinden.  
- **Development Environment** – Visual Studio, Rider of elke IDE die .NET‑ontwikkeling ondersteunt.  
- **DWG File** – Zorg voor een DWG‑bestand klaar voor conversie. Je kunt het meegeleverde voorbeeldbestand gebruiken of je eigen DWG‑bestand.

## Hoe viewport in te stellen voor precieze PDF-export

Het instellen van de viewport is de kernstap waarmee je het exacte gebied van de tekening kunt definiëren dat je wilt renderen. In de onderstaande code maken we een nieuw `CadVportTableObject`, positioneren het met de linkerboven‑coördinaat en berekenen breedte, hoogte en beeldverhouding. Dit is de **how to set viewport**‑implementatie die de rest van de conversie aandrijft.

## Namespaces importeren

In je C#‑project importeer je de benodigde namespaces:

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

Laten we de code stap voor stap ontleden voor een beter begrip:

## Stap 1: Definieer de documentmap

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Stel het bron‑DWG‑bestandspad in

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Stap 3: Laad DWG‑bestand en configureer rasterisatie‑opties

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Stap 4: Definieer coördinaten en viewport  

Hier **set the viewport** (how to set viewport) we echt door de linkerboven‑hoek, breedte en hoogte van het gebied dat je wilt exporteren op te geven.

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

## Stap 5: Pas viewport‑instellingen toe

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

## Stap 6: Configureer PDF‑opties en exporteer  

Nu koppelen we alles samen en **convert DWG to PDF** met behulp van de rasterisatie‑opties die we zojuist hebben voorbereid.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Stap 7: Toon succesbericht

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Veelvoorkomende gebruikssituaties

- **Construction documentation** – Genereer afdrukbare PDF's van specifieke plattegrond‑secties.  
- **BIM coordination** – Exporteer alleen het interessegebied voor clash‑detectie.  
- **Client presentations** – Bied een nette PDF van een geselecteerde kamer of elevatie zonder de volledige tekening bloot te stellen.

## Conclusie

Gefeliciteerd! Je hebt succesvol **converted DWG to PDF** met precieze coördinaten en geleerd **how to set viewport** te gebruiken met Aspose.CAD voor .NET. Deze **dwg to pdf tutorial** toont hoe je **create pdf from dwg** en **export dwg as pdf c#** kunt maken terwijl je volledige controle behoudt over het uitvoergebied.

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD gebruiken met andere CAD‑bestandsformaten?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD‑formaten, waaronder DWG, DXF, DWF en meer.

### Q2: Hoe kan ik fouten afhandelen tijdens het conversieproces?

A2: Implementeer foutafhandelingsmechanismen met try‑catch‑blokken om uitzonderingen te vangen en te beheren.

### Q3: Is Aspose.CAD geschikt voor zowel Windows- als Linux‑omgevingen?

A3: Ja, Aspose.CAD is compatibel met zowel Windows‑ als Linux‑platforms.

### Q4: Kan ik de PDF‑output verder aanpassen?

A4: Zeker! Verken de uitgebreide opties die Aspose.CAD biedt om de PDF‑output af te stemmen op jouw specifieke eisen.

### Q5: Waar kan ik extra ondersteuning of community‑discussies vinden?

A5: Bezoek het [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

## Aanvullende veelgestelde vragen

**Q: Werkt deze aanpak met grote DWG‑bestanden (honderden MB)?**  
**A:** Ja. De rasterisatie wordt pagina voor pagina uitgevoerd, en je kunt `rasterizationOptions` (bijv. `Resolution`) aanpassen om kwaliteit en geheugenverbruik in balans te brengen.

**Q: Kan ik meerdere viewports exporteren naar afzonderlijke PDF‑pagina's?**  
**A:** Je kunt door `cadImage.ViewPorts` itereren, elk als actief instellen en `Save` aanroepen voor elke pagina, vervolgens de PDF's samenvoegen met Aspose.PDF.

**Q: Is het mogelijk een watermerk toe te voegen aan de gegenereerde PDF?**  
**A:** Na het opslaan van de PDF kun je deze opnieuw openen met Aspose.PDF en een tekst‑ of afbeelding‑watermerk toepassen voordat je deze aan de gebruiker levert.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}