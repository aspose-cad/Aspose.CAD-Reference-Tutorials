---
title: Wsparcie dla DGN V7 w Aspose.CAD dla .NET
linktitle: Wsparcie dla DGN V7
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Poznaj Aspose.CAD pod kątem płynnej obsługi .NET dla DGN V7. Konwertuj pliki DGN na obrazy rastrowe bez wysiłku, korzystając ze wskazówek krok po kroku.
weight: 19
url: /pl/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wsparcie dla DGN V7 w Aspose.CAD dla .NET

## Wstęp

dziedzinie programowania .NET Aspose.CAD wyróżnia się jako potężna biblioteka do obsługi plików CAD. Ten samouczek omawia specyficzną funkcję Aspose.CAD dla .NET – obsługę plików DGN V7. DGN, skrót od Design, jest szeroko stosowanym formatem plików w domenie CAD. Aspose.CAD upraszcza proces pracy z plikami DGN V7, oferując programistom bezproblemową obsługę.

## Warunki wstępne

Zanim przejdziemy do wdrożenia, upewnij się, że spełnione są następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Można go pobrać z[strona internetowa](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Skonfiguruj działające środowisko programistyczne .NET, w tym Visual Studio lub dowolne inne preferowane IDE.

Teraz, gdy mamy już posortowane wymagania wstępne, przyjrzyjmy się, jak wykorzystać obsługę DGN V7 w Aspose.CAD dla .NET.

## Importuj przestrzenie nazw

Zacznij od zaimportowania niezbędnych przestrzeni nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DGN

 Rozpocznij od załadowania istniejącego pliku DGN jako`CadImage` Zastępować`"Your Document Directory"` I`"Nikon_D90_Camera.dgn"` z odpowiednią ścieżką katalogu i nazwą pliku.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Kod dalszych kroków znajduje się tutaj...
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

 Stwórz`CadRasterizationOptions` obiekt do definiowania i ustawiania różnych właściwości związanych z rasteryzacją.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Krok 3: Ustaw opcje rasteryzacji wektora

 Stwórz`JpegOptions` obiekt, ponieważ zamierzamy przekonwertować plik DGN do formatu JPEG. Przypisz wcześniej utworzony`CadRasterizationOptions` sprzeciwić się temu.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Krok 4: Zapisz obraz rastrowy

 Zadzwoń do`Save` metoda`CadImage` class, aby wyeksportować plik DGN do obrazu rastrowego, w tym przypadku do pliku JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Po wykonaniu tych kroków plik DGN zostanie pomyślnie wyeksportowany do obrazu rastrowego.

## Wniosek

W tym samouczku zbadaliśmy bezproblemową obsługę DGN V7 w Aspose.CAD dla .NET. Postępując zgodnie ze szczegółowym przewodnikiem, programiści mogą bez wysiłku konwertować pliki DGN na obrazy rastrowe, rozszerzając możliwości swoich aplikacji .NET.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny z najnowszymi specyfikacjami DGN V7?

Odpowiedź 1: Tak, Aspose.CAD został zaprojektowany tak, aby bezproblemowo obsługiwać pliki DGN V7, zapewniając zgodność z najnowszymi specyfikacjami.

### P2: Czy mogę dostosować opcje rasteryzacji dla konwersji plików DGN?

 A2: Absolutnie. Samouczek pokazuje, jak utworzyć i skonfigurować`CadRasterizationOptions` dostosować proces konwersji.

### P3: Czy oprócz JPEG istnieją inne obsługiwane formaty wyjściowe?

O3: Tak, Aspose.CAD obsługuje różne formaty wyjściowe. Pełną listę można znaleźć w dokumentacji.

### P4: Jak mogę uzyskać pomoc dotyczącą zapytań związanych z Aspose.CAD?

 A4: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?

 Odpowiedź 5: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
