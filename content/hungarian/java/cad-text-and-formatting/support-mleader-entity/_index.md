---
title: Támogassa az MLeader entitást DWG formátumhoz az Aspose.CAD for Java segítségével
linktitle: Támogassa az MLeader entitást DWG formátumhoz Java-val
second_title: Aspose.CAD Java API
description: Fedezze fel az Aspose.CAD for Java erejét lépésenkénti oktatóanyagunkkal az MLeader entitások támogatásáról DWG formátumban.
type: docs
weight: 12
url: /hu/java/cad-text-and-formatting/support-mleader-entity/
---
## Bevezetés

A Java-val ellátott számítógépes tervezés (CAD) területén az MLeader entitások támogatásának megértése és megvalósítása DWG formátumban értékes készség. Az Aspose.CAD for Java robusztus megoldást kínál az ilyen feladatokra, és hatékony eszközöket és funkciókat kínál. Ez az oktatóanyag végigvezeti az MLeader entitások DWG-fájlokon belüli támogatásának folyamatán Java és Aspose.CAD használatával.

## Előfeltételek

Mielőtt belemerülnénk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

1. Java fejlesztői környezet: Győződjön meg arról, hogy a rendszeren be van állítva Java fejlesztői környezet.

2.  Aspose.CAD Library: Töltse le és telepítse a Java Aspose.CAD könyvtárát a[letöltési link](https://releases.aspose.com/cad/java/).

## Névterek importálása

Java-projektjében importálja a szükséges névtereket az Aspose.CAD képességeinek hatékony kihasználásához. Helyezze be a következő sorokat a kódba:

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

Most bontsuk le a kódot egy lépésről lépésre, hogy támogassuk az MLeader entitásokat DWG formátumhoz Java és Aspose.CAD használatával.

## 1. Töltse be a DWG-fájlt, és lépjen be a CadImage-be

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Érvényesítse az MLeader entitásokat

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Ellenőrizze az MLeader stílusát és attribútumait

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Hozzáférés az MLeader kontextusadatokhoz

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Érvényesítse a környezeti attribútumokat

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Hozzáférés az MLeader csomóponthoz és a Leader Line-hoz

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

## 7. Érvényesítse a további MLeader attribútumokat

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Érvényesítse a szövegattribútumokat

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. További MLeader attribútumok

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Következtetés

Gratulálunk! Sikeresen navigált az átfogó útmutatóban az MLeader entitások támogatásáról DWG formátumban Java és Aspose.CAD használatával. Ez a képesség kaput nyit a fejlett CAD-manipulációk előtt, és továbbfejleszti a Java fejlesztői eszközkészletet.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for Java-t más CAD formátumokkal?

1. válasz: Igen, az Aspose.CAD a DWG-n kívül számos CAD formátumot is támogat, sokoldalúságot biztosítva a projektekben.

### 2. kérdés: Hol találom az Aspose.CAD for Java részletes dokumentációját?

 A2: Lásd a[dokumentáció](https://reference.aspose.com/cad/java/) az Aspose.CAD képességeibe való mélyreható betekintéshez.

### 3. kérdés: Van ingyenes próbaverzió?

 3. válasz: Igen, első kézből fedezze fel a funkciókat a[ingyenes próbaverzió](https://releases.aspose.com/).

### 4. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD számára?

A4: Szerezzen ideiglenes engedélyt a következőn keresztül[ez a link](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Hol kérhetek közösségi támogatást és segítséget?

A5: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) kapcsolatba lépni a közösséggel és segítséget kapni.