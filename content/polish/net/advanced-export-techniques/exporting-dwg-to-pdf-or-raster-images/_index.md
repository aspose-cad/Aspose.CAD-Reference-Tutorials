---
title: Eksportowanie plików DWG do plików PDF lub obrazów rastrowych - Przewodnik Aspose.CAD
linktitle: Eksportowanie plików DWG do plików PDF lub obrazów rastrowych
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Zapoznaj się z obszernym przewodnikiem na temat eksportowania plików DWG do formatu PDF lub obrazów rastrowych przy użyciu Aspose.CAD dla .NET. Poznaj kroki, wymagania wstępne i poznaj tę zaawansowaną bibliotekę.
type: docs
weight: 11
url: /pl/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Wstęp

Czy chcesz bezproblemowo konwertować pliki DWG do formatu PDF lub obrazów rastrowych w aplikacji .NET? Nie szukaj dalej! Ten przewodnik krok po kroku przeprowadzi Cię przez proces korzystania z potężnej biblioteki Aspose.CAD dla .NET. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten samouczek jest przeznaczony dla wszystkich poziomów umiejętności.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że masz następujące elementy:

- Podstawowa znajomość programowania .NET.
-  Zainstalowana biblioteka Aspose.CAD dla .NET. Jeśli nie, pobierz go[Tutaj](https://releases.aspose.com/cad/net/).
- Twoje ulubione zintegrowane środowisko programistyczne (IDE) skonfigurowane do programowania .NET.

## Importuj przestrzenie nazw

Zacznijmy od zaimportowania niezbędnych przestrzeni nazw do projektu .NET. Dzięki temu masz dostęp do funkcjonalności Aspose.CAD w swoim kodzie.

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

Rozpocznij od załadowania pliku DWG, który chcesz przekonwertować. Zastąp „Twój katalog dokumentów” ścieżką do pliku DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Twój kod do ładowania pliku DWG znajduje się tutaj
}
```

## Krok 2: Skonfiguruj eksport PDF

Teraz skonfigurujmy ustawienia eksportu PDF. Ten przykład pokazuje, jak ustawić układ i obsługiwać konwersje jednostek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Sprawdź i zdefiniuj układ jednostek
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Twój kod konfigurujący eksport do pliku PDF znajduje się tutaj
```

## Krok 3: Eksportuj do pliku PDF

Wykonaj eksport do pliku PDF, korzystając ze skonfigurowanych ustawień.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Krok 4: Eksportuj do obrazów rastrowych

Rozszerz funkcjonalność o eksport do obrazów rastrowych, takich jak PNG.

```csharp
// Rozmiar A4 przy 300 DPI – 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się używać Aspose.CAD dla .NET do eksportowania plików DWG zarówno do plików PDF, jak i obrazów rastrowych. Ta potężna biblioteka usprawnia ten proces, czyniąc go wydajnym i przyjaznym dla programistów.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET w moich projektach komercyjnych?

 A1: Tak, możesz. Odwiedzać[zakup.aspose.com/buy](https://purchase.aspose.com/buy) w celu uzyskania szczegółów licencji.

### P2: Czy dostępny jest bezpłatny okres próbny?

 A2: Oczywiście! Skorzystaj z bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla .NET?

 A3: Udaj się do[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności.

### P4: Czy mogę uzyskać tymczasową licencję do celów testowych?

 A4: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć szczegółową dokumentację?

 Odpowiedź 5: Dokumentacja jest dostępna pod adresem[Aspose.CAD](https://reference.aspose.com/cad/net/).