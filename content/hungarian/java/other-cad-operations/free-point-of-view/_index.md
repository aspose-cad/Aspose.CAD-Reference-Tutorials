---
title: Ingyenes nézőponti renderelés az Aspose.CAD for Java segítségével
linktitle: Ingyenes nézőpont
second_title: Aspose.CAD Java API
description: Fedezze fel az Aspose.CAD for Java erejét ebben az oktatóanyagban, amely a CAD-rajzok ingyenes nézőpont-megjelenítésének eléréséről szól. Engedd szabadjára az Aspose.CAD-ben rejlő lehetőségeket.
type: docs
weight: 14
url: /hu/java/other-cad-operations/free-point-of-view/
---
## Bevezetés

Üdvözöljük a "Free Point of View - Aspose.CAD for Java Tutorial" oldalán. Ebben az átfogó útmutatóban végigvezetjük az Aspose.CAD for Java kihasználásának folyamatán, hogy a CAD-rajzokhoz ingyenes nézőpontú megjelenítést érhessen el. Az Aspose.CAD egy hatékony Java-könyvtár, amely szolgáltatások széles skáláját kínálja a számítógéppel segített tervezési (CAD) fájlokkal való munkavégzéshez. Az oktatóanyag lefedi a szükséges előfeltételeket, az alapvető csomagok importálását, és az egyes példákat lépésről lépésre lebontja.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:
-  Aspose.CAD for Java Library: Töltse le és telepítse az Aspose.CAD for Java könyvtárat a[letöltési link](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Győződjön meg arról, hogy a Java telepítve van a gépen.

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat a Java projektbe. Adja hozzá a következő kódsorokat a Java fájl elejéhez:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

Ezek a csomagok elengedhetetlenek a CAD-fájlokkal való munkavégzéshez és a renderelési beállítások testreszabásához.

Most bontsuk fel a megadott példát több lépésre:

## 1. lépés: Állítsa be a dokumentumkönyvtárat

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Cserélje le a „Saját dokumentumkönyvtár” elemet a tényleges dokumentumkönyvtár elérési útjával.

## 2. lépés: Töltse be a CAD-rajzot

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

Adja meg a CAD-rajz elérési útját, és töltse be a segítségével`Image` osztály.

## 3. lépés: Konfigurálja a CAD-raszterezési beállításokat

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

Testreszabhatja a CAD raszterezési beállításait igényei szerint, például az oldal magassága és szélessége szerint.

## 4. lépés: A JpegOptions beállítása

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Hozzon létre egy példányt a`JpegOptions` és társítsa a korábban beállított raszterezési beállításokhoz.

## 5. lépés: Határozza meg az elforgatási szögeket

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

Adja meg az elforgatási szögeket az X, Y és Z tengelyek mentén a szabad nézőpontú rendereléshez.

## 6. lépés: Mentse el a renderelt képet

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

Mentse el a renderelt képet a megadott opciókkal a kívánt helyre.

Ismételje meg ezeket a lépéseket az Ön konkrét felhasználási esetére, így biztosítva a CAD-rajzok szabad nézőpontú megjelenítését.

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan valósítson meg ingyenes nézőpont-megjelenítést az Aspose.CAD for Java használatával. Ez az oktatóanyag az alapvető lépéseket ismertette, az előfeltételek beállításától a renderelési beállítások testreszabásáig és a kimeneti kép mentéséig.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for Java-t több platformon?

1. válasz: Igen, az Aspose.CAD for Java platformfüggetlen, és különféle operációs rendszereken használható.

### 2. kérdés: Vannak-e licencelési lehetőségek az Aspose.CAD for Java számára?

 2. válasz: Igen, felfedezheti a licencelési lehetőségeket, és vásárolhat[itt](https://purchase.aspose.com/buy).

### 3. kérdés: Van ingyenes próbaverzió?

 3. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 4. kérdés: Hol találok támogatást az Aspose.CAD for Java számára?

 A4: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásra és beszélgetésekre.

### 5. kérdés: Hogyan szerezhetek ideiglenes engedélyt?

 V5: Szerezzen ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).