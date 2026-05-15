---
date: 2026-03-07
description: Dowiedz się, jak eksportować pliki CAD do SVG przy użyciu Aspose.CAD
  dla .NET, dostosować kolor SVG oraz efektywnie konwertować DWG na SVG.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Eksport CAD do SVG – Eksport rysunków CAD do formatu SVG – Przewodnik Aspose.CAD
url: /pl/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport CAD do SVG – Eksport rysunków CAD do formatu SVG

## Wprowadzenie

Eksportowanie rysunków CAD do SVG jest powszechnym wymogiem, gdy potrzebujesz grafiki niezależnej od rozdzielczości dla stron internetowych, raportów lub interaktywnych wizualizacji. W tym samouczku dowiesz się **jak eksportować CAD do SVG** przy użyciu Aspose.CAD for .NET, poznasz opcje **dostosowywania koloru SVG** oraz zobaczysz, jak **konwertować DWG do SVG** (lub DXF do SVG) w zaledwie kilku linijkach kodu. Kroki są szybkie, API jest intuicyjne, a powstałe pliki SVG skalują się perfekcyjnie na każdym urządzeniu.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje konwersję?** Aspose.CAD for .NET.  
- **Czy mogę zmienić tryb kolorów?** Tak – użyj `SvgColorMode`, aby ustawić odcienie szarości, czarno‑biały lub pełny kolor.  
- **Jakie formaty CAD są obsługiwane?** DWG, DXF i wiele innych (zobacz dokumentację Aspose.CAD).  
- **Czy potrzebuję licencji do rozwoju?** Dostępna jest tymczasowa licencja do testów.  
- **Jak długo trwa konwersja?** Zazwyczaj poniżej sekundy dla standardowych rysunków.

## Co to jest „eksport CAD do SVG”?
Eksport CAD do SVG oznacza wzięcie natywnego pliku CAD (takiego jak DWG lub DXF) i wyrenderowanie go w formacie Scalable Vector Graphics. SVG jest oparty na XML, jest lekki i może być stylizowany przy użyciu CSS — co czyni go idealnym dla nowoczesnych aplikacji internetowych i mobilnych.

## Dlaczego używać Aspose.CAD do eksportu CAD do SVG?
- **Brak zewnętrznych zależności** – czyste API .NET, nie wymaga instalacji AutoCAD.  
- **Precyzyjna kontrola** – możesz **dostosować kolor SVG**, zdecydować, czy tekst ma pozostać jako kształty, oraz wybrać opcje rasteryzacji.  
- **Szerokie wsparcie formatów** – ten sam kod działa dla **konwersji DWG do SVG**, **konwersji DXF do SVG** i innych formatów, upraszczając bazę kodu.  
- **Wysoka wydajność** – zoptymalizowane pod kątem szybkości i niskiego zużycia pamięci, odpowiednie do przetwarzania wsadowego.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

- **Aspose.CAD for .NET** zainstalowane. Bibliotekę możesz pobrać [tutaj](https://releases.aspose.com/cad/net/).  
- Środowisko programistyczne .NET (Visual Studio, Rider lub .NET CLI).  
- Plik CAD (DWG lub DXF), który chcesz przekonwertować.

## Importowanie przestrzeni nazw

Najpierw wprowadź wymagane przestrzenie nazw do swojego projektu, aby klasy były dostępne.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog dokumentu  
Zdefiniuj folder, w którym znajduje się źródłowy plik CAD oraz w którym zostanie zapisany wynikowy plik SVG.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Krok 2: Załaduj rysunek CAD  
Użyj `Image.Load`, aby odczytać plik DWG (lub DXF). Działa to w scenariuszach **load DWG .NET**.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Krok 3: Skonfiguruj opcje eksportu SVG  
Dostosuj ustawienia eksportu do swoich potrzeb. Tutaj ustawiamy tryb koloru na odcienie szarości i wymuszamy renderowanie całego tekstu jako kształtów wektorowych.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Krok 4: Zapisz plik SVG  
Na koniec zapisz plik SVG na dysku. Ten krok **zapisuje CAD jako SVG** i kończy konwersję.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Postępując zgodnie z tymi czterema zwięzłymi krokami, możesz **konwertować DWG do SVG** (lub **konwertować DXF do SVG**) z pełną kontrolą nad wyglądem wyniku.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **Pusty wynik SVG** | Ścieżka do pliku źródłowego jest nieprawidłowa lub plik jest uszkodzony. | Sprawdź `MyDir` i upewnij się, że plik CAD otwiera się bez błędów. |
| **Kolory wyglądają nieprawidłowo** | `SvgColorMode` ustawiony na Grayscale nieumyślnie. | Zmień `options.ColorType` na `SvgColorMode.FullColor`, aby zachować oryginalne kolory. |
| **Brak tekstu** | `TextAsShapes` ustawiony na `false` i przeglądarka nie obsługuje wbudowanych czcionek. | Ustaw `TextAsShapes = true` lub osadź wymagane czcionki w SVG. |

## FAQ

### Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami CAD?
A1: Aspose.CAD obsługuje różne formaty CAD, w tym DWG i DXF, zapewniając szeroką kompatybilność.

### Q2: Czy mogę dostosować tryb kolorów przy eksporcie do SVG?
A2: Tak, Aspose.CAD pozwala wybrać tryb kolorów, zapewniając elastyczność w wyniku.

### Q3: Czy dostępne są tymczasowe licencje do celów testowych?
A3: Tak, możesz uzyskać tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/) do oceny.

### Q4: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD?
A4: Dokumentacja jest dostępna [tutaj](https://reference.aspose.com/cad/net/).

### Q5: Jak mogę uzyskać wsparcie lub zadać pytania dotyczące Aspose.CAD?
A5: Odwiedź forum społeczności [tutaj](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia i dyskusji.

## Najczęściej zadawane pytania

**Q: Czy mogę używać tego kodu z .NET Core lub .NET 6?**  
A: Oczywiście. Aspose.CAD for .NET jest kompatybilny z .NET Framework, .NET Core oraz .NET 5/6+.

**Q: Czy możliwe jest wyeksportowanie tylko konkretnego układu lub warstwy?**  
A: Tak. Użyj `SvgOptions`, aby ustawić `PageIndex` lub przefiltrować warstwy przed zapisem.

**Q: Jak wstawić własne style CSS do wygenerowanego SVG?**  
A: Po zapisaniu możesz przetworzyć XML SVG, aby wstrzyknąć elementy `<style>`, lub użyć `options.CustomCss`, jeśli jest dostępne w nowszych wersjach.

**Q: Jakie istnieją limity rozmiaru dla źródłowego pliku CAD?**  
A: Biblioteka obsługuje duże pliki, ale zużycie pamięci rośnie wraz ze złożonością. Dla bardzo dużych rysunków rozważ przetwarzanie stron pojedynczo.

**Q: Czy konwersja zachowuje grubość i typy linii?**  
A: Domyślnie grubość linii jest zachowywana. Możesz dostosować opcje renderowania w `SvgOptions` dla większej precyzji.

**Ostatnia aktualizacja:** 2026-03-07  
**Testowano z:** Aspose.CAD for .NET 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}