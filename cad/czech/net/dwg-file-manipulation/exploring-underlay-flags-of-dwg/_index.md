---
title: Zkoumání podložních příznaků souborů DWG – výukový program Aspose.CAD
linktitle: Prozkoumání podložních příznaků souborů DWG
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Odemkněte sílu Aspose.CAD for .NET při zkoumání příznaků podložení souborů DWG. Postupujte podle našeho podrobného průvodce.
weight: 13
url: /cs/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zkoumání podložních příznaků souborů DWG – výukový program Aspose.CAD

## Úvod

Pokud se ponoříte do spletitého světa CAD souborů, konkrétně souborů DWG, a chcete odemknout tajemství podkladových vlajek, jste na správném místě. Tento tutoriál vás provede procesem zkoumání příznaků podložení v souborech DWG pomocí výkonné knihovny Aspose.CAD for .NET.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte následující:

- Základní znalost programování v C# a .NET.
-  Nainstalovaná knihovna Aspose.CAD for .NET. Pokud ne, můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).
- Soubor DWG pro testování. Můžete použít ukázkový soubor "BlockRefDgn.dwg" poskytnutý v tutoriálu.

## Importovat jmenné prostory

Chcete-li začít, musíte importovat potřebné jmenné prostory. Zde je úryvek, který vám pomůže:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Krok 1: Načtěte soubor DWG a převeďte jej na CadImage

Začněte načtením existujícího souboru DWG a jeho převedením na CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Načtěte soubor DWG a převeďte jej na CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Zde bude váš kód pro další kroky
}
```

## Krok 2: Iterujte přes entity

Dále iterujte každou entitu uvnitř souboru DWG:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Zde bude váš kód pro další kroky
}
```

## Krok 3: Zkontrolujte typ CadDgnUnderlay

Zkontrolujte, zda je entita typu CadDgnUnderlay:

```csharp
if (entity is CadDgnUnderlay)
{
    // Zde bude váš kód pro další kroky
}
```

## Krok 4: Přístup k podložním vlajkám

Získejte přístup k různým vlajkám podložení a extrahujte relevantní informace:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Závěr

Gratulujeme! Úspěšně jste prozkoumali příznaky podložení souborů DWG pomocí Aspose.CAD for .NET. Tento výukový program vás vybavil znalostmi k procházení entitami a získávání důležitých informací o podloženích.

## FAQ

### Q1: Mohu použít Aspose.CAD pro .NET s jinými formáty souborů CAD?

Odpověď 1: Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DGN a dalších. Úplný seznam naleznete v dokumentaci.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD pro .NET?

 A2: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q3: Kde najdu podporu pro Aspose.CAD pro .NET?

 A3: Navštivte fórum podpory[tady](https://forum.aspose.com/c/cad/19) pro pomoc.

### Q4: Jak koupím Aspose.CAD pro .NET?

A4: Kupte si knihovnu[tady](https://purchase.aspose.com/buy).

### Q5: Je k dispozici bezplatná zkušební verze?

 A5: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
