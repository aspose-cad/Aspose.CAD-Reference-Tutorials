---
date: 2026-01-07
description: Naučte se, jak exportovat CAD do SVG pomocí Aspose.CAD pro Javu. Tento
  podrobný návod vám ukáže, jak převést DWG na SVG, nastavit barevný režim SVG a integrovat
  knihovnu do vašeho Java projektu.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Export CAD do SVG pomocí Aspose.CAD pro Java
url: /cs/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD do SVG pomocí Aspose.CAD pro Java

## Úvod

Vítejte ve světě Aspose.CAD pro Java, výkonné knihovny, která vývojářům umožňuje snadno manipulovat s CAD výkresy. Ať už jste zkušený vývojář nebo nováček v oblasti CAD, tento komplexní průvodce vás provede **exportem CAD do SVG** krok za krokem, ukáže vám, jak převést DWG na SVG, nastavit režim barev SVG a integrovat API do vašeho Java projektu.

## Rychlé odpovědi
- **Co znamená „export CAD do SVG“?** Převádí CAD výkres (např. DWG) do souboru Scalable Vector Graphics, který lze zobrazit v prohlížečích.  
- **Která knihovna provádí konverzi?** Aspose.CAD pro Java poskytuje jednoduché API pro tento úkol.  
- **Potřebuji licenci pro vývoj?** Pro testování stačí bezplatná zkušební verze; pro produkci je vyžadována komerční licence.  
- **Mohu ovládat výstupní barvy SVG?** Ano, můžete nastavit režim barev SVG (např. odstíny šedi).  
- **Je potřeba další software?** Pouze Java runtime a soubor Aspose.CAD JAR.

## Požadavky

Předtím, než se pustíte do tutoriálu, ujistěte se, že máte následující:

- Vývojové prostředí Java: Ověřte, že máte na svém systému nainstalovanou Javu.  
- Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Java z [odkazu ke stažení](https://releases.aspose.com/cad/java/).  
- Adresář dokumentů: Vytvořte adresář pro své CAD výkresy a poznamenejte si jeho cestu.

## Importovat jmenné prostory

V tomto kroku importujeme potřebné jmenné prostory, abychom zahájili naši cestu s Aspose.CAD. Postupujte podle následujících kroků:

### Krok 1: Otevřete svůj Java projekt
Otevřete svůj Java projekt v IDE dle vašeho výběru.

### Krok 2: Přidejte knihovnu Aspose.CAD
Přidejte knihovnu Aspose.CAD do svého projektu. To můžete provést zahrnutím JAR souboru do závislostí projektu.

### Krok 3: Importujte jmenné prostory
Ve své Java třídě importujte požadované jmenné prostory:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Export CAD do SVG

Nyní, když máme připravený základ, pojďme se ponořit do krok‑za‑krokem procesu **exportu CAD do SVG** pomocí Aspose.CAD pro Java.

### Krok 1: Zadejte adresář zdrojů
Definujte cestu k vašemu adresáři zdrojů, kde se nacházejí CAD výkresy:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Krok 2: Načtěte CAD výkres
Načtěte CAD výkres pomocí knihovny Aspose.CAD:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Krok 3: Nakonfigurujte možnosti exportu SVG
Nakonfigurujte možnosti exportu SVG pro přizpůsobení výstupu. Zde **nastavujeme režim barev SVG** na odstíny šedi a říkáme exportéru, aby převáděl text na tvary:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Krok 4: Uložte jako SVG
Uložte CAD výkres jako SVG soubor:

```java
image.save(dataDir + "meshes.svg");
```

> **Tip:** Pokud potřebujete **převést DWG na SVG** a zachovat barvy, změňte `SvgColorMode.Grayscale` na `SvgColorMode.FullColor`.

Gratulujeme! Úspěšně jste exportovali CAD výkres do SVG pomocí Aspose.CAD pro Java.

## Proč použít Aspose.CAD k exportu CAD do SVG?
- **Vysoká věrnost:** Vektorová data jsou zachována, což zajišťuje, že SVG vypadá přesně jako původní CAD výkres.  
- **Žádné externí závislosti:** Konverze probíhá kompletně v Java, což eliminuje potřebu dalších nástrojů.  
- **Přizpůsobitelný výstup:** Možnosti jako `setColorType` vám umožňují řídit, zda bude SVG ve stupních šedi nebo v plné barvě.

## Časté problémy a řešení
- **Soubor nenalezen:** Ověřte, že `dataDir` ukazuje na správný adresář a že název DWG souboru odpovídá.  
- **Prázdný SVG výstup:** Ujistěte se, že jste nastavili `options.setTextAsShapes(true)`, pokud výkres obsahuje text, který má být zobrazen jako tvary.  
- **Není podporován formát CAD:** Aspose.CAD podporuje DWG, DXF, DWF a několik dalších formátů; podívejte se do dokumentace pro úplný seznam.

## Závěr

V tomto tutoriálu jsme prozkoumali bezproblémový proces využití Aspose.CAD pro Java k **exportu CAD do SVG**. Díky intuitivnímu API a robustním funkcím Aspose.CAD zjednodušuje složité úkoly a poskytuje vývojářům univerzální nástroj pro manipulaci s CAD.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro Java s jinými formáty CAD?

A1: Ano, Aspose.CAD podporuje různé CAD formáty, včetně DWG, DXF, DWF a dalších.

### Q2: Je Aspose.CAD vhodný jak pro začátečníky, tak pro zkušené vývojáře?

A2: Rozhodně! Aspose.CAD nabízí uživatelsky přívětivé API, které je přístupné pro začátečníky, a zároveň poskytuje pokročilé funkce pro zkušené vývojáře.

### Q3: Kde mohu najít další podporu nebo diskuse v komunitě?

A3: Navštivte [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pro podporu a diskuse.

### Q4: Je k dispozici bezplatná zkušební verze?

A4: Ano, můžete vyzkoušet Aspose.CAD pomocí [bezplatné zkušební verze](https://releases.aspose.com/).

### Q5: Jak mohu zakoupit licenci pro Aspose.CAD pro Java?

A5: Licenci můžete zakoupit na [stránce nákupu](https://purchase.aspose.com/buy).

## Často kladené otázky

**Q: Mohu převést soubor DXF na SVG pomocí stejného kódu?**  
A: Ano, stačí nahradit název souboru souborem DXF; API zvládne oba formáty.

**Q: Jak změním výstup na plnobarevný SVG?**  
A: Nastavte `options.setColorType(SvgColorMode.FullColor);` před uložením.

**Q: Je možné vložit fonty do generovaného SVG?**  
A: Aspose.CAD v současnosti převádí text na tvary; vložení fontů není vyžadováno.

**Q: Funguje knihovna na Linuxu a macOS?**  
A: Java knihovna je platformně nezávislá a běží kdekoliv, kde je k dispozici kompatibilní JVM.

**Q: Jaká verze Aspose.CAD byla použita v tomto tutoriálu?**  
A: Příklad byl testován s Aspose.CAD pro Java 24.10.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-07  
**Testováno s:** Aspose.CAD pro Java 24.10  
**Autor:** Aspose  

---