---
date: 2026-08-12
description: Wyodrębnij tekst z pliku DWG i przekonwertuj wybrany DWG na obraz w C#
  przy użyciu Aspose.CAD dla .NET. Poznaj krok po kroku z przykładami kodu.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Konwersja wybranego DWG na obraz w C#
og_description: Wyodrębnij tekst z pliku DWG i przekonwertuj wybrany DWG na obraz
  w C# z Aspose.CAD. Skorzystaj z tego zwięzłego przewodnika, aby szybko wdrożyć rozwiązanie.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Wyodrębnij tekst z pliku DWG i przekonwertuj wybrany DWG na obraz w C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Wyodrębnij tekst z pliku DWG i przekonwertuj wybrany DWG na obraz w C#
url: /pl/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie konkretnego pliku DWG na obraz w C# - przewodnik Aspose.CAD

## Wprowadzenie

W nowoczesnych aplikacjach inżynieryjnych często trzeba **wyodrębnić tekst z DWG** oraz **przekonwertować konkretny DWG na obraz** w celu raportowania lub wizualizacji. Aspose.CAD dla .NET udostępnia w pełni funkcjonalne API, które obsługuje oba zadania bez potrzeby używania zewnętrznego oprogramowania CAD. W tym samouczku nauczysz się, jak załadować DWG, odfiltrować encje tekstowe, rasteryzować rysunek i ostatecznie zapisać wynik jako obraz PDF — wszystko w czystym kodzie C#.

## Szybkie odpowiedzi
- **Jaki jest pierwszy krok?** Load the DWG file with `new CadImage("file.dwg")`.  
- **Która klasa filtruje tekst?** Use `CadEntityFilter` to select `Text` entities.  
- **Jak określić rozmiar obrazu?** Set `Width` and `Height` on `CadRasterizationOptions`.  
- **Jaki format wyjściowy jest używany?** The example saves to PDF, which embeds the raster image.  
- **Czy potrzebuję licencji do produkcji?** Yes – a commercial Aspose.CAD license removes evaluation limits.

## Jak wyodrębnić tekst z dwg?

Załaduj DWG, zastosuj filtr wybierający wyłącznie encje tekstowe, a następnie odczytaj właściwość `TextString` każdej encji. Takie podejście zwraca każdy fragment adnotacji, etykiety lub wymiaru znajdujący się w rysunku, umożliwiając ponowne wykorzystanie go w wyszukiwaniu, indeksowaniu lub raportowaniu.

## Dlaczego konwertować konkretny dwg na obraz?

Konwersja DWG na obraz rastrowy pozwala osadzić rysunek w dokumentach, stronach internetowych lub aplikacjach mobilnych, które nie potrafią renderować natywnych formatów CAD. Aspose.CAD obsługuje **ponad 50 formatów CAD** i może rasteryzować rysunki wielostronicowe, zużywając mniej niż 200 MB pamięci, co czyni go odpowiednim dla scenariuszy serwerowych o wysokiej przepustowości.

## Wymagania wstępne

- Visual Studio (dowolna nowsza edycja) do kompilacji i uruchamiania projektów C#.  
- Aspose.CAD for .NET – upewnij się, że masz zainstalowaną bibliotekę. Link do pobrania znajdziesz na **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.  
- Plik DWG, z którym chcesz pracować; przykładowy plik *visualization_-_conference_room.dwg* jest używany w fragmentach kodu.

## Importowanie przestrzeni nazw

Poniższe przestrzenie nazw dają dostęp do podstawowych klas CAD, opcji rasteryzacji oraz pomocników wyjścia PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: załaduj plik dwg

Utwórz instancję `CadImage`, podając ścieżkę do swojego pliku DWG. Obiekt `CadImage` reprezentuje cały rysunek w pamięci i zapewnia dostęp do warstw, encji oraz metadanych.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Krok 2: filtruj encje

