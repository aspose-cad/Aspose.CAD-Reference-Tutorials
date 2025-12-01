---
date: 2025-12-01
description: Dowiedz się, jak ustawić rozmiar strony PDF, konwertować DWG do PDF oraz
  włączyć śledzenie zmian w DWG przy użyciu Aspose.CAD dla Javy.
language: pl
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Ustaw rozmiar strony PDF i śledź DWG przy użyciu Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw rozmiar strony PDF i śledź DWG przy użyciu Aspose.CAD Java

## Wprowadzenie

Podczas współpracy nad projektami CAD często trzeba **ustawić rozmiar strony PDF** dla spójnego układu, **przekonwertować DWG na PDF** oraz śledzić każdą zmianę w rysunku. Aspose.CAD dla Javy umożliwia to wszystko w jednym, uproszczonym procesie. W tym samouczku przeprowadzimy Cię krok po kroku przez **ustawienie rozmiaru strony PDF**, włączenie **śledzenia zmian DWG** oraz eksport rysunku jako PDF – wszystko przy użyciu Javy.

## Szybkie odpowiedzi
- **Jak ustawić rozmiar strony PDF?** Użyj `CadRasterizationOptions.setPageWidth()` i `setPageHeight()` przed eksportem.  
- **Czy mogę śledzić zmiany podczas eksportu?** Tak – zaimplementuj własny `CadRenderHandler`, aby przechwycić wyniki śledzenia.  
- **Która metoda konwertuje DWG na PDF?** Wywołaj `image.save(stream, pdfOptions)` po skonfigurowaniu opcji.  
- **Jakie są główne wymagania wstępne?** JDK, Aspose.CAD dla Javy oraz folder z plikami DWG/DXF.  
- **Czy licencja jest wymagana w środowisku produkcyjnym?** Tak, wymagana jest ważna licencja Aspose.CAD dla wdrożeń nie‑trialowych.

## Co oznacza „ustaw rozmiar strony PDF” w kontekście eksportu DWG?

Ustawienie rozmiaru strony PDF określa wymiary docelowego płótna PDF (szerokość × wysokość w pikselach). Jest to niezbędne, gdy chcesz, aby wyeksportowany rysunek pasował do określonego rozmiaru papieru lub układu ekranu, zapewniając, że wszystkie elementy będą dokładnie tam, gdzie ich oczekujesz.

## Dlaczego włączać śledzenie podczas eksportu plików DWG?

Śledzenie (lub change‑tracking) rejestruje wszelkie problemy z renderowaniem, brakujące czcionki lub nieobsługiwane elementy, które występują podczas konwersji. Przechwytywanie tych informacji pozwala:

- Szybko zidentyfikować problemy wymagające naprawy przed ostatecznym dostarczeniem.  
- Dostarczyć zespołowi jasną informację zwrotną o tym, co zostało zmienione lub pominięte.  
- Utrzymać ślad audytu dla branż o wysokich wymaganiach regulacyjnych.

## Wymagania wstępne

