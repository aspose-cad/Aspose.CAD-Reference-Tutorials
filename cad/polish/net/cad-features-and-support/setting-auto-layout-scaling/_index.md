---
date: 2026-03-26
description: Dowiedz się, jak tworzyć PDF z CAD i konwertować DXF na PDF przy użyciu
  Aspose.CAD dla .NET z automatycznym skalowaniem układu, zapewniającym precyzyjne
  i elastyczne renderowanie.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Utwórz PDF z CAD: Automatyczne skalowanie układu – Aspose.CAD'
url: /pl/net/cad-features-and-support/setting-auto-layout-scaling/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz PDF z CAD: Automatyczne Skalowanie Układu – Aspose.CAD

W nowoczesnych aplikacjach .NET konwertowanie rysunków CAD na wysokiej jakości pliki PDF jest powszechnym wymaganiem — niezależnie od tego, czy musisz **create PDF from CAD** do raportowania, udostępniania czy archiwizacji. Ten samouczek przeprowadzi Cię przez użycie Aspose.CAD dla .NET w celu włączenia Auto Layout Scaling, zapewniając wyniki o perfekcyjnej rozdzielczości pikseli, a także pokazując, jak **convert DXF to PDF** i **export CAD to PDF** przy minimalnym kodzie.

## Szybkie odpowiedzi
- **What does Auto Layout Scaling do?** Automatycznie dostosowuje układ do rozmiaru strony, zachowując wierność geometrii.  
- **Which formats are supported?** Każdy format odczytywany przez Aspose.CAD (DXF, DWG, DGN itp.) może być wyeksportowany do PDF.  
- **Do I need a license?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Can I change page size?** Tak — ustaw `PageWidth` i `PageHeight` w `CadRasterizationOptions`.  
- **Is it .NET Core compatible?** Absolutnie, działa z .NET Framework oraz .NET Core/5/6+.

## Co oznacza „create PDF from CAD”?
Utworzenie PDF z pliku CAD oznacza rasteryzację danych wektorowych rysunku do formatu dokumentu przenośnego. Ta konwersja zachowuje warstwy, grubości linii i kolory, jednocześnie umożliwiając wyświetlanie pliku na dowolnym urządzeniu bez oprogramowania CAD.

## Dlaczego używać Auto Layout Scaling?
Auto Layout Scaling zapewnia, że cały rysunek mieści się schludnie na stronie wyjściowej, eliminując ręczne obliczenia współczynników skalowania. Jest to szczególnie przydatne przy rysunkach o różnych wymiarach, takich jak plany architektoniczne czy schematy mechaniczne.

## Wymagania wstępne
1. **Aspose.CAD for .NET** – pobierz najnowszą bibliotekę ze [strony pobierania](https://releases.aspose.com/cad/net/).  
2. **Środowisko programistyczne .NET** – Visual Studio, Rider lub dowolny edytor obsługujący C#.  
3. **Przykładowy plik DXF** – np. `conic_pyramid.dxf` lub dowolny plik CAD, który chcesz przekonwertować.

## Importowanie przestrzeni nazw
Dodaj wymagane przestrzenie nazw, aby uzyskać dostęp do klas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik CAD
Załaduj źródłowy rysunek do obiektu `Image`. To jest punkt wejścia dla dalszego przetwarzania.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji
Zdefiniuj wymiary strony wyjściowej. Dostosuj te wartości, aby odpowiadały pożądanemu rozmiarowi PDF.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Krok 3: Włącz Auto Layout Scaling
Włącz automatyczne skalowanie, aby rysunek mieścił się na stronie bez przycinania.

```csharp
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Krok 4: Utwórz opcje PDF
Połącz ustawienia rasteryzacji z eksporterem PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Zapisz wynik – create PDF from CAD
Określ ścieżkę wyjściową i zapisz obraz jako PDF. Ten krok **creates PDF from CAD** z skonfigurowanym skalowaniem.

```csharp
MyDir = MyDir + "result_out.pdf";
image.Save(MyDir, pdfOptions);
```

## Częste problemy i wskazówki
- **Missing fonts or line styles?** Upewnij się, że odwołania w pliku CAD są osadzone lub dostępne na serwerze.  
- **Large files cause memory pressure?** Przetwarzaj rysunek w częściach lub zwiększ limit pamięci aplikacji.  
- **Output looks blurry?** Zwiększ `PageWidth`/`PageHeight` dla wyższej DPI lub ustaw `Resolution` w `CadRasterizationOptions`.

## Najczęściej zadawane pytania

**Q: Can I apply Auto Layout Scaling to other file formats besides DXF?**  
A: Tak, Aspose.CAD obsługuje DWG, DGN i wiele innych formatów CAD do automatycznego skalowania.

**Q: How can I handle errors during the rendering process?**  
A: Owiń kod konwersji w blok `try‑catch` i przechwyć `Aspose.CAD.CadException`, aby uzyskać szczegółowe informacje o błędach.

**Q: Is there a limit to the file size that Aspose.CAD can handle?**  
A: Biblioteka jest przeznaczona do obsługi dużych plików, ale wydajność zależy od dostępnej pamięci RAM i CPU. Rozważ przetwarzanie bardzo dużych rysunków na serwerze z dużymi zasobami.

**Q: Can I further customize the output PDF (e.g., add watermarks or metadata)?**  
A: Oczywiście. Po zapisaniu możesz użyć Aspose.PDF do modyfikacji PDF — dodać znaki wodne, ustawić właściwości dokumentu lub scalić strony.

**Q: Where can I find additional resources and support for Aspose.CAD?**  
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy społeczności oraz zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/net/) w celu uzyskania szczegółowych informacji o API.

## Podsumowanie
Teraz wiesz, jak **create PDF from CAD**, włączyć **Auto Layout Scaling** i skutecznie **convert DXF to PDF** przy użyciu Aspose.CAD dla .NET. To podejście daje pełną kontrolę nad jakością renderowania, jednocześnie utrzymując implementację prostą.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-03-26  
**Testowano z:** Aspose.CAD for .NET 24.12 (latest)  
**Autor:** Aspose  

---