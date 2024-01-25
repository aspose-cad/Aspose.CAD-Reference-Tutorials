---
title: Przewodnik konwersji DGN do formatu PDF - Aspose.CAD dla Java
linktitle: Wsparcie dla DGN V7
second_title: Aspose.CAD API Java
description: Bez wysiłku konwertuj pliki DGN do formatu PDF za pomocą Aspose.CAD dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać bezproblemową integrację i efektywny przepływ pracy.
type: docs
weight: 11
url: /pl/java/other-cad-operations/support-for-dgn-v7/
---
## Wstęp

W dynamicznym świecie CAD (projektowanie wspomagane komputerowo) wydajna konwersja plików DGN (projektowanie) do formatu PDF (przenośny format dokumentu) jest kluczowym wymogiem. Aspose.CAD dla Java jawi się jako potężne rozwiązanie, oferujące bezproblemową integrację i solidne możliwości. Ten przewodnik krok po kroku ma na celu przeprowadzić Cię przez proces eksportowania plików DGN do formatu PDF przy użyciu Aspose.CAD dla Java, zapewniając płynny i wydajny przepływ pracy.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
-  Aspose.CAD dla biblioteki Java: Pobierz i zainstaluj bibliotekę z[Strona pobierania Aspose.CAD dla Java](https://releases.aspose.com/cad/java/).
- Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne Java.

## Importuj pakiety

Zacznij od zaimportowania niezbędnych pakietów do projektu Java:

## Krok 1: Zaimportuj niezbędne pakiety

W swoim projekcie Java zaimportuj wymagane pakiety dla Aspose.CAD dla Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Krok 2: Ustaw ścieżki plików

Zdefiniuj ścieżki wejściowego pliku DGN i wyjściowego pliku PDF.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Krok 3: Załaduj obraz DGN

Załaduj obraz DGN przy użyciu biblioteki Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Krok 4: Skonfiguruj opcje eksportu PDF

Skonfiguruj opcje eksportu do pliku PDF, w tym wymiary strony, automatyczne skalowanie układu, kolor tła i określone układy do wyeksportowania.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //eksportuj tylko 4 widoki (1,2,3 i 9).
options.setVectorRasterizationOptions(vectorOptions);
```

## Krok 5: Zapisz plik PDF

Zapisz obraz DGN jako plik PDF z określonymi opcjami.

```java
objImage.save(outFile, options);
```

Powtórz te kroki dla różnych plików DGN, dostosowując ścieżki plików i opcje w razie potrzeby.

## Wniosek

Dzięki Aspose.CAD dla Java konwersja plików DGN do formatu PDF staje się prostym procesem. Ten przewodnik wyposaża Cię w wiedzę niezbędną do bezproblemowej integracji biblioteki z projektami Java, ułatwiając wydajną konwersję plików CAD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, zapewniając wszechstronną funkcjonalność wykraczającą poza konwersję DGN do formatu PDF.

### P2: Czy dostępna jest tymczasowa licencja na Aspose.CAD dla Java?

 Odpowiedź 2: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/) do celów testowych.

### P3: Jak mogę uzyskać pomoc lub zadać pytania dotyczące Aspose.CAD dla Java?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)nawiązać kontakt ze społecznością i poprosić o pomoc.

### P4: Jakie układy mogę wyeksportować podczas konwersji DGN do formatu PDF?

 O4: Możesz określić układy do wyeksportowania, dostosowując plik`setLayouts` tablica w kodzie.

### P5: Gdzie mogę znaleźć obszerną dokumentację dla Aspose.CAD dla Java?

 Odpowiedź 5: Patrz[Aspose.CAD dla dokumentacji Java](https://reference.aspose.com/cad/java/) aby uzyskać szczegółowe informacje.