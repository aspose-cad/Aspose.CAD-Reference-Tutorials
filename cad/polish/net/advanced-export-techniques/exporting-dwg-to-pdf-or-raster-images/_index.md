---
date: 2026-03-16
description: Naucz się konwertować pliki DWG na PDF lub obrazy rastrowe za pomocą
  Aspose.CAD dla .NET. Ten krok po kroku poradnik CAD‑do‑PDF obejmuje eksportowanie
  DWG do formatów graficznych, takich jak PNG, i pokazuje, jak efektywnie eksportować
  pliki DWG do obrazów.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak konwertować pliki DWG na PDF i obrazy rastrowe przy użyciu Aspose.CAD dla
  .NET
url: /pl/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie DWG do PDF lub obrazów rastrowych – przewodnik Aspose.CAD

## Wprowadzenie

Jeśli potrzebujesz **convert DWG to PDF** (lub do formatów rastrowych, takich jak PNG) bezpośrednio z aplikacji .NET, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię krok po kroku przez dokładne czynności potrzebne do użycia Aspose.CAD for .NET w celu wykonania konwersji, wyjaśnimy, dlaczego biblioteka jest solidnym wyborem, oraz pokażemy, jak obsłużyć zarówno wyjście PDF, jak i obrazowe przy użyciu kilku linijek kodu.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje konwersję DWG?** Aspose.CAD for .NET  
- **Czy mogę eksportować DWG do PNG oraz PDF?** Tak – te same opcje rasteryzacji działają dla obu formatów.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w produkcji.  
- **Jakie wersje .NET są wspierane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy konwersja jednostek jest obsługiwana automatycznie?** Możesz ręcznie określić system jednostek (metryczny lub imperialny), jak pokazano w kodzie.

## Co to jest „convert DWG to PDF”?
Konwersja DWG do PDF polega na wzięciu rysunku CAD (DWG) i przetworzeniu go na przenośny dokument tylko do odczytu (PDF). Jest to przydatne przy udostępnianiu projektów interesariuszom, którzy nie posiadają oprogramowania CAD, tworzeniu dokumentacji do druku lub archiwizacji rysunków w formacie czytelnym na wszystkich platformach.

## Dlaczego używać Aspose.CAD do tej konwersji?
- **Brak zewnętrznych zależności** – biblioteka działa w pełni w kodzie zarządzanym.  
- **Wysoka wierność** – zachowuje warstwy, grubości linii i informacje o układzie.  
- **Wbudowane opcje rasteryzacji** – umożliwiają eksport do PNG, JPEG, BMP itp. przy użyciu jednego obiektu konfiguracyjnego.  
- **Cross‑platform** – działa na Windows, Linux i macOS z .NET Core.

## Prerequisites

Zanim przejdziesz do samouczka, upewnij się, że masz przygotowane:

- Podstawowa znajomość programowania w .NET.  
- Zainstalowaną bibliotekę Aspose.CAD for .NET. Jeśli jej nie masz, pobierz ją [tutaj](https://releases.aspose.com/cad/net/).  
- Ulubione zintegrowane środowisko programistyczne (IDE) skonfigurowane do pracy z .NET.

## Importowanie przestrzeni nazw

Rozpocznijmy od zaimportowania niezbędnych przestrzeni nazw w Twoim projekcie .NET. Dzięki temu będziesz mieć dostęp do funkcjonalności Aspose.CAD w kodzie.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Załaduj plik DWG

Rozpocznij od załadowania pliku DWG, który chcesz przekonwertować. Zastąp `"Your Document Directory"` ścieżką do swojego pliku DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Krok 2: Konfiguracja eksportu PDF (Jak wyeksportować DWG do PDF)

Teraz skonfigurujemy ustawienia eksportu PDF. Ten przykład pokazuje, jak ustawić układ i obsłużyć konwersję jednostek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Krok 3: Eksport do PDF

Wykonaj eksport do PDF przy użyciu skonfigurowanych ustawień.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Krok 4: Eksport do obrazów rastrowych (export dwg to image)

Rozszerz funkcjonalność o eksport do obrazów rastrowych, takich jak PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Jak naprawić |
|-------|----------------|------------|
| **Blank pages in PDF** | Layout not specified correctly | Ensure `rasterizationOptions.Layouts` includes the correct layout name (e.g., `"Model"`). |
| **Incorrect dimensions** | DPI or page size mismatch | Adjust `PageHeight`, `PageWidth`, and DPI values in `CadRasterizationOptions`. |
| **Units appear wrong** | Unit conversion not defined | Use `DefineUnitSystem` to set `currentUnitIsMetric` and `currentUnitCoefficient` based on `cadImage.UnitType`. |
| **License exception** | Trial version limits | Apply a temporary or permanent license before calling `Image.Load`. |

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET w moich projektach komercyjnych?
A1: Tak, możesz. Odwiedź [purchase.aspose.com/buy](https://purchase.aspose.com/buy) po szczegóły licencjonowania.

### P2: Czy dostępna jest darmowa wersja próbna?
A2: Oczywiście! Pobierz darmową wersję próbną [tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla .NET?
A3: Przejdź na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) po pomoc społeczności.

### P4: Czy mogę uzyskać tymczasową licencję do celów testowych?
A4: Tak, tymczasową licencję znajdziesz [tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć szczegółową dokumentację?
A5: Dokumentacja jest dostępna pod adresem [Aspose.CAD](https://reference.aspose.com/cad/net/).

### P6: Jak **zapisać CAD jako PNG** w wysokiej jakości?
A6: Ustaw `PageHeight` i `PageWidth` na żądane wymiary w pikselach oraz wybierz DPI 300 lub wyższe w `CadRasterizationOptions`.

### P7: Jaki jest najlepszy sposób na **how to convert dwg**, gdy plik źródłowy zawiera wiele układów?
A7: Wypełnij `rasterizationOptions.Layouts` wszystkimi nazwami układów, które chcesz wyeksportować, a następnie iteruj po każdym układzie i wywołuj `Save` dla każdego formatu wyjściowego.

---

**Last Updated:** 2026-03-16  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}