---
title: Praca z plikami DWG w języku C# — pobieranie rozmiaru układu DWF
linktitle: Praca z plikami DWG w języku C# — pobieranie rozmiaru układu DWF
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Poznaj moc Aspose.CAD dla .NET w obsłudze plików DWG. Dowiedz się, jak łatwo wyodrębniać rozmiary układów DWF przy użyciu języka C#.
weight: 10
url: /pl/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Praca z plikami DWG w języku C# — pobieranie rozmiaru układu DWF

## Wstęp

W dziedzinie projektowania wspomaganego komputerowo (CAD) i programowania .NET Aspose.CAD jest potężnym narzędziem do obsługi plików DWG. Ten samouczek poprowadzi Cię przez proces pracy z plikami DWG w języku C# i wyodrębniania rozmiaru układu DWF. Zanim zagłębimy się w kod, upewnijmy się, że masz wszystko skonfigurowane, aby wyruszyć w tę podróż.

## Warunki wstępne

Aby bezproblemowo wykonać ten samouczek, upewnij się, że spełnione są następujące wymagania wstępne:

-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowany Aspose.CAD dla .NET. Można go pobrać z[Strona pobierania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).

Teraz, gdy masz już niezbędne narzędzia, wskoczmy na arenę kodowania.

## Importuj przestrzenie nazw

Zanim zaczniemy pracować z kodem, zaimportujmy wymagane przestrzenie nazw:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Te przestrzenie nazw zapewnią podstawowe klasy i metody obsługi plików CAD za pomocą Aspose.CAD w aplikacji C#.

## Krok 1: Skonfiguruj swoje środowisko

Zacznij od upewnienia się, że masz skonfigurowane odpowiednie środowisko dla swojego projektu. Odwołaj się do biblioteki Aspose.CAD w swoim projekcie C#.

## Krok 2: Zdefiniuj ścieżki plików

Zdefiniuj ścieżki do pliku DWG i katalog wyjściowy dla wygenerowanych plików JPG:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Krok 3: Załaduj obraz DWF

Załaduj obraz DWF za pomocą Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Tutaj znajdziesz kod opisujący dalsze kroki
}
```

## Krok 4: Iteruj po stronach

Iteruj po stronach obrazu DWF:

```csharp
foreach (var page in image.Pages)
{
    // Tutaj znajdziesz kod opisujący dalsze kroki
}
```

## Krok 5: Uzyskaj informacje o układzie

Uzyskaj informacje o układzie z każdej strony:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Krok 6: Skonfiguruj opcje JPG

Skonfiguruj opcje zapisywania układu jako pliku JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Tutaj znajdziesz kod opisujący dalsze kroki
}
```

## Krok 7: Określ rozmiar strony

Określ rozmiar układu DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Tutaj znajdziesz kod opisujący dalsze kroki
```

## Krok 8: Skonfiguruj wymiary strony

Skonfiguruj wymiary strony w oparciu o typ jednostki:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Krok 9: Zapisz plik JPG

Zapisz plik JPG z określonymi opcjami:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Teraz pomyślnie wyodrębniłeś rozmiar układu DWF z pliku DWG przy użyciu Aspose.CAD w C#. Zachęcamy do zapoznania się z większą liczbą funkcji i funkcjonalności, które Aspose.CAD oferuje dla rozwoju .NET.

## Wniosek

W tym samouczku omówiliśmy proces pracy z plikami DWG w języku C# przy użyciu Aspose.CAD. Wykonując te kroki, możesz nie tylko uzyskać rozmiar układu DWF, ale także wykorzystać możliwości Aspose.CAD do różnych zadań związanych z CAD w swoich projektach .NET.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny z najnowszymi formatami plików DWG?

 O1: Aspose.CAD obsługuje różne formaty plików DWG, w tym najnowsze wersje. Patrz[dokumentacja](https://reference.aspose.com/cad/net/) aby uzyskać szczegółowe informacje na temat zgodności.

### P2: Czy mogę używać Aspose.CAD zarówno do projektów komercyjnych, jak i osobistych?

 Odpowiedź 2: Tak, Aspose.CAD oferuje elastyczne opcje licencjonowania zarówno do użytku komercyjnego, jak i osobistego. Odwiedzić[strona zakupu](https://purchase.aspose.com/buy) po więcej szczegółów.

### P3: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?

 A3: Możesz uzyskać tymczasową licencję od[Tutaj](https://purchase.aspose.com/temporary-license/) w celach ewaluacyjnych.

### P4: Gdzie mogę znaleźć wsparcie dla Aspose.CAD?

A4: W przypadku jakichkolwiek pytań lub pomocy odwiedź stronę[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?

 Odpowiedź 5: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.CAD[Tutaj](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
