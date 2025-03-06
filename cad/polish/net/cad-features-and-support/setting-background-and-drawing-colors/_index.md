---
title: Ustawianie kolorów tła i rysunków w Aspose.CAD dla .NET
linktitle: Ustawianie kolorów tła i rysunku
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Opanuj Aspose.CAD dla .NET. Ustawiaj kolory tła i rysowania bez wysiłku. Postępuj zgodnie z naszym przewodnikiem krok po kroku.
weight: 15
url: /pl/net/cad-features-and-support/setting-background-and-drawing-colors/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustawianie kolorów tła i rysunków w Aspose.CAD dla .NET

## Wstęp

dynamicznym świecie rozwoju .NET Aspose.CAD jawi się jako potężne narzędzie do obsługi plików CAD. Jeśli chcesz udoskonalić swoje umiejętności manipulowania rysunkami CAD, ten samouczek będzie dla Ciebie bramą. Zagłębimy się w zawiłości ustawiania tła i rysowania kolorów za pomocą Aspose.CAD dla .NET, dostarczając przewodnik krok po kroku, który zapewni przejrzystość i skuteczność.

## Warunki wstępne

Zanim wyruszymy w tę podróż, upewnijmy się, że spełniamy następujące warunki wstępne:

- Podstawowa wiedza na temat programowania .NET.
-  Instalacja Aspose.CAD dla .NET. Jeśli jeszcze tego nie zrobiłeś, możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).
- Przykładowy plik CAD do eksperymentów. Znajdziesz go w katalogu dokumentów.

## Importuj przestrzenie nazw

W projekcie .NET rozpocznij od zaimportowania niezbędnych przestrzeni nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik CAD

Zacznij od załadowania pliku CAD, z którym chcesz pracować, używając następującego fragmentu kodu:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Tutaj znajduje się Twój kod do dalszego przetwarzania
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

 Utwórz instancję`CadRasterizationOptions` i ustaw jego właściwości dla ustawień koloru tła i rysunku:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## Krok 3: Eksportuj do pliku PDF

 Utwórz instancję`PdfOptions` i ustaw`VectorRasterizationOptions` nieruchomość:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// Eksportuj CAD do formatu PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Krok 4: Eksportuj do TIFF

 Utwórz instancję`TiffOptions` i ustaw`VectorRasterizationOptions` nieruchomość:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// Eksportuj CAD do TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się ustawiać kolory tła i rysunków w Aspose.CAD dla .NET. Ten samouczek wyposaży Cię w umiejętności łatwego manipulowania plikami CAD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET z dowolnym typem pliku CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF i DGN.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?

 Odpowiedź 2: Tak, możesz skorzystać z bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla .NET?

 Odpowiedź 3: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/cad/net/).

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?

 A4: Można uzyskać licencje tymczasowe[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Potrzebujesz pomocy lub chcesz nawiązać kontakt ze społecznością?

 Odpowiedź 5: Odwiedź forum pomocy technicznej[Tutaj](https://forum.aspose.com/c/cad/19).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
