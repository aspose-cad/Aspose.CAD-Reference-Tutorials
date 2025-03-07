---
title: Eksportuj DWG do formatu PDF lub rastra za pomocą Aspose.CAD dla Java
linktitle: Eksportuj plik DWG do pliku PDF lub rastra
second_title: Aspose.CAD API Java
description: Poznaj bezproblemowy proces eksportowania plików DWG do formatu PDF lub obrazów rastrowych w Javie przy użyciu Aspose.CAD. Ten przewodnik krok po kroku zapewnia precyzję i wydajność.
weight: 13
url: /pl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj DWG do formatu PDF lub rastra za pomocą Aspose.CAD dla Java

## Wstęp

dynamicznym świecie projektowania wspomaganego komputerowo (CAD) sprawna obsługa rysunków ma kluczowe znaczenie. Aspose.CAD dla Java zapewnia potężne rozwiązanie do eksportowania plików DWG do plików PDF lub obrazów rastrowych. Ten samouczek poprowadzi Cię przez proces, upewniając się, że wykorzystasz pełny potencjał Aspose.CAD dla Java.

## Warunki wstępne

Zanim zagłębisz się w samouczek, upewnij się, że posiadasz następujące informacje:

- Podstawowa znajomość programowania w języku Java.
-  Zainstalowana biblioteka Aspose.CAD dla Java. Jeśli nie, pobierz go[Tutaj](https://releases.aspose.com/cad/java/).
- Plik DWG do celów testowych. Można skorzystać z dostarczonego pliku „Bottom_plate.dwg”.

## Importuj przestrzenie nazw

W projekcie Java zaimportuj niezbędne przestrzenie nazw, aby rozpocząć proces:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Krok 1: Załaduj plik DWG

 Zacznij od załadowania pliku DWG przy użyciu programu Aspose.CAD`Image` klasa:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Krok 2: Określ typ jednostki

Następnie sprawdź typ jednostki wczytanego pliku DWG:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Krok 3: Ustaw opcje rasteryzacji

W zależności od typu jednostki skonfiguruj opcje rasteryzacji:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Jednostki metryczne
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Jednostki imperialne
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Krok 4: Skonfiguruj opcje PDF

Skonfiguruj opcje eksportu PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Krok 5: Zapisz jako plik PDF

Na koniec zapisz plik DWG jako plik PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

I masz to! Pomyślnie wyeksportowałeś plik DWG do formatu PDF przy użyciu Aspose.CAD dla Java.

## Wniosek

Ten samouczek zawiera przewodnik krok po kroku dotyczący wykorzystania Aspose.CAD dla Java do eksportowania plików DWG do formatu PDF lub obrazów rastrowych. Ta biblioteka upraszcza proces, umożliwiając wydajną obsługę rysunków CAD w aplikacjach Java.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi frameworkami Java?

Odpowiedź 1: Tak, Aspose.CAD dla Java płynnie integruje się z popularnymi frameworkami Java.

### P2: Czy dostępna jest tymczasowa licencja na Aspose.CAD dla Java?

 Odpowiedź 2: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P3: Gdzie mogę znaleźć wsparcie dla Aspose.CAD dla Java?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) o pomoc ze strony gminy.

### P4: Jak mogę kupić licencję na Aspose.CAD dla Java?

 A4: Możesz kupić licencję[Tutaj](https://purchase.aspose.com/buy).

### P5: Jakie jednostki obsługuje Aspose.CAD dla Java?

O5: Aspose.CAD dla Java obsługuje zarówno jednostki metryczne, jak i imperialne.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
