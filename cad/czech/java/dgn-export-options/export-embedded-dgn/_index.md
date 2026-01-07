---
date: 2026-01-07
description: Naučte se, jak exportovat CAD do PDF a převést DGN do PDF pomocí Aspose.CAD
  pro Javu. Průvodce krok za krokem pro vývojáře Javy.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Export CAD do PDF – Export vloženého DGN pomocí Aspose.CAD pro Java
url: /cs/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD do PDF – Export vloženého DGN pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se dozvíte **jak exportovat CAD do PDF** převodem vloženého souboru DGN na vysoce kvalitní PDF dokument pomocí Aspose.CAD pro Java. Aspose.CAD je robustní knihovna, která dává vývojářům Java plnou kontrolu nad manipulací CAD souborů, ať už potřebujete **převést DGN do PDF**, **převést DWG do PDF**, nebo jen vykreslit CAD výkresy v jiných formátech. Postupujte podle níže uvedeného krok‑za‑krokem návodu a během několika minut budete schopni tuto funkci integrovat do svých aplikací.

## Rychlé odpovědi
- **Co znamená „export CAD do PDF“?** Převádí CAD výkresy (DWG, DGN, atd.) do souborů PDF při zachování vektorové kvality.  
- **Která knihovna se používá?** Aspose.CAD pro Java.  
- **Potřebuji licenci?** Licence je vyžadována pro produkční použití; k dispozici je bezplatná zkušební verze.  
- **Jaké jsou hlavní předpoklady?** Vývojové prostředí Java a JAR Aspose.CAD pro Java.  
- **Mohu výstup přizpůsobit?** Ano – můžete vybírat rozvržení, nastavit možnosti rasterizace a ovládat nastavení PDF.

## Co je „export CAD do PDF“?
Export CAD do PDF znamená převzetí nativního CAD souboru (např. DWG nebo DGN) a vytvoření PDF dokumentu, který věrně reprezentuje původní geometrii. PDF lze zobrazit na jakékoli platformě bez potřeby CAD softwaru, což je ideální pro sdílení, tisk nebo archivaci.

## Proč použít Aspose.CAD pro Java k převodu DGN do PDF?
- **Žádné externí závislosti** – funguje čistě v Javě.  
- **Zachovává vektorová data** – PDF zůstává ostré při libovolném přiblížení.  
- **Detailní kontrola** – vyberte konkrétní rozvržení, nastavte DPI rasterizace a vložte fonty.  
- **Podniková připravenost** – podporuje velké soubory, dávkové zpracování a licenční možnosti.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

- **Vývojové prostředí Java** – nainstalovaný a nakonfigurovaný JDK 8 nebo vyšší.  
- **Aspose.CAD pro Java** – stáhněte nejnovější JAR [zde](https://releases.aspose.com/cad/java/).  

## Import balíčků

Pro zahájení je třeba importovat potřebné třídy do vašeho Java projektu. Přidejte následující importy do svého zdrojového souboru:

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

## Jak exportovat DGN do PDF pomocí Aspose.CAD pro Java?

Níže je přehledný, číslovaný průvodce, který ukazuje, jak převést vložený soubor DGN (uložený uvnitř DWG) do PDF.

### Krok 1: Nastavení vstupních a výstupních cest

Definujte adresář, který obsahuje váš zdrojový soubor, a uveďte DWG, který obsahuje vložený DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Krok 2: Načtení souboru DWG

Načtěte soubor DWG do objektu `Image`. Aspose.CAD automaticky detekuje vložená DGN data.

```java
Image objImage = Image.load(fileName);
```

### Krok 3: Konfigurace možností rasterizace

Vyberte, které rozvržení(a) chcete zahrnout do PDF. V tomto příkladu exportujeme pouze rozvržení **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Krok 4: Konfigurace možností PDF

Připojte nastavení rasterizace k možnostem exportu PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Uložení souboru PDF

Nakonec zapište PDF na disk pomocí nakonfigurovaných možností.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Převod DWG do PDF – další tip

Pokud je váš zdrojový soubor obyčejný DWG (bez vloženého DGN), můžete použít stejný kód – stačí změnit `fileName`, aby ukazoval na DWG, který chcete převést. Nastavení rasterizace a PDF zůstávají stejná, což vám poskytuje konzistentní workflow **převodu DWG do PDF**.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|----------|
| **Prázdný výstup PDF** | Neshoda názvu rozvržení | Ověřte, že název rozvržení předaný do `setLayouts` přesně odpovídá názvu rozvržení ve zdrojovém souboru (rozlišuje velká a malá písmena). |
| **Výjimka licence** | Používání zkušební verze bez licence | Aplikujte platnou Aspose.CAD před načtením obrázku (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Soubor nenalezen** | Nesprávná cesta `dataDir` | Použijte absolutní cestu nebo se ujistěte, že relativní cesta je správná vzhledem k pracovnímu adresáři projektu. |
| **Grafika s nízkým rozlišením** | Výchozí DPI rasterizace je nízké | Nastavte `rasterizationOptions.setPageWidth/Height` nebo `setResolution` pro zvýšení DPI. |

## Často kladené otázky

**Q: Můžu použít Aspose.CAD pro Java v komerčním projektu?**  
A: Ano, Aspose.CAD pro Java je komerční knihovna. Licenci můžete získat [zde](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, bezplatnou zkušební verzi Aspose.CAD pro Java získáte [zde](https://releases.aspose.com/).

**Q: Jak mohu získat podporu pro Aspose.CAD pro Java?**  
A: Podporu můžete hledat v komunitě Aspose.CAD na [fóru](https://forum.aspose.com/c/cad/19).

**Q: Co když potřebuji dočasnou licenci?**  
A: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

**Q: Kde najdu dokumentaci?**  
A: Dokumentace je k dispozici [zde](https://reference.aspose.com/cad/java/).

## Závěr

Nyní jste se naučili, **jak exportovat CAD do PDF**, konkrétně **jak převést DGN do PDF** a také **jak převést DWG do PDF** pomocí Aspose.CAD pro Java. Dodržením výše uvedených kroků můžete do libovolného řešení založeného na Javě integrovat bezproblémový převod CAD‑na‑PDF a poskytovat uživatelům vysoce kvalitní PDF bez nutnosti dalšího CAD softwaru.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-07  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose