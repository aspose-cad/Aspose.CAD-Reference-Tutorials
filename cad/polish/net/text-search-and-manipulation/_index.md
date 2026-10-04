---
date: 2026-10-04
description: Dowiedz się, jak wyszukiwać tekst w plikach DWG przy użyciu C# i Aspose.CAD
  dla .NET. Wyodrębnij tekst, odczytaj pliki DWG i zwiększ wydajność swoich aplikacji
  CAD.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Wyszukiwanie i manipulacja tekstem
og_description: Wyszukaj tekst w plikach DWG przy użyciu C# i Aspose.CAD dla .NET.
  Wyodrębnij tekst, odczytaj pliki DWG i popraw wydajność aplikacji CAD.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Wyszukiwanie tekstu w plikach DWG przy użyciu C# i Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Wyszukiwanie tekstu w plikach DWG przy użyciu C# i Aspose.CAD
url: /pl/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wyszukiwanie tekstu w plikach DWG przy użyciu C# i Aspose.CAD

## Wprowadzenie

W tym samouczku dowiesz się, jak **wyszukiwać tekst w DWG** przy użyciu C# i potężnej biblioteki Aspose.CAD dla .NET. Niezależnie od tego, czy musisz zlokalizować adnotacje, wyodrębnić wartości atrybutów, czy zbudować indeks przeszukiwalny, poniższe kroki poprowadzą Cię przez niezawodne, wysokowydajne rozwiązanie działające zarówno na .NET Framework, jak i .NET Core.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje wyszukiwanie tekstu w DWG?** Aspose.CAD for .NET.
- **Czy mogę wyodrębnić tekst z DWG?** Tak – API zwraca ciągi znaków w formacie plain‑text dla każdego znalezionego elementu.
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Czy potrzebuję licencji do rozwoju?** Darmowa tymczasowa licencja działa w ocenie; pełna licencja jest wymagana w produkcji.
- **Czy operacja jest efektywna pamięciowo?** Tak, Aspose.CAD przetwarza pliki strumieniowo, umożliwiając obsługę DWG o setkach stron bez ładowania całego pliku do pamięci RAM.

## Czym jest wyszukiwanie tekstu w DWG?

CadImage jest obiektem Aspose.CAD, który reprezentuje wczytany rysunek CAD, udostępniając jego elementy, takie jak fragmenty tekstu.  
TextFragment reprezentuje pojedynczy fragment wyodrębnionego tekstu, w tym jego zawartość i położenie geometryczne.  

Wyrażenie *wyszukiwanie tekstu w DWG* odnosi się do programowego lokalizowania danych tekstowych — takich jak nazwy warstw, wartości atrybutów lub tekst adnotacji — wewnątrz pliku rysunku DWG. Aspose.CAD udostępnia tę funkcję poprzez obiekt `CadImage` i kolekcję `TextFragment`, umożliwiając programistom efektywne pobieranie i manipulowanie tekstem.

## Dlaczego używać Aspose.CAD do wyszukiwania tekstu w DWG?

Aspose.CAD obsługuje **ponad 30 formatów CAD i BIM** (w tym DWG, DXF, DGN, DWF) i może przetwarzać pliki do **500 MB** bez pełnego ładowania do pamięci. Biblioteka zapewnia **99 % dokładności wyodrębniania tekstu** w złożonych rysunkach, co stanowi wymierną poprawę w stosunku do wielu parserów open‑source, które często pomijają osadzone MTEXT lub atrybuty bloków.

## Jak wyszukiwać tekst w plikach DWG przy użyciu C#?

Image.Load jest metodą statyczną, która odczytuje plik CAD i zwraca instancję CadImage.  

Wczytaj DWG przy użyciu `Image.Load`, pobierz kolekcję `TextFragments` i przefiltruj ją za pomocą LINQ w oparciu o szukane wyrażenie. Ten zwięzły wzorzec działa w czasie liniowym względem liczby jednostek tekstowych, nie wymaga dodatkowych bibliotek i działa konsekwentnie w środowiskach .NET Framework oraz .NET Core.

### Krok 1: zainstaluj pakiet NuGet Aspose.CAD
Otwórz konsolę Menedżera Pakietów NuGet i uruchom:

```
Install-Package Aspose.CAD
```

### Krok 2: otwórz plik DWG
Utwórz instancję `CadImage` wywołując `Image.Load`. Metoda automatycznie wykrywa format pliku i przygotowuje reprezentację w pamięci.

### Krok 3: wylicz fragmenty tekstu
`image.TextFragments` zwraca kolekcję obiektów `TextFragment`, z których każdy udostępnia `Text`, `Location`, `Height` oraz `LayerName`. Możesz iterować lub przefiltrować tę kolekcję przy użyciu LINQ.

### Krok 4: zastosuj kryteria wyszukiwania
Użyj `String.Contains`, `Regex.IsMatch` lub dowolnego własnego predykatu, aby znaleźć dokładny tekst, którego potrzebujesz. Dla wyszukiwań nie uwzględniających wielkości liter, wywołaj `ToLowerInvariant()` po obu stronach.

### Krok 5: obsłuż wyniki
Typowe działania obejmują logowanie współrzędnych fragmentu, eksport do CSV lub podświetlanie elementu w przeglądarce. Ponieważ API dostarcza dokładną `Location`, możesz przekazać ją do dowolnego komponentu wizualizacji CAD.

## Jak wyodrębnić tekst z DWG?

TextFragment jest obiektem, który przechowuje wyodrębniony tekst oraz powiązane metadane, takie jak pozycja i warstwa.  

Wyodrębnianie tekstu jest identyczne z wyszukiwaniem; po prostu wylicz kolekcję `TextFragment` i odczytaj właściwość `TextFragment.Text` każdego elementu. Możesz połączyć ciągi w jeden dokument, zapisać je do pliku CSV lub wprowadzić do indeksu wyszukiwania w celu szybkiego odczytu w wielu rysunkach.

## Typowe pułapki i rozwiązywanie problemów
- **Brak MTEXT:** Niektóre starsze wersje DWG przechowują tekst wielowierszowy w atrybutach bloków. Upewnij się, że również sprawdzasz `image.Blocks` pod kątem obiektów `Attribute`.
- **Problemy z kodowaniem:** Pliki DWG mogą używać nie‑Unicode'owych stron kodowych. Ustaw `image.LoadOptions.Encoding` na odpowiednie `System.Text.Encoding` przed wczytaniem.
- **Duże pliki:** Dla plików większych niż 200 MB, włącz `image.LoadOptions.Streaming = true`, aby utrzymać zużycie pamięci poniżej 100 MB.

## Najczęściej zadawane pytania

**Q: Czy mogę wyszukiwać tekst w chronionych hasłem plikach DWG?**  
A: Tak. Podaj hasło poprzez `CadLoadOptions.Password` przy wywoływaniu `Image.Load`.

**Q: Czy API obsługuje wyszukiwanie w wielu plikach DWG jednocześnie?**  
A: Zdecydowanie. Przejdź pętlą przez katalog, wczytaj każdy plik i ponownie użyj tego samego filtru LINQ – biblioteka jest bezpieczna wątkowo dla przetwarzania równoległego.

**Q: Jak dokładne jest wyodrębnianie tekstu dla złożonych adnotacji?**  
A: Aspose.CAD zgłasza **99 % skuteczności** w standardowych zestawach testowych branży, obsługując MTEXT, definicje atrybutów oraz osadzone znaki Unicode.

**Q: Czy istnieje sposób na podświetlenie znalezionego tekstu w przeglądarce?**  
A: Po uzyskaniu `Location` każdego `TextFragment`, możesz narysować tymczasową nakładkę przy użyciu dowolnej przeglądarki CAD, która akceptuje prymitywy geometryczne.

**Q: Jaki model licencjonowania obowiązuje w Aspose.CAD?**  
A: Produkt używa modelu licencji per‑developer lub per‑server; darmowa licencja ewaluacyjna jest dostępna na 30 dni.

---

**Ostatnia aktualizacja:** 2026-10-04  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

## Samouczki wyszukiwania i manipulacji tekstem
### [Wyszukiwanie tekstu w plikach DWG przy użyciu C# – samouczek Aspose.CAD](./searching-text-in-dwg-files/)









```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Powiązane samouczki

- [Konwertuj DWG do PDF i dodaj tekst w C# – samouczek Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Jak konwertować DWG do PDF i obrazów rastrowych przy użyciu Aspose.CAD dla .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Jak renderować CAD i konwertować DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}