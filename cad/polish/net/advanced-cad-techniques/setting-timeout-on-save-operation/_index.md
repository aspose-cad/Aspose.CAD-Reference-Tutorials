---
date: 2026-03-05
description: Dowiedz się, jak ustawić limit czasu operacji zapisu podczas konwertowania
  plików DWG na PDF za pomocą Aspose.CAD dla .NET. Zwiększ wydajność i kontrolę w
  swoich aplikacjach .NET.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak ustawić limit czasu operacji zapisu – Poradnik Aspose.CAD
url: /pl/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak ustawić limit czasu operacji zapisu – Aspose.CAD Tutorial

## Wprowadzenie

W tym przewodniku dowiesz się **jak ustawić limit czasu** operacji zapisu CAD, techniki, która pomaga zapobiegać przekształcaniu długotrwałych konwersji w nieodpowiadające procesy. Zarządzanie limitem czasu jest szczególnie przydatne, gdy **konwertujesz DWG na PDF** lub **eksportujesz pliki CAD PDF** w zadaniach wsadowych lub usługach sieciowych. Aspose.CAD dla .NET udostępnia przejrzyste API, które pozwala kontrolować operację zapisu, jednocześnie korzystając z potężnego silnika rasteryzacji.

## Szybkie odpowiedzi
- **Co kontroluje limit czasu?** Przerywa operację zapisu/eksportu, jeśli trwa dłużej niż określony okres.  
- **Które formaty korzystają najbardziej?** Konwersja dużych plików DWG na PDF lub obrazy rastrowe, gdzie czas przetwarzania może się różnić.  
- **Czy potrzebna jest licencja?** Wymagana jest ważna licencja Aspose.CAD do użytku produkcyjnego; darmowa wersja próbna działa w celach oceny.  
- **Czy mogę dostosować czas trwania?** Tak — po prostu zmień wartość `Thread.Sleep` (w milisekundach), aby dopasować ją do swojego scenariusza.  
- **Czy to podejście jest przyjazne dla async?** Przykład używa `Task.Factory.StartNew`, co ułatwia integrację z asynchronicznymi przepływami pracy.

## Co oznacza „jak ustawić limit czasu” w kontekście zapisu CAD?

Ustawienie limitu czasu oznacza dołączenie `InterruptionToken` do opcji zapisu i wywołanie przerwania po określonym przedziale czasu. Zapobiega to niekończącemu się zawieszaniu operacji, zapewniając przewidywalną wydajność i lepsze zarządzanie zasobami.

## Dlaczego używać Aspose.CAD do konwersji DWG na PDF z limitem czasu?
- **Reliability:** Gwarantuje, że niekontrolowana konwersja nie zablokuje Twojej usługi.  
- **Scalability:** Umożliwia przetwarzanie wielu plików równocześnie bez obawy, że pojedynczy plik zatrzyma pipeline.  
- **Quality:** Zachowuje wysoką wierność rasteryzacji Aspose.CAD, jednocześnie dodając kontrolę bezpieczeństwa.

## Wymagania wstępne

Zanim przejdziemy dalej, upewnij się, że masz następujące elementy:

