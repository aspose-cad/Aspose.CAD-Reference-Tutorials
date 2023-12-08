---
title: Timeout vid Spara för CAD med Aspose.CAD
linktitle: Sätt Timeout på Spara
second_title: Aspose.CAD Java API
description: Lär dig hur du förbättrar din Java-applikations prestanda med Aspose.CAD. Sätt en timeout på spara för CAD-ritningar. Följ vår steg-för-steg-guide.
type: docs
weight: 15
url: /sv/java/other-cad-operations/put-timeout-on-save/
---
## Introduktion

Välkommen till handledningen om hur du sätter en timeout för att spara med Aspose.CAD för Java. I den här guiden går vi igenom processen att ställa in en timeout för att spara CAD-ritningar för att förbättra din applikations prestanda. Aspose.CAD för Java är ett kraftfullt bibliotek som låter dig arbeta med CAD-filer i dina Java-applikationer sömlöst.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:
-  Aspose.CAD for Java Library: Se till att du har Aspose.CAD for Java-biblioteket integrerat i ditt projekt. Du kan ladda ner biblioteket från[hemsida](https://releases.aspose.com/cad/java/).
- Utvecklingsmiljö: Konfigurera din Java-utvecklingsmiljö med alla nödvändiga verktyg och beroenden.

## Importera paket

För att komma igång, importera de nödvändiga paketen till ditt Java-projekt. Lägg till följande rader i början av din Java-fil:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Låt oss nu dela upp exempelkoden i steg-för-steg-instruktioner:

## Steg 1: Ställ in käll- och utdatakataloger

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Se till att du har rätt käll- och utdatakataloger för dina CAD-ritningar.

## Steg 2: Skapa avbrottstokenkälla

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initiera en avbrottstokenkälla för att hantera avbrott under lagringsoperationen.

## Steg 3: Ladda CAD-ritning

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Ladda CAD-ritningen i en`CadImage` objekt.

## Steg 4: Konfigurera rasteriseringsalternativ

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurera rastreringsalternativ för CAD-ritningen.

## Steg 5: Konfigurera PDF-alternativ

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ställ in PDF-alternativ med vektorrasteriseringsalternativ och avbrottstoken.

## Steg 6: Spara ritning med Timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Spara CAD-ritningen till en PDF-fil med angiven timeout.

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

Skapa en tråd för att hantera sparoperationen och avbryt den efter en angiven timeout.

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du sätter en timeout för att spara med Aspose.CAD för Java. Denna funktion kan avsevärt förbättra effektiviteten för dina CAD-relaterade applikationer.

## FAQ's

### F1: Hur kan jag ladda ner Aspose.CAD för Java?

 A1: Du kan ladda ner det från[släpper sida](https://releases.aspose.com/cad/java/).

### F2: Var kan jag hitta dokumentationen för Aspose.CAD för Java?

 A2: Se[dokumentation](https://reference.aspose.com/cad/java/) för omfattande information.

### F3: Finns det en gratis provperiod?

A3: Ja, du kan få en gratis provperiod från[den här länken](https://releases.aspose.com/).

### F4: Hur får jag en tillfällig licens?

 A4: Besök[här](https://purchase.aspose.com/temporary-license/) för tillfälliga licensdetaljer.

### F5: Behöver du hjälp eller har frågor?

 A5: Gå över till[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd.