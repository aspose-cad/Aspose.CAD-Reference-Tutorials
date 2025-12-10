---
date: 2025-12-10
description: Dowiedz się, jak konwertować CAD na PDF przy użyciu Aspose.CAD dla Javy,
  ustawiając rozmiar płótna, automatyczne skalowanie układu i eksportując do TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Konwertuj CAD na PDF – Ustaw rozmiar i tryb płótna (Java)
url: /pl/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw Rozmiar Płótna i Tryb

## Wprowadzenie

Czy chcesz **convert CAD to PDF** mając pełną kontrolę nad rozmiarem płótna i trybem renderowania? Ten kompleksowy przewodnik poprowadzi Cię krok po kroku przez ustawienie rozmiaru płótna w Javie, włączenie automatycznego skalowania układu, a następnie eksport wyniku do formatów PDF i TIFF przy użyciu Aspose.CAD. Niezależnie od tego, czy udoskonalasz pipeline produkcyjny, czy eksperymentujesz z prototypem, znajdziesz tutaj jasne, praktyczne instrukcje.

## Szybkie Odpowiedzi
- **What does “convert CAD to PDF” mean?** Transformowanie rysunku CAD (np. DXF, DWG) w dokument PDF, który może być wyświetlany na dowolnej platformie.  
- **Can I also export to TIFF?** Tak — użyj `TiffOptions`, aby utworzyć obrazy rastrowe o wysokiej rozdzielczości.  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **What is automatic layout scaling?** Flaga (`setAutomaticLayoutsScaling(true)`), która zachowuje oryginalne proporcje układu przy zmianie rozmiaru płótna.  
- **Do I need a license for Aspose.CAD?** Wymagana jest tymczasowa lub stała licencja do użytku produkcyjnego.

## Co to jest **convert CAD to PDF**?

Konwersja CAD do PDF oznacza przekształcenie wektorowych rysunków inżynierskich w strony PDF, zachowując linie, warstwy i geometrie, jednocześnie udostępniając plik w formacie uniwersalnym.

## Dlaczego ustawiać rozmiar płótna **java**?

Ustawienie rozmiaru płótna w Javie pozwala określić rozdzielczość wyjściową i wymiary strony, zapewniając, że wynikowy PDF lub TIFF spełnia wymagania drukowania lub wyświetlania. Daje także kontrolę nad zachowaniem skalowania, co jest kluczowe przy dużych rysunkach.

## Wymagania wstępne

Przed przystąpieniem do samouczka upewnij się, że spełniasz następujące wymagania:

- Aspose.CAD for Java: Upewnij się, że biblioteka Aspose.CAD jest zainstalowana w Twoim środowisku Java. Możesz ją pobrać [tutaj](https://releases.aspose.com/cad/java/).

- Document Directory: Skonfiguruj katalog dokumentów do przechowywania plików CAD. Ten katalog będzie odwoływany w kolejnych krokach samouczka.

Teraz przejdźmy do przewodnika krok po kroku.

## Importowanie Przestrzeni Nazw

W tym kroku zaimportujemy niezbędne przestrzenie nazw, aby rozpocząć projekt Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Importowanie Klas Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

W tym fragmencie ustawiamy ścieżkę do katalogu zasobów i wczytujemy plik DXF przy użyciu klasy `Image` z Aspose.CAD.

## Krok 2: Ustawienie Właściwości **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Tutaj tworzymy instancję `CadRasterizationOptions` i konfigurujemy właściwości takie jak szerokość strony, wysokość strony oraz **automatic layout scaling**. To jest sedno **configure canvas mode** dla Twojej konwersji.

## Krok 3: Utworzenie PdfOptions i Ustawienie VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Teraz tworzymy instancję `PdfOptions` i ustawiamy jej właściwość `VectorRasterizationOptions` na wcześniej skonfigurowane `CadRasterizationOptions`.

## Krok 4: Eksport do PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Na koniec zapisujemy obraz CAD do pliku PDF przy użyciu określonych opcji, kończąc proces **convert CAD to PDF**.

## Krok 5: Utworzenie TiffOptions i Ustawienie VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

W tym kroku konfigurujemy instancję `TiffOptions` oraz jej właściwość `VectorRasterizationOptions`.

## Krok 6: Eksport do TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Na koniec zapisujemy obraz CAD do pliku TIFF przy użyciu określonych opcji, demonstrując, jak **export CAD to TIFF** po skonfigurowaniu rozmiaru płótna.

## Typowe Problemy i Rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|--------------|
| Wyjściowy PDF jest pusty | `setNoScaling(true)` wyłącza renderowanie niektórych rysunków | Usuń `setNoScaling(true)` lub ustaw na `false`. |
| Rozdzielczość TIFF wygląda nisko | Szerokość/ wysokość strony jest za mała | Zwiększ wartości `setPageWidth` / `setPageHeight`. |
| Układ wygląda zniekształcony | Automatyczne skalowanie układu wyłączone | Upewnij się, że `setAutomaticLayoutsScaling(true)` jest włączone. |

## Zakończenie

Gratulacje! Pomyślnie **convert CAD to PDF** i **export CAD to TIFF** przy **set canvas size java**, włączając **automatic layout scaling**, oraz nauczyłeś się **configure canvas mode** dla wysokiej jakości wyników. Ten samouczek stanowi solidną podstawę dla Twoich projektów konwersji CAD. Odkryj więcej funkcji i możliwości w [dokumentacji Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Czy mogę używać Aspose.CAD for Java z innymi frameworkami Java?

A1: Tak, Aspose.CAD jest zaprojektowany tak, aby płynnie integrować się z różnymi frameworkami Java.

### Q2: Czy dostępna jest tymczasowa licencja dla Aspose.CAD?

A2: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

### Q3: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD?

A3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia i dyskusji.

### Q4: Czy mogę wypróbować Aspose.CAD za darmo?

A4: Oczywiście! Pobierz wersję próbną [tutaj](https://releases.aspose.com/).

### Q5: Jak mogę zakupić Aspose.CAD for Java?

A5: Produkt możesz zakupić [tutaj](https://purchase.aspose.com/buy).

**Dodatkowe Pytania i Odpowiedzi**

**Q: Czy rozmiar płótna wpływa na jakość wektorową w PDF?**  
A: Nie. Rozmiar płótna kontroluje wymiary strony; dane wektorowe pozostają niezależne od rozdzielczości, zapewniając ostre renderowanie przy dowolnym poziomie powiększenia.

**Q: Czy mogę ustawić inną wartość DPI dla wyjścia TIFF?**  
A: Tak. Dostosuj `rasterizationOptions.setResolution(dpiValue)` przed utworzeniem `TiffOptions`.

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}