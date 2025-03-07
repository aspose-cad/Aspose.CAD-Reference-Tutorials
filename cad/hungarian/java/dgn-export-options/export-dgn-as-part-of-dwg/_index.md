---
title: DGN exportálása DWG-be az Aspose.CAD for Java segítségével
linktitle: DGN exportálása a DWG részeként
second_title: Aspose.CAD Java API
description: Fedezze fel, hogyan exportálhat DGN-t a DWG részeként az Aspose.CAD for Java segítségével. Kövesse lépésről lépésre útmutatónkat a hatékony CAD-fájlok kezeléséhez.
weight: 10
url: /hu/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN exportálása DWG-be az Aspose.CAD for Java segítségével

## Bevezetés

Ebben az oktatóanyagban megvizsgáljuk, hogyan használhatja az Aspose.CAD for Java-t DGN (MicroStation Design) fájl exportálására DWG (AutoCAD rajz) fájl részeként. Az Aspose.CAD egy hatékony könyvtár, amely átfogó funkcionalitást biztosít a CAD fájlformátumokkal való munkavégzéshez. Ez a lépésenkénti útmutató segít megérteni a DGN-exportálás folyamatát a DWG részeként Java használatával.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:
1. Aspose.CAD Library: Töltse le és telepítse a Java Aspose.CAD könyvtárat. Megtalálhatod a könyvtárat[itt](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Győződjön meg arról, hogy a Java telepítve van a rendszeren.
3. Integrált fejlesztői környezet (IDE): Válasszon egy Java IDE-t, például az Eclipse-t vagy az IntelliJ-t a gördülékenyebb fejlesztési élmény érdekében.

## Csomagok importálása

Java-projektjében importálja a szükséges Aspose.CAD csomagokat a CAD-fájlok kezelésének engedélyezéséhez. Íme egy példa:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 1. lépés: Állítsa be a fájl elérési útját

 Határozza meg a DWG fájl bemeneti és kimeneti fájljának elérési útját. Frissítse a`dataDir`, `fileName` , és`outPath` változókat ennek megfelelően.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 2. lépés: PdfOptions példány létrehozása

 Hozzon létre egy példányt a`PdfOptions` osztályba, mivel a DWG fájlt PDF formátumba exportáljuk.

```java
PdfOptions exportOptions = new PdfOptions();
```

## 3. lépés: Töltse be a DWG fájlt

 Töltse be a meglévő DWG fájlt képként, és konvertálja a`CadImage` típus.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 4. lépés: Iterálás entitásokon keresztül

Menjen végig a DWG-fájlon belüli egyes entitásokon, és ellenőrizze, hogy képdefiníció-e. Ha igen, kérje le az objektum külső hivatkozását.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 5. lépés: Adja meg a raszterezési beállításokat

 Beállítások megadása a`CadRasterizationOptions`objektum, beleértve az oldal szélességét, magasságát, elrendezését és háttérszínét.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 6. lépés: Állítsa be a vektorraszterezési beállításokat

Állítsa be az exportálás vektorraszterezési beállításait.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 7. lépés: DWG exportálása PDF-be

 Végül exportálja a DWG fájlt PDF formátumba a`save` módszer.

```java
cadImage.save(outPath, exportOptions);
```

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan exportálhat DGN-fájlt DWG-fájl részeként az Aspose.CAD for Java segítségével. Ez a nagy teljesítményű könyvtár széleskörű lehetőségeket kínál a CAD-fájlokkal való munkavégzéshez, így a CAD-fájlkezelési feladatok hatékonyak és egyszerűek.

## GYIK

### 1. kérdés: Hol találom az Aspose.CAD for Java dokumentációját?

 V1: A dokumentáció megtalálható[itt](https://reference.aspose.com/cad/java/).

### 2. kérdés: Hogyan tölthetem le az Aspose.CAD könyvtárat Java számára?

 2. válasz: A könyvtárat innen töltheti le[ez a link](https://releases.aspose.com/cad/java/).

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.CAD for Java számára?

 V3: Igen, megtalálja az ingyenes próbaverziót[itt](https://releases.aspose.com/).

### 4. kérdés: Hol szerezhetek ideiglenes licencet az Aspose.CAD for Java számára?

 V4: Szerezzen ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Segítségre van szüksége, vagy kérdései vannak?

 5. válasz: Látogassa meg az Aspose.CAD közösségi támogatási fórumot[itt](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
