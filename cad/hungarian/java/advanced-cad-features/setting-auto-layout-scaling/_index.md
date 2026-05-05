---
date: 2026-02-15
description: Tanulja meg, hogyan állíthat be egyedi oldalméretet, és hozhat létre
  PDF-et CAD-ből az Aspose.CAD for Java használatával. Ez a lépésről‑lépésre útmutató
  bemutatja a CAD PDF‑be exportálását automatikus elrendezésméretezéssel.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Egyéni oldalméret beállítása – PDF CAD-ből automatikus elrendezés méretezéssel
url: /hu/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Egyéni oldalméret beállítása – PDF létrehozása CAD-ből automatikus elrendezésméretezéssel

## Introduction

Ha gyorsan és tökéletes méretezéssel kell **egyéni oldalméretet beállítania**, miközben **PDF-et hoz létre CAD** fájlokból, az Aspose.CAD for Java megoldást nyújt. Az Auto Layout Scaling automatikusan beállítja az elrendezés méreteit, így a létrehozott PDF pontosan úgy néz ki, ahogy elvárható, függetlenül az eredeti CAD oldalmérettől. Ebben az útmutatóban végigvezetjük a teljes folyamaton – a DXF fájl betöltésétől a PDF exportálásáig – kiemelve a könyvtár **export CAD to PDF** képességeit, és bemutatva, hogyan **konvertálhat DWG-t PDF-be** vagy **növelheti a PDF felbontását** szükség esetén.

## Quick Answers
- **Mi a Auto Layout Scaling feladata?** Automatikusan átméretezi a CAD elrendezéseket, hogy illeszkedjenek a céloldal méreteire rasterizáláskor.
- **Mely formátumokat konvertálhatom?** Bármely, az Aspose.CAD által támogatott formátum (pl. DXF, DWG, DWF) konvertálható PDF-be.
- **Szükségem van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges a nem‑értékelő használathoz.
- **Mennyi ideig tart a konvertálás?** Általában egy másodpercnél kevesebb a szokásos fájlok esetén modern hardveren.
- **Módosíthatom az oldalméretet?** Igen, egyéni oldalméreteket állíthat be a `CadRasterizationOptions` segítségével.

## What is “create PDF from CAD”?

A PDF létrehozása CAD-ből azt jelenti, hogy egy vektor‑alapú mérnöki rajzot (DXF, DWG stb.) rasterizálunk egy PDF dokumentummá. A PDF megőrzi az eredeti rajz vizuális hűségét, miközben bármely platformon széles körben megtekinthető.

## Why use Auto Layout Scaling?

- **Következetes kimenet:** Biztosítja, hogy minden elrendezés kitöltse a PDF oldalt manuális méret számítások nélkül.
- **Időmegtakarítás:** Megszünteti a manuális méretezési tényezők minden egyes rajzhoz való beállításának szükségességét.
- **Magas minőség:** Megőrzi a vonalvastagságot és a geometriai pontosságot a konvertálás során.
- **Rugalmasság:** Alkalmazható **convert dxf to pdf**, **convert dwg to pdf** esetén, és még akkor is, ha **növelni kell a PDF felbontását** nyomtatásra kész fájlokhoz.

## Prerequisites

