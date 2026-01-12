---
date: 2026-01-12
description: Lär dig hur du lägger till en bild i DWG‑filer med Aspose.CAD för Java
  och även konverterar DWG till PDF. Följ vår steg‑för‑steg‑guide för effektiv utveckling.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Lägg till bild i DWG-filer enkelt med Aspose.CAD Java
url: /sv/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till bild i DWG‑filer enkelt med Aspose.CAD Java

I moderna Java‑applikationer är **att lägga till en bild i DWG**‑filer ett vanligt krav – oavsett om du bygger en CAD‑visare, automatiserar uppdateringar av ritningar eller genererar dokumentation. Aspose.CAD för Java ger dig ett enkelt, högpresterande sätt att bädda in rasterbilder direkt i DWG‑ritningar utan att behöva en fullständig CAD‑motor. I den här handledningen går vi igenom hela processen, från att läsa in en DWG till att exportera resultatet som PDF.

## Snabba svar
- **Vilket bibliotek behövs?** Aspose.CAD för Java  
- **Kan jag också exportera till PDF?** Ja – använd `PdfOptions` tillsammans med `CadRasterizationOptions`  
- **Behövs licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion  
- **Vilken Java‑version stöds?** Java 8 och högre  
- **Hur lång tid tar implementeringen?** Cirka 10‑15 minuter för en grundläggande bildimport

## Vad betyder “add image to dwg”?
Att lägga till en bild i en DWG‑fil innebär att infoga en rasterbild (PNG, JPEG osv.) som ett `CadRasterImage`‑objekt i ritningens modellutrymme. Bilden blir en del av CAD‑entitetsträdet och kan positioneras, skalas och beskäras precis som alla andra CAD‑objekt.

## Varför använda Aspose.CAD för Java för att lägga till bild i dwg?
- **Ingen CAD‑programvara krävs** – API‑et hanterar DWG‑parsing internt.  
- **Fin‑granulär kontroll** över infogningspunkt, skalningsvektorer och beskärning.  
- **Inbyggd PDF‑konvertering** så att du kan generera en utskrivbar PDF i samma arbetsflöde.  
- **Plattformsoberoende** – fungerar på Windows, Linux och macOS.

## Förutsättningar
- Aspose.CAD för Java: Se till att du har Aspose.CAD‑biblioteket installerat. Du kan ladda ner det [här](https://releases.aspose.com/cad/java/).  
- Java‑utvecklingsmiljö: JDK 8+ med din favoriteditor (IntelliJ, Eclipse, VS Code osv.).

## Importera paket
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Steg‑för‑steg‑guide

### Steg 1: Läs in DWG‑filen
Ange först mappen som innehåller din DWG‑ritning och läs in den med `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Steg 2: Definiera rasterbilddefinitionen
Skapa en `CadRasterImageDef` som refererar till den externa PNG‑filen du vill bädda in. Konstruktorn tar bildfilens namn och dess pixelmått.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Steg 3: Ange infogningspunkt och skalningsvektorer
Infogningspunkten bestämmer var bildens nedre vänstra hörn kommer att placeras. **U**‑ och **V**‑vektorerna styr horisontell respektive vertikal skalning.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Steg 4: Skapa CadRasterImage‑objektet
Kombinera definitionen, infogningspunkten och vektorerna till ett `CadRasterImage`. Du kan också sätta beskärningsgränser om du bara vill visa en del av bilden.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Steg 5: Lägg till bilden i modellutrymmet
Infoga rasterbilden i blocket `*Model_Space` och uppdatera sedan ritningens objektkollektion så att definitionen sparas.
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

### Steg 6: Konfigurera PDF‑exportalternativ (valfritt)
Om du också behöver en PDF‑version av ritningen, konfigurera `PdfOptions` tillsammans med `CadRasterizationOptions`. Detta steg visar hur du **konverterar dwg till pdf** i samma flöde.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Steg 7: Spara den resulterande PDF‑filen
Exportera slutligen den modifierade ritningen som en PDF‑fil. Samma `image`‑instans används, så PDF‑filen innehåller den nyinfogade rasterbilden.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Genom att följa dessa steg kan du **lägga till bild i dwg**‑filer snabbt och även **spara dwg som pdf** om så behövs.

## Vanliga problem och lösningar
- **Bilden visas inte** – Kontrollera att bildfilens sökväg (`road-sign-custom.png`) är korrekt och att bildens dimensioner matchar de värden som skickas till `CadRasterImageDef`.  
- **Felaktig skalning** – Justera U‑ och V‑vektorerna; de representerar ritningsenheter per pixel.  
- **PDF blir tom** – Säkerställ att `CadRasterizationOptions.setDrawType` är satt till `UseObjectColor` eller ett annat lämpligt läge.

## Vanliga frågor

**Q: Är Aspose.CAD för Java kompatibel med alla Java‑utvecklingsmiljöer?**  
A: Ja, Aspose.CAD för Java är kompatibel med de flesta Java‑utvecklingsmiljöer.

**Q: Kan jag använda Aspose.CAD för Java i kommersiella projekt?**  
A: Ja, du kan använda Aspose.CAD för Java i kommersiella projekt. Besök [här](https://purchase.aspose.com/buy) för licensinformation.

**Q: Finns det en gratis provversion av Aspose.CAD för Java?**  
A: Ja, du kan komma åt den gratis provversionen [här](https://releases.aspose.com/).

**Q: Hur får jag support för Aspose.CAD för Java?**  
A: Du kan söka support på [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19).

**Q: Kan jag få en tillfällig licens för Aspose.CAD för Java?**  
A: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

---

**Senast uppdaterad:** 2026-01-12  
**Testad med:** Aspose.CAD för Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}