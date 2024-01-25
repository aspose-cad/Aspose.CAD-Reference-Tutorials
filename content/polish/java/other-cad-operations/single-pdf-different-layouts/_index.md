---
title: Tworzenie dynamicznych plików PDF za pomocą Aspose.CAD dla Java
linktitle: Pojedynczy plik PDF z różnymi układami
second_title: Aspose.CAD API Java
description: Twórz wspaniałe pliki PDF z różnorodnymi układami na podstawie rysunków CAD za pomocą Aspose.CAD dla Java. Łatwa integracja i zaawansowane funkcje dla programistów Java.
type: docs
weight: 16
url: /pl/java/other-cad-operations/single-pdf-different-layouts/
---
## Wstęp

Witamy w świecie Aspose.CAD dla Java, potężnej biblioteki, która umożliwia programistom łatwe manipulowanie rysunkami CAD. W tym samouczku zajmiemy się tworzeniem pojedynczych plików PDF z różnymi układami przy użyciu Aspose.CAD dla Java. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten przewodnik krok po kroku przeprowadzi Cię przez cały proces.

## Warunki wstępne

Zanim wyruszymy w tę podróż, upewnijmy się, że spełniliśmy następujące wymagania wstępne:
- Środowisko Java: Upewnij się, że masz zainstalowaną Javę na swoim komputerze.
-  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Java z[link do pobrania](https://releases.aspose.com/cad/java/).
- Katalog dokumentów: skonfiguruj katalog dla swoich rysunków DWG.

## Importuj pakiety

W swoim projekcie Java zaimportuj niezbędne pakiety:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Krok 1: Załaduj rysunek CAD

 Rozpocznij od załadowania rysunku CAD do pliku`CadImage` obiekt:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Krok 2: Skonfiguruj opcje rasteryzacji

Skonfiguruj opcje rasteryzacji obrazu CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Krok 3: Dostosuj rozmiary strony układu

Zdefiniuj niestandardowe rozmiary dla kilku układów w rysunku CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Krok 4: Ustaw opcje PDF

Skonfiguruj opcje PDF, uwzględniając ustawienia rasteryzacji:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Zapisz jako plik PDF

Zapisz przetworzony obraz CAD jako plik PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Gratulacje! Pomyślnie utworzyłeś pojedynczy plik PDF z różnymi układami przy użyciu Aspose.CAD dla Java.

## Wniosek

W tym samouczku zbadaliśmy bezproblemową integrację Aspose.CAD dla Java w celu generowania plików PDF z różnymi układami na podstawie rysunków CAD. Elastyczność i solidne funkcje biblioteki sprawiają, że jest to doskonały wybór do zadań związanych z manipulacją CAD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi bibliotekami Java?

Odpowiedź 1: Tak, Aspose.CAD dla Java został zaprojektowany tak, aby bezproblemowo integrować się z innymi bibliotekami Java, zapewniając rozbudowaną funkcjonalność.

### P2: Czy dostępna jest wersja próbna?

 A2: Absolutnie! Możesz uzyskać dostęp do bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć dodatkowe wsparcie?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.

### P4: Jak uzyskać licencję tymczasową?

 A4: Możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę kupić pełną wersję?

A5: Kup pełną wersję Aspose.CAD dla Java[Tutaj](https://purchase.aspose.com/buy).