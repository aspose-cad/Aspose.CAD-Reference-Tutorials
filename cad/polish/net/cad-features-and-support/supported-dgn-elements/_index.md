---
date: 2026-03-29
description: Naucz się konwertować DGN na PNG przy użyciu Aspose.CAD dla .NET. Ten
  przewodnik obejmuje także obsługę formatu plików CAD oraz pełny zestaw obsługiwanych
  elementów DGN.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DGN na PNG za pomocą Aspose.CAD dla .NET
url: /pl/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DGN do PNG przy użyciu Aspose.CAD dla .NET

## Wprowadzenie

Czy jesteś programistą .NET, który chce **konwertować DGN do PNG** bezproblemowo? Aspose.CAD dla .NET zapewnia solidne rozwiązanie do efektywnego obsługiwania plików DGN. W tym samouczku przyjrzymy się obsługiwanym elementom DGN, prowadząc Cię przez proces pracy z Aspose.CAD dla .NET i pokazując dokładnie, jak wyeksportować te elementy do obrazów PNG.

## Szybkie odpowiedzi
- **Co robi Aspose.CAD?** Odczytuje, modyfikuje i konwertuje pliki CAD/BIM (w tym DGN) do formatów rastrowych, takich jak PNG.  
- **Czy mogę konwertować elementy DGN 2D i 3D?** Tak – obsługiwane są zarówno encje 2‑D, jak i 3‑D.  
- **Jakie wersje .NET są wymagane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy potrzebuję licencji do testów?** Dostępna jest bezpłatna wersja próbna; licencja jest wymagana w środowisku produkcyjnym.  
- **Gdzie mogę pobrać bibliotekę?** Pobierz ją z oficjalnej strony Aspose (link poniżej).

## Co oznacza „konwertować DGN do PNG”?
Konwersja DGN do PNG oznacza renderowanie wektorowego rysunku DGN (2‑D lub 3‑D) do formatu obrazu rastrowego (PNG). Jest to przydatne, gdy trzeba wyświetlić rysunki CAD w sieci, osadzić je w raportach lub generować miniatury bez konieczności używania przeglądarki CAD.

## Dlaczego warto używać Aspose.CAD dla .NET do obsługi formatów plików CAD?
- **Pełna obsługa formatów plików CAD** – DGN, DWG, DXF, DWF i inne.  
- **Brak zewnętrznych zależności** – czysta biblioteka .NET, bez natywnych instalacji CAD.  
- **Renderowanie o wysokiej wierności** – zachowuje grubości linii, kolory i geometrię 3‑D.  
- **Przetwarzanie wsadowe** – łatwe iterowanie wielu plików w aplikacji po stronie serwera.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

- Podstawową wiedzę o programowaniu w .NET.  
- Zainstalowane Visual Studio na komputerze.  
- Bibliotekę Aspose.CAD dla .NET, którą możesz pobrać [tutaj](https://releases.aspose.com/cad/net/).

## Importowanie przestrzeni nazw

Aby rozpocząć projekt, zaimportuj niezbędne przestrzenie nazw do swojej aplikacji .NET. Ten krok zapewnia dostęp do funkcjonalności udostępnianych przez Aspose.CAD dla .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Jak konwertować DGN do PNG

Poniżej znajduje się przewodnik krok po kroku, który prowadzi Cię przez ładowanie pliku DGN, iterację jego elementów, obsługę encji 2‑D i 3‑D oraz ostateczny eksport wyniku do obrazu rastrowego PNG.

### Krok 1: Załaduj plik DGN

Rozpocznij od załadowania istniejącego pliku DGN jako `DgnImage` w swojej aplikacji .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Krok 2: Iteruj elementy DGN

Iteruj elementy DGN przy użyciu pętli `foreach`. Aspose.CAD dla .NET udostępnia różnorodne typy elementów DGN, z którymi możesz pracować.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Krok 3: Obsługa wcześniej obsługiwanych encji 2‑D

Te encje są teraz również obsługiwane przy renderowaniu 3‑D. Instrukcja switch pozwala rozgałęzić logikę w zależności od typu elementu.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Krok 4: Obsługa obsługiwanych encji 3‑D

Aspose.CAD dodaje pełne wsparcie dla kilku elementów DGN 3‑D. Rozszerz instrukcję switch, aby przetwarzać je w razie potrzeby.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Krok 5: Eksport i zapis jako PNG

Po wszelkich niezbędnych modyfikacjach wyeksportuj rysunek DGN do obrazu rastrowego PNG i zapisz go w określonym katalogu.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Porada:** Użyj `Image.Save` z `new PngOptions()`, aby kontrolować rozdzielczość, kolor tła i inne ustawienia specyficzne dla PNG.

## Przegląd wsparcia formatów plików CAD

Aspose.CAD dla .NET nie ogranicza się tylko do DGN. Obsługuje także DWG, DXF, DWF i wiele innych formatów CAD, zapewniając jedną API do obsługi szerokiego spektrum rysunków inżynieryjnych. Dzięki temu jest idealny dla projektów wymagających **obsługi formatów plików CAD** w wielu standardach.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| **Obraz jest pusty** | Eksportowany z zerową DPI | Określ `ResolutionX` i `ResolutionY` w `PngOptions`. |
| **Brak geometrii 3‑D** | Typ elementu nieobsłużony w instrukcji switch | Dodaj brakujący przypadek `DgnElementType` i renderuj odpowiednio. |
| **Brak pamięci przy dużych plikach** | Ładowanie całego pliku jednocześnie | Przetwarzaj elementy w partiach lub używaj strumieniowania, gdy to możliwe. |

## Najczęściej zadawane pytania

### Q1: Gdzie mogę znaleźć dokumentację Aspose.CAD dla .NET?
Możesz znaleźć dokumentację [tutaj](https://reference.aspose.com/cad/net/).

### Q2: Jak pobrać Aspose.CAD dla .NET?
Możesz pobrać bibliotekę [tutaj](https://releases.aspose.com/cad/net/).

### Q3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?
Tak, możesz uzyskać dostęp do wersji próbnej [tutaj](https://releases.aspose.com/).

### Q4: Gdzie mogę uzyskać tymczasowe licencje dla Aspose.CAD dla .NET?
Tymczasowe licencje są dostępne [tutaj](https://purchase.aspose.com/temporary-license/).

### Q5: Potrzebujesz pomocy lub masz pytania?
Odwiedź społeczność Aspose.CAD dla .NET [forum wsparcia](https://forum.aspose.com/c/cad/19).

---

**Ostatnia aktualizacja:** 2026-03-29  
**Testowano z:** Aspose.CAD dla .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}