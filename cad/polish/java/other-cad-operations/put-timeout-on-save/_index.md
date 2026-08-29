---
date: 2026-06-19
description: Dowiedz się, jak ustawić limit czasu przy zapisywaniu rysunków CAD przy
  użyciu Aspose.CAD dla Java. Zwiększ wydajność, unikaj zawieszeń i efektywnie eksportuj
  CAD do PDF.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Ustaw Timeout przy zapisie
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Jak ustawić limit czasu przy zapisywaniu CAD przy użyciu Aspose.CAD
url: /pl/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak ustawić limit czasu przy zapisywaniu CAD przy użyciu Aspose.CAD

## Wprowadzenie

W tym obszernym przewodniku dowiesz się **jak ustawić limit czasu** podczas zapisywania rysunków CAD przy użyciu Aspose.CAD dla Javy. Zastosowanie limitu czasu zapobiega długotrwałym operacjom zapisu, które mogą zawiesić aplikację, co jest szczególnie ważne, gdy musisz **eksportować CAD do PDF** lub **konwertować DWG do PDF** w scenariuszach przetwarzania wsadowego. Aspose.CAD dla Javy obsługuje ponad 50 formatów CAD i może obsługiwać pliki o setkach stron bez ładowania całego dokumentu do pamięci, zapewniając przewidywalną wydajność i zużycie zasobów.

## Szybkie odpowiedzi
- **Co robi limit czasu?** Przerywa operację zapisu po określonym czasie, zwalniając wątek i zapobiegając wyciekom zasobów.  
- **Która klasa kontroluje limit czasu?** `InterruptionTokenSource` dostarcza token anulowania używany przez procedurę zapisu.  
- **Czy nadal mogę eksportować CAD do PDF po upływie limitu czasu?** Tak – możesz przechwycić wyjątek przerwania i ponowić próbę lub zalogować błąd.  
- **Czy potrzebna jest specjalna licencja?** Standardowa licencja Aspose.CAD jest wystarczająca; funkcja limitu czasu jest wbudowana.  
- **Czy to podejście jest bezpieczne wątkowo?** Tak, gdy każdy zapis działa w osobnym wątku z własnym tokenem.

## Czym jest limit czasu w operacjach zapisu CAD?

Limit czasu to konfigurowalny limit czasowy, który po przekroczeniu zmusza proces zapisu do zatrzymania i zgłoszenia wyjątku przerwania. Chroni to aplikację Java przed niekończącymi się zawieszeniami spowodowanymi skomplikowanymi rysunkami lub wąskimi gardłami I/O.

## Dlaczego ustawiać limit czasu przy zapisywaniu plików CAD?

Aspose.CAD może **konwertować DWG do PDF** i **eksportować CAD do PDF** w mniej niż sekundę dla typowych rysunków, ale bardzo duże lub uszkodzone pliki mogą zajmować minuty. Definiując limit czasu, zapewniasz, że żaden pojedynczy zapis nie przekroczy, na przykład, 30 sekund, co utrzymuje stabilną wydajność przetwarzania wsadowego i zapobiega wyczerpaniu wątków.

## Wymagania wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania:
- **Aspose.CAD for Java Library** – Upewnij się, że biblioteka Aspose.CAD for Java jest zintegrowana z Twoim projektem. Bibliotekę możesz pobrać ze [strony internetowej](https://releases.aspose.com/cad/java/).
- **Środowisko programistyczne** – Skonfiguruj środowisko programistyczne Java ze wszystkimi niezbędnymi narzędziami i zależnościami.

## Importowanie pakietów

Aby rozpocząć, zaimportuj wymagane pakiety do swojego projektu Java. Dodaj następujące linie na początku pliku Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Teraz rozbijmy przykładowy kod na instrukcje krok po kroku:

## Jak ustawić limit czasu przy zapisywaniu rysunków CAD?

Wczytaj plik CAD, utwórz `InterruptionTokenSource` z żądanym limitem czasu i przekaż token do opcji zapisu PDF. Jeśli operacja przekroczy limit czasu, Aspose.CAD rzuca `OperationCanceledException`, który możesz przechwycić, aby elegancko obsłużyć błąd.

### Krok 1: Ustaw katalogi źródłowe i wyjściowe

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Upewnij się, że masz prawidłowe katalogi źródłowe i wyjściowe dla swoich rysunków CAD.

### Krok 2: Utwórz źródło tokenu przerwania

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Zainicjalizuj źródło tokenu przerwania, aby zarządzać przerwami podczas operacji zapisu.

### Krok 3: Wczytaj rysunek CAD

Klasa `CadImage` jest podstawowym obiektem Aspose.CAD, który reprezentuje rysunek CAD w pamięci, oferując metody renderowania i konwersji.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Krok 4: Skonfiguruj opcje rasteryzacji

`CadRasterizationOptions` określa, w jaki sposób rysunek CAD jest rasteryzowany do obrazu.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Skonfiguruj opcje rasteryzacji dla rysunku CAD.

### Krok 5: Skonfiguruj opcje PDF

`PdfOptions` definiuje ustawienia zapisu rysunku CAD jako dokumentu PDF.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ustaw opcje PDF z opcjami rasteryzacji wektorowej oraz tokenem przerwania.

### Krok 6: Zapisz rysunek z limitem czasu

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Zapisz rysunek CAD do pliku PDF z określonym limitem czasu.

### Krok 7: Obsłuż przerwanie

`OperationCanceledException` jest rzucany, gdy operacja zapisu przekracza określony limit czasu.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Utwórz wątek do obsługi operacji zapisu i przerwij go po określonym limicie czasu.

## Częste problemy i rozwiązania

- **Limit czasu zbyt krótki** – Jeśli otrzymujesz częste przerwania, zwiększ wartość limitu czasu, aby pomieścić większe rysunki.  
- **InterruptedException nie przechwycony** – Zawsze otaczaj wywołanie zapisu blokiem try‑catch dla `OperationCanceledException`, aby zapobiec awarii aplikacji.  
- **Zużycie pamięci** – Użyj `PdfOptions.setVectorRasterizationOptions`, aby strumieniować wyjście zamiast ładować cały plik do pamięci.

## Najczęściej zadawane pytania

**Q: Czy mogę używać tej funkcji do konwertowania DWG do PDF w zadaniu wsadowym?**  
A: Tak, opakuj każdą konwersję w osobny wątek z oddzielnym tokenem przerwania, aby wymusić limity czasowe dla każdego pliku.

**Q: Czy limit czasu działa we wszystkich formatach wyjściowych?**  
A: Mechanizm limitu czasu jest powiązany z `InterruptionTokenSource` i działa z każdym formatem, który respektuje token, w tym PDF, PNG i SVG.

**Q: Co się dzieje z częściowo zapisanymi plikami po upływie limitu czasu?**  
A: Aspose.CAD automatycznie odrzuca niekompletny wynik, więc nie otrzymasz uszkodzonych plików PDF.

**Q: Czy wymagana jest licencja do użytku produkcyjnego?**  
A: Tak, wymagana jest ważna licencja Aspose.CAD do wdrożeń komercyjnych; dostępna jest bezpłatna wersja próbna do oceny.

**Q: Gdzie mogę znaleźć więcej przykładów użycia tokenów przerwania?**  
A: Oficjalna dokumentacja Aspose.CAD zawiera dodatkowe fragmenty kodu i wytyczne najlepszych praktyk.

## Dodatkowe zasoby

- [releases page](https://releases.aspose.com/cad/java/) – Bezpośrednia strona pobierania najnowszych wydań Aspose.CAD dla Java.  
- [documentation](https://reference.aspose.com/cad/java/) – Pełna dokumentacja API i przewodniki dla deweloperów.  
- [this link](https://releases.aspose.com/) – Ogólne wydania produktów Aspose.  
- [here](https://purchase.aspose.com/temporary-license/) – Uzyskaj tymczasową licencję do testów.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Wsparcie społeczności i dyskusje.

## Zakończenie

Teraz opanowałeś **jak ustawić limit czasu** przy zapisywaniu rysunków CAD przy użyciu Aspose.CAD dla Java. Integrując `InterruptionTokenSource` w swoim przepływie pracy, możesz niezawodnie **eksportować CAD do PDF** lub **konwertować DWG do PDF** bez ryzyka długotrwałych zawieszeń, utrzymując aplikację responsywną i skalowalną.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksportuj DWG do PDF lub rastrowego przy użyciu Aspose.CAD dla Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Eksportuj określony układ DWG do PDF przy użyciu Aspose.CAD dla Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Konwertuj DWG do PNG i innych formatów rastrowych przy użyciu Aspose.CAD dla Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}