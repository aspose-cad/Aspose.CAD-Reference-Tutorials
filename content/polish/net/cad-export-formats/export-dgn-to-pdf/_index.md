---
title: Eksportuj DGN do formatu PDF w Aspose.CAD dla .NET
linktitle: Eksportuj DGN do pliku PDF
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak bez wysiłku eksportować pliki DGN do formatu PDF za pomocą Aspose.CAD dla .NET. Przewodnik krok po kroku dotyczący płynnej manipulacji plikami CAD.
type: docs
weight: 12
url: /pl/net/cad-export-formats/export-dgn-to-pdf/
---
## Wstęp

W świecie programowania .NET Aspose.CAD jest potężną biblioteką ułatwiającą manipulację i konwersję plików CAD. Jednym z typowych zadań, z jakim często spotykają się programiści, jest eksportowanie plików DGN do formatu PDF. W tym samouczku przejdziemy przez proces krok po kroku, używając Aspose.CAD dla .NET.

## Warunki wstępne

Zanim zagłębisz się w samouczek, upewnij się, że masz następujące elementy:

- Praktyczna znajomość C# i frameworka .NET.
-  Zainstalowana biblioteka Aspose.CAD dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).
- Przykładowy plik DGN, na przykład „Nikon_D90_Camera.dgn” na potrzeby tego samouczka.

## Importuj przestrzenie nazw

W projekcie C# rozpocznij od zaimportowania niezbędnych przestrzeni nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Twój kod tutaj...
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Krok 3: Utwórz opcje PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Zapisz jako plik PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś plik DGN do formatu PDF przy użyciu Aspose.CAD dla .NET. W tym samouczku omówiono podstawowe kroki, od załadowania pliku DGN po skonfigurowanie opcji rasteryzacji i zapisanie wyników w formacie PDF.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET bez wcześniejszej znajomości CAD?

A1: Absolutnie! Aspose.CAD upraszcza złożone zadania CAD, czyniąc go dostępnym dla programistów z różnym doświadczeniem.

### P2: Gdzie mogę znaleźć więcej przykładów i dokumentacji dla Aspose.CAD?

 A2: Poznaj[dokumentacja](https://reference.aspose.com/cad/net/) obszerne przewodniki i przykłady.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?

A3: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać tymczasowe licencje na Aspose.CAD?

 A4: Uzyskaj tymczasowe licencje[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Potrzebujesz pomocy lub masz pytania?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności.