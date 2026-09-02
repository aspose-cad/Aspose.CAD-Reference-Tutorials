---
date: 2026-07-04
description: Dowiedz się, jak ustawić rozmiar strony PDF podczas konwertowania plików
  OBJ do PDF przy użyciu Aspose.CAD dla .NET. Przewodnik krok po kroku z wymaganiami
  wstępnymi, opcjami rastrowania i opcjami PDF.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: Obsługa formatu OBJ w Aspose.CAD – Poradnik
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ustaw rozmiar strony PDF dla plików OBJ w Aspose.CAD – Poradnik
url: /pl/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw rozmiar strony PDF dla plików OBJ przy użyciu Aspose.CAD – Samouczek

## Wprowadzenie

Jeśli tworzysz aplikacje CAD w .NET i potrzebujesz **ustawić rozmiar strony PDF** podczas konwertowania modeli OBJ, Aspose.CAD dla .NET oferuje czyste API code‑first, które obsługuje rasteryzację i generowanie PDF w jednym przepływie. W tym samouczku przeprowadzimy instalację biblioteki, wczytanie pliku OBJ, skonfigurowanie wymiarów strony oraz zapisanie wyniku jako PDF. Po zakończeniu będziesz mieć wielokrotnego użytku wzorzec do przekształcania dowolnego modelu 3‑D w idealnie dopasowany dokument PDF.

## Szybkie odpowiedzi
- **Czy Aspose.CAD może konwertować OBJ do PDF?** Tak – wczytaj OBJ za pomocą `Image.Load` i rasteryzuj go do PDF.
- **Jak ustawić własny rozmiar strony PDF?** Użyj `PdfOptions` → `PageSize` lub ustaw szerokość/wysokość w `RasterizationOptions`.
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa do oceny; licencja jest wymagana w produkcji.
- **Czy konwersja jest efektywna pamięciowo?** Aspose.CAD strumieniuje dane i może obsługiwać PDF‑y o setkach stron bez ładowania całego pliku do pamięci.

## Co to jest format OBJ?

Format OBJ jest powszechnie używanym, tekstowym opisem geometrii 3‑D, który przechowuje pozycje wierzchołków, współrzędne tekstur oraz definicje ścian. Jest obsługiwany przez większość narzędzi do modelowania 3‑D i jest idealny do wymiany między CAD a pipeline’ami renderującymi.

## Dlaczego ustawiać własny rozmiar strony PDF?

Aspose.CAD może renderować rysunek CAD do dowolnego rozmiaru rastrowego. Poprzez wyraźne ustawienie wymiarów strony PDF zapewniasz, że końcowy dokument spełnia Twoje standardy raportowania, pasuje do standardowych rozmiarów papieru (A4, Letter) lub odpowiada własnym układom druku. Korzyść ilościowa: API może generować PDF‑y do **200 mm × 200 mm** w jednym wywołaniu, przetwarzając pliki większe niż **500 MB** bez przekraczania 250 MB pamięci RAM.

## Wymagania wstępne

- **Biblioteka Aspose.CAD** – Upewnij się, że biblioteka Aspose.CAD jest zainstalowana w Twoim projekcie .NET. Możesz ją pobrać [tutaj](https://releases.aspose.com/cad/net/) i zobaczyć pełną referencję API w [dokumentacji](https://reference.aspose.com/cad/net/).
- **Katalog dokumentów** – Utwórz folder na zasoby CAD; będziemy odnosić się do niego jako „Your Document Directory” w całym przewodniku.
- **Środowisko programistyczne .NET** – Visual Studio 2022 lub dowolne IDE obsługujące .NET 6+.

## Jak ustawić rozmiar strony PDF przy konwertowaniu OBJ do PDF?

Wczytaj plik OBJ, skonfiguruj opcje rasteryzacji z żądaną szerokością i wysokością, dołącz te opcje do instancji `PdfOptions` i wywołaj `Save`. Ten dwustopniowy wzorzec zapewnia, że strona PDF odpowiada podanym wymiarom, zachowując jednocześnie szczegóły modelu.

## Krok 1: Importuj przestrzenie nazw

`Image` obsługuje wszystkie formaty CAD, a `PdfOptions` kontroluje wyjście PDF.  
`Image` reprezentuje dokument CAD i udostępnia metody do wczytywania i zapisywania plików. `PdfOptions` definiuje ustawienia generowania PDF, takie jak rozmiar strony i kompresja.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 2: Wczytaj plik OBJ

Wczytaj plik OBJ do obiektu obrazu Aspose.CAD. Zastąp `"example-580-W.obj"` nazwą swojego pliku OBJ.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## Krok 3: Skonfiguruj opcje rasteryzacji

`RasterizationOptions` definiuje rozmiar rastra, który ostatecznie staje się rozmiarem strony PDF. Ustawienie `PageWidth` i `PageHeight` pozwala kontrolować dokładne wymiary wyjściowego PDF.  
`CadRasterizationOptions` (udostępniany przez `RasterizationOptions`) określa parametry rasteryzacji, takie jak wymiary strony i rozdzielczość.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## Krok 4: Utwórz opcje PDF

`PdfOptions` łączy ustawienia rasteryzacji z zapisem PDF. Przypisując instancję `RasterizationOptions`, zapewniasz, że PDF dziedziczy określony przez Ciebie rozmiar strony.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Zapisz jako PDF

Wywołaj metodę `Save` na obiekcie `Image`, przekazując docelową nazwę pliku oraz skonfigurowane `PdfOptions`. Biblioteka zapisuje PDF z dokładnym rozmiarem strony, który określiłeś.  
`Save` zapisuje obraz do pliku w określonym formacie i z podanymi opcjami.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## Częste problemy i rozwiązania

- **Nieprawidłowe wymiary strony** – Upewnij się, że `PageWidth` i `PageHeight` są ustawione w **pikselach**; użyj `Resolution`, aby przeliczyć cale lub milimetry na piksele (np. 300 dpi → 1 inch = 300 px).
- **Brakujące tekstury** – Pliki OBJ często odwołują się do zewnętrznych plików `.mtl`; upewnij się, że plik materiału znajduje się w tym samym katalogu co OBJ.
- **Wysokie zużycie pamięci przy dużych plikach** – Włącz `Image.SaveOptions.Compression`, aby zmniejszyć obciążenie pamięci przy renderowaniu wysokiej rozdzielczości.

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD jest kompatybilny z innymi formatami plików CAD?**  
O: Tak, Aspose.CAD obsługuje ponad **30** formatów wejściowych — w tym DWG, DXF, DGN i STL — i może eksportować do ponad **20** formatów rastrowych i wektorowych.

**P: Czy mogę wypróbować Aspose.CAD przed zakupem?**  
O: Oczywiście! Możesz przetestować wersję próbną [tutaj](https://releases.aspose.com/).

**P: Jak uzyskać wsparcie dla Aspose.CAD?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby zadawać pytania i dzielić się doświadczeniami z społecznością.

**P: Czy dostępne są tymczasowe licencje do testów?**  
O: Tak, tymczasowe licencje można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**P: Gdzie mogę kupić pełną licencję?**  
O: Możesz kupić Aspose.CAD [tutaj](https://purchase.aspose.com/buy).

---

**Ostatnia aktualizacja:** 2026-07-04  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Eksportowanie plików IGES do PDF – przewodnik Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Eksportowanie DXF do formatu PDF – samouczek Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Eksportowanie rysunków CAD do PDF – samouczek Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}