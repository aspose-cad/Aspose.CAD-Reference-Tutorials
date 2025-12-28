---
date: 2025-12-28
description: Naučte se, jak přizpůsobit písma v DWG výkresech pomocí Aspose.CAD pro
  Javu. Krok‑za‑krokem průvodce přidáváním textu, výměnou písem a zdokonalováním CAD
  anotací.
linktitle: CAD Text and Annotation
second_title: Aspose.CAD Java API
title: Jak přizpůsobit písma v CAD textu a anotacích
url: /cs/java/cad-text-and-annotation/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přizpůsobit písma v CAD textu a anotacích

## Úvod

Pokud hledáte **jak přizpůsobit písma** ve svých DWG výkresech, jste na správném místě. V tomto tutoriálu vás provedeme přidáváním textu, nahrazováním písem a úpravou stylů písem pomocí Aspose.CAD pro Java. Ať už vylepšujete schéma, připravujete stavební dokumentaci nebo jen chcete jasnější **dwg textovou anotaci**, tyto kroky vám pomohou rychle a spolehlivě dosáhnout profesionálního výsledku.

## Rychlé odpovědi
- **Jaký je hlavní účel přizpůsobení písem v DWG?** Zlepšit čitelnost a sladit se s brandingem nebo projektovými standardy.  
- **Která knihovna provádí změny?** Aspose.CAD pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Mohu zpracovávat velké DWG soubory?** Ano – API efektivně streamuje data, což je vhodné pro velké výkresy.  
- **Je potřeba další software?** Pouze Java runtime (JDK 8 nebo novější) a Aspose.CAD JAR.

## Co znamená “jak přizpůsobit písma” v CADu?

Přizpůsobení písem znamená nahrazení výchozího textového stylu v DWG souboru písmem dle vašeho výběru, úpravu jeho velikosti, tloušťky nebo aplikaci jiného stylu na konkrétní vrstvy či objekty. To zajišťuje, že výkres vypadá přesně tak, jak zamýšlíte, ve všech prohlížečích.

## Proč použít Aspose.CAD pro Java k přizpůsobení písem?

- **Plná kontrola** nad textovými objekty bez otevírání výkresu v GUI editoru.  
- **Dávkové zpracování** – zpracujte desítky souborů v jednom skriptu.  
- **Cross‑platform** – funguje na Windows, Linuxu i macOS.  
- **Žádné externí závislosti** – API interně spravuje parsování DWG.

## Předpoklady
- Java Development Kit 8 nebo novější nainstalovaný.  
- Aspose.CAD pro Java JAR přidán do classpath vašeho projektu.  
- DWG soubor, který chcete upravit.

## Jak přidat text do DWG

Přidání nových textových informací je běžná potřeba, když chcete označit součásti, přidat poznámky nebo vytvořit **dwg textovou anotaci**. Postupujte podle následujících kroků:

1. **Načtěte DWG soubor** pomocí `CadImage`.  
2. **Vytvořte entitu `CadText`** s požadovaným řetězcem, umístěním a písmem.  
3. **Přidejte entitu** do kolekce entit výkresu.  
4. **Uložte** upravený soubor.

> *Poznámka: Skutečný úryvek kódu zůstává nezměněn oproti originálnímu tutoriálu a je zahrnut v propojeném pod‑tutoriálu.*

## Jak nahradit písmo v DWG

Nahrazení existujícího písma v celém výkresu pomáhá udržet konzistenci, zejména když originální písmo není na cílovém systému dostupné.

1. **Otevřete DWG** pomocí `CadImage`.  
2. **Iterujte** přes všechny objekty `CadText`.  
3. **Nastavte vlastnost `FontName`** na požadované písmo (např. “Arial”).  
4. **Uložte** aktualizovaný výkres.

Tato metoda je podrobně popsána v pod‑tutoriálu “Substitute Font in DWG”.

## Jak změnit styl písma DWG pro konkrétní styl

Někdy jen konkrétní textový styl (např. “Title”) potřebuje nové písmo, zatímco ostatní zůstávají beze změny.

1. **Identifikujte název stylu**, který chcete upravit.  
2. **Najděte odpovídající objekt `CadTextStyle`**.  
3. **Aktualizujte jeho `FontName`** a případné další atributy stylu.  
4. **Uložte změny** uložení souboru.

Podrobný návod je k dispozici v pod‑tutoriálu “Substitute Font of a Particular Style in DWG”.

## Běžné případy použití
- **Stavební výkresy**, kde jsou povinná firemní standardní písma.  
- **Architektonické plány**, které potřebují čitelné anotace pro klienty.  
- **Dávková konverze** starých DWG souborů na novou sadu firemních písem.

## Tutoriály CAD textu a anotací
### [Add Text in DWG Using Aspose.CAD for Java](./add-text-in-dwg/)
Vylepšete své DWG výkresy snadno pomocí Aspose.CAD pro Java. Přidejte text plynule s naším krok‑za‑krokem průvodcem.

### [Substitute Font in DWG with Aspose.CAD for Java](./substitute-font-in-dwg/)
Vylepšete své CAD návrhy snadno. Naučte se nahrazovat písma v DWG souborech pomocí Aspose.CAD pro Java. Krok‑za‑krokem průvodce pro vizuální dokonalost.

### [Substitute Font of a Particular Style in DWG Using Aspose.CAD for Java](./substitute-font-of-particular-style-in-dwg/)
Naute se, jak nahrazovat písma v DWG souborech pomocí Aspose.CAD pro Java. Krok‑za‑krokem průvodce pro precizní přizpůsobení stylů.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## Často kladené otázky

**Q: Mohu tyto metody použít s DWG soubory vytvořenými ve starších verzích AutoCADu?**  
A: Ano. Aspose.CAD podporuje DWG verze od R12 až po nejnovější vydání.

**Q: Co se stane, pokud cílové písmo není nainstalováno na počítači uživatele?**  
A: Výkres se vrátí k výchozímu písmu, což může ovlivnit rozvržení. Doporučuje se vložit písmo nebo zajistit, aby bylo nainstalováno na všech počítačích.

**Q: Je možné nahradit písma jen na konkrétní vrstvě?**  
A: Rozhodně. Před změnou `FontName` filtrujte objekty `CadText` podle jejich `LayerName`.

**Q: Musím po změně písem výkres znovu sestavit?**  
A: Není vyžadována žádná ruční rekonstrukce; uložení `CadImage` zapíše všechny aktualizace do souboru.

**Q: Jak mohu ověřit, že změna písma byla aplikována správně?**  
A: Otevřete DWG v libovolném prohlížeči, který podporuje zvolené písmo, nebo programově enumerujte objekty `CadText` a přečtěte zpět `FontName`.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose