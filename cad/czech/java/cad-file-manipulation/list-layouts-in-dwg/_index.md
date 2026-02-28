---
date: 2026-02-28
description: Naučte se číst soubory DWG pomocí Aspose.CAD pro Javu a bez námahy vypsat
  layouty v souborech DWG. Integrujte výkonnou CAD funkčnost do svých Java aplikací.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Jak načíst DWG a vypsat rozvržení v DWG pomocí Aspose.CAD pro Javu
url: /cs/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

 content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak číst DWG a vypsat rozvržení v DWG pomocí Aspose.CAD pro Java

## Úvod

Pokud hledáte spolehlivý způsob **jak číst dwg** soubory programově, Aspose.CAD pro Java poskytuje čisté, multiplatformní API, které vám umožní načíst výkres a získat jakékoli potřebné informace – například názvy všech rozvržení v souboru. V tomto krok‑za‑krokem tutoriálu vám ukážeme **jak číst DWG** a vypsat každé rozvržení obsažené v souboru DWG (nebo DXF), abyste tuto funkci mohli integrovat do jakékoli Java aplikace pracující s CAD daty.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.CAD pro Java.  
- **Mohu číst DWG soubory na libovolném OS?** Ano – Java je multiplatformní, takže můžete **read dwg on linux** stejně snadno jako na Windows.  
- **Potřebuji licenci pro spuštění ukázky?** Bezplatná zkušební verze stačí pro hodnocení; licence je vyžadována pro produkční nasazení.  
- **Jaké CAD formáty jsou podporovány?** DWG, DXF, DWF a další.  
- **Je kód kompatibilní s Java 8+?** Naprosto.

## Co je „how to read dwg“ v Javě?

Čtení DWG souboru znamená načtení binárních CAD dat do objektového modelu, který můžete dotazovat. Aspose.CAD abstrahuje složitou strukturu DWG za jednoduché Java třídy, což vám umožní soustředit se na informace, které potřebujete – v tomto případě na názvy rozvržení.

## Proč vypsat rozvržení v souboru DWG?

DWG může obsahovat více rozvržení (paper space, model space, vlastní listy). Znalost názvů rozvržení vám umožní:

- Generovat zprávy pro jednotlivá rozvržení.  
- Exportovat konkrétní rozvržení do obrázků nebo PDF.  
- Automatizovat hromadné zpracování výkresů.  

## Požadavky

Než se pustíme do kódu, ujistěte se, že máte následující:

- **Aspose.CAD pro Java Library** – stáhněte nejnovější JAR z [webové stránky](https://releases.aspose.com/cad/java/).  
- **Java Development Environment** – JDK 8 nebo vyšší a IDE nebo nástroj pro sestavování dle vašeho výběru.

## Importovat jmenné prostory

Ve vašem Java zdrojovém souboru importujte požadované třídy Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nahraďte **“Your Document Directory”** absolutní cestou, kde jsou uloženy vaše CAD soubory. Na Linuxu můžete použít cestu jako `/home/user/cad/`.

## Krok 2: Načtěte soubor DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Metoda `Image.load` automaticky detekuje formát souboru, takže stejný kód funguje pro soubory **DWG** i **DXF**.

## Krok 3: Získejte rozvržení a vytiskněte názvy

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Smyčka prochází každým objektem rozvržení a vypisuje jeho název do konzole – jednoduchý způsob, jak ověřit, že jste úspěšně **read DWG** a získali informace o rozvrženích.

## Jak převést DWG na PDF na Linuxu

Pokud později potřebujete převést konkrétní rozvržení na PDF, Aspose.CAD může rozvržení vykreslit do obrázku a poté můžete použít Aspose.PDF (nebo libovolnou jinou PDF knihovnu) k vložení tohoto obrázku do PDF dokumentu. Kód pro konverzi je na Linuxu stejný, protože API je čistě Java.

## Časté úskalí a tipy

- **Incorrect file path** – Ověřte, že `dataDir` končí oddělovačem (`/` nebo `\\`) vhodným pro váš OS.  
- **Unsupported DWG version** – Ujistěte se, že používáte aktuální verzi Aspose.CAD; starší verze DWG mohou vyžadovat konverzi.  
- **Memory usage** – Velké výkresy mohou spotřebovat značnou paměť. Uvolněte objekt `CadImage` po dokončení: `cadImage.dispose();`.  
- **Running on headless servers** – UI komponenty nejsou potřeba, takže kód funguje na Linux serverech bez grafického prostředí.

## Závěr

Gratulujeme! Nyní víte **jak číst dwg** a vypsat jeho rozvržení pomocí Aspose.CAD pro Java. Tato technika tvoří základ pro pokročilejší CAD automatizaci, jako je export konkrétních rozvržení do obrázků, PDF nebo dokonce převod DWG na PDF na Linuxu. Pro hlubší průzkum se podívejte na oficiální [dokumentaci](https://reference.aspose.com/cad/java/).

## Často kladené otázky

**Q1: Mohu použít Aspose.CAD pro Java s jinými CAD formáty?**  
A1: Ano, Aspose.CAD podporuje různé CAD formáty, včetně DWG, DXF, DWF a dalších.

**Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Java?**  
A2: Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

**Q3: Kde mohu získat komunitní podporu pro Aspose.CAD pro Java?**  
A3: Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) pro komunitní podporu.

**Q4: Jak si mohu zakoupit licenci pro Aspose.CAD pro Java?**  
A4: Licenci můžete zakoupit na [stránce nákupu](https://purchase.aspose.com/buy).

**Q5: Mohu použít dočasnou licenci pro testovací účely?**  
A5: Ano, dočasnou licenci získáte [zde](https://purchase.aspose.com/temporary-license/).

**Další otázky**

**Q: Funguje tento přístup pro čtení DWG souborů na Linuxu?**  
A: Naprosto. Protože je řešení čistě Java, běží na libovolném OS s kompatibilní JDK.

**Q: Mohu číst DWG soubor bez načtení celého výkresu do paměti?**  
A: Aspose.CAD načítá výkres do paměti; u velmi velkých souborů zvažte jejich zpracování v samostatných vláknech nebo použití streaming API, pokud bude v budoucích verzích k dispozici.

**Q: Existuje způsob, jak filtrovat rozvržení podle názvu?**  
A: Ano – po získání `CadLayoutDictionary` můžete před zpracováním zkontrolovat `layout.getLayoutName().equalsIgnoreCase("MyLayout")`.

**Poslední aktualizace:** 2026-02-28  
**Testováno s:** Aspose.CAD pro Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}