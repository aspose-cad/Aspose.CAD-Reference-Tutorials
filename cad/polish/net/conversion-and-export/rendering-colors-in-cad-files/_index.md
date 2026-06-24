---
date: 2026-04-03
description: Dowiedz się, jak renderować pliki CAD i konwertować DWG na PNG przy użyciu
  Aspose.CAD dla .NET. Przewodnik krok po kroku, jak zapisać CAD jako obraz.
keywords:
- how to render cad
- convert dwg to png
- export cad to png
- save cad as image
- load dwg in .net
linktitle: Renderowanie kolorów w plikach CAD
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak renderować pliki CAD z kolorami – przewodnik Aspose.CAD
url: /pl/net/conversion-and-export/rendering-colors-in-cad-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak renderować pliki CAD z kolorami – przewodnik Aspose.CAD

## Wprowadzenie

Czy zmagasz się z **jak renderować CAD** plikami w żywych kolorach przy użyciu .NET? W tym obszernej, krok po kroku, instrukcji pokażemy dokładnie, jak renderować kolory w plikach CAD, konwertować DWG na PNG i zapisywać rysunki CAD jako obrazy wysokiej jakości przy użyciu biblioteki Aspose.CAD.

## Szybkie odpowiedzi
- **Jaka biblioteka jest najlepsza do renderowania kolorów CAD?** Aspose.CAD for .NET  
- **Czy mogę przekonwertować DWG na PNG w jednym kroku?** Tak – rasteryzuj DWG i zapisz jako PNG.  
- **Czy potrzebuję licencji do użytku produkcyjnego?** Tymczasowa licencja działa w testach; pełna licencja jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Czy proces jest wystarczająco szybki do konwersji wsadowej?** Renderowanie odbywa się w pamięci i jest odpowiednie do operacji masowych.

## Co to jest renderowanie kolorów w plikach CAD?

Renderowanie kolorów oznacza pobranie informacji wektorowych zapisanych w rysunku CAD (DWG, DXF itp.) i rasteryzację ich do obrazu bitmapowego przy zachowaniu oryginalnych kolorów obiektów. Jest to niezbędne, gdy trzeba udostępnić wizualizacje CAD interesariuszom, którzy nie posiadają oprogramowania CAD.

## Dlaczego warto używać Aspose.CAD do konwersji DWG na PNG?

- **Brak zewnętrznych zależności** – działa całkowicie offline.  
- **Pełna wierność** – kolory obiektów, grubości linii i warstwy są zachowane.  
- **Proste API** – jednowierszowy kod do ładowania, konfigurowania i zapisywania.  
- **Wieloplatformowy** – działa na środowiskach .NET w Windows, Linux i macOS.  

## Wymagania wstępne

- Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD z [tutaj](https://releases.aspose.com/cad/net/).  
- Środowisko programistyczne: Upewnij się, że masz skonfigurowane środowisko programistyczne .NET.  
- Plik CAD: Przygotuj przykładowy plik CAD do testów. Możesz użyć „test1.dwg” w tym samouczku.

## Importowanie przestrzeni nazw

W swoim projekcie .NET zaimportuj niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD. Dodaj następujące linie na początku swojego kodu:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Krok 1: Konfiguracja projektu

Utwórz nowy projekt .NET i skonfiguruj wymagane katalogi. Upewnij się, że biblioteka Aspose.CAD jest dodana jako odwołanie w Twoim projekcie.

## Krok 2: Definiowanie ścieżek plików

Określ ścieżki do pliku CAD wejściowego oraz pliku PNG wyjściowego. Zaktualizuj następujące linie w swoim kodzie:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## Krok 3: Ładowanie pliku CAD

Użyj poniższego kodu, aby otworzyć i załadować plik CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## Krok 4: Konfiguracja opcji rasteryzacji

Skonfiguruj opcje rasteryzacji, aby dostosować proces renderowania. Zaktualizuj następujące linie:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## Krok 5: Zapis renderowanego obrazu

Zapisz renderowany obraz przy użyciu określonych opcji:

```csharp
document.Save(output, saveOptions);
```

## Dlaczego to jest ważne

Zapisywanie CAD jako obrazu (PNG, JPEG itp.) jest powszechnym wymogiem, gdy trzeba osadzić rysunki w raportach, stronach internetowych lub załącznikach e‑mail. Opanowując **jak renderować CAD**, eliminujesz potrzebę używania zewnętrznych przeglądarek i zapewniasz spójny wygląd wizualny na wszystkich platformach.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| Pusty obraz wyjściowy | `NoScaling` ustawione na `true` przy zerowych wymiarach | Upewnij się, że `PageHeight` i `PageWidth` są obliczane na podstawie załadowanego obrazu (jak pokazano). |
| Kolory wyświetlane niepoprawnie | Nieprawidłowy `DrawType` | Użyj `CadDrawTypeMode.UseObjectColor`, aby zachować oryginalne kolory obiektów. |
| Plik nie znaleziony | Niepoprawna ścieżka `MyDir` | Sprawdź, czy ścieżka katalogu kończy się ukośnikiem lub użyj `Path.Combine`. |
| Brak pamięci przy dużych plikach | Renderowanie przy bardzo wysokim DPI | Zmniejsz współczynnik skalowania (np. `*5` zamiast `*10`). |

## Zakończenie

Gratulacje! Pomyślnie nauczyłeś się **jak renderować CAD** pliki, konwertować DWG na PNG oraz **zapisywać CAD jako obraz** przy użyciu Aspose.CAD dla .NET. Ta wiedza pozwala zintegrować renderowanie CAD bezpośrednio w aplikacjach, automatyzując generowanie raportów, podglądy internetowe i wiele innych.

## FAQ

### P1: Czy mogę używać Aspose.CAD za darmo?

Aspose.CAD oferuje wersję próbną dostępną [tutaj](https://releases.aspose.com/). Możesz przetestować jej funkcje przed zakupem.

### P2: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD?

Zapoznaj się z dokumentacją [tutaj](https://reference.aspose.com/cad/net/) aby uzyskać szczegółowe informacje o funkcjonalnościach Aspose.CAD.

### P3: Jak uzyskać tymczasową licencję dla Aspose.CAD?

Uzyskaj tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/) do celów testowych.

### P4: Potrzebujesz pomocy lub masz pytania?

Odwiedź społeczność Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia i dyskusji.

### P5: Gdzie mogę kupić bibliotekę Aspose.CAD?

Kup bibliotekę Aspose.CAD [tutaj](https://purchase.aspose.com/buy), aby odblokować jej pełny potencjał.

## Dodatkowe często zadawane pytania

**P: Jak mogę **konwertować DWG na PNG** bez utraty grubości linii?**  
A: Zachowaj domyślne skalowanie `PageHeight` i `PageWidth` (np. pomnóż przez 10) oraz ustaw `options.DrawType` na `UseObjectColor`. To zachowuje grubość linii i kolory.

**P: Czy możliwe jest **eksportowanie CAD do PNG** w usłudze w tle?**  
A: Tak. API Aspose.CAD jest bezpieczne wątkowo dla operacji tylko do odczytu, więc możesz ładować i rasteryzować pliki w tle w workerze.

**P: Czy mogę **ładować DWG w .NET** z tablicy bajtów zamiast z pliku?**  
A: Oczywiście. Użyj `Image.Load(byteArray)` zamiast `FileStream` i postępuj zgodnie z tymi samymi krokami rasteryzacji.

**P: Jaki format wybrać dla najlepszej jakości przy **zapisywaniu CAD jako obrazu**?**  
A: PNG zapewnia bezstratną kompresję i zachowuje wierność kolorów, co czyni go idealnym dla rysunków technicznych.

**P: Czy Aspose.CAD obsługuje inne formaty rastrowe, takie jak JPEG lub BMP?**  
A: Tak – po prostu zamień `PngOptions` na `JpegOptions` lub `BmpOptions` i dostosuj ustawienia specyficzne dla formatu.

---

**Ostatnia aktualizacja:** 2026-04-03  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}