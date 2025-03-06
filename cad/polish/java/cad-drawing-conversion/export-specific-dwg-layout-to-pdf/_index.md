---
title: Eksportuj określony układ DWG do pliku PDF za pomocą Aspose.CAD dla Java
linktitle: Eksportuj określony układ DWG do pliku PDF
second_title: Aspose.CAD API Java
description: Zapoznaj się z przewodnikiem krok po kroku dotyczącym eksportowania określonych układów DWG do formatu PDF przy użyciu Aspose.CAD dla Java. Zoptymalizuj przepływ pracy CAD bez wysiłku.
weight: 14
url: /pl/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj określony układ DWG do pliku PDF za pomocą Aspose.CAD dla Java

## Wstęp

W dynamicznym świecie projektowania wspomaganego komputerowo (CAD), Aspose.CAD dla Java jawi się jako potężne narzędzie do manipulowania i konwertowania rysunków DWG. W tym samouczku omówimy konkretny scenariusz: eksportowanie wyznaczonego układu DWG do pliku PDF. Proces ten zapewnia precyzję i elastyczność projektów CAD.

## Warunki wstępne

Przed przystąpieniem do samouczka upewnij się, że spełnione są następujące wymagania wstępne:

- Środowisko programistyczne Java: Upewnij się, że w systemie masz funkcjonalne środowisko programistyczne Java.
-  Biblioteka Aspose.CAD: Pobierz i skonfiguruj bibliotekę Aspose.CAD dla języka Java. Możesz znaleźć drogę do biblioteki[Tutaj](https://releases.aspose.com/cad/java/).
- Plik DWG: Przygotuj plik DWG do eksportu. Możesz użyć przykładowego pliku „wizualizacja_-_Conference_room.dwg” w tym samouczku.

## Importuj przestrzenie nazw

## Krok 1: Skonfiguruj środowisko projektu

Rozpocznij od utworzenia projektu Java i upewnienia się, że biblioteka Aspose.CAD jest poprawnie zintegrowana. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/java/).

## Krok 2: Zaimportuj niezbędne pakiety

W swojej klasie Java zaimportuj wymagane pakiety Aspose.CAD, aby bezproblemowo korzystać z funkcjonalności.

```java

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 3: Załaduj plik DWG

Określ ścieżkę pliku DWG i załaduj go do obiektu obrazu Aspose.CAD.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

## Krok 4: Skonfiguruj opcje rasteryzacji

 Utwórz instancję`CadRasterizationOptions` i dostosuj jego właściwości do swoich wymagań.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Określ żądaną nazwę układu
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

## Krok 5: Ustaw opcje eksportu PDF

 Stwórz`PdfOptions` instancję i ustaw ją`VectorRasterizationOptions` właściwość do wcześniej skonfigurowanej`CadRasterizationOptions`.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 6: Eksportuj DWG do formatu PDF

Zapisz zmodyfikowany obraz do pliku PDF, kończąc proces konwersji.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Wniosek

Opanowanie sztuki eksportowania określonych układów DWG do formatu PDF przy użyciu Aspose.CAD dla Java może znacznie usprawnić przepływ pracy CAD. Dzięki podanym krokom możesz bezproblemowo zintegrować tę funkcjonalność ze swoimi projektami, zapewniając precyzję i wydajność.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi bibliotekami CAD opartymi na Javie?

Aspose.CAD dla Java jest samodzielną biblioteką, ale można ją zintegrować z innymi bibliotekami opartymi na Javie w celu uzyskania rozszerzonych funkcjonalności.

### P2: Czy są jakieś opcje licencjonowania dla Aspose.CAD?

 Tak, możesz sprawdzić opcje licencjonowania i szczegóły zakupu[Tutaj](https://purchase.aspose.com/buy).

### P3: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?

 Odwiedzać[ten link](https://purchase.aspose.com/temporary-license/) w celu uzyskania tymczasowej licencji na Aspose.CAD.

### P4: Gdzie mogę znaleźć wsparcie dla Aspose.CAD?

 W razie jakichkolwiek pytań lub pomocy odwiedź stronę[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?

 Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
