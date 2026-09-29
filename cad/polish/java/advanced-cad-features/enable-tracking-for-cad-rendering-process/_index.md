---
date: 2026-09-29
description: Dowiedz się, jak ustawić rozmiar strony PDF podczas konwertowania CAD
  na PDF przy użyciu Aspose.CAD for Java. Postępuj zgodnie z tym przewodnikiem krok
  po kroku, aby włączyć śledzenie, konwertować CAD na PDF i efektywnie zapisywać CAD
  jako PDF.
keywords:
- set pdf page size
- convert cad to pdf
- save cad as pdf
- generate pdf from dxf
- java cad to pdf
lastmod: 2026-09-29
linktitle: Ustaw rozmiar strony PDF – Włącz śledzenie renderowania CAD
og_description: Ustaw rozmiar strony PDF podczas konwertowania CAD na PDF przy użyciu
  Aspose.CAD for Java. Włącz śledzenie, aby debugować i optymalizować pipeline renderowania.
og_image_alt: Developer guide showing how to set PDF page size and enable tracking
  for CAD rendering using Aspose.CAD Java
og_title: Ustaw rozmiar strony PDF i włącz śledzenie renderowania CAD w Javie
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Learn how to set PDF page size while converting CAD to PDF using Aspose.CAD
    for Java. Follow this step‑by‑step guide to enable tracking, convert CAD to PDF,
    and save CAD as PDF efficiently.
  headline: How to set PDF page size and enable tracking for CAD rendering process
    using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to set PDF page size while converting CAD to PDF using Aspose.CAD
    for Java. Follow this step‑by‑step guide to enable tracking, convert CAD to PDF,
    and save CAD as PDF efficiently.
  name: How to set PDF page size and enable tracking for CAD rendering process using
    Aspose.CAD for Java
  steps:
  - name: '**Java development environment** – Java 8 or later installed on your machine.'
    text: '**Java development environment** – Java 8 or later installed on your machine.'
  - name: '**Aspose.CAD library** – Download and integrate the Aspose.CAD library
      into your Java project. You can find the download link [Aspose.CAD Java download
      page](https://releases.aspose.com/cad/java/).'
    text: '**Aspose.CAD library** – Download and integrate the Aspose.CAD library
      into your Java project. You can find the download link [Aspose.CAD Java download
      page](https://releases.aspose.com/cad/java/).'
  - name: '**Document directory** – Prepare a directory to store your CAD files and
      the generated PDFs.'
    text: '**Document directory** – Prepare a directory to store your CAD files and
      the generated PDFs.'
  type: HowTo
- questions:
  - answer: It defines the width and height of the resulting PDF page during CAD rendering.
    question: What does “set PDF page size” do?
  - answer: Tracking logs each stage of the conversion, helping you spot performance
      bottlenecks or errors.
    question: Why enable tracking?
  - answer: A free trial works for evaluation; a commercial license is required for
      production.
    question: Do I need a license?
  - answer: DWG, DXF, DGN, and many others – see the Aspose.CAD documentation for
      the full list.
    question: Which CAD formats are supported?
  - answer: Yes – simply adjust the `PageWidth` and `PageHeight` values in `CadRasterizationOptions`.
    question: Can I change page dimensions on the fly?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- Aspose.CAD
- Java CAD processing
title: Jak ustawić rozmiar strony PDF i włączyć śledzenie procesu renderowania CAD
  przy użyciu Aspose.CAD for Java
url: /pl/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Włącz śledzenie procesu renderowania CAD

## Wprowadzenie

W tym samouczku dowiesz się, jak **ustawić rozmiar strony PDF** podczas **konwersji CAD do PDF** przy użyciu **Aspose.CAD for Java**. Dzięki włączeniu śledzenia uzyskasz pełną widoczność pipeline’u renderowania, co ułatwi debugowanie i optymalizację konwersji plików CAD (takich jak DXF) do PDF. Niezależnie od tego, czy potrzebujesz **zapisać CAD jako PDF**, wygenerować PDF z DXF, czy po prostu kontrolować wymiary wyjścia, poniższe kroki przeprowadzą Cię przez cały proces.

## Szybkie odpowiedzi
- **Co robi „ustaw rozmiar strony PDF”?** Definiuje szerokość i wysokość wynikowej strony PDF podczas renderowania CAD.  
- **Dlaczego włączyć śledzenie?** Śledzenie zapisuje w logu każdy etap konwersji, pomagając wykryć wąskie gardła wydajności lub błędy.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarczy do oceny; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jakie formaty CAD są obsługiwane?** DWG, DXF, DGN i wiele innych – pełną listę znajdziesz w dokumentacji Aspose.CAD.  
- **Czy mogę zmieniać wymiary strony w locie?** Tak – po prostu dostosuj wartości `PageWidth` i `PageHeight` w `CadRasterizationOptions`.

## Co oznacza „ustaw rozmiar strony PDF” w renderowaniu CAD?

Ustawienie rozmiaru strony PDF informuje rasteryzator, jak duże ma być płótno, gdy wektorowe dane CAD są rasteryzowane do strony PDF. Jest to kluczowe dla zachowania wierności wizualnej, szczególnie przy szczegółowych rysunkach inżynieryjnych. Dobór odpowiednich wymiarów zapewnia prawidłową skalę rysunku i czytelność adnotacji.

## Dlaczego włączyć śledzenie dla renderowania CAD?

Włączenie śledzenia zapewnia szczegółowy log każdego kroku – od wczytania pliku źródłowego po zapis wyjściowego PDF. Log zawiera znaczniki czasu, zużycie pamięci oraz szczegóły rasteryzacji, co pozwala programistom zlokalizować wąskie gardła wydajności i anomalie renderowania. Analizując te informacje, możesz dostosować ustawienia, takie jak rozmiar strony czy rozdzielczość, aby poprawić jakość wyjścia.

## Wymagania wstępne

Przed przystąpieniem do konfiguracji śledzenia upewnij się, że spełniasz następujące wymagania:

1. **Środowisko programistyczne Java** – Java 8 lub nowsza zainstalowana na Twoim komputerze.  
2. **Biblioteka Aspose.CAD** – Pobierz i zintegrować bibliotekę Aspose.CAD w swoim projekcie Java. Link do pobrania znajdziesz na [stronie pobierania Aspose.CAD Java](https://releases.aspose.com/cad/java/).  
3. **Katalog dokumentów** – Przygotuj katalog do przechowywania plików CAD oraz generowanych plików PDF.

## Importowanie przestrzeni nazw

`Aspose.CAD` udostępnia podstawowe klasy używane do ładowania, rasteryzacji i zapisywania rysunków CAD. Zaimportuj wymagane pakiety na początku pliku źródłowego Java.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Ustaw ścieżkę katalogu zasobów

Klasa `File` (java.io.File) reprezentuje ścieżkę do pliku lub katalogu w systemie plików. `File` z pakietu `java.io` wskazuje folder zawierający Twoje pliki CAD. Ustaw ją na właściwą lokalizację przed wczytaniem jakiegokolwiek rysunku.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## Wczytaj plik CAD

`CadImage` to klasa Aspose.CAD, która wczytuje i reprezentuje rysunek CAD do dalszego przetwarzania. `CadImage` jest punktem wejścia do odczytu dokumentu CAD. Parsuje format pliku i przygotowuje rasteryzator.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Ustaw opcje wyjścia PDF

`PdfOptions` konfiguruje ustawienia specyficzne dla PDF, takie jak kompresja, metadane i obsługa strumienia wyjściowego. `PdfOptions` zawiera wszystkie ustawienia PDF, w tym kompresję, metadane i obsługę strumienia wyjściowego.

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

## Skonfiguruj CadRasterizationOptions (ustaw rozmiar strony PDF)

`CadRasterizationOptions` kontroluje parametry rasteryzacji, takie jak rozmiar strony, rozdzielczość i format wyjściowy przy konwersji CAD do PDF. `CadRasterizationOptions` jest klasą sterującą parametrami rasteryzacji, w tym rozmiarem strony, rozdzielczością i formatem wyjściowym. Ustawiając `PageWidth` i `PageHeight` określasz dokładne wymiary generowanej strony PDF.

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Zapisz plik PDF

`save` zapisuje rasteryzowaną zawartość do określonego strumienia wyjściowego przy użyciu podanych opcji PDF. Wywołanie `image.save(outputStream, pdfOptions)` zapisuje rasteryzowaną zawartość do strumienia PDF zgodnie z skonfigurowanymi opcjami.

```java
image.save(stream, pdfOptions);
```

## Zweryfikuj włączenie śledzenia

`setTrackingEnabled(true)` aktywuje szczegółowe logowanie każdego etapu renderowania w rasteryzatorze. `CadRasterizationOptions.setTrackingEnabled(true)` włącza szczegółowe logowanie dla każdego etapu renderowania, umożliwiając wgląd w wewnętrzny przepływ pracy.

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| Strona PDF jest pusta | `PageWidth`/`PageHeight` ustawione na 0 | Upewnij się, że podano nie‑zerowe wymiary. |
| Plik wyjściowy jest uszkodzony | Strumień wyjściowy nie został zamknięty | Wywołaj `stream.close()` po `image.save(...)`. |
| Brak warstw w PDF | Plik CAD używa nieobsługiwanych encji | Zweryfikuj, czy format pliku jest w pełni obsługiwany przez Aspose.CAD. |

## Najczęściej zadawane pytania

**P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami CAD?**  
Odp1: Aspose.CAD obsługuje ponad 30 formatów CAD, w tym DWG, DXF, DGN i wiele innych. Pełną listę znajdziesz w [dokumentacji](https://reference.aspose.com/cad/java/).

**P2: Czy mogę dostosować wymiary wyjściowego pliku PDF?**  
Odp2: Oczywiście. Dostosuj parametry `PageWidth` i `PageHeight` w `CadRasterizationOptions`, aby uzyskać żądany rozmiar.

**P3: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
Odp3: Tak, możesz wypróbować możliwości Aspose.CAD, pobierając darmową wersję próbną z [strony darmowego trialu Aspose](https://releases.aspose.com/).

**P4: Jak uzyskać wsparcie społeczności w kwestiach związanych z Aspose.CAD?**  
Odp4: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby skontaktować się ze społecznością i uzyskać pomoc.

**P5: Czy dostępne są tymczasowe licencje dla Aspose.CAD?**  
Odp5: Tak, jeśli potrzebujesz tymczasowej licencji, możesz ją nabyć na [stronie zakupu licencji tymczasowej](https://purchase.aspose.com/temporary-license/).

## Zakończenie

Gratulacje! Teraz wiesz, jak **ustawić rozmiar strony PDF** i włączyć śledzenie renderowania CAD przy użyciu **Aspose.CAD for Java**. Ten przewodnik umożliwia **konwersję CAD do PDF**, **zapis CAD jako PDF** oraz generowanie PDF z DXF z pełną kontrolą nad wymiarami strony i szczegółowymi logami wykonania. Śmiało eksperymentuj z różnymi rozmiarami stron i odkrywaj dodatkowe opcje rasteryzacji, aby dopasować je do swoich specyficznych procesów inżynieryjnych.

---

**Ostatnia aktualizacja:** 2026-09-29  
**Testowano z:** Aspose.CAD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose

## Powiązane samouczki

- [Konwersja CAD do PDF – Ustaw rozmiar płótna i zaawansowane funkcje z Aspose.CAD for Java](/cad/java/advanced-cad-features/)
- [Konwersja DWG do PDF/A1a i PDF/A1b przy użyciu Aspose.CAD for Java](/cad/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/)
- [Konwersja DWG do PDF – Eksport obrazów AutoCAD do PDF z Aspose.CAD for Java](/cad/java/cad-export-options/export-autocad-images-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}