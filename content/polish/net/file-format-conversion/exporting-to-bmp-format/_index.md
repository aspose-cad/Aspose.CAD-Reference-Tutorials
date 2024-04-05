---
title: Eksport do formatu BMP - poradnik Aspose.CAD
linktitle: Eksport do formatu BMP
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Poznaj płynny świat eksportu obrazów 3D do BMP przy użyciu Aspose.CAD dla .NET. Postępuj zgodnie z naszym samouczkiem, aby uzyskać bezproblemową obsługę.
type: docs
weight: 11
url: /pl/net/file-format-conversion/exporting-to-bmp-format/
---
## Wstęp

dynamicznym świecie tworzenia oprogramowania Aspose.CAD dla .NET wyróżnia się jako potężne narzędzie do obsługi plików CAD. Jeśli chcesz wyeksportować obrazy CAD do powszechnie używanego formatu BMP, ten samouczek będzie Twoim przewodnikiem. W tym przewodniku krok po kroku zbadamy proces eksportowania obrazów 3D do BMP przy użyciu Aspose.CAD dla .NET. Zanurzmy się!

## Warunki wstępne

Zanim przejdziemy do tego samouczka, upewnij się, że spełnione są następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Pobierz i zainstaluj bibliotekę Aspose.CAD z[Tutaj](https://releases.aspose.com/cad/net/).
- Środowisko programistyczne: skonfiguruj środowisko programistyczne .NET.
- Plik CAD: przygotuj plik CAD do eksportu. W tym przykładzie użyjemy „18-12-11 9644 - site.dwf”.

## Importuj przestrzenie nazw

W projekcie .NET pamiętaj o zaimportowaniu niezbędnych przestrzeni nazw:

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

Rozpocznij od załadowania obrazu CAD do swojego projektu. Zastąp „Twój katalog dokumentów” rzeczywistą ścieżką katalogu.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Twój kod do załadowania obrazu znajduje się tutaj
}
```

## Krok 2: Skonfiguruj opcje eksportu BMP

Skonfiguruj opcje eksportu BMP, w tym opcje rasteryzacji wektorowej dla plików CAD.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Krok 3: Eksportuj do BMP

Wykonaj proces eksportu, określając ścieżkę wyjściową dla pliku BMP.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś obraz 3D do BMP przy użyciu Aspose.CAD dla .NET. Ten samouczek daje wgląd w wszechstronność Aspose.CAD, dzięki czemu złożone zadania stają się proste.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET z dowolnym formatem pliku CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty plików CAD, zapewniając elastyczność w Twoich projektach.

### P2: Czy dostępna jest licencja tymczasowa do celów testowych?

 A2: Oczywiście! Możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/) dla ewolucji.

### P3: Gdzie mogę znaleźć obszerną dokumentację dla Aspose.CAD?

 Odpowiedź 3: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/cad/net/) szczegółowe informacje i przykłady.

### P4: Jak szukać wsparcia lub nawiązać kontakt ze społecznością?

 A4: Odwiedź forum Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19) do zadawania pytań i nawiązywania kontaktu ze społecznością.

### P5: Czy mogę kupić Aspose.CAD dla .NET?

 A5: Tak, możesz kupić Aspose.CAD[Tutaj](https://purchase.aspose.com/buy) aby uwolnić jego pełny potencjał dla swoich projektów.
