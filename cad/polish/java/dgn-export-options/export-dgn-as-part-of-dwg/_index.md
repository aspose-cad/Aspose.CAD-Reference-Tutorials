---
date: 2026-01-10
description: Dowiedz się, jak wyeksportować DGN do DWG i przekonwertować MicroStation
  DGN na AutoCAD DWG przy użyciu Aspose.CAD dla Javy. Przewodnik krok po kroku.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Eksport DGN do DWG z Aspose.CAD dla Javy
url: /pl/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport DGN do DWG przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

W tym samouczku dowiesz się, jak **export dgn to dwg** i osadzić projekt MicroStation DGN wewnątrz pliku AutoCAD DWG przy użyciu biblioteki Aspose.CAD dla Javy. Niezależnie od tego, czy migrujesz starsze rysunki MicroStation, czy potrzebujesz połączyć podkłady DGN z układami DWG, ten przewodnik przeprowadzi Cię przez każdy krok — od konfiguracji środowiska po wygenerowanie podglądu PDF końcowego pliku DWG.

## Szybkie odpowiedzi
- **Co osiąga „export dgn to dwg”?** Osadza podkład DGN w DWG, umożliwiając płynne przeglądanie w AutoCAD.
- **Do jakiego formatu mogę wyeksportować wynik w celu szybkiego podglądu?** Możesz **export cad file to pdf** używając `PdfOptions`.
- **Czy potrzebna jest licencja do uruchomienia kodu?** Wymagana jest tymczasowa lub płatna licencja Aspose.CAD do użytku produkcyjnego.
- **Jaką wersję Javy obsługuje?** Java 8 lub nowsza działa z najnowszą wersją Aspose.CAD dla Javy.
- **Czy dostępna jest darmowa wersja próbna?** Tak — pobierz wersję próbną ze strony Aspose.

## Co to jest „export dgn to dwg”?

Eksportowanie DGN do DWG oznacza konwersję lub osadzenie projektu MicroStation DGN jako podkładu wewnątrz rysunku AutoCAD DWG. Pozwala to specjalistom CAD wykorzystać istniejące zasoby DGN bez konieczności od nowa tworzenia geometrii.

## Dlaczego konwertować MicroStation DGN na AutoCAD DWG?
- **Współpraca:** Zespoły korzystające z AutoCAD mogą bezpośrednio przeglądać i edytować zawartość DGN.
- **Standaryzacja:** DWG jest de facto formatem dla wielu dalszych procesów (np. generowanie PDF, renderowanie 3D).
- **Zachowanie:** Utrzymuje oryginalne odniesienia DGN, zmniejszając utratę danych.

## Wymagania wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania:
1. **Biblioteka Aspose.CAD:** Pobierz i zainstaluj bibliotekę Aspose.CAD dla Javy. Bibliotekę znajdziesz [tutaj](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Upewnij się, że masz zainstalowaną Javę w systemie.
3. **Zintegrowane Środowisko Programistyczne (IDE):** Wybierz IDE Java, takie jak Eclipse lub IntelliJ, aby uzyskać płynniejsze doświadczenie programistyczne.

## Importowanie pakietów

W swoim projekcie Java zaimportuj niezbędne pakiety Aspose.CAD, aby umożliwić manipulację plikami CAD. Oto przykład:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Krok 1: Ustaw ścieżki plików

Zdefiniuj ścieżki wejściowe i wyjściowe dla pliku DWG. Zaktualizuj zmienne `dataDir`, `fileName` i `outPath` odpowiednio.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Krok 2: Utwórz instancję PdfOptions

Utwórz instancję klasy `PdfOptions`, ponieważ **export cad file to pdf** w celu szybkiej weryfikacji.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Krok 3: Załaduj plik DWG

Załaduj istniejący plik DWG jako obraz i przekonwertuj go na typ `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Krok 4: Iteruj przez encje

Przejdź przez każdą encję w pliku DWG i sprawdź, czy jest definicją obrazu. Jeśli tak, pobierz zewnętrzne odniesienie do obiektu.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Krok 5: Zdefiniuj opcje rasteryzacji

Zdefiniuj ustawienia dla obiektu `CadRasterizationOptions`, w tym szerokość i wysokość strony, układy oraz kolor tła.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Krok 6: Ustaw opcje rasteryzacji wektorowej

Ustaw opcje rasteryzacji wektorowej dla eksportu.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Krok 7: Eksportuj DWG do PDF

Na koniec wyeksportuj DWG do PDF, wywołując metodę `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| **Brak podkładu DGN** | Plik DWG nie zawiera encji `DGNUNDERLAY`. | Zweryfikuj, że źródłowy DWG zawiera odniesienie DGN. |
| **PDF jest pusty** | Opcje rasteryzacji ustawione na zerowy rozmiar lub niewłaściwy układ. | Upewnij się, że `setPageWidth`/`setPageHeight` są dodatnie, a `setLayouts` odpowiada nazwie układu DWG. |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji Aspose.CAD. | Zastosuj tymczasową lub zakupioną licencję przed wywołaniem jakichkolwiek metod API. |

## Często zadawane pytania

### Q1: Gdzie mogę znaleźć dokumentację Aspose.CAD dla Javy?

Dokumentację można znaleźć [tutaj](https://reference.aspose.com/cad/java/).

### Q2: Jak mogę pobrać bibliotekę Aspose.CAD dla Javy?

Bibliotekę możesz pobrać z [tego linku](https://releases.aspose.com/cad/java/).

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Javy?

Tak, darmową wersję próbną znajdziesz [tutaj](https://releases.aspose.com/).

### Q4: Gdzie mogę uzyskać tymczasową licencję Aspose.CAD dla Javy?

Uzyskaj tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/).

### Q5: Potrzebujesz pomocy lub masz pytania?

Odwiedź forum wsparcia społeczności Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19).

### Q6: Czy mogę przekonwertować otrzymany PDF z powrotem do DWG?

PDF jest podglądem rastrowym; konwersja z powrotem do DWG wymaga osobnego narzędzia do inżynierii odwrotnej.

### Q7: Czy to podejście działa z innymi formatami CAD, takimi jak DWF lub DXF?

Tak, Aspose.CAD obsługuje wiele formatów; wystarczy odpowiednio dostosować rozszerzenia plików i ustawienia rasteryzacji.

---

**Ostatnia aktualizacja:** 2026-01-10  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}