---
date: 2026-07-04
description: Dowiedz się, jak ustawić rozmiar strony PDF i wyeksportować PDF z obrazów
  3D CAD przy użyciu Aspose.CAD dla .NET – przewodnik krok po kroku, jak przekonwertować
  DWG na PDF i zapisać CAD jako PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Eksportowanie obrazów 3D do PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ustaw rozmiar strony PDF – Eksportowanie obrazów 3D do PDF przy użyciu Aspose.CAD
url: /pl/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie obrazów 3D do PDF - Poradnik Aspose.CAD

## Wprowadzenie

Jeśli potrzebujesz **ustawić rozmiar strony PDF** podczas konwertowania rysunku CAD 3‑D do PDF, trafiłeś we właściwe miejsce. Ten poradnik pokazuje krok po kroku, jak wczytać plik CAD, skonfigurować opcje rasteryzacji — w tym niestandardowe wymiary strony — i wygenerować wysokiej jakości PDF przy użyciu Aspose.CAD dla .NET. Po zakończeniu będziesz w stanie **eksportować PDF z CAD**, **zapisać CAD jako PDF** i kontrolować każdy szczegół układu bez instalacji AutoCAD.

## Szybkie odpowiedzi
- **Co oznacza „eksport PDF z CAD”?** Konwertuje rysunek CAD (DWG, DXF, DGN itp.) na PDF, który można otworzyć na dowolnym urządzeniu.  
- **Która biblioteka wykonuje konwersję?** Aspose.CAD dla .NET zapewnia rasteryzację i eksport PDF bez zewnętrznych zależności.  
- **Czy potrzebna jest licencja?** Wymagana jest tymczasowa lub pełna licencja do użytku produkcyjnego; dostępna jest darmowa wersja próbna.  
- **Czy mogę ustawić niestandardowe wymiary strony?** Tak — użyj `PageWidth` i `PageHeight` w `RasterizationOptions`.  
- **Czy geometria 3‑D zostanie zachowana?** Obiekty 3‑D są rasteryzowane; włącz `TypeOfEntities.Entities3D`, aby uzyskać pełne wsparcie 3‑D.

## Co oznacza „eksport PDF” w kontekście CAD?

Eksportowanie PDF z CAD oznacza pobranie rysunku CAD (DWG, DXF, DGN itp.) i przekształcenie go w plik PDF, który może zawierać grafikę wektorową, rasteryzowane widoki 3‑D oraz precyzyjne informacje o układzie strony, co ułatwia udostępnianie osobom nieposiadającym oprogramowania CAD.

## Dlaczego używać Aspose.CAD do eksportu PDF?

Aspose.CAD pozwala **ustawić rozmiar strony PDF** i eksportować PDF-y w pełni w zarządzanym kodzie .NET. Obsługuje ponad 50 formatów CAD, przetwarza pliki do 2 GB bez wczytywania całego dokumentu do pamięci oraz zachowuje grubości linii, kolory i opcjonalne renderowanie obiektów 3‑D przy rozdzielczości rasteryzacji do 1200 DPI. Biblioteka działa na Windows, Linux i macOS, więc wygenerowane PDF-y działają na każdej platformie.

## Wymagania wstępne

- **Aspose.CAD for .NET** zainstalowany. Pobierz go ze [strony pobierania Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).  
- Folder zawierający pliki CAD, które chcesz konwertować (np. `C:\CAD\`).  
- .NET 6.0 lub nowszy (lub .NET Framework 4.7.2).  

## Importowanie przestrzeni nazw

Instrukcje `using` importują przestrzenie nazw Aspose.CAD potrzebne do pracy z opcjami rasteryzacji i PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Przewodnik krok po kroku

### Jak ustawić rozmiar strony PDF przy eksporcie CAD do PDF?

Wczytaj plik CAD, skonfiguruj wymiary strony w `RasterizationOptions`, dołącz te opcje do instancji `PdfOptions` i wywołaj `Save`. Ten czterostopniowy przepływ daje pełną kontrolę nad rozmiarem i jakością wyjścia, zachowując jednocześnie zwięzłość kodu.

### Krok 1: Załaduj obraz CAD

Klasa `Image` reprezentuje rysunek CAD wczytany do pamięci, gotowy do rasteryzacji.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Krok 2: Skonfiguruj opcje rasteryzacji (Zapisz CAD jako PDF)

Klasa `RasterizationOptions` definiuje, jak dane CAD są rasteryzowane, w tym rozmiar strony, DPI oraz czy renderowane są obiekty 3‑D.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Krok 3: Ustaw opcje PDF (Utwórz PDF z CAD)

Klasa `PdfOptions` przechowuje ustawienia formatu wyjściowego i łączy opcje rasteryzacji z generowaniem PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 4: Zapisz jako PDF (Wygeneruj PDF z modelu 3D)

Metoda `Save` obiektu `Image` zapisuje rasteryzowaną zawartość do określonego pliku PDF, tworząc gotowy do udostępnienia dokument.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| **Output PDF is blank** | Nieprawidłowa nazwa układu lub brak układu `Model`. | Zweryfikuj, że `rasterizationOptions.Layouts` odpowiada układowi istniejącemu w pliku CAD. |
| **Low resolution** | Domyślne DPI rasteryzacji jest niskie. | Ustaw `rasterizationOptions.Resolution = 300;` przed zapisem. |
| **3‑D entities not shown** | `TypeOfEntities` jest zakomentowane. | Odkomentuj `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **License exception** | Używanie wersji próbnej bez licencji. | Zastosuj tymczasową lub stałą licencję poprzez `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?**  
A: Tak, Aspose.CAD obsługuje ponad 50 formatów wejściowych i wyjściowych, w tym DWG, DXF, DGN, STL i IFC, zapewniając elastyczność dla każdego projektu.

**Q: Czy mogę dostosować wymiary strony przy eksporcie do PDF?**  
A: Oczywiście. Ustaw `PageWidth` i `PageHeight` w `RasterizationOptions` na dowolny rozmiar w punktach, calach lub milimetrach przed wywołaniem `Save`.

**Q: Czy dostępne są tymczasowe licencje dla Aspose.CAD?**  
A: Tak, tymczasowe licencje dla Aspose.CAD można uzyskać, odwiedzając [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?**  
A: Odwiedź [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc ekspertów i wymianę doświadczeń z innymi użytkownikami.

**Q: Czy istnieje darmowa wersja próbna Aspose.CAD?**  
A: Tak, funkcje Aspose.CAD możesz wypróbować, korzystając z [free trial](https://releases.aspose.com/).

## Podsumowanie

Masz teraz kompletną, gotową do produkcji metodę **ustawiania rozmiaru strony PDF** i **eksportu PDF z obrazów CAD 3D** przy użyciu Aspose.CAD dla .NET. Dzięki regulacji opcji rasteryzacji możesz precyzyjnie dostroić rozdzielczość, układ strony i renderowanie obiektów 3‑D, aby spełnić wszelkie wymagania dokumentacyjne. Eksperymentuj z różnymi ustawieniami DPI i wymiarami stron, aby osiągnąć idealną równowagę między rozmiarem pliku a jakością wizualną.

{{< blocks/products/products-backtop-button >}}

## Powiązane poradniki

- [Eksportowanie konkretnych układów do PDF - Poradnik Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Eksportowanie DWG do PDF lub obrazów rastrowych - Poradnik Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Eksport DGN do PDF w Aspose.CAD dla .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Last Updated:** 2026-07-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose