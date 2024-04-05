---
title: Eksportowanie określonych układów do formatu PDF - Przewodnik Aspose.CAD
linktitle: Eksportowanie określonych układów do pliku PDF
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak eksportować określone układy do formatu PDF za pomocą Aspose.CAD dla .NET. Przewodnik krok po kroku dotyczący bezproblemowej integracji.
type: docs
weight: 13
url: /pl/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## Wstęp

Witamy w naszym przewodniku krok po kroku dotyczącym eksportowania określonych układów do formatu PDF przy użyciu Aspose.CAD dla .NET. Aspose.CAD to potężna biblioteka, która umożliwia programistom płynną pracę z formatami plików CAD. W tym samouczku skupimy się na eksportowaniu określonych układów z pliku DWG do formatu PDF przy użyciu Aspose.CAD w środowisku .NET.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: skonfiguruj środowisko programistyczne .NET, takie jak Visual Studio.

## Importuj przestrzenie nazw

W projekcie .NET zaimportuj niezbędne przestrzenie nazw dla Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DWG

```csharp
// Ścieżka do katalogu dokumentów.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Twój kod dalszych kroków znajduje się tutaj.
}
```

## Krok 2: Ustaw opcje CadRasterization

```csharp
// Utwórz instancję CadRasterizationOptions i ustaw jej różne właściwości
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Krok 3: Określ nazwę układu

```csharp
// Określ żądaną nazwę układu
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Krok 4: Utwórz opcje PDF

```csharp
// Utwórz instancję PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Ustaw właściwość VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Eksportuj do pliku PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Eksportuj plik DWG do formatu PDF
image.Save(MyDir, pdfOptions);
```

## Krok 6: Wyświetl komunikat o powodzeniu

```csharp
// Wyświetl komunikat o powodzeniu
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się eksportować określone układy do formatu PDF przy użyciu Aspose.CAD dla .NET. Ten przewodnik zawiera szczegółowy przewodnik, dzięki któremu możesz bez problemu zintegrować tę funkcjonalność ze swoimi projektami.

## Często zadawane pytania

### P1: Czy mogę eksportować wiele układów jednocześnie?

 A1: Tak, po prostu zmodyfikuj plik`Layouts` array w kroku 3, aby uwzględnić nazwy wszystkich żądanych układów.

### P2: Czy Aspose.CAD jest kompatybilny z innymi formatami plików CAD?

Odpowiedź 2: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne.

### P3: Jak mogę dostosować ustawienia wyjściowe PDF?

 A3: Poznaj właściwości`CadRasterizationOptions` w kroku 2, aby zapoznać się z opcjami dostosowywania.

### P4: Gdzie mogę znaleźć dodatkową dokumentację Aspose.CAD?

 A4: Odwiedź[dokumentacja](https://reference.aspose.com/cad/net/) w celu uzyskania szczegółowych informacji.

### P5: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 5: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).