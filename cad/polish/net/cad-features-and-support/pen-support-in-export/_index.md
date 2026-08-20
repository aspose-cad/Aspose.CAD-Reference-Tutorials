---
date: 2026-03-26
description: Dowiedz się, jak tworzyć pliki PDF z CAD i konwertować DXF na PDF przy
  użyciu Aspose.CAD dla .NET. Dostosuj opcje pióra, aby uzyskać zachwycające wizualizacje
  w formatach PDF, PNG, BMP i nie tylko.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Utwórz PDF z CAD z niestandardowymi opcjami pióra – Aspose.CAD dla .NET
url: /pl/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podnieś eksport CAD z niestandardowymi opcjami pióra w Aspose.CAD dla .NET

## Introduction

Jeśli potrzebujesz **tworzyć PDF z CAD** szybko i z pełną kontrolą wizualną, Aspose.CAD dla .NET zapewnia dokładnie to. Korzystając z funkcji obsługi pióra w bibliotece, możesz definiować końcówki początkowe i końcowe, połączenia linii oraz inne atrybuty rysowania, tworząc PDF‑y wyglądające dokładnie tak, jak tego oczekujesz. Ten samouczek przeprowadzi Cię przez cały proces — od wczytania pliku DXF po wyeksportowanie dopracowanego PDF — a także pokaże, jak te same ustawienia można ponownie wykorzystać przy **eksportowaniu CAD do PNG** lub **rasteryzacji obrazu CAD** dla innych formatów.

## Quick Answers
- **Co oznacza „tworzyć PDF z CAD”?** Konwertuje wektorowe rysunki CAD (np. DXF) na dokument PDF, zachowując geometrię i stylizację.  
- **Które formaty obsługują opcje pióra?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF i WMF.  
- **Czy potrzebna jest licencja do programowania?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę zmienić końcówki linii dla innych formatów?** Tak — opcje pióra mają zastosowanie do każdego docelowego formatu rasteryzacji obsługiwanego przez Aspose.CAD.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is pen support in CAD export?

Obsługa pióra pozwala dostosować sposób rysowania linii, gdy rysunek CAD jest rasteryzowany lub wektorowo‑rasteryzowany. Możesz ustawić właściwości takie jak `StartCap`, `EndCap`, `LineJoin` i `DashStyle`. Te ustawienia wpływają na ostateczny wygląd wyeksportowanego obrazu lub PDF, dając precyzyjną kontrolę nad jakością wizualną.

## Why use custom pen options when you **create PDF from CAD**?

- **Spójna identyfikacja wizualna** – dopasuj style linii korporacyjnych we wszystkich dokumentach.  
- **Lepsza czytelność** – grubsze końcówki i połączenia sprawiają, że rysunki techniczne są wyraźniejsze na ekranie i w druku.  
- **Elastyczność międzyformatowa** – ta sama konfiguracja pióra działa dla PNG, BMP i innych formatów rastrowych, oszczędzając Twój czas.

## Prerequisites

- Aspose.CAD dla .NET zainstalowany (pobierz ze [strony wydania](https://releases.aspose.com/cad/net/)).  
- Podstawowa znajomość formatu DXF (Drawing Exchange Format).  
- Znajomość programowania w C#.

## Import Namespaces

Aby rozpocząć, upewnij się, że importujesz niezbędne przestrzenie nazw w swoim projekcie C#:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Step 1: Set Up Your Document Directory

Zdefiniuj folder zawierający źródłowy plik CAD:

```csharp
string MyDir = "Your Document Directory";
```

## Step 2: Load the CAD Image

Wczytaj rysunek CAD (na przykład plik DXF) do obiektu `Aspose.CAD.Image`:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

Utwórz obiekty opcji rasteryzacji i PDF. Te obiekty pozwalają kontrolować, jak dane CAD są przekształcane w obraz rastrowy lub stronę PDF:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Step 4: Customize Pen Options

Tutaj **dostosowujesz pióro**, które rysuje linie. Możesz ustawić końcówki początkowe i końcowe na `Flat`, `Round`, `Square` itp. To jest sedno „jak eksportować CAD” z potrzebnym stylem wizualnym:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Wskazówka:* Eksperymentuj z `LineCap.Round` dla płynniejszych zakończeń linii przy **eksportowaniu CAD do PNG**.

## Step 5: Apply Vector Rasterization Options

Dołącz ustawienia rasteryzacji do opcji PDF, aby proces eksportu wiedział, której konfiguracji pióra użyć:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 6: Save the Exported PDF

Na koniec wygeneruj plik PDF. Ten krok **tworzy PDF z CAD** z zastosowanymi niestandardowymi ustawieniami pióra:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

Możesz zamienić `PdfOptions` na `PngOptions`, `BmpOptions` itp., aby **eksportować CAD do PNG** lub inne formaty rastrowe, zachowując tę samą konfigurację pióra.

## Common Use Cases

- **Dokumentacja techniczna** – wstaw precyzyjne style linii w inżynierskich PDF‑ach.  
- **Automatyczne generowanie raportów** – przetwarzaj wsadowo wiele plików DXF do PDF‑ów przy użyciu jednego profilu pióra.  
- **Usługi internetowe** – udostępnij API, które konwertuje przesłane pliki DXF na PDF‑y w locie, zapewniając spójny styl.

## Troubleshooting & Common Pitfalls

| Problem | Przyczyna | Rozwiązanie |
|-------|--------|----------|
| Wyeksportowane linie wyglądają na grubsze niż oczekiwano | DPI jest wyższe niż zamierzone | Ustaw `rasterizationOptions.PageWidth` / `PageHeight` lub dostosuj `Resolution`. |
| Opcje pióra są ignorowane przy wyjściu PNG | Używanie `ImageOptions` zamiast `VectorRasterizationOptions` | Upewnij się, że przypisujesz `rasterizationOptions.PenOptions` przed zapisem. |
| Plik PDF jest pusty | Ścieżka źródłowego DXF jest nieprawidłowa lub plik jest uszkodzony | Sprawdź `sourceFilePath` i potwierdź, że DXF ładuje się bez wyjątków. |

## FAQ

### Q1: Czy mogę używać tych opcji pióra dla innych formatów obrazu poza PDF?

A1: Tak, opcje pióra można zastosować do różnych formatów obrazu, takich jak PNG, BMP, GIF, JPEG i inne.

### Q2: Gdzie mogę znaleźć dodatkową dokumentację dla Aspose.CAD dla .NET?

A2: Odwołaj się do [dokumentacji](https://reference.aspose.com/cad/net/) po kompleksowe informacje i przykłady.

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla .NET?

A3: Tak, darmową wersję próbną można uzyskać [tutaj](https://releases.aspose.com/).

### Q4: Jak mogę uzyskać tymczasowe licencje dla Aspose.CAD dla .NET?

A4: Odwiedź [stronę tymczasowych licencji](https://purchase.aspose.com/temporary-license/), aby uzyskać opcje tymczasowego licencjonowania.

### Q5: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD dla .NET?

A5: Skontaktuj się ze społecznością na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

## Additional Frequently Asked Questions

**Q: Jak **przekonwertować DXF na PDF** programowo?**  
A: Wczytaj DXF za pomocą `Image.Load`, skonfiguruj `CadRasterizationOptions` i `PdfOptions`, a następnie wywołaj `Save`, jak pokazano w powyższych krokach.

**Q: Czy mogę rasteryzować obraz CAD bez tworzenia PDF?**  
A: Tak — użyj `PngOptions`, `BmpOptions` lub dowolnej innej klasy formatu rastrowego i przypisz te same `rasterizationOptions`, aby uzyskać wysokiej jakości rasteryzację.

**Q: Czy można zmienić szerokość linii przy tworzeniu PDF z CAD?**  
A: Dostosuj `rasterizationOptions.CustomLineWidth` lub zmodyfikuj właściwość `PenOptions.Width` przed zapisem.

**Q: Czy biblioteka obsługuje pliki DXF 3D?**  
A: Aspose.CAD koncentruje się na danych wektorowych 2D; elementy 3D są pomijane podczas rasteryzacji.

**Q: Jaka wersja Aspose.CAD jest wymagana dla tych funkcji?**  
A: Obsługa pióra jest dostępna od wersji 20.9; każda nowsza wersja będzie działać.

---

**Ostatnia aktualizacja:** 2026-03-26  
**Testowano z:** Aspose.CAD dla .NET 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}