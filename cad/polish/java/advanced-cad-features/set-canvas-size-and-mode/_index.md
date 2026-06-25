---
date: 2026-02-15
description: Dowiedz się, jak ustawić rozmiar strony PDF i konwertować CAD na PDF
  przy użyciu Aspose.CAD dla Javy, z automatycznym skalowaniem układu i eksportem
  do formatu TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Ustaw rozmiar strony PDF – konwertuj CAD do PDF (Java)
url: /pl/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw Rozmiar Płótna i Tryb

## Wprowadzenie

Jeśli potrzebujesz **ustawić rozmiar strony PDF** podczas konwertowania rysunków CAD do PDF, trafiłeś we właściwe miejsce. W tym samouczku pokażemy, jak używać Aspose.CAD for Java, aby określić dokładne wymiary płótna, włączyć automatyczne skalowanie układu, a następnie wyeksportować wynik zarówno do PDF, jak i TIFF. Niezależnie od tego, czy przygotowujesz schematy inżynieryjne do druku, czy generujesz miniatury do galerii internetowej, kontrola rozmiaru strony i rozdzielczości wyjściowej jest niezbędna.

## Szybkie odpowiedzi
- **Co oznacza „convert CAD to PDF”?** Transformację rysunku CAD (np. DXF, DWG) w dokument PDF, który może być wyświetlany na dowolnej platformie.  
- **Czy mogę także eksportować do TIFF?** Tak — użyj `TiffOptions`, aby tworzyć obrazy rastrowe o wysokiej rozdzielczości.  
- **Która opcja kontroluje rozmiar płótna w Javie?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Czym jest automatyczne skalowanie układu?** Flaga (`setAutomaticLayoutsScaling(true)`), która zachowuje pierwotne proporcje układu przy zmianie rozmiaru płótna.  
- **Czy potrzebna jest licencja na Aspose.CAD?** Wymagana jest tymczasowa lub stała licencja do użytku produkcyjnego.

## Jak ustawić rozmiar strony PDF przy konwertowaniu CAD do PDF (Java)

Ustawienie rozmiaru strony PDF (lub płótna) pozwala określić ostateczne wymiary dokumentu, co jest szczególnie przydatne, gdy musisz **zmienić wymiary PDF**, aby dopasować je do standardów drukowania lub wymagań interfejsu użytkownika. Poniżej przeprowadzimy Cię przez każdy krok, wyjaśniając *dlaczego* za każdą linią kodu.

## Co to jest **convert CAD to PDF**?

Konwersja CAD do PDF oznacza pobranie wektorowych rysunków inżynieryjnych i renderowanie ich jako stron PDF, zachowując linie, warstwy i geometrię, a jednocześnie czyniąc plik powszechnie dostępnym.

## Dlaczego ustawiać rozmiar płótna **java**?

Ustawienie rozmiaru płótna w Javie pozwala określić rozdzielczość wyjściową i wymiary strony, zapewniając, że powstały PDF lub TIFF spełni Twoje wymagania dotyczące druku lub wyświetlania. Daje także kontrolę nad zachowaniem skalowania, co jest kluczowe przy rysunkach wielkoformatowych.

## Wymagania wstępne

Zanim przejdziesz do samych instrukcji, upewnij się, że spełniasz następujące wymagania:

- Aspose.CAD for Java: Upewnij się, że biblioteka Aspose.CAD jest zainstalowana w Twoim środowisku Java. Możesz ją pobrać [tutaj](https://releases.aspose.com/cad/java/).
- Katalog dokumentów: Utwórz katalog, w którym będą przechowywane pliki CAD. Ten katalog będzie odwoływany w kolejnych krokach samouczka.

Teraz przejdźmy do przewodnika krok po kroku.

## Importowanie przestrzeni nazw

W tym kroku zaimportujemy niezbędne przestrzenie nazw, aby rozpocząć projekt Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Importowanie klas Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

W tym fragmencie ustawiamy ścieżkę do katalogu zasobów i wczytujemy plik DXF za pomocą klasy `Image` z Aspose.CAD.

## Krok 2: Ustawienie właściwości **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Tutaj tworzymy instancję `CadRasterizationOptions` i konfigurujemy właściwości takie jak szerokość strony, wysokość strony oraz **automatyczne skalowanie układu**. To jest sedno **konfiguracji trybu płótna** dla Twojej konwersji.

## Krok 3: Utworzenie PdfOptions i ustawienie VectorRasterizationOptions

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

## Krok 5: Utworzenie TiffOptions i ustawienie VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

W tym kroku tworzymy instancję `TiffOptions` i konfigurujemy jej właściwość `VectorRasterizationOptions`.

## Krok 6: Eksport do TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Na koniec zapisujemy obraz CAD do pliku TIFF przy użyciu określonych opcji, demonstrując, jak **export CAD to TIFF** po skonfigurowaniu rozmiaru płótna.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| PDF wyjściowy jest pusty | `setNoScaling(true)` wyłącza renderowanie niektórych rysunków | Usuń `setNoScaling(true)` lub ustaw na `false`. |
| Rozdzielczość TIFF wydaje się niska | Zbyt mała szerokość/wysokość strony | Zwiększ wartości `setPageWidth` / `setPageHeight`. |
| Układ jest zniekształcony | Automatyczne skalowanie układu wyłączone | Upewnij się, że `setAutomaticLayoutsScaling(true)` jest włączone. |

## Dlaczego warto dostosować rozmiar płótna i DPI?

Zmiana rozmiaru płótna bezpośrednio wpływa na rozdzielczość rasteryzacji wyjścia. Jeśli potrzebujesz **zwiększyć rozdzielczość TIFF**, po prostu podnieś wartości `setPageWidth` / `setPageHeight` lub wywołaj `rasterizationOptions.setResolution(300)` przed utworzeniem `TiffOptions`. Dzięki temu uzyskasz obrazy rastrowe wysokiej jakości, odpowiednie do druku lub szczegółowej inspekcji.

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.CAD for Java z innymi frameworkami Java?

A1: Tak, Aspose.CAD został zaprojektowany tak, aby bezproblemowo integrować się z różnymi frameworkami Java.

### Q2: Czy dostępna jest tymczasowa licencja na Aspose.CAD?

A2: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

### Q3: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD?

A3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie społeczności i dyskusje.

### Q4: Czy mogę wypróbować Aspose.CAD za darmo?

A4: Oczywiście! Pobierz darmową wersję próbną [tutaj](https://releases.aspose.com/).

### Q5: Jak mogę kupić Aspose.CAD for Java?

A5: Produkt można zakupić [tutaj](https://purchase.aspose.com/buy).

**Dodatkowe Q&A**

**Q: Czy rozmiar płótna wpływa na jakość wektorową w PDF?**  
A: Nie. Rozmiar płótna kontroluje wymiary strony; dane wektorowe pozostają niezależne od rozdzielczości, zapewniając ostre renderowanie przy dowolnym poziomie powiększenia.

**Q: Czy mogę ustawić inną wartość DPI dla wyjścia TIFF?**  
A: Tak. Dostosuj `rasterizationOptions.setResolution(dpiValue)` przed utworzeniem `TiffOptions`.

**Q: Jak mogę **change PDF dimensions** istniejącego PDF bez ponownego renderowania CAD?**  
A: Użyj Aspose.PDF, aby załadować wygenerowany PDF i wywołać `pdf.getPages().setPageSize(PageSize.A4)` lub rozmiar niestandardowy.

**Q: Jaki jest najlepszy sposób na **convert dxf to pdf** przy zachowaniu warstw?**  
A: Zachowaj `setAutomaticLayoutsScaling(true)` i unikaj `setNoScaling(true)`; to utrzyma widoczność warstw i wierność układu.

## Zakończenie

Gratulacje! Pomyślnie **convert CAD to PDF** i **export CAD to TIFF**, jednocześnie **set canvas size java**, włączając **automatic layout scaling**, oraz ucząc się **configure canvas mode** dla wysokiej jakości wyników. Ten samouczek zapewnia solidne podstawy dla Twoich projektów konwersji CAD. Odkryj więcej funkcji i możliwości w [dokumentacji Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Ostatnia aktualizacja:** 2026-02-15  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}