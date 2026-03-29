---
date: 2026-03-29
description: Dowiedz się, jak skonfigurować opcje rasteryzacji CAD i eksportować pliki
  DGN do PDF z obsługą 3D przy użyciu Aspose.CAD dla .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Skonfiguruj opcje rasteryzacji CAD dla DGN V7 3D
url: /pl/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skonfiguruj opcje rasteryzacji CAD dla DGN V7 3D

## Wprowadzenie

W tym obszernym samouczku dowiesz się **jak skonfigurować opcje rasteryzacji CAD**, aby wyeksportować plik 3‑D DGN V7 do PDF przy użyciu Aspose.CAD dla .NET. Niezależnie od tego, czy tworzysz przeglądarkę CAD, narzędzie raportujące, czy zautomatyzowany potok konwersji, opanowanie tych ustawień daje Ci precyzyjną kontrolę nad rozmiarem strony, skalowaniem układu, kolorami tła oraz konkretnymi widokami, które chcesz renderować. Przejdźmy krok po kroku przez proces.

## Szybkie odpowiedzi
- **Co oznacza „konfiguracja opcji rasteryzacji CAD”?**  
  Odnosi się do ustawiania właściwości takich jak wymiary strony, skalowanie, kolor tła i wybór układu przed konwersją pliku CAD do formatu rastrowego (np. PDF).
- **Jak wyeksportować DGN do PDF z obsługą 3‑D?**  
  Załaduj DGN przy użyciu `DgnImage`, zdefiniuj `PdfOptions` + `CadRasterizationOptions`, a następnie wywołaj `Save`.
- **Czy potrzebna jest licencja do użytku produkcyjnego?**  
  Tak – wymagana jest licencja komercyjna do wdrożenia; dostępna jest darmowa wersja próbna.
- **Jakie wersje .NET są obsługiwane?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Czy mogę wybrać konkretne widoki do eksportu?**  
  Oczywiście – ustaw tablicę `Layouts` w opcjach rasteryzacji.

## Czym jest „konfiguracja opcji rasteryzacji CAD”?

Konfiguracja opcji rasteryzacji CAD oznacza dostosowanie sposobu rasteryzacji rysunku CAD (konwersji z wektora na bitmapę lub PDF). Poprzez regulację tych ustawień kontrolujesz wygląd wyjściowy, wydajność oraz rozmiar pliku powstałego dokumentu.

## Dlaczego używać Aspose.CAD do eksportu 3‑D DGN V7?

- **Pełna integracja z .NET** – nie wymaga COM ani natywnych bibliotek DLL.  
- **Obsługa geometrii 3‑D** – zachowuje informacje o głębokości przy renderowaniu do PDF.  
- **Precyzyjna kontrola** – wybierz dokładne układy, skalowanie i kolory tła.  
- **Wieloplatformowość** – działa na Windows, Linux i macOS z .NET Core.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- **Aspose.CAD for .NET** – pobierz go z [tutaj](https://releases.aspose.com/cad/net/).  
- **Visual Studio** lub dowolne kompatybilne środowisko IDE .NET.  
- **Przykładowy plik DGN** – w tym przewodniku użyjemy `Nikon_D90_Camera.dgn` (zawartego w pakiecie przykładów Aspose).  

Teraz, gdy wszystko jest gotowe, przejdźmy do kodu.

## Importowanie przestrzeni nazw

W swoim projekcie .NET zaimportuj wymagane przestrzenie nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Ustaw katalog dokumentu

Utwórz zmienną wskazującą folder, w którym będą znajdować się źródłowy plik DGN oraz pliki wyjściowe.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Załaduj plik DGN

Załaduj plik DGN jako `DgnImage`. Ten obiekt zapewnia dostęp do danych CAD oraz pipeline rasteryzacji.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Krok 3: Skonfiguruj opcje eksportu PDF (Konfiguracja opcji rasteryzacji CAD)

Tutaj **konfigurujemy opcje rasteryzacji CAD**, które określają, jak model 3‑D jest renderowany do PDF. Możesz dostosować rozmiar strony, włączyć automatyczne skalowanie układów, ustawić kolor tła oraz wybrać dokładne układy (widoki), które chcesz wyeksportować.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Krok 4: Zapisz obraz rastrowy

Na koniec wyeksportuj DGN do pliku PDF, używając właśnie skonfigurowanych opcji.

```csharp
dgnImage.Save(outFile, options);
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Pusty wynik PDF** | Sprawdź, czy tablica `Layouts` zawiera prawidłowe identyfikatory widoków obecne w pliku DGN. |
| **Nieprawidłowe kolory** | Upewnij się, że `BackgroundColor` jest ustawiony na żądaną wartość; użyj `Color.White` dla jasnego tła. |
| **Wąskie gardło wydajności przy dużych plikach** | Włącz `AutomaticLayoutsScaling` i rozważ zmniejszenie `PageWidth/PageHeight` dla niższej rozdzielczości rastrowej. |
| **Wyjątek licencyjny** | Zainstaluj ważną licencję Aspose.CAD przed załadowaniem obrazu, aby uniknąć znaków wodnych wersji próbnej. |

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD dla .NET z innymi formatami plików CAD?**  
O: Tak, Aspose.CAD obsługuje DWG, DXF, DWF, DGN i wiele innych formatów.

**P: Jak mogę obsługiwać wyjątki podczas pracy z Aspose.CAD?**  
O: Otocz swój kod blokiem `try‑catch` i sprawdzaj `Aspose.CAD.CADException` w celu uzyskania szczegółowych informacji o błędach.

**P: Czy Aspose.CAD jest odpowiedni dla projektów komercyjnych?**  
O: Zdecydowanie tak. Możesz zakupić licencję [tutaj](https://purchase.aspose.com/buy).

**P: Czy mogę wypróbować Aspose.CAD dla .NET przed zakupem?**  
O: Tak, dostępna jest darmowa wersja próbna [tutaj](https://releases.aspose.com/).

**P: Gdzie mogę znaleźć wsparcie społeczności dla Aspose.CAD?**  
O: Dołącz do forum dyskusyjnego [tutaj](https://forum.aspose.com/c/cad/19).

---

**Ostatnia aktualizacja:** 2026-03-29  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}