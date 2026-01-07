---
date: 2026-01-07
description: Dowiedz się, jak wyeksportować CAD do PDF i przekonwertować DGN na PDF
  przy użyciu Aspose.CAD dla Javy. Przewodnik krok po kroku dla programistów Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Eksport CAD do PDF – Eksport osadzonego DGN z Aspose.CAD dla Javy
url: /pl/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD do PDF – Eksport osadzonego DGN przy użyciu Aspose.CAD for Java

## Wprowadzenie

W tym samouczku odkryjesz **jak wyeksportować CAD do PDF** poprzez konwersję osadzonego pliku DGN do wysokiej jakości dokumentu PDF przy użyciu Aspose.CAD for Java. Aspose.CAD to solidna biblioteka, która daje programistom Java pełną kontrolę nad manipulacją plikami CAD, niezależnie od tego, czy musisz **konwertować DGN do PDF**, **konwertować DWG do PDF**, czy po prostu renderować rysunki CAD w innych formatach. Postępuj zgodnie z poniższym przewodnikiem krok po kroku, a w kilka minut będziesz mógł zintegrować tę funkcjonalność ze swoimi aplikacjami.

## Szybkie odpowiedzi
- **Co oznacza „export CAD to PDF”?** Konwertuje rysunki CAD (DWG, DGN itp.) na pliki PDF zachowując jakość wektorową.  
- **Jakiej biblioteki użyto?** Aspose.CAD for Java.  
- **Czy potrzebna jest licencja?** Licencja jest wymagana w środowisku produkcyjnym; dostępna jest darmowa wersja próbna.  
- **Jakie są główne wymagania wstępne?** Środowisko programistyczne Java oraz plik JAR Aspose.CAD for Java.  
- **Czy mogę dostosować wynik?** Tak – możesz wybrać układy, ustawić opcje rasteryzacji i kontrolować ustawienia PDF.

## Co to jest „export CAD to PDF”?
Eksportowanie CAD do PDF oznacza wzięcie natywnego pliku CAD (takiego jak DWG lub DGN) i wygenerowanie dokumentu PDF, który wiernie odzwierciedla oryginalną geometrię. PDF można przeglądać na dowolnej platformie bez potrzeby posiadania oprogramowania CAD, co czyni go idealnym do udostępniania, drukowania lub archiwizacji.

## Dlaczego używać Aspose.CAD for Java do konwersji DGN do PDF?
- **Brak zewnętrznych zależności** – działa wyłącznie w Javie.  
- **Zachowuje dane wektorowe** – PDF-y pozostają wyraźne przy dowolnym poziomie powiększenia.  
- **Precyzyjna kontrola** – wybierz konkretne układy, ustaw DPI rasteryzacji i osadź czcionki.  
- **Gotowe dla przedsiębiorstw** – obsługuje duże pliki, przetwarzanie wsadowe i opcje licencjonowania.

## Wymagania wstępne

Zanim przejdziesz dalej, upewnij się, że masz następujące elementy:

- **Środowisko programistyczne Java** – zainstalowany i skonfigurowany JDK 8 lub nowszy.  
- **Aspose.CAD for Java** – pobierz najnowszy plik JAR z [tutaj](https://releases.aspose.com/cad/java/).  

## Importowanie pakietów

Aby rozpocząć, musisz zaimportować niezbędne klasy w swoim projekcie Java. Dodaj następujące instrukcje importu do pliku źródłowego:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak wyeksportować DGN do PDF przy użyciu Aspose.CAD for Java?

Poniżej znajduje się przejrzysty, numerowany przewodnik, który pokazuje dokładnie, jak przekonwertować osadzony plik DGN (przechowywany wewnątrz DWG) do PDF.

### Krok 1: Ustaw ścieżki wejściowe i wyjściowe

Zdefiniuj katalog zawierający plik źródłowy i określ DWG, w którym znajduje się osadzony DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Krok 2: Załaduj plik DWG

Załaduj plik DWG do obiektu `Image`. Aspose.CAD automatycznie wykrywa osadzone dane DGN.

```java
Image objImage = Image.load(fileName);
```

### Krok 3: Skonfiguruj opcje rasteryzacji

Wybierz, które układy chcesz uwzględnić w PDF. W tym przykładzie eksportujemy tylko układ **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Krok 4: Skonfiguruj opcje PDF

Dołącz ustawienia rasteryzacji do opcji eksportu PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Zapisz plik PDF

Na koniec zapisz PDF na dysku, używając skonfigurowanych opcji.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Konwersja DWG do PDF – dodatkowa wskazówka

Jeśli Twój plik źródłowy jest zwykłym DWG (bez osadzonego DGN), możesz ponownie użyć tego samego kodu – po prostu zmień `fileName`, aby wskazywał na DWG, który chcesz przekonwertować. Opcje rasteryzacji i PDF pozostają identyczne, zapewniając spójny **workflow konwersji DWG do PDF**.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| **Pusty plik PDF** | Niezgodność nazwy układu | Sprawdź, czy nazwa układu przekazana do `setLayouts` dokładnie odpowiada nazwie układu w pliku źródłowym (uwzględniając wielkość liter). |
| **Wyjątek licencyjny** | Używanie wersji próbnej bez licencji | Zastosuj ważną licencję Aspose.CAD przed załadowaniem obrazu (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Plik nie znaleziony** | Niepoprawna ścieżka `dataDir` | Użyj ścieżki bezwzględnej lub upewnij się, że ścieżka względna jest poprawna względem katalogu roboczego projektu. |
| **Grafika o niskiej rozdzielczości** | Domyślne DPI rasteryzacji jest niskie | Ustaw `rasterizationOptions.setPageWidth/Height` lub `setResolution`, aby zwiększyć DPI. |

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD for Java w projekcie komercyjnym?**  
O: Tak, Aspose.CAD for Java jest biblioteką komercyjną. Licencję można uzyskać [tutaj](https://purchase.aspose.com/buy).

**P: Czy dostępna jest darmowa wersja próbna?**  
O: Tak, darmową wersję próbną Aspose.CAD for Java można uzyskać [tutaj](https://releases.aspose.com/).

**P: Jak mogę uzyskać wsparcie dla Aspose.CAD for Java?**  
O: Wsparcie można uzyskać w społeczności Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19).

**P: Co zrobić, jeśli potrzebuję tymczasowej licencji?**  
O: Tymczasową licencję można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**P: Gdzie mogę znaleźć dokumentację?**  
O: Dokumentacja jest dostępna [tutaj](https://reference.aspose.com/cad/java/).

## Podsumowanie

Nauczyłeś się teraz, **jak wyeksportować CAD do PDF**, w szczególności **jak konwertować DGN do PDF** oraz **jak konwertować DWG do PDF** przy użyciu Aspose.CAD for Java. Postępując zgodnie z powyższymi krokami, możesz zintegrować płynną konwersję CAD‑do‑PDF w dowolnym rozwiązaniu opartym na Javie, dostarczając użytkownikom wysokiej jakości pliki PDF bez konieczności dodatkowego oprogramowania CAD.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-07  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose