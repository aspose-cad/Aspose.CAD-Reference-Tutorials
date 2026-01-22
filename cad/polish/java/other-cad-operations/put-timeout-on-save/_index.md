---
date: 2026-01-22
description: Dowiedz się, jak ustawić limit czasu przy zapisywaniu CAD do PDF przy
  użyciu Aspose.CAD dla Javy. Zwiększ wydajność dzięki temu przewodnikowi krok po
  kroku.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Jak ustawić limit czasu przy zapisywaniu CAD przy użyciu Aspose.CAD
url: /pl/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Limit czasu przy zapisywaniu CAD z Aspose.CAD

## Introduction

Witamy w samouczku dotyczącym **ustawiania limitu czasu** przy zapisywaniu rysunków CAD przy użyciu Aspose.CAD dla Javy. W tym przewodniku przeprowadzimy Cię przez proces konfigurowania limitu czasu dla operacji zapisu, co pomaga utrzymać responsywność aplikacji i poprawia ogólną wydajność. Aspose.CAD dla Javy to potężna biblioteka, która umożliwia płynną pracę z plikami CAD.

## Quick Answers
- **Co robi limit czasu?** Przerywa operację zapisu, jeśli przekroczy określony czas, zapobiegając długotrwałym zawieszeniom.  
- **Jaki format jest używany w przykładzie?** Rysunek CAD jest zapisywany jako plik PDF.  
- **Czy potrzebna jest licencja?** Do użytku produkcyjnego wymagana jest tymczasowa lub stała licencja Aspose.CAD.  
- **Jaką wersję Javy obsługuje?** Kod działa z Java 8 i nowszymi.  
- **Czy mogę dostosować długość limitu czasu?** Tak — wystarczy zmienić wartość w `TimeUnit.SECONDS.sleep(...)`.

## How to Set Timeout on Save

### Czym jest limit czasu w kontekście Aspose.CAD?
Limit czasu jest zabezpieczeniem, które zatrzymuje długi proces rasteryzacji lub konwersji. Dostarczając `InterruptionTokenSource`, możesz sygnalizować bibliotece, aby przerwała operację po określonym czasie, zapewniając responsywność aplikacji.

### Dlaczego ustawiać limit czasu przy zapisywaniu CAD do PDF?
Zapisywanie dużych lub złożonych rysunków CAD może zużywać znaczną ilość CPU i pamięci. Dodanie limitu czasu:
- Zapobiega zawieszeniu aplikacji.  
- Umożliwia eleganckie obsługiwanie długotrwałych zadań.  
- Poprawia ogólne doświadczenie użytkownika, szczególnie w środowiskach webowych lub opartych na interfejsie UI.

## Prerequisites

- **Aspose.CAD for Java Library** – Upewnij się, że biblioteka jest zintegrowana z Twoim projektem. Możesz pobrać bibliotekę ze [strony internetowej](https://releases.aspose.com/cad/java/).  
- **Środowisko programistyczne** – IDE Java (IntelliJ, Eclipse itp.) z zainstalowanym JDK 8+.

## Import Packages

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Teraz rozbijmy przykładowy kod na instrukcje krok po kroku:

## Krok 1: Ustaw katalogi źródłowy i wyjściowy

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Upewnij się, że masz prawidłowe katalogi źródłowy i wyjściowy dla swoich rysunków CAD.

## Krok 2: Utwórz źródło tokenu przerwania

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Zainicjuj źródło tokenu przerwania, aby zarządzać przerwami podczas operacji zapisu.

## Krok 3: Wczytaj rysunek CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Wczytaj rysunek CAD do obiektu `CadImage`.

## Krok 4: Skonfiguruj opcje rasteryzacji

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Skonfiguruj opcje rasteryzacji dla rysunku CAD.

## Krok 5: Skonfiguruj opcje PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ustaw opcje PDF z opcjami rasteryzacji wektorowej oraz tokenem przerwania.

## Krok 6: Zapisz rysunek z limitem czasu

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Zapisz rysunek CAD do pliku PDF z określonym limitem czasu.

## Krok 7: Obsłuż przerwanie

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

Utwórz wątek, który obsłuży operację zapisu i przerwie ją po określonym czasie.

## Typowe pułapki i rozwiązywanie problemów

- **Limit czasu zbyt krótki** – Jeśli rysunek jest duży, bardzo krótki limit czasu może przerwać operację, zanim się zakończy. Zwiększ czas snu lub dostosuj ustawienia rasteryzacji.  
- **Brak licencji** – Uruchomienie bez ważnej licencji spowoduje wyrzucenie wyjątku. Zastosuj tymczasową lub stałą licencję przed wykonaniem kodu.  
- **Nieprawidłowe ścieżki** – Upewnij się, że `SourceDir` i `OutputDir` wskazują istniejące foldery; w przeciwnym razie `Image.load` lub `save` zakończy się niepowodzeniem.

## Najczęściej zadawane pytania

**P: Jak mogę pobrać Aspose.CAD dla Javy?**  
O: Możesz pobrać go ze [strony wydań](https://releases.aspose.com/cad/java/).

**P: Gdzie mogę znaleźć dokumentację Aspose.CAD dla Javy?**  
O: Zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/java/) po szczegółowe informacje.

**P: Czy dostępna jest darmowa wersja próbna?**  
O: Tak, możesz uzyskać darmową wersję próbną pod [tym linkiem](https://releases.aspose.com/).

**P: Jak uzyskać tymczasową licencję?**  
O: Odwiedź [tutaj](https://purchase.aspose.com/temporary-license/) po szczegóły dotyczące tymczasowej licencji.

**P: Potrzebujesz pomocy lub masz pytania?**  
O: Przejdź na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) po wsparcie społeczności.

## Podsumowanie

 Aspose.CAD dla Javy niezawodność i responsywność Twoich aplikacji związanych z CAD.

---

**Ostatnia aktualizacja:** 2026-01-22  
**Testowano z:** Aspose.CAD for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}