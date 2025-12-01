---
date: 2025-12-01
description: Ismerje meg, hogyan állíthatja be a PDF oldal méretét, konvertálhatja
  a DWG-t PDF-be, és engedélyezheti a DWG változások nyomon követését az Aspose.CAD
  for Java használatával.
language: hu
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: PDF oldalméret beállítása és DWG nyomon követése az Aspose.CAD Java-val
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF oldalméret beállítása és DWG nyomon követése az Aspose.CAD Java-val

## Bevezetés

CAD projektek közös munkája során gyakran szükség van a **PDF oldalméret beállítására** a konzisztens elrendezés érdekében, a **DWG PDF‑re konvertálására**, és a rajzon végrehajtott minden változás nyomon követésére. Az Aspose.CAD for Java mindezt egyetlen, egyszerűsített munkafolyamatban teszi lehetővé. Ebben az útmutatóban lépésről lépésre bemutatjuk, hogyan **állítsuk be a PDF oldalméretet**, engedélyezzük a **DWG változások nyomon követését**, és exportáljuk a rajzot PDF‑ként – mindezt Java‑val.

## Gyors válaszok
- **Hogyan állíthatom be a PDF oldalméretet?** Használja a `CadRasterizationOptions.setPageWidth()` és `setPageHeight()` metódusokat az exportálás előtt.  
- **Nyomon követhetem a változásokat exportálás közben?** Igen – valósítson meg egy egyedi `CadRenderHandler`‑t a nyomon követési eredmények rögzítéséhez.  
- **Melyik metódus konvertálja a DWG‑t PDF‑re?** Hívja a `image.save(stream, pdfOptions)`‑t a beállítások konfigurálása után.  
- **Mik a fő előfeltételek?** JDK, Aspose.CAD for Java, és egy mappa DWG/DXF fájlokkal.  
- **Szükséges licenc a termeléshez?** Igen, egy érvényes Aspose.CAD licenc szükséges a nem‑próba környezetekhez.

## Mi az a „PDF oldalméret beállítása a DWG exportálás kontextusában?

A PDF oldalméret beállítása meghatározza a létrejövő PDF vászon méreteit (szélesség × magasság pixelben). Ez akkor elengedhetetlen, ha azt szeretné, hogy az exportált rajz egy adott papírmérethez vagy képernyőelrendezéshez illeszkedjen, biztosítva, hogy minden elem pontosan a várt helyen jelenjen meg.

## Miért engedélyezzük a nyomon követést DWG fájlok exportálásakor?

A nyomon követés (vagy változás‑követés) rögzíti a konverzió során felmerülő renderelési problémákat, hiányzó betűtípusokat vagy nem támogatott entitásokat. Ennek az információnak a rögzítésével a következőket teheti:
- Gyorsan azonosíthatja a végső szállítás előtt javítandó problémákat.
- Világos visszajelzést adhat a csapattagoknak arról, mi változott vagy mi került kihagyásra.
- Audit nyomvonalat tart fenn a szigorú szabályozású iparágak számára.

## Előfeltételek

- **Java Development Kit (JDK)** – bármely friss verzió (8+).  
- **Aspose.CAD for Java** – töltse le a hivatalos [Aspose CAD letöltési oldalról](https://releases.aspose.com/cad/java/).  
- **Document Directory** – egy mappa, amely a feldolgozni kívánt DWG/DXF fájlokat tartalmazza.

## Névterek importálása

Kezdje a szükséges Aspose.CAD osztályok és a standard Java I/O osztályok importálásával.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## 1. lépés: DWG (vagy DXF) fájl betöltése

Töltse be a forrásrajzot egy `Image` objektumba. Állítsa be az elérési utat a saját könyvtárára.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 2. lépés: PDF exportálási beállítások konfigurálása (beleértve az oldalméretet)

Itt állítjuk be a PDF opciókat, és kifejezetten **beállítjuk a PDF oldalméretet** 800 × 600 pixelre. Itt kerül alkalmazásra a fő kulcsszó.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## 3. lépés: Nyomon követés megvalósítása

Hozzon létre egy egyedi hibakezelőt, amely a konverziós folyamat során nyomon követési információkat kap.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 4. lépés: Exportálás PDF‑be

A beállítások és a nyomon követési kezelő megadása után exportálja a rajzot. Ez a lépés **DWG‑t PDF‑re konvertál** (vagy a példánkban DXF‑t PDF‑re).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 5. lépés: CadRenderHandler osztály – Nyomon követési eredmények rögzítése

Az `ErrorHandler` osztály kiterjeszti a `CadRenderHandler`‑t, és kiír minden renderelési problémát, amely a **DWG fájlok változásainak nyomon követése** közben történt.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Megoldás |
|----------|------------------|----------|
| **Hiányzó betűtípusok** | A CAD fájl olyan betűtípusokra hivatkozik, amelyek nincsenek telepítve a szerveren. | Telepítse a szükséges betűtípusokat, vagy ágyazza be őket a forrásrajzba. |
| **Nem támogatott entitások** | Bizonyos DWG entitásokat még nem támogat az Aspose.CAD. | Használja a nyomon követési kimenetet az azonosításukhoz, és egyszerűsítse a rajzot. |
| **Helytelen oldalméret** | Az exportálás előtt nem hívták meg a `setPageWidth/Height` metódusokat. | Győződjön meg róla, hogy a fenti módon be van állítva a `CadRasterizationOptions`‑ban az oldalméret. |

## Gyakran Ismételt Kérdések

### Q1: Engedélyezhetem a nyomon követést más CAD fájlformátumokhoz az Aspose.CAD for Java használatával?

A1: Az Aspose.CAD elsősorban a DWG/DXF fájlok nyomon követését támogatja. Más formátumok esetén tekintse meg a hivatalos dokumentációt, hogy milyen funkciók állnak rendelkezésre.

### Q2: Hogyan kezelhetem a további exportálási beállításokat az Aspose.CAD for Java-ban?

A2: A könyvtár számos beállítást kínál, például DPI, háttérszín és vektor rasterizálás. Tekintse meg ezeket a [Aspose.CAD Java Dokumentációban](https://reference.aspose.com/cad/java/).

### Q3: Elérhető próba verzió az Aspose.CAD for Java-hoz?

A3: Igen, letölthet egy ingyenes próbaverziót a [Aspose.CAD Free Trial](https://releases.aspose.com/) oldalról.

### Q4: Hol kérhetek segítséget vagy vitathatok kérdéseket az Aspose.CAD for Java-val kapcsolatban?

A4: A közösségi fórum a [Aspose.CAD fórumon](https://forum.aspose.com/c/cad/19) kiváló hely kérdések feltevésére és tapasztalatok megosztására.

### Q5: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for Java-hoz?

A5: Kövesse a [Temporary License](https://purchase.aspose.com/temporary-license/) oldalon leírt lépéseket, hogy időkorlátos licencet kérjen kiértékeléshez.

### Q6: Tudok **DWG‑t PDF‑re konvertálni** a rétegek megőrzése mellett?

A6: Igen. A `CadRasterizationOptions` konfigurálásával megőrizheti a réteginformációkat a létrehozott PDF‑ben.

### Q7: Mi a legjobb módja a **DWG PDF‑ként történő exportálásának** egyedi oldalméretekkel?

A7: Állítsa be a kívánt szélességet és magasságot a `setPageWidth` és `setPageHeight` használatával, mielőtt meghívná a `image.save()`‑t – pontosan úgy, ahogy a 2. lépésben bemutattuk.

## Összegzés

A fenti lépések követésével **beállíthatja a PDF oldalméretet**, **DWG‑t PDF‑re konvertálhat**, és **nyomon követheti a DWG fájlok változásait** az Aspose.CAD for Java segítségével. Ez a munkafolyamat teljes irányítást biztosít a kimeneti elrendezés felett, miközben értékes diagnosztikát nyújt, amely a CAD együttműködést zökkenőmentessé és hibamentessé teszi. Nyugodtan fedezze fel a további renderelési beállításokat, és integrálja ezt a kódot nagyobb automatizálási csővezetékekbe.

---

**Utoljára frissítve:** 2025-12-01  
**Tesztelve:** Aspose.CAD for Java 24.12 (a legújabb a kiadás időpontjában)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}