1. **Aspose.CAD for Java Library** – töltse le a legújabb verziót a [download page](https://releases.aspose.com/cad/java/) oldalról.  
2. **Resource Directory** – hozzon létre egy mappát a gépén a CAD fájlok tárolásához; a kódban cserélje le a `"Your Document Directory"` értéket a megfelelő útvonalra.  
3. **Sample CAD File** – ebben az útmutatóban a `conic_pyramid.dxf` fájlt használjuk, amely az Aspose mintaadatkészletben található.

## Import Namespaces

Először importálja a szükséges osztályokat. Ez hozzáférést biztosít a kép betöltéséhez, rasterizáláshoz és a PDF exportálási funkciókhoz.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to Set Custom Page Size for PDF from CAD

Mielőtt belemerülnénk a lépésről‑lépésre kódba, értsük meg, miért fontos az egyéni oldalméret beállítása. Amikor **egyéni oldalméretet állít be**, a létrehozott PDF fizikai méreteit szabályozza (pl. A4, Letter vagy egyedi méret). Ez elengedhetetlen a mérnöki munkafolyamatokban, ahol a rajzoknak meg kell felelniük a lap szabványoknak, vagy amikor a PDF-et nagyobb dokumentumokba kell beágyazni.

### Step 1: Load the CAD File

A forrásfájl betöltése az első lépés a **how to export CAD** PDF-dokumentummá alakításában.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Step 2: Create Rasterization Options

Határozza meg a céloldal méreteit. Ezt a blokkot használhatja arra is, hogy manuálisan **set CAD page size** egyedi elrendezés esetén.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 3: Set Auto Layout Scaling

Engedélyezze az automatikus méretezési funkciót. Ez a **how to set scaling** CAD‑PDF konvertálásának központja.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Step 4: Create PDF Options

Kapcsolja össze a rasterizálási beállításokat a PDF export opciókkal.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Export to PDF

Végül mentse a renderelt képet PDF fájlként. Ez a lépés fejezi be a **convert dxf to pdf** munkafolyamatot.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ismételje meg a fenti lépéseket minden további CAD fájlra, amelyet feldolgozni szeretne, legyen az **DWG**, **DWF**, vagy más támogatott formátum.

## Common Use Cases

| Scenario | Why set a custom page size? |
|----------|-----------------------------|
| **Construction drawing submission** | A PDF-et a szabályozó hatóságok által előírt A1/A2 szabványos lapméretekkel igazítja. |
| **Embedding in technical manuals** | Biztosítja, hogy a rajz a kézikönyv előre meghatározott elrendezésébe illeszkedjen további méretezés nélkül. |
| **High‑resolution printing** | Lehetővé teszi a DPI növelését (pl. `rasterizationOptions.setResolution(300)`) miközben az oldalméretek konzisztens maradnak. |

## Common Issues & Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterizálási beállítások nincsenek megadva vagy a fájl útvonal hibás | Ellenőrizze a `srcFile` útvonalat és győződjön meg róla, hogy a `setPageWidth/Height` nem nulla |
| Distorted scaling | `setAutomaticLayoutsScaling` `false` értéken maradt | Engedélyezze az automatikus méretezést vagy számolja ki manuálisan a méretezési tényezőt |
| Missing layers | A forrás DXF nem támogatott entitásokat tartalmaz | Ellenőrizze az Aspose.CAD kiadási megjegyzéseit a támogatott entitástípusokért |

## Frequently Asked Questions

**Q: Az Aspose.CAD for Java kompatibilis minden CAD fájlformátummal?**  
A: Az Aspose.CAD for Java számos CAD formátumot támogat, beleértve a DWG, DXF és DWF formátumokat.

**Q: Testreszabhatom a méretezési beállításokat tovább?**  
A: Igen, a `CadRasterizationOptions` osztály tulajdonságokat biztosít a méretezés, DPI és egyéb rasterizálási beállítások finomhangolásához.

**Q: Hol találok további dokumentációt az Aspose.CAD for Java-hoz?**  
A: Tekintse meg a [documentation](https://reference.aspose.com/cad/java/) oldalt a részletes információkért és példákért.

**Q: Elérhető ingyenes próba az Aspose.CAD for Java-hoz?**  
A: Igen, egy [free trial](https://releases.aspose.com/) keretében kipróbálhatja az Aspose.CAD for Java képességeit.

**Q: Hogyan kérhetek segítséget vagy vehet részt a beszélgetésekben az Aspose.CAD for Java-ról?**  
A: Látogassa meg az [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) oldalt, hogy csatlakozzon a közösséghez és segítséget kérjen.

**Additional Common Questions**

**Q: Hogyan konvertálhatok DWG fájlt PDF-be a DXF helyett?**  
A: Ugyanaz a kód működik; csak változtassa meg a `srcFile` kiterjesztését `.dwg`-re.

**Q: Beállíthatok egyedi DPI-t a magasabb felbontású PDF-ekhez?**  
A: Igen, használja a `rasterizationOptions.setResolution(300);` (vagy a kívánt DPI értéket).

**Q: Lehetséges betűtípusokat beágyazni a generált PDF-be?**  
A: Az Aspose.CAD rasterizálja a rajzot, így a betűtípusok vektorokként jelennek meg; külön betűtípus beágyazásra nincs szükség.

## Conclusion

Ezzel az útmutatóval most már tudja, hogyan **állíthat be egyéni oldalméretet** és **hozhat létre PDF-et CAD-ből** az Aspose.CAD for Java segítségével Auto Layout Scaling használatával. A folyamat egyszerűsíti a **export CAD to PDF** munkafolyamatot, biztosítja a konzisztens méretezést, és értékes fejlesztési időt takarít meg. Nyugodtan kísérletezzen különböző oldalméretekkel, felbontásokkal és CAD formátumokkal, hogy megfeleljen projektigényeinek, legyen szó **DWG konvertálásáról PDF-be**, **PDF felbontás növeléséről**, vagy egy **java CAD to PDF** kötegelt feldolgozó építéséről.

---

**Legutóbb frissítve:** 2026-02-15  
**Tesztelve:** Aspose.CAD for Java 24.12 (legújabb)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}