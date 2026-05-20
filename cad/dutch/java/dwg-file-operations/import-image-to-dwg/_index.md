---
date: 2026-05-20
description: Leer hoe je een afbeelding toevoegt aan DWG-bestanden met Aspose.CAD
  voor Java en tevens DWG naar PDF converteert. Volg onze stapsgewijze handleiding
  voor efficiënte ontwikkeling.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Afbeelding importeren in DWG-bestand met Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Afbeelding toevoegen aan DWG-bestanden moeiteloos met Aspose.CAD Java
url: /nl/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding toevoegen aan DWG‑bestanden moeiteloos met Aspose.CAD Java

In moderne Java‑toepassingen is **het toevoegen van een afbeelding aan DWG**‑bestanden een veelvoorkomende eis—of je nu een CAD‑viewer bouwt, tekeningen automatisch bijwerkt of documentatie genereert. Aspose.CAD voor Java biedt een eenvoudige, hoge‑prestaties manier om rasterafbeeldingen direct in DWG‑tekeningen in te sluiten zonder een volledige CAD‑engine te hoeven gebruiken. In deze tutorial lopen we het volledige proces door, van het laden van een DWG tot het exporteren van het resultaat als PDF, en we behandelen ook hoe je **een afbeelding in een dwg importeert** en **dwg naar pdf converteert** in één workflow.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.CAD voor Java  
- **Kan ik ook exporteren naar PDF?** Ja – gebruik `PdfOptions` met `CadRasterizationOptions`  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie  
- **Welke Java‑versie wordt ondersteund?** Java 8 en hoger  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisafbeeldingsimport  

## Wat is “afbeelding toevoegen aan dwg”?

Een afbeelding toevoegen aan een DWG‑bestand betekent dat je een rasterafbeelding (PNG, JPEG, enz.) als een **CadRasterImage**‑entiteit in de model‑space van de tekening embedde, waar deze kan worden gepositioneerd, geschaald en eventueel bijgesneden net als elk ander CAD‑object. Het wordt opgeslagen in de objecttabel van de tekening en weergegeven door standaard CAD‑viewers.

## Waarom Aspose.CAD voor Java gebruiken om afbeelding toe te voegen aan dwg?

Je kunt rastergrafische bestanden in DWG‑bestanden embedden zonder enige derde‑partij CAD‑software te installeren, en de API geeft je pixel‑preciese controle over het invoegpunt, de schaalsvectoren en de bijsnijdingsgrenzen. Aspose.CAD verwerkt bestanden tot 2 GB, ondersteunt **meer dan 50 invoer‑ en uitvoerformaten**, en draait op Windows, Linux en macOS, zodat je CAD‑manipulatie kunt integreren in elke Java‑gebaseerde backend.

## Vereisten
- **Aspose.CAD voor Java** – download de nieuwste JAR van de officiële site **[hier](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 of nieuwer, met je favoriete IDE (IntelliJ IDEA, Eclipse, VS Code, enz.).  
- Een geldige **Aspose.CAD‑licentie** voor productiegebruik (de proefversie werkt voor experimenten).  

## Importpakketten
De volgende imports brengen de essentiële Aspose.CAD‑klassen binnen die worden gebruikt voor afbeeldingsmanipulatie en PDF‑conversie.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Stapsgewijze handleiding

### Stap 1: Laad het DWG‑bestand
Geef eerst de map op die je DWG‑tekening bevat en laad deze met `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Stap 2: Definieer de rasterafbeeldingsdefinitie
De `CadRasterImageDef`‑klasse definieert de externe rasterafbeeldingsbron die in de tekening moet worden ingebed.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Stap 3: Stel invoegpunt en schaalsvectoren in
Het invoegpunt bepaalt waar de linksonderhoek van de afbeelding verschijnt. De **U**‑ en **V**‑vectoren regelen respectievelijk de horizontale en verticale schaal.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Stap 4: Maak het CadRasterImage‑object aan
De `CadRasterImage`‑entiteit vertegenwoordigt een rasterafbeelding die in de DWG‑model‑space is geplaatst.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Stap 5: Voeg de afbeelding toe aan Model Space
Voeg de rasterafbeelding in het `*Model_Space`‑blok in en werk vervolgens de objectcollectie van de tekening bij zodat de definitie wordt opgeslagen.  
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

### Stap 6: Configureer PDF‑exportopties (optioneel)
`PdfOptions` specificeert instellingen voor het opslaan van een CAD‑tekening als PDF‑bestand. `CadRasterizationOptions` bepaalt hoe de CAD‑inhoud wordt gerasterd tijdens de PDF‑conversie.  
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
Exporteer tenslotte de gewijzigde tekening als een PDF‑bestand. Dezelfde `image`‑instantie wordt gebruikt, zodat de PDF de nieuw toegevoegde rasterafbeelding weergeeft.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Door deze stappen te volgen kun je **afbeelding toevoegen aan dwg**‑bestanden snel uitvoeren en tevens **dwg opslaan als pdf** wanneer dat nodig is, waardoor de meest voorkomende **dwg‑bestandsbewerkingen** in één compacte routine worden gedekt.

## Veelvoorkomende problemen en oplossingen
- **Afbeelding verschijnt niet** – Controleer of het afbeeldingspad (`road-sign-custom.png`) correct is en of de afbeeldingsafmetingen overeenkomen met de waarden die aan `CadRasterImageDef` zijn doorgegeven.  
- **Onjuiste schaal** – Pas de U‑ en V‑vectoren aan; ze vertegenwoordigen de tekeneenheden per pixel.  
- **PDF ziet er leeg uit** – Zorg ervoor dat `CadRasterizationOptions.setDrawType` is ingesteld op `UseObjectColor` of een andere geschikte modus.  

## Veelgestelde vragen

**V: Is Aspose.CAD voor Java compatibel met alle Java‑ontwikkelomgevingen?**  
A: Ja, Aspose.CAD voor Java werkt met elke IDE die JDK 8+ ondersteunt, inclusief IntelliJ IDEA, Eclipse en VS Code.

**V: Mag ik Aspose.CAD voor Java gebruiken in commerciële projecten?**  
A: Ja, je kunt Aspose.CAD voor Java gebruiken in commerciële projecten. Bezoek **[hier](https://purchase.aspose.com/buy)** voor licentie‑details.

**V: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt de gratis proefversie **[hier](https://releases.aspose.com/)** verkrijgen.

**V: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?**  
A: Je kunt ondersteuning zoeken op het **[Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19)**.

**V: Kan ik een tijdelijke licentie verkrijgen voor Aspose.CAD voor Java?**  
A: Ja, je kunt een tijdelijke licentie **[hier](https://purchase.aspose.com/temporary-license/)** krijgen.

---

**Laatst bijgewerkt:** 2026-05-20  
**Getest met:** Aspose.CAD voor Java 24.11  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [DWG exporteren naar PDF of raster met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aangepaste eigenschappen toevoegen aan DWG‑bestanden met Aspose.CAD voor Java](/cad/java/additional-features/add-custom-properties/)
- [CAD opslaan als PNG – CAD‑tekening converteren naar rasterafbeeldingsformaat met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}