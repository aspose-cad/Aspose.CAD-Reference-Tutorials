---
title: Eksportuj układy CAD do formatów obrazów rastrowych w Aspose.CAD dla .NET
linktitle: Eksportuj układy CAD do formatów obrazów rastrowych
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak eksportować układy CAD do obrazów rastrowych za pomocą Aspose.CAD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać bezproblemową konwersję.
weight: 10
url: /pl/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj układy CAD do formatów obrazów rastrowych w Aspose.CAD dla .NET

## Wstęp

Czy chcesz efektywnie konwertować układy CAD do formatów obrazów rastrowych za pomocą Aspose.CAD dla .NET? Ten przewodnik krok po kroku przeprowadzi Cię przez proces, dostarczając szczegółowych instrukcji i fragmentów kodu, dzięki którym zadanie będzie przebiegać bezproblemowo. Niezależnie od tego, czy jesteś doświadczonym programistą, czy nowicjuszem w Aspose.CAD, ten samouczek przeznaczony jest dla wszystkich poziomów wiedzy.

## Warunki wstępne

Zanim zagłębisz się w samouczek, upewnij się, że posiadasz następujące informacje:

- Biblioteka Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Jeśli nie, możesz pobrać go ze strony[Witryna Aspose.CAD](https://releases.aspose.com/cad/net/).

- Plik rysunku CAD: Przygotuj plik rysunku CAD (np. conic_pyramid.dxf), który chcesz przekonwertować na formaty obrazu rastrowego.

## Importuj przestrzenie nazw

W swoim projekcie .NET zaimportuj niezbędne przestrzenie nazw, aby wykorzystać funkcjonalności Aspose.CAD. Na początku kodu umieść następujące przestrzenie nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj rysunek CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Załaduj rysunek CAD do instancji Image
using (var image = Image.Load(sourceFilePath))
{
    // Twój kod do wczytania rysunku CAD znajduje się tutaj
}
```

## Krok 2: Utwórz opcje CadRasterization

```csharp
// Utwórz instancję CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Krok 3: Określ warstwy

```csharp
// Dodaj nazwę warstwy do listy warstw CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Krok 4: Utwórz opcje Jpeg

```csharp
// Utwórz instancję JpegOptions (lub dowolne ImageOptions dla formatów rastrowych)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Eksportuj do formatu JPEG

```csharp
// Eksportuj każdą warstwę do formatu JPEG
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Dodatkowy krok: Konwertuj wszystkie warstwy

Jeśli chcesz przekonwertować wszystkie warstwy, użyj następującej metody:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Ta metoda polega na iteracji po wszystkich warstwach rysunku CAD, eksportując każdą warstwę do osobnego pliku Jpeg.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się eksportować układy CAD do formatów obrazów rastrowych przy użyciu Aspose.CAD dla .NET. Ten samouczek stanowi kompleksowy przewodnik dla programistów poszukujących wydajnych i niezawodnych rozwiązań do konwersji CAD.

## Często zadawane pytania

### P1: Czy mogę używać innych formatów obrazów do eksportu?

 A1: Tak, możesz. Po prostu wymień`JpegOptions` z opcjami żądanego formatu, takimi jak`PngOptions` Lub`BmpOptions`.

### P2: Czy dostępna jest wersja próbna?

 Odpowiedź 2: Tak, możesz poznać funkcjonalność Aspose.CAD, pobierając wersję próbną[Tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD?

 A3: Odwiedź Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) wsparcia społecznościowego lub rozważ zakup licencji na wsparcie dedykowane.

### P4: Czy dostępne są licencje tymczasowe?

 Odpowiedź 4: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć dokumentację?

 Odpowiedź 5: Zapoznaj się ze szczegółową dokumentacją[Tutaj](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
