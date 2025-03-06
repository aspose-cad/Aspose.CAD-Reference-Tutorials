---
title: Eksportuj DGN jako część DWG w Aspose.CAD dla .NET
linktitle: Eksportuj DGN jako część DWG
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak eksportować DGN jako część DWG w Aspose.CAD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
weight: 11
url: /pl/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj DGN jako część DWG w Aspose.CAD dla .NET

## Wstęp

świecie programowania .NET Aspose.CAD wyróżnia się jako potężna biblioteka do pracy z plikami projektowania wspomaganego komputerowo (CAD). Ten samouczek poprowadzi Cię przez proces eksportowania pliku DGN (projekt) jako części pliku DWG (rysunek) przy użyciu Aspose.CAD dla .NET. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten przewodnik krok po kroku pomoże Ci wykorzystać możliwości Aspose.CAD, aby efektywnie wykonać to konkretne zadanie.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: skonfiguruj preferowane środowisko programistyczne .NET, takie jak Visual Studio.

- Podstawowa znajomość języka C#: Zapoznaj się z językiem programowania C#.

## Importuj przestrzenie nazw

W swoim projekcie C# uwzględnij niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD. Dodaj następujące dyrektywy using na początku pliku kodu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Podzielmy teraz dostarczony kod na kilka kroków:

## Krok 1: Zdefiniuj ścieżki plików

```csharp
//Ścieżki plików wejściowych i wyjściowych
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Krok 2: Utwórz instancję PdfOptions

```csharp
// Utwórz instancję klasy PdfOptions do eksportowania pliku DWG do formatu PDF
PdfOptions exportOptions = new PdfOptions();
```

## Krok 3: Załaduj plik DWG

```csharp
// Załaduj istniejący plik DWG jako obraz i przekonwertuj go na typ CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Krok 4: Iteruj po elementach

```csharp
// Wykonaj iterację po każdym elemencie w pliku DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Krok 5: Sprawdź typ jednostki

```csharp
// Sprawdź, czy encja jest definicją obrazu
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Krok 6: Uzyskaj ścieżkę podkładu

```csharp
// Jeśli jest to definicja obrazu, uzyskaj zewnętrzne odniesienie do obiektu
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Krok 7: Zdefiniuj opcje rasteryzacji

```csharp
// Zdefiniuj ustawienia dla obiektu CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Krok 8: Eksportuj DWG do formatu PDF

```csharp
// Wyeksportuj plik DWG do formatu PDF, wywołując metodę Save
cadImage.Save(outPath, exportOptions);
```

## Wniosek

Gratulacje! Pomyślnie przeszedłeś przez proces eksportowania pliku DGN jako części pliku DWG przy użyciu Aspose.CAD dla .NET. W tym samouczku przedstawiono podstawowe kroki i fragmenty kodu umożliwiające bezproblemowe wykonanie tego konkretnego zadania.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET w moich projektach komercyjnych?
 A1: Tak, możesz. Odwiedzać[Tutaj](https://purchase.aspose.com/buy) aby poznać opcje licencjonowania.

### P2: Czy istnieją jakieś ograniczenia dotyczące rozmiaru plików DWG, które mogę przetwarzać?
O2: Aspose.CAD obsługuje duże pliki DWG, ale mogą obowiązywać ograniczenia sprzętowe.

### P3: Czy dostępna jest wersja próbna?
A3: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać licencje tymczasowe?
 A4: Można uzyskać licencje tymczasowe[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę szukać pomocy, jeśli napotkam problemy?
 O5: Możesz odwiedzić forum Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19) dla wsparcia.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
