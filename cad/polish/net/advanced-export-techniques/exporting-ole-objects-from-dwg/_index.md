---
title: Eksportowanie obiektów OLE z plików DWG - poradnik Aspose.CAD
linktitle: Eksportowanie obiektów OLE z plików DWG
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Zapoznaj się z przewodnikiem krok po kroku dotyczącym eksportowania obiektów OLE z plików DWG przy użyciu Aspose.CAD dla .NET. Zwiększ swoje umiejętności manipulowania plikami CAD bez wysiłku.
weight: 12
url: /pl/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie obiektów OLE z plików DWG - poradnik Aspose.CAD

## Wstęp

Czy chcesz z łatwością wyodrębnić obiekty OLE z plików DWG? Aspose.CAD dla .NET jest tutaj, aby usprawnić proces. W tym samouczku poprowadzimy Cię krok po kroku przez eksportowanie obiektów OLE, zapewniając maksymalne wykorzystanie tej potężnej biblioteki .NET. 

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę. Można go pobrać z[Strona pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).

-  Katalog dokumentów: skonfiguruj katalog, w którym przechowywane są pliki DWG. Zastępować`"Your Document Directory"` w podanym fragmencie kodu z rzeczywistą ścieżką.

## Importuj przestrzenie nazw

W projekcie .NET będziesz musiał zaimportować niezbędne przestrzenie nazw, aby wykorzystać funkcjonalności Aspose.CAD. Użyj następującego fragmentu kodu:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Ustaw katalog dokumentów

```csharp
string MyDir = "Your Document Directory";
```

 Zastępować`"Your Document Directory"` ze ścieżką, w której znajdują się pliki DWG.

## Krok 2: Określ pliki DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Wyświetl listę plików DWG, które chcesz przetworzyć w szyku.

## Krok 3: Skonfiguruj opcje eksportu

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Dostosuj opcje eksportu w oparciu o swoje wymagania. W tym przykładzie konfigurujemy eksport PNG z określonym układem.

## Krok 4: Iteruj po plikach i eksportuj

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Wykonaj iterację po określonych plikach DWG, załaduj każdy z nich i zapisz wyeksportowany plik PNG ze zdefiniowanymi opcjami.

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś obiekty OLE z plików DWG przy użyciu Aspose.CAD dla .NET. Ta potężna biblioteka upraszcza złożone zadania, zapewniając wydajność i elastyczność w manipulacji plikami CAD.

## Często zadawane pytania

### P1: Czy Aspose.CAD dla .NET jest odpowiedni zarówno dla młodszych, jak i starszych plików CAD?

Odpowiedź 1: Tak, Aspose.CAD dla .NET jest wszechstronny i może obsługiwać szeroką gamę plików CAD, w tym zarówno wersje młodsze, jak i starsze.

### P2: Czy mogę dostosować opcje eksportu dla różnych układów?

A2: Absolutnie! Jak pokazano w samouczku, możesz dostosować opcje eksportu, w tym układy, do swoich konkretnych potrzeb.

### P3: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla .NET?

 A3: Poznaj[Dokumentacja Aspose.CAD dla .NET](https://reference.aspose.com/cad/net/) szczegółowe informacje i przykłady.

### P4: Czy dostępny jest bezpłatny okres próbny?

 O4: Tak, możesz poznać możliwości Aspose.CAD dla .NET w ramach bezpłatnej wersji próbnej. Odwiedzać[ten link](https://releases.aspose.com/) rozpocząć.

### P5: Jak mogę uzyskać wsparcie lub połączyć się ze społecznością?

 Odpowiedź 5: Aby uzyskać wsparcie i zaangażowanie społeczności, odwiedź stronę[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
