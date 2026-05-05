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

# Jak włączyć śledzenie w plikach DWG przy użyciu Aspose.CAD w Javie

## Introduction

Jeśli pracujesz nad współdzielonymi projektami CAD, znajomość **jak włączyć śledzenie** w swoim przepływie pracy DWG jest przełomowa. Daje Ci wgląd w czasie rzeczywistym w problemy z renderowaniem, pozwala wcześnie wykrywać błędy konwersji i utrzymuje wszystkich interesariuszy poinformowanych. W tym samouczku przeprowadzimy Cię krok po kroku przez dokładne kroki włączenia śledzenia przy użyciu Aspose.CAD dla Javy, a także pokażemy **jak konwertować DXF do PDF** w ramach tego samego potoku. Po zakończeniu będziesz mieć kompletny, gotowy do produkcji fragment kodu, który raportuje błędy za pomocą **niestandardowej klasy obsługi błędów Java** podczas eksportowania rysunków.

## Quick Answers
- **Co robi “enable dwg tracking java”?** Aktywuje wywołania zwrotne obsługi błędów Aspose.CAD, dzięki czemu możesz zobaczyć problemy z renderowaniem podczas eksportu.  
- **Czy potrzebna jest licencja?** Wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę także konwertować DXF do PDF?** Tak – te same `PdfOptions` użyte dla DWG działają dla DXF, spełniając scenariusz *java convert dxf pdf*.  
- **Jakiej wersji JDK wymaga się?** Java 8 lub nowsza.  
- **Gdzie mogę znaleźć więcej przykładów?** Sprawdź dokumentację Aspose.CAD Java pod linkiem poniżej.

## How to Enable Tracking in DWG Files Using Aspose.CAD

Włączenie śledzenia DWG w aplikacji Java oznacza podłączenie własnego renderera, który przechwytuje ostrzeżenia, błędy i inne informacje diagnostyczne podczas rasteryzacji lub eksportu pliku CAD. Ta widoczność pomaga programistom debugować potoki konwersji i zapewnia wyższą jakość dostarczanych produktów.

## Why Use Aspose.CAD for Java?

- **Pełne wsparcie CAD** – DWG, DXF, DGN i inne.  
- **Brak zewnętrznych zależności** – czysta biblioteka Java, idealna do automatyzacji po stronie serwera.  
- **Wbudowane śledzenie** – szczegółowe wyniki renderowania za pomocą `CadRenderHandler`.  
- **Łatwy eksport do PDF** – konwersja jedną linią przy zachowaniu danych wektorowych.  

## Prerequisites

Zanim przejdziemy do implementacji, upewnij się, że masz spełnione następujące wymagania:

- Java Development Kit (JDK): Upewnij się, że Java jest zainstalowana w Twoim systemie.
- Aspose.CAD for Java: Pobierz i zainstaluj Aspose.CAD for Java z [download link](https://releases.aspose.com/cad/java/).
- Document Directory: Przygotuj katalog, w którym znajdują się Twoje pliki DWG.

## Import Namespaces

W swoim projekcie Java rozpocznij od zaimportowania niezbędnych przestrzeni nazw, aby wykorzystać funkcje Aspose.CAD:

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

## Step 1: Load the DWG File

Rozpocznij od załadowania pliku DWG (lub DXF) do swojej aplikacji Java. Dostosuj ścieżkę do pliku odpowiednio:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (How to Convert DXF to PDF)

Skonfiguruj opcje eksportu do PDF, określając opcje rasteryzacji wektorowej dla CAD. To także demonstruje możliwość *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Step 3: Implement Tracking (Custom Error Handler Java)

Zaimplementuj śledzenie przy użyciu własnej klasy obsługi błędów. Ta klasa będzie przechwytywać problemy z renderowaniem i wyświetlać je w konsoli:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

Rozpocznij proces eksportu, aby przekonwertować plik DWG/DXF na PDF z włączonym śledzeniem:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

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

## Why This Matters

Włączając śledzenie, uzyskasz przejrzysty ślad audytu każdego kroku konwersji. Jest to szczególnie cenne w regulowanych branżach (architektura, inżynieria, budownictwo), gdzie dowód dokładnego renderowania jest wymagany podczas audytów zgodności. Własna klasa obsługi błędów daje także możliwość logowania problemów do systemu monitorowania lub wyzwalania automatycznych ponownych prób.

## Common Issues and Solutions

- **`NullPointerException` przy `RenderResult`** – Upewnij się, że używasz Aspose.CAD w wersji 23.10 lub nowszej; starsze wydania nie posiadają API `RenderResult`.  
- **Plik nie znaleziony** – Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku dokładnie się zgadza, łącznie z wielkością liter.  
- **Brak wyjścia śledzenia** – Upewnij się, że własny `ErrorHandler` jest poprawnie przypisany do `cadRasterizationOptions.RenderResult`.  

## Frequently Asked Questions

**Q:** Czy mogę włączyć śledzenie dla innych formatów plików CAD przy użyciu Aspose.CAD dla Java?  
A: Aspose.CAD głównie obsługuje śledzenie DWG. Dla innych formatów odwołaj się do oficjalnej dokumentacji.

**Q:** Jak mogę obsłużyć dodatkowe opcje eksportu w Aspose.CAD dla Java?  
A: Zapoznaj się z obszerną dokumentacją pod adresem [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**Q:** Czy dostępna jest wersja próbna Aspose.CAD dla Java?  
A: Tak, wersję próbną możesz uzyskać pod adresem [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q:** Gdzie mogę uzyskać pomoc lub dyskutować problemy związane z Aspose.CAD dla Java?  
A: Odwiedź [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) aby uzyskać wsparcie społeczności.

**Q:** Jak uzyskać tymczasową licencję dla Aspose.CAD dla Java?  
A: Postępuj zgodnie z procesem opisanym pod adresem [Temporary License](https://purchase.aspose.com/temporary-license/).

## Conclusion

Włączenie śledzenia DWG w Javie przy użyciu Aspose.CAD nie tylko zapewnia wgląd w problemy konwersji, ale także usprawnia współpracę w procesach projektowania. Postępując zgodnie z powyższymi krokami, możesz **włączyć śledzenie**, konwertować DXF do PDF i radzić sobie z wszelkimi problemami renderowania w elegancki sposób.

---

**Last Updated:** 2026-02-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}