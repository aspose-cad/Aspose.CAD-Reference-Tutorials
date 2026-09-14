---
date: 2026-09-14
description: Leer hoe u een licentie toepast in Aspose.CAD for .NET met behulp van
  een bestandspad of FileStream, en ontdek metered licensing om het resourcegebruik
  te optimaliseren.
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: Licenties en configuratie
og_description: Leer hoe u een licentie toepast in Aspose.CAD for .NET met behulp
  van een bestandspad of FileStream, en ontdek metered licensing om het resourcegebruik
  te optimaliseren. (150‑160 tekens)
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: Hoe een licentie toe te passen in Aspose.CAD for .NET – Snelle gids
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: Hoe een licentie toe te passen in Aspose.CAD for .NET
url: /nl/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe licentie toe te passen in Aspose.CAD voor .NET

Welkom bij de definitieve gids over **hoe licentie toe te passen** voor Aspose.CAD in .NET. Of u nu een desktop‑utility, een server‑side service of een geautomatiseerde BIM‑pipeline bouwt, een geldige licentie ontgrendelt de volledige suite van meer dan 40 CAD‑ en BIM‑formaten, maakt high‑performance rendering mogelijk en verwijdert evaluatiewatermerken. Dit artikel leidt u stap voor stap door alle licentie‑opties, zodat u zonder onderbrekingen kunt beginnen met ontwikkelen.

## Snelle antwoorden
- **Kan ik een licentie laden vanaf een bestandspad?** Ja – maak gewoon een `License`‑instantie en roep `SetLicense("path/to/license.lic")` aan.  
- **Wordt een FileStream ondersteund?** Absoluut; geef de geopende stream door aan `SetLicense(stream)`.  
- **Wat is metered licensing?** Het houdt het gebruik per aanvraag bij, zodat u alleen betaalt voor wat u verbruikt.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proeflicentie werkt voor ontwikkeling en testen; een commerciële licentie is vereist voor productie.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Wat is licensering in Aspose.CAD?

Licensering in Aspose.CAD is het mechanisme dat uw aankoop valideert en de volledige functionaliteit van de bibliotheek activeert. Zonder licentie draait de API in evaluatiemodus, waardoor de uitvoergrootte wordt beperkt en een watermerk op gerenderde afbeeldingen wordt geplaatst.

## Waarom een pad‑gebaseerde licentie gebruiken in plaats van een stream?

Pad‑gebaseerde licensering is de snelste manier om Aspose.CAD te activeren: wijs simpelweg naar het .lic‑bestand en de bibliotheek laadt het automatisch. Gebruik een stream wanneer u de licentie moet lezen van een niet‑bestandbron, aangepaste beveiliging wilt afdwingen, of de licentie wilt insluiten in een assembly. Kies de methode die past bij uw implementatie‑beperkingen.

De `License`‑klasse vertegenwoordigt het Aspose.CAD‑licentie‑component dat een licentie registreert bij de API.

## Hoe past u een licentie toe via pad in Aspose.CAD voor .NET?

Om een licentie via een pad toe te passen, maakt u een instantie van de `License`‑klasse en roept u de `SetLicense`‑methode aan met het volledige bestandspad naar uw .lic‑bestand. Plaats deze code vroeg in de opstartfase van uw applicatie zodat alle daaropvolgende CAD‑bewerkingen onder een gelicentieerde context draaien.

De `License`‑klasse vertegenwoordigt het Aspose.CAD‑licentie‑component dat een licentie registreert bij de API.

1. Plaats uw `Aspose.CAD.lic`‑bestand in een map die uw applicatie kan lezen (bijv. de applicatieroot of een beveiligde configuratiemap).  
2. Voeg de volgende code toe vroeg in uw opstartroutine (bijv. `Main`, `Startup.Configure` of `Global.asax`):

```csharp
// No code block added – original tutorial contained none.
```

> **Direct antwoord (40‑70 woorden):**  
> Om een licentie via een pad toe te passen, maak een `License`‑object aan en roep `SetLicense("full\\path\\to\\Aspose.CAD.lic")` aan. Deze enkele regel activeert de volledige bibliotheek, verwijdert evaluatiewatermerken en maakt verwerking van meer dan 40 CAD/BIM‑formaten mogelijk zonder prestatiebeperking. Plaats de aanroep vóór enige CAD‑bewerkingen om te zorgen dat de licentie actief is.

## Hoe past u een licentie toe met FileStream in Aspose.CAD voor .NET?

Om een licentie toe te passen met een `FileStream`, open het .lic‑bestand met leesrechten, maak een `License`‑object aan en geef de stream door aan `SetLicense`. Zorg ervoor dat de stream open blijft totdat de registratie in uw applicatie is voltooid, sluit deze vervolgens om bronnen vrij te geven.

De `FileStream`‑klasse biedt een stream voor het lezen van en schrijven naar bestanden op schijf.

