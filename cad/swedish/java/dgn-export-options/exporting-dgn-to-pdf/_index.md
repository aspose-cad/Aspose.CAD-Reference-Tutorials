---
date: 2026-05-04
description: Lär dig hur du konverterar CAD‑PDF‑filer genom att exportera DGN till
  AutoCAD‑PDF med Aspose.CAD för Java. Steg‑för‑steg‑guide med anpassningsbar PDF‑storlek
  och alternativ.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Exportera DGN i AutoCAD‑format till PDF
second_title: Aspose.CAD Java API
title: Konvertera CAD PDF – Enkel DGN‑till‑AutoCAD PDF‑export med Aspose.CAD för Java
url: /sv/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera CAD PDF: Enkel DGN till AutoCAD PDF-export med Aspose.CAD för Java

## Introduktion

Om du behöver **konvertera CAD PDF**‑filer direkt från DGN‑källor, har du kommit till rätt ställe. I den här handledningen går vi igenom hur du använder Aspose.CAD för Java för att exportera DGN‑filer till en AutoCAD‑kompatibel PDF. Du får se hur du ställer in anpassade sidmått, väljer specifika layouter och finjusterar PDF‑utdata — allt med tydlig, steg‑för‑steg‑kod som du kan klistra in i ditt eget projekt.

## Snabba svar
- **Vad betyder “convert CAD PDF”?** Det avser att omvandla CAD‑källfiler (som DGN) till en PDF som bevarar vektordata och layout‑noggrannhet.  
- **Vilket bibliotek hanterar konverteringen?** Aspose.CAD för Java erbjuder en pålitlig, licensfri provversion för denna uppgift.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktionsbruk.  
- **Kan jag anpassa PDF‑storleken?** Ja – `CadRasterizationOptions` låter dig ange sidbredd, höjd och skalning.  
- **Hur många kodrader krävs?** Mindre än 20 rader Java‑kod för att läsa in, konfigurera och spara PDF‑filen.

## Vad är “convert CAD PDF”?
Att konvertera CAD PDF innebär att ta en inbyggd CAD‑ritning (t.ex. DGN) och producera en PDF som behåller de ursprungliga vektorgrafikerna, lagren och layout‑informationen. Den resulterande PDF‑filen kan visas på vilken enhet som helst utan att behöva CAD‑programvara, vilket gör den idealisk för delning, utskrift eller arkivering.

## Varför använda Aspose.CAD för Java för att konvertera CAD PDF?
- **Fullt formatstöd** – DGN, DWG, DXF och många fler.  
- **Inga externa beroenden** – ren Java, inga inhemska DLL‑filer.  
- **Fin‑granulär kontroll** – du kan välja vilka layouter som ska exporteras, ange anpassade sidstorlekar och styra rasteriseringskvaliteten.  
- **Skalbar för batchjobb** – läs in och spara dussintals filer i en loop med minimal overhead.

## Förutsättningar
Innan vi dyker ner, se till att du har följande:

- **Aspose.CAD Library** – ladda ner den [här](https://releases.aspose.com/cad/java/).  
- **Document Directory** – en mapp på din maskin där indata‑DGN‑filer och utdata‑PDF‑filer kommer att lagras.

## Importera paket

I ditt Java‑projekt importerar du de nödvändiga paketen för att få åtkomst till Aspose.CAD‑funktionerna:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nu bryter vi ner exempel­koden i flera steg:

## Steg 1: Definiera filsökvägar (hur man exporterar dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Se till att ersätta `"Your Document Directory"` med den faktiska sökvägen där dina filer finns.

## Steg 2: Ladda DGN‑bild

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Läs in DGN‑filen med Aspose.CAD.

## Steg 3: Ställ in PDF‑exportalternativ (anpassa pdf‑storlek, ställ in pdf‑alternativ)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Här definierar vi PDF‑exportalternativen, inklusive sidmått, automatisk skalning och de specifika DGN‑layouterna (vyer) du vill inkludera i den slutgiltiga PDF‑filen.

## Steg 4: Spara PDF‑fil

```java
objImage.save(outFile, options);
```

Spara den exporterade PDF‑filen. `save`‑metoden tillämpar alla de alternativ du konfigurerade i föregående steg.

Upprepa dessa steg för eventuella ytterligare DGN‑filer du vill konvertera. Grattis! Du har framgångsrikt **konverterat CAD PDF** genom att exportera DGN‑filer till AutoCAD‑format i PDF med Aspose.CAD för Java.

## Vanliga problem och lösningar
| Problem | Varför det händer | Lösning |
|-------|----------------|-----|
| **Filen hittades inte** | Felaktig `dataDir`‑sökväg | Dubbelkolla mappsökvägen och säkerställ att DGN‑filen finns. |
| **Tomma sidor i PDF** | `AutomaticLayoutsScaling` är satt till `false` eller saknar layout‑ID:n | Behåll `setAutomaticLayoutsScaling(true)` och verifiera layout‑namnen (`"1","2",…`). |
| **Lågupplöst output** | Standard‑DPI för rasterisering är låg | Använd `vectorOptions.setResolution(300);` för att öka kvaliteten (lägg till innan `setVectorRasterizationOptions`). |
| **Licensundantag** | Kör utan giltig licens i produktion | Applicera en tillfällig eller köpt licens enligt Aspose‑dokumentationen. |

## Vanliga frågor (tillägg)

**F: Kan jag exportera endast en enskild layout från en DGN‑fil med flera layouter?**  
S: Ja – ange önskade layout‑ID:n i `vectorOptions.setLayouts(new String[] { "2" });`.

**F: Är det möjligt att bädda in teckensnitt i den resulterande PDF‑filen?**  
S: Aspose.CAD bäddar automatiskt in de nödvändiga teckensnitten när vektordata rasteriseras; du kan också styra teckensnitts‑inbäddning via `PdfOptions` om så önskas.

**F: Hur bearbetar jag många DGN‑filer i en batch?**  
S: Lägg in stegen i en `for`‑loop som itererar över en lista med filnamn, och återanvänd samma `PdfOptions`‑instans för varje iteration.

**F: Stöder biblioteket lösenordsskyddade PDF‑filer?**  
S: Ja – du kan sätta ett lösenord på `PdfOptions`‑objektet via `options.setPassword("yourPassword");`.

**F: Var kan jag hitta fler exempel?**  
S: Den officiella Aspose.CAD‑dokumentationen och exempel‑repo innehåller många ytterligare scenarier.

## Vanliga frågor (Original)

### Q1: Är Aspose.CAD kompatibel med alla CAD‑filformat?

A1: Ja, Aspose.CAD stödjer ett brett spektrum av CAD‑format, vilket säkerställer mångsidighet vid hantering av olika filtyper.

### Q2: Kan jag anpassa PDF‑exportinställningarna?

A2: Absolut. Som visas i handledningen kan du justera alternativ som sidmått och layouter för att passa dina krav.

### Q3: Var kan jag hitta ytterligare support eller hjälp?

A3: Besök [Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för gemenskapsstöd och diskussioner.

### Q4: Finns det en gratis provversion?

A4: Ja, du kan komma åt den gratis provversionen [här](https://releases.aspose.com/).

### Q5: Hur kan jag skaffa en tillfällig licens?

A5: Skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

## Slutsats

I den här handledningen har vi utforskat hur man **konverterar CAD PDF**‑filer genom att utnyttja Aspose.CAD för Java. Med bara några rader kod kan du läsa in en DGN‑ritning, finjustera PDF‑exportalternativen och generera högkvalitativa PDF‑filer redo för delning eller arkivering. Känn dig fri att experimentera med olika sidstorlekar, layouter eller batch‑bearbetning för att passa ditt projekts behov.

---

**Senast uppdaterad:** 2026-05-04  
**Testad med:** Aspose.CAD för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}