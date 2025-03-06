---
title: Renderowanie dokumentów DWG w C# - Przewodnik Aspose.CAD
linktitle: Renderowanie dokumentów DWG w C#
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak renderować dokumenty DWG w języku C# przy użyciu Aspose.CAD. Ten przewodnik krok po kroku obejmuje importowanie, konfigurowanie i zapisywanie z przykładami kodu.
weight: 17
url: /pl/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderowanie dokumentów DWG w C# - Przewodnik Aspose.CAD

## Wstęp

Witamy w obszernym przewodniku na temat renderowania dokumentów DWG w języku C# przy użyciu Aspose.CAD. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz z .NET, ten samouczek przeprowadzi Cię przez proces wykorzystania Aspose.CAD do wydajnego renderowania plików DWG. Aspose.CAD to potężny interfejs API zapewniający solidne funkcje do pracy z formatami plików CAD, co czyni go chętnie wybieranym wyborem dla programistów zajmujących się plikami DWG.

## Warunki wstępne

Przed przystąpieniem do samouczka upewnij się, że spełniasz następujące wymagania wstępne:

- Podstawowa znajomość języka programowania C#.
- Program Visual Studio zainstalowany na Twoim komputerze.
-  Biblioteka Aspose.CAD zintegrowana z Twoim projektem. Można go pobrać z[Tutaj](https://releases.aspose.com/cad/net/).
- Przykładowy plik DWG, taki jak „Bottom_plate.dwg”, do naśladowania wraz z przykładami.

## Importuj przestrzenie nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw na początku kodu C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Podzielmy teraz podany przykład na kilka kroków:

## Krok 1: Załaduj plik DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Twój kod do ładowania pliku DWG znajduje się tutaj.
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Można tutaj dodać dodatkowe konfiguracje rasteryzacji.
```

## Krok 3: Zdefiniuj obszar do narysowania

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Krok 4: Utwórz nową rzutnię

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: Zamień aktywną rzutnię

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Krok 6: Skonfiguruj opcje PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 7: Zapisz wyrenderowany plik DWG jako plik PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Wniosek

Gratulacje! Pomyślnie wyrenderowałeś dokument DWG do formatu PDF przy użyciu Aspose.CAD w C#. Możesz odkrywać więcej funkcji i dostosowywać kod w oparciu o swoje specyficzne wymagania.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD z innymi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne.

### P2: Czy Aspose.CAD jest kompatybilny z .NET Core?

O2: Tak, Aspose.CAD jest kompatybilny zarówno z .NET Framework, jak i .NET Core.

### P3: Jak mogę obsługiwać różne układy w pliku DWG?

 O3: Możesz określić żądany układ w`Layouts` własność`CadRasterizationOptions`.

### P4: Czy istnieją jakieś uwagi licencyjne dotyczące korzystania z Aspose.CAD?

 O4: Aby uzyskać szczegółowe informacje na temat licencji, odwiedź stronę[Tutaj](https://purchase.aspose.com/buy).

### P5: Gdzie mogę znaleźć dodatkowe wsparcie?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
