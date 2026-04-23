---
date: 2026-03-21
description: Dowiedz się, jak konwertować pliki dxf na png i inne formaty rastrowe
  przy użyciu Aspose.CAD dla .NET. Skorzystaj z naszego przewodnika krok po kroku,
  aby uzyskać płynny eksport warstw CAD.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DXF na PNG przy użyciu Aspose.CAD dla .NET
url: /pl/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport układów CAD do formatów obrazów rastrowych w Aspose.CAD dla .NET

## Wprowadzenie

Czy chcesz efektywnie **convert dxf to png** i inne formaty obrazów rastrowych przy użyciu Aspose.CAD dla .NET? Ten przewodnik krok po kroku przeprowadzi Cię przez proces, dostarczając szczegółowe instrukcje i fragmenty kodu, aby zadanie było płynne. Niezależnie od tego, czy jesteś doświadczonym programistą, czy nowicjuszem w Aspose.CAD, ten tutorial jest przeznaczony dla wszystkich poziomów zaawansowania.

### Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje konwersję?** Aspose.CAD dla .NET  
- **Podstawowy format obsługiwany od razu?** Obrazy rastrowe JPEG, PNG, BMP i TIFF  
- **Czy mogę eksportować konkretne warstwy CAD?** Tak – użyj `CadRasterizationOptions.Layers`, aby wybrać poszczególne warstwy  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.CAD dla użytku nie‑trialowego  
- **Obsługiwane wersje .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Co to jest **convert dxf to png**?

Konwersja pliku DXF (Drawing Exchange Format) do PNG oznacza rasteryzację wektorowych danych CAD do obrazu pikselowego. Jest to przydatne, gdy potrzebujesz osadzić rysunki CAD na stronach internetowych, w raportach lub w dowolnym środowisku obsługującym wyłącznie grafikę rastrową.

## Dlaczego eksportować warstwy CAD osobno?

Eksportowanie warstw CAD pojedynczo daje precyzyjną kontrolę nad wyglądem wyjściowym, zmniejsza rozmiar pliku dla każdego obrazu i umożliwia stosowanie specyficznych stylów lub przetwarzanie po‑renderingu. Jest to szczególnie przydatne w dużych rysunkach inżynieryjnych, gdzie tylko podzbiór warstw jest istotny dla określonej grupy odbiorców.

## Wymagania wstępne

Zanim przejdziesz do tutorialu, upewnij się, że masz następujące elementy:

- **Biblioteka Aspose.CAD dla .NET** – pobierz ją ze [strony Aspose.CAD](https://releases.aspose.com/cad/net/).  
- **Plik rysunku CAD** – plik DXF (np. `conic_pyramid.dxf`), który chcesz przekonwertować do formatów rastrowych.  

## Importowanie przestrzeni nazw

W swoim projekcie .NET zaimportuj niezbędne przestrzenie nazw, aby wykorzystać funkcje Aspose.CAD. Dodaj następujące dyrektywy na początku kodu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Jak **convert dxf to png** – przewodnik krok po kroku

### Krok 1: Załaduj rysunek CAD

Najpierw wczytaj plik DXF do obiektu `Image`. Obiekt ten reprezentuje cały rysunek CAD w pamięci.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Krok 2: Utwórz `CadRasterizationOptions`

Skonfiguruj ustawienia rasteryzacji, takie jak wymiary wyjściowe i rozdzielczość. Opcje te kontrolują, w jaki sposób dane wektorowe są rasteryzowane.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Krok 3: Określ warstwy (Eksport warstw CAD)

Jeśli potrzebujesz tylko konkretnej warstwy, podaj jej nazwę tutaj. To pokazuje **export cad layers** indywidualnie.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Krok 4: Wybierz format obrazu – zapisz CAD jako PNG (lub JPEG)

Utwórz obiekt opcji specyficzny dla formatu obrazu. Zastąp `JpegOptions` przez `PngOptions`, gdy chcesz **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** Aby generować pliki PNG, po prostu utwórz `new PngOptions()` zamiast `JpegOptions`.

### Krok 5: Eksportuj do formatu JPEG (lub PNG)

Na koniec zapisz rasteryzowany obraz na dysku. Rozszerzenie pliku określa format wyjściowy.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Gdy zamienisz `JpegOptions` na `PngOptions`, ten sam kod **convert dxf to png** i wygeneruje plik `.png`.

### Dodatkowy krok: Konwertuj wszystkie warstwy

Jeśli potrzebujesz **convert cad to raster** dla każdej warstwy w rysunku, wywołaj poniższą metodę pomocniczą. Przechodzi ona po wszystkich warstwach i zapisuje każdą jako osobny obraz.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Uwaga:* Implementacja `ConvertAllLayersToRasterImageFormats` jest częścią pełnego zestawu przykładów Aspose.CAD i demonstruje przetwarzanie wsadowe warstw.

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| Pusty lub biały obraz | Opcje rasteryzacji nie ustawione (np. `PageWidth`/`PageHeight` = 0) | Upewnij się, że `PageWidth` i `PageHeight` mają dodatnie wartości |
| Brak warstw | Nieprawidłowa nazwa warstwy w tablicy `Layers` | Zweryfikuj dokładną nazwę warstwy w pliku CAD (uwzględniając wielkość liter) |
| Niska jakość PNG | Domyślna DPI jest niska | Ustaw `rasterizationOptions.Resolution = 300;` dla wyższej jakości |

## Najczęściej zadawane pytania (Original)

### Q1: Czy mogę używać innych formatów obrazu do eksportu?

A1: Tak, możesz. Po prostu zamień `JpegOptions` na opcje żądanego formatu, takie jak `PngOptions` lub `BmpOptions`.

### Q2: Czy dostępna jest wersja trial?

A2: Tak, możesz przetestować funkcjonalność Aspose.CAD, pobierając wersję próbną [tutaj](https://releases.aspose.com/).

### Q3: Jak mogę uzyskać wsparcie dla Aspose.CAD?

A3: Odwiedź forum Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy społeczności lub rozważ zakup licencji dla dedykowanego wsparcia.

### Q4: Czy dostępne są licencje tymczasowe?

A4: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

### Q5: Gdzie znajdę dokumentację?

A5: Zapoznaj się ze szczegółową dokumentacją [tutaj](https://reference.aspose.com/cad/net/).

## Dodatkowe FAQ

**Q: Czy mogę wyeksportować wszystkie warstwy jednym poleceniem?**  
A: Tak, użyj metody `ConvertAllLayersToRasterImageFormats` pokazanej powyżej.

**Q: Czy Aspose.CAD obsługuje formaty wektorowe, takie jak SVG?**  
A: Głównie celuje w formaty rastrowe, ale możesz eksportować do PDF, który zachowuje dane wektorowe.

**Q: Jak kontrolować kolor tła eksportowanego PNG?**  
A: Ustaw `rasterizationOptions.BackgroundColor` na żądany `Color` przed zapisem.

**Q: Czy można wyeksportować pojedynczy układ zamiast całego rysunku?**  
A: Tak, skonfiguruj `rasterizationOptions.Layouts`, aby określić nazwę(y) układu(ów), które chcesz rasteryzować.

## Zakończenie

Teraz wiesz, jak **convert dxf to png**, **export cad layers** oraz **save cad as png** lub JPEG przy użyciu Aspose.CAD dla .NET. Poprzez dostosowanie `CadRasterizationOptions` i zamianę opcji formatu obrazu, możesz dopasować konwersję do praktycznie dowolnego wyjścia rastrowego, którego potrzebujesz. Eksploruj inne opcje formatów w API Aspose.CAD, aby rozszerzyć swój przepływ pracy CAD‑do‑raster.

---

**Ostatnia aktualizacja:** 2026-03-21  
**Testowano z:** Aspose.CAD dla .NET 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}