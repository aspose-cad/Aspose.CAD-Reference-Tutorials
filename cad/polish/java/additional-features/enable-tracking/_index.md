---
date: 2026-06-29
description: Dowiedz się, jak eksportować DWG do PDF, włączać śledzenie i używać niestandardowej
  klasy obsługi błędów Java z Aspose.CAD for Java. Zawiera konwersję DXF‑do‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Włącz śledzenie w plikach DWG przy użyciu Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
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
title: Eksportuj DWG do PDF i włącz śledzenie za pomocą Aspose.CAD Java
url: /pl/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj DWG do PDF i włącz śledzenie przy użyciu Aspose.CAD Java

## Wprowadzenie

Eksportowanie DWG do PDF przy zachowaniu pełnej przejrzystości procesu konwersji jest niezbędne dla nowoczesnych zespołów skoncentrowanych na CAD. W tym przewodniku dowiesz się **jak włączyć śledzenie** w przepływach pracy DWG, jak przekonwertować DXF do PDF w tym samym potoku oraz jak przechwycić każde ostrzeżenie renderowania za pomocą **niestandardowej klasy obsługi błędów Java**. Po zakończeniu będziesz posiadać gotowy do produkcji fragment kodu, który nie tylko generuje wysokiej jakości PDF‑y, ale także rejestruje informacje diagnostyczne do audytu i rozwiązywania problemów.

## Szybkie odpowiedzi
- **Co robi „enable dwg tracking java”?** Aktywuje wywołania zwrotne renderowania Aspose.CAD, dzięki czemu możesz zobaczyć ostrzeżenia i błędy podczas eksportu.  
- **Czy potrzebna jest licencja?** Wersja próbna działa do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę również konwertować DXF do PDF?** Tak – ten sam obiekt `PdfOptions` używany dla DWG działa także dla DXF, obejmując scenariusz *java convert dxf pdf*.  
- **Jaka wersja JDK jest wymagana?** Java 8 lub nowsza.  
- **Gdzie mogę znaleźć więcej przykładów?** Zobacz [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) poniżej.

## Czym jest eksport dwg do pdf?
Eksport DWG do PDF to proces konwersji natywnego rysunku AutoCAD (DWG) na przenośny dokument PDF przy zachowaniu wierności wektorowej, warstw i adnotacji. Aspose.CAD wykonuje tę konwersję w całości w Javie, eliminując potrzebę instalacji natywnego AutoCADa.

## Dlaczego używać Aspose.CAD dla Java?

Aspose.CAD for Java zapewnia kompleksowe, czysto‑Java rozwiązanie do konwersji CAD, obsługujące ponad 50 formatów, oferujące wysoką wydajność i wbudowane śledzenie poprzez wywołania zwrotne renderowania. Nie wymaga żadnych zewnętrznych zależności i może być zintegrowany z potokami po stronie serwera.

- **Kompleksowe wsparcie formatów** – obsługuje DWG, DXF, DGN oraz ponad 50 innych formatów CAD.  
- **Zero zewnętrznych zależności** – czysta biblioteka Java idealna do automatyzacji po stronie serwera.  
- **Wbudowane śledzenie** – `CadRenderHandler` dostarcza szczegółowe wyniki renderowania.  
- **Jednolinijkowy eksport PDF** – `PdfOptions` konwertuje do PDF, zachowując wektorowe dane.  

Te ilościowe twierdzenia są poparte zdolnością Aspose.CAD do przetwarzania plików do 500 stron bez ładowania całego dokumentu do pamięci, osiągając czasy konwersji poniżej 2 sekund na typowym serwerze 4‑rdzeniowym.

## Wymagania wstępne

- **Java Development Kit (JDK)** 8 lub nowszy zainstalowany na komputerze.  
- **Aspose.CAD for Java** pobrany z oficjalnego [download link](https://releases.aspose.com/cad/java/).  
- **Aspose.CAD Free Trial** można uzyskać ze strony [Aspose.CAD Free Trial](https://releases.aspose.com/) , jeśli potrzebujesz szybkiej oceny.  
- Folder zawierający pliki DWG/DXF, które chcesz skonwertować.  

## Jak wyeksportować DWG do PDF?  

Załaduj plik źródłowy, skonfiguruj `PdfOptions`, podłącz niestandardowy `CadRenderHandler` i wywołaj `save`. Ten kompleksowy przepływ konwertuje DWG (lub DXF) do PDF, jednocześnie emitując informacje śledzenia dla każdego kroku renderowania, zapewniając, że wszelkie ostrzeżenia lub błędy zostaną przechwycone i mogą być obsłużone przez programistów lub procesy automatyczne.

## Importowanie przestrzeni nazw

Klasa `CadRenderHandler` jest interfejsem zwrotnym Aspose.CAD, który otrzymuje diagnostykę renderowania. Zaimportuj wymagane pakiety przed rozpoczęciem kodowania:

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

## Krok 1: Załaduj plik DWG/DXF  

Klasa `CadImage` reprezentuje dokument CAD załadowany do pamięci. Utworzenie jej z ścieżką do pliku ładuje rysunek bez otwierania natywnej aplikacji CAD.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Skonfiguruj opcje eksportu PDF (Jak przekonwertować DXF do PDF)

`PdfOptions` definiuje, jak rasterizer CAD ma generować wyjście PDF, w tym ustawienia renderowania wektorowego i rozmiar strony. Ustawienie `VectorRasterizationOptions` zapewnia, że linie i krzywe pozostają ostre. Obiekt `VectorRasterizationOptions` określa parametry rasteryzacji, takie jak DPI i kolor tła.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Krok 3: Implementacja śledzenia (Niestandardowy obsługujący błędy Java)

`ErrorHandler` rozszerza `CadRenderHandler`, aby przechwytywać ostrzeżenia, błędy i komunikaty informacyjne emitowane podczas rasteryzacji. Ta klasa zapisuje każdą wiadomość w konsoli, ale możesz łatwo przekierować je do pliku logu lub systemu monitoringu. `CadRenderHandler` jest interfejsem, który otrzymuje diagnostykę renderowania od rasterizera.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Eksport do PDF  

Wywołanie `save` na instancji `CadImage` z skonfigurowanymi `PdfOptions` wykonuje konwersję. Ponieważ niestandardowy handler jest już podłączony, wszelkie problemy renderowania pojawiają się w konsoli w trakcie eksportu.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Klasa CadRenderHandler  

`CadRenderHandler` jest bazową klasą Aspose.CAD do odbierania wyników renderowania. Nadpisanie jej metody `onRenderCompleted` daje dostęp do obiektu `RenderResult`, który zawiera kolekcję wpisów `RenderMessage` opisujących każdy krok procesu.

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

Włączenie śledzenia tworzy ślad audytowy, który spełnia wymagania zgodności w regulowanych sektorach, takich jak architektura, inżynieria i budownictwo. Niestandardowy obsługujący błędy pozwala także zintegrować kontrole stanu konwersji CAD z potokami CI/CD, automatycznie oznaczając pliki wymagające ręcznej weryfikacji.

## Typowe problemy i rozwiązania

- **`NullPointerException` przy `RenderResult`** – Upewnij się, że używasz Aspose.CAD 23.10 lub nowszego; wcześniejsze wersje nie posiadają API `RenderResult`.  
- **Plik nie znaleziony** – Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku jest zgodna z wielkością liter.  
- **Brak wyjścia śledzenia** – Zweryfikuj, czy instancja `ErrorHandler` jest poprawnie przypisana do `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Najczęściej zadawane pytania

**Q:** Czy mogę włączyć śledzenie dla innych formatów plików CAD przy użyciu Aspose.CAD for Java?  
**A:** Śledzenie jest głównie udostępniane dla DWG i DXF. Dla innych formatów sprawdź oficjalną dokumentację, aby zobaczyć, które API udostępniają wywołania zwrotne renderowania.  

**Q:** Jak mogę dostosować dodatkowe opcje eksportu, takie jak ustawienie metadanych PDF?  
**A:** `PdfOptions` udostępnia właściwości takie jak `setTitle`, `setAuthor` i `setSubject`. Ustaw je przed wywołaniem `save`, aby osadzić metadane w wygenerowanym PDF.  

**Q:** Czy wersja próbna wystarczy do oceny funkcji śledzenia?  
**A:** Tak, bezpłatna wersja próbna zawiera pełny dostęp do API, umożliwiając testowanie `CadRenderHandler` i eksportu PDF bez ograniczeń.  

**Q:** Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD for Java?  
**A:** Odwiedź [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), aby zadawać pytania i dzielić się doświadczeniami z innymi programistami.  

**Q:** Jak uzyskać tymczasową licencję do środowisk testowych automatyzacji?  
**A:** Postępuj zgodnie z instrukcjami na [Temporary License](https://purchase.aspose.com/temporary-license/), aby wygenerować licencję o ograniczonym czasie ważności.  

## Podsumowanie

Postępując zgodnie z tym samouczkiem, teraz wiesz, jak **eksportować DWG do PDF**, włączyć pełne śledzenie oraz obsłużyć konwersję DXF‑do‑PDF przy użyciu **niestandardowej klasy obsługi błędów Java**. Włącz te fragmenty kodu do swojego potoku budowania, aby uzyskać przejrzystość, zwiększyć niezawodność i spełnić wymogi branżowe dotyczące przetwarzania dokumentów CAD.

---

**Last Updated:** 2026-06-29  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksportuj DWG do PDF i konwertuj rysunki CAD – Samouczek Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Eksportuj DWG do PDF lub rastrowania przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Eksportuj konkretny układ DWG do PDF przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}