- **Aspose.CAD for .NET** – zintegrowany z Twoim projektem. Możesz go pobrać [tutaj](https://releases.aspose.com/cad/net/).
- **Document Directory** – folder, w którym będą przechowywane Twoje pliki DWG źródłowe oraz wyjściowe pliki PDF.

## Importowanie przestrzeni nazw

Najpierw zaimportuj przestrzenie nazw, które dostarczają klasy potrzebne do rasteryzacji, opcji PDF oraz mechanizmu przerywania.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## Jak ustawić limit czasu operacji zapisu

Poniżej znajduje się instrukcja krok po kroku. Każdy krok zawiera krótkie wyjaśnienie, po którym następuje oryginalny blok kodu (bez zmian).

### Krok 1: Załaduj rysunek CAD

Ładujemy plik DWG źródłowy z wyznaczonego katalogu. Metoda `Image.Load` zwraca obiekt `Image`, który reprezentuje rysunek CAD.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Krok 2: Skonfiguruj opcje rasteryzacji

Ustaw opcje rasteryzacji tak, aby wyeksportowany PDF odpowiadał wymiarom oryginalnego rysunku. Tutaj kontrolujesz szerokość i wysokość strony oraz inne ustawienia renderowania.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Krok 3: Utwórz opcje PDF (Eksport CAD PDF)

Utwórz instancję `PdfOptions` i dołącz ustawienia rasteryzacji. Ten obiekt zostanie przekazany do metody `Save`, aby wygenerować wersję PDF pliku DWG.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 4: Zaimplementuj mechanizm limitu czasu

Używamy `InterruptionTokenSource`, aby uzyskać token, który może przerwać operację zapisu. Zadanie w tle wykonuje eksport, podczas gdy główny wątek śpi przez określony czas limitu (np. 10 sekund). Po zakończeniu snu wywołujemy `Interrupt()`, aby anulować operację, jeśli nadal działa.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Krok 5: Zakończ i potwierdź

Po eksporcie (lub przerwaniu) wypisz komunikat potwierdzający na konsolę. W rzeczywistej aplikacji możesz zalogować wynik lub wywołać zdarzenie.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| Eksport zawiesza się nieustannie | Brak podłączonego tokenu przerywania | Upewnij się, że `CADf.InterruptionToken = its.Token;` jest ustawiony przed uruchomieniem zadania. |
| PDF jest pusty lub uszkodzony | Niepoprawna ścieżka katalogu wyjściowego | Sprawdź, czy `OutputDir` kończy się separatorem ścieżki i nazwa pliku jest prawidłowa. |
| Limit czasu zbyt krótki, powodujący przedwczesne przerwanie | Wartość `Thread.Sleep` zbyt niska dla dużych plików | Zwiększ czas snu lub oblicz adaptacyjny limit czasu w zależności od rozmiaru pliku. |

## Najczęściej zadawane pytania

**Q1: Czy mogę dostosować czas trwania limitu?**  
A: Oczywiście. Zmień wartość przekazywaną do `Thread.Sleep` (w milisekundach), aby dopasować ją do swoich oczekiwań wydajnościowych.

**Q2: Czy istnieją inne opcje rasteryzacji?**  
A: Tak. `CadRasterizationOptions` udostępnia właściwości takie jak `Resolution`, `BackgroundColor` i `DrawType`, aby precyzyjnie dostroić wyjście PDF.

**Q3: Jak mogę obsłużyć przerwania w mojej aplikacji?**  
A: Użyj klas `InterruptionToken` i `InterruptionTokenSource` jak pokazano. Zapewniają one bezpieczny wątkowo sposób na przerwanie długotrwałych operacji.

**Q4: Czy Aspose.CAD jest odpowiedni zarówno dla plików CAD 2D, jak i 3D?**  
A: Obsługuje szeroką gamę formatów 2D i 3D, w tym DWG, DXF, DGN i inne.

**Q5: Gdzie mogę znaleźć dalszą pomoc lub wsparcie społeczności?**  
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uczestniczyć w dyskusjach społeczności, uzyskać przykładowy kod i wskazówki rozwiązywania problemów.

## Zakończenie

Postępując zgodnie z powyższymi krokami, teraz wiesz **jak ustawić limit czasu** operacji zapisu CAD, co umożliwia niezawodne **konwertowanie DWG na PDF** lub **eksportowanie plików CAD PDF** bez ryzyka nieodpowiadających procesów. Włącz ten wzorzec do konwerterów wsadowych, usług sieciowych lub dowolnego zautomatyzowanego pipeline’u, w którym istotna jest przewidywalność.

---

**Ostatnia aktualizacja:** 2026-03-05  
**Testowano z:** Aspose.CAD 24.12 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}