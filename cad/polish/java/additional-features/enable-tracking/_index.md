---
date: 2025-12-03
description: Dowiedz się, jak ustawić rozmiar strony PDF podczas konwertowania DWG
  na PDF i włączyć śledzenie w plikach DWG przy użyciu Aspose.CAD dla Javy – kompletny
  przewodnik po precyzyjnym eksportowaniu rysunków CAD do formatu PDF.
language: pl
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Ustaw rozmiar strony PDF i włącz śledzenie w plikach DWG przy użyciu Aspose.CAD
  w Javie
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw rozmiar strony PDF i włącz śledzenie w plikach DWG przy użyciu Aspose.CAD w Javie

## Introduction

Jeśli potrzebujesz **ustawić rozmiar strony PDF** podczas *konwersji DWG do PDF* i jednocześnie śledzić ewentualne problemy z renderowaniem, Aspose.CAD for Java zapewnia czysty, programowy sposób na wykonanie obu zadań. W tym samouczku przeprowadzimy Cię krok po kroku przez konfigurację wymiarów strony, włączenie śledzenia i eksport rysunku CAD do PDF — wszystko z poziomu Javy. Po zakończeniu zrozumiesz, dlaczego ustawienie prawidłowego rozmiaru strony ma znaczenie dla rysunków CAD oraz jak uzyskać szczegółowe informacje śledzenia podczas procesu eksportu.

## Quick Answers
- **Co wpływa ustawienie „rozmiaru strony PDF”?** Definiuje szerokość i wysokość wynikowego płótna PDF, zapewniając idealne dopasowanie rysunku.  
- **Czy potrzebna jest licencja do używania tej funkcji?** Wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Jaka wersja Aspose.CAD jest wymagana?** Dowolna nowsza wersja obsługująca `CadRasterizationOptions`.  
- **Czy mogę używać tego z innymi formatami CAD?** Przykład pokazuje DWG/DXF, ale to samo podejście działa dla większości obsługiwanych formatów.  
- **Jak długo trwa konwersja?** Zazwyczaj poniżej sekundy dla umiarkowanych plików; większe rysunki mogą zająć więcej czasu.

## Co oznacza „ustawienie rozmiaru strony PDF” w kontekście eksportu CAD?

Ustawienie rozmiaru strony PDF informuje renderer o dokładnych wymiarach (w pikselach lub punktach) wyjściowego płótna. Jest to szczególnie ważne w rysunkach technicznych, gdzie muszą być zachowane skala i układ. Bez wyraźnych ustawień rozmiaru strony PDF może domyślnie przyjąć rozmiar, który przycina lub zniekształca rysunek.

## Dlaczego ustawiać rozmiar strony PDF przy eksporcie rysunków CAD?

- **Zachowanie skali** – Inżynierowie polegają na wydrukach w rzeczywistej skali.  
- **Dopasowanie do papieru** – Wybierz A4, Letter lub własny rozmiar odpowiadający specyfikacjom projektu.  
- **Poprawa czytelności** – Większe strony mogą wyświetlać drobne szczegóły bez przybliżania.  
- **Spójny wynik** – Zautomatyzowane pipeline’y generują PDF-y o identycznych wymiarach przy każdym uruchomieniu.

## Jak ustawić rozmiar strony PDF przy konwersji DWG do PDF?

Poniżej skonfigurujemy `CadRasterizationOptions` z własnymi wartościami szerokości i wysokości przed eksportem. Ten krok bezpośrednio odnosi się do głównego słowa kluczowego **ustaw rozmiar strony PDF**.

## Prerequisites

- **Java Development Kit (JDK)** – Java 8 lub nowsza zainstalowana na Twoim komputerze.  
- **Aspose.CAD for Java** – Pobierz z oficjalnej [strony pobierania Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Katalog dokumentów** – Folder zawierający pliki DWG/DXF, które chcesz przetworzyć.

## Import Namespaces

Najpierw zaimportuj potrzebne klasy. Blok kodu pozostaje niezmieniony w stosunku do oryginalnego samouczka.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Step 1: Load the DWG/DXF File

Załaduj swój rysunek źródłowy. Dostosuj ścieżkę, aby wskazywała na Twój własny plik.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (including page size)

Tutaj ustawiamy szerokość i wysokość strony — to miejsce, w którym **ustawiamy rozmiar strony PDF**. Wartości podane są w pikselach; w razie potrzeby możesz przeliczyć je z cali lub milimetrów.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Wskazówka:** Jeśli wolisz standardowe rozmiary papieru, użyj przeliczenia `1 cal = 72 punkty`. Dla strony A4 (8,27 × 11,69 in), ustaw `pageWidth = 595` i `pageHeight = 842`.

## Step 3: Implement Tracking

Śledzenie przechwytuje wszelkie problemy z renderowaniem. Dołączamy własny handler, który zostanie wywołany po eksporcie.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

Teraz wykonaj konwersję. PDF zostanie utworzony z podanymi wymiarami, a wszelkie informacje śledzenia zostaną wypisane w konsoli.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

Handler wypisuje wszelkie niepowodzenia, które wystąpiły podczas renderowania. Pomaga to w debugowaniu problemów przy **eksportowaniu rysunku CAD do PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Common Issues and Solutions

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| **Pusty PDF** | Rozmiar strony ustawiony na 0 lub zbyt mały | Sprawdź, czy `setPageWidth` i `setPageHeight` mają wartości dodatnie. |
| **Brak geometrii** | Błędy renderowania przechwycone przez handler | Przejrzyj wyjście konsoli z `ErrorHandler` i napraw konkretny `RenderCode`. |
| **Plik nie znaleziony** | Nieprawidłowa ścieżka `dataDir` | Użyj ścieżki bezwzględnej lub upewnij się, że katalog istnieje. |
| **Wyjątek licencyjny** | Używanie wersji próbnej bez ważnej licencji przy dużych plikach | Zastosuj licencję Aspose.CAD przed załadowaniem obrazu. |

## Frequently Asked Questions

**P: Czy mogę włączyć śledzenie dla innych formatów plików CAD przy użyciu Aspose.CAD for Java?**  
O: Aspose.CAD głównie obsługuje DWG/DXF pod kątem śledzenia. Dla innych formatów zapoznaj się z oficjalną dokumentacją.

**P: Jak mogę obsłużyć dodatkowe opcje eksportu w Aspose.CAD for Java?**  
O: Biblioteka oferuje wiele opcji, takich jak DPI, kolor tła i rasteryzacja wektorowa. Zobacz [Dokumentację Aspose.CAD Java](https://reference.aspose.com/cad/java/) po szczegóły.

**P: Czy dostępna jest wersja próbna Aspose.CAD for Java?**  
O: Tak, możesz pobrać darmową wersję próbną z [Aspose.CAD Free Trial](https://releases.aspose.com/).

**P: Gdzie mogę uzyskać pomoc lub dyskutować o problemach związanych z Aspose.CAD for Java?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia społeczności i oficjalnych odpowiedzi.

**P: Jak uzyskać tymczasową licencję dla Aspose.CAD for Java?**  
O: Postępuj zgodnie z instrukcjami na stronie [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Ostatnia aktualizacja:** 2025-12-03  
**Testowano z:** Aspose.CAD for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}