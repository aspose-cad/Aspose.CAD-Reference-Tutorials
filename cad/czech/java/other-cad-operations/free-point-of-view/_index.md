---
title: Bezplatné vykreslování pohledu s Aspose.CAD pro Javu
linktitle: Volný úhel pohledu
second_title: Aspose.CAD Java API
description: Prozkoumejte sílu Aspose.CAD pro Java v tomto tutoriálu o dosažení bezplatného vykreslování úhlů pohledu pro výkresy CAD. Uvolněte potenciál Aspose.CAD.
weight: 14
url: /cs/java/other-cad-operations/free-point-of-view/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bezplatné vykreslování pohledu s Aspose.CAD pro Javu

## Úvod

Vítejte v "Free Point of View - Aspose.CAD for Java Tutorial." V tomto komplexním průvodci vás provedeme procesem využití Aspose.CAD pro Java k dosažení bezplatného vykreslování úhlů pohledu pro výkresy CAD. Aspose.CAD je výkonná Java knihovna, která poskytuje širokou škálu funkcí pro práci se soubory CAD (Computer-Aided Design). Výukový program se bude zabývat nezbytnými předpoklady, importem základních balíčků a rozdělením každého příkladu do podrobných průvodců.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
-  Knihovna Aspose.CAD for Java: Stáhněte a nainstalujte knihovnu Aspose.CAD for Java z[odkaz ke stažení](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovanou Java.

## Importujte balíčky

Chcete-li začít, importujte požadované balíčky do svého projektu Java. Na začátek souboru Java přidejte následující řádky kódu:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

Tyto balíčky jsou nezbytné pro práci se soubory CAD a přizpůsobení možností vykreslování.

Nyní rozdělme poskytnutý příklad do několika kroků:

## Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nahraďte "Your Document Directory" cestou k vašemu skutečnému adresáři dokumentů.

## Krok 2: Načtěte výkres CAD

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

Zadejte cestu k výkresu CAD a načtěte jej pomocí`Image` třída.

## Krok 3: Nakonfigurujte možnosti CAD rastrování

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

Přizpůsobte si možnosti rastrování CAD podle svých požadavků, jako je výška a šířka stránky.

## Krok 4: Nastavte JpegOptions

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Vytvořte instanci`JpegOptions` a přidružit jej k dříve nakonfigurovaným možnostem rasterizace.

## Krok 5: Definujte úhly rotace

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

Určete úhly natočení podél os X, Y a Z pro vykreslení volného úhlu pohledu.

## Krok 6: Uložte vykreslený obrázek

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

Uložte vykreslený obrázek se zadanými možnostmi na požadované místo.

Opakujte tyto kroky pro váš konkrétní případ použití a zajistěte si volné vykreslování pohledu pro vaše výkresy CAD.

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak implementovat bezplatné vykreslování pohledu pomocí Aspose.CAD for Java. Tento výukový program se zabýval základními kroky, od nastavení předpokladů až po přizpůsobení možností vykreslování a uložení výstupního obrazu.

## FAQ

### Q1: Mohu používat Aspose.CAD for Java na více platformách?

Odpověď 1: Ano, Aspose.CAD for Java je nezávislý na platformě a lze jej použít na různých operačních systémech.

### Q2: Existují nějaké možnosti licencování pro Aspose.CAD for Java?

 A2: Ano, můžete prozkoumat možnosti licencování a provést nákup[tady](https://purchase.aspose.com/buy).

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Kde najdu podporu pro Aspose.CAD pro Javu?

 A4: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q5: Jak mohu získat dočasnou licenci?

 A5: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
