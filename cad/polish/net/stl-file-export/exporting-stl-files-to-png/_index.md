---
title: Łatwa konwersja STL do PNG dzięki Aspose.CAD dla .NET
linktitle: Eksportowanie plików STL do formatu PNG
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Bez wysiłku konwertuj pliki STL do PNG za pomocą Aspose.CAD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację. Pobierz teraz!
type: docs
weight: 10
url: /pl/net/stl-file-export/exporting-stl-files-to-png/
---
## Wstęp
W dynamicznym świecie projektowania wspomaganego komputerowo (CAD) wydajna konwersja plików ma kluczowe znaczenie. Aspose.CAD dla .NET to potężny zestaw narzędzi, który upraszcza proces eksportowania plików STL do formatu PNG, zapewniając programistom elastyczność i funkcjonalność, której potrzebują. Ten samouczek poprowadzi Cię krok po kroku przez proces, zapewniając płynne przejście z STL do PNG przy użyciu Aspose.CAD.
## Warunki wstępne
Zanim przejdziemy do samouczka, upewnij się, że masz następujące elementy:
1.  Aspose.CAD dla .NET: Pobierz i zainstaluj bibliotekę Aspose.CAD. Możesz to znaleźć[Tutaj](https://releases.aspose.com/cad/net/).
2. Środowisko programistyczne: skonfiguruj preferowane środowisko programistyczne .NET.
3. Plik STL: przygotuj plik STL do konwersji. W tym samouczku użyjemy przykładowego pliku o nazwie „galeon.stl”.
## Importuj przestrzenie nazw
Aby rozpocząć proces, zaimportuj niezbędne przestrzenie nazw do swojej aplikacji .NET. Dzięki temu masz dostęp do klas i metod wymaganych do konwersji STL na PNG.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## Krok 1: Zdefiniuj katalog i ścieżkę pliku źródłowego
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
Upewnij się, że zastąpiłeś „Twój katalog dokumentów” rzeczywistą ścieżką katalogu, w którym znajduje się plik STL.
## Krok 2: Załaduj obraz CAD
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Dalsze kroki zostaną wykonane w ramach tego bloku
}
```
Ten krok ładuje plik STL jako obraz CAD, umożliwiając jego obróbkę i eksport.
## Krok 3: Ustaw opcje rasteryzacji
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
Dostosuj szerokość i wysokość strony zgodnie ze swoimi preferencjami i wymaganiami. Te ustawienia określają wymiary eksportowanego pliku PNG.
## Krok 4: Skonfiguruj opcje PNG
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
Utwórz opcje PNG, uwzględniając ustawienia rasteryzacji zdefiniowane w poprzednim kroku.
## Krok 5: Zapisz plik PNG
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
Określ ścieżkę wyjściową pliku PNG i zapisz obraz CAD w formacie PNG, korzystając z dostępnych opcji.
Powtórz te kroki, jeśli jest to potrzebne w konkretnym przypadku użycia, a pomyślnie wyeksportujesz pliki STL do formatu PNG za pomocą Aspose.CAD dla .NET.
## Wniosek
Aspose.CAD dla .NET upraszcza skomplikowane zadanie konwersji plików STL do PNG, udostępniając programistom niezawodny zestaw narzędzi. Postępując zgodnie z tym przewodnikiem krok po kroku, możesz bezproblemowo zintegrować tę funkcjonalność ze swoimi aplikacjami.
## Często zadawane pytania
### P: Czy mogę dostosować wymiary eksportowanego pliku PNG?
 Absolutnie! W kroku 3 dostosuj`PageWidth` I`PageHeight` wartości, aby spełnić Twoje specyficzne wymagania.
### P: Czy dostępna jest licencja tymczasowa do celów testowych?
 Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/) do testowania i oceny.
### P: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?
 Odwiedzić[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie i wspólne dyskusje.
### P: Czy konwersja obsługuje inne formaty plików?
 Tak, Aspose.CAD obsługuje różne formaty CAD poza STL. Patrz[dokumentacja](https://reference.aspose.com/cad/net/) dla pełnej listy.
### P: Czy mogę przetwarzać wsadowo wiele plików STL?
Z pewnością! Zaimplementuj pętlę w oparciu o podane kroki, aby przetwarzać wsadowo wiele plików STL.