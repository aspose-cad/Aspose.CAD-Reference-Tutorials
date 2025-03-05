---
title: Przekroczono limit czasu zapisu dla CAD za pomocą Aspose.CAD
linktitle: Ustaw limit czasu na zapisywanie
second_title: Aspose.CAD API Java
description: Dowiedz się, jak zwiększyć wydajność aplikacji Java za pomocą Aspose.CAD. Ustaw limit czasu zapisu rysunków CAD. Postępuj zgodnie z naszym przewodnikiem krok po kroku.
type: docs
weight: 15
url: /pl/java/other-cad-operations/put-timeout-on-save/
---
## Wstęp

Witamy w samouczku dotyczącym ustawiania limitu czasu zapisu przy użyciu Aspose.CAD dla Java. W tym przewodniku przeprowadzimy Cię przez proces ustawiania limitu czasu zapisywania rysunków CAD w celu zwiększenia wydajności aplikacji. Aspose.CAD for Java to potężna biblioteka, która umożliwia płynną pracę z plikami CAD w aplikacjach Java.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
-  Biblioteka Aspose.CAD for Java: Upewnij się, że biblioteka Aspose.CAD for Java jest zintegrowana z projektem. Bibliotekę można pobrać ze strony[strona internetowa](https://releases.aspose.com/cad/java/).
- Środowisko programistyczne: Skonfiguruj środowisko programistyczne Java ze wszystkimi niezbędnymi narzędziami i zależnościami.

## Importuj pakiety

Aby rozpocząć, zaimportuj wymagane pakiety do swojego projektu Java. Dodaj następujące wiersze na początku pliku Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Podzielmy teraz przykładowy kod na instrukcje krok po kroku:

## Krok 1: Ustaw katalogi źródłowe i wyjściowe

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Upewnij się, że masz prawidłowe katalogi źródłowe i wyjściowe dla rysunków CAD.

## Krok 2: Utwórz źródło tokenu przerwania

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Zainicjuj źródło tokenu przerwania, aby zarządzać przerwami podczas operacji zapisywania.

## Krok 3: Załaduj rysunek CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Załaduj rysunek CAD do pliku`CadImage` obiekt.

## Krok 4: Skonfiguruj opcje rasteryzacji

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Skonfiguruj opcje rasteryzacji rysunku CAD.

## Krok 5: Skonfiguruj opcje PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Skonfiguruj opcje PDF z opcjami rasteryzacji wektorowej i tokenem przerwania.

## Krok 6: Zapisz rysunek z limitem czasu

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Zapisz rysunek CAD w pliku PDF z określonym limitem czasu.

## Krok 7: Obsługuj przerwanie

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

Utwórz wątek do obsługi operacji zapisywania i przerwij ją po upływie określonego limitu czasu.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak ustawić limit czasu zapisu przy użyciu Aspose.CAD dla Java. Ta funkcja może znacznie zwiększyć wydajność aplikacji związanych z CAD.

## Często zadawane pytania

### P1: Jak mogę pobrać Aspose.CAD dla Java?

 Odpowiedź 1: Możesz pobrać go z[strona z wydaniami](https://releases.aspose.com/cad/java/).

### P2: Gdzie mogę znaleźć dokumentację Aspose.CAD dla Java?

 Odpowiedź 2: Patrz[dokumentacja](https://reference.aspose.com/cad/java/) w celu uzyskania wyczerpujących informacji.

### P3: Czy dostępny jest bezpłatny okres próbny?

A3: Tak, możesz uzyskać bezpłatną wersję próbną[ten link](https://releases.aspose.com/).

### P4: Jak uzyskać licencję tymczasową?

 A4: Odwiedź[Tutaj](https://purchase.aspose.com/temporary-license/) aby uzyskać szczegółowe informacje o licencji tymczasowej.

### P5: Potrzebujesz pomocy lub masz pytania?

 A5: Udaj się do[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności.