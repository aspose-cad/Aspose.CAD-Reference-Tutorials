---
title: Eksportowanie obrazów 3D do formatu PDF - samouczek Aspose.CAD
linktitle: Eksportowanie obrazów 3D do formatu PDF
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Bez wysiłku konwertuj obrazy 3D CAD do formatu PDF za pomocą Aspose.CAD dla .NET. Postępuj zgodnie z naszym samouczkiem krok po kroku, aby bezproblemowo eksportować pliki PDF.
weight: 10
url: /pl/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie obrazów 3D do formatu PDF - samouczek Aspose.CAD

## Wstęp

Czy chcesz bezproblemowo eksportować obrazy 3D do formatu PDF za pomocą Aspose.CAD dla .NET? Ten samouczek krok po kroku poprowadzi Cię przez proces, upewniając się, że wykorzystasz moc Aspose.CAD do bezproblemowej konwersji obrazów 3D do formatu PDF.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD dla .NET. Jeśli nie, możesz pobrać go ze strony[Strona pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).

- Katalog dokumentów: skonfiguruj katalog, w którym przechowywane są pliki CAD i zanotuj ścieżkę.

## Importuj przestrzenie nazw

W swoim projekcie .NET zaimportuj niezbędne przestrzenie nazw do pracy z Aspose.CAD. Dodaj następujące wiersze na górze pliku kodu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Załaduj obraz CAD

 Rozpocznij od załadowania obrazu CAD, który chcesz wyeksportować do pliku PDF. Użyj`Load` metoda z biblioteki Aspose.CAD. Zastępować`"conic_pyramid.dxf"` ze ścieżką do pliku CAD.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Twój kod do załadowania obrazu CAD znajduje się tutaj
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

 Skonfiguruj opcje rasteryzacji obrazu CAD. Ustaw parametry, takie jak szerokość strony, wysokość strony i układy. Odkomentuj linię powiązaną z`TypeOfEntities` jeśli twoje podmioty są 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 3: Ustaw opcje PDF

Utwórz opcje PDF i powiąż je z opcjami rasteryzacji.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Zapisz jako plik PDF

Zapisz obraz CAD jako plik PDF, korzystając ze skonfigurowanych opcji. Określ ścieżkę wyjściową pliku PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś obrazy 3D do formatu PDF przy użyciu Aspose.CAD dla .NET. Dzięki temu prostemu samouczkowi bez trudu przekonwertujesz pliki CAD na bardziej przystępny format.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje szeroką gamę formatów CAD, zapewniając elastyczność w obsłudze różnych typów plików.

### P2: Czy mogę dostosować wymiary strony podczas eksportowania do pliku PDF?

A2: Absolutnie. W samouczku pokazano, jak skonfigurować szerokość i wysokość strony zgodnie z własnymi wymaganiami.

### P3: Czy dostępne są licencje tymczasowe dla Aspose.CAD?

 A3: Tak, możesz uzyskać tymczasowe licencje na Aspose.CAD odwiedzając stronę[Licencja tymczasowa](https://purchase.aspose.com/temporary-license/).

### P4: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?

 A4: Udaj się do[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie i współpracę ze społecznością.

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?

 O5: Tak, możesz poznać funkcje Aspose.CAD, uzyskując dostęp do[bezpłatna wersja próbna](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
