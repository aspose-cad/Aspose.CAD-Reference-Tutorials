---
title: Eksportowanie osadzonych plików DGN - samouczek Aspose.CAD
linktitle: Eksportowanie osadzonych plików DGN
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Poznaj moc Aspose.CAD dla .NET. Dzięki temu samouczkowi krok po kroku nauczysz się bez wysiłku eksportować osadzone pliki DGN do formatu PDF.
type: docs
weight: 14
url: /pl/net/export-techniques/exporting-embedded-dgn-files/
---
## Wstęp

dynamicznym świecie tworzenia oprogramowania Aspose.CAD dla .NET wyróżnia się jako potężne narzędzie do obsługi plików CAD. Ten samouczek poprowadzi Cię przez proces eksportowania osadzonych plików DGN przy użyciu Aspose.CAD dla .NET. Niezależnie od tego, czy jesteś doświadczonym programistą, czy ciekawskim początkującym, ten przewodnik krok po kroku pomoże Ci skutecznie wykorzystać możliwości Aspose.CAD.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

1.  Aspose.CAD dla .NET: Pobierz i zainstaluj bibliotekę z[Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).

2. Środowisko programistyczne: Skonfiguruj środowisko programistyczne .NET za pomocą programu Visual Studio lub innego preferowanego IDE.

3. Przykładowy plik DXF: W tym samouczku użyjemy pliku „conic_pyramid.dxf”. Upewnij się, że masz go w wyznaczonym katalogu dokumentów.

## Importuj przestrzenie nazw

W kodzie C# pamiętaj o zaimportowaniu niezbędnych przestrzeni nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Załaduj plik DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Twój kod dalszych kroków będzie tutaj
}
```

## Krok 2: Ustaw opcje rasteryzacji

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Krok 3: Ustaw opcje PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Zapisz jako plik PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Krok 5: Wyświetl komunikat o powodzeniu

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś osadzony plik DGN do formatu PDF przy użyciu Aspose.CAD dla .NET. W tym samouczku omówiono podstawowe kroki, zapewniając podstawę do odkrywania bardziej zaawansowanych funkcjonalności oferowanych przez Aspose.CAD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET z innymi językami programowania?

Odpowiedź 1: Aspose.CAD obsługuje przede wszystkim .NET, ale Aspose udostępnia biblioteki dla różnych języków, w tym Java i Python.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?

 A2: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć obszerną dokumentację dla Aspose.CAD dla .NET?

 Odpowiedź 3: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/cad/net/).

### P4: Jak uzyskać tymczasową licencję na Aspose.CAD dla .NET?

 A4: Uzyskaj tymczasową licencję[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Potrzebujesz pomocy lub chcesz nawiązać kontakt ze społecznością?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie i dyskusje.