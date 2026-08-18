---
date: 2026-02-28
description: Dowiedz się, jak konwertować pliki DWG na PDF za pomocą Aspose.CAD dla
  Javy, tworząc szybko i dokładnie pliki zgodne z PDF/A1a i PDF/A1b.
linktitle: DWG to Compliance PDF
second_title: Aspose.CAD Java API
title: Konwertuj DWG na PDF (PDF/A1a i A1b) przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PDF (PDF/A1a i A1b) przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

We współczesnych przepływach pracy inżynierskiej i projektowej **konwersja DWG do PDF** jest codziennym wymogiem w zakresie udostępniania, archiwizacji i spełniania standardów dokumentów branżowych. PDF/A‑1a i PDF/A‑1b są najpowszechniej akceptowanymi standardami archiwizacji, gwarantującymi, że Twoje rysunki będą wyświetlane identycznie na każdym systemie. Aspose.CAD dla Javy sprawia, że ta konwersja jest prosta, niezawodna i w pełni programowalna. W tym samouczku dowiesz się dokładnie, jak konwertować pliki DWG do PDF‑ów zgodnych z PDF/A, używając zaledwie kilku linii kodu Java.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje konwersję?** Aspose.CAD for Java  
- **Jakie standardy PDF/A są obsługiwane?** PDF/A‑1a i PDF/A‑1b  
- **Czy potrzebna jest licencja do testów?** Tak – tymczasowa licencja jest dostępna od Aspose.  
- **Jaka jest minimalna wersja Javy?** Java 8 lub nowsza jest zalecana.  
- **Czy mogę przetwarzać wsadowo wiele plików DWG?** Absolutnie – powtórz kroki dla każdego pliku lub iteruj po folderze.

## Czym jest „konwersja DWG do PDF” i dlaczego ma znaczenie?
Konwersja rysunku DWG do PDF tworzy dokument uniwersalnie czytelny, zachowując przy tym wierność wektorów. Wybierając zgodność z PDF/A‑1a lub PDF/A‑1b, plik dodatkowo zawiera profile kolorów, czcionki i metadane niezbędne do długoterminowej archiwizacji, co jest kluczowe przy składaniu dokumentacji regulacyjnej, dokumentacji budowlanej i dostawach dla klientów.

## Dlaczego używać Aspose.CAD dla Javy?
- **Pełne wsparcie wersji DWG** – od starszych R12 po najnowsze wydania.  
- **Brak zewnętrznych zależności** – biblioteka działa od razu, nie wymaga oprogramowania CAD.  
- **Szczegółowa kontrola** – możesz ustawić opcje rasteryzacji, DPI, rozmiar strony i zgodność PDF/A.  
- **Wysoka wydajność** – odpowiednia do wsadowego przetwarzania tysięcy rysunków.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- Środowisko programistyczne Java (JDK 8 lub nowszy) z ulubionym IDE.  
- Bibliotekę Aspose.CAD for Java – pobierz ją z [download link](https://releases.aspose.com/cad/java/).  
- Folder zawierający rysunki DWG, które chcesz przekonwertować.

## Importowanie przestrzeni nazw

Najpierw zaimportuj klasy, których będziesz potrzebować. Trzymanie importów na początku pliku ułatwia czytanie i utrzymanie kodu.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Ustaw katalog zasobów

Zdefiniuj ścieżkę, w której znajdują się Twoje pliki DWG. Dostosuj łańcuch znaków, aby wskazywał na rzeczywisty katalog.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Krok 2: Załaduj plik DWG

Użyj `Image.load`, aby wczytać plik DWG do pamięci. Ten obiekt zostanie później zapisany jako PDF.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Krok 3: Utwórz opcje PDF

Utwórz instancję `PdfOptions` i dołącz obiekt `CadRasterizationOptions`. Opcje rasteryzacji pozwalają kontrolować, jak dane wektorowe są renderowane w PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Krok 4: Ustaw podstawowe opcje PDF (Zgodność)

Tutaj informujesz Aspose.CAD, jaki poziom zgodności PDF/A jest potrzebny. Przykład zaczyna się od PDF/A‑1a.

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Krok 5: Zapisz PDF z zgodnością PDF/A‑1a

Teraz zapisz plik PDF na dysku. Plik wyjściowy będzie zgodny z PDF/A‑1a, gotowy do archiwizacji.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Krok 6: Zmień zgodność na PDF/A‑1b i zapisz ponownie

Jeśli potrzebujesz PDF/A‑1b, po prostu zmień flagę zgodności i zapisz drugi plik.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

> **Pro tip:** Owiń logikę konwersji w metodę wielokrotnego użytku, aby móc wywoływać ją dla każdego DWG w folderze, redukując kod szablonowy i zwiększając łatwość utrzymania.

## Typowe przypadki użycia

| Scenariusz | Dlaczego PDF/A? |
|------------|-----------------|
| **Zgłoszenia regulacyjne** | Gwarantuje długoterminową czytelność i dopuszczalność prawną. |
| **Dostarczane klientowi** | Klienci mogą otworzyć plik bez potrzeby oprogramowania CAD. |
| **Systemy zarządzania dokumentami** | Pliki PDF/A są indeksowane i przeszukiwalne w większości platform DMS. |

## Typowe problemy i rozwiązania

- **Brakujące czcionki lub symbole** – Upewnij się, że plik DWG zawiera wszystkie wymagane czcionki, lub ustaw `CadRasterizationOptions.setEmbedFonts(true)`.  
- **Duży rozmiar pliku** – Zmniejsz DPI w opcjach rasteryzacji lub włącz kompresję za pomocą `PdfDocumentOptions.setCompress(true)`.  
- **Nie znaleziono licencji** – Zastosuj tymczasową lub stałą licencję przed konwersją; w przeciwnym razie otrzymasz znak wodny.

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
A: Aspose.CAD obsługuje szeroką gamę wersji DWG, w tym najnowsze wydania. Zobacz [documentation](https://reference.aspose.com/cad/java/) po szczegółową listę kompatybilności.

**Q: Czy mogę dostosować ustawienia wyjściowe PDF?**  
A: Absolutnie! Opcje takie jak rozmiar strony, DPI, rasteryzacja wektorowa i zgodność PDF/A są konfigurowalne poprzez `PdfOptions` i `CadRasterizationOptions`.

**Q: Czy tymczasowa licencja jest dostępna do testów?**  
A: Tak, możesz uzyskać tymczasową licencję do oceny z [this link](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę uzyskać wsparcie społeczności?**  
A: Forum [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to świetne miejsce na zadawanie pytań i dzielenie się doświadczeniami.

**Q: Czy mogę wypróbować Aspose.CAD za darmo przed zakupem?**  
A: Oczywiście! Pobierz wersję próbną za darmo z [here](https://releases.aspose.com/) i poznaj pełen zestaw funkcji.

---

**Ostatnia aktualizacja:** 2026-02-28  
**Testowano z:** Aspose.CAD for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}