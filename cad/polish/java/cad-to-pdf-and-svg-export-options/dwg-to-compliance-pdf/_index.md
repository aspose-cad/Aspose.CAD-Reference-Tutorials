---
title: DWG do zgodności z PDF przy użyciu Aspose.CAD dla Java
linktitle: DWG do zgodności PDF
second_title: Aspose.CAD API Java
description: Bez wysiłku konwertuj rysunki DWG do plików zgodnych z formatem PDF/A1a i PDF/A1b za pomocą Aspose.CAD dla Java. Usprawnij przepływ pracy z precyzją i łatwością.
type: docs
weight: 11
url: /pl/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---
## Wstęp

W stale rozwijającym się świecie projektowania cyfrowego konieczność konwersji rysunków DWG do zgodnych formatów PDF ma kluczowe znaczenie dla płynnej współpracy i ujednoliconej dokumentacji. Aspose.CAD dla Java jawi się jako potężne narzędzie oferujące wydajność i precyzję w tym procesie. W tym samouczku odkryjemy, jak wykorzystać Aspose.CAD dla Java do bezproblemowej konwersji plików DWG do zgodnych plików PDF, zapewniając zgodność ze standardami PDF/A1a i PDF/A1b.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Środowisko programistyczne Java: Upewnij się, że w systemie skonfigurowane jest działające środowisko programistyczne Java.
-  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Java z[link do pobrania](https://releases.aspose.com/cad/java/).
- Katalog dokumentów: Utwórz katalog do przechowywania rysunków DWG.

## Importuj przestrzenie nazw

W swoim projekcie Java zaimportuj niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD. Dodaj następujące wiersze na początku pliku Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Ustaw katalog zasobów

Zdefiniuj ścieżkę do katalogu zasobów, w którym przechowywane są rysunki DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Krok 2: Załaduj plik DWG

Załaduj plik DWG, korzystając z biblioteki Aspose.CAD.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Krok 3: Utwórz opcje PDF

Utwórz instancję PdfOptions i ustaw opcje rasteryzacji wektora.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Krok 4: Ustaw podstawowe opcje PDF

Ustaw podstawowe opcje PDF, określając standard zgodności (PDF/A1a lub PDF/A1b).

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Krok 5: Zapisz plik PDF zgodnie ze zgodnością A1a

Zapisz plik PDF z zachowaniem zgodności A1a.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Krok 6: Zmień zgodność na A1b

Zmień zgodność na PDF/A1b i zapisz plik PDF.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Powtórz te kroki dla każdego pliku DWG, który chcesz przekonwertować.

## Wniosek

Podsumowując, Aspose.CAD dla Java zapewnia solidne rozwiązanie do konwersji plików DWG do zgodnych plików PDF. Postępując zgodnie z tym szczegółowym przewodnikiem, możesz usprawnić proces konwersji i mieć pewność, że Twoje dokumenty są zgodne ze standardami branżowymi.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?

 O1: Aspose.CAD obsługuje różne wersje plików DWG, w tym najnowsze. Patrz[dokumentacja](https://reference.aspose.com/cad/java/) aby uzyskać szczegółowe informacje o kompatybilności.

### P2: Czy mogę dostosować ustawienia wyjściowe PDF za pomocą Aspose.CAD?

A2: Absolutnie! Aspose.CAD oferuje szereg opcji dostosowywania, umożliwiając dostosowanie wyjściowego pliku PDF do konkretnych wymagań.

### P3: Czy dostępna jest tymczasowa licencja dla Aspose.CAD?

 Odpowiedź 3: Tak, możesz uzyskać tymczasową licencję do celów testowych od[ten link](https://purchase.aspose.com/temporary-license/).

### P4: Gdzie mogę szukać wsparcia lub nawiązać kontakt ze społecznością Aspose.CAD?

 A4: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.

### P5: Czy mogę wypróbować Aspose.CAD za darmo przed dokonaniem zakupu?

 A5: Oczywiście! Pobierz bezpłatną wersję próbną ze strony[Tutaj](https://releases.aspose.com/) aby zbadać możliwości przed podjęciem decyzji.