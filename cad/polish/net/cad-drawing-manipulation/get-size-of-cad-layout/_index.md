---
title: Uzyskaj rozmiar układu CAD w Aspose.CAD dla .NET
linktitle: Uzyskaj rozmiar układu CAD
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak pobrać rozmiar układu CAD w .NET przy użyciu Aspose.CAD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby efektywnie manipulować plikami CAD.
weight: 14
url: /pl/net/cad-drawing-manipulation/get-size-of-cad-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uzyskaj rozmiar układu CAD w Aspose.CAD dla .NET

## Wstęp

Witamy w tym kompleksowym przewodniku na temat uzyskiwania rozmiaru układów CAD przy użyciu Aspose.CAD dla .NET. Aspose.CAD to potężna biblioteka, która umożliwia programistom płynną pracę z plikami CAD. W tym samouczku przeprowadzimy Cię przez proces pobierania rozmiaru układów CAD, korzystając z praktycznych przykładów i instrukcji krok po kroku.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Można go pobrać z[Strona pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).

- Pliki dokumentów: Przygotuj pliki CAD, z którymi chcesz pracować. W tym samouczku jako przykłady wykorzystano pliki „conic_pyramid.dxf” i „Bottom_plate.dwg”.

Teraz zaczynajmy!

## Importuj przestrzenie nazw

W projekcie .NET rozpocznij od zaimportowania niezbędnych przestrzeni nazw:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Skonfiguruj katalog dokumentów

 Ustaw ścieżkę do katalogu dokumentów. Zastępować`"Your Document Directory"` z rzeczywistą ścieżką.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Określ ścieżki plików CAD

Zdefiniuj tablicę ścieżek plików CAD, które chcesz analizować. W tym przykładzie używamy plików „conic_pyramid.dxf” i „Bottom_plate.dwg”.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Krok 3: Iteruj po plikach CAD

Wykonaj iterację po każdym pliku CAD i pobierz informacje o układzie.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (przejdź do następnego kroku)
    }
}
```

## Krok 4: Uzyskaj niepuste układy

Zdefiniuj metodę pomocniczą, aby uzyskać niepuste układy w oparciu o typ pliku CAD.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (przejdź do następnego kroku)
}
```

## Krok 5: Uzyskaj układy plików DWG

Zaimplementuj logikę pobierania niepustych układów dla plików DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (przejdź do następnego kroku)
}
```

## Krok 6: Uzyskaj układy plików DXF

Zaimplementuj logikę pobierania niepustych układów dla plików DXF.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (przejdź do następnego kroku)
}
```

## Krok 7: Pobierz rozmiar układu i zapisz jako obraz

Zakończ proces uzyskiwania rozmiaru układu i zapisywania go jako obrazu.

```csharp
foreach (string layout in layouts)
{
    // ... (przejdź do następnego kroku)
}
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak uzyskać rozmiar układów CAD za pomocą Aspose.CAD dla .NET. W tym samouczku omówiono podstawowe kroki, od skonfigurowania projektu po pobranie informacji o układzie i zapisanie go jako obrazu. Teraz możesz zastosować tę wiedzę w swoich aplikacjach .NET, aby efektywnie manipulować plikami CAD.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty plików CAD, w tym DWG i DXF.

### P2: Czy mogę dostosować opcje zapisywania obrazu?

A2: Absolutnie! Możesz dostosować opcje obrazu, takie jak format i rozdzielczość, aby spełnić Twoje specyficzne wymagania.

### P3: Gdzie mogę znaleźć dodatkową dokumentację?

 A3: Patrz[Dokumentacja Aspose.CAD](https://reference.aspose.com/cad/net/) szczegółowe informacje i przykłady.

### P4: Czy dostępny jest bezpłatny okres próbny?

 O4: Tak, możesz eksplorować Aspose.CAD za pomocą[bezpłatna wersja próbna](https://releases.aspose.com/).

### Pytanie 5; Jak mogę uzyskać wsparcie techniczne?

 O5: Aby uzyskać pomoc techniczną, odwiedź stronę[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
