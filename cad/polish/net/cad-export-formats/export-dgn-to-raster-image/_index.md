---
date: 2026-03-24
description: Dowiedz się, jak konwertować pliki DGN na PNG i zapisywać CAD jako JPEG
  przy użyciu Aspose.CAD dla .NET – szybki przewodnik po konwersji CAD na obrazy.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak przekonwertować DGN na PNG w Aspose.CAD dla .NET
url: /pl/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie DGN do PNG w Aspose.CAD dla .NET

W nowoczesnym rozwoju .NET, **convert dgn to png** jest powszechnym wymaganiem, gdy trzeba wyświetlić rysunki CAD w sieci lub osadzić je w raportach. Aspose.CAD dla .NET upraszcza tę konwersję, umożliwiając zamianę pliku DGN na wysokiej jakości obraz rastrowy przy użyciu kilku linijek kodu. W tym przewodniku przeprowadzimy Cię przez cały proces, od konfiguracji projektu po zapisanie ostatecznego pliku PNG (lub JPEG).

## Szybkie odpowiedzi
- **Czy mogę konwertować DGN do PNG przy użyciu Aspose.CAD?** Tak – wystarczy skonfigurować opcje rasteryzacji i wybrać wyjście PNG lub JPEG.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest ważna licencja Aspose.CAD dla wdrożeń nie‑trialowych.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Jakie formaty obrazu są dostępne?** PNG, JPEG, BMP, GIF, TIFF i inne.  
- **Czy obsługa wyjątków jest konieczna?** Zdecydowanie – otocz konwersję blokiem try/catch, aby obsłużyć problemy z dostępem do plików.

## Co to jest „convert dgn to png”?
Konwersja pliku DGN (MicroStation) do PNG oznacza rasteryzację wektorowych danych CAD do obrazu opartego na pikselach. Jest to przydatne przy generowaniu podglądów, osadzaniu rysunków w wiadomościach HTML lub tworzeniu miniatur dla systemów zarządzania dokumentami.

## Dlaczego warto używać Aspose.CAD do konwersji CAD na obraz?
- **Brak zewnętrznych zależności** – działa wyłącznie w kodzie zarządzanym.  
- **Wysoka wierność** – zachowuje grubości linii, warstwy i kolory.  
- **Elastyczny format wyjściowy** – przełączaj się między PNG, JPEG, BMP itp., zmieniając jedną opcję.  
- **Optymalizacja wydajności** – rasteryzacja jest szybka nawet dla dużych rysunków.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz:

- **Aspose.CAD for .NET** zainstalowany w projekcie. Możesz go pobrać ze [strony](https://reference.aspose.com/cad/net/).  
- Przykładowy plik DGN (np. `Nikon_D90_Camera.dgn`) umieszczony w znanym katalogu.

## Import Namespaces

Rozpocznij od dodania wymaganych dyrektyw `using`, aby uzyskać dostęp do klas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DGN

Wczytaj źródłowy plik DGN do obiektu `CadImage`. Obiekt ten reprezentuje rysunek CAD w pamięci i będzie źródłem rasteryzacji.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Krok 2: Zdefiniuj opcje rasteryzacji

Skonfiguruj, w jaki sposób rysunek CAD ma być rasteryzowany. Tutaj możesz kontrolować rozmiar obrazu, skalowanie i kolor tła.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Krok 3: Wybierz format wyjściowy (PNG lub JPEG)

Choć tutorial koncentruje się na PNG, możesz także **zapisać cad jako jpeg**. Utwórz odpowiedni obiekt opcji obrazu i podłącz ustawienia rasteryzacji.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** Aby wygenerować plik PNG, zamień `new JpegOptions()` na `new PngOptions()`.

## Krok 4: Zapisz obraz rastrowy

Na koniec wywołaj `Save` na instancji `CadImage`, podając żądaną nazwę pliku oraz skonfigurowany obiekt opcji.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Jeśli przełączyłeś się na `PngOptions`, plik zostanie zapisany jako `ExportDGNToRasterImage_out.png`.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **Pusty obraz wyjściowy** | `NoScaling` ustawione niepoprawnie lub nie wybrano układu | Ustaw `AutomaticLayoutsScaling = true` lub określ żądany układ. |
| **Brak pamięci przy dużych plikach** | Ładowanie ogromnego pliku DGN bez strumieniowania | Użyj `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Nieobsługiwana wersja DGN** | Starsze wersje MicroStation | Upewnij się, że masz najnowszą wersję Aspose.CAD obsługującą formaty starsze. |

## Frequently Asked Questions

**Q: Czy mogę eksportować pliki DGN do formatów innych niż JPEG?**  
A: Tak, Aspose.CAD for .NET obsługuje PNG, BMP, GIF, TIFF i inne – wystarczy zamienić klasę opcji (np. `new PngOptions()`).

**Q: Jak powinienem obsługiwać wyjątki podczas konwersji?**  
A: Otocz kod konwersji blokiem `try/catch` i loguj `Aspose.CAD.CadException` w celu uzyskania szczegółowych informacji o błędzie.

**Q: Czy dostępna jest wersja trial Aspose.CAD for .NET?**  
A: Tak, możesz wypróbować produkt w darmowej wersji trial. Odwiedź [tutaj](https://releases.aspose.com/) po więcej informacji.

**Q: Gdzie mogę uzyskać pomoc lub dyskutować problemy związane z Aspose.CAD for .NET?**  
A: Przejdź na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie społeczności i dyskusje.

**Q: Jak uzyskać tymczasową licencję dla Aspose.CAD for .NET?**  
A: Odwiedź [ten link](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję na potrzeby rozwoju.

## Podsumowanie

Teraz wiesz, jak **convert dgn to png** (lub JPEG) przy użyciu Aspose.CAD dla .NET. Dostosowując opcje rasteryzacji i zamieniając klasę opcji obrazu, możesz dopasować wynik do wymagań każdego projektu. Śmiało eksperymentuj z różnymi rozmiarami stron, ustawieniami DPI i formatami plików, aby uzyskać idealny obraz rastrowy dla swojej aplikacji.

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}