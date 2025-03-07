---
title: Obsługiwane elementy DGN w Aspose.CAD dla .NET
linktitle: Obsługiwane elementy DGN
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Poznaj zaawansowane funkcje Aspose.CAD for .NET do obsługi plików DGN. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby bezproblemowo pracować z elementami 2D i 3D.
weight: 18
url: /pl/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obsługiwane elementy DGN w Aspose.CAD dla .NET

## Wstęp

Czy jesteś programistą .NET i chcesz bezproblemowo pracować z plikami DGN? Aspose.CAD dla .NET zapewnia solidne rozwiązanie do wydajnej obsługi plików DGN. W tym samouczku zagłębimy się w obsługiwane elementy DGN, prowadząc Cię przez proces pracy z Aspose.CAD dla .NET.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

- Podstawowa znajomość programowania .NET.
- Program Visual Studio zainstalowany na Twoim komputerze.
-  Biblioteka Aspose.CAD dla .NET, którą możesz pobrać[Tutaj](https://releases.aspose.com/cad/net/).

## Importuj przestrzenie nazw

Aby rozpocząć projekt, zaimportuj niezbędne przestrzenie nazw do aplikacji .NET. Ten krok gwarantuje, że masz dostęp do funkcjonalności zapewnianych przez Aspose.CAD dla .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Krok 1: Załaduj plik DGN

Rozpocznij od załadowania istniejącego pliku DGN jako CadImage w aplikacji .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Twój kod tutaj
}
```

## Krok 2: Iteracja po elementach DGN

Iteruj po elementach DGN za pomocą pętli foreach. Aspose.CAD dla .NET zapewnia różnorodne typy elementów DGN, z którymi możesz pracować.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Twój kod tutaj
}
```

## Krok 3: Obsługuj wcześniej obsługiwane encje

Obsługuj wcześniej obsługiwane elementy 2D, które są teraz obsługiwane również w 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Dodatkowe przypadki
        {
            // Twój kod tutaj
            break;
        }
}
```

## Krok 4: Obsługuj obsługiwane elementy 3D

Obsługuj obsługiwane elementy 3D dostarczane przez Aspose.CAD dla .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Twój kod tutaj
            break;
        }
}
```

## Krok 5: Eksportuj i zapisz

Na koniec wyeksportuj zmodyfikowany plik DGN do obrazu rastrowego i zapisz go we wskazanym katalogu.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Wniosek

tym samouczku zbadaliśmy możliwości Aspose.CAD dla .NET w obsłudze i manipulowaniu plikami DGN. Postępując zgodnie ze szczegółowym przewodnikiem, można efektywnie pracować z obsługiwanymi elementami DGN, niezależnie od tego, czy są to elementy 2D, czy 3D. Aspose.CAD dla .NET umożliwia bezproblemową integrację przetwarzania plików DGN z aplikacjami .NET.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.CAD dla .NET?

 Odpowiedź 1: Możesz znaleźć dokumentację[Tutaj](https://reference.aspose.com/cad/net/).

### P2: Jak pobrać Aspose.CAD dla .NET?

 Odpowiedź 2: Możesz pobrać bibliotekę[Tutaj](https://releases.aspose.com/cad/net/).

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę uzyskać tymczasowe licencje na Aspose.CAD dla .NET?

 A4: Dostępne są licencje tymczasowe[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Potrzebujesz pomocy lub masz pytania?

 A5: Odwiedź społeczność Aspose.CAD dla .NET[forum wsparcia](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
