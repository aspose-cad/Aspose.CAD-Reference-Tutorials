---
date: 2026-02-28
description: Lär dig hur du läser DWG-filer med Aspose.CAD för Java och enkelt listar
  layouter i DWG-filer. Integrera kraftfull CAD-funktionalitet i dina Java-applikationer.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Hur man läser DWG och listar layouter i DWG med Aspose.CAD för Java
url: /sv/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

codes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man läser DWG och listar layouter i DWG med Aspose.CAD för Java

## Introduction

Om du letar efter ett pålitligt sätt **how to read dwg** filer programatiskt, erbjuder Aspose.CAD för Java ett rent, plattformsoberoende API som låter dig ladda en ritning och hämta all information du behöver—t.ex. namnen på alla layouter i filen. I den här steg‑för‑steg‑handledningen visar vi dig **how to read DWG** och listar varje layout som finns i en DWG‑ (eller DXF‑)fil, så att du kan integrera denna funktion i vilken Java‑applikation som helst som arbetar med CAD‑data.

## Quick Answers
- **Vilket bibliotek krävs?** Aspose.CAD for Java.  
- **Kan jag läsa DWG‑filer på vilket operativsystem som helst?** Ja – Java är plattformsoberoende, så du kan **read dwg on linux** lika enkelt som på Windows.  
- **Behöver jag en licens för att köra exemplet?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.  
- **Vilka CAD‑format stöds?** DWG, DXF, DWF och andra.  
- **Är koden kompatibel med Java 8+?** Absolut.

## What is “how to read dwg” in Java?

Att läsa en DWG‑fil innebär att ladda den binära CAD‑datan i en objektmodell som du kan fråga. Aspose.CAD abstraherar den komplexa DWG‑strukturen bakom enkla Java‑klasser, vilket låter dig fokusera på den information du behöver – i detta fall layoutnamn.

## Why list layouts in a DWG file?

En DWG kan innehålla flera layouter (paperspace, modelspace, anpassade blad). Att känna till layoutnamnen låter dig:

- Generera rapporter per layout.  
- Exportera specifika layouter till bilder eller PDF‑filer.  
- Automatisera batch‑behandling av ritningar.  

## Prerequisites

Innan vi dyker ner i koden, verifiera att du har följande:

- **Aspose.CAD for Java Library** – ladda ner den senaste JAR‑filen från [website](https://releases.aspose.com/cad/java/).  
- **Java Development Environment** – JDK 8 eller högre, samt en IDE eller byggverktyg du föredrar.

## Import Namespaces

I din Java‑källfil, importera de nödvändiga Aspose.CAD‑klasserna:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Step 1: Set up Your Document Directory

## Steg 1: Ställ in din dokumentkatalog

Byt ut **“Your Document Directory”** mot den absoluta sökvägen där dina CAD‑filer finns. På Linux kan du använda en sökväg som `/home/user/cad/`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## Step 2: Load the DWG File

## Steg 2: Ladda DWG‑filen

`Image.load`‑metoden upptäcker filformatet automatiskt, så samma kod fungerar för både **DWG**‑ och **DXF**‑filer.

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

## Step 3: Get Layouts and Print Names

## Steg 3: Hämta layouter och skriv ut namn

Loopen itererar över varje layout‑objekt och skriver dess namn till konsolen – ett enkelt sätt att verifiera att du framgångsrikt **read DWG** och extraherat layoutinformation.

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

## How to Convert DWG to PDF on Linux

## Så konverterar du DWG till PDF på Linux

Om du senare behöver omvandla en specifik layout till en PDF, kan Aspose.CAD rendera layouten till en bild och sedan kan du använda Aspose.PDF (eller något annat PDF‑bibliotek) för att bädda in den bilden i ett PDF‑dokument. Konverteringskoden är identisk på Linux eftersom API‑et är rent Java.

## Common Pitfalls & Tips

## Vanliga fallgropar & tips

- **Felaktig filsökväg** – Dubbelkolla att `dataDir` slutar med en separator (`/` eller `\\`) som passar ditt OS.  
- **Ej stödd DWG‑version** – Säkerställ att du använder en recent Aspose.CAD‑version; äldre DWG‑versioner kan behöva konverteras.  
- **Minnesanvändning** – Stora ritningar kan förbruka mycket minne. Frigör `CadImage`‑objektet när du är klar: `cadImage.dispose();`.  
- **Körning på huvudlösa servrar** – Inga UI‑komponenter krävs, så koden fungerar på Linux‑servrar utan grafisk miljö.

## Conclusion

## Slutsats

Grattis! Du vet nu **how to read dwg** och hur du listar dess layouter med Aspose.CAD för Java. Denna teknik utgör grunden för mer avancerad CAD‑automatisering, såsom att exportera specifika layouter till bilder, PDF‑filer eller till och med konvertera DWG till PDF på Linux. För djupare utforskning, se den officiella [documentation](https://reference.aspose.com/cad/java/).

## Frequently Asked Questions

## Vanliga frågor

**Q1: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?**  
A1: Ja, Aspose.CAD stöder olika CAD‑format, inklusive DWG, DXF, DWF och fler.

**Q2: Finns det en gratis provversion av Aspose.CAD för Java?**  
A2: Ja, du kan få en gratis provversion från [here](https://releases.aspose.com/).

**Q3: Var kan jag få community‑support för Aspose.CAD för Java?**  
A3: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑support.

**Q4: Hur köper jag en licens för Aspose.CAD för Java?**  
A4: Du kan köpa en licens på [purchase page](https://purchase.aspose.com/buy).

**Q5: Kan jag använda en tillfällig licens för testning?**  
A5: Ja, du kan få en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

**Additional Questions**

**Ytterligare frågor**

**Q: Fungerar detta tillvägagångssätt för att läsa DWG‑filer på Linux?**  
A: Absolut. Eftersom lösningen är ren Java kör den på alla OS med en kompatibel JDK.

**Q: Kan jag läsa en DWG‑fil utan att ladda hela ritningen i minnet?**  
A: Aspose.CAD laddar ritningen i minnet; för mycket stora filer kan du överväga att bearbeta dem i separata trådar eller använda streaming‑API:er om de blir tillgängliga i framtida versioner.

**Q: Finns det ett sätt att filtrera layouter efter namn?**  
A: Ja – efter att ha hämtat `CadLayoutDictionary` kan du kontrollera `layout.getLayoutName().equalsIgnoreCase("MyLayout")` innan bearbetning.

---

**Senast uppdaterad:** 2026-02-28  
**Testad med:** Aspose.CAD for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}