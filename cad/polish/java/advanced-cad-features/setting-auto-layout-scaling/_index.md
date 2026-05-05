---
date: 2026-02-15
description: Dowiedz się, jak ustawić niestandardowy rozmiar strony i utworzyć PDF
  z CAD przy użyciu Aspose.CAD for Java. Ten przewodnik krok po kroku opisuje eksport
  CAD do PDF z automatycznym skalowaniem układu.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Ustaw niestandardowy rozmiar strony – PDF z CAD z automatycznym skalowaniem
  układu
url: /pl/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustaw niestandardowy rozmiar strony – Tworzenie PDF z CAD z automatycznym skalowaniem układu

## Wprowadzenie

Jeśli potrzebujesz **ustawić niestandardowy rozmiar strony** podczas **tworzenia PDF z CAD** szybko i z idealnym skalowaniem, Aspose.CAD for Java ma dla Ciebie rozwiązanie. Auto Layout Scaling automatycznie dostosowuje wymiary układu, tak aby powstały PDF wyglądał dokładnie tak, jak zamierzono, niezależnie od pierwotnego rozmiaru strony CAD. W tym samouczku przeprowadzimy Cię przez cały proces — od wczytania pliku DXF po eksport do PDF — podkreślając możliwości **export CAD to PDF** biblioteki oraz pokazując, jak możesz także **convert DWG to PDF** lub **increase PDF resolution**, gdy zajdzie taka potrzeba.

## Szybkie odpowiedzi
- **Co robi Auto Layout Scaling?** Automatycznie zmienia rozmiar układów CAD, aby pasowały do wymiarów docelowej strony podczas rasteryzacji.  
- **Jakie formaty mogę konwertować?** Każdy format obsługiwany przez Aspose.CAD (np. DXF, DWG, DWF) może być skonwertowany do PDF.  
- **Czy potrzebna jest licencja do produkcji?** Tak, do użytku nie‑ewaluacyjnego wymagana jest licencja komercyjna.  
- **Jak długo trwa konwersja?** Zazwyczaj poniżej sekundy dla standardowych plików na nowoczesnym sprzęcie.  
- **Czy mogę zmienić rozmiar strony?** Tak, możesz ustawić własne wymiary strony za pomocą `CadRasterizationOptions`.

## Co to jest „tworzenie PDF z CAD”?

Tworzenie PDF z CAD oznacza pobranie wektorowego rysunku inżynieryjnego (DXF, DWG itp.) i rasteryzację go do dokumentu PDF. PDF zachowuje wizualną wierność oryginalnego rysunku, jednocześnie będąc szeroko dostępny na każdej platformie.

## Dlaczego używać automatycznego skalowania układu?

- **Spójny wynik:** Gwarantuje, że wszystkie układy wypełnią stronę PDF bez ręcznych obliczeń rozmiaru.  
- **Oszczędność czasu:** Eliminuję potrzebę ręcznego dostosowywania współczynników skalowania dla każdego rysunku.  
- **Wysoka jakość:** Zachowuje grubość linii i dokładność geometrii podczas konwersji.  
- **Elastyczność:** Działa dla **convert dxf to pdf**, **convert dwg to pdf**, a także gdy potrzebujesz **increase PDF resolution** dla plików gotowych do druku.

## Wymagania wstępne

1. **Aspose.CAD for Java Library** – pobierz najnowszą wersję ze [strony pobierania](https://releases.aspose.com/cad/java/).  
2. **Katalog zasobów** – utwórz folder na swoim komputerze do przechowywania plików CAD; zamień `"Your Document Directory"` w kodzie na tę ścieżkę.  
3. **Przykładowy plik CAD** – w tym przewodniku użyjemy `conic_pyramid.dxf`, który jest częścią zestawu danych przykładowych Aspose.

## Importowanie przestrzeni nazw

Najpierw zaimportuj wymagane klasy. Dzięki temu uzyskasz dostęp do funkcji wczytywania obrazu, rasteryzacji i eksportu PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak ustawić niestandardowy rozmiar strony dla PDF z CAD

Zanim przejdziemy do kodu krok po kroku, wyjaśnijmy, dlaczego ustawienie niestandardowego rozmiaru strony ma znaczenie. Kiedy **ustawiasz niestandardowy rozmiar strony**, kontrolujesz fizyczne wymiary powstałego PDF (np. A4, Letter lub rozmiar specjalny). Jest to niezbędne w przepływach pracy inżynieryjnej, gdzie rysunki muszą odpowiadać standardom arkuszy lub gdy trzeba osadzić PDF w większych dokumentach.

### Krok 1: Załaduj plik CAD

Wczytanie pliku źródłowego to pierwszy krok w **how to export CAD** do dokumentu PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Krok 2: Utwórz opcje rasteryzacji

Zdefiniuj docelowe wymiary strony. Ten blok możesz także użyć do **set CAD page size** ręcznie, jeśli wolisz własny układ.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Krok 3: Ustaw automatyczne skalowanie układu

Włącz funkcję automatycznego skalowania. To jest sedno **how to set scaling** dla konwersji CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Krok 4: Utwórz opcje PDF

Połącz ustawienia rasteryzacji z opcjami eksportu PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Eksportuj do PDF

Na koniec zapisz wyrenderowany obraz jako plik PDF. Ten krok kończy przepływ **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Powtórz powyższe kroki dla dowolnych dodatkowych plików CAD, które musisz przetworzyć, niezależnie od tego, czy są to **DWG**, **DWF**, czy inne obsługiwane formaty.

## Typowe przypadki użycia

| Scenariusz | Dlaczego ustawić niestandardowy rozmiar strony? |
|------------|---------------------------------------------------|
| **Złożenie rysunku budowlanego** | Dopasowuje PDF do standardowych rozmiarów arkuszy A1/A2 wymaganych przez organy regulacyjne. |
| **Osadzanie w podręcznikach technicznych** | Gwarantuje, że rysunek pasuje do wcześniej określonego układu podręcznika bez dodatkowego skalowania. |
| **Druk wysokiej rozdzielczości** | Pozwala zwiększyć DPI (np. `rasterizationOptions.setResolution(300)`) przy zachowaniu stałych wymiarów strony. |

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| Pusty plik PDF | Opcje rasteryzacji nie ustawione lub niepoprawna ścieżka pliku | Sprawdź ścieżkę `srcFile` i upewnij się, że `setPageWidth/Height` nie są zerowe |
| Zniekształcone skalowanie | `setAutomaticLayoutsScaling` pozostawiono jako `false` | Włącz automatyczne skalowanie lub ręcznie oblicz współczynnik skalowania |
| Brak warstw | Źródłowy DXF zawiera nieobsługiwane encje | Sprawdź notatki wydania Aspose.CAD pod kątem obsługiwanych typów encji |

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD for Java jest kompatybilny ze wszystkimi formatami plików CAD?**  
O: Aspose.CAD for Java obsługuje różne formaty CAD, w tym DWG, DXF i DWF.

**P: Czy mogę dalej dostosowywać opcje skalowania?**  
O: Tak, klasa `CadRasterizationOptions` udostępnia właściwości do precyzyjnego dostrajania skalowania, DPI i innych ustawień rasteryzacji.

**P: Gdzie mogę znaleźć dodatkową dokumentację dla Aspose.CAD for Java?**  
O: Odwołaj się do [dokumentacji](https://reference.aspose.com/cad/java/) po szczegółowe informacje i przykłady.

**P: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
O: Tak, możesz wypróbować [bezpłatną wersję próbną](https://releases.aspose.com/), aby zapoznać się z możliwościami Aspose.CAD for Java.

**P: Jak mogę uzyskać pomoc lub wziąć udział w dyskusjach o Aspose.CAD for Java?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby połączyć się ze społecznością i uzyskać wsparcie.

**Dodatkowe typowe pytania**

**P: Jak przekonwertować plik DWG na PDF zamiast DXF?**  
O: Ten sam kod działa; wystarczy zmienić rozszerzenie pliku w `srcFile` na `.dwg`.

**P: Czy mogę ustawić własne DPI dla PDF‑ów o wyższej rozdzielczości?**  
O: Tak, użyj `rasterizationOptions.setResolution(300);` (lub dowolnego wymaganego DPI).

**P: Czy istnieje możliwość osadzenia czcionek w generowanym PDF?**  
O: Aspose.CAD rasteryzuje rysunek, więc czcionki są renderowane jako wektory; osobne osadzanie czcionek nie jest wymagane.

## Podsumowanie

Korzystając z tego przewodnika, teraz wiesz, jak **ustawić niestandardowy rozmiar strony** i **tworzyć PDF z CAD** przy użyciu Aspose.CAD for Java z Auto Layout Scaling. Proces usprawnia **export CAD to PDF**, zapewnia spójne skalowanie i oszczędza cenny czas programistyczny. Śmiało eksperymentuj z różnymi rozmiarami stron, rozdzielczościami i formatami CAD, aby dopasować je do potrzeb projektu, niezależnie od tego, czy **konwertujesz DWG to PDF**, **zwiększasz rozdzielczość PDF**, czy tworzysz **java CAD to PDF** batch processor.

---

**Ostatnia aktualizacja:** 2026-02-15  
**Testowano z:** Aspose.CAD for Java 24.12 (najnowsza)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}