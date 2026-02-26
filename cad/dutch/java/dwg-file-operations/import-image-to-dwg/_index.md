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

In moderne Java‑toepassingen is **het toevoegen van een afbeelding aan DWG**‑bestanden een veelvoorkomende behoefte—of je nu een CAD‑viewer bouwt, tekeningen automatisch bijwerkt, of documentatie genereert. Aspose.CAD voor Java biedt een eenvoudige, hoog‑presterende manier om rasterafbeeldingen direct in DWG‑tekeningen in te sluiten zonder een volledige CAD‑engine. In deze tutorial lopen we stap voor stap het hele proces door, van het laden van een DWG tot het exporteren van het resultaat als PDF.

## Quick Answers
- **Welke bibliotheek heb ik nodig?** Aspose.CAD voor Java  
- **Kan ik ook exporteren naar PDF?** Ja – gebruik `PdfOptions` met `CadRasterizationOptions`  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie  
- **Welke Java‑versie wordt ondersteund?** Java 8 en hoger  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis‑afbeeldingsimport

## Wat is “add image to dwg”?
Een afbeelding toevoegen aan een DWG‑bestand betekent dat je een rasterafbeelding (PNG, JPEG, enz.) invoegt als een `CadRasterImage`‑object in de model‑space van de tekening. De afbeelding wordt onderdeel van de CAD‑entiteitboom en kan worden gepositioneerd, geschaald en bijgesneden net als elk ander CAD‑object.

## Waarom Aspose.CAD voor Java gebruiken om afbeelding toe te voegen aan dwg?
- **Geen CAD‑software nodig** – de API verwerkt DWG‑parsing intern.  
- **Fijne controle** over invoegpunt, schaalsvectoren en bijsnijden.  
- **Ingebouwde PDF‑conversie** zodat je een afdrukbare PDF kunt genereren in dezelfde workflow.  
- **Cross‑platform** – werkt op Windows, Linux en macOS.

## Prerequisites
- Aspose.CAD voor Java: Zorg ervoor dat je de Aspose.CAD‑bibliotheek hebt geïnstalleerd. Je kunt deze downloaden [hier](https://releases.aspose.com/cad/java/).  
- Java‑ontwikkelomgeving: JDK 8+ met je favoriete IDE (IntelliJ, Eclipse, VS Code, enz.).

## Import Packages
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File
First, point to the folder that contains your DWG drawing and load it with `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Step 2: Define the Raster Image Definition
Create a `CadRasterImageDef` that references the external PNG you want to embed. The constructor takes the image file name and its pixel dimensions.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Step 3: Set Insertion Point and Scaling Vectors
The insertion point determines where the lower‑left corner of the image will appear. The **U** and **V** vectors control horizontal and vertical scaling.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Step 4: Create the CadRasterImage Object
Combine the definition, insertion point, and vectors into a `CadRasterImage`. You can also set clipping boundaries if you only want part of the picture visible.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Step 5: Add the Image to Model Space
Insert the raster image into the `*Model_Space` block, then update the drawing’s object collection so the definition is saved.
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

### Step 6: Configure PDF Export Options (Optional)
If you also need a PDF version of the drawing, configure `PdfOptions` together with `CadRasterizationOptions`. This step demonstrates how to **convert dwg to pdf** in the same flow.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Step 7: Save the Resulting PDF
Finally, export the modified drawing as a PDF file. The same `image` instance is used, so the PDF reflects the newly added raster image.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

By following these steps, you can **add image to dwg** files quickly and also **save dwg as pdf** if needed.

## Common Issues and Solutions
- **Image not appearing** – Verify that the image file path (`road-sign-custom.png`) is correct and that the image dimensions match the values passed to `CadRasterImageDef`.  
- **Incorrect scaling** – Adjust the U and V vectors; they represent the drawing units per pixel.  
- **PDF looks blank** – Ensure `CadRasterizationOptions.setDrawType` is set to `UseObjectColor` or another appropriate mode.

## Frequently Asked Questions

**Q: Is Aspose.CAD for Java compatible with all Java development environments?**  
A: Yes, Aspose.CAD for Java is compatible with most Java development environments.

**Q: Can I use Aspose.CAD for Java for commercial projects?**  
A: Yes, you can use Aspose.CAD for Java for commercial projects. Visit [here](https://purchase.aspose.com/buy) for licensing details.

**Q: Is there a free trial available for Aspose.CAD for Java?**  
A: Yes, you can access the free trial [here](https://releases.aspose.com/).

**Q: How can I get support for Aspose.CAD for Java?**  
A: You can seek support on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

**Q: Can I obtain a temporary license for Aspose.CAD for Java?**  
A: Yes, you can get a temporary license [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-01-12  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}