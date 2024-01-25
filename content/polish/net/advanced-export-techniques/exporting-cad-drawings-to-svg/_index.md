---
title: Eksportowanie rysunków CAD do formatu SVG - Przewodnik Aspose.CAD
linktitle: Eksportowanie rysunków CAD do formatu SVG
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Poznaj bezproblemowy proces eksportowania rysunków CAD do formatu SVG przy użyciu Aspose.CAD dla .NET. Ulepsz swój rozwój CAD dzięki elastyczności i dostosowaniu.
type: docs
weight: 15
url: /pl/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---
## Wstęp

dynamicznym świecie CAD (Computer-Aided Design) umiejętność eksportowania rysunków do różnych formatów jest kluczową umiejętnością. SVG (Scalable Vector Graphics) to jeden z takich formatów, który zyskał popularność dzięki swojej skalowalności i wszechstronności. W tym samouczku przyjrzymy się, jak eksportować rysunki CAD do formatu SVG przy użyciu potężnej biblioteki Aspose.CAD dla .NET.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.CAD dla .NET: Pobierz i zainstaluj bibliotekę Aspose.CAD dla .NET. Możesz znaleźć drogę do biblioteki[Tutaj](https://releases.aspose.com/cad/net/).

- Środowisko programistyczne: Skonfiguruj odpowiednie środowisko programistyczne za pomocą programu Visual Studio lub dowolnego innego narzędzia programistycznego .NET.

## Importuj przestrzenie nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Ustaw katalog dokumentów

```csharp
// Ścieżka do katalogu dokumentów.
string MyDir = "Your Document Directory";
```

## Krok 2: Załaduj rysunek CAD

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## Krok 3: Skonfiguruj opcje eksportu SVG

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## Krok 4: Zapisz plik SVG

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Wykonując te proste kroki, możesz bezproblemowo eksportować rysunki CAD do SVG przy użyciu Aspose.CAD dla .NET. Biblioteka zapewnia elastyczność i opcje dostosowywania, dzięki czemu możesz dostosować wydruk do swoich wymagań.

## Wniosek

Podsumowując, Aspose.CAD dla .NET upraszcza proces eksportowania rysunków CAD do SVG. Intuicyjny interfejs API i solidne funkcje sprawiają, że jest to cenne narzędzie dla programistów pracujących z aplikacjami CAD.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami CAD?

O1: Aspose.CAD obsługuje różne formaty CAD, w tym DWG i DXF, zapewniając szeroką kompatybilność.

### P2: Czy mogę dostosować tryb kolorów podczas eksportowania do formatu SVG?

Odpowiedź 2: Tak, Aspose.CAD pozwala wybrać tryb koloru, zapewniając elastyczność wydruku.

### P3: Czy dostępne są licencje tymczasowe do celów testowych?

 Odpowiedź 3: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/) dla ewolucji.

### P4: Gdzie mogę znaleźć szczegółową dokumentację dla Aspose.CAD?

 A4: Dokumentacja jest dostępna[Tutaj](https://reference.aspose.com/cad/net/).

### P5: Jak mogę uzyskać pomoc lub zadać pytania związane z Aspose.CAD?

 Odpowiedź 5: Odwiedź forum społeczności[Tutaj](https://forum.aspose.com/c/cad/19) za wsparcie i dyskusje.