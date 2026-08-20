---
date: 2026-04-03
description: Dowiedz się, jak ustawić viewport i konwertować pliki DWG na PDF w C#
  przy użyciu Aspose.CAD. Ten poradnik konwersji DWG do PDF pokazuje precyzyjny eksport
  z współrzędnymi.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Konwertowanie DWG na PDF z współrzędnymi w C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak ustawić viewport podczas konwertowania DWG na PDF z współrzędnymi w C#
  – Poradnik Aspose.CAD
url: /pl/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie DWG do PDF z współrzędnymi w C# - Poradnik Aspose.CAD

## Wprowadzenie

Witamy w tym kompleksowym poradniku dotyczącym **how to set viewport** podczas konwertowania plików DWG do PDF z określonymi współrzędnymi przy użyciu Aspose.CAD dla .NET. Kontrolując viewport, otrzymujesz PDF‑y o perfekcyjnej jakości pikseli, które dokładnie odpowiadają potrzebnemu obszarowi — idealne dla rysunków konstrukcyjnych, podglądów planów pięter lub dowolnego procesu BIM.

## Szybkie odpowiedzi
- **Co oznacza „set viewport”?** Definiuje widoczny region i skalowanie rysunku CAD podczas rasteryzacji.  
- **Która biblioteka obsługuje konwersję?** Aspose.CAD for .NET.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w celach oceny; licencja komercyjna jest wymagana w produkcji.  
- **Obsługiwane platformy?** Windows, Linux i macOS z .NET 5/6/7 lub .NET Framework 4.6+.  
- **Typowy czas implementacji?** Około 10‑15 minut dla podstawowej konwersji.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące wymagania wstępne:

- **Aspose.CAD Library** – Pobierz i zainstaluj bibliotekę Aspose.CAD dla .NET. Bibliotekę znajdziesz [tutaj](https://releases.aspose.com/cad/net/).
- **Development Environment** – Visual Studio, Rider lub dowolne IDE wspierające rozwój w .NET.
- **DWG File** – Przygotuj plik DWG do konwersji. Możesz użyć dostarczonego przykładowego pliku lub własnego pliku DWG.

## Jak ustawić viewport dla precyzyjnego eksportu PDF

Ustawienie viewportu jest kluczowym krokiem, który pozwala zdefiniować dokładny obszar rysunku, który chcesz wyrenderować. W poniższym kodzie tworzymy nowy `CadVportTableObject`, pozycjonujemy go za pomocą współrzędnej lewego górnego rogu oraz obliczamy szerokość, wysokość i współczynnik proporcji. To jest implementacja **how to set viewport**, która napędza resztę konwersji.

## Importowanie przestrzeni nazw

W swoim projekcie C# zaimportuj niezbędne przestrzenie nazw:

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

Rozbijmy kod na przewodnik krok po kroku, aby lepiej go zrozumieć:

## Krok 1: Zdefiniuj katalog dokumentu

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Ustaw ścieżkę do źródłowego pliku DWG

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

## Krok 4: Zdefiniuj współrzędne i viewport  

Tutaj faktycznie **set the viewport** (how to set viewport), określając lewy górny róg, szerokość i wysokość obszaru, który chcesz wyeksportować.

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

## Krok 5: Zastosuj ustawienia viewportu

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

Teraz łączymy wszystko razem i **convert DWG to PDF** przy użyciu przygotowanych opcji rasteryzacji.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Krok 7: Wyświetl komunikat sukcesu

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Typowe przypadki użycia

- **Construction documentation** – Generuj drukowalne PDF‑y konkretnych sekcji planu piętra.  
- **BIM coordination** – Eksportuj tylko interesujący obszar do wykrywania kolizji.  
- **Client presentations** – Dostarcz czysty PDF wybranego pomieszczenia lub elewacji bez ujawniania całego rysunku.

## Podsumowanie

Gratulacje! Pomyślnie **converted DWG to PDF** z precyzyjnymi współrzędnymi i nauczyłeś się **how to set viewport** przy użyciu Aspose.CAD dla .NET. Ten **dwg to pdf tutorial** pokazuje, jak **create pdf from dwg** oraz **export dwg as pdf c#**, zachowując pełną kontrolę nad obszarem wyjściowym.

## FAQ

### Q1: Czy mogę używać Aspose.CAD z innymi formatami plików CAD?

A1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne.

### Q2: Jak mogę obsłużyć błędy podczas procesu konwersji?

A2: Zaimplementuj mechanizmy obsługi błędów przy użyciu bloków try‑catch, aby przechwytywać i zarządzać wyjątkami.

### Q3: Czy Aspose.CAD jest odpowiedni zarówno dla środowisk Windows, jak i Linux?

A3: Tak, Aspose.CAD jest kompatybilny zarówno z platformami Windows, jak i Linux.

### Q4: Czy mogę dalej dostosować wyjście PDF?

A4: Oczywiście! Zapoznaj się z rozbudowanymi opcjami oferowanymi przez Aspose.CAD, aby dostosować wyjście PDF do swoich konkretnych wymagań.

### Q5: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społecznościowe?

A5: Odwiedź [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie społeczności i dyskusje.

## Dodatkowe często zadawane pytania

**Q: Czy to podejście działa z dużymi plikami DWG (setki MB)?**  
A: Tak. Rasteryzacja jest wykonywana strona po stronie, a możesz dostosować `rasterizationOptions` (np. `Resolution`), aby zrównoważyć jakość i zużycie pamięci.

**Q: Czy mogę wyeksportować wiele viewportów na oddzielne strony PDF?**  
A: Możesz iterować przez `cadImage.ViewPorts`, ustawiać każdy jako aktywny i wywoływać `Save` dla każdej strony, a następnie scalać PDF‑y przy użyciu Aspose.PDF.

**Q: Czy można dodać znak wodny do wygenerowanego PDF?**  
A: Po zapisaniu PDF możesz otworzyć go ponownie za pomocą Aspose.PDF i zastosować znak wodny tekstowy lub graficzny przed udostępnieniem go użytkownikowi.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}