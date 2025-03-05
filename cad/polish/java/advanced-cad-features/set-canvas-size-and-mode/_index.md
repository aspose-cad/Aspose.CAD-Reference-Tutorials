---
title: Ustaw rozmiar i tryb płótna
linktitle: Ustaw rozmiar i tryb płótna
second_title: Aspose.CAD API Java
description: Poznaj możliwości Aspose.CAD dla Java, korzystając z naszego przewodnika krok po kroku dotyczącego ustawiania rozmiaru i trybu obszaru roboczego. Bez wysiłku konwertuj pliki CAD do formatów PDF i TIFF.
type: docs
weight: 16
url: /pl/java/advanced-cad-features/set-canvas-size-and-mode/
---
## Wstęp

Czy chcesz wykorzystać moc Aspose.CAD dla Java, aby usprawnić proces konwersji CAD? Ten kompleksowy przewodnik przeprowadzi Cię przez etapy ustawiania rozmiaru i trybu płótna przy użyciu Aspose.CAD dla Java. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten samouczek zapewni Ci potrzebne informacje.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla Java: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD w swoim środowisku Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/java/).

- Katalog dokumentów: skonfiguruj katalog dokumentów do przechowywania plików CAD. Do tego katalogu będą się odwoływać w krokach samouczka.

Zacznijmy teraz od przewodnika krok po kroku.

## Importuj przestrzenie nazw

tym kroku zaimportujemy niezbędne przestrzenie nazw, aby rozpocząć Twój projekt Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Zaimportuj klasy Aspose.CAD

```java
// Ścieżka do katalogu zasobów.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 W tym fragmencie ustawiamy ścieżkę do katalogu zasobów i ładujemy plik DXF za pomocą Aspose.CAD`Image` klasa.

## Krok 2: Ustaw właściwości CadRasterizationOptions

```java
// Utwórz instancję CadRasterizationOptions i ustaw jej różne właściwości
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Tutaj tworzymy instancję`CadRasterizationOptions` i skonfiguruj właściwości, takie jak szerokość strony, wysokość strony i opcje skalowania.

## Krok 3: Utwórz PdfOptions i ustaw VectorRasterizationOptions

```java
// Utwórz instancję PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Ustaw właściwość VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Teraz tworzymy`PdfOptions` instancję i ustaw ją`VectorRasterizationOptions` właściwość do wcześniej skonfigurowanej`CadRasterizationOptions`.

## Krok 4: Eksportuj do pliku PDF

```java
// Eksportuj CAD do formatu PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Na koniec zapisujemy obraz CAD do pliku PDF, korzystając z określonych opcji.

## Krok 5: Utwórz TiffOptions i ustaw VectorRasterizationOptions

```java
// Utwórz instancję TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Ustaw właściwość VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Na tym etapie konfigurujemy plik`TiffOptions` instancję i skonfiguruj ją`VectorRasterizationOptions` nieruchomość.

## Krok 6: Eksportuj do TIFF

```java
// Eksportuj CAD do TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Na koniec zapisujemy obraz CAD do pliku TIFF, korzystając z określonych opcji.

## Wniosek

 Gratulacje! Pomyślnie ustawiłeś rozmiar i tryb płótna za pomocą Aspose.CAD dla Java. Ten samouczek zapewnia solidną podstawę dla projektów konwersji CAD. Odkryj więcej funkcji i możliwości w[Dokumentacja Aspose.CAD](https://reference.aspose.com/cad/java/).

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi frameworkami Java?

Odpowiedź 1: Tak, Aspose.CAD został zaprojektowany tak, aby bezproblemowo integrować się z różnymi frameworkami Java.

### P2: Czy dostępna jest tymczasowa licencja dla Aspose.CAD?

 Odpowiedź 2: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P3: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.

### P4: Czy mogę wypróbować Aspose.CAD za darmo?

 A4: Absolutnie! Uzyskaj bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P5: Jak kupić Aspose.CAD dla Java?

 A5: Kup produkt[Tutaj](https://purchase.aspose.com/buy).