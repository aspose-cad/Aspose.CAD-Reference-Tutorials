---
description: Dowiedz się, jak konwertować pliki DWG na PNG i wyodrębniać obiekty OLE
  z plików DWG przy użyciu Aspose.CAD dla .NET – szybki przewodnik skoncentrowany
  na kodzie.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DWG na PNG i eksportuj obiekty OLE – Samouczek Aspose.CAD
url: /pl/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie obiektów OLE z plików DWG – Aspose.CAD Tutorial

## Wprowadzenie

Jeśli potrzebujesz **konwertować DWG na PNG** jednocześnie wyciągając osadzone obiekty OLE, trafiłeś we właściwe miejsce. Aspose.CAD dla .NET upraszcza ten dwustopniowy proces, umożliwiając automatyzację ekstrakcji i rasteryzacji w kilku linijkach C#. W ciągu kilku minut przeprowadzimy Cię przez cały przepływ pracy, od konfiguracji środowiska po zapisanie każdego pliku DWG jako PNG zawierającego wyodrębnione dane OLE.

## Szybkie odpowiedzi
- **Co obejmuje ten poradnik?** Konwersja DWG na PNG oraz wyodrębnianie obiektów OLE przy użyciu Aspose.CAD dla .NET.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy mogę przetwarzać wiele plików DWG jednocześnie?** Tak – przykład iteruje przez tablicę nazw plików.  
- **Gdzie mogę znaleźć więcej przykładów?** Sprawdź oficjalną dokumentację Aspose.CAD oraz linki do forum poniżej.

## Co to jest **convert DWG to PNG**?
Konwersja pliku DWG (rysunek AutoCAD) na obraz PNG rasteryzuje dane wektorowe, co ułatwia ich przeglądanie lub osadzanie w stronach internetowych, raportach czy innych aplikacjach, które nie obsługują natywnie formatu DWG. Gdy obecne są obiekty OLE, mogą być wyodrębnione i zapisane jako oddzielne zasoby podczas konwersji.

## Dlaczego wyodrębniać obiekty OLE z plików CAD?
Wiele rysunków DWG osadza arkusze kalkulacyjne, wykresy lub inne dokumenty Office jako obiekty OLE. Ich wyodrębnienie pozwala ponownie wykorzystać oryginalne dane, zautomatyzować raportowanie lub przenieść zawartość do nowszych formatów bez utraty osadzonych informacji.

## Wymagania wstępne

- Biblioteka Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę. Możesz ją pobrać ze [strony pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).
- Katalog dokumentów: Utwórz katalog, w którym przechowywane są pliki DWG. Zastąp `"Your Document Directory"` w podanym fragmencie kodu rzeczywistą ścieżką.

## Importowanie przestrzeni nazw

W swoim projekcie .NET zaimportuj wymagane przestrzenie nazw:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog dokumentów

```csharp
string MyDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką, w której znajdują się Twoje pliki DWG.

### Krok 2: Wymień pliki DWG, które chcesz przetworzyć

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Krok 3: Skonfiguruj opcje eksportu dla konwersji do PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Możesz dostosować `CadRasterizationOptions` (np. `PageWidth`, `PageHeight`, `BackgroundColor`), aby uzyskać pożądaną rozdzielczość wyjścia.

### Krok 4: Iteruj przez każdy plik DWG i wykonaj konwersję

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Podczas tej pętli biblioteka automatycznie **wyodrębnia obiekty OLE** osadzone w każdym rysunku i zawiera je w wygenerowanym pliku PNG. Jeśli potrzebujesz surowych strumieni OLE, możesz uzyskać dostęp do kolekcji `cadImage.OleObjects` – wygodny sposób na **how to extract ole** danych programowo.

## Typowe problemy i rozwiązywanie

- **Missing layout name** – Upewnij się, że układ, który podajesz (`"Layout1"` w przykładzie), istnieje w źródłowym pliku DWG; w przeciwnym razie rasteryzator przejdzie do domyślnej przestrzeni modelu.
- **Large files cause memory pressure** – Przetwarzaj pliki pojedynczo (jak pokazano) i niezwłocznie zwalniaj obiekty `CadImage` przy pomocy `using`.
- **Unexpected colors** – Ustaw `rasterizationOptions.BackgroundColor` tak, aby odpowiadał tłu rysunku, jeśli wymagana jest przezroczystość.

## Najczęściej zadawane pytania

### Q1: Czy Aspose.CAD dla .NET jest odpowiedni zarówno dla prostych, jak i zaawansowanych plików CAD?
A1: Tak, Aspose.CAD dla .NET jest wszechstronny i może obsługiwać szeroką gamę plików CAD, w tym zarówno warianty junior, jak i senior.

### Q2: Czy mogę dostosować opcje eksportu dla różnych układów?
A2: Oczywiście! Jak pokazano w poradniku, możesz dostosować opcje eksportu, w tym układy, do swoich konkretnych potrzeb.

### Q3: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla .NET?
A3: Zapoznaj się z [dokumentacją Aspose.CAD dla .NET](https://reference.aspose.com/cad/net/), aby uzyskać szczegółowe informacje i przykłady.

### Q4: Czy dostępna jest darmowa wersja próbna?
A4: Tak, możesz wypróbować możliwości Aspose.CAD dla .NET w ramach darmowej wersji próbnej. Odwiedź [ten link](https://releases.aspose.com/), aby rozpocząć.

### Q5: Jak mogę uzyskać wsparcie lub połączyć się ze społecznością?
A5: Aby uzyskać wsparcie i uczestniczyć w społeczności, odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q6: Jak **extract OLE from CAD** pliki bez konwertowania na PNG?
A6: Użyj kolekcji `CadImage.OleObjects` po załadowaniu pliku DWG; możesz iterować przez każdy `OleObject` i zapisać jego surowe dane do pliku.

## Podsumowanie

Teraz widzisz, jak **konwertować DWG na PNG** jednocześnie płynnie **wyodrębniając obiekty OLE** przy użyciu Aspose.CAD dla .NET. To podejście oszczędza czas, eliminuje ręczne kopiowanie i wklejanie oraz łatwo integruje się z automatycznymi pipeline’ami. Śmiało eksperymentuj z innymi formatami rastrowymi (JPEG, BMP) lub odkrywaj bogaty zestaw funkcji manipulacji CAD oferowanych przez Aspose.

---

**Ostatnia aktualizacja:** 2026-03-13  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}