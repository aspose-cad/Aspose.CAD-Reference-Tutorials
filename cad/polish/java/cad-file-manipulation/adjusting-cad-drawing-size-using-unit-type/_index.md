---
title: Dostosowywanie rozmiaru rysunku CAD przy użyciu typu jednostki w Aspose.CAD dla Java
linktitle: Dostosowywanie rozmiaru rysunku CAD za pomocą typu jednostki
second_title: Aspose.CAD API Java
description: Odkryj moc Aspose.CAD dla Java w łatwym dostosowywaniu rozmiarów rysunków CAD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać precyzję i możliwości dostosowania.
type: docs
weight: 14
url: /pl/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## Wstęp

stale rozwijającej się dziedzinie projektowania wspomaganego komputerowo (CAD) precyzja i zdolność adaptacji są najważniejsze. Jednym z powszechnych wymagań jest dostosowanie rozmiaru rysunków CAD w oparciu o określone typy jednostek. Aspose.CAD dla Java jawi się jako potężny sojusznik, zapewniający płynne możliwości programowego manipulowania plikami CAD.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane funkcjonalne środowisko programistyczne Java.

-  Biblioteka Aspose.CAD dla Java: Pobierz i zintegruj bibliotekę Aspose.CAD ze swoim projektem Java. Można uzyskać bibliotekę[Tutaj](https://releases.aspose.com/cad/java/).

## Importuj przestrzenie nazw

W swoim kodzie Java uwzględnij niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD. Dodaj następujący import:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Podzielmy teraz proces dostosowywania rozmiaru rysunku CAD przy użyciu typu jednostki na możliwe do wykonania kroki:

## Krok 1: Zdefiniuj katalog danych

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ustaw ścieżkę do katalogu, w którym znajdują się pliki CAD.

## Krok 2: Załaduj rysunek CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Załaduj rysunek CAD za pomocą Aspose.CAD`Image` klasa.

## Krok 3: Utwórz opcje BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Utwórz instancję`BmpOptions` klasa do eksportowania układu CAD do formatu BMP.

## Krok 4: Skonfiguruj opcje rasteryzacji

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Utwórz instancję`CadRasterizationOptions` i powiązać go z`BmpOptions` do rasteryzacji wektorowej.

## Krok 5: Ustaw typ jednostki

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Określ żądany typ jednostki dla rysunku CAD. W tym przykładzie ustawiliśmy go na Centymetr.

## Krok 6: Ustaw układy

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Zdefiniuj układy, które będą brane pod uwagę podczas eksportu. W tym przypadku wybraliśmy układ „Model”.

## Krok 7: Eksportuj do BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Na koniec zapisz zmodyfikowany rysunek CAD w formacie BMP.

## Wniosek

Dzięki Aspose.CAD dla Java dostosowywanie rozmiarów rysunków CAD staje się proste. Ten samouczek przeprowadził Cię przez cały proces, podkreślając znaczenie każdego kroku w osiąganiu precyzyjnych wyników.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi językami programowania?

O1: Aspose.CAD obsługuje przede wszystkim Javę, ale dostępne są wersje dla innych języków, np. .NET.

### P2: Czy są jakieś opcje licencjonowania dla Aspose.CAD?

 Odpowiedź 2: Tak, możesz zapoznać się z opcjami licencjonowania i kupić Aspose.CAD[Tutaj](https://purchase.aspose.com/buy).

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?

 Odpowiedź 3: Z pewnością możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.CAD dla Java?

 A4: Odwiedź forum Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19) za kompleksowe wsparcie.

### P5: Czy mogę uzyskać tymczasową licencję na Aspose.CAD?

 Odpowiedź 5: Tak, możesz nabyć licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).