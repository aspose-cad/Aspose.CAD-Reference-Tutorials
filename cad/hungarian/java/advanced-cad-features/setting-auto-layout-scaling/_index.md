---
date: 2026-08-29
description: Ismerje meg, hogyan állíthat be egyedi PDF oldalméretet, és hozhat létre
  PDF-et CAD-ből az Aspose.CAD for Java használatával. Ez a lépésről‑lépésre útmutató
  bemutatja a CAD PDF-be exportálását Auto Layout Scaling segítségével.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Auto Layout Scaling beállítása
og_description: Állítson be egyedi PDF oldalméretet a CAD fájlok PDF-re konvertálásakor
  az Aspose.CAD for Java segítségével. Kövesse a lépésről‑lépésre útmutatót az Auto
  Layout Scaling használatához, és érjen el tökéletes elrendezési eredményeket.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: Egyedi PDF oldalméret beállítása a CAD PDF exportáláshoz – Aspose.CAD Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: Hogyan állítsunk be egyedi PDF oldalméretet a CAD PDF exportáláshoz
url: /hu/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Állíts be egyedi PDF oldalméretet – PDF létrehozása CAD-ből automatikus elrendezésméretezéssel

## Bevezetés

Ha **egyedi PDF oldalméretet** kell beállítanod, miközben **PDF-et hozol létre CAD** fájlokból gyorsan és tökéletes méretezéssel, az Aspose.CAD for Java megoldja ezt. Az Auto Layout Scaling automatikusan átméretezi a CAD elrendezéseket, hogy kitöltsék a céloldal méreteit, biztosítva, hogy a létrehozott PDF a kívánt lapmérettel egyezzen a forrásrajz függetlenül. Ebben az útmutatóban végigvezetünk a teljes folyamaton – a DXF fájl betöltésétől a PDF exportálásáig – miközben kiemeljük a könyvtár **export CAD to PDF** képességeit, és megmutatjuk, hogyan **konvertálhatsz DWG-t PDF-be** vagy **növelheted a PDF felbontását**, ha szükséges.

## Gyors válaszok
- **Mi a Auto Layout Scaling funkciója?** Automatikusan átméretezi a CAD elrendezéseket, hogy a rasterizálás során illeszkedjenek a céloldal méreteihez.  
- **Milyen CAD formátumokat konvertálhatok?** Bármely, az Aspose.CAD által támogatott formátum (pl. DXF, DWG, DWF) konvertálható PDF‑be.  
- **Szükségem van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges nem‑értékelő használathoz.  
- **Mennyi időt vesz igénybe egy tipikus konverzió?** Modern hardveren egy szabványos fájl másodperc alatt konvertálódik.  
- **Megváltoztathatom az oldalméretet?** Természetesen – használja a `CadRasterizationOptions`‑t egyedi oldalméretek beállításához.

## Mi az a „PDF létrehozása CAD-ből”?

A PDF létrehozása CAD-ből azt jelenti, hogy egy vektoralapú mérnöki rajzot (DXF, DWG stb.) rasterizálunk egy PDF dokumentummá. A PDF megőrzi az eredeti rajz vizuális hűségét, miközben széles körben megtekinthető bármely platformon, és megnyitható olyan eszközökön is, amelyek nem támogatják a natív CAD formátumokat.

## Miért használjuk az automatikus elrendezésméretezést?

Az Auto Layout Scaling garantálja, hogy minden elrendezés teljesen kitöltse a PDF oldalt manuális számítások nélkül, időt takarítva meg és kiküszöbölve a méretezési hibákat. Emellett biztosítja, hogy a vonalvastagságok és színek pontosan megmaradjanak különböző kimeneti méretek között. Következetes, magas minőségű kimenetet biztosít tucatnyi CAD fájl esetén, és támogatja a kötegelt feldolgozást nagy projektekhez.

## Előfeltételek

