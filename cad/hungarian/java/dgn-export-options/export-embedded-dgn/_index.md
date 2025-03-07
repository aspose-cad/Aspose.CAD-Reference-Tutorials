---
title: Exportáljon beágyazott DGN-t PDF-be az Aspose.CAD for Java segítségével
linktitle: Beágyazott DGN exportálása
second_title: Aspose.CAD Java API
description: Tekintse meg a beágyazott DGN-fájlok PDF-formátumba exportálásáról szóló, lépésről lépésre szóló útmutatót az Aspose.CAD for Java használatával. Bővítse Java-alkalmazásait a zökkenőmentes CAD-fájlkezeléssel.
weight: 11
url: /hu/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportáljon beágyazott DGN-t PDF-be az Aspose.CAD for Java segítségével

## Bevezetés

Üdvözöljük ebben az átfogó oktatóanyagban a beágyazott DGN-fájlok Aspose.CAD for Java használatával történő exportálásával kapcsolatban. Az Aspose.CAD egy hatékony könyvtár, amely lehetővé teszi a Java fejlesztők számára, hogy zökkenőmentesen dolgozzanak CAD fájlokkal. Ebben az oktatóanyagban lépésről lépésre végigvezetjük a beágyazott DGN-fájlok PDF-formátumba exportálásának folyamatán. Akár tapasztalt fejlesztő, akár most kezdő, ez az oktatóanyag segít az Aspose.CAD képességeinek kihasználásában Java-alkalmazásai fejlesztéséhez.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
- Java fejlesztői környezet: Győződjön meg arról, hogy be van állítva Java fejlesztői környezet a gépén.
-  Aspose.CAD for Java: Töltse le és telepítse az Aspose.CAD for Java könyvtárat innen[itt](https://releases.aspose.com/cad/java/).

## Csomagok importálása

kezdéshez importálnia kell a szükséges csomagokat a Java projektbe. Adja hozzá a következő importálási utasításokat a kódhoz:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Most bontsuk fel a példakódot több lépésre:

## 1. lépés: Állítsa be a bemeneti és kimeneti útvonalakat

Határozza meg a könyvtár elérési útját, ahol a dokumentum található, és adja meg a bemeneti DWG fájl nevét.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## 2. lépés: Töltse be a DWG fájlt

 Töltse be a DWG fájlt egy`Image` objektumot az Aspose.CAD használatával.

```java
Image objImage = Image.load(fileName);
```

## 3. lépés: Konfigurálja a raszterezési beállításokat

Konfigurálja a raszterezési beállításokat, például az exportálásba bevonandó elrendezéseket.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## 4. lépés: Konfigurálja a PDF-beállításokat

Állítsa be a PDF-beállításokat, beleértve a vektorraszterezési beállításokat is.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 5. lépés: Mentse el a PDF fájlt

Mentse el a PDF-fájlt a beállított opciókkal.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Következtetés

Gratulálunk! Sikeresen exportált egy beágyazott DGN-fájlt PDF-be az Aspose.CAD for Java használatával. Ez az oktatóanyag az Aspose.CAD Java-alkalmazásba történő integrálásának alapvető lépéseit ismerteti a hatékony CAD-fájlkezelés érdekében.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for Java-t kereskedelmi projektekben?

 1. válasz: Igen, az Aspose.CAD for Java egy kereskedelmi könyvtár. Engedélyt szerezhet be[itt](https://purchase.aspose.com/buy).

### 2. kérdés: Van ingyenes próbaverzió?

 2. válasz: Igen, hozzáférhet az Aspose.CAD for Java ingyenes próbaverziójához[itt](https://releases.aspose.com/).

### 3. kérdés: Hogyan kaphatok támogatást az Aspose.CAD for Java számára?

3. válasz: Kérhet támogatást az Aspose.CAD közösségtől a webhelyen[fórum](https://forum.aspose.com/c/cad/19).

### 4. kérdés: Mi a teendő, ha ideiglenes engedélyre van szükségem?

 V4: Kaphat ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Hol találom a dokumentációt?

 V5: A dokumentáció elérhető[itt](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
