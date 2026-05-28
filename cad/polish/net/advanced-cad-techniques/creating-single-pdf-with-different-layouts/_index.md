---
date: 2026-03-02
description: Dowiedz się, jak stworzyć pojedynczy plik PDF z różnymi układami przy
  użyciu Aspise.CAD dla .NET – konwertuj CAD na PDF, eksportuj DWG do PDF i efektywnie
  zapisuj CAD jako PDF.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak utworzyć pojedynczy plik PDF z różnymi układami – przewodnik Aspose.CAD
url: /pl/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak utworzyć pojedynczy plik PDF z różnymi układami – przewodnik Aspose.CAD

## Wprowadzenie

Jeśli potrzebujesz **utworzyć pojedynczy plik PDF**, który zawiera kilka układów CAD, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię krok po kroku przez proces konwersji rysunków CAD do jednego dokumentu PDF, obsługując przy tym wiele układów. Zobaczysz, jak Aspose.CAD dla .NET ułatwia **konwersję CAD do PDF**, **eksport DWG do PDF** oraz **zapis CAD jako PDF** przy użyciu kilku linii kodu C#.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Generowanie jednego PDF‑a, który zawiera wiele układów CAD.  
- **Jakiej biblioteki użyto?** Aspose.CAD dla .NET.  
- **Czy potrzebna jest licencja?** Bezpłatna wersja próbna wystarczy do oceny; licencja jest wymagana w środowisku produkcyjnym.  
- **Obsługiwane formaty CAD?** DWG, DXF, DGN i wiele innych.  
- **Typowy czas implementacji?** Około 10‑15 minut dla podstawowej konwersji.

## Co oznacza „utworzyć pojedynczy PDF” w kontekście CAD?

Utworzenie jednego PDF oznacza wzięcie jednego pliku źródłowego CAD, który może zawierać kilka definicji układów (przestrzeni papieru), i połączenie każdego układu w osobne strony jednego dokumentu PDF. Jest to szczególnie przydatne przy planach architektonicznych, schematach inżynieryjnych lub w sytuacjach, gdy klient oczekuje skonsolidowanego pakietu PDF.

## Dlaczego warto używać Aspose.CAD do tego zadania?

- **Brak zewnętrznych zależności** – czysty .NET, bez wymogu instalacji AutoCADa.  
- **Pełna kontrola nad rasteryzacją** – możesz ustawić rozmiar strony, DPI oraz własne wymiary układu.  
- **Renderowanie o wysokiej wierności** – dane wektorowe są zachowywane tam, gdzie to możliwe, zapewniając wyraźny rezultat.  
- **Gotowość do przetwarzania wsadowego** – ten sam kod może być umieszczony w pętli, aby automatycznie przetwarzać wiele rysunków.

## Wymagania wstępne

- Aspose.CAD dla .NET: Upewnij się, że masz zainstalowane Aspose.CAD dla .NET. Możesz pobrać go [tutaj](https://releases.aspose.com/cad/net/).  
- Środowisko programistyczne: Skonfiguruj środowisko .NET i posiądź podstawową znajomość programowania w C#.

## Importowanie przestrzeni nazw

W projekcie C# dołącz niezbędne przestrzenie nazw, aby wykorzystać funkcje Aspose.CAD dla .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj obraz CAD

Najpierw wczytaj plik CAD (na przykład rysunek DWG). Klasa `CadImage` daje dostęp do wszystkich układów znajdujących się w pliku.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Krok 2: Dostosuj opcje rasteryzacji

Zdefiniuj, jak każdy układ ma być rasteryzowany. Możesz ustawić domyślny rozmiar strony, a następnie nadpisać go dla konkretnych układów przy użyciu `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Wskazówka:** Dostosuj DPI (`rasterizationOptions.Resolution`), jeśli potrzebujesz wyjścia o wyższej rozdzielczości dla szczegółowych rysunków.

### Krok 3: Zdefiniuj opcje PDF

Umieść ustawienia rasteryzacji w obiekcie `PdfOptions`. Dzięki temu Aspose.CAD renderuje dane CAD bezpośrednio do strumienia PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Krok 4: Zapisz jako PDF

Na koniec wywołaj `Save` na instancji `CadImage`, podając docelową nazwę pliku PDF oraz przygotowane opcje. Biblioteka wygeneruje pojedynczy PDF zawierający stronę dla każdego skonfigurowanego układu.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Po tym wywołaniu będziesz mieć PDF, który łączy układy „ANSI C Plot” i „8.5 x 11 Plot” w jeden spójny dokument.

## Typowe problemy i rozwiązywanie ich

| Problem | Przyczyna | Rozwiązanie |
|-------|--------|-----|
| Brak układów w PDF | `LayoutPageSizes` nie zdefiniowano dla nazwy układu | Sprawdź dokładne nazwy układów w pliku CAD (uwzględniając wielkość liter). |
| Niska jakość wyjścia | Domyślne DPI wynosi 96 | Ustaw `rasterizationOptions.Resolution = 300` (lub wyższą) przed zapisem. |
| Plik nie został znaleziony | Niepoprawna ścieżka `MyDir` | Użyj `Path.Combine`, aby budować ścieżki niezależne od platformy. |

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.CAD dla .NET z innymi formatami CAD?

A1: Tak, Aspose.CAD dla .NET obsługuje różne formaty CAD, takie jak DWG, DXF, DGN i inne.

### Q2: Czy dostępna jest bezpłatna wersja próbna?

A2: Tak, możesz wypróbować bezpłatną wersję [tutaj](https://releases.aspose.com/).

### Q3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla .NET?

A3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy od społeczności.

### Q4: Gdzie znajdę szczegółową dokumentację?

A4: Dokumentację znajdziesz [tutaj](https://reference.aspose.com/cad/net/).

### Q5: Czy mogę kupić licencję na Aspose.CAD dla .NET?

A5: Tak, licencję można nabyć [tutaj](https://purchase.aspose.com/buy).

**Dodatkowe pytania i odpowiedzi**

**P:** Jak **wyeksportować DWG do PDF** z własnymi rozmiarami stron?  
**O:** Użyj `CadRasterizationOptions.LayoutPageSizes`, aby przypisać każdy układ DWG do żądanych wymiarów strony PDF, jak pokazano w Kroku 2.

**P:** Czy można **zapisać CAD jako PDF** bez rasteryzacji danych wektorowych?  
**O:** Aspose.CAD zawsze rasteryzuje przy tworzeniu PDF, ale możesz zwiększyć DPI, aby zachować wysoką wierność wizualną.

## Zakończenie

W tym przewodniku pokazaliśmy, jak **utworzyć pojedynczy plik PDF** z rysunków CAD zawierających wiele układów, korzystając z Aspose.CAD dla .NET. Masz teraz wszystkie elementy potrzebne do **konwersji CAD do PDF**, **eksportu DWG do PDF** oraz **zapisu CAD jako PDF** w jednym, zautomatyzowanym procesie. Eksperymentuj z różnymi ustawieniami rasteryzacji, aby dopasować jakość do wymagań projektu, i włącz ten kod do większych potoków przetwarzania wsadowego w razie potrzeby.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-03-02  
**Testowano z:** Aspose.CAD dla .NET 24.11  
**Autor:** Aspose  

---