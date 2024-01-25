---
title: Dopasowywanie rozmiaru rysunku CAD w Aspose.CAD dla .NET
linktitle: Dopasowywanie rozmiaru rysunku CAD
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak bez wysiłku dostosować rozmiary rysunków CAD w .NET przy użyciu Aspose.CAD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby bezproblemowo zmieniać rozmiar.
type: docs
weight: 10
url: /pl/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Wstęp

Czy chcesz płynnie dostosować rozmiar rysunków CAD w aplikacjach .NET? Aspose.CAD dla .NET zapewnia solidne rozwiązanie, umożliwiające bezproblemową obsługę zmiany rozmiaru rysunków CAD. W tym samouczku przeprowadzimy Cię przez proces, dzieląc każdy krok, aby upewnić się, że zrozumiesz zawiłości zmiany rozmiaru rysunków CAD za pomocą Aspose.CAD.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Biblioteka Aspose.CAD dla .NET: Pobierz i zainstaluj bibliotekę z[Strona pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).
- Przykładowy rysunek CAD: Upewnij się, że masz przykładowy plik rysunku CAD (np. „sample.dwg”) w katalogu dokumentów.

## Importuj przestrzenie nazw

Rozpocznij od zaimportowania niezbędnych przestrzeni nazw do aplikacji .NET. Ten krok jest kluczowy, aby uzyskać dostęp do funkcjonalności zapewnianych przez Aspose.CAD dla .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj rysunek CAD

Zacznij od załadowania rysunku CAD do instancji klasy Aspose.CAD.Image. Upewnij się, że masz poprawną ścieżkę pliku przykładowego rysunku.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Załaduj rysunek CAD do instancji Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Twój kod tutaj...
}
```

## Krok 2: Utwórz BmpOptions

Utwórz instancję klasy BmpOptions, która odpowiada za określenie opcji podczas zapisywania rysunku CAD jako pliku BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Krok 3: Ustaw opcje CadRasterization

Utwórz instancję klasy CadRasterizationOptions i skonfiguruj jej właściwości pod kątem rasteryzacji wektorowej.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Krok 4: Ustaw właściwość UnitType

Ustaw właściwość UnitType CadRasterizationOptions, aby określić typ jednostki do zmiany rozmiaru. W tym przykładzie jest ustawiona na Centymetr.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Krok 5: Ustaw właściwość układów

Określ układy, które chcesz uwzględnić w rysunku o zmienionym rozmiarze, ustawiając właściwość Układy.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 6: Eksportuj do BMP

Na koniec zapisz układ o zmienionym rozmiarze jako plik BMP, korzystając z metody Zapisz.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Teraz pomyślnie dostosowałeś rozmiar swojego rysunku CAD za pomocą Aspose.CAD dla .NET!

## Wniosek

W tym samouczku przeszliśmy przez proces zmiany rozmiaru rysunków CAD w .NET przy użyciu Aspose.CAD. Wykonując poniższe kroki, możesz bezproblemowo zintegrować tę funkcjonalność ze swoimi aplikacjami, zapewniając płynną obsługę.

## Często zadawane pytania

### P1: Czy Aspose.CAD dla .NET jest kompatybilny ze wszystkimi formatami CAD?

 O1: Aspose.CAD dla .NET obsługuje szeroką gamę formatów CAD, w tym DWG, DXF, DWF i inne. Sprawdź[dokumentacja](https://reference.aspose.com/cad/net/) dla pełnej listy.

### P2: Czy mogę jednocześnie zmieniać rozmiar wielu układów?

Odpowiedź 2: Tak, możesz zmienić rozmiar wielu układów, dostosowując tablicę układów w CadRasterizationOptions.

### P3: Gdzie mogę uzyskać wsparcie dla Aspose.CAD dla .NET?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie i pomoc społeczną.

### P4: Czy dostępny jest bezpłatny okres próbny?

 A4: Tak, możesz odkryć a[bezpłatna wersja próbna](https://releases.aspose.com/) aby ocenić funkcje Aspose.CAD dla .NET.

### P5: Jak mogę uzyskać tymczasową licencję na Aspose.CAD dla .NET?

 A5: Uzyskaj tymczasową licencję do celów testowych[Tutaj](https://purchase.aspose.com/temporary-license/).