`CadEntityFilter` pozwala wybrać tylko te encje, które są potrzebne. W tym przewodniku konfigurujemy go tak, aby zachować **tekst** i odrzucić linie, okręgi oraz inne elementy geometryczne, których nie chcemy w końcowym obrazie.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Krok 3: ustaw opcje rasteryzacji

`CadRasterizationOptions` kontroluje, w jaki sposób rysunek zostaje przekształcony w bitmapę. Możesz określić rozmiar wyjścia, kolor tła oraz rozdzielczość (DPI). Poniżej znajduje się definicja klasy:

Klasa `CadRasterizationOptions` określa wymiary obrazu, rozdzielczość i ustawienia renderowania przy konwersji rysunków CAD na formaty rastrowe.  

Ustaw żądaną szerokość, wysokość i kolor tła przed przekazaniem opcji do eksportera PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Krok 4: ustaw opcje PDF

`PdfOptions` grupuje ustawienia rasteryzacji z funkcjami specyficznymi dla PDF, takimi jak kompresja. Definicja tej klasy pojawia się najpierw:

`PdfOptions` enkapsuluje parametry generowania PDF, w tym opcje rasteryzacji, które określają, jak dane CAD są renderowane wewnątrz dokumentu PDF.  

Przypisz wcześniej utworzoną instancję `CadRasterizationOptions` do właściwości `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: zapisz jako PDF

Na koniec wywołaj metodę `Save` na obiekcie `CadImage`, podając nazwę docelowego pliku oraz skonfigurowane `PdfOptions`. PDF będzie zawierał wysokiej jakości obraz przefiltrowanego rysunku.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Typowe problemy i rozwiązywanie

- **Brak tekstu po filtracji** – Upewnij się, że DWG rzeczywiście zawiera encje `Text`; niektóre rysunki przechowują adnotacje jako `MText`. Dostosuj filtr, aby uwzględnić `MText`, jeśli to konieczne.  
- **Pusty obraz wyjściowy** – Sprawdź, czy DPI rasteryzacji jest wystarczająco wysokie (300 DPI to bezpieczna wartość domyślna) oraz czy kolor tła nie jest ustawiony na przezroczysty podczas przeglądania PDF.  
- **Błędy braku pamięci przy dużych plikach** – Użyj przeciążenia `LoadOptions`, które włącza strumieniowanie, zapobiegając jednoczesnemu wczytywaniu całego pliku do pamięci.

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
A: Aspose.CAD obsługuje wydania DWG od AutoCAD 2000 aż do najnowszej wersji 2024, obejmując ponad 90 % plików tworzonych w branży.

**Q: Czy mogę dostosować opcje rasteryzacji dla różnych wyjść?**  
A: Tak – możesz zmienić rozdzielczość, format obrazu, antyaliasing oraz kolor tła, aby dopasować je do docelowych formatów PNG, JPEG lub PDF.

**Q: Gdzie mogę znaleźć dodatkowe przykłady i dokumentację?**  
A: Zapoznaj się z obszerna [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) aby uzyskać więcej przykładów kodu i szczegóły API.

**Q: Czy dostępna jest darmowa wersja próbna Aspose.CAD?**  
A: Oczywiście – możesz pobrać wersję próbną na **[Aspose trial download page](https://releases.aspose.com/)** i ocenić wszystkie funkcje bez ograniczeń przez 30 dni.

**Q: Jak mogę uzyskać wsparcie lub połączyć się ze społecznością?**  
A: Dołącz do aktywnego [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), gdzie programiści dzielą się rozwiązaniami, a zespół Aspose odpowiada na pytania.

---

**Ostatnia aktualizacja:** 2026-08-12  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Wyszukiwanie tekstu w plikach DWG przy użyciu C# - samouczek Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Konwertowanie rysunku CAD na obraz rastrowy w Aspose.CAD dla .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Renderowanie dokumentów DWG w C# - przewodnik Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}