---
title: Konwersja pliku DWG do formatu PDF zgodności - samouczek Aspose.CAD
linktitle: Konwersja pliku DWG do formatu PDF zgodności
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Konwertuj plik DWG na zgodny plik PDF za pomocą Aspose.CAD dla .NET. Postępuj zgodnie z naszym samouczkiem, aby uzyskać wskazówki krok po kroku.
weight: 13
url: /pl/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwersja pliku DWG do formatu PDF zgodności - samouczek Aspose.CAD

## Wstęp

Witamy w naszym samouczku krok po kroku dotyczącym konwersji plików DWG do formatu Compliance PDF przy użyciu Aspose.CAD dla .NET. Aspose.CAD to potężny interfejs API .NET, który umożliwia programistom bezproblemową pracę z formatami plików CAD. W tym samouczku przeprowadzimy Cię przez proces konwersji pliku DWG do formatu Compliance PDF, podając szczegółowe przykłady i objaśnienia.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że biblioteka Aspose.CAD jest zintegrowana z projektem .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Zainstaluj działające środowisko programistyczne .NET i upewnij się, że jest ono poprawnie skonfigurowane.

- Przykładowy plik DWG: Pobierz przykładowy plik DWG, który chcesz przekonwertować do formatu PDF zgodności.

## Importuj przestrzenie nazw

W swoim projekcie .NET zaimportuj niezbędne przestrzenie nazw, aby móc korzystać z funkcjonalności Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Podzielmy teraz proces konwersji pliku DWG na plik PDF zgodny z przepisami na kilka etapów.

## Krok 1: Załaduj plik DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Krok 2: Ustaw opcje rasteryzacji

 Utwórz instancję`CadRasterizationOptions` i skonfiguruj jego właściwości, takie jak kolor tła, szerokość strony i wysokość strony.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Krok 3: Utwórz opcje PDF

 Utwórz instancję`PdfOptions` i ustaw opcje rasteryzacji wektorowej.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Krok 4: Zapisz jako plik PDF (zgodność A1a)

Zapisz obraz CAD jako plik PDF zgodny ze standardem A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Krok 5: Zapisz jako plik PDF (zgodność A1b)

Zmień typ zgodności na A1b i zapisz obraz CAD w formacie Compliance PDF.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Wniosek

Gratulacje! Pomyślnie przekonwertowałeś plik DWG do formatu Compliance PDF przy użyciu Aspose.CAD dla .NET. Ten samouczek stanowi kompleksowy przewodnik dla programistów chcących zintegrować możliwości konwersji CAD ze swoimi aplikacjami.

## Często zadawane pytania

### P1: Czy mogę konwertować inne formaty CAD do formatu Compliance PDF przy użyciu Aspose.CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, umożliwiając konwersję do formatu Compliance PDF.

### P2: Czy Aspose.CAD jest kompatybilny z .NET Core?

O2: Tak, Aspose.CAD jest kompatybilny zarówno z .NET Framework, jak i .NET Core.

### P3: Czy są jakieś opcje licencjonowania dla Aspose.CAD?

 Odpowiedź 3: Tak, możesz zapoznać się z opcjami licencjonowania[Tutaj](https://purchase.aspose.com/buy).

### P4: Czy dostępny jest bezpłatny okres próbny?

 A4: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę uzyskać wsparcie dla Aspose.CAD?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w przypadku jakichkolwiek pytań związanych ze wsparciem.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
