---
title: Eksportuj DGN do obrazu rastrowego w Aspose.CAD dla .NET
linktitle: Eksportuj DGN do obrazu rastrowego
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Konwertuj DGN na obrazy rastrowe bez wysiłku za pomocą Aspose.CAD dla .NET. Zapoznaj się z przewodnikiem krok po kroku i uwolnij moc platformy .NET w manipulacji plikami CAD.
weight: 13
url: /pl/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj DGN do obrazu rastrowego w Aspose.CAD dla .NET

## Wstęp

W dynamicznym środowisku rozwoju .NET Aspose.CAD jawi się jako potężne narzędzie do obsługi plików CAD. Ten samouczek omawia proces eksportowania plików DGN do obrazów rastrowych przy użyciu Aspose.CAD dla .NET. Jeśli chcesz bezproblemowo przekształcić pliki DGN w atrakcyjne wizualnie obrazy rastrowe, jesteś we właściwym miejscu.

## Warunki wstępne

Zanim wyruszymy w tę podróż, upewnijmy się, że spełniamy następujące warunki wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD w swoim projekcie .NET. Bibliotekę i odpowiednią dokumentację można znaleźć na stronie[strona internetowa](https://reference.aspose.com/cad/net/).

- Przykładowy plik DGN: Przygotuj plik DGN do konwersji. W naszym przykładzie użyjemy pliku „Nikon_D90_Camera.dgn”.

Przejdźmy teraz do przewodnika krok po kroku.

## Importuj przestrzenie nazw

projekcie .NET rozpocznij od zaimportowania niezbędnych przestrzeni nazw dla Aspose.CAD. Ten krok umożliwia dostęp do klas i metod wymaganych do konwersji obrazu DGN na obraz rastrowy.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DGN

 Zacznij od załadowania pliku DGN do pliku`CadImage` obiekt. Stanowi to podstawę do dalszych działań.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Tutaj znajduje się Twój kod do dalszego przetwarzania
}
```

## Krok 2: Zdefiniuj opcje rasteryzacji

 Stwórz`CadRasterizationOptions` obiektu i ustawić różne właściwości, aby dostosować proces rasteryzacji zgodnie z własnymi wymaganiami.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Krok 3: Utwórz obiekt JpegOptions

 Ponieważ naszym celem jest konwersja pliku DGN do formatu JPEG, utwórz plik`JpegOptions` obiekt i przypisz wcześniej zdefiniowany`CadRasterizationOptions` do tego.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Zapisz obraz rastrowy

 Skorzystaj z`Save` metoda`CadImage` class, aby wyeksportować plik DGN do obrazu rastrowego w żądanym formacie, w tym przypadku JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Wniosek

Gratulacje! Pomyślnie wykonałeś kroki eksportu pliku DGN do obrazu rastrowego przy użyciu Aspose.CAD dla .NET. Ten samouczek wyposażył Cię w niezbędną wiedzę pozwalającą na bezproblemową integrację tej funkcjonalności z projektami .NET.

## Często zadawane pytania

### P1: Czy mogę eksportować pliki DGN do formatów innych niż JPEG?

O1: Tak, Aspose.CAD dla .NET obsługuje różne formaty wyjściowe. Możesz odpowiednio zmodyfikować opcje w kroku 3.

### Q2 Jak mogę obsłużyć wyjątki podczas procesu konwersji?

Odpowiedź 2: Upewnij się, że masz odpowiednią obsługę wyjątków, jak pokazano w dostarczonym kodzie, aby rozwiązać potencjalne problemy.

### P3: Czy dostępna jest wersja próbna Aspose.CAD dla .NET?

 Odpowiedź 3: Tak, możesz zapoznać się z produktem w ramach bezpłatnego okresu próbnego. Odwiedzać[Tutaj](https://releases.aspose.com/) po więcej informacji.

### P4: Gdzie mogę szukać pomocy lub omówić kwestie związane z Aspose.CAD dla .NET?

 A4: Udaj się do[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.

### P5: Jak uzyskać tymczasową licencję na Aspose.CAD dla .NET?

 A5: Odwiedź[ten link](https://purchase.aspose.com/temporary-license/)aby nabyć tymczasową licencję na Twoje potrzeby rozwojowe.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
