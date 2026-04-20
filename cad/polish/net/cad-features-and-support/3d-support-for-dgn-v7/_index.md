---
date: 2026-03-24
description: Dowiedz się, jak konwertować DGN na PDF (i PNG) z obsługą 3D dla DGN
  V7 przy użyciu Aspose.CAD dla .NET – przewodnik krok po kroku.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DGN na PDF (obsługa 3D) z Aspose.CAD dla .NET
url: /pl/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DGN do PDF (obsługa 3D) przy użyciu Aspose.CAD dla .NET

## Wprowadzenie

W nowoczesnych przepływach pracy CAD możliwość **konwersji DGN do PDF** szybko i zachowania geometrii 3‑D jest niezbędna. Niezależnie od tego, czy generujesz dokumentację, udostępniasz projekty interesariuszom nie‑CAD, czy archiwizujesz projekty, Aspose.CAD dla .NET zapewnia niezawodny sposób przekształcania plików DGN V7 w wysokiej jakości wyjścia PDF (a nawet PNG). W tym samouczku przeprowadzimy Cię przez dokładne kroki potrzebne do włączenia obsługi 3D i wygenerowania PDF z pliku DGN.

## Szybkie odpowiedzi
- **Co obejmuje samouczek?** Włączenie obsługi 3D i konwersja DGN V7 do PDF przy użyciu Aspose.CAD dla .NET.  
- **Jaki główny format jest tworzony?** PDF (z opcjonalnym eksportem PNG).  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Obsługiwane wersje .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowej konwersji.

## Co to jest „konwersja DGN do PDF”?

Konwersja DGN do PDF oznacza renderowanie danych wektorowych przechowywanych w pliku MicroStation DGN do przenośnego formatu dokumentu, który może być wyświetlany na dowolnym urządzeniu bez specjalistycznego oprogramowania CAD. Dzięki silnikowi rasteryzacji 3‑D Aspose.CAD konwersja zachowuje układ, kolory i wskazówki głębokości, dostarczając wierną reprezentację wizualną.

## Dlaczego używać Aspose.CAD do tej konwersji?

- **Pełna rasteryzacja 3‑D** – zachowuje informacje o głębokości i układzie.  
- **Brak zewnętrznych zależności** – czysta biblioteka .NET, nie wymaga MicroStation.  
- **Wiele formatów wyjściowych** – PDF, PNG, JPEG, TIFF itp. (drugorzędne słowo kluczowe *convert dgn to png* jest obsługiwane od ręki).  
- **Cross‑platform** – działa na Windows, Linux i macOS.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz następujące elementy:

- Aspose.CAD dla .NET zainstalowany. Możesz go pobrać ze [strony pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).
- Prawidłowy plik DGN V7, który chcesz przetworzyć.
- Środowisko programistyczne .NET (Visual Studio, VS Code lub interfejs wiersza poleceń). Instrukcje instalacji są dostępne w [.NET documentation](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Importuj przestrzenie nazw

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Te przestrzenie nazw dają dostęp do podstawowych klas Aspose.CAD oraz standardowych narzędzi .NET.

## Krok 1: Skonfiguruj środowisko

Określ, gdzie znajduje się źródłowy plik DGN i gdzie ma zostać zapisany wyjściowy PDF.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Wskazówka:** Użyj `Path.Combine` do konstrukcji ścieżek niezależnych od platformy.

## Krok 2: Załaduj plik DGN

Utwórz instancję `DgnImage`, ładując plik za pomocą `Image.Load`. Ten krok przygotowuje dane CAD do rasteryzacji.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Krok 3: Skonfiguruj opcje eksportu

Skonfiguruj `PdfOptions` wraz z `CadRasterizationOptions`. Tutaj kontrolujesz rozmiar strony, tło oraz które układy (widoki) mają być wyeksportowane.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

Jeśli zamiast tego potrzebujesz **konwersji DGN do PNG**, po prostu zamień `PdfOptions` na `PngOptions`, zachowując te same ustawienia rasteryzacji.

## Krok 4: Zapisz wynik

Na koniec zapisz wyrenderowany wynik w wybranej lokalizacji.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

Po wykonaniu znajdziesz plik PDF (lub PNG, jeśli zmieniłeś opcje), który wiernie odzwierciedla oryginalny rysunek 3‑D DGN.

## Typowe problemy i wskazówki

- **Brakujące układy:** Upewnij się, że nazwy układów w `Layouts` odpowiadają tym w pliku DGN; w przeciwnym razie zostaną zignorowane.  
- **Duże pliki:** Zwiększaj `PageWidth`/`PageHeight` stopniowo, aby uniknąć wysokiego zużycia pamięci.  
- **Dokładność kolorów:** Jeśli tło wydaje się ciemne, sprawdź, czy `BackgroundColor` jest ustawiony na pożądaną wartość (np. `Color.White`).

## Podsumowanie

Teraz opanowałeś, jak **konwertować DGN do PDF** z pełnym wsparciem 3‑D przy użyciu Aspose.CAD dla .NET. Ten przepływ pracy może być zintegrowany z automatycznymi pipeline'ami, narzędziami desktopowymi lub usługami webowymi, aby dostarczać wizualizacje CAD każdej grupie odbiorców.

## FAQ

### Q1: Czy mogę przetwarzać wiele plików DGN jednocześnie przy użyciu tego podejścia?

A1: Tak, możesz zmodyfikować kod, aby obsługiwał wiele plików w pętli lub jako część systemu przetwarzania wsadowego.

### Q2: Jakie inne formaty eksportu są obsługiwane przez Aspose.CAD dla .NET?

A2: Aspose.CAD dla .NET obsługuje różne formaty eksportu, w tym PDF, PNG, JPG i inne. Zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/net/) po szczegóły.

### Q3: Czy Aspose.CAD dla .NET jest kompatybilny z najnowszymi wersjami .NET Core?

A3: Tak, Aspose.CAD dla .NET jest zaprojektowany tak, aby być kompatybilnym z najnowszymi wersjami .NET Core. Upewnij się, że masz zainstalowaną odpowiednią wersję w swoim środowisku.

### Q4: Czy mogę dalej dostosować ustawienia eksportu do moich konkretnych wymagań?

A4: Oczywiście! Dostarczony kod stanowi punkt wyjścia. Możesz zbadać dodatkowe opcje i konfiguracje w [dokumentacji Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q5: Gdzie mogę uzyskać pomoc lub podzielić się doświadczeniami z Aspose.CAD dla .NET?

A5: Dołącz do społeczności Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), aby współpracować z innymi programistami i uzyskać pomoc.

---

**Ostatnia aktualizacja:** 2026-03-24  
**Testowano z:** Aspose.CAD 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}