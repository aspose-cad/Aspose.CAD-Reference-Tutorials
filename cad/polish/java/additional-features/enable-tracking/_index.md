---
date: 2026-02-10
description: Przewodnik krok po kroku, jak włączyć śledzenie w plikach DWG przy użyciu
  Aspose.CAD dla Javy oraz jak konwertować DXF na PDF z własnym obsługiwaczem błędów.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Jak włączyć śledzenie w plikach DWG przy użyciu Aspose.CAD w Javie
url: /pl/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak włączyć w plikach DWG przy użyciu Aspose.CAD w Javie

## Wstęp

Jeśli pracujesz nad współdzielonymi projektami CAD, dostępność **jak włączyć** w swoim przepływie pracy DWG jest przełomowa. Daje Ci wgląd w czasie problemów z renderowaniem, pozwala na obecność błędów i wszystkich zainteresowań, które występują. W tym samouczku przeprowadzimy Cię krok po kroku przez szczegółowe kroki włączenia aplikacji przy użyciu Aspose.CAD dla Javy, a także elementymy **jak konwertować DXF do PDF** w ramach tego samego potoku. Po usunięciu, gotowe do produkcji fragmentu kodu, który raportuje błędy za pomocą **niestandardowej klasy obsługi błędów Java** podczas eksportowania.

## Szybkie odpowiedzi
- **Co robi „enable dwg śledzenia java”?** Aktywuje wywołanie zwrotne obsługi błędów Aspose.CAD, dzięki czemu można zobaczyć problemy z renderowaniem podczas eksportu.
- **Czy jest licencjat?** Wersja próbna działa do testów; licencjat komercyjny jest wymagany w produkcji.
- **Czy mogę także konwertować DXF do PDF?** Tak – te same `PdfOptions` wykorzystywane dla DWG uzupełniające dla DXF, spełniając scenariusz *java konwertuj dxf pdf*.
- **Jakiej wersji JDK wymaga?** Java 8 lub nowsza.
- **Gdzie można znaleźć więcej zastosowań?** Sprawdź książkę Aspose.CAD Java pod linkiem poniżej.

## Jak włączyć śledzenie w plikach DWG przy użyciu Aspose.CAD

Włączenie aplikacji DWG w aplikacji Java oznacza własne renderera, które przechwytuje, błędy i inne informacje diagnostyczne podczas rasteryzacji lub eksportu pliku CAD. Ta informacja pomaga programistom debugować potoki końcowe i zapewnia najwyższej jakości produkty dostarczane.

## Dlaczego warto używać Aspose.CAD dla Java?

- **Pełne wsparcie CAD** – DWG, DXF, DGN i inne.
- **Brak zewnętrznych zależności** – czysta biblioteka Java, idealna do automatyzacji po stronie serwera.
- **Wbudowane** – szczegółowe wyniki renderowania za pomocą `CadRenderHandler`.
- **Łatwy eksport do PDF** – konwersja jednej linii przy zachowaniu danych wektorowych.

## Warunki wstępne

Zanim przejdziemy do implementacji, zakończymy, że zostaną spełnione szczegółowe wymagania:

- Java Development Kit (JDK): zastosowanie, że Java jest zainstalowana w systemie.
- Aspose.CAD dla Java: Pobierz i zainstaluj Aspose.CAD dla Java z [link do pobrania](https://releases.aspose.com/cad/java/).
- Katalog dokumentów: katalog, w którym znajdują się Twoje pliki DWG.

## Importuj przestrzenie nazw

W swoim środowisku Java rozpocznij od zaimportowania przestrzeni nazw, aby funkcje Aspose.CAD:

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

## Krok 1: Załaduj plik DWG

Rozpocznij od załadowania pliku DWG (lub DXF) do swojej aplikacji Java. Dostosuj ścieżkę do pliku odpowiednio:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Skonfiguruj opcje eksportu PDF (Jak przekonwertować DXF do PDF)

Skonfiguruj opcje eksportu do PDF, określając opcje rasteryzacji wektorowej dla CAD. To także demonstruje możliwość *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Krok 3: Wdróż śledzenie (niestandardowy moduł obsługi błędów Java)

Zaimplementuj śledzenie przy użyciu własnej klasy obsługi błędów. Ta klasa będzie przechwytywać problemy z renderowaniem i wyświetlać je w konsoli:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Eksport do PDF

Rozpocznij proces eksportu, aby przekonwertować plik DWG/DXF na PDF z włączonym śledzeniem:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Klasa CadRenderHandler

Zdefiniuj klasę `ErrorHandler` (rozszerzającą `CadRenderHandler`), aby przetwarzać wyniki renderowania i wyświetlać informacje o śledzeniu:

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

Włączając urządzenie, uzyskałeś dostęp do śledzenia audytu każdego kroku. Jest to szczególnie ważne w urządzeniach branżowych (architektura, inżynieria, budownictwo), gdy dowód dokładnego renderowania jest wymagany podczas audytów zgodności. Własna klasa obsługi błędów daje także możliwość logowania do systemu kontroli lub automatycznych testów.

## Typowe problemy i rozwiązania

- **`NullPointerException` przy `RenderResult`** – działanie, które następuje, że Aspose.CAD w wersji 23.10 lub nowszej; starsze wydanie nie opracowane API `RenderResult`.
- **Plik nie znaleziony** – Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku jest dokładnie równa, łącznie z wielkością litra.
- **Brak wyjścia** – zastosowanie, że własne `ErrorHandler` jest poprawnie przypisane do `cadRasterizationOptions.RenderResult`.

## Często zadawane pytania

**P:** Czy mogę włączyć dla innych formatów plików CAD przy użyciu Aspose.CAD dla Java?
A: Aspose.CAD jest obsługiwany przez DWG. Dla innych formatów można zastosować do przechowywania dokumentacji.

**Q:** Jak mogę obsłużyć dodatkowe wyposażenie eksportu w Aspose.CAD dla Java?
O: Zapoznaj się z obszerną dokumentacją pod adresem [Dokumentacja Java Aspose.CAD](https://reference.aspose.com/cad/java/).

**P:** Czy dostępna jest wersja próbna Aspose.CAD dla Java?
O: Tak, można spróbować uzyskać dostęp pod adresem [Bezpłatna wersja próbna Aspose.CAD](https://releases.aspose.com/).

**P:** Gdzie mogę uzyskać pomoc lub omówić problemy związane z Aspose.CAD dla Java?
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie społeczności.

**Q:** Jak uzyskać tymczasową różnicę dla Aspose.CAD dla Java?
A: Postępuj zgodnie z posiadaniem pod adresem [Licencja tymczasowa] (https://purchase.aspose.com/temporary-license/).

## Wniosek

Włączenie oprogramowania DWG w Javie przy użyciu Aspose.CAD nie tylko zapewnia wgląd w problemy zdrowotne, ale także usprawnia urządzenia w procesach projektowania. Po zapewnieniu zgodności z krokami, można **w urządzeniu dostępnym**, konwertować DXF do PDF i urządzenia z określonymi funkcjami renderowania w elegancki sposób.

---

**Ostatnia aktualizacja:** 10.02.2026
**Testowano z:** Aspose.CAD dla Java 24.12
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}