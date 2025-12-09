---
date: 2025-11-30
description: Tanulja meg, hogyan adhat hozzá egyedi tulajdonságokat DWG fájlokhoz
  Java-ban az Aspose.CAD használatával. Javítsa a CAD-rajzok szervezését és az információk
  lekérdezését könnyedén.
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: Egyedi tulajdonságok hozzáadása DWG fájlokhoz az Aspose.CAD for Java használatával
url: /hu/java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Egyedi tulajdonságok hozzáadása DWG fájlokhoz az Aspose.CAD for Java használatával

A CAD rajzok programozott módon történő manipulálása mindennapi szükséglet sok Java fejlesztő számára. Ebben az útmutatóban megtudja, **hogyan adjon hozzá egyedi tulajdonságokat DWG** fájlokhoz a hatékony Aspose.CAD for Java könyvtár használatával. A útmutató végére egy újrahasználható kódrészletet kap, amely közvetlenül a DWG fájl fejlécébe injektál metaadatokat, megkönnyítve a rajzok katalogizálását, keresését és karbantartását.

## Introduction

Az Aspose.CAD for Java egy teljesen menedzselt, .NET‑mentes könyvtár, amely lehetővé teszi a CAD formátumok széles skálájának olvasását, szerkesztését és írását AutoCAD nélkül. Egyedi tulajdonságok hozzáadása egy DWG fájlhoz könnyű módot biztosít további információk – például projektkódok, revíziójegyzetek vagy tulajdonos adatok – tárolására közvetlenül a rajzfájlban.

## Quick Answers
- **Mi jelent a “add custom properties dwg”?** Ez azt jelenti, hogy felhasználó által definiált név/érték párokat szúr be egy DWG fájl fejléc metaadataiba.  
- **Melyik könyvtár kezeli ezt?** Azose.CAD for Java egyszerű API-t biztosít ezeknek a tulajdonságoknak a olvasásához és írásához.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 5‑10 perc egy alap példához.  
- **Szükségem van licencre?** A fejlesztéshez egy ingyenes próba verzió elegendő; a termeléshez kereskedelmi licenc szükséges.  
- **Kompatibilis más CAD formátumokkal?** Igen – a DXF, DWF és további formátumok támogatottak.

## What is Adding Custom Properties to DWG Files?

Az egyedi tulajdonságok kulcs‑érték párok, amelyek a DWG fejlécben tárolódnak. Nem jelennek meg a rajz geometriájában, de bármely CAD‑tudatos alkalmazás hozzáférhet, lehetővé téve a jobb adatkezelést, az automatizált jelentéskészítést és a PLM rendszerekkel való integrációt.

## Why Use Aspose.CAD for This Task?

- **Nincs AutoCAD függőség** – bármely operációs rendszeren vagy CI pipeline-ban működik.  
- **Teljes körű API** – olvasás, módosítás és mentés a pontosság megőrzése nélkül.  
- **Nagy teljesítmény** – nagy rajzokat dolgoz fel másodpercek alatt.  
- **Keresztformátum támogatás** – ugyanaz a kód működik DXF, DWF és egyéb formátumoknál.

## Prerequisites

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

- **Java Development Kit (JDK) 8+** telepítve és konfigurálva az IDE-jében.  
- **Aspose.CAD for Java** könyvtárral – töltse le a legújabb JAR-t a [Aspose.CAD letöltési oldalról](https://releases.aspose.com/cad/java/).  
- Egy **példa DWG/DXF fájllal** a kísérletezéshez (az útmutató a `conic_pyramid.dxf` fájlt használja).

## Import Namespaces

Adja hozzá a szükséges importokat a Java osztályához, hogy az Aspose.CAD objektumokkal dolgozhasson.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## Step‑by‑Step Guide

### Step 1: Set Up Your Project

Hozzon létre egy új Maven/Gradle projektet (vagy egy egyszerű IDE projektet), és helyezze az Aspose.CAD JAR-t a classpath-ra. Ez biztosítja, hogy a `com.aspose.cad.*` csomagok elérhetők legyenek fordítási időben.

### Step 2: Define File Paths

Adja meg, hogy hol található a forrásrajz, és hová kell írni a módosított fájlt.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### Step 3: Load the DWG File

Használja a statikus `Image.load` metódust a rajz `CadImage` objektumba történő beolvasásához.

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### Step 4: Add Custom Properties

Illessze be a metaadatait közvetlenül a rajz fejlécébe. Minden hívás egy új név/érték párt ad hozzá.

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **Tip:** Tartsa a tulajdonságneveket röviden (max 31 karakter) és kerüljön el szóközöket a régebbi CAD megjelenítők kompatibilitásának megőrzése érdekében.

### Step 5: Save the Modified DWG File

Mentse el a változtatásokat a `save` hívással. A kimeneti fájl most már tartalmazza a hozzáadott egyedi tulajdonságokat.

```java
cadImage.save(outFile);
```

### Step 6: Execute the Code

Futtassa a programot az IDE-jéből vagy a parancssorból. Ha minden helyesen van beállítva, egy megerősítő üzenetet fog látni.

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## Common Issues & Solutions

| Probléma | Valószínű ok | Megoldás |
|----------|--------------|----------|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | Az Aspose.CAD JAR nincs a classpath-on | Adja hozzá a JAR-t a projekt `libs` mappájához, vagy deklarálja Maven/Gradle-ban. |
| **A tulajdonságok nem jelennek meg a mentett fájlban** | DWG verzió használata, amely nem támogatja az egyedi tulajdonságokat | Győződjön meg róla, hogy DWG/DXF 2000 vagy újabb verzióval dolgozik; a régebbi formátumok figyelmen kívül hagyhatják az egyedi fejléceket. |
| **`OutOfMemoryError` on large files** | Nagyon nagy rajz betöltése streaming nélkül | `Image.load` használata `LoadOptions` objektummal, amely memóriahatékony betöltést tesz lehetővé. |

## Frequently Asked Questions

**Q: Hozzáadhatok egyedi tulajdonságokat más CAD fájlformátumokhoz?**  
A: Igen. Az Aspose.CAD for Java támogatja a DXF, DWF, DGN és egyéb formátumokat, és ugyanaz a `getHeader().getCustomProperties()` API működik ezeken a formátumokon.

**Q: Az Aspose.CAD for Java kompatibilis minden főbb IDE-vel?**  
A: Teljes mértékben. Működik Eclipse, IntelliJ IDEA, NetBeans, és még egyszerű parancssori build-ekkel is.

**Q: Hol találok további példákat és részletes dokumentációt?**  
A: Látogassa meg a hivatalos [Aspose.CAD Java API Reference](https://reference.aspose.com/cad/java/) oldalt a teljes osztály-, metódus- és mintaprojektlistáért.

**Q: Kipróbálhatom az Aspose.CAD for Java-t vásárlás előtt?**  
A: Igen – töltsön le egy ingyenes 30‑napos próba verziót a [Aspose.CAD letöltési oldalról](https://releases.aspose.com/).

**Q: Hogyan kaphatok támogatást, ha nehézségekbe ütközöm?**  
A: Az Aspose közösségi fórum és a dedikált [Aspose.CAD támogatási portál](https://forum.aspose.com/c/cad/19) nagyszerű helyek kérdések feltevésére és megoldások megosztására.

---

**Utoljára frissítve:** 2025-11-30  
**Tesztelve:** Aspose.CAD for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}