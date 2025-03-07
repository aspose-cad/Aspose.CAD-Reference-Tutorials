---
title: Konwertuj układy na obraz rastrowy w Aspose.CAD dla .NET
linktitle: Konwertuj układy na obraz rastrowy
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Bez wysiłku konwertuj układy CAD na obrazy rastrowe za pomocą Aspose.CAD dla .NET. Usprawnij swój rozwój dzięki potężnym możliwościom manipulacji CAD.
weight: 12
url: /pl/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj układy na obraz rastrowy w Aspose.CAD dla .NET

## Wstęp

Czy chcesz bez wysiłku konwertować układy na obrazy rastrowe w aplikacjach .NET? Nie szukaj dalej! Ten przewodnik krok po kroku przeprowadzi Cię przez proces korzystania z Aspose.CAD dla .NET, potężnej biblioteki, która upraszcza zadania projektowania wspomaganego komputerowo (CAD).

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Biblioteka Aspose.CAD dla .NET: Pobierz i zainstaluj bibliotekę z[Strona pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Upewnij się, że na swoim komputerze skonfigurowano działające środowisko programistyczne .NET.

- Dokument do konwersji: Przygotuj dokument CAD zawierający układy, które chcesz przekonwertować na obrazy rastrowe.

- Twój katalog dokumentów: Zastąp symbol zastępczy „Twój katalog dokumentów” w kodzie ścieżką do katalogu dokumentów.

## Importuj przestrzenie nazw

Najpierw zaimportujmy niezbędne przestrzenie nazw, aby funkcjonalności Aspose.CAD były dostępne w Twoim kodzie.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj dokument CAD

Rozpocznij od załadowania dokumentu CAD przy użyciu biblioteki Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Twój kod dalszych kroków będzie tutaj
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

 Utwórz instancję`CadRasterizationOptions` , aby ustawić szerokość i wysokość strony oraz określić układy, które chcesz przekonwertować.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Krok 3: Skonfiguruj opcje TiffOptions dla obrazu wynikowego

 Utwórz instancję`TiffOptions` celu zdefiniowania formatu wynikowego obrazu.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Zapisz wynikowy obraz

Określ ścieżkę wyjściową i zapisz przekonwertowany obraz.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Wniosek

Gratulacje! Pomyślnie przekonwertowałeś układy CAD do formatu obrazu rastrowego przy użyciu Aspose.CAD dla .NET. Możliwości są ogromne, a ten przewodnik służy jako punkt wyjścia do wysiłków związanych z CAD.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami CAD?

 O1: Aspose.CAD obsługuje szeroką gamę formatów CAD, w tym DWG, DXF, DWF, STL i inne. Sprawdź[dokumentacja](https://reference.aspose.com/cad/net/) dla pełnej listy.

### P2: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?

 A2: Odwiedź[strona licencji tymczasowej](https://purchase.aspose.com/temporary-license/) nabyć tymczasową licencję do celów testowania i oceny.

### P3: Gdzie mogę znaleźć wsparcie dla Aspose.CAD?

 Odpowiedź 3: Fora są doskonałym miejscem do szukania pomocy. Odwiedzić[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) aby nawiązać kontakt ze społecznością i uzyskać pomoc.

### P4: Czy mogę wypróbować Aspose.CAD za darmo?

 A4: Absolutnie! Chwyć swoje[bezpłatna wersja próbna](https://releases.aspose.com/) aby poznać funkcje i możliwości Aspose.CAD.

### P5: Gdzie mogę kupić licencję na Aspose.CAD?

 A5: Przejdź do[strona zakupu](https://purchase.aspose.com/buy) kupić licencję i odblokować pełny potencjał Aspose.CAD.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
