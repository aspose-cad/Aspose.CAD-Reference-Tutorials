---
title: Wsparcie 3D dla DGN V7 w Aspose.CAD dla .NET
linktitle: Obsługa 3D dla DGN V7
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Odblokuj moc obsługi 3D dla DGN V7 w Aspose.CAD dla .NET. Postępuj zgodnie z naszym samouczkiem krok po kroku.
type: docs
weight: 20
url: /pl/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## Wstęp

Witamy w naszym kompleksowym samouczku na temat wykorzystania obsługi 3D dla DGN V7 w Aspose.CAD dla .NET! Aspose.CAD to potężna biblioteka, która umożliwia programistom bezproblemową pracę z plikami CAD w aplikacjach .NET. W tym samouczku omówimy kroki umożliwiające wykorzystanie obsługi 3D w DGN V7, zapewniając wiedzę niezbędną do ulepszenia projektów związanych z CAD.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowany Aspose.CAD dla .NET. Jeśli nie, możesz go pobrać z[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Skonfiguruj odpowiednie środowisko programistyczne, takie jak Visual Studio, do tworzenia aplikacji .NET.

- Przykładowy plik DGN: Przygotuj przykładowy plik DGN do testowania. Możesz skorzystać z dostarczonego przykładowego pliku „Nikon_D90_Camera.dgn”.

Przejdźmy teraz do kolejnych kroków, aby uzyskać obsługę 3D dla DGN V7 przy użyciu Aspose.CAD dla .NET!

## Importuj przestrzenie nazw

W aplikacji .NET zacznij od zaimportowania niezbędnych przestrzeni nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Skonfiguruj katalog dokumentów

 Upewnij się, że w projekcie masz skonfigurowany katalog dokumentów. Zastępować`"Your Document Directory"` z rzeczywistą ścieżką do katalogu dokumentów.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Załaduj plik DGN

Załaduj istniejący plik DGN jako CadImage, używając następującego kodu:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Tutaj znajduje się Twój kod do dalszego przetwarzania
}
```

## Krok 3: Skonfiguruj opcje eksportu PDF

Skonfiguruj opcje eksportu do pliku PDF, określając opcje rasteryzacji wektorowej, takie jak wymiary strony, automatyczne skalowanie układów, kolor tła i układy do eksportu.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Eksportuj tylko określone widoki
    }
};
```

## Krok 4: Zapisz obraz rastrowy

Zapisz plik DGN jako obraz rastrowy ze skonfigurowanymi opcjami.

```csharp
dgnImage.Save(outFile, options);
```

## Wniosek

Gratulacje! Udało Ci się wykorzystać Aspose.CAD dla .NET do wyeksportowania pliku DGN z obsługą 3D do obrazu rastrowego. W tym samouczku przedstawiono podstawowe kroki umożliwiające integrację tej funkcji z projektami CAD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET z innymi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty plików CAD, w tym DWG i DXF.

### P2: Jak mogę obsługiwać wyjątki podczas pracy z Aspose.CAD?

Odpowiedź 2: Zawiń kod w blok try-catch, jak pokazano w podanym przykładzie, aby sprawnie obsługiwać wyjątki.

### P3: Czy Aspose.CAD nadaje się do projektów komercyjnych?

 A3: Absolutnie! Możesz kupić Aspose.CAD dla .NET[Tutaj](https://purchase.aspose.com/buy).

### P4: Czy przed zakupem mogę wypróbować Aspose.CAD dla .NET?

A4: Oczywiście! Poznaj bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę znaleźć wsparcie społeczności dla Aspose.CAD dla .NET?

 Odpowiedź 5: Odwiedź forum społeczności[Tutaj](https://forum.aspose.com/c/cad/19).