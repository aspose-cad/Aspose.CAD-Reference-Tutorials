---
date: 2026-04-09
description: Dowiedz się, jak eksportować warstwy DWG, konwertować obraz DWG i zapisywać
  DWG jako JPEG przy użyciu C# i Aspose.CAD dla .NET. Przewodnik krok po kroku, umożliwiający
  efektywną manipulację plikami CAD.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Obsługa warstw w plikach DWG w C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Eksport warstw DWG w C# – Poradnik Aspose.CAD
url: /pl/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport warstw DWG przy użyciu C# – Samouczek Aspose.CAD

## Wprowadzenie

W tym obszernej przewodniku dowiesz się **jak eksportować warstwy DWG** przy użyciu C# i biblioteki Aspose.CAD. Niezależnie od tego, czy potrzebujesz **konwertować obrazy DWG**, kontrolować **widoczność warstw DWG**, czy po prostu **zapisać pliki DWG JPEG**, poniższe kroki pokażą Ci dokładnie, jak zrobić to efektywnie. Po zakończeniu samouczka będziesz mieć gotowy fragment kodu, który izoluje określoną warstwę i renderuje ją jako wysokiej jakości JPEG.

## Szybkie odpowiedzi
- **Co oznacza „export dwg layers”?** Oznacza rasteryzację wybranych warstw pliku DWG do formatu obrazu, takiego jak JPEG lub PNG.  
- **Która biblioteka jest najlepsza do tego zadania?** Aspose.CAD for .NET zapewnia pełną funkcjonalność bez konieczności posiadania AutoCADa.  
- **Czy mogę wyeksportować wiele warstw jednocześnie?** Tak – przekaż tablicę nazw warstw do opcji rasteryzacji.  
- **Czy potrzebuję licencji do użytku produkcyjnego?** Wymagana jest licencja komercyjna; dostępna jest darmowa wersja próbna do oceny.  
- **Jakie formaty wyjściowe są obsługiwane?** JPEG, PNG, BMP, TIFF oraz kilka innych poprzez klasy ImageOptions.

## Co to jest export dwg layers?
Eksportowanie warstw DWG oznacza pobranie danych wektorowych należących do jednej lub kilku warstw w rysunku DWG i rasteryzację ich do obrazu bitmapowego. Jest to przydatne, gdy chcesz udostępnić widok konkretnej części rysunku bez ujawniania całego pliku CAD.

## Dlaczego kontrolować widoczność warstw DWG?
Kontrolowanie widoczności warstw pozwala Ci:

- Tworzyć czyste materiały wizualne do prezentacji lub dokumentacji.  
- Zmniejszyć rozmiar pliku, eksportując tylko potrzebną geometrię.  
- Chronić własnościowe szczegóły projektu, ukrywając poufne warstwy.  

## Wymagania wstępne

Zanim przejdziesz dalej, upewnij się, że masz:

