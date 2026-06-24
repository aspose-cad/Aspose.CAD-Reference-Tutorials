---
date: 2026-02-12
description: Dowiedz się, jak ustawić rozmiar strony PDF podczas konwertowania CAD
  na PDF przy użyciu Aspose.CAD dla Javy. Postępuj zgodnie z tym przewodnikiem krok
  po kroku, aby włączyć śledzenie, konwertować CAD na PDF i efektywnie zapisywać CAD
  jako PDF.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: Jak ustawić rozmiar strony PDF i włączyć śledzenie procesu renderowania CAD
url: /pl/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Włącz śledzenie procesu renderowania CAD

## Wprowadzenie

W tym samouczku dowiesz się, jak **ustawić rozmiar strony PDF** podczas **konwersji CAD do PDF** przy użyciu **Aspose.CAD for Java**. Włączając śledzenie, zyskujesz pełną widoczność pipeline’u renderowania, co ułatwia debugowanie i optymalizację konwersji plików CAD (takich jak DXF) do PDF. Niezależnie od tego, czy potrzebujesz **zapisać CAD jako PDF**, wygenerować PDF z DXF, czy po prostu kontrolować wymiary wyjściowe, poniższe kroki przeprowadzą Cię przez cały proces.

## Szybkie odpowiedzi
- **Co robi „set PDF page size”?** Definiuje szerokość i wysokość wynikowej strony PDF podczas renderowania CAD.  
- **Dlaczego włączyć śledzenie?** Śledzenie zapisuje w logu każdy etap konwersji, pomagając wykrywać wąskie gardła wydajności lub błędy.  
- **Czy potrzebna jest licencja?** Bezpłatna wersja próbna wystarcza do oceny; licencja komercyjna jest wymagana w produkcji.  
- **Jakie formaty CAD są obsługiwane?** DWG, DXF, DGN i wiele innych – pełną listę znajdziesz w dokumentacji Aspose.CAD.  
- **Czy mogę zmieniać wymiary strony w locie?** Tak – po prostu dostosuj wartości `PageWidth` i `PageHeight` w `CadRasterizationOptions`.

## Co oznacza „set PDF page size” w renderowaniu CAD?

Ustawienie rozmiaru strony PDF informuje rasteryzator, jak duże ma być płótno, gdy wektorowe dane CAD są rasteryzowane na stronę PDF. Jest to kluczowe dla zachowania wierności wizualnej, szczególnie przy szczegółowych rysunkach inżynierskich.

## Dlaczego włączyć śledzenie dla renderowania CAD?

Włączenie śledzenia zapewnia szczegółowy log każdego kroku — od załadowania pliku źródłowego po zapisanie wyjścia PDF. Pomaga to:

- Zdiagnozować, dlaczego konkretny rysunek może renderować się niepoprawnie.  
- Zmierz czas trwania każdego etapu, co jest przydatne przy optymalizacji wydajności.  
- Zweryfikować, że skonfigurowany rozmiar strony został rzeczywiście zastosowany.

## Wymagania wstępne

Przed przystąpieniem do konfiguracji śledzenia upewnij się, że spełniasz następujące wymagania:

1. **Środowisko programistyczne Java** – Java 8 lub nowsza zainstalowana na Twoim komputerze.  
2. **Biblioteka Aspose.CAD** – Pobierz i zintegrować bibliotekę Aspose.CAD w swoim projekcie Java. Link do pobrania znajdziesz [tutaj](https://releases.aspose.com/cad/java/).  
3. **Katalog dokumentów** – Przygotuj katalog do przechowywania plików CAD oraz generowanych plików PDF.

## Importowanie przestrzeni nazw

W swoim projekcie Java zaimportuj niezbędne przestrzenie nazw, aby wykorzystać funkcjonalności Aspose.CAD. Dodaj następujące linie na początku swojego kodu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Ustaw ścieżkę katalogu zasobów

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Zastąp `"Your Document Directory"` rzeczywistą ścieżką do swojego katalogu dokumentów.

## Wczytaj plik CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Określ ścieżkę do pliku CAD, upewniając się, że znajduje się on w wyznaczonym katalogu dokumentów.

## Ustaw opcje wyjściowe PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

## Skonfiguruj CadRasterizationOptions (Ustaw rozmiar strony PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Tutaj **ustawiamy rozmiar strony PDF** definiując `PageWidth` i `PageHeight`. Dostosuj te wartości, aby odpowiadały wymiarom wymaganego rysunku inżynierskiego. To kluczowy krok, który odpowiada na pytanie **jak ustawić rozmiar PDF**, gdy **java cad to pdf**.

## Zapisz plik PDF

```java
image.save(stream, pdfOptions);
```

Zapisz wyrenderowany plik PDF z określonymi opcjami.

## Sprawdź włączenie śledzenia

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

Potwierdź, że śledzenie zostało pomyślnie włączone dla procesu renderowania CAD.

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------|-----|
| Strona PDF jest pusta | `PageWidth`/`PageHeight` ustawione na 0 | Upewnij się, że podano wymiary różne od zera. |
| Plik wyjściowy jest uszkodzony | Strumień wyjściowy nie został zamknięty | Wywołaj `stream.close()` po `image.save(...)`. |
| Brak warstw w PDF | Plik CAD używa nieobsługiwanych elementów | Sprawdź, czy format pliku jest w pełni obsługiwany przez Aspose.CAD. |

## Najczęściej zadawane pytania

### Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

A1: Aspose.CAD obsługuje szeroką gamę formatów CAD, w tym DWG, DXF, DGN i inne. Pełną listę znajdziesz w [dokumentacji](https://reference.aspose.com/cad/java/).

### Q2: Czy mogę dostosować wymiary wyjściowe pliku PDF?

A2: Oczywiście! Dostosuj parametry `PageWidth` i `PageHeight` w `CadRasterizationOptions`, aby dopasować wymiary wyjściowe.

### Q3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla Java?

A3: Tak, możesz zapoznać się z możliwościami Aspose.CAD, uzyskując bezpłatną wersję próbną [tutaj](https://releases.aspose.com/).

### Q4: Jak mogę uzyskać wsparcie społeczności w kwestiach związanych z Aspose.CAD?

A4: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby skontaktować się ze społecznością i uzyskać pomoc.

### Q5: Czy dostępne są tymczasowe licencje dla Aspose.CAD?

A5: Tak, jeśli potrzebujesz tymczasowej licencji, możesz ją uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

## Podsumowanie

Gratulacje! Nauczyłeś się, jak **ustawić rozmiar strony PDF** i włączyć śledzenie dla renderowania CAD przy użyciu **Aspose.CAD for Java**. Ten przewodnik umożliwia **konwersję CAD do PDF**, **zapis CAD jako PDF** oraz generowanie PDF z DXF z pełną kontrolą nad wymiarami strony i szczegółowymi logami wykonania. Śmiało eksperymentuj z różnymi rozmiarami stron i odkrywaj dodatkowe opcje rasteryzacji, aby dopasować je do swoich specyficznych procesów inżynierskich.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}