---
title: Tworzenie pojedynczego pliku PDF z różnymi układami - Przewodnik Aspose.CAD
linktitle: Tworzenie pojedynczego pliku PDF z różnymi układami
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Utwórz pojedynczy plik PDF z różnymi układami za pomocą Aspose.CAD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać bezproblemową integrację i wydajne generowanie plików PDF.
type: docs
weight: 13
url: /pl/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Wstęp

Czy chcesz wygenerować pojedynczy dokument PDF z rysunku CAD o różnych układach przy użyciu Aspose.CAD dla .NET? Ten przewodnik krok po kroku przeprowadzi Cię przez cały proces, pomagając w osiągnięciu bezproblemowej integracji i wydajnego tworzenia plików PDF. Aspose.CAD dla .NET zapewnia zaawansowane funkcje do programowego manipulowania rysunkami CAD, a w tym samouczku skupimy się na tworzeniu pojedynczego pliku PDF z różnymi układami.

## Warunki wstępne

Przed przystąpieniem do samouczka upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowany Aspose.CAD dla .NET. Można go pobrać z[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: skonfiguruj środowisko programistyczne .NET i posiadaj podstawową wiedzę na temat programowania w języku C#.

## Importuj przestrzenie nazw

swoim projekcie C# uwzględnij niezbędne przestrzenie nazw, aby wykorzystać funkcjonalności Aspose.CAD dla .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Załaduj obraz CAD

```csharp
// Ścieżka do katalogu dokumentów.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Twój kod kroku 1 znajduje się tutaj
}
```

## Krok 2: Dostosuj opcje rasteryzacji

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Niestandardowe rozmiary dla kilku układów
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Krok 3: Zdefiniuj opcje PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Krok 4: Zapisz jako plik PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Teraz pomyślnie utworzyłeś pojedynczy dokument PDF z różnymi układami przy użyciu Aspose.CAD dla .NET. Zachęcamy do odkrywania większej liczby funkcji i dostosowywania kodu zgodnie ze swoimi konkretnymi wymaganiami.

## Wniosek

W tym samouczku omówiliśmy proces tworzenia pojedynczego pliku PDF z rysunku CAD o różnych układach przy użyciu Aspose.CAD dla .NET. Ta potężna biblioteka upraszcza zadania manipulacji CAD i oferuje elastyczność w różnych scenariuszach.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET z innymi formatami CAD?

O1: Tak, Aspose.CAD dla .NET obsługuje różne formaty CAD, takie jak DWG, DXF, DGN i inne.

### P2: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 2: Tak, możesz skorzystać z bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla .NET?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności.

### P4: Gdzie mogę znaleźć szczegółową dokumentację?

 Odpowiedź 4: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/cad/net/).

### P5: Czy mogę kupić licencję na Aspose.CAD dla .NET?

 Odpowiedź 5: Tak, możesz kupić licencję[Tutaj](https://purchase.aspose.com/buy).