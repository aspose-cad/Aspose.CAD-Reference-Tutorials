---
date: 2026-08-29
description: Dowiedz się, jak ustawić rozmiar strony pdf i konwertować CAD na PDF
  przy użyciu Aspose.CAD dla Java, z automatycznym skalowaniem układu i eksportem
  TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Ustaw rozmiar strony pdf – konwertuj cad na pdf
og_description: Dowiedz się, jak ustawić rozmiar strony pdf podczas konwertowania
  rysunków CAD na PDF w Java przy użyciu Aspose.CAD. Ten przewodnik omawia canvas
  dimensions, automatic layout scaling i eksport do high‑resolution TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Ustaw rozmiar strony pdf – konwertuj CAD na PDF z Aspose w Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Ustaw rozmiar strony pdf – konwertuj cad na pdf (Java)
url: /pl/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw rozmiar strony PDF – konwertuj CAD do PDF (Java)

## Wprowadzenie

Jeśli potrzebujesz **ustawić rozmiar strony PDF** podczas konwertowania rysunków CAD do PDF, trafiłeś we właściwe miejsce. W tym samouczku pokażemy, jak używać Aspose.CAD for Java do określenia dokładnych wymiarów płótna, włączenia automatycznego skalowania układu, a następnie wyeksportowania wyniku zarówno do PDF, jak i TIFF. Niezależnie od tego, czy przygotowujesz schematy inżynieryjne do druku, czy generujesz miniatury do galerii internetowej, kontrola rozmiaru strony i rozdzielczości wyjściowej jest niezbędna.

## Szybkie odpowiedzi
- **Co oznacza „convert CAD to PDF”?** Przekształcenie rysunku CAD (np. DXF, DWG) w dokument PDF, który może być wyświetlany na dowolnej platformie.  
- **Czy mogę również eksportować do TIFF?** Tak — użyj `TiffOptions`, aby tworzyć obrazy rastrowe o wysokiej rozdzielczości.  
- **Która opcja kontroluje rozmiar płótna w Javie?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Czym jest automatyczne skalowanie układu?** Flaga (`setAutomaticLayoutsScaling(true)`), która zachowuje oryginalne proporcje układu, gdy zmienia się rozmiar płótna.  
- **Czy potrzebna jest licencja na Aspose.CAD?** Do użytku produkcyjnego wymagana jest tymczasowa lub stała licencja.

## Jak ustawić rozmiar strony PDF podczas konwertowania CAD do PDF w Javie

Wczytaj plik CAD, skonfiguruj `CadRasterizationOptions` z żądaną szerokością i wysokością, włącz automatyczne skalowanie układu, a następnie zapisz wynik jako PDF. To dwustopniowe podejście pozwala kontrolować dokładne wymiary strony wyjściowej bez utraty jakości wektorowej.

## Co to jest konwersja CAD do PDF?

Konwersja CAD do PDF oznacza przekształcenie wektorowych rysunków inżynieryjnych w strony PDF, zachowując linie, warstwy i geometrię, jednocześnie udostępniając plik w sposób uniwersalny. Proces rasteryzuje rysunek zgodnie z określonymi opcjami, tworząc PDF, który można otworzyć na dowolnym urządzeniu bez potrzeby oprogramowania CAD, i zachowuje wizualną wierność oryginalnego projektu.

## Dlaczego ustawiać rozmiar płótna w Javie?

Ustawienie rozmiaru płótna w Javie pozwala określić rozdzielczość wyjściową i wymiary strony, zapewniając, że powstały PDF lub TIFF spełnia wymagania drukowania lub wyświetlania. Daje także kontrolę nad zachowaniem skalowania, co jest niezbędne przy rysunkach w dużym formacie.

## Wymagania wstępne

Zanim zanurzysz się w samouczek, upewnij się, że spełniasz następujące wymagania:

