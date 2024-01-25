---
title: Podporujte entitu MLeader pro formát DWG pomocí Aspose.CAD pro Javu
linktitle: Podporujte entitu MLeader pro formát DWG pomocí Java
second_title: Aspose.CAD Java API
description: Odemkněte sílu Aspose.CAD for Java s naším podrobným návodem na podporu entit MLeader ve formátu DWG.
type: docs
weight: 12
url: /cs/java/cad-text-and-formatting/support-mleader-entity/
---
## Úvod

V oblasti počítačově podporovaného navrhování (CAD) s Javou je pochopení a implementace podpory pro entity MLeader ve formátu DWG cennou dovedností. Aspose.CAD for Java poskytuje robustní řešení pro takové úkoly a nabízí sadu výkonných nástrojů a funkcí. Tento tutoriál vás provede procesem podpory entit MLeader v souborech DWG pomocí Java s Aspose.CAD.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1. Vývojové prostředí Java: Ujistěte se, že máte ve svém systému nastavené vývojové prostředí Java.

2.  Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Javu z[odkaz ke stažení](https://releases.aspose.com/cad/java/).

## Importovat jmenné prostory

Do svého projektu Java importujte potřebné jmenné prostory, abyste efektivně využili schopnosti Aspose.CAD. Zahrňte do svého kódu následující řádky:

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

Nyní si rozeberme kód do podrobného průvodce pro podporu entit MLeader pro formát DWG pomocí Java s Aspose.CAD.

## 1. Načtěte soubor DWG a otevřete CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Ověřte entity MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Ověřte styl a atributy MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Přístup k kontextovým datům MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Ověřte kontextové atributy

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Otevřete MLeader Node a Leader Line

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

## 7. Ověřte další atributy MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Ověřte textové atributy

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Další atributy MLeader

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Závěr

Gratulujeme! Úspěšně jste prošli obsáhlým průvodcem o podpoře entit MLeader pro formát DWG pomocí Java a Aspose.CAD. Tato schopnost otevírá dveře pokročilým CAD manipulacím a vylepšuje vaši sadu nástrojů pro vývoj Java.

## FAQ

### Q1: Mohu použít Aspose.CAD for Java s jinými formáty CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD nad rámec DWG a poskytuje všestrannost ve vašich projektech.

### Q2: Kde najdu podrobnou dokumentaci k Aspose.CAD for Java?

 A2: Viz[dokumentace](https://reference.aspose.com/cad/java/) pro hloubkový náhled do možností Aspose.CAD.

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, prozkoumejte funkce z první ruky s[zkušební verze zdarma](https://releases.aspose.com/).

### Q4: Jak mohu získat dočasné licencování pro Aspose.CAD?

A4: Získejte dočasnou licenci prostřednictvím[tento odkaz](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu hledat podporu a pomoc komunity?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) spojit se s komunitou a získat pomoc.