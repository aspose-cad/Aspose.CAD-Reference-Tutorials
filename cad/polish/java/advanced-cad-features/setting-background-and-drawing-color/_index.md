---
title: Ustawianie koloru tła i rysunku za pomocą Aspose.CAD dla Java
linktitle: Ustawianie koloru tła i rysunku
second_title: Aspose.CAD API Java
description: Bez wysiłku konwertuj pliki CAD do formatu PDF i TIFF za pomocą Aspose.CAD dla Java. Ustaw niestandardowe kolory tła i rysunku, aby uzyskać oszałamiające wizualnie rezultaty.
weight: 15
url: /pl/java/advanced-cad-features/setting-background-and-drawing-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustawianie koloru tła i rysunku za pomocą Aspose.CAD dla Java

## Wstęp

dynamicznym świecie projektowania wspomaganego komputerowo (CAD) wydajna konwersja plików ma kluczowe znaczenie dla płynnej współpracy i komunikacji. Aspose.CAD dla Java jawi się jako potężne narzędzie oferujące solidne możliwości konwersji plików CAD do formatów PDF i TIFF. W tym samouczku zagłębimy się w proces ustawiania tła i koloru rysowania za pomocą Aspose.CAD dla Java, dostarczając przewodnik krok po kroku zapewniający optymalne rezultaty.

## Warunki wstępne

Zanim wyruszymy w tę podróż, upewnijmy się, że spełniliśmy następujące wymagania wstępne:

-  Biblioteka Aspose.CAD dla Java: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD dla Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/java/).

-  Katalog dokumentów: Miej dedykowany katalog na swoje pliki CAD. Zastępować`"Your Document Directory" + "CADConversion/"` ze ścieżką do swojego katalogu.

Teraz zagłębimy się w ten proces.

## Importuj przestrzenie nazw

Upewnij się, że zaimportowałeś niezbędne przestrzenie nazw, aby wykorzystać funkcjonalność Aspose.CAD dla Java. W naszym przykładzie używamy:

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Załaduj plik CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

## Krok 2: Ustaw kolor tła i rysunku

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());
```

## Krok 3: Utwórz plik PDF i zapisz

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## Krok 4: Utwórz TIFF i zapisz

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Wykonaj poniższe kroki, aby osiągnąć optymalne wyniki w konwersji CAD do PDF i TIFF przy użyciu Aspose.CAD dla Java.

## Wniosek

Aspose.CAD dla Java zapewnia programistom wszechstronny zestaw narzędzi do manipulacji plikami CAD. Opanowując zawiłości ustawiania tła i koloru rysunku, zwiększasz swoje możliwości tworzenia atrakcyjnych wizualnie i dokładnych konwersji.

## Często zadawane pytania

### P1: Czy Aspose.CAD dla Java nadaje się do konwersji zbiorczych?

A1: Absolutnie! Aspose.CAD dla Java wyróżnia się konwersją masową, zapewniając wydajność i dokładność.

### P2: Czy mogę dostosować kolor tła w wygenerowanych plikach?

Odpowiedź 2: Tak, samouczek pokazuje, jak ustawić niestandardowe kolory tła dla plików wyjściowych PDF i TIFF.

### P3: Gdzie mogę znaleźć obszerną dokumentację Aspose.CAD dla Java?

 A3: Patrz[dokumentacja](https://reference.aspose.com/cad/java/) szczegółowe informacje i przykłady.

### P4: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 4: Tak, zapoznaj się z funkcjami za pomocą[bezpłatna wersja próbna](https://releases.aspose.com/).

### P5: Jak mogę uzyskać wsparcie dla Aspose.CAD dla Java?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) szukać pomocy i współpracować ze społecznością.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