- Aspose.CAD for Java: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD w swoim środowisku Java. Bibliotekę Aspose.CAD for Java możesz pobrać [tutaj](https://releases.aspose.com/cad/java/).
- Katalog dokumentów: Utwórz katalog, w którym będą przechowywane pliki CAD. Ten katalog będzie używany w kolejnych krokach samouczka.

Teraz rozpocznijmy przewodnik krok po kroku.

## Importowanie przestrzeni nazw

W tym kroku zaimportujemy niezbędne przestrzenie nazw, aby rozpocząć projekt Aspose.CAD.  
`Image` jest główną klasą używaną do wczytywania plików CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: importowanie klas Aspose.CAD

Klasa `Image` udostępnia metody do wczytywania i zapisywania rysunków CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

W tym fragmencie ustawiamy ścieżkę do katalogu zasobów i wczytujemy plik DXF przy użyciu klasy `Image` z Aspose.CAD.

## Krok 2: ustawienie właściwości CadRasterizationOptions (ustaw rozmiar płótna w Javie)

`CadRasterizationOptions` określa ustawienia rasteryzacji, takie jak rozmiar strony i skalowanie, dla konwersji CAD‑do‑raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Tutaj tworzymy instancję `CadRasterizationOptions` i konfigurujemy właściwości takie jak szerokość strony, wysokość strony oraz **automatyczne skalowanie układu**. To jest sedno **konfigurowania trybu płótna** dla twojej konwersji.

## Krok 3: utworzenie PdfOptions i ustawienie vectorRasterizationOptions

`PdfOptions` definiuje ustawienia wyjściowe PDF dla konwersji.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Teraz tworzymy instancję `PdfOptions` i ustawiamy jej właściwość `VectorRasterizationOptions` na wcześniej skonfigurowane `CadRasterizationOptions`.

## Krok 4: eksport do PDF (konwersja CAD do PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Na koniec zapisujemy obraz CAD do pliku PDF przy użyciu określonych opcji, kończąc proces **konwersji CAD do PDF**.

## Krok 5: utworzenie TiffOptions i ustawienie vectorRasterizationOptions (eksport CAD do TIFF)

`TiffOptions` konfiguruje parametry wyjściowe TIFF, takie jak kompresja i rozdzielczość.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

W tym kroku tworzymy instancję `TiffOptions` i konfigurujemy jej właściwość `VectorRasterizationOptions`.

## Krok 6: eksport do TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Na koniec zapisujemy obraz CAD do pliku TIFF przy użyciu określonych opcji, demonstrując, jak **eksportować CAD do TIFF** po skonfigurowaniu rozmiaru płótna.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| PDF jest pusty | `setNoScaling(true)` wyłącza renderowanie niektórych rysunków | Usuń `setNoScaling(true)` lub ustaw na `false`. |
| Rozdzielczość TIFF jest niska | Szerokość/wysokość strony zbyt mała | Zwiększ wartości `setPageWidth` / `setPageHeight`. |
| Układ wygląda zniekształcony | Automatyczne skalowanie układu wyłączone | Upewnij się, że `setAutomaticLayoutsScaling(true)` jest włączone. |

## Dlaczego dostosować rozmiar płótna i DPI?

Zmiana rozmiaru płótna bezpośrednio wpływa na rozdzielczość rasteryzacji wyjścia. Jeśli potrzebujesz **zwiększyć rozdzielczość TIFF**, po prostu podnieś wartości `setPageWidth` / `setPageHeight` lub wywołaj `rasterizationOptions.setResolution(300)` przed utworzeniem `TiffOptions`. Dzięki temu otrzymasz obrazy rastrowe wysokiej jakości, odpowiednie do druku lub szczegółowej inspekcji.

## Najczęściej zadawane pytania

**Q1: czy mogę używać Aspose.CAD for Java z innymi frameworkami Java?**  
A: Tak, Aspose.CAD jest zaprojektowany tak, aby bezproblemowo integrować się z różnymi frameworkami Java.

**Q2: czy dostępna jest tymczasowa licencja dla Aspose.CAD?**  
A: Tak, tymczasową licencję można uzyskać na stronie [tutaj](https://purchase.aspose.com/temporary-license/).

**Q3: gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD?**  
A: Odwiedź forum Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia i dyskusji.

**Q4: czy mogę wypróbować Aspose.CAD za darmo?**  
A: Oczywiście! Pobierz wersję próbną [tutaj](https://releases.aspose.com/).

**Q5: jak mogę kupić Aspose.CAD for Java?**  
A: Zakup Aspose.CAD for Java [tutaj](https://purchase.aspose.com/buy).

**Q: czy rozmiar płótna wpływa na jakość wektorową w PDF?**  
A: Nie. Rozmiar płótna kontroluje wymiary strony; dane wektorowe pozostają niezależne od rozdzielczości, zapewniając wyraźne renderowanie przy dowolnym poziomie powiększenia.

**Q: czy mogę ustawić inną wartość DPI dla wyjścia TIFF?**  
A: Tak. Dostosuj `rasterizationOptions.setResolution(dpiValue)` przed utworzeniem `TiffOptions`.

**Q: jak mogę zmienić wymiary PDF istniejącego pliku PDF bez ponownego renderowania CAD?**  
A: Użyj Aspose.PDF, aby wczytać wygenerowany PDF i wywołać `pdf.getPages().setPageSize(PageSize.A4)` lub niestandardowy rozmiar.

**Q: jaka jest najlepsza metoda konwersji dxf do pdf przy zachowaniu warstw?**  
A: Zachowaj `setAutomaticLayoutsScaling(true)` i unikaj `setNoScaling(true)`; to utrzymuje widoczność warstw i wierność układu.

## Zakończenie

Gratulacje! Pomyślnie **przekonwertowałeś CAD do PDF** i **wyeksportowałeś CAD do TIFF**, jednocześnie **ustawiając rozmiar płótna w Javie**, włączając **automatyczne skalowanie układu** oraz ucząc się, jak **konfigurować tryb płótna** dla wysokiej jakości wyników. Ten samouczek zapewnia solidną podstawę dla twoich projektów konwersji CAD. Odkryj więcej funkcji i możliwości w [dokumentacji Aspose.CAD](https://reference.aspose.com/cad/java/).

**Ostatnia aktualizacja:** 2026-08-29  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose

## Powiązane samouczki

- [Ustaw rozmiar płótna – Zaawansowane funkcje CAD z Aspose.CAD for Java](/cad/java/advanced-cad-features/)
- [Eksport DWG do PDF w Javie – Ustaw rozmiar strony PDF z Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Ustaw niestandardowy rozmiar strony – PDF z CAD z automatycznym skalowaniem układu](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}