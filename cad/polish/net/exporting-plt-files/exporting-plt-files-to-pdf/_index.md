---
date: 2026-08-12
description: Dowiedz się, jak konwertować PLT do PDF przy użyciu Aspose.CAD dla .NET
  – szybki sposób na zapis CAD jako PDF z pełnym wsparciem formatu.
keywords:
- convert plt to pdf
- save cad as pdf
- cad file to pdf
- export plt as pdf
- cad plt to pdf
lastmod: 2026-08-12
linktitle: Eksportowanie plików PLT do PDF
og_description: Dowiedz się, jak konwertować PLT do PDF przy użyciu Aspose.CAD dla
  .NET – szybki sposób na zapis CAD jako PDF z pełnym wsparciem formatu.
og_image_alt: Guide showing how to convert PLT files to PDF using Aspose.CAD for .NET
og_title: Konwertuj PLT do PDF przy użyciu Aspose.CAD dla .NET – samouczek
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Learn how to convert PLT to PDF using Aspose.CAD for .NET – a fast
    way to save CAD as PDF with full format support.
  headline: Convert PLT to PDF with Aspose.CAD for .NET – tutorial
  type: TechArticle
- questions:
  - answer: '`CadImage` loads and rasterizes PLT files.'
    question: What is the primary class?
  - answer: Only two lines are needed for the actual conversion.
    question: How many lines of code?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license?
  - answer: .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.
    question: Supported .NET versions?
  - answer: Yes—loop through files and reuse the same rasterization options.
    question: Can I batch convert?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert plt
- Aspose.CAD
- .NET CAD conversion
title: Konwertuj PLT do PDF przy użyciu Aspose.CAD dla .NET – samouczek
url: /pl/net/exporting-plt-files/exporting-plt-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie PLT do PDF przy użyciu Aspose.CAD dla .NET – samouczek

W tym samouczku dowiesz się, jak **konwertować PLT do PDF** przy użyciu biblioteki Aspose.CAD dla .NET. Niezależnie od tego, czy tworzysz narzędzie desktopowe, czy usługę po stronie serwera, poniższe kroki poprowadzą Cię przez ładowanie rysunku PLT, konfigurowanie rasteryzacji i zapisywanie wyniku jako plik PDF — wszystko z jasnymi wyjaśnieniami i wskazówkami najlepszych praktyk.

## Szybkie odpowiedzi
- **Jaka jest główna klasa?** `CadImage` ładuje i rasteryzuje pliki PLT.  
- **Ile linii kodu?** Do rzeczywistej konwersji potrzebne są tylko dwie linie.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Obsługiwane wersje .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy mogę konwertować wsadowo?** Tak — iteruj po plikach i ponownie używaj tych samych opcji rasteryzacji.

## Co to jest konwersja PLT do PDF?
Wyrażenie „konwertować PLT do PDF” opisuje proces przekształcania pliku wykresu opartego na HPGL (PLT) do formatu Portable Document Format (PDF), który może być wyświetlany na dowolnym urządzeniu. Aspose.CAD udostępnia API jednego wywołania, które wykonuje tę konwersję bez potrzeby używania zewnętrznego oprogramowania CAD.

## Dlaczego używać Aspose.CAD do tej konwersji?
Aspose.CAD obsługuje **ponad 30** formatów CAD i BIM oraz może eksportować pliki do **2 GB** bez ładowania całego dokumentu do pamięci, zapewniając wysokowydajną obróbkę wsadową dla obciążeń korporacyjnych.

## Wymagania wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania:

1. Biblioteka Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Możesz pobrać bibliotekę Aspose.CAD dla .NET [tutaj](https://releases.aspose.com/cad/net/).

2. Środowisko programistyczne: Miej gotowe działające środowisko programistyczne .NET.

## Importowanie przestrzeni nazw

W swoim projekcie .NET rozpocznij od zaimportowania niezbędnych przestrzeni nazw:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

Te przestrzenie nazw zapewnią niezbędne klasy i funkcje do obsługi operacji CAD.

## Jak konwertować PLT do PDF przy użyciu Aspose.CAD?

Klasa `CadImage` reprezentuje rysunek CAD i udostępnia metody do ładowania i zapisywania obrazów. Załaduj swój plik PLT przy użyciu `CadImage.Load("input.plt")`, a następnie wywołaj `image.Save("output.pdf", pdfOptions)` — to pojedyncze wywołanie wykonuje pełną konwersję, zachowując wierność wektorową i jakość rasteryzacji. W przypadku dużych rysunków dostosuj `RasterizationOptions`, aby kontrolować DPI i rozmiar strony przed zapisem.

## Krok 1: Ustaw katalog dokumentów

Zacznij od zdefiniowania ścieżki do katalogu dokumentów w kodzie:

```csharp
string MyDir = "Your Document Directory";
```

Zastąp „Your Document Directory” rzeczywistą ścieżką do swoich dokumentów.

## Krok 2: Załaduj plik PLT

Załaduj plik PLT do obrazu CAD, używając poniższego fragmentu kodu:

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```

**Kotwica definicji:** Klasa `CadImage` reprezentuje rysunek CAD i zapewnia możliwości rasteryzacji.

## Krok 3: Skonfiguruj opcje rasteryzacji

`CadRasterizationOptions` określa, jak rysunek CAD jest rasteryzowany, w tym rozmiar strony, DPI i kolor tła.

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1600,
    PageWidth = 1600,
    DrawType = CadDrawTypeMode.UseObjectColor,
    BackgroundColor = Color.White
};
```

## Krok 4: Ustaw opcje PDF

`PdfOptions` określa ustawienia wyjściowe PDF i łączy się z opcjami rasteryzacji dla konwersji.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## Krok 5: Zapisz jako PDF

Zapisz obraz CAD jako plik PDF:

```csharp
cadImage.Save(MyDir + "50states.pdf", pdfOptions);
```

## Typowe problemy i wskazówki rozwiązywania

- **Błąd pliku nie znaleziono:** Sprawdź, czy ścieżka podana do `CadImage.Load` wskazuje istniejący plik PLT i czy aplikacja ma uprawnienia do odczytu.  
- **Puste strony w PDF:** Upewnij się, że `RasterizationOptions.PageWidth` i `PageHeight` odpowiadają proporcjom źródłowego rysunku, lub ustaw `LayoutOptions` na `LayoutOptions.AutoFit`.  
- **Zużycie pamięci przy dużych plikach:** Użyj `image.Save` z `PdfOptions`, które odwołują się do współdzielonej instancji `RasterizationOptions`, aby uniknąć wielokrotnego ładowania całego obrazu do pamięci.

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET w mojej aplikacji webowej?
A: Tak, Aspose.CAD dla .NET jest kompatybilny zarówno z aplikacjami desktopowymi, jak i webowymi, w tym projektami ASP.NET Core i MVC.

### P2: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla .NET?
A: Oczywiście, możesz zapoznać się ze stroną darmowej wersji próbnej Aspose [tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla .NET?
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie społeczności i wskazówki.

### P4: Jakie formaty plików obsługuje Aspose.CAD?
A: Aspose.CAD obsługuje szeroką gamę formatów CAD, w tym DWG, DXF i PLT.

### P5: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla .NET?
A: Zapoznaj się z [dokumentacją Aspose.CAD](https://reference.aspose.com/cad/net/), aby uzyskać szczegółowe informacje.

### P6: Czy mogę wsadowo konwertować wiele plików PLT do PDF w jednym uruchomieniu?
A: Tak — iteruj po katalogu z plikami PLT, ponownie używaj tych samych `RasterizationOptions` i wywołuj `Save` dla każdego obrazu.

### P7: Czy biblioteka zachowuje dane wektorowe przy konwersji do PDF?
A: Konwersja rasteryzuje rysunek, ale możesz włączyć wyjście wektorowe PDF, ustawiając `PdfOptions.VectorRasterization = true`.

---

**Ostatnia aktualizacja:** 2026-08-12  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Eksportowanie plików PLT do obrazu - Samouczek Aspose.CAD](/cad/net/exporting-plt-files/exporting-plt-files-to-image/)
- [Obsługa formatu PLT w Aspose.CAD – kompleksowy samouczek](/cad/net/plt-and-watermarking/plt-format-support-in-aspose-cad/)
- [Eksportowanie DXF do formatu PDF – Samouczek Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}