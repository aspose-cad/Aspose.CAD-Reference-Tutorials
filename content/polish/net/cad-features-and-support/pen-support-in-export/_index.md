---
title: Ulepsz eksport CAD dzięki niestandardowym opcjom pióra w Aspose.CAD dla .NET
linktitle: Obsługa pióra w eksporcie
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak ulepszyć eksport obrazów CAD za pomocą Aspose.CAD dla .NET. Dostosuj opcje pióra, aby uzyskać oszałamiające efekty wizualne w plikach PDF, PNG, BMP i innych.
type: docs
weight: 12
url: /pl/net/cad-features-and-support/pen-support-in-export/
---
## Wstęp

Aspose.CAD dla .NET zapewnia potężny zestaw narzędzi do pracy z plikami projektowania wspomaganego komputerowo (CAD), umożliwiając programistom płynną manipulację i eksportowanie obrazów CAD. Godną uwagi funkcją jest obsługa piór podczas eksportu, umożliwiająca użytkownikom dostosowywanie ustawień początku i zakończenia piór podczas eksportowania obrazów CAD do różnych formatów, takich jak PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF i WMF.

W tym samouczku zagłębimy się w specyfikę obsługi pióra w eksporcie przy użyciu Aspose.CAD dla .NET. Omówimy każdy krok, dostarczając jasnych wyjaśnień i przykładów, które poprowadzą Cię przez proces.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Aspose.CAD dla .NET zainstalowany w Twoim środowisku programistycznym. Można go pobrać z[strona wydania](https://releases.aspose.com/cad/net/).

- Podstawowa znajomość formatów plików CAD, w szczególności DXF (Format wymiany rysunków).

- Praktyczna znajomość języka programowania C#.

## Importuj przestrzenie nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu C#:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Skonfiguruj katalog dokumentów

Zdefiniuj katalog, w którym znajduje się dokument CAD:

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Załaduj obraz CAD

Załaduj obraz CAD za pomocą Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Krok 3: Skonfiguruj opcje rasteryzacji

Utwórz opcje rasteryzacji i PDF, aby dostosować proces eksportu:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 4: Dostosuj opcje pióra

Ustaw opcje zakończeń początkowych i końcowych dla piór:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Krok 5: Zastosuj opcje rasteryzacji wektorowej

Zastosuj opcje rasteryzacji do opcji PDF:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 6: Zapisz wyeksportowany plik PDF

Zapisz obraz CAD z dostosowanymi opcjami pióra jako plik PDF:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Wniosek

W tym samouczku omówiliśmy obsługę pióra w funkcji eksportu Aspose.CAD dla .NET. Postępując zgodnie ze szczegółowym przewodnikiem, można łatwo dostosować ustawienia zakończeń początkowych i końcowych dla pisaków, zwiększając elastyczność eksportu obrazów CAD.

Możesz eksperymentować z różnymi opcjami pióra, aby uzyskać pożądane efekty wizualne w eksportowanych obrazach.

## Często zadawane pytania

### P1: Czy mogę używać tych opcji pióra do innych formatów obrazów oprócz PDF?

Odpowiedź 1: Tak, opcje pióra można zastosować do różnych formatów obrazów, takich jak PNG, BMP, GIF, JPEG i inne.

### P2: Gdzie mogę znaleźć dodatkową dokumentację dla Aspose.CAD dla .NET?

 Odpowiedź 2: Patrz[dokumentacja](https://reference.aspose.com/cad/net/) w celu uzyskania wyczerpujących informacji i przykładów.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać tymczasowe licencje na Aspose.CAD dla .NET?

 A4: Odwiedź[strona licencji tymczasowej](https://purchase.aspose.com/temporary-license/) w przypadku opcji licencjonowania tymczasowego.

### P5: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD dla .NET?

 A5: Nawiąż kontakt ze społecznością na[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).