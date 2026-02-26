---
date: 2026-01-10
description: Leer hoe u DWG‑bestanden kunt lezen en multileader‑DWG‑entiteiten kunt
  maken met Aspose.CAD voor Java in deze stapsgewijze tutorial.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Hoe DWG te lezen en MLeader te ondersteunen met Aspose.CAD voor Java
url: /nl/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe DWG te lezen en MLeader te ondersteunen met Aspose.CAD voor Java

## Inleiding

Als je **DWG**‑bestanden moet **lezen** en wilt werken met **multileader DWG**‑entiteiten in een Java‑applicatie, ben je hier aan het juiste adres. Aspose.CAD voor Java biedt een nette, programmeerbare manier om DWG‑tekeningen te openen, MLeader‑objecten te inspecteren en hun eigenschappen te valideren — zonder dat je een volledige CAD‑werkstation nodig hebt. In deze tutorial lopen we stap voor stap door het proces, van het laden van een DWG‑bestand tot het bevestigen dat de multileader‑gegevens overeenkomen met de verwachte stijl.

## Snelle antwoorden
- **Waar bestaat “hoe dwg te lezen” uit?** Het laden van de DWG met `Image.load()` en casten naar `CadImage`.
- **Kan ik multileader‑dwg‑entiteiten maken?** Ja — je kunt MLeader‑objecten toevoegen, bewerken en valideren met de CadMLeader‑API.
- **Welke bibliotheekversie is vereist?** Elke recente Aspose.CAD voor Java‑release (de getoonde API werkt met builds vanaf 2024+).
- **Heb ik een licentie nodig voor ontwikkeling?** Een tijdelijke licentie werkt voor testen; een volledige licentie is vereist voor productie.
- **Is de code platform‑onafhankelijk?** Absoluut — Java draait op Windows, Linux en macOS.

## Wat is “hoe dwg te lezen” met Aspose.CAD?

Een DWG‑bestand lezen betekent het omzetten van de binaire tekening naar een `CadImage`‑object in het geheugen. Zodra je dat object hebt, kun je de entiteiten (lijnen, cirkels, tekst, **MLeader**‑objecten, enz.) enumereren en hun eigenschappen inspecteren.

## Waarom MLeader‑entiteiten ondersteunen?

MLeader (multileader)‑objecten combineren leidende lijnen met gekoppelde tekst of blokken, waardoor ze essentieel zijn voor annotaties in technische tekeningen. Het ondersteunen ervan stelt je in staat om:

- Te verifiëren dat annotaties voldoen aan de bedrijfsnormen.
- Tekst te extraheren voor downstream‑verwerking (bijv. BOM‑generatie).
- Leiderschapsstijlen programmatisch aan te passen of blokinhoud te vervangen.

## Voorvereisten

Voordat we beginnen, zorg dat je het volgende hebt:

1. **Java‑ontwikkelomgeving** — JDK 11+ en je favoriete IDE (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD voor Java** — Download de nieuwste JAR van de [download‑link](https://releases.aspose.com/cad/java/).  

## Import‑namespaces

Voeg de volgende imports toe aan je Java‑klasse zodat je met DWG‑entiteiten en rasterisatie‑opties kunt werken:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hoe DWG‑bestanden lezen met Aspose.CAD voor Java

### Stap 1: Laad het DWG‑bestand en verkrijg een `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Stap 2: Valideer dat de tekening MLeader‑entiteiten bevat

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Stap 3: Verifieer MLeader‑stijl en basisattributen

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Stap 4: Toegang tot de MLeader‑contextgegevens (het hart van de multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Stap 5: Valideer context‑niveau attributen

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Stap 6: Werk met de MLeader‑node en zijn leidende lijn

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Stap 7: Valideer aanvullende MLeader‑node‑attributen

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Stap 8: Controleer tekst‑gerelateerde eigenschappen

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Stap 9: Bekijk andere MLeader‑attributen voor volledigheid

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| `ClassCastException` bij het casten van entiteit | De geselecteerde index is geen MLeader‑object. | Controleer `cadImage.getEntities()[i] instanceof CadMLeader` vóór het casten. |
| `null`‑waarden voor punten van de leidende lijn | De tekening gebruikt een aangepaste leiderschapsstijl die niet volledig wordt ondersteund. | Gebruik de nieuwste Aspose.CAD‑versie of val terug op de standaardstijl voor testdoeleinden. |
| Assertion‑fouten op numerieke waarden | Kleine afrondingsverschillen tussen CAD‑versies. | Pas de tolerantie aan in `Assert.areEqual(..., delta)` zoals getoond in de voorbeelden. |

## Veelgestelde vragen

**V: Kan ik Aspose.CAD voor Java gebruiken met andere CAD‑formaten?**  
A: Ja, Aspose.CAD ondersteunt DXF, DWF, DGN en verschillende rasterformaten naast DWG.

**V: Waar vind ik gedetailleerde documentatie voor Aspose.CAD voor Java?**  
A: Raadpleeg de officiële [documentatie](https://reference.aspose.com/cad/java/) voor API‑details en code‑voorbeelden.

**V: Is er een gratis proefversie beschikbaar?**  
A: Absoluut — je kunt een proefversie downloaden vanaf de [free trial](https://releases.aspose.com/) pagina.

**V: Hoe verkrijg ik een tijdelijke licentie voor testen?**  
A: Vraag een tijdelijke licentie aan via de [temporary license link](https://purchase.aspose.com/temporary-license/).

**V: Waar kan ik de community om hulp vragen?**  
A: Het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) is de beste plek om vragen te stellen en oplossingen te delen.

## Conclusie

Je hebt nu een volledige, end‑to‑end walkthrough voor **hoe DWG‑bestanden te lezen** en **multileader‑DWG‑entiteiten te maken** met Aspose.CAD voor Java. Door de bovenstaande stappen te volgen, kun je MLeader‑stijlen valideren, annotatiedata extraheren en DWG‑verwerking integreren in elke Java‑gebaseerde workflow.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-01-10  
**Getest met:** Aspose.CAD 24.11 for Java  
**Auteur:** Aspose