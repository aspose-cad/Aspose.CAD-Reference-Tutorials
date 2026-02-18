---
date: 2026-01-07
description: Ismerje meg, hogyan exportálhat CAD-et PDF-be, és konvertálhat DGN-t
  PDF-be az Aspose.CAD for Java segítségével. Lépésről lépésre útmutató Java fejlesztőknek.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CAD exportálása PDF-be – Beágyazott DGN exportálása az Aspose.CAD for Java-val
url: /hu/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD exportálása PDF‑be – Beágyazott DGN exportálása az Aspose.CAD for Java segítségével

## Bevezetés

Ebben az útmutatóban megtanulja, **hogyan exportálhat CAD fájlokat PDF‑be** úgy, hogy egy beágyazott DGN fájlt magas minőségű PDF dokumentummá konvertál az Aspose.CAD for Java segítségével. Az Aspose.CAD egy robusztus könyvtár, amely a Java fejlesztőknek teljes kontrollt biztosít a CAD fájlok manipulálása felett, legyen szó **DGN‑ről PDF‑re konvertálásról**, **DWG‑ről PDF‑re konvertálásról**, vagy egyszerűen CAD rajzok más formátumokba történő rendereléséről. Kövesse az alábbi lépésről‑lépésre útmutatót, és percek alatt beépítheti ezt a funkciót alkalmazásaiba.

## Gyors válaszok
- **Mit jelent a „CAD exportálása PDF‑be”?** A CAD rajzok (DWG, DGN stb.) PDF fájlokká konvertálását jelenti, miközben megőrzi a vektoros minőséget.  
- **Melyik könyvtárat használja?** Aspose.CAD for Java.  
- **Szükség van licencre?** Licenc szükséges a termelési környezetben; ingyenes próbaverzió elérhető.  
- **Mik a fő előfeltételek?** Java fejlesztői környezet és az Aspose.CAD for Java JAR.  
- **Testreszabható a kimenet?** Igen – kiválaszthatja a layoutokat, beállíthatja a rasterizálási opciókat, és szabályozhatja a PDF beállításait.

## Mi az a „CAD exportálása PDF‑be”?
A CAD exportálása PDF‑be azt jelenti, hogy egy natív CAD fájlt (például DWG vagy DGN) PDF dokumentummá alakítunk, amely hűen tükrözi az eredeti geometriát. A PDF bármely platformon megtekinthető CAD szoftver nélkül, így ideális megosztásra, nyomtatásra vagy archiválásra.

## Miért használja az Aspose.CAD for Java‑t a DGN‑ről PDF‑re konvertáláshoz?
- **Nincsenek külső függőségek** – tisztán Java környezetben működik.  
- **Megőrzi a vektoradatokat** – a PDF-ek bármilyen zoomolásnál élesek maradnak.  
- **Finomhangolt vezérlés** – kiválaszthatja a konkrét layoutokat, beállíthatja a rasterizálási DPI‑t, és beágyazhat betűtípusokat.  
- **Vállalati szintű** – nagy fájlok, kötegelt feldolgozás és licencelési lehetőségek támogatása.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy a következők rendelkezésre állnak:

- **Java fejlesztői környezet** – telepített és konfigurált JDK 8 vagy újabb.  
- **Aspose.CAD for Java** – töltse le a legújabb JAR‑t innen: [here](https://releases.aspose.com/cad/java/).  

## Csomagok importálása

A kezdéshez importálja a szükséges osztályokat Java projektjébe. Adja hozzá a következő import nyilatkozatokat a forrásfájlhoz:

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

## Hogyan exportáljunk DGN‑t PDF‑be az Aspose.CAD for Java segítségével?

Az alábbi számozott útmutató pontosan bemutatja, hogyan konvertálhat egy beágyazott DGN fájlt (amely egy DWG‑ben van tárolva) PDF‑be.

### 1. lépés: Bemeneti és kimeneti útvonalak beállítása

Határozza meg a forrásfájlt tartalmazó könyvtárat, és adja meg azt a DWG‑t, amely a beágyazott DGN‑t tartalmazza.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 2. lépés: DWG fájl betöltése

Töltse be a DWG fájlt egy `Image` objektumba. Az Aspose.CAD automatikusan felismeri a beágyazott DGN adatokat.

```java
Image objImage = Image.load(fileName);
```

### 3. lépés: Rasterizálási beállítások konfigurálása

Válassza ki, mely layout(ok) kerüljenek a PDF‑be. Ebben a példában csak a **Model** layoutot exportáljuk.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 4. lépés: PDF beállítások konfigurálása

Csatolja a rasterizálási beállításokat a PDF export opciókhoz.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 5. lépés: PDF fájl mentése

Végül írja a PDF‑et a lemezre a konfigurált opciók használatával.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG‑ről PDF‑re konvertálás – egy további tipp

Ha a forrásfájl egy egyszerű DWG (beágyazott DGN nélkül), ugyanazt a kódot használhatja – csak módosítsa a `fileName` változót, hogy a kívánt DWG‑re mutasson. A rasterizálási és PDF opciók változatlanok maradnak, így egy konzisztens **DWG‑ről PDF‑re konvertálás** munkafolyamatot kap.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Üres PDF kimenet** | Layout név eltérés | Ellenőrizze, hogy a `setLayouts`‑nek átadott layout név pontosan megegyezik a forrásfájlban lévővel (kis‑nagybetű érzékeny). |
| **Licenc kivétel** | Próbaverzió licenc nélkül | Töltsön be egy érvényes Aspose.CAD licencet a kép betöltése előtt (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Fájl nem található** | Hibás `dataDir` útvonal | Használjon abszolút útvonalat, vagy ellenőrizze, hogy a relatív útvonal helyes‑e a projekt munkakönyvtárához képest. |
| **Alacsony felbontású grafika** | Alapértelmezett rasterizálási DPI alacsony | Állítsa be a `rasterizationOptions.setPageWidth/Height` vagy `setResolution` értékét a DPI növeléséhez. |

## Gyakran feltett kérdések

**K: Használhatom az Aspose.CAD for Java‑t kereskedelmi projektben?**  
V: Igen, az Aspose.CAD for Java egy kereskedelmi könyvtár. Licencet vásárolhat [itt](https://purchase.aspose.com/buy).

**K: Van ingyenes próbaverzió?**  
V: Igen, ingyenes próbaverzió elérhető [itt](https://releases.aspose.com/).

**K: Hol kaphatok támogatást az Aspose.CAD for Java‑hoz?**  
V: Támogatást kérhet az Aspose.CAD közösségtől a [forumon](https://forum.aspose.com/c/cad/19).

**K: Ha ideiglenes licencre van szükségem?**  
V: Ideiglenes licencet szerezhet [itt](https://purchase.aspose.com/temporary-license/).

**K: Hol találom a dokumentációt?**  
V: A dokumentáció elérhető [itt](https://reference.aspose.com/cad/java/).

## Összegzés

Most már tudja, hogyan **exportáljon CAD‑t PDF‑be**, különösen hogyan **konvertáljon DGN‑t PDF‑re**, és akár **DWG‑t PDF‑re** is az Aspose.CAD for Java segítségével. A fenti lépések követésével könnyedén integrálhat CAD‑PDF konverziót bármely Java‑alapú megoldásba, magas minőségű PDF‑eket biztosítva felhasználóinak anélkül, hogy további CAD szoftverre lenne szükség.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utoljára frissítve:** 2026-01-07  
**Tesztelt verzió:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose