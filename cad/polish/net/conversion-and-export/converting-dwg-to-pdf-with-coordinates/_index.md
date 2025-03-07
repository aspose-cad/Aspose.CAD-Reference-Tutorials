---
title: Konwersja DWG do formatu PDF ze współrzędnymi w języku C# - samouczek Aspose.CAD
linktitle: Konwersja DWG na PDF ze współrzędnymi w C#
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak przekonwertować plik DWG na format PDF z określonymi współrzędnymi w języku C# przy użyciu Aspose.CAD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać precyzyjną i wydajną konwersję plików CAD.
weight: 11
url: /pl/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwersja DWG do formatu PDF ze współrzędnymi w języku C# - samouczek Aspose.CAD

## Wstęp

Witamy w tym kompleksowym samouczku dotyczącym konwersji plików DWG do formatu PDF z określonymi współrzędnymi przy użyciu Aspose.CAD dla .NET. Aspose.CAD to potężna biblioteka, która umożliwia programistom płynną pracę z formatami plików CAD w aplikacjach .NET. W tym samouczku przeprowadzimy Cię przez proces konwersji pliku DWG do formatu PDF, podając jednocześnie określone współrzędne w celu zwiększenia precyzji.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

- Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla .NET. Możesz znaleźć drogę do biblioteki[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Upewnij się, że masz skonfigurowane kompatybilne środowisko programistyczne, w tym Visual Studio lub inne preferowane IDE.

- Plik DWG: Przygotuj plik DWG do konwersji. Możesz użyć dostarczonego przykładowego pliku lub własnego pliku DWG.

## Importuj przestrzenie nazw

W projekcie C# zaimportuj niezbędne przestrzenie nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Podzielmy kod na przewodnik krok po kroku, aby lepiej zrozumieć:

## Krok 1: Zdefiniuj katalog dokumentów

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Ustaw ścieżkę źródłowego pliku DWG

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Krok 3: Załaduj plik DWG i skonfiguruj opcje rasteryzacji

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Krok 4: Zdefiniuj współrzędne i rzutnię

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: Zastosuj ustawienia rzutni

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Krok 6: Skonfiguruj opcje PDF i eksport

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Krok 7: Wyświetl komunikat o powodzeniu

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Wniosek

Gratulacje! Pomyślnie przekonwertowałeś plik DWG na PDF z określonymi współrzędnymi przy użyciu Aspose.CAD dla .NET. W tym samouczku omówiono najważniejsze kroki i zapewniono jasny przewodnik dla programistów.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD z innymi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne.

### P2: Jak mogę poradzić sobie z błędami podczas procesu konwersji?

A2: Zaimplementuj mechanizmy obsługi błędów, używając bloków try-catch do przechwytywania wyjątków i zarządzania nimi.

### P3: Czy Aspose.CAD jest odpowiedni zarówno dla środowisk Windows, jak i Linux?

O3: Tak, Aspose.CAD jest kompatybilny zarówno z platformami Windows, jak i Linux.

### P4: Czy mogę bardziej dostosować wydruk PDF?

A4: Oczywiście! Zapoznaj się z rozbudowanymi opcjami Aspose.CAD, aby dostosować wydruk PDF do swoich konkretnych wymagań.

### P5: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