1. **Aspose.CAD for Java Library** – töltse le a legújabb verziót a [download page](https://releases.aspose.com/cad/java/) oldalról.  
2. **Resource directory** – hozzon létre egy mappát a gépén a CAD fájlok tárolásához; cserélje le a kódban a `"Your Document Directory"` értéket erre az útvonalra.  
3. **Sample CAD file** – ebben az útmutatóban a `conic_pyramid.dxf` fájlt használjuk, amely az Aspose mintaadatkészletben megtalálható.

## Névterek importálása

Először importálja a szükséges osztályokat. Ez hozzáférést biztosít a képbetöltéshez, rasterizáláshoz és a PDF exportálási funkciókhoz.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hogyan állítsunk be egyedi oldalméretet PDF-hez CAD-ből

Mielőtt belemerülnénk a lépésről‑lépésre kódba, tisztázzuk, miért fontosak az egyedi oldalméretek. Egy **egyedi pdf oldalméret** beállítása lehetővé teszi, hogy megfeleljen ipari szabványú lapméreteknek (A4, A1, Letter), vagy egyedi vásznat definiáljon, ami elengedhetetlen szabályozási benyújtásokhoz, műszaki kézikönyvekhez vagy nagy felbontású nyomtatási feladatokhoz.

### 1. lépés: CAD fájl betöltése

A forrásfájl betöltése az első lépés a **CAD exportálásához PDF dokumentumba**.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 2. lépés: rasterizálási beállítások létrehozása

A `CadRasterizationOptions` osztály meghatározza, hogyan kerül rasterizálásra a CAD rajz, és mely oldalméreteket használja. Emellett lehetővé teszi a DPI, a háttérszín és egyéb megjelenítési részletek szabályozását.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 3. lépés: automatikus elrendezésméretezés beállítása

Engedélyezze az automatikus méretezési funkciót. Ez a **hogyan állítsuk be a méretezést** a CAD‑PDF konverzióhoz.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### 4. lépés: PDF beállítások létrehozása

Kösse össze a rasterizálási beállításokat a PDF exportálási opciókkal.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 5. lépés: exportálás PDF-be

Végül mentse a renderelt képet PDF fájlként. Ez a lépés fejezi be a **convert dxf to pdf** munkafolyamatot.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ismételje meg a fenti lépéseket minden további CAD fájl esetén, amelyet feldolgozni szeretne, legyen az **DWG**, **DWF**, vagy más támogatott formátum.

## Gyakori felhasználási esetek

| Szenárió | Miért állítsunk be egyedi oldalméretet? |
|----------|------------------------------------------|
| **Építési rajz benyújtása** | Az PDF-et a szabályozó hatóságok által megkövetelt standard A1/A2 lapméretekkel igazítja. |
| **Beágyazás műszaki kézikönyvekbe** | Biztosítja, hogy a rajz a kézikönyv előre meghatározott elrendezésébe illeszkedjen további méretezés nélkül. |
| **Nagy felbontású nyomtatás** | Lehetővé teszi a DPI növelését (pl. `rasterizationOptions.setResolution(300)`) miközben az oldalméretek konzisztens maradnak. |

## Gyakori problémák és hibaelhárítás

| Tünet | Valószínű ok | Megoldás |
|---------|--------------|-----|
| Üres PDF kimenet | A rasterizálási beállítások nincsenek megadva vagy a fájl útvonala helytelen | Ellenőrizze a `srcFile` útvonalat és győződjön meg arról, hogy a `setPageWidth/Height` nem nulla |
| Torz méretezés | `setAutomaticLayoutsScaling` `false` értéken maradt | Engedélyezze az automatikus méretezést vagy számolja ki manuálisan a méretezési tényezőt |
| Hiányzó rétegek | A forrás DXF nem támogatott entitásokat tartalmaz | Tekintse meg az Aspose.CAD kiadási megjegyzéseit a támogatott entitástípusokért |

Az Aspose.CAD támogatja **30+ CAD formátum** konvertálását, és akár **500 MB** méretű fájlokat is képes feldolgozni a teljes dokumentum memóriába betöltése nélkül, gyors, memóriahatékony konverziókat biztosítva vállalati terhelésekhez.

## Gyakran feltett kérdések

**Q: Az Aspose.CAD for Java kompatibilis minden CAD fájlformátummal?**  
A: Az Aspose.CAD for Java széles körű formátumot támogat, beleértve a DWG, DXF, DWF és több mint 30 további CAD típust.

**Q: Testreszabhatom a méretezési beállításokat tovább?**  
A: Igen, a `CadRasterizationOptions` osztály tulajdonságokat biztosít a méretezés, DPI, háttérszín és egyéb rasterizálási beállítások finomhangolásához.

**Q: Hol találok további dokumentációt az Aspose.CAD for Java-hoz?**  
A: Tekintse meg a [documentation](https://reference.aspose.com/cad/java/) oldalt a részletes információkért és példákért.

**Q: Elérhető ingyenes próba az Aspose.CAD for Java-hoz?**  
A: Igen, felfedezhet egy [free trial](https://releases.aspose.com/) lehetőséget, hogy megtapasztalja az Aspose.CAD for Java képességeit.

**Q: Hogyan kérhetek segítséget vagy vehetünk részt a beszélgetésekben az Aspose.CAD for Java-ról?**  
A: Látogassa meg az [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) oldalt, hogy csatlakozzon a közösséghez és segítséget kérjen.

**További gyakori kérdések**

**Q: Hogyan konvertálhatok DWG fájlt PDF-be a DXF helyett?**  
A: Ugyanaz a kód működik; csak változtassa meg a `srcFile` fájlkiterjesztését `.dwg`‑re.

**Q: Beállíthatok egyedi DPI-t a magasabb felbontású PDF-ekhez?**  
A: Igen, használja a `rasterizationOptions.setResolution(300);` (vagy bármilyen szükséges DPI).

**Q: Lehet betűtípusokat beágyazni a generált PDF-be?**  
A: Az Aspose.CAD rasterizálja a rajzot, így a betűtípusok vektorokként jelennek meg; külön betűtípus beágyazás nem szükséges.

## Következtetés

Ezzel az útmutatóval már tudja, hogyan **állíts be egyedi pdf oldalméretet** és **hozzon létre PDF-et CAD fájlokból** az Aspose.CAD for Java segítségével Auto Layout Scaling használatával. A folyamat egyszerűsíti a **export CAD to PDF** munkafolyamatot, biztosítja a konzisztens méretezést, és értékes fejlesztési időt takarít meg. Nyugodtan kísérletezzen különböző oldalméretekkel, felbontásokkal és CAD formátumokkal, hogy megfeleljen projektigényeinek, legyen szó **DWG PDF-be konvertálásáról**, **PDF felbontás növeléséről**, vagy egy **java CAD to PDF** kötegelt feldolgozó építéséről.

---

**Utoljára frissítve:** 2026-08-29  
**Tesztelve ezzel:** Aspose.CAD for Java 24.12 (legújabb)  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Hogyan állítsuk be a PDF oldalméretet és engedélyezzük a nyomon követést a CAD renderelési folyamat során az Aspose.CAD for Java használatával](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [PDF oldalméret beállítása – CAD konvertálása PDF-be (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Gyors DWG exportálás PDF-be vagy rasterként a java CAD könyvtár Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}