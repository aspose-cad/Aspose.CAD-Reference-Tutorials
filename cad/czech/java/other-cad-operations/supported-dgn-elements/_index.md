---
date: 2026-01-25
description: Naučte se, jak převést DGN na PDF pomocí Aspose.CAD pro Javu. Tento krok‑za‑krokem
  průvodce zahrnuje podporované prvky DGN, ukázky kódu a osvědčené postupy.
linktitle: Supported DGN Elements
second_title: Aspose.CAD Java API
title: Jak převést DGN na PDF pomocí Aspose.CAD pro Javu
url: /cs/java/other-cad-operations/supported-dgn-elements/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak převést DGN na PDF pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se dozvíte **jak převést DGN na PDF** rychle a spolehlivě pomocí Aspose.CAD pro Java. Ať už vytváříte službu pro dávkové zpracování nebo přidáváte funkci exportu CAD do desktopové aplikace, níže uvedené kroky vás provedou zdu?** Ano** Pro neomezené používání je vyžadována platná licence Aspose.CAD; kební verze.  
- **Je podporována Java 8 a novější?** Rozhodně – knihovna funguje s Java 8 a novějšími runtime.  
- **Do jakých dalších formátů mohu exportovat?** Kromě PDF můžete exportovat do PNG, JPEG, SVG a dalších.

## Co znamená „převod DGN na PDF“?

Převod DGN (soubory návrhů MicroStation) na PDF znamená transformaci vektorových CAD výkresů do široce kompatibilního, prohledávatelného formátu dokumentu. PDF zachovává vrstvy, tlít Aspose.CADkálování tisíců souborů s minimální spotřebou paměti.

## Požadavky

1. **Java vývojové prostředí** – nainstalovaný JDK 8 nebo novější.  
2. **Knihovna Aspose.CAD** – Stáhněte a nainstalujte z oficiálního webu [zde](https://releases.aspose.com/cad/java/).  
3. **Adresář dokumentů** – Vytvořte složku na vašem počítači, kde budou umístěny soubory DGN a výsledné PDF.

## Průvodce krok za krokem pro převod DGN na PDF

### Krok 1: Nastavte adresář dokumentů
Zadejte složku, která obsahuje vaše zdrojové soubory DGN a kam bude PDF uloženo.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
```

> **Tip:** Nahraďte `"Your Document Directory"` absolutní cestou (např. `C:/CADFiles/`), abyste se vyhnuli překvapením s relativními cestami.

### Krok 2: Definujte vstupní a výstupní cesty
Řekněte API, který soubor DGN (nebo DWG) má načíst a jaký název má mít generované PDF.

```java
String fileName = "BlockRefDgn.dwg";
String outPath = "BlockRefDgn.dwg.pdf";
```

> **Proč název DWG?** Vzorek používá soubor DWG, který Aspose.CAD dokáže načíst jako DGN‑kompatibilní stream, což ukazuje, že stejný kód funguje i pro scénáře **convert dwg to pdf**.

### Krok 3: Načtěte DGN obrázek
Načtěte CAD soubor do objektu `Image`. Aspose.CAD automaticky detekuje formát.

```java
DgnImage dgnImage = (DgnImage)Image.load(dataDir);
```

### Krok 4: Procházejte DGN prvky
Před převodem můžete potřebovat zkontrolovat nebo upravit konkrétní prvky (čáry, oblouky, 3‑D tělesa). Níže uvedená smyčka ukazuje, jak zacházet s každým podporovaným typem prvku.

```java
for (DgnDrawingElementBase element : dgnImage.getElements())
{
    switch (element.getMetadata().getType())
    {
        // Handle different DGN element types
        case DgnElementType.Line:
        case DgnElementType.Ellipse:
        case DgnElementType.Curve:
        // ... (other cases)
        {
            // Perform specific actions based on the element type
            break;
        }
    }
}
```

### Krok 5: Zpracujte podporované 3D entity
Pokud váš DGN soubor obsahuje 3‑D geometrii, můžete tyto prvky zpracovat samostatně.

```java
case DgnElementType.SolidHeader3D:
case DgnElementType.Cone:
case DgnElementType.CellHeader:
{
    // Handle supported 3D entities
    break;
}
```

### Krok 6: Uložte jako PDF
Po případných úpravách jednoduše uložte obrázek jako PDF. Tento jediný řádek dokončuje operaci **convert DGN to PDF**.

```java
dgnImage.save(outPath, new com.aspose.cad.imageoptions.PdfOptions());
```

> **Výsledek:** `BlockRefDgn.dwg.pdf` se objeví ve složce `ExportingDGN`, připravený k distribuci.

## Jak převést DWG na PDF (související případ použití)
Stejný vzor kódu funguje pro soubory DWG. Stačí změnit `fileName` na DWG zdroj a zbytek ponechat beze změny. To ukazuje flexibilitu Aspose.CAD pro úkoly **convert dgn to pdf** i **convert dwg to pdf**.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Soubor nenalezen** | Ověřte, že `dataDir` ukazuje na správnou absolutní cestu a že název souboru odpovídá velikosti písmen. |
| **Chybějící fonty nebo styly čar** | Ujistěte se, že CAD soubor obsahuje potřebné zdroje, nebo poskytněte vlastní `LoadOptions` s adresáři fontů. |
| **Nedostatek paměti u velkých souborů** | Zpracovávejte soubor po částech nebo zvyšte haldu JVM (`-Xmx2g`). |
| **PDF vypadá prázdně** | Potvrďte, že DGN skutečně obsahuje viditelné entity; použijte smyčku iterace k zaznamenání typů prvků. |

## Závěr
Nyní máte kompletní, připravený workflow pro **convert dgn to pdf** pomocí Aspose.CAD pro Java. Iterací podporovaných DGN prvků, zpracováním 3‑D entit a voláním jediného `save` můžete s jistotou integrovat převod CAD‑na‑PDF do jakékoli Java aplikace.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD s jinými Java CAD knihovnami?
A1: Aspose.CAD je samostatná knihovna, ale můžete ji integrovat s dalšími Java knihovnami podle požadavků vašeho projektu.

### Q2: Je k dispozici zkušební verze pro Aspose.CAD?
A2: Ano, můžete si stáhnout bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q3: Kde najdu podrobnou dokumentaci pro Aspose.CAD?
A3: Odkazujte na dokumentaci [zde](https://reference.aspose.com/cad/java/).

### Q4: Jak získám podporu pro Aspose.CAD?
A4: Navštivte fórum podpory [zde](https://forum.aspose.com/c/cad/19) pro jakoukoli pomoc.

### Q5: Jsou k dispozici dočasné licence pro Aspose.CAD?
A5: Ano, můžete získat dočasné licence [zde](https://purchase.aspose.com/temporary-license/).

## Často kladené otázky (další)

**Q: Zachovává převod viditelnost vrstev?**  
A: Ano, Aspose.CAD zachovává informace o vrstvách a můžete přepínat viditelnost vrstev před uložením do PDF.

**Q: Mohu během převodu nastavit metadata PDF (autor, název)?**  
A: Rozhodně – použijte `PdfOptions` k určení vlastností `DocumentInfo`.

**Q: Je možné dávkově převést více DGN souborů?**  
A: Zabalte kód do smyčky, která prochází adresář souborů; stejné volání `Image.load` a `save` se použije pro každý soubor.

---

**Poslední aktualizace:** 2026-01-25  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}