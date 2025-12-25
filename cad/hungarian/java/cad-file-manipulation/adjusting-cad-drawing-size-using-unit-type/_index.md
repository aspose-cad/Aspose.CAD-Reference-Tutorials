---
date: 2025-12-25
description: Ismerje meg, hogyan exportálhat DWG fájlt BMP‑be az Aspose.CAD for Java
  segítségével. Ez a lépésről‑lépésre útmutató bemutatja a CAD rajz méretének beállítását
  és a CAD BMP‑be történő hatékony konvertálását.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG exportálása BMP-be – CAD méret beállítása egységtípus szerint (Java)
url: /hu/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG exportálása BMP‑be – CAD rajz méretének beállítása egységtípus használatával az Aspose.CAD for Java segítségével

## Introduction

Amikor **DWG‑t BMP‑be kell exportálni**, a kimeneti méret és a mértékegység szabályozása elengedhetetlen a további feldolgozáshoz vagy nyomtatáshoz. Ebben az útmutatóban megtanulja, hogyan állíthatja be a CAD rajz méretét és konvertálhatja a CAD‑ot BMP‑be az Aspose.CAD for Java használatával, a `UnitType` tulajdonság segítségével a mértékegység meghatározásához. A lépéseket egyszerű nyelven magyarázzuk, így még a könyvtár újdonságai számára is könnyen követhető.

## Quick Answers
- **Mit jelent a „export DWG to BMP”?** A DWG rajz BMP raszteres képpé konvertálása.  
- **Melyik tulajdonság szabályozza a kimeneti méretet?** A `CadRasterizationOptions.setUnitType()` állítja be az egységet (pl. centiméter).  
- **Szükség van licencre a kód futtatásához?** Egy ingyenes próba verzió elegendő értékeléshez; licenc szükséges a termeléshez.  
- **Választhatók más elrendezések?** Igen, a `setLayouts()` használatával megadható modell vagy papírtér elrendezés.  
- **Milyen kimeneti formátumok támogatottak?** A BMP mellett PNG, JPEG, TIFF stb. exportálható a beállítási osztály módosításával.

## What is **export DWG to BMP**?

A DWG‑t BMP‑be exportálni azt jelenti, hogy egy vektor‑alapú DWG fájlt bitmap (BMP) képpé rasterizálunk. Ez akkor hasznos, amikor pixel‑pontos ábrázolásra van szükség régi rendszerek, képfeldolgozó csővezetékek vagy egyszerű megjelenítési helyzetek esetén.

## Why adjust CAD drawing size with **Unit Type**?

Az egységtípus beállítása lehetővé teszi a exportált kép fizikai méretének szabályozását anélkül, hogy manuálisan kellene számolni a skálázási tényezőket. Ez biztosítja, hogy a bitmap megfeleljen a valós méréseknek (pl. centiméter), ami kulcsfontosságú a mérnöki rajzok és a nyomtatott dokumentáció esetén.

## Prerequisites

Mielőtt elkezdené a gyakorlati példát, ellenőrizze, hogy a következő előfeltételek teljesülnek:

- **Java fejlesztői környezet** – működő JDK (8 vagy újabb) és egy IDE vagy build eszköz (Maven/Gradle).  
- **Aspose.CAD for Java könyvtár** – töltse le és integrálja az Aspose.CAD könyvtárat a Java projektjébe. A könyvtárat [itt](https://releases.aspose.com/cad/java/) szerezheti be.

## Import Namespaces

A Java kódban importálja a szükséges névtereket az Aspose.CAD funkciók eléréséhez. Adja hozzá a következő importokat:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Most bontsuk le a CAD rajz méretének egységtípus szerinti beállítását kezelhető lépésekre:

## Step 1: Define Data Directory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Állítsa be azt az elérési utat, ahol a CAD fájlok találhatók.

## Step 2: Load CAD Drawing

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Töltse be a CAD rajzot az Aspose.CAD `Image` osztályával.

## Step 3: Create BMP Options

```java
BmpOptions bmpOptions = new BmpOptions();
```

Hozza létre a `BmpOptions` osztályt a CAD elrendezés BMP formátumba történő exportálásához.

## Step 4: Configure Rasterization Options

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Hozzon létre egy `CadRasterizationOptions` példányt, és kapcsolja össze a `BmpOptions`-sal a vektor rasterizálásához.

## Step 5: Set Unit Type

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Adja meg a kívánt egységtípust a CAD rajzhoz. Ebben a példában **Centimeter**‑re állítottuk, ami közvetlenül befolyásolja az exportált kép méretét, amikor **a CAD rajz méretét állítja be**.

## Step 6: Set Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Határozza meg az exportálás során figyelembe veendő elrendezéseket. Ebben az esetben a **"Model"** elrendezést választottuk, de szükség esetén átválthat papírtér elrendezésekre is.

## Step 7: Export to BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Végül mentse el a módosított CAD rajzot BMP formátumban. Ez a lépés fejezi be a **DWG‑t BMP‑be exportálás** munkafolyamatot, miközben megőrzi a beállított méretkorrekciókat.

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **Output image is too small** | Unit type not set or default (pixel) used | Call `setUnitType()` with the desired measurement (e.g., `UnitType.Centimeter`). |
| **Wrong layout exported** | Layout name typo | Verify layout names with a CAD viewer; use exact string in `setLayouts()`. |
| **License exception** | Running without a valid license in production | Apply a temporary or permanent license as described in the FAQ. |

## Frequently Asked Questions (Extended)

**Q: Can I use Aspose.CAD for Java with other programming languages?**  
A: Aspose.CAD primarily supports Java, but there are versions available for other languages like .NET.

**Q: Are there any licensing options for Aspose.CAD?**  
A: Yes, you can explore licensing options and purchase Aspose.CAD [here](https://purchase.aspose.com/buy).

**Q: Is there a free trial available for Aspose.CAD?**  
A: Certainly, you can access a free trial [here](https://releases.aspose.com/).

**Q: How can I get support for Aspose.CAD for Java?**  
A: Visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for comprehensive support.

**Q: Can I obtain a temporary license for Aspose.CAD?**  
A: Yes, you can acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}