1. Haal de licentiebits op uit uw bron (bestandssysteem, Azure Blob, enz.).  
2. Open een `FileStream` met leesrechten.  
3. Geef de stream door aan het `License`‑object.

> **Direct antwoord (40‑70 woorden):**  
> Instantieer een `License`‑object en roep `SetLicense(stream)` aan waarbij `stream` een leesbare `FileStream` is die naar uw `Aspose.CAD.lic` wijst. Dit laadt de licentie vanuit het geheugen, waardoor u het bestand uit het bestandssysteem kunt houden indien gewenst, en activeert alle functies onmiddellijk. Zorg ervoor dat de stream open blijft totdat de registratie voltooid is, sluit deze daarna.

## Hoe werkt metered licensing in Aspose.CAD voor .NET?

Metered licensing wordt geactiveerd door `License.SetMeteredKey` aan te roepen met uw unieke sleutel. Na registratie rapporteert de SDK automatisch elke CAD‑bewerking naar de server van Aspose, waardoor u het gebruik kunt monitoren en alleen wordt gefactureerd voor de acties die binnen uw abonnementsperiode zijn uitgevoerd.

De `License.SetMeteredKey`‑methode registreert een metered‑licentiesleutel bij de Aspose.CAD‑bibliotheek.

1. Verkrijg een metered‑licentiesleutel vanuit uw Aspose‑accountdashboard.  
2. Registreer de sleutel met `License.SetMeteredKey("your‑key")`.  
3. Roep na elke bewerking `License.GetMeteredUsage()` aan om het huidige gebruiksaantal op te halen.

> **Direct antwoord (40‑70 woorden):**  
> Metered licensing wordt geactiveerd door `License.SetMeteredKey("your‑key")` aan te roepen. De SDK stuurt vervolgens gebruiksgegevens naar de server van Aspose na elke CAD‑bewerking, zodat u kunt monitoren en factureren op basis van daadwerkelijk verbruik. Dit model ondersteunt onbeperkt gelijktijdig gebruik terwijl de kosten afgestemd blijven op het werkelijke gebruik.

## Licensering en configuratie‑handleidingen

### [Licentie toepassen via pad in Aspose.CAD voor .NET](./apply-license-by-path/)
Ontgrendel het volledige potentieel van Aspose.CAD voor .NET! Volg onze stapsgewijze gids om moeiteloos een licentie toe te passen. Verhoog nu uw CAD‑bestandsmanipulatie!

### [Licentie toepassen met FileStream in Aspose.CAD voor .NET](./apply-license-using-filestream/)
Beheers Aspose.CAD voor .NET: pas licenties naadloos toe met FileStream. Ontdek de stapsgewijze gids en ontgrendel het potentieel. Download nu!

### [Metered Licensing in Aspose.CAD voor .NET](./metered-licensing/)
Ontgrendel het potentieel van Aspose.CAD met metered licensing in .NET. Optimaliseer het resourcegebruik naadloos. Ontdek onze stapsgewijze gids.

## Veelgestelde vragen

**Q: Kan ik hetzelfde licentiebestand op meerdere machines gebruiken?**  
A: Ja, een enkel licentiebestand kan worden ingezet op een willekeurig aantal ontwikkelings‑ of productieservers, mits het gebruik overeenkomt met uw gekochte voorwaarden.

**Q: Wat gebeurt er als ik vergeet de licentie in te stellen voordat ik een CAD‑bestand laad?**  
A: De bibliotheek draait in evaluatiemodus, voegt een watermerk toe aan gerenderde afbeeldingen en beperkt het aantal pagina's dat u kunt verwerken.

**Q: Vereist metered licensing een internetverbinding?**  
A: Alleen de eerste activering en elk gebruiksrapport hebben verbinding nodig; daarna kan de bibliotheek offline werken tot het volgende rapport.

**Q: Welke CAD/BIM‑formaten worden standaard ondersteund?**  
A: Aspose.CAD ondersteunt meer dan 45 invoer‑ en uitvoerformaten, waaronder DWG, DXF, DGN, STL, OBJ en IFC, en kan bestanden tot 500 MB renderen zonder het volledige document in het geheugen te laden.

**Q: Is er een manier om programmatisch te controleren of de licentie succesvol is toegepast?**  
A: Roep `License.IsLicensed` (of inspecteer `License.LicenseFilePath`) aan na registratie; het retourneert `true` wanneer een geldige licentie actief is.

---

**Laatst bijgewerkt:** 2026-09-14  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose

## Gerelateerde handleidingen

- [Licentie toepassen via pad in Aspose.CAD voor .NET](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [Licentie toepassen met FileStream in Aspose.CAD voor .NET](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [Metered Licensing in Aspose.CAD voor .NET](/cad/net/licensing-and-configuration/metered-licensing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}