- **Java Development Kit (JDK)** – dowolna aktualna wersja (8+).  
- **Aspose.CAD dla Javy** – pobierz z oficjalnej [strony pobierania Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Katalog dokumentów** – folder zawierający pliki DWG/DXF, które chcesz przetworzyć.

## Import przestrzeni nazw

Rozpocznij od zaimportowania niezbędnych klas Aspose.CAD oraz standardowych klas Java I/O.

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

## Krok 1: Załaduj plik DWG (lub DXF)

Wczytaj źródłowy rysunek do obiektu `Image`. Dostosuj ścieżkę, aby wskazywała na Twój własny katalog.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Skonfiguruj opcje eksportu PDF (w tym rozmiar strony)

Tutaj ustawiamy opcje PDF i wyraźnie **ustawiamy rozmiar strony PDF** na 800 × 600 pikseli. To miejsce, w którym stosujemy główne słowo kluczowe.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Krok 3: Implementacja śledzenia

Utwórz własny handler błędów, który będzie odbierał informacje śledzenia podczas procesu konwersji.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Eksport do PDF

Po skonfigurowaniu opcji i handlera śledzenia, wyeksportuj rysunek. Ten krok **konwertuje DWG na PDF** (lub DXF na PDF w naszym przykładzie).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Klasa CadRenderHandler – przechwytywanie wyników śledzenia

Klasa `ErrorHandler` rozszerza `CadRenderHandler` i wypisuje wszelkie problemy renderowania, które wystąpiły podczas **śledzenia zmian w plikach DWG**.

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

## Typowe problemy i ich rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Brakujące czcionki** | Plik CAD odwołuje się do czcionek niezainstalowanych na serwerze. | Zainstaluj wymagane czcionki lub osadź je w źródłowym rysunku. |
| **Nieobsługiwane elementy** | Niektóre elementy DWG nie są jeszcze obsługiwane przez Aspose.CAD. | Skorzystaj z wyjścia śledzenia, aby je zidentyfikować i uprościć rysunek. |
| **Nieprawidłowy rozmiar strony** | `setPageWidth/Height` nie zostało wywołane przed eksportem. | Upewnij się, że rozmiar strony jest ustawiony w `CadRasterizationOptions`, jak pokazano wyżej. |

## Najczęściej zadawane pytania

### Q1: Czy mogę włączyć śledzenie dla innych formatów CAD przy użyciu Aspose.CAD dla Javy?

A1: Aspose.CAD głównie obsługuje śledzenie dla plików DWG/DXF. Dla innych formatów sprawdź oficjalną dokumentację, aby zobaczyć dostępne funkcje.

### Q2: Jak mogę obsłużyć dodatkowe opcje eksportu w Aspose.CAD dla Javy?

A2: Biblioteka oferuje wiele opcji, takich jak DPI, kolor tła i rasteryzacja wektorowa. Zapoznaj się z nimi w [Dokumentacji Aspose.CAD Java](https://reference.aspose.com/cad/java/).

### Q3: Czy dostępna jest wersja próbna Aspose.CAD dla Javy?

A3: Tak, możesz pobrać darmową wersję próbną z [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Gdzie mogę uzyskać pomoc lub dyskutować o problemach związanych z Aspose.CAD dla Javy?

A4: Forum społecznościowe pod adresem [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to świetne miejsce, aby zadawać pytania i dzielić się doświadczeniami.

### Q5: Jak uzyskać tymczasową licencję dla Aspose.CAD dla Javy?

A5: Postępuj zgodnie z instrukcjami na stronie [Temporary License](https://purchase.aspose.com/temporary-license/), aby zamówić licencję czasowo‑ograniczoną do oceny.

### Q6: Czy mogę **konwertować DWG na PDF** zachowując warstwy?

A6: Tak. Konfigurując `CadRasterizationOptions`, możesz zachować informacje o warstwach w wygenerowanym pliku PDF.

### Q7: Jaki jest najlepszy sposób na **eksport DWG jako PDF** z niestandardowymi wymiarami strony?

A7: Ustaw żądaną szerokość i wysokość przy użyciu `setPageWidth` i `setPageHeight` przed wywołaniem `image.save()` – dokładnie tak, jak pokazano w Kroku 2.

## Podsumowanie

Postępując zgodnie z powyższymi krokami, możesz **ustawić rozmiar strony PDF**, **konwertować DWG na PDF** oraz **śledzić zmiany w plikach DWG** przy użyciu Aspose.CAD dla Javy. Ten proces daje pełną kontrolę nad układem wyjściowym, jednocześnie dostarczając cennych diagnostyk, które utrzymują współpracę CAD płynną i wolną od błędów. Zachęcamy do eksploracji dodatkowych opcji renderowania i integracji tego kodu w większych pipeline’ach automatyzacji.

---

**Ostatnia aktualizacja:** 2025-12-01  
**Testowano z:** Aspose.CAD dla Javy 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}