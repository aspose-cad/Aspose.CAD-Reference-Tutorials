---
date: 2026-04-06
description: Dowiedz się, jak konwertować DWF na JPG w C# przy użyciu Aspose.CAD i
  odkryj, jak wyodrębnić rozmiar układu DWF z plików DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Praca z plikami DWG w C# – Pobierz rozmiar układu DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DWF na JPG w C# – Pobierz rozmiar układu DWF z DWG
url: /pl/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWF do JPG w C# – Pobierz rozmiar układu DWF z DWG

## Wprowadzenie

Jeśli potrzebujesz **konwertować DWF do JPG**, jednocześnie ustalając dokładne wymiary układu, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię przez kompletny przykład od początku do końca, wykorzystujący Aspose.CAD for .NET do otwarcia pliku DWF pochodzącego z DWG, odczytania rozmiaru każdego układu oraz zapisania układu jako wysokiej jakości obraz JPG. Po zakończeniu nie tylko będziesz wiedział, jak wyodrębnić informacje o układzie DWF, ale także będziesz miał gotowy fragment kodu, który możesz wstawić do dowolnego projektu C#.

## Szybkie odpowiedzi
- **Co oznacza „convert DWF to JPG”?** Oznacza rasteryzację wektorowego układu DWF do bitmapowego obrazu JPEG.  
- **Dlaczego najpierw odczytać rozmiar układu?** Znając dokładne wymiary, możesz ustawić prawidłowe wymiary strony, unikając rozciągniętego lub przyciętego wyniku.  
- **Która biblioteka to obsługuje?** Aspose.CAD for .NET zapewnia pełne wsparcie dla DWG, DWF i konwersji obrazów rastrowych.  
- **Czy potrzebna jest licencja?** Licencja tymczasowa działa w trybie ewaluacji; pełna licencja jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Czym jest „convert DWF to JPG” i dlaczego ma to znaczenie?

Konwersja pliku DWF (Design Web Format) do JPG tworzy przenośny obraz, który może być wyświetlany w przeglądarkach, osadzany w raportach lub udostępniany interesariuszom, którzy nie posiadają oprogramowania CAD. Konwersja daje również możliwość manipulacji obrazem (zmiana rozmiaru, kompresja, znak wodny) przy użyciu standardowych narzędzi do przetwarzania obrazów.

## Dlaczego wyodrębniać rozmiar układu DWF?

Plik DWF może zawierać wiele układów, z których każdy ma własny system współrzędnych i jednostki (cale, milimetry itp.). Wyodrębnienie rozmiaru układu pozwala:

1. Zachować oryginalny współczynnik proporcji podczas rasteryzacji.  
2. Wybrać właściwe DPI dla wyjścia w wysokiej rozdzielczości.  
3. Zautomatyzować przetwarzanie wsadowe wielu układów bez ręcznej ingerencji.

## Wymagania wstępne

Aby płynnie podążać za tym samouczkiem, upewnij się, że spełniasz następujące wymagania wstępne:

- Aspose.CAD for .NET: Upewnij się, że masz zainstalowany Aspose.CAD for .NET. Możesz go pobrać ze [strony pobierania Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

Posiadanie gotowej biblioteki oznacza, że możesz skupić się na kodzie, a nie na szukaniu zależności.

## Importowanie przestrzeni nazw

Zanim zaczniemy kodować, zaimportuj wymagane przestrzenie nazw. Dostarczają one klasy potrzebne do pracy z plikami CAD, opcjami rasteryzacji oraz operacjami we/wy.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Krok 1: Przygotuj środowisko

Utwórz nowy projekt konsolowy C# lub bibliotekę klas, dodaj odwołanie do **Aspose.CAD.dll** i upewnij się, że projekt celuje w kompatybilną wersję .NET.

## Krok 2: Zdefiniuj ścieżki plików (jak wyodrębnić DWF)

Określ, gdzie znajduje się źródłowy plik DWF oraz gdzie mają być zapisywane wygenerowane pliki JPG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Wskazówka:** Użyj `Path.Combine(MyDir, "blocks_and_tables.dwf")` dla bezpieczniejszego obsługi ścieżek na różnych systemach operacyjnych.

## Krok 3: Załaduj obraz DWF

Załaduj plik DWF do obiektu `Aspose.CAD.Image`. Rzutujemy go na `DwfImage`, ponieważ potrzebujemy dostępu do właściwości specyficznych dla stron.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Krok 4: Iteruj przez strony

Plik DWF może zawierać kilka stron (układów). Przejdź pętlą po każdej, aby móc przetwarzać je indywidualnie.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Krok 5: Pobierz informacje o układzie

Wewnątrz pętli pobierz nazwę układu. Nazwa ta będzie używana zarówno do logowania, jak i do nazewnictwa pliku wyjściowego JPG.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Krok 6: Skonfiguruj opcje JPG

Utwórz instancję `JpegOptions` i skonfiguruj opcje rasteryzacji. Właściwość `Layouts` informuje Aspose.CAD, który układ ma zostać wyrenderowany.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Krok 7: Określ rozmiar strony (konwersja dwg do jpg)

Oblicz szerokość i wysokość układu w jego natywnych jednostkach. Informacje te są niezbędne do prawidłowego ustawienia rozmiaru strony rastera.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Krok 8: Ustaw wymiary strony

Przelicz natywne jednostki (cale lub milimetry) na piksele przy użyciu metod pomocniczych dostarczonych przez Aspose.CAD. Jeśli typ jednostki jest inny, używamy surowych wartości.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Krok 9: Zapisz plik JPG

Na koniec powiąż opcje rasteryzacji z opcjami JPEG i zapisz obraz na dysku.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Po zakończeniu pętli będziesz mieć plik JPG dla każdego układu, każdy o dokładnym rozmiarze odpowiadającym oryginalnym wymiarom DWF.

## Typowe problemy i rozwiązania

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------|-----|
| Pusty plik JPG | `options.Layouts` nie jest poprawnie ustawione | Sprawdź, czy nazwa układu pasuje do `page.Name`. |
| Zniekształcony obraz | Błędna konwersja DPI | Użyj `CommonHelper.DPI = 300` (lub docelowego DPI) przed konwersją. |
| Plik nie znaleziony | Nieprawidłowa ścieżka `MyDir` | Użyj ścieżek bezwzględnych lub `Path.Combine`. |
| Wyjątek licencyjny | Nie zastosowano licencji | Załaduj tymczasową lub stałą licencję przed wywołaniem `Image.Load`. |

## Najczęściej zadawane pytania

### Pytanie 1: Czy Aspose.CAD jest kompatybilny z najnowszymi formatami plików DWG?

Aspose.CAD obsługuje różne formaty plików DWG, w tym najnowsze wersje. Zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/net/) po szczegółowe informacje o kompatybilności.

### Pytanie 2: Czy mogę używać Aspose.CAD zarówno w projektach komercyjnych, jak i prywatnych?

Tak, Aspose.CAD oferuje elastyczne opcje licencjonowania zarówno dla użytku komercyjnego, jak i prywatnego. Odwiedź [stronę zakupu](https://purchase.aspose.com/buy) po więcej szczegółów.

### Pytanie 3: Jak mogę uzyskać tymczasową licencję dla Aspose.CAD?

Możesz uzyskać tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/) do celów ewaluacyjnych.

### Pytanie 4: Gdzie mogę znaleźć wsparcie dla Aspose.CAD?

W razie pytań lub potrzeb pomocy, odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Pytanie 5: Czy dostępna jest darmowa wersja próbna Aspose.CAD?

Tak, możesz uzyskać dostęp do darmowej wersji próbnej Aspose.CAD [tutaj](https://releases.aspose.com/).

### Pytanie 6: Jak przekonwertować plik DWG bezpośrednio do JPG bez wcześniejszego wyodrębniania DWF?

Możesz załadować plik DWG przy użyciu `Aspose.CAD.Image.Load` i zastosować ten sam przepływ rasteryzacji; wystarczy ustawić `options.Layouts` na żądaną nazwę (nazwy) układu z DWG.

### Pytanie 7: Czy konwersja zachowuje jakość wektorową?

Po rasteryzacji do JPG obraz jest oparty na bitmapie, więc skalowalność wektorowa zostaje utracona. W celu skalowania bez utraty jakości rozważ eksport do PNG lub SVG.

---

**Ostatnia aktualizacja:** 2026-04-06  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}