- Podstawową znajomość języka programowania C#.  
- Zainstalowane Visual Studio na komputerze.  
- Bibliotekę Aspose.CAD for .NET, którą możesz pobrać ze [strony Aspose.CAD](https://releases.aspose.com/cad/net/).

## Importowanie przestrzeni nazw

Aby rozpocząć, zaimportuj przestrzenie nazw, które dają dostęp do funkcji rasteryzacji i eksportu obrazów.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Krok 1: Załaduj plik DWG

Załaduj źródłowy plik DWG (lub DWF) do obiektu `Image`. Obiekt ten reprezentuje cały rysunek w pamięci.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Dlaczego to ważne:* Załadowanie pliku raz pozwala ponownie używać tej samej instancji `image` do dowolnej liczby eksportów specyficznych dla warstw, co poprawia wydajność.

## Krok 2: Skonfiguruj opcje rasteryzacji

Utwórz instancję `CadRasterizationOptions`, aby poinformować Aspose.CAD, jak renderować rysunek. Tutaj ustawiamy wysoką rozdzielczość (1600 × 1600), aby wyeksportowany JPEG był ostry.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Możesz także dostosować kolor tła, skalowanie grubości linii lub ustawienia antyaliasingu, jeśli jest to potrzebne.

## Krok 3: Określ warstwy (widoczność warstw DWG)

Dodaj warstwy, które chcesz **export dwg layers**. W tym przykładzie eksportujemy tylko „LayerA”. Aby wyeksportować wiele warstw, po prostu wymień je w tablicy.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Wskazówka:* Użyj dokładnej nazwy warstwy takiej, jaka pojawia się w rysunku; nazwy warstw są rozróżniane pod względem wielkości liter.

## Krok 4: Skonfiguruj opcje eksportu obrazu

Wybierz format obrazu, który chcesz utworzyć. Użyjemy `JpegOptions`, ponieważ JPEG zapewnia dobrą równowagę między jakością a rozmiarem pliku, co jest idealne, gdy potrzebujesz **save dwg jpeg** plików do podglądu w sieci.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Jeśli potrzebujesz **convert dwg image** do PNG lub TIFF, zamień `JpegOptions` na odpowiednią klasę opcji.

## Krok 5: Zapisz wyeksportowany obraz

Zdefiniuj ścieżkę pliku wyjściowego i wywołaj `Save`. Silnik rasteryzacji respektuje podaną listę warstw, więc w ostatecznym JPEG pojawi się tylko „LayerA”.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Po wykonaniu tej linii znajdziesz `for_layers_test.jpg` w katalogu dokumentu, zawierający tylko wybraną warstwę.

## Typowe problemy i rozwiązania

| Issue | Resolution |
|-------|------------|
| **Layer name not found** | Sprawdź dokładną pisownię i wielkość liter nazwy warstwy w oryginalnym pliku DWG. Użyj przeglądarki CAD, aby wyświetlić listę nazw warstw. |
| **Blank output image** | Upewnij się, że opcje rasteryzacji mają nieprzezroczyste tło oraz że wybrane warstwy rzeczywiście zawierają geometrię. |
| **Low‑resolution output** | Zwiększ `PageWidth` i `PageHeight` lub ustaw `Resolution` w `CadRasterizationOptions`. |
| **Unsupported DWG version** | Zaktualizuj do najnowszej wersji Aspose.CAD; dodaje ona wsparcie dla nowszych wydań AutoCADa. |

## Najczęściej zadawane pytania

### Q1: Czy mogę obsługiwać wiele warstw jednocześnie?
A1: Tak, możesz. Po prostu dodaj nazwy warstw do tablicy `rasterizationOptions.Layers`.

### Q2: Czy dostępna jest wersja próbna Aspose.CAD?
A2: Tak, możesz uzyskać darmową wersję próbną [tutaj](https://releases.aspose.com/).

### Q3: Gdzie mogę znaleźć dokumentację?
A3: Dokumentacja jest dostępna [tutaj](https://reference.aspose.com/cad/net/).

### Q4: Jak uzyskać wsparcie dla Aspose.CAD?
A4: Wsparcie możesz uzyskać na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Jakie są opcje licencjonowania Aspose.CAD?
A5: Opcje licencjonowania i szczegóły zakupu możesz sprawdzić [tutaj](https://purchase.aspose.com/buy).

**Dodatkowe pytania i odpowiedzi**

**Q: Czy mogę wyeksportować rysunek do PNG zamiast JPEG?**  
A: Oczywiście. Zamień `JpegOptions` na `PngOptions` i odpowiednio zmień rozszerzenie pliku.

**Q: Czy biblioteka zachowuje style linii i kolory?**  
A: Tak. Wszystkie właściwości wektorowe są wiernie renderowane podczas rasteryzacji.

---

**Ostatnia aktualizacja:** 2026-04-09  
**Testowano z:** Aspose.CAD for .NET (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}