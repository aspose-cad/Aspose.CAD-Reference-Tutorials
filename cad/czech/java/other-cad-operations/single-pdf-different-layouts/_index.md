---
date: 2026-01-22
description: Naučte se vytvářet PDF z CAD výkresů, převádět DWG do PDF a přizpůsobovat
  velikost stránky PDF pomocí Aspose.CAD pro Javu.
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Jak vytvořit PDF z CAD výkresů pomocí Aspose.CAD pro Javu
url: /cs/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

 na PDF**, exportovat složitý CAD soubor nebo použít **vlastní velikost PDF stránky**, níže uvedené, pomocí několika řádků Java kódu.

## Rychlé odpovědi
- **Co dělá Aspose.CAD?** Umožňuje vývojářům Java načítat, manipulovat a exportovat CAD výkresy do formátů jako PDF.
- **Mohu exportovat více rozvržení do jednoho PDF?** Ano, úpravou velikostí stránek rozvržení před uložením.
- **Které CAD formáty jsou podporovány?** DWG, DXF, DWF, DGN a mnoho dalších.
- **Potřebuji licenci pro produkci?** Dočasná licence funguje pro testování; pro komerční použití je vyžadována plná licence.
- **Jaká verze Javy je vyžadována?** Java 8 nebo novější.

## Co znamená „vytvořit PDF z CAD“?
Vytvoření PDF z CAD znamená rasterizaci vektorových CAD výkresů do pevně definovaného dokumentu (PDF), který lze zobrazit na jakémkoli zařízení bez potřeby CAD softwaru. To je ideální pro sdílení návrhů, tisk výkresů nebo archivaci inženýrské práce.

## Proč používat Aspose.CAD pro Java?
- **Žádné externí závislosti** – čistá Java, žádné nativní DLL soubory.
- **Detailní kontrola** nad možnostmi rasterizace, jako je DPI, velikost stránky a výběr rozvržení.
- **Dávkové zpracování** – zpracování mnoha výkresů v jednom běhu.
- **Přesná konverze** – zachovává tloušťky čar, barvy a vrstvy.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

- **Java prostředí** – nainstalovaný JDK 8 nebo novější.
- **Knihovna Aspose.CAD** – Stáhněte a nainstalujte knihovnu Aspose.CAD pro Java z [odkazu ke stažení](https://releases.aspose.com/cad/java/).
- **Adresář dokumentů** – Složka obsahující DWG (nebo jiné CAD) výkresy, které chcete převést.

## Import balíčků

Ve svém Java projektu importujte potřebné třídy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Průvodce krok za krokem

### Krok 1: Načtení CAD výkresu

Nejprve načtěte zdrojový CAD soubor (např. DWG) do objektu `CadImage`. Toto je vstupní bod pro jakoukoli operaci **export CAD to PDF**.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Krok 2: Nastavení možností rasterizace

Definujte, jak mají být CAD data rasterizována. Zde nastavujeme základní šířku a výšku stránky, které budou použity pro rozvržení bez vlastní velikosti.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Krok 3: Přizpůsobení velikostí stránek rozvržení

Pokud potřebujete **vlastní velikost PDF stránky**, přidejte položky pro každé rozvržení, které má být zahrnuto v konečném PDF. To vám umožní **převést DWG na PDF** s různými rozměry pro jednotlivá rozvržení.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Krok 4: Nastavení PDF možností

Spojte nastavení rasterizace s PDF‑specifickými možnostmi. Vlastnost `VectorRasterizationOptions` říká Aspose.CAD, aby použil velikosti rozvržení, které jsme právě definovali.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Uložení jako PDF

Nakonec exportujte CAD výkres do jediného PDF souboru, který obsahuje všechna specifikovaná rozvržení. Tento krok **uloží CAD jako PDF** jedním voláním.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Tip:** Znovu použijte stejný objekt `PdfOptions`, pokud potřebujete exportovat více výkresů v dávce – snižuje to režii vytváření objektů.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Prázdné stránky v PDF výstupu** | Ověřte, že názvy rozvržení (`"ANSI C Plot"`, `"8.5 x 11 Plot"`) přesně odpovídají těm definovaným v CAD souboru. |
| **Nízké rozlišení výstupu** | Zvyšte DPI voláním `rasterizationOptions.setResolution(300);` před uložením. |
| **Licence nebyla použita** | Načtěte svou dočasnou nebo plnou licenci před jakýmkoli voláním Aspose.CAD: `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro Java s jinými Java knihovnami?
**A1:** Ano, Aspose.CAD pro Java je navrženo tak, aby se hladce integrovalo s ostatními Java knihovnami a poskytovalo rozsáhlou funkcionalitu.

### Q2: Je k dispozici zkušební verze?
**A2:** Rozhodně! Bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

### Q3: Kde mohu najít další podporu?
**A3:** Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuze.

### Q4: Jak získat dočasnou licenci?
**A4:** Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu zakoupit plnou verzi?
**A5:** Plnou verzi Aspose.CAD pro Java můžete zakoupit [zde](https://purchase.aspose.com/buy).

---

**Poslední aktualizace:** 2026-01-22  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}