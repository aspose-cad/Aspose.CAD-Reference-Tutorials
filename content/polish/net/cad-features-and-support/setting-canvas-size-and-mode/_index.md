---
title: Ustawianie rozmiaru i trybu płótna w Aspose.CAD dla .NET
linktitle: Ustawianie rozmiaru i trybu płótna
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Zapoznaj się z przewodnikiem krok po kroku dotyczącym ustawiania rozmiaru i trybu płótna w Aspose.CAD dla .NET. Z łatwością zoptymalizuj renderowanie CAD, korzystając z tego obszernego samouczka.
type: docs
weight: 16
url: /pl/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Wstęp

Czy jesteś gotowy, aby odblokować pełny potencjał Aspose.CAD dla .NET i zrewolucjonizować swoje doświadczenie w renderowaniu CAD? W tym samouczku krok po kroku zagłębimy się w zawiłości ustawiania rozmiaru i trybu płótna przy użyciu potężnej biblioteki Aspose.CAD. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten przewodnik przeprowadzi Cię przez proces, zapewniając efektywne wykorzystanie możliwości Aspose.CAD.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD z[Witryna Aspose.CAD](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne .NET.

-  Przykładowy plik CAD: W tym samouczku użyjemy przykładowego pliku DXF. Znajdziesz taki w[Dokumentacja Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importuj przestrzenie nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw na początku aplikacji .NET:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik CAD

Rozpocznij od załadowania pliku CAD przy użyciu następującego kodu:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Twój kod dalszych kroków będzie tutaj
}
```

## Krok 2: Utwórz opcje CadRasterization

 Utwórz instancję`CadRasterizationOptions` i ustaw jego właściwości:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Krok 3: Utwórz opcje PDF

 Utwórz instancję`PdfOptions` i ustaw`VectorRasterizationOptions` nieruchomość:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Eksportuj do pliku PDF

Eksportuj plik CAD do formatu PDF, korzystając ze skonfigurowanych opcji:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Krok 5: Utwórz opcje Tiff

 Utwórz instancję`TiffOptions` i ustaw`VectorRasterizationOptions` nieruchomość:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 6: Eksportuj do TIFF

Eksportuj plik CAD do formatu TIFF, korzystając ze skonfigurowanych opcji:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Wniosek

Gratulacje! Pomyślnie ustawiłeś rozmiar i tryb płótna w Aspose.CAD dla .NET. Ta potężna funkcja otwiera świat możliwości renderowania CAD. Eksperymentuj z różnymi opcjami i odkryj pełny potencjał Aspose.CAD w swoich aplikacjach .NET.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD z innymi bibliotekami .NET?

Odpowiedź 1: Tak, Aspose.CAD bezproblemowo integruje się z innymi bibliotekami .NET, zapewniając ulepszone możliwości manipulacji CAD.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?

 Odpowiedź 2: Tak, możesz poznać funkcje Aspose.CAD w ramach bezpłatnej wersji próbnej. Odwiedzać[Tutaj](https://releases.aspose.com/) rozpocząć.

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD?

 A3: Aby uzyskać wsparcie i dyskusje, odwiedź stronę[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P4: Gdzie mogę znaleźć obszerną dokumentację dla Aspose.CAD?

 A4: Patrz[Dokumentacja Aspose.CAD](https://reference.aspose.com/cad/net/) szczegółowe informacje i przykłady.

### P5: Jak kupić Aspose.CAD dla .NET?

 O5: Aby kupić Aspose.CAD, odwiedź stronę[strona zakupu](https://purchase.aspose.com/buy).