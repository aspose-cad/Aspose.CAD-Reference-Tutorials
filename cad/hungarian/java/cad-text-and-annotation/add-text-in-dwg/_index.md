---
date: 2025-12-28
description: Tanulja meg, hogyan hozhat létre PDF-et DWG‑ből, menthet DWG‑t PDF‑ként,
  és adhat szöveget DWG‑rajzokhoz az Aspose.CAD for Java‑val – lépésről‑lépésre útmutató.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: PDF létrehozása DWG‑ből és szöveg hozzáadása az Aspose.CAD for Java segítségével
url: /hu/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF létrehozása DWG-ből és szöveg hozzáadása az Aspose.CAD for Java segítségével

## Bevezetés

Ha **PDF-et szeretne létrehozni DWG** fájlokból, miközben egyedi szöveget is beillesztene, jó helyen jár. Ebben az útmutatóban végigvezetjük a teljes folyamaton – a DWG rajz betöltésén, egy szöveges annotáció hozzáadásán, és végül az eredmény PDF-ként történő mentésén az Aspose.CAD for Java használatával. A végére megérti, hogyan **save DWG as PDF**, testre szabhatja a szövegmagasságot, és akár alapvető annotációkat is hozzáadhat.

## Gyors válaszok
- **Átalakíthatom a DWG-t PDF-re Java-ban?** Igen, az Aspose.CAD for Java egyszerű API-t biztosít.  
- **Szükségem van licencre a termeléshez?** Kereskedelmi licenc szükséges; ingyenes próba elérhető.  
- **Melyik metódus ad szöveget a DWG-hez?** Használja a `CadText` objektumot és adja hozzá a modell térhez.  
- **Beállíthatom a szövegmagasságot?** Természetesen—használja a `setTextHeight()`-t a `CadText` példányon.  
- **Vektor‑alapú a kimenet?** Ha a rasterizálási beállítások `UseObjectColor` értékre vannak állítva, a PDF megőrzi a magas minőségű vektor adatot.

## Előkövetelmények

Mielőtt belemerülne az útmutatóba, győződjön meg róla, hogy a következő előkövetelmények rendelkezésre állnak:

- Aspose.CAD for Java könyvtár: Töltse le és telepítse a könyvtárat a [Aspose.CAD for Java oldalról](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Győződjön meg róla, hogy a legújabb JDK telepítve van a rendszerén.
- DWG rajz: Készítsen elő egy DWG rajzfájlt, amelyhez szöveget szeretne hozzáadni.

## Névterek importálása

A Java kódban importálja a szükséges névtereket az Aspose.CAD-hez:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Most bontsuk le a megadott kódrészletet több lépésre:

## 1. lépés: Dokumentum könyvtár és DWG fájl útvonal beállítása

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

## 4. lépés: Szöveg hozzáadása a CadImage-hez (annotáció beszúrása)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 5. lépés: PDF beállítások konfigurálása (PDF létrehozása DWG-ből)

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

## 7. lépés: Módosított DWG mentése PDF-ként (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Ezeket a lépéseket követve képes lesz **PDF-et létrehozni DWG-ből**, egyedi szöveget hozzáadni, és a szövegmagasságot szabályozni – mindezt csak néhány Java sorral.

## Miért érdemes szöveget hozzáadni a DWG-hez és PDF-be konvertálni?

A szöveg közvetlen hozzáadása egy DWG fájlhoz hasznos:

- **Megjegyzések hozzáadása** a tervekhez jegyzetekkel vagy alkatrész számokkal.
- **Nyomtatható dokumentáció készítése**, ahol a PDF csak olvasható, széles körben támogatott formátum.
- **Kötegelt feldolgozás automatizálása** nagy CAD könyvtárak esetén manuális szerkesztés nélkül.

## Gyakori problémák és tippek

- **A szöveg nem jelenik meg?** Ellenőrizze, hogy az X/Y koordináták a rajz kiterjedésén belül vannak-e, és hogy a réteg látható-e.
- **Helytelen szövegmagasság?** Állítsa be a `setTextHeight()`-t; az érték a rajz egységrendszerében van.
- **A PDF rasterizáltnak tűnik?** Győződjön meg róla, hogy a `CadDrawTypeMode.UseObjectColor` be van állítva a vektor információk megtartásához.
- **Teljesítmény nagy fájloknál?** Növelje a `pageHeight`/`pageWidth` értékeket csak szükség szerint; a nagyobb értékek több memóriát fogyasztanak.

## Gyakran ismételt kérdések

**Q: Az Aspose.CAD kompatibilis minden DWG verzióval?**  
A: Az Aspose.CAD különböző DWG verziókat támogat, biztosítva a kompatibilitást a széles körű CAD szoftverekkel.

**Q: Testreszabhatom a hozzáadott szöveg betűtípusát és formázását?**  
A: Igen, az Aspose.CAD segítségével testreszabhatja a betűtípust, stílust és egyéb formázási beállításokat a DWG fájlokhoz hozzáadott szöveghez.

**Q: Elérhető ingyenes próba az Aspose.CAD for Java-hoz?**  
A: Igen, az Aspose.CAD funkcióit egy ingyenes próba letöltésével ismerheti meg [itt](https://releases.aspose.com/).

**Q: Hol találom az Aspose.CAD for Java részletes dokumentációját?**  
A: A részletes információkért és példákért tekintse meg a dokumentációt [itt](https://reference.aspose.com/cad/java/).

**Q: Hogyan kaphatok támogatást vagy segítséget az Aspose.CAD-hez?**  
A: Látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19), ahol segítséget kaphat és csatlakozhat a közösséghez.

---

**Utolsó frissítés:** 2025-12-28  
**Tesztelve:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}