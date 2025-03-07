---
title: A CAD rajz méretének beállítása az egységtípus használatával az Aspose.CAD for Java segítségével
linktitle: A CAD rajz méretének beállítása az egységtípus használatával
second_title: Aspose.CAD Java API
description: Fedezze fel az Aspose.CAD for Java erejét a CAD rajzméretek könnyed beállításában. Kövesse lépésenkénti útmutatónkat a pontosság és az alkalmazkodóképesség érdekében.
weight: 14
url: /hu/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# A CAD rajz méretének beállítása az egységtípus használatával az Aspose.CAD for Java segítségével

## Bevezetés

számítógéppel segített tervezés (CAD) folyamatosan fejlődő birodalmában a precizitás és az alkalmazkodóképesség a legfontosabb. Az egyik általános követelmény a CAD-rajzok méretének beállítása az egyes egységtípusok alapján. Az Aspose.CAD for Java hatékony szövetségesként jelenik meg, amely zökkenőmentes képességeket biztosít a CAD-fájlok programozott kezeléséhez.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

- Java fejlesztői környezet: Győződjön meg arról, hogy működő Java fejlesztői környezet van beállítva a gépen.

-  Aspose.CAD for Java Library: Töltse le és integrálja az Aspose.CAD könyvtárat Java projektjébe. Megkaphatja a könyvtárat[itt](https://releases.aspose.com/cad/java/).

## Névterek importálása

Java kódjában adja meg az Aspose.CAD funkciók eléréséhez szükséges névtereket. Adja hozzá a következő importokat:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Most bontsuk fel a CAD rajzméret egységtípussal történő beállításának folyamatát kezelhető lépésekre:

## 1. lépés: Adja meg az adatkönyvtárat

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Állítsa be annak a könyvtárnak az elérési útját, ahol a CAD-fájlok találhatók.

## 2. lépés: Töltse be a CAD-rajzot

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Töltse be a CAD rajzot az Aspose.CAD segítségével`Image` osztály.

## 3. lépés: BMP-beállítások létrehozása

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Példányosítsa a`BmpOptions` osztály a CAD-elrendezés BMP formátumba exportálásához.

## 4. lépés: Konfigurálja a raszterezési beállításokat

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Hozzon létre egy példányt a`CadRasterizationOptions` és társítsa a`BmpOptions` vektor raszterizálásához.

## 5. lépés: Állítsa be az egység típusát

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Adja meg a kívánt egységtípust a CAD-rajzhoz. Ebben a példában centiméterre állítottuk.

## 6. lépés: Állítsa be az elrendezéseket

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Határozza meg az exportálás során figyelembe veendő elrendezéseket. Ebben az esetben a „Modell” elrendezést választottuk.

## 7. lépés: Exportálás BMP-be

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Végül mentse el a módosított CAD rajzot BMP formátumban.

## Következtetés

Az Aspose.CAD for Java segítségével a CAD rajzméretek beállítása gyerekjáték lesz. Ez az oktatóanyag végigvezette Önt a folyamaton, hangsúlyozva az egyes lépések jelentőségét a pontos eredmények elérésében.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for Java-t más programozási nyelvekkel?

1. válasz: Az Aspose.CAD elsősorban a Java-t támogatja, de vannak verziók más nyelvekhez is, például a .NET-hez.

### 2. kérdés: Vannak-e licencelési lehetőségek az Aspose.CAD számára?

 2. válasz: Igen, felfedezheti a licencelési lehetőségeket, és megvásárolhatja az Aspose.CAD-t[itt](https://purchase.aspose.com/buy).

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.CAD számára?

 3. válasz: Természetesen hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 4. kérdés: Hogyan kaphatok támogatást az Aspose.CAD for Java számára?

 4. válasz: Látogassa meg az Aspose.CAD fórumot[itt](https://forum.aspose.com/c/cad/19) átfogó támogatásért.

### 5. kérdés: Kaphatok ideiglenes licencet az Aspose.CAD számára?

 V5: Igen, szerezhet ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
