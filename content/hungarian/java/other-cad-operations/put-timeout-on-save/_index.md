---
title: Időtúllépés a CAD-mentésnél az Aspose.CAD segítségével
linktitle: Állítsa be az időtúllépést a Mentés lehetőségre
second_title: Aspose.CAD Java API
description: Ismerje meg, hogyan javíthatja Java-alkalmazása teljesítményét az Aspose.CAD segítségével. Tegyen időtúllépést a CAD-rajzok mentésére. Kövesse lépésenkénti útmutatónkat.
type: docs
weight: 15
url: /hu/java/other-cad-operations/put-timeout-on-save/
---
## Bevezetés

Üdvözöljük az Aspose.CAD for Java használatával történő mentés időtúllépésének oktatóanyagában. Ebben az útmutatóban végigvezetjük a CAD-rajzok mentéséhez szükséges időtúllépés beállításának folyamatán, hogy javítsa alkalmazása teljesítményét. Az Aspose.CAD for Java egy hatékony könyvtár, amely lehetővé teszi, hogy zökkenőmentesen dolgozzon a Java-alkalmazásokban lévő CAD-fájlokkal.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:
-  Aspose.CAD for Java Library: Győződjön meg arról, hogy az Aspose.CAD for Java könyvtár integrálva van a projektjébe. A könyvtár letölthető a[weboldal](https://releases.aspose.com/cad/java/).
- Fejlesztői környezet: Állítsa be Java fejlesztői környezetét az összes szükséges eszközzel és függőséggel.

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat a Java projektbe. Adja hozzá a következő sorokat a Java fájl elejéhez:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Most bontsuk le a példakódot lépésről lépésre:

## 1. lépés: Állítsa be a forrás- és kimeneti könyvtárakat

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Győződjön meg arról, hogy a megfelelő forrás- és kimeneti könyvtárakkal rendelkezik a CAD-rajzokhoz.

## 2. lépés: Hozzon létre megszakítási token forrást

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicializáljon egy megszakítási token-forrást a mentési művelet közbeni megszakítások kezelésére.

## 3. lépés: Töltse be a CAD-rajzot

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Töltse be a CAD rajzot a`CadImage` tárgy.

## 4. lépés: Konfigurálja a raszterezési beállításokat

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurálja a raszterezési beállításokat a CAD-rajzhoz.

## 5. lépés: Konfigurálja a PDF-beállításokat

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Állítsa be a PDF-beállításokat a vektorraszterezési beállításokkal és a megszakítási tokennel.

## 6. lépés: Mentse el a rajzot időtúllépéssel

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Mentse el a CAD-rajzot PDF-fájlba a megadott időtúllépéssel.

## 7. lépés: Kezelje a megszakítást

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

Hozzon létre egy szálat a mentési művelet kezeléséhez, és szakítsa meg azt egy megadott időkorlát után.

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan állíthat be időtúllépést a mentéshez az Aspose.CAD for Java használatával. Ez a funkció nagymértékben növelheti a CAD-hez kapcsolódó alkalmazások hatékonyságát.

## GYIK

### 1. kérdés: Hogyan tölthetem le az Aspose.CAD for Java-t?

 V1: Letöltheti a[kiadások oldala](https://releases.aspose.com/cad/java/).

### 2. kérdés: Hol találom az Aspose.CAD for Java dokumentációját?

 A2: Lásd a[dokumentáció](https://reference.aspose.com/cad/java/) átfogó tájékoztatásért.

### 3. kérdés: Van ingyenes próbaverzió?

3. válasz: Igen, ingyenes próbaverziót kaphat a webhelyről[ez a link](https://releases.aspose.com/).

### 4. kérdés: Hogyan szerezhetek ideiglenes engedélyt?

 A4: Látogassa meg[itt](https://purchase.aspose.com/temporary-license/) az ideiglenes engedély részleteiért.

### 5. kérdés: Segítségre van szüksége, vagy kérdései vannak?

 A5: Menjen át a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásért.