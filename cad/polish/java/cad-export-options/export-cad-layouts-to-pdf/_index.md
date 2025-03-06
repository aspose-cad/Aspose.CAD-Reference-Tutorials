---
title: Eksportuj układy CAD do formatu PDF za pomocą Aspose.CAD dla Java
linktitle: Eksportuj układy CAD do formatu PDF
second_title: Aspose.CAD API Java
description: Przeglądaj Aspose.CAD dla Java, aby bez wysiłku eksportować układy CAD do formatu PDF. Wydajny, niezawodny i przyjazny dla programistów.
weight: 11
url: /pl/java/cad-export-options/export-cad-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj układy CAD do formatu PDF za pomocą Aspose.CAD dla Java

## Wstęp

W stale rozwijającej się dziedzinie projektowania wspomaganego komputerowo (CAD), Aspose.CAD dla Java wyróżnia się jako potężne narzędzie do manipulowania i konwertowania plików CAD. W tym samouczku przeprowadzimy Cię przez proces eksportowania układów CAD do formatu PDF przy użyciu Aspose.CAD dla Java. Niezależnie od tego, czy jesteś doświadczonym programistą, czy po prostu nurkujesz w świecie CAD, ten przewodnik krok po kroku pomoże Ci wykorzystać pełny potencjał tej wszechstronnej biblioteki Java.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla Java: Upewnij się, że masz zainstalowaną bibliotekę. Można go pobrać ze strony Aspose[Tutaj](https://releases.aspose.com/cad/java/).

- Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne Java.

Teraz, gdy już wszystko skonfigurowałeś, zacznijmy od samouczka.

## Importuj przestrzenie nazw

W kodzie Java zacznij od zaimportowania niezbędnych przestrzeni nazw. Importy te zapewniają dostęp do klas i metod potrzebnych do pracy z Aspose.CAD dla Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Krok 1: Załaduj plik CAD

 Rozpocznij od załadowania pliku CAD do aplikacji Java za pomocą`Image.load` metoda. Zastępować`"conic_pyramid.dxf"` ze ścieżką do pliku CAD.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Krok 2: Ustaw opcje rasteryzacji

 Utwórz instancję`CadRasterizationOptions` aby zdefiniować sposób rastrowania elementów CAD. Dostosuj parametry, takie jak szerokość strony, wysokość strony i skalowanie układu, zgodnie z własnymi wymaganiami.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Krok 3: Ustaw opcje PDF

 Utwórz instancję`PdfOptions` i powiąż go z opcjami rasteryzacji. Dodatkowo ustaw opcje graficzne dla eksportu PDF, takie jak tryb wygładzania, wskazówka dotycząca renderowania tekstu i tryb interpolacji.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Krok 4: Eksportuj do pliku PDF

 Na koniec wyeksportuj układy CAD do pliku PDF za pomocą`save` metoda`cadImage` obiekt.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Gratulacje! Pomyślnie wyeksportowałeś układy CAD do formatu PDF przy użyciu Aspose.CAD dla Java. Zachęcamy do zapoznania się z dodatkowymi funkcjami i funkcjonalnościami oferowanymi przez Aspose.CAD, aby ulepszyć doświadczenie manipulacji plikami CAD.

## Wniosek

W tym samouczku przeszliśmy przez proces eksportowania układów CAD do formatu PDF przy użyciu Aspose.CAD dla Java. Dzięki solidnym funkcjom i łatwemu w użyciu interfejsowi API, Aspose.CAD umożliwia programistom efektywną pracę z plikami CAD w aplikacjach Java.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi formatami plików CAD?

 Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne. Sprawdź dokumentację[Tutaj](https://reference.aspose.com/cad/java/) aby uzyskać pełną listę.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla Java?

 Odpowiedź 2: Tak, możesz poznać funkcje Aspose.CAD w ramach bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla Java?

 A3: Odwiedź forum Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19) za wsparcie społeczności. Aby uzyskać wsparcie premium, rozważ zakup licencji[Tutaj](https://purchase.aspose.com/buy).

### P4: Jaka jest różnica między automatycznym i ręcznym skalowaniem układu?

O4: Automatyczne skalowanie układu dostosowuje rozmiar układu na podstawie określonych wymiarów strony, natomiast skalowanie ręczne umożliwia ustawienie niestandardowych wartości skalowania.

### P5: Czy mogę dostosować wygląd eksportowanych plików PDF?

O5: Tak, możesz dostosować opcje graficzne w kodzie, aby kontrolować jakość i wygląd eksportowanego pliku PDF.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
