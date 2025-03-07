---
title: Eksportuj osadzone DGN do formatu PDF za pomocą Aspose.CAD dla Java
linktitle: Eksportuj osadzone DGN
second_title: Aspose.CAD API Java
description: Zapoznaj się z przewodnikiem krok po kroku dotyczącym eksportowania osadzonych plików DGN do formatu PDF przy użyciu Aspose.CAD dla Java. Ulepsz swoje aplikacje Java dzięki płynnej manipulacji plikami CAD.
weight: 11
url: /pl/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj osadzone DGN do formatu PDF za pomocą Aspose.CAD dla Java

## Wstęp

Witamy w tym kompleksowym samouczku na temat eksportowania osadzonych plików DGN przy użyciu Aspose.CAD dla Java. Aspose.CAD to potężna biblioteka, która umożliwia programistom Java płynną pracę z plikami CAD. W tym samouczku poprowadzimy Cię przez proces eksportowania osadzonych plików DGN do formatu PDF, korzystając z instrukcji krok po kroku. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten samouczek pomoże Ci wykorzystać możliwości Aspose.CAD w celu ulepszenia aplikacji Java.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
- Środowisko programistyczne Java: Upewnij się, że na komputerze skonfigurowano środowisko programistyczne Java.
-  Aspose.CAD dla Java: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Java z[Tutaj](https://releases.aspose.com/cad/java/).

## Importuj pakiety

Aby rozpocząć, musisz zaimportować niezbędne pakiety do swojego projektu Java. Dodaj następujące instrukcje importu do swojego kodu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Podzielmy teraz przykładowy kod na kilka kroków:

## Krok 1: Skonfiguruj ścieżki wejściowe i wyjściowe

Zdefiniuj ścieżkę katalogu, w którym znajduje się dokument i podaj nazwę wejściowego pliku DWG.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Krok 2: Załaduj plik DWG

 Załaduj plik DWG do pliku`Image` obiekt przy użyciu Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Krok 3: Skonfiguruj opcje rasteryzacji

Skonfiguruj opcje rasteryzacji, takie jak układy, które mają zostać uwzględnione w eksporcie.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 4: Skonfiguruj opcje PDF

Skonfiguruj opcje PDF, w tym opcje rasteryzacji wektorowej.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Zapisz plik PDF

Zapisz plik PDF ze skonfigurowanymi opcjami.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś osadzony plik DGN do formatu PDF przy użyciu Aspose.CAD dla Java. W tym samouczku omówiono podstawowe kroki integracji Aspose.CAD z aplikacją Java w celu wydajnej manipulacji plikami CAD.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java w projekcie komercyjnym?

 O1: Tak, Aspose.CAD dla Java jest biblioteką komercyjną. Licencję można uzyskać od[Tutaj](https://purchase.aspose.com/buy).

### P2: Czy dostępna jest bezpłatna wersja próbna?

 Odpowiedź 2: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.CAD dla Java[Tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla Java?

A3: Możesz szukać pomocy w społeczności Aspose.CAD na stronie[forum](https://forum.aspose.com/c/cad/19).

### P4: Co się stanie, jeśli potrzebuję licencji tymczasowej?

 A4: Możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć dokumentację?

 Odpowiedź 5: Dokumentacja jest dostępna[Tutaj](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
