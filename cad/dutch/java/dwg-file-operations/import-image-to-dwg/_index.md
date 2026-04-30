---
date: 2026-01-12
description: Leer hoe u een afbeelding kunt toevoegen aan DWG‑bestanden met Aspose.CAD
  voor Java en tevens DWG naar PDF kunt converteren. Volg onze stapsgewijze handleiding
  voor efficiënte ontwikkeling.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Afbeelding toevoegen aan DWG‑bestanden moeiteloos met Aspose.CAD Java
url: /nl/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding toevoegen aan DWG‑bestanden moeiteloos met Aspose.CAD Java

In moderne Java‑toepassingen is **het toevoegen van een afbeelding aan DWG**‑bestanden een veelvoorkomende behoefte—of je nu een CAD‑viewer gebouwd, tekeningen automatisch bijwerkt, of documentatie aangedreven. Aspose.CAD voor Java biedt een eenvoudige, hoogpresterende manier om rasterafbeeldingen direct in DWG-tekeningen in te sluiten zonder een volledige CAD-engine. In deze tutorial lopen we stap voor stap het hele proces door, van het laden van een DWG tot de export van het resultaat als PDF.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.CAD voor Java
- **Kan ik ook exporteren naar PDF?** Ja – gebruik `PdfOptions` met `CadRasterizationOptions`
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een wettelijke licentie is vereist voor productie
- **Welke Java‑versie wordt ondersteund?** Java8 en hoger
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis‑afbeeldingsimport

## Wat is “afbeelding toevoegen aan dwg”?
Een afbeelding toevoegen aan een DWG‑bestand betekent dat je een rasterafbeelding (PNG, JPEG, enz.) invoegt als een `CadRasterImage`‑object in de model‑ruimte van de tekening. De afbeelding wordt onderdeel van de CAD-entiteitboom en kan worden gepositioneerd, geschaald en bijgesneden net als elk ander CAD-object.

## Waarom Aspose.CAD voor Java gebruiken om afbeelding toe te voegen aan dwg?
- **Geen CAD‑software nodig** – de API verwerkt DWG‑parsing intern.
- **Fijne controle** over invoegpunt, schaalvectoren en bijsnijden.
- **Ingebouwde PDF-conversie** zodat je een afdrukbare PDF kunt genereren in dezelfde workflow.
- **Cross‑platform** – werkt op Windows, Linux en macOS.

## Vereisten
- Aspose.CAD voor Java: Zorg ervoor dat je de Aspose.CAD‑bibliotheek hebt geïnstalleerd. Je kunt dit downloaden [hier](https://releases.aspose.com/cad/java/).
- Java‑ontwikkelomgeving: JDK8+ met je favoriete IDE (IntelliJ, Eclipse, VSCode, enz.).

## Pakketten importeren
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Stapsgewijze handleiding

### Stap 1: Het DWG-bestand laden
Wijs eerst naar de map met uw DWG-tekening en laad deze met `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Stap 2: De rasterafbeelding definiëren
Maak een `CadRasterImageDef` die verwijst naar de externe PNG-afbeelding die u wilt insluiten. De constructor vereist de bestandsnaam van de afbeelding en de pixelafmetingen.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Stap 3: Invoegpunt en schaalvectoren instellen
Het invoegpunt bepaalt waar de linkerbenedenhoek van de afbeelding verschijnt. De vectoren **U** en **V** regelen de horizontale en verticale schaling.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Stap 4: Het CadRasterImage-object maken
Combineer de definitie, het invoegpunt en de vectoren tot een `CadRasterImage`. U kunt ook knipgrenzen instellen als u slechts een deel van de afbeelding zichtbaar wilt maken.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Stap 5: Voeg de afbeelding toe aan de modelruimte
Voeg de rasterafbeelding in het `*Model_Space`-blok in en werk vervolgens de objectverzameling van de tekening bij, zodat de definitie wordt opgeslagen.
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Stap 6: Configureer de PDF-exportopties (optioneel)
Als u ook een PDF-versie van de tekening nodig hebt, configureert u `PdfOptions` samen met `CadRasterizationOptions`. Deze stap laat zien hoe u **dwg naar pdf converteert** in dezelfde workflow.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Stap 7: Sla de resulterende PDF op
Exporteer ten slotte de gewijzigde tekening als een PDF-bestand. Dezelfde `image`-instantie wordt gebruikt, dus de PDF weerspiegelt de nieuw toegevoegde rasterafbeelding.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Door deze stappen te volgen, kunt u snel **afbeeldingen toevoegen aan DWG-bestanden** en indien nodig ook **DWG-bestanden opslaan als PDF**.

## Veelvoorkomende problemen en oplossingen
- **Afbeelding wordt niet weergegeven** – Controleer of het pad naar het afbeeldingsbestand (`road-sign-custom.png`) correct is en of de afmetingen van de afbeelding overeenkomen met de waarden die aan `CadRasterImageDef` zijn doorgegeven.

- **Onjuiste schaling** – Pas de U- en V-vectoren aan; deze vertegenwoordigen de tekeneenheden per pixel.

- **PDF ziet er leeg uit** – Zorg ervoor dat `CadRasterizationOptions.setDrawType` is ingesteld op `UseObjectColor` of een andere geschikte modus.

## Veelgestelde vragen

**V: Is Aspose.CAD voor Java compatibel met alle Java-ontwikkelomgevingen?**
A: Ja, Aspose.CAD voor Java is compatibel met de meeste Java-ontwikkelomgevingen.

**V: Kan ik Aspose.CAD voor Java gebruiken voor commerciële projecten?**
A: Ja, u kunt Aspose.CAD voor Java gebruiken voor commerciële projecten. Ga naar [hier](https://purchase.aspose.com/buy) voor licentiegegevens.

**V: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?**
A: Ja, u kunt de gratis proefversie [hier](https://releases.aspose.com/) downloaden.

**V: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?**
A: U kunt ondersteuning zoeken op het [Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).

**V: Kan ik een tijdelijke licentie verkrijgen voor Aspose.CAD voor Java?**
A: Ja, u kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 12-01-2026
**Getest met:** Aspose.CAD voor Java 24.11
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}