---
date: 2025-12-21
description: Naučte se, jak převést DWG na PDF exportováním konkrétního rozvržení
  DWG do PDF pomocí Aspose.CAD pro Javu. Postupujte podle tohoto krok‑za‑krokem tutoriálu
  převodu DWG na PDF a zefektivněte svůj CAD pracovní postup.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: Převod DWG na PDF – Export rozvržení pomocí Aspose.CAD pro Javu
url: /cs/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PDF – Export konkrétního rozvržení pomocí Aspose.CAD pro Java

## Úvod

Ve dynamickém světě počítačově podporovaného návrhu (CAD) je **convert DWG to PDF** častým požadavkem při sdílení výkresů s klienty, dodavateli nebo ne‑technickými zúčastněnými stranami. Aspose.CAD pro Java tento převod usnadňuje a dokonce umožňuje vybrat jedno rozvržení z DWG souboru s více rozvrženími. V tomto tutoriálu si ukážeme **jak exportovat specifická rozvržení DWG** do PDF, abyste mohli dodat přesně to, co váš projekt potřebuje, bez zbytečných stránek nebo ručního ořezávání.

## Rychlé odpovědi
- **Co znamená “convert DWG to PDF”?** Přemění DWG výkres na PDF dokument, přičemž zachová vektorová data a věrnost rozvržení.  
- **Která knihovna provádí převod?** Aspose.CAD pro Java poskytuje připravené API.  
- **Potřebuji licenci pro produkční nasazení?** Ano, je vyžadována komerční licence; pro hodnocení stačí bezplatná zkušební verze.  
- **Mohu vybrat jediné rozvržení?** Rozhodně – nastavte vlastnost `Layouts` na požadovaný název rozvržení.  
- **Jaká verze Javy je podporována?** Java 8 a novější jsou plně kompatibilní.

## Předpoklady

Předtím, než se pustíte do práce, zajistěte si:

- **Java Development Environment** – JDK 8+ a vaše oblíbené IDE.  
- **Aspose.CAD Library** – Stáhněte nejnovější JAR z oficiální stránky **[here](https://releases.aspose.com/cad/java/)**.  
- **DWG File** – Výkres, který obsahuje alespoň jedno rozvržení (např. *visualization_-_conference_room.dwg*).  

## Proč exportovat konkrétní rozvržení DWG do PDF?

Mnoho DWG souborů obsahuje více papírových prostorů (rozvržení). Export celého souboru může vytvořit objemné PDF s nežádoucími stránkami. Výběrem jediného rozvržení:

- Sníží velikost souboru.  
- Zaměří pozornost čtenáře na relevantní výkresový list.  
- Odpovídá standardům projektové dokumentace.  

## Průvodce krok za krokem

### Krok 1: Nastavení prostředí projektu

Vytvořte nový Java projekt (Maven, Gradle nebo čisté IDE) a přidejte Aspose.CAD JAR do classpath. Můžete jej stáhnout **[here](https://releases.aspose.com/cad/java/)**.

### Krok 2: Import potřebných balíčků

Přidejte požadované Aspose.CAD jmenné prostory do vaší Java třídy.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Krok 3: Načtení souboru DWG

Ukažte na DWG, který chcete převést, a načtěte jej do objektu `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Krok 4: Konfigurace možností rasterizace

Definujte velikost stránky a, co je nejdůležitější, rozvržení, které chcete exportovat.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Krok 5: Nastavení možností exportu do PDF

Propojte nastavení rasterizace s PDF exportérem.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 6: Export DWG do PDF

Uložte výsledek jako PDF soubor. Výstup bude obsahovat pouze **Layout1**, čímž dosáhnete čisté operace **convert DWG to PDF**.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Časté problémy a řešení

| Problém | Proč se to stane | Řešení |
|-------|----------------|-----|
| **Layout not found** | Název rozvržení je špatně napsán nebo v DWG neexistuje. | Použijte `image.getLayoutNames()` k vypsání dostupných rozvržení a vyberte správné. |
| **Low resolution PDF** | `PageWidth`/`PageHeight` jsou příliš malé. | Zvyšte rozměry (např. 2000 × 2000) nebo nastavte `rasterizationOptions.setResolution(300);`. |
| **License exception** | Spuštění bez platné licence v ne‑zkušebním prostředí. | Aplikujte svou Aspose.CAD licenci před načtením obrázku: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Často kladené otázky

**Q1: Mohu použít Aspose.CAD pro Java s jinými Java‑založenými CAD knihovnami?**  
A: Aspose.CAD pro Java je samostatná knihovna, ale může být integrována s jinými Java‑založenými knihovnami pro rozšířené funkce.

**Q2: Existují různé licenční možnosti pro Aspose.CAD?**  
A: Ano, můžete prozkoumat licenční možnosti a podrobnosti o nákupu **[here](https://purchase.aspose.com/buy)**.

**Q3: Jak získám dočasnou licenci pro Aspose.CAD?**  
A: Navštivte **[this link](https://purchase.aspose.com/temporary-license/)** a požádejte o dočasnou licenci.

**Q4: Kde mohu najít podporu pro Aspose.CAD?**  
A: Pro jakékoli dotazy nebo pomoc navštivte **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q5: Je k dispozici bezplatná zkušební verze Aspose.CAD?**  
A: Ano, bezplatnou zkušební verzi získáte **[here](https://releases.aspose.com/)**.

## Závěr

Po absolvování tohoto **dwg to pdf tutorial** máte spolehlivý způsob, jak **convert DWG to PDF** s cílením na jediné rozvržení. Tento přístup šetří úložiště, urychluje sdílení dokumentů a udržuje váš CAD workflow přehledný. Nebojte se experimentovat s různými nastaveními rasterizace nebo kombinovat více rozvržení do jednoho PDF podle vývoje projektu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2025-12-21  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose