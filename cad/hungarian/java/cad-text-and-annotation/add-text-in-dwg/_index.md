---
date: 2026-02-28
description: Ismerje meg, hogyan hozhat létre PDF-et DWG‑ből, menthet DWG‑t PDF‑ként,
  és adhat szöveget DWG‑rajzokhoz az Aspose.CAD for Java segítségével – lépésről lépésre
  útmutató.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: PDF létrehozása DWG‑ből és szöveg hozzáadása az Aspose.CAD for Java használatával
url: /hu/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF létrehozása DWG-ből és szöveg hozzáadása az Aspose.CAD for Java használatával

## Bevezetés

Ha **PDF-et szeretne létrehozni DWG** fájlokból, miközben egyedi szöveget is beillesztene, jó helyen jár. Ebben az útmutatóban végigvezetjük a teljes folyamaton – a DWG rajz betöltését, egy szöveges megjegyzés hozzáadását, majd a végeredmény PDF‑ként történő mentését az Aspose.CAD for Java segítségével. A végére megérti, hogyan **menthet DWG‑t PDF‑ként**, hogyan szabhatja testre a szövegmagasságot, és hogyan adhat hozzá egyszerű annotációkat.

## Gyors válaszok
- **Átalakíthatom a DWG-t PDF‑be Java‑ban?** Igen, az Aspose.CAD for Java egy egyszerű API‑t biztosít.  
- **Szükség van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges; ingyenes próba elérhető.  
- **Melyik metódus ad szöveget a DWG-hez?** Használja a `CadText` objektumot, és adja hozzá a modell térhez.  
- **Be tudom állítani a szövegmagasságot?** Természetesen – a `CadText` példányon hívja a `setTextHeight()`‑t.  
- **Vektor‑alapú lesz a kimenet?** Ha a rasterizálási beállítások `UseObjectColor`‑ra vannak állítva, a PDF megőrzi a magas minőségű vektor adatokat.

## Mi az a „PDF létrehozása DWG-ből”?
A PDF létrehozása egy DWG rajzból azt jelenti, hogy a natív CAD formátumot egy széles körben támogatott, csak‑olvasásra alkalmas dokumentummá konvertáljuk, miközben megőrizve az eredeti geometriát. Ez a konverzió elengedhetetlen, ha a terveket olyan érintettekkel kell megosztani, akiknek nincs CAD szoftverük.

## Miért használjuk az Aspose.CAD for Java‑t a DWG PDF‑be konvertálásához?
Az Aspose.CAD egy tisztán Java‑alapú megoldást kínál, amelyhez nincs szükség külső CAD telepítésre. Támogatja a **DWG‑t PDF‑re konvertálást**, megőrzi a vektor pontosságot, és lehetővé teszi, hogy programozottan annotációkat (például szöveget, méreteket vagy egyedi grafikákat) adjunk hozzá a konverzió előtt.

## Előfeltételek

Mielőtt elkezdené a gyakorlati részt, győződjön meg róla, hogy a következő előfeltételek teljesülnek:

- Aspose.CAD for Java könyvtár: Töltse le és telepítse a könyvtárat az [Aspose.CAD for Java oldalról](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Győződjön meg róla, hogy a legújabb JDK telepítve van a rendszerén.
- DWG rajz: Készítsen elő egy DWG fájlt, amelyhez szöveget szeretne hozzáadni.

## Névterek importálása

A Java kódban importálja a szükséges névtereket az Aspose.CAD‑hez:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Most bontsuk le a megadott kódrészletet több lépésre:

## 1. lépés: Dokumentumkönyvtár és DWG fájl útvonal beállítása

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 2. lépés: DWG kép betöltése

```java
Image image = Image.load(dwgPathToFile);
```

## 3. lépés: CadText objektum létrehozása (szöveg hozzáadása a DWG-hez)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## 4. lépés: Szöveg hozzáadása a CadImage‑hez (annotáció beszúrása)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 5. lépés: PDF beállítások előkészítése (PDF létrehozása DWG‑ből)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 6. lépés: CadRasterizationOptions konfigurálása (PDF renderelés vezérlése)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 7. lépés: Módosított DWG mentése PDF‑ként (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Ezeknek a lépéseknek a követésével képes lesz **PDF-et létrehozni DWG‑ből**, egyedi szöveget hozzáadni, és a szövegmagasságot szabályozni – mindezt csak néhány Java sorral.

## Hogyan konvertáljunk DWG‑t PDF‑be Java‑ban nagy mennyiségben?
Ha **tömegesen szeretne DWG‑t PDF‑re konvertálni**, csomagolja be a fenti kódot egy ciklusba, amely egy DWG‑rajzokkal teli mappán iterál. A `pageHeight`/`pageWidth` értékeket csak szükség esetén módosítsa, hogy alacsony maradjon a memóriahasználat, és minden fájlhoz használja ugyanazt a `PdfOptions` példányt a teljesítmény javítása érdekében.

## Gyakori problémák és tippek

- **A szöveg nem jelenik meg?** Ellenőrizze, hogy az X/Y koordináták a rajz kiterjedésein belül vannak-e, és hogy a réteg látható‑e.
- **Helytelen szövegmagasság?** Állítsa be a `setTextHeight()`‑t; az érték a rajz egységrendszerében van.
- **A PDF rasterizáltnak tűnik?** Győződjön meg róla, hogy a `CadDrawTypeMode.UseObjectColor` be van állítva a vektorinformációk megtartásához.
- **Teljesítmény nagy fájlok esetén?** A `pageHeight`/`pageWidth` értékeket csak szükség szerint növelje; a nagyobb értékek több memóriát igényelnek.

## Gyakran Ismételt Kérdések

**K: Az Aspose.CAD kompatibilis minden DWG verzióval?**  
V: Az Aspose.CAD különböző DWG verziókat támogat, így széles körű CAD szoftverrel kompatibilis.

**K: Testreszabhatom a hozzáadott szöveg betűtípusát és formázását?**  
V: Igen, a szöveg betűtípusát, stílusát és egyéb formázási beállításait testreszabhatja az Aspose.CAD használatával.

**K: Van ingyenes próba az Aspose.CAD for Java‑hoz?**  
V: Igen, a funkciókat ingyenes próba verzióval is kipróbálhatja [itt](https://releases.aspose.com/).

**K: Hol találok részletes dokumentációt az Aspose.CAD for Java‑hoz?**  
V: Tekintse meg a dokumentációt [itt](https://reference.aspose.com/cad/java/) a mélyebb információk és példák érdekében.

**K: Hogyan kaphatok támogatást vagy segítséget az Aspose.CAD‑hez?**  
V: Látogasson el az [Aspose.CAD fórumra](https://forum.aspose.com/c/cad/19), ahol segítséget és közösségi támogatást talál.

---

**Utoljára frissítve:** 2026-02-28  
**Tesztelt verzió:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}