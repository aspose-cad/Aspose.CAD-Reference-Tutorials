---
date: 2026-03-21
description: Dowiedz się, jak uzyskać rozmiar układu CAD w .NET przy użyciu Aspose.CAD.
  Skorzystaj z naszego przewodnika krok po kroku, aby efektywnie manipulować plikami
  CAD.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Pobierz rozmiar układu CAD w Aspose.CAD dla .NET
url: /pl/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Pobieranie rozmiaru układu CAD w Aspose.CAD dla .NET

## Wprowadzenie

W tym obszernej tutorialu dowiesz się **jak pobrać rozmiar układu CAD** przy użyciu biblioteki Aspose.CAD dla .NET. Niezależnie od tego, czy tworzysz przeglądarkę CAD, generujesz miniatury, czy potrzebujesz precyzyjnych wymiarów układu do dalszego przetwarzania, znajomość dokładnego rozmiaru każdego układu jest niezbędna. Przeprowadzimy Cię przez cały proces – od wczytania rysunku po wyodrębnienie wymiarów układu i opcjonalne zapisanie ich jako obrazy – abyś mógł z pełnym przekonaniem wbudować tę funkcjonalność w własne aplikacje.

## Szybkie odpowiedzi
- **Co oznacza „pobieranie rozmiaru układu CAD”?** Oznacza to odczytanie szerokości i wysokości (w jednostkach rysunku) każdego nie‑pustego układu w pliku CAD.  
- **Która biblioteka to obsługuje?** Aspose.CAD dla .NET udostępnia prostą API do uzyskiwania informacji o układach.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Obsługiwane formaty?** DWG, DXF i wiele innych formatów CAD/BIM jest w pełni obsługiwanych.  
- **Typowy czas implementacji?** Około 10‑15 minut dla podstawowej procedury pobierania rozmiaru.

## Co to jest „pobieranie rozmiaru układu CAD”?
Pobieranie rozmiaru układu CAD oznacza wyodrębnienie geometrycznych granic każdego układu (przestrzeni papieru) zdefiniowanego w rysunku CAD. Granice te wyrażane są w natywnych jednostkach rysunku (zazwyczaj milimetrach lub calach) i są przydatne przy skalowaniu, drukowaniu lub generowaniu podglądów.

## Dlaczego pobierać rozmiar układu CAD przy użyciu Aspose.CAD?
- **Brak wymogu posiadania oprogramowania CAD** – działa w pełni po stronie serwera.  
- **Wieloplatformowość** – działa z .NET Framework, .NET Core oraz .NET 5/6+.  
- **Dokładne pomiary** – zwraca dokładne granice tak, jak są zapisane w pliku, eliminując ręczne parsowanie.  
- **Łatwa integracja** – proste wywołania API naturalnie wpasowują się w istniejące projekty C#.

## Wymagania wstępne

Zanim przejdziesz do kodu, upewnij się, że masz następujące elementy:

- Aspose.CAD dla .NET zainstalowane. Możesz pobrać ją ze [strony pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).
- Jeden lub więcej plików CAD (DWG, DXF itp.), które chcesz przeanalizować. W tym przewodniku użyto plików `conic_pyramid.dxf` oraz `Bottom_plate.dwg` jako przykładów.

## Importowanie przestrzeni nazw

W swoim projekcie .NET rozpocznij od zaimportowania wymaganych przestrzeni nazw:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Ustawienie katalogu dokumentów

Zdefiniuj folder, w którym znajdują się Twoje pliki CAD. Zamień symbol zastępczy na rzeczywistą ścieżkę w swoim systemie.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Określenie ścieżek do plików CAD

Utwórz tablicę wskazującą na każdy plik CAD, który chcesz przetworzyć.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Krok 3: Iteracja po plikach CAD

Wczytaj każdy plik, wykryj jego format i przygotuj się do wyodrębnienia informacji o układach.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Krok 4: Pobieranie nie‑pustych układów

Potrzebujemy metody pomocniczej, która zwróci tylko te układy, które faktycznie zawierają elementy rysunku. Puste układy są pomijane, ponieważ nie mają rozmiaru do zgłoszenia.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Krok 5: Pobieranie układów dla plików DWG

Pliki DWG przechowują informacje o układach w tabeli `HeaderVariables`. Poniższa metoda wyodrębnia nazwy wszystkich nie‑pustych układów w rysunku DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Krok 6: Pobieranie układów dla plików DXF

Pliki DXF używają innej struktury. Ta metoda przetwarza kolekcję `Tables`, aby znaleźć układy przestrzeni papieru zawierające elementy.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Krok 7: Pobieranie rozmiaru układu i zapisywanie jako obraz

Na koniec przeiteruj każdy wykryty układ, odczytaj jego granice i opcjonalnie wyrenderuj układ do pliku obrazu w celu wizualnej weryfikacji.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Typowe problemy i wskazówki

- **Brak nazw układów:** Upewnij się, że plik CAD rzeczywiście zawiera układy przestrzeni papieru; niektóre pliki mają tylko przestrzeń modelu.  
- **Nieprawidłowe jednostki:** Rozmiar zwracany jest w natywnych jednostkach rysunku. W razie potrzeby przelicz go na milimetry lub cale.  
- **Wydajność:** Ładowanie bardzo dużych plików DWG/DXF może być intensywne pod względem pamięci; rozważ przetwarzanie asynchroniczne lub w partiach.

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?**  
O: Tak, Aspose.CAD obsługuje szeroką gamę formatów, w tym DWG, DXF, DGN oraz wiele typów plików BIM.

**P: Czy mogę dostosować opcje zapisu obrazu?**  
O: Oczywiście! Możesz zmienić `CadRasterizationOptions` (format, rozdzielczość, kolor tła itp.), aby dopasować je do swoich potrzeb.

**P: Gdzie znajdę dodatkową dokumentację?**  
O: Odwiedź [dokumentację Aspose.CAD](https://reference.aspose.com/cad/net/) po szczegółowe odniesienia API i więcej przykładów.

**P: Czy dostępna jest darmowa wersja próbna?**  
O: Tak, możesz wypróbować Aspose.CAD korzystając z [darmowej wersji próbnej](https://releases.aspose.com/).

**P: Jak uzyskać wsparcie techniczne?**  
O: W sprawach technicznych odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Ostatnia aktualizacja:** 2026-03-21  
**Testowane z:** Aspose.CAD 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}