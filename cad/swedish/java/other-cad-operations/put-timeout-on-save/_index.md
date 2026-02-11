---
date: 2026-01-22
description: Lär dig hur du ställer in timeout när du sparar CAD till PDF med Aspose.CAD
  för Java. Öka prestanda med den här steg‑för‑steg‑guiden.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Hur man ställer in timeout för sparning av CAD med Aspose.CAD
url: /sv/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Timeout vid sparande för CAD med Aspose.CAD

## Introduktion

Välkommen till handledningen om **hur man ställer in timeout** när man sparar CAD-ritningar med Aspose.CAD för Java. I den här guiden går vi igenom processen för att konfigurera en timeout för sparoperationen, vilket hjälper till att hålla din applikation responsiv och förbättrar den övergripande prestandan. Aspose.CAD för Java är ett kraftfullt bibliotek som låter dig arbeta med CAD-filer sömlöst.

## Snabba svar
- **Vad gör timeouten?** Den avbryter sparoperationen om den överskrider den angivna varaktigheten, vilket förhindrar långa hängningar.  
- **Vilket format används i exemplet?** CAD-ritningen sparas som en PDF-fil.  
- **Behöver jag en licens?** En tillfällig eller permanent Aspose.CAD-licens krävs för produktionsanvändning.  
- **Vilken Java-version stöds?** Koden fungerar med Java 8 och senare.  
- **Kan jag justera timeoutens längd?** Ja – ändra helt enkelt värdet i `TimeUnit.SECONDS.sleep(...)`.

## Hur man ställer in timeout vid sparande

### Vad är en timeout i samband med Aspose.CAD?
En timeout är ett skydd som stoppar en långvarig rasteriserings- eller konverteringsprocess. Genom att tillhandahålla en `InterruptionTokenSource` kan du signalera till biblioteket att avbryta operationen efter en definierad period, vilket säkerställer att din applikation förblir responsiv.

### Varför ställa in en timeout när man sparar CAD till PDF?
Att spara stora eller komplexa CAD-ritningar kan förbruka betydande CPU och minne. Genom att lägga till en timeout:
- Förhindrar att applikationen fryser.  
- Gör att du kan hantera långvariga uppgifter på ett smidigt sätt.  
- Förbättrar den övergripande användarupplevelsen, särskilt i webb- eller UI‑drivna miljöer.

## Förutsättningar

- **Aspose.CAD for Java Library** – Se till att du har biblioteket integrerat i ditt projekt. Du kan ladda ner biblioteket från [webbplatsen](https://releases.aspose.com/cad/java/).  
- **Utvecklingsmiljö** – En Java-IDE (IntelliJ, Eclipse, etc.) med JDK 8+ installerad.

## Importera paket

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Nu ska vi gå igenom exempel­koden steg för steg:

## Steg 1: Ange käll- och utmatningskataloger

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Se till att du har rätt käll- och utmatningskataloger för dina CAD-ritningar.

## Steg 2: Skapa Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initiera en interruption token source för att hantera avbrott under sparoperationen.

## Steg 3: Ladda CAD-ritning

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Ladda CAD-ritningen i ett `CadImage`-objekt.

## Steg 4: Konfigurera rasteriseringsalternativ

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurera rasteriseringsalternativ för CAD-ritningen.

## Steg 5: Konfigurera PDF-alternativ

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ställ in PDF-alternativ med vektor‑rasteriseringsalternativ och interruption token.

## Steg 6: Spara ritning med timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Spara CAD-ritningen till en PDF-fil med den angivna timeouten.

## Steg 7: Hantera avbrott

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Skapa en tråd för att hantera sparoperationen och avbryt den efter en specificerad timeout.

## Vanliga fallgropar & felsökning

- **Timeouten för kort** – Om ritningen är stor kan en mycket kort timeout avbryta operationen innan den är klar. Öka sömnperioden eller justera rasteriseringsinställningarna.  
- **Saknad licens** – Att köra utan en giltig licens kommer att kasta ett undantag. Använd en tillfällig eller permanent licens innan du kör koden.  
- **Felaktiga sökvägar** – Se till att `SourceDir` och `OutputDir` pekar på befintliga mappar; annars kommer `Image.load` eller `save` att misslyckas.

## Vanliga frågor

**Q: Hur kan jag ladda ner Aspose.CAD för Java?**  
A: Du kan ladda ner det från [releases‑sidan](https://releases.aspose.com/cad/java/).

**Q: Var kan jag hitta dokumentationen för Aspose.CAD för Java?**  
A: Se [dokumentationen](https://reference.aspose.com/cad/java/) för omfattande information.

**Q: Finns det en gratis provversion?**  
A: Ja, du kan få en gratis provversion via [denna länk](https://releases.aspose.com/).

**Q: Hur får jag en tillfällig licens?**  
A: Besök [här](https://purchase.aspose.com/temporary-license/) för detaljer om tillfällig licens.

**Q: Behöver du hjälp eller har du frågor?**  
A: Gå till [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för gemenskapsstöd.

## Slutsats

Grattis! Du vet nu **hur man ställer in timeout** för sparoperationer när du konverterar CAD-ritningar till PDF med Aspose.CAD för Java. Att implementera denna timeout förbättrar pålitligheten och responsen i dina CAD‑relaterade applikationer.

---

**Last Updated:** 2026-01-22  
**Tested With:** Aspose.CAD for Java 24.11 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}