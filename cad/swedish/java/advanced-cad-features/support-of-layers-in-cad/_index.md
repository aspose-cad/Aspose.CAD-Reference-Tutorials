---
date: 2025-12-13
description: Lär dig hur du sparar CAD som JPEG i Java med Aspose.CAD, lägger till
  flera lager och justerar CAD-dimensioner för exakt bildkonvertering.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Spara CAD som JPEG med lagerstöd i Java
url: /sv/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara CAD som JPEG med lagerstöd i Java

## Introduktion

I den här handledningen kommer du att upptäcka hur du **sparar CAD som JPEG** samtidigt som du utnyttjar lagerstöd i Aspose.CAD för Java. Lager låter dig isolera specifika delar av en ritning, vilket gör det enkelt att exportera bara det du behöver. Vi går igenom varje steg, från att konfigurera miljön till att exportera en JPEG som bara innehåller de lager du väljer.

## Snabba svar
- **Vad betyder “save CAD as JPEG”?** Det konverterar en CAD-ritning till en raster JPEG-bild.
- **Kan jag inkludera endast valda lager?** Ja – använd `setLayers`-metoden för att ange vilka lager som ska renderas.
- **Hur ändrar jag bildens storlek?** Justera `setPageWidth` och `setPageHeight` i `CadRasterizationOptions`.
- **Är detta en lösning enbart för Java?** Exemplet använder Aspose.CAD för Java, men samma koncept gäller för andra språk.
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.

## Förutsättningar

Innan du dyker ner, se till att du har följande:

1. **Aspose.CAD for Java Library** – ladda ner den från [webbplatsen](https://releases.aspose.com/cad/java/). Följ installationsguiden för att lägga till JAR-filerna i ditt projekts classpath.  
2. **Java Development Environment** – en aktuell JDK (8 eller nyare) installerad på din maskin.

Nu när vi är klara, låt oss utforska koden som behövs för att **spara CAD som JPEG** med selektiv lagerrendering.

## Importera namnrymder

Börja med att importera de nödvändiga Aspose.CAD-klasserna och standard Java-verktygen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Steg‑för‑steg‑guide

### Steg 1: Ange filsökvägar

Definiera var källfilen DWF finns och var den resulterande JPEG-filen ska skrivas.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Steg 2: Läs in DWF‑bilden

Använd Aspose.CAD:s `Image.load`-metod för att läsa CAD-ritningen.

```java
Image image = Image.load(srcFile);
```

### Steg 3: Konfigurera rasteriseringsalternativ (justera CAD-dimensioner)

Skapa en `CadRasterizationOptions`-instans och ange önskad utskriftsstorlek. Att ändra dessa värden låter dig **justera CAD-dimensioner** för den slutliga JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Steg 4: Ange lager (lägg till flera lager)

Om du vill rendera mer än ett lager, lägg helt enkelt till deras namn i listan. Här börjar vi med ett enda lager som heter “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Proffstips:* För att **lägga till flera lager**, utöka `Arrays.asList`-anropet, t.ex. `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Steg 5: Konfigurera JPEG‑alternativ (Java konverterar CAD‑bild)

Koppla rasteriseringsinställningarna till JPEG-utdataformatet.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 6: Exportera till JPG (spara CAD som JPEG)

Skriv slutligen bilden till disk. Detta steg **sparar CAD-ritningen som en JPEG**-fil som bara innehåller de valda lagren.

```java
image.save(outFile, jpegOptions);
```

Genom att följa dessa steg har du framgångsrikt **sparat CAD som JPEG** samtidigt som du styr vilka lager som visas och anpassar bildens dimensioner.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Lager visas inte** | Verifiera att lagernamnen exakt matchar vad som finns i DWF-filen (skiftlägeskänsligt). |
| **Utdatabilden är tom** | Se till att `setPageWidth` och `setPageHeight` är tillräckligt stora för ritningens omfattning. |
| **Licensundantag** | Använd en provlicens för testning; skaffa en full licens för produktionsmiljöer. |

## Vanliga frågor

**Q: Kan jag lägga till flera lager i rasteriseringsalternativen?**  
A: Absolut. Utöka `stringList` med ytterligare lagernamn, t.ex. `Arrays.asList("LayerA", "LayerB")`.

**Q: Är Aspose.CAD kompatibel med andra CAD-format?**  
A: Ja, den stöder DWG, DXF, DWF och många fler format.

**Q: Hur kan jag ändra bildens utdata-dimensioner?**  
A: Ändra `setPageWidth` och `setPageHeight` i `CadRasterizationOptions`-instansen.

**Q: Var kan jag köpa en licens för Aspose.CAD?**  
A: Du kan utforska licensalternativ [här](https://purchase.aspose.com/buy).

**Q: Var kan jag få community‑support?**  
A: Gå med i Aspose.CAD‑communityn på [forumet](https://forum.aspose.com/c/cad/19) för hjälp och diskussioner.

---

**Senast uppdaterad:** 2025-12-13  
**Testat med:** Aspose.CAD for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}