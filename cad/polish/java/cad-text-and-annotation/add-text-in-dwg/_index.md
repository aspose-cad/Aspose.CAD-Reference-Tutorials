---
title: Dodaj tekst w formacie DWG za pomocą Aspose.CAD dla Java
linktitle: Dodaj tekst w formacie DWG
second_title: Aspose.CAD API Java
description: Ulepsz swoje rysunki DWG bez wysiłku dzięki Aspose.CAD dla Java. Dodaj tekst bezproblemowo, korzystając z naszego przewodnika krok po kroku.
type: docs
weight: 10
url: /pl/java/cad-text-and-annotation/add-text-in-dwg/
---
## Wstęp

W dziedzinie projektowania wspomaganego komputerowo (CAD) Aspose.CAD dla Java wyróżnia się jako potężne narzędzie do manipulowania i konwertowania rysunków DWG. Jedną z przydatnych funkcji jest możliwość płynnego dodawania tekstu do plików DWG. W tym samouczku przeprowadzimy Cię przez proces dodawania tekstu do rysunków DWG przy użyciu Aspose.CAD dla Java.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla biblioteki Java: Pobierz i zainstaluj bibliotekę z[Strona Aspose.CAD dla Java](https://releases.aspose.com/cad/java/).

- Zestaw Java Development Kit (JDK): Upewnij się, że w systemie zainstalowana jest najnowsza wersja pakietu JDK.

- Rysunek DWG: Przygotuj plik rysunku DWG, do którego chcesz dodać tekst.

## Importuj przestrzenie nazw

kodzie Java zaimportuj niezbędne przestrzenie nazw dla Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Podzielmy teraz dostarczony fragment kodu na kilka kroków:

## Krok 1: Skonfiguruj katalog dokumentów i ścieżkę pliku DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Krok 2: Załaduj obraz DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Krok 3: Utwórz obiekt CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## Krok 4: Dodaj tekst do CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Krok 5: Skonfiguruj opcje PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 6: Skonfiguruj opcje CadRasterization

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 7: Zapisz zmodyfikowany plik DWG jako plik PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Wykonując poniższe kroki, będziesz mógł bezproblemowo dodawać tekst do rysunków DWG przy użyciu Aspose.CAD dla Java.

## Wniosek

Aspose.CAD dla Java umożliwia programistom programowe ulepszanie i modyfikowanie rysunków DWG. Ten samouczek zawiera przejrzysty przewodnik krok po kroku dotyczący dodawania tekstu do plików DWG, pokazując prostotę i możliwości Aspose.CAD.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?

Odpowiedź 1: Aspose.CAD obsługuje różne wersje plików DWG, zapewniając kompatybilność z szeroką gamą oprogramowania CAD.

### P2: Czy mogę dostosować czcionkę i formatowanie dodanego tekstu?

O2: Tak, możesz dostosować czcionkę, styl i inne opcje formatowania tekstu dodawanego do plików DWG za pomocą Aspose.CAD.

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla Java?

 Odpowiedź 3: Tak, możesz poznać funkcje Aspose.CAD, uzyskując bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla Java?

 Odpowiedź 4: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/cad/java/) szczegółowe informacje i przykłady.

### P5: Jak mogę uzyskać wsparcie lub szukać pomocy związanej z Aspose.CAD?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) aby uzyskać pomoc i nawiązać kontakt ze społecznością.