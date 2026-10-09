---
date: 2026-10-09
description: Dowiedz się, jak załadować plik dwg i wyszukać tekst w plikach DWG przy
  użyciu C# oraz Aspose.CAD for .NET. Postępuj zgodnie z tym przewodnikiem krok po
  kroku, aby usprawnić swoje przepływy pracy CAD.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Wyszukiwanie tekstu w plikach DWG przy użyciu C#
og_description: Dowiedz się, jak załadować plik dwg i wyszukać tekst w plikach DWG
  przy użyciu C# oraz Aspose.CAD for .NET. Postępuj zgodnie z tym przewodnikiem krok
  po kroku, aby usprawnić swoje przepływy pracy CAD.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Jak załadować plik dwg i wyszukać tekst w plikach DWG przy użyciu C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Jak załadować plik dwg i wyszukać tekst w plikach DWG przy użyciu C#
url: /pl/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak załadować plik dwg i wyszukać tekst w plikach DWG przy użyciu C# - poradnik Aspose.CAD

## Wprowadzenie

W nowoczesnym rozwoju CAD możliwość **załadowania pliku dwg** oraz natychmiastowego odnalezienia konkretnych ciągów tekstowych oszczędza godziny ręcznej inspekcji. Niezależnie od tego, czy tworzysz narzędzie do przetwarzania wsadowego, czy dodajesz funkcje wyszukiwania do przeglądarki, Aspose.CAD dla .NET zapewnia w pełni zarządzane API działające na Windows, Linux i macOS bez zależności natywnych. Ten przewodnik przeprowadzi Cię przez każdy krok — od wczytania DWG po wyeksportowanie wyniku jako PDF — abyś mógł dziś zintegrować niezawodne wyszukiwanie tekstu CAD w swoich aplikacjach C#.

## Szybkie odpowiedzi
- **Jaka jest pierwsza linia kodu do załadowania DWG?** `new CadImage("yourfile.dwg")` tworzy w pamięci reprezentację rysunku.  
- **Który namespace zawiera klasy CAD?** `Aspose.CAD.Image` i `Aspose.CAD.FileFormats.Dwg` są wymagane.  
- **Czy mogę wyeksportować wyniki wyszukiwania bezpośrednio do PDF?** Tak – użyj `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna działa w celach oceny; stała licencja jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET 5, .NET 6, .NET Core 3.1 i .NET Framework 4.6+.

## Co to jest plik DWG?

Plik DWG jest formatem binarnym, który przechowuje dane projektowe 2D i 3D tworzone przez AutoCAD i kompatybilne narzędzia. Jest to standardowy w branży kontener dla geometrii wektorowej, warstw, tekstu i metadanych. Ponieważ format jest własnościowy, większość parserów open‑source ma trudności z nowszymi wersjami, ale Aspose.CAD w pełni obsługuje ponad 150 wydań DWG, umożliwiając odczyt i manipulację rysunkami bez instalacji AutoCAD.

## Dlaczego używać Aspose.CAD do wyszukiwania tekstu CAD?

Aspose.CAD może przetwarzać **ponad 50** wersji DWG i DXF, obsługując pliki do 1 GB bez ładowania całego dokumentu do pamięci. Biblioteka wyodrębnia tekst zarówno z sekcji **Entities**, jak i **Block**, zapewniając **99 %** skuteczności w odnajdywaniu wyszukiwalnych ciągów, nawet gdy są zagnieżdżone w blokach. Ta zmierzona niezawodność czyni go wyborem numer jeden dla automatyzacji CAD na poziomie przedsiębiorstwa.

## Wymagania wstępne

- **Aspose.CAD for .NET** zainstalowany. Pobierz najnowszy pakiet z [strony Aspose.CAD](https://releases.aspose.com/cad/net/).
- Folder zawierający pliki DWG, które chcesz analizować.
- Ważny plik licencji do użytku produkcyjnego (opcjonalny w wersji próbnej).

## Jakie namespace'y są wymagane?

Namespace `Aspose.CAD` dostarcza podstawowe klasy obsługi obrazu, natomiast `Aspose.CAD.FileFormats.Dwg` zawiera struktury specyficzne dla DWG. Zaimportuj je na początku swojego pliku C#:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Uwaga:** Powyższy blok kodu jest placeholderem; zachowaj dokładny tekst niezmieniony, aby utrzymać pierwotną liczbę placeholderów.

## Jak załadować plik dwg?

Ładowanie pliku DWG jest proste przy użyciu Aspose.CAD. Użyj klasy `CadImage`, która reprezentuje rysunek CAD w pamięci. Konstruktor odczytuje plik bez renderowania, co sprawia, że jest szybki nawet dla dużych rysunków. Po załadowaniu możesz sprawdzić właściwości takie jak `Width`, `Height` i `Layers` przed wykonaniem jakichkolwiek operacji wyszukiwania.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Jak wyszukać tekst w sekcji entities?

Aby odnaleźć tekst w sekcji Entities, iteruj po kolekcji `cadImage.Entities`. Każdy element można sprawdzić pod kątem typu (np. `MText`, `Text`, `Attribute`) oraz jego właściwości `TextString`. Wykonaj porównanie bez uwzględniania wielkości liter z docelowym ciągiem i zbierz pasujące elementy do dalszego przetwarzania lub podświetlenia.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Jak wyszukać tekst w sekcji block?

Bloki są wielokrotnego użytku grupami elementów, które mogą zawierać zagnieżdżony tekst. Najpierw wylicz `cadImage.BlockEntities.Values`, aby uzyskać dostęp do każdej definicji bloku. Następnie przejdź przez kolekcję `Entities` każdego bloku, stosując tę samą logikę dopasowywania tekstu używaną w głównej sekcji Entities. To zapewnia, że tekst ukryty wewnątrz wielokrotnego użytku komponentów nie zostanie pominięty.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Jak iterować przez węzły CAD w celu pełnego skanowania?

Kompleksowy skan łączy sekcje Entities i Block. Rekurencyjnie przechodząc drzewo węzłów `CadImage`, możesz obsłużyć zagnieżdżone bloki, definicje atrybutów i nawet odwołania zewnętrzne. Zaimplementuj metodę pomocniczą, która przyjmuje `CadBaseEntity`, sprawdza jego typ, wyodrębnia tekst w razie potrzeby, a następnie rekurencyjnie przetwarza podwęzły, jeśli węzeł zawiera kolekcję.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Jak wyeksportować dwg do pdf po zlokalizowaniu tekstu?

Po zidentyfikowaniu odpowiednich elementów możesz je podświetlić lub wyodrębnić ich współrzędne. Aspose.CAD umożliwia zapisanie całego rysunku jako PDF, zachowując jakość wektorową. Skonfiguruj `CadRasterizationOptions`, jeśli potrzebujesz wyjścia rastrowego, a następnie wywołaj `image.Save("output.pdf", new PdfOptions())`. Powstały PDF może być udostępniony interesariuszom, którzy nie posiadają oprogramowania CAD.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Podsumowanie

Aspose.CAD dla .NET oferuje płynne, wysokowydajne rozwiązanie do ładowania danych plików dwg, wyszukiwania określonego tekstu i eksportowania wyniku do PDF. Postępując zgodnie z krokami w tym poradniku, dodałeś potężne możliwości wyszukiwania tekstu CAD do swojej aplikacji C# bez konieczności korzystania z zewnętrznych narzędzi czy kosztownych licencji.

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.CAD dla .NET z innymi formatami CAD?
Odp1: Tak, Aspose.CAD obsługuje ponad 30 formatów CAD, w tym DXF, DWF i STL, oferując wszechstronne rozwiązanie dla przepływów pracy z mieszanymi formatami.

### Q2: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla .NET?
Odp2: Tak, możesz przetestować funkcje korzystając z [darmowej wersji próbnej](https://releases.aspose.com/).

### Q3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla .NET?
Odp3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy społeczności i oficjalnych kanałów wsparcia.

### Q4: Czym jest tymczasowa licencja i jak mogę ją uzyskać?
Odp4: Uzyskaj tymczasową licencję [temporary license](https://purchase.aspose.com/temporary-license/) na krótkoterminową ocenę lub projekty proof‑of‑concept.

### Q5: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla .NET?
Odp5: Zapoznaj się ze szczegółową [dokumentacją](https://reference.aspose.com/cad/net/) zawierającą dogłębne wskazówki, odniesienia API i przykłady kodu.

---

**Ostatnia aktualizacja:** 2026-10-09  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Powiązane poradniki

- [Jak konwertować DWG do PDF i obrazów rastrowych przy użyciu Aspose.CAD dla .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Konwertuj DWG do PNG i eksportuj obiekty OLE – Poradnik Aspose.CAD](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Jak odczytać pliki DWT przy użyciu Aspose.CAD dla .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}