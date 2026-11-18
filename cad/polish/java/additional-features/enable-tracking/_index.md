---
date: 2026-11-18
description: Dowiedz się, jak eksportować DWG do PDF, włączać śledzenie i używać własnej
  klasy obsługi błędów w Javie z Aspose.CAD for Java. Zawiera konwersję DXF‑to‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: Włącz śledzenie w plikach DWG przy użyciu Java
og_description: Eksportuj DWG do PDF i włącz pełne śledzenie w Java z Aspose.CAD.
  Dowiedz się, jak używać własnej klasy obsługi błędów, konwertować DXF do PDF i rejestrować
  ostrzeżenia renderowania.
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: Eksportuj DWG do PDF ze śledzeniem przy użyciu Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-11-18'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: Eksportuj DWG do PDF i włącz śledzenie z Aspose.CAD Java
url: /pl/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport DWG do PDF i włączenie śledzenia przy użyciu Aspose.CAD Java

## Wprowadzenie

Eksportowanie DWG do PDF przy zachowaniu pełnej przejrzystości procesu konwersji jest niezbędne dla nowoczesnych zespołów skoncentrowanych na CAD. W tym przewodniku odkryjesz **jak włączyć śledzenie** w przepływach pracy DWG, konwertować DXF do PDF w tym samym potoku oraz przechwytywać każde ostrzeżenie renderowania za pomocą **niestandardowej klasy obsługi błędów Java**. Po zakończeniu będziesz miał gotowy fragment kodu produkcyjnego, który nie tylko generuje wysokiej jakości PDF‑y, ale także rejestruje informacje diagnostyczne do audytu i rozwiązywania problemów.

## Szybkie odpowiedzi
- **Co robi „enable dwg tracking java”?** Aktywuje wywołania zwrotne renderowania Aspose.CAD, dzięki czemu możesz zobaczyć ostrzeżenia i błędy podczas eksportu.  
- **Czy potrzebuję licencji?** Wersja próbna działa do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę także konwertować DXF do PDF?** Tak – ten sam obiekt `PdfOptions` używany dla DWG działa dla DXF, obejmując scenariusz *java convert dxf pdf*.  
- **Jakiej wersji JDK wymagana jest?** Java 8 lub nowsza.  
- **Gdzie mogę znaleźć więcej przykładów?** Zobacz [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) poniżej.

## Co to jest eksport dwg do pdf?

Eksport DWG do PDF to proces konwertowania natywnego rysunku AutoCAD (DWG) do przenośnego dokumentu PDF przy zachowaniu dokładności wektorowej, warstw i adnotacji. **Aspose.CAD konwertuje DWG do PDF w czystej Javie, więc nigdy nie potrzebujesz licencjonowanej instalacji AutoCAD.** Ta konwersja zachowuje dokładne grubości linii, style tekstu i geometrię układu, co sprawia, że PDF jest odpowiedni do przeglądu przez klienta, archiwizacji lub dalszego przetwarzania.

## Dlaczego używać Aspose.CAD dla Java?

Aspose.CAD dla Java zapewnia kompleksowe, czysto‑Java rozwiązanie do konwersji CAD, obsługujące ponad 50 formatów, oferujące wysoką wydajność i wbudowane śledzenie poprzez wywołania zwrotne renderowania. Nie wymaga żadnych zewnętrznych zależności i może być zintegrowany z potokami po stronie serwera. Biblioteka zawiera także przetwarzanie oszczędzające pamięć, umożliwiając konwersję plików do 500 stron bez ładowania całego dokumentu do RAM.

## Wymagania wstępne

- **Java Development Kit (JDK)** 8 lub nowszy zainstalowany na twoim komputerze.  
- **Aspose.CAD for Java** pobrany z oficjalnego [download link](https://releases.aspose.com/cad/java/).  
- **Aspose.CAD Free Trial** można uzyskać ze strony [Aspose.CAD Free Trial](https://releases.aspose.com/) jeśli potrzebujesz szybkiej oceny.  
- Folder zawierający pliki DWG/DXF, które chcesz skonwertować.  

## Jak wyeksportować DWG do PDF?

Wczytaj swój plik źródłowy, skonfiguruj `PdfOptions`, podłącz niestandardowy `CadRenderHandler` i wywołaj `save`. Ten przepływ end‑to‑end konwertuje DWG (lub DXF) do PDF, jednocześnie emitując informacje śledzenia dla każdego kroku renderowania, zapewniając, że wszystkie ostrzeżenia lub błędy są przechwytywane i mogą być obsłużone przez programistów lub procesy automatyczne.

## Importuj przestrzenie nazw

Interfejs `CadRenderHandler` otrzymuje diagnostykę renderowania, taką jak ostrzeżenia i błędy podczas konwersji.  
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

## Krok 1: wczytaj plik dwg/dxf  

`CadImage` reprezentuje rysunek CAD wczytany do pamięci i zapewnia dostęp do jego stron i warstw.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: skonfiguruj opcje eksportu pdf (jak konwertować dxf do pdf)

`PdfOptions` definiuje ustawienia wyjściowe PDF, natomiast `VectorRasterizationOptions` kontroluje parametry rasteryzacji, takie jak DPI i kolor tła.  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Krok 3: zaimplementuj śledzenie (custom error handler java)

`ErrorHandler` rozszerza `CadRenderHandler`, aby przechwytywać i logować komunikaty renderowania emitowane podczas procesu konwersji.  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: eksportuj do pdf  

Wywołanie metody `save` na instancji `CadImage` zapisuje wyrenderowany PDF do określonej ścieżki wyjściowej.  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: klasa cadrenderhandler  

`CadRenderHandler` jest bazową klasą wywołań zwrotnych, która otrzymuje `RenderResult` zawierający szczegółowe komunikaty po zakończeniu renderowania.  
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

## Dlaczego to ma znaczenie

Włączenie śledzenia tworzy ślad audytowy, który spełnia wymogi zgodności w regulowanych sektorach, takich jak architektura, inżynieria i budownictwo. Niestandardowy handler błędów pozwala także zintegrować kontrole stanu konwersji CAD z potokami CI/CD, automatycznie oznaczając pliki wymagające ręcznej weryfikacji.

## Typowe problemy i rozwiązania

- **`NullPointerException` on `RenderResult`** – Upewnij się, że używasz Aspose.CAD 23.10 lub nowszej; wcześniejsze wersje nie posiadają API `RenderResult`.  
- **File not found** – Sprawdź dwukrotnie, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku jest zgodna z wielkością liter.  
- **Missing tracking output** – Zweryfikuj, czy twoja instancja `ErrorHandler` jest poprawnie przypisana do `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Najczęściej zadawane pytania

**Q:** Czy mogę włączyć śledzenie dla innych formatów plików CAD przy użyciu Aspose.CAD dla Java?  
**A:** Śledzenie jest głównie dostępne dla DWG i DXF. Dla innych formatów zapoznaj się z oficjalną dokumentacją, aby sprawdzić, które API udostępniają wywołania zwrotne renderowania.

**Q:** Jak mogę dostosować dodatkowe opcje eksportu, takie jak ustawianie metadanych PDF?  
**A:** `PdfOptions` udostępnia właściwości takie jak `setTitle`, `setAuthor` i `setSubject`. Ustaw je przed wywołaniem `save`, aby osadzić metadane w powstałym PDF.

**Q:** Czy wersja próbna jest wystarczająca do oceny funkcji śledzenia?  
**A:** Tak, darmowa wersja próbna zawiera pełny dostęp do API, umożliwiając testowanie `CadRenderHandler` i eksportu PDF bez ograniczeń.

**Q:** Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD dla Java?  
**A:** Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby zadawać pytania i dzielić się doświadczeniami z innymi programistami.

**Q:** Jak uzyskać tymczasową licencję do środowisk testów automatycznych?  
**A:** Postępuj zgodnie z instrukcjami na stronie [Temporary License](https://purchase.aspose.com/temporary-license/), aby wygenerować licencję o ograniczonym czasie ważności.

## Podsumowanie

Postępując zgodnie z tym samouczkiem, teraz wiesz, jak **eksportować DWG do PDF**, włączyć pełne śledzenie oraz obsłużyć konwersję DXF‑do‑PDF przy użyciu **niestandardowej klasy obsługi błędów Java**. Włącz te fragmenty kodu do swojego potoku budowania, aby uzyskać przejrzystość, zwiększyć niezawodność i spełnić wymogi zgodności na poziomie branżowym przy przetwarzaniu dokumentów CAD.

---

**Ostatnia aktualizacja:** 2026-11-18  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

## Powiązane samouczki

- [Eksport DWG do PDF i konwersja rysunków CAD – Samouczek Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Eksport DWG do PDF lub rastrowania przy użyciu Aspose.CAD dla Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Eksport konkretnego układu DWG do PDF przy użyciu Aspose.CAD dla Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}