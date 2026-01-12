---
date: 2026-01-12
description: Naucz się eksportować pliki DWG jako PDF przy użyciu Javy i Aspose.CAD.
  Przewodnik krok po kroku, jak konwertować DWG na PDF, dostosować rozdzielczość wyjściową
  i zapisać DWG jako obraz.
linktitle: Convert Particular DWG to PDF Using Java
second_title: Aspose.CAD Java API
title: dwg do pdf java – Konwertuj konkretny plik DWG do PDF przy użyciu Javy
url: /pl/java/dwg-file-operations/convert-dwg-to-image/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# dwg to pdf java – Konwersja konkretnego DWG do PDF przy użyciu Java

## Wprowadzenie

W nowoczesnych przepływach pracy architektonicznej i inżynieryjnej konwersja rysunku DWG do dokumentu PDF jest częstym wymogiem — zarówno w celu przeglądu przez klienta, dokumentacji, jak i archiwizacji. Korzystając z **Aspose.CAD for Java**, możesz programowo eksportować DWG jako PDF, dostosowywać rozdzielczość wyjścia i nawet filtrować określone encje przed renderowaniem. W tym samouczku przeprowadzimy Cię krok po kroku przez cały proces konwersji **dwg to pdf java**, abyś mógł go już dziś zintegrować ze swoimi aplikacjami Java.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje konwersję?** Aspose.CAD for Java.  
- **Czy mogę ustawić rozdzielczość obrazu?** Tak – użyj `CadRasterizationOptions`, aby określić szerokość i wysokość.  
- **Czy można filtrować encje (np. zachować tylko tekst)?** Absolutnie; możesz usunąć niechciane encje przed zapisem.  
- **Jaki format wyjściowy generuje przykład?** Plik PDF, ale te same opcje rasteryzacji działają dla PNG, JPEG itp.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest licencja komercyjna dla wdrożeń nie‑ewaluacyjnych.

## Co to jest dwg to pdf java?
`dwg to pdf java` odnosi się do programistycznej konwersji plików AutoCAD DWG na dokumenty PDF przy użyciu kodu Java. Takie podejście eliminuje ręczne kroki eksportu, umożliwia przetwarzanie wsadowe i daje pełną kontrolę nad opcjami renderowania, takimi jak rozmiar strony, skalowanie i widoczność encji.

## Dlaczego warto używać Aspose.CAD for Java?
- **Brak wymogu instalacji AutoCAD** – biblioteka obsługuje parsowanie DWG wewnętrznie.  
- **Renderowanie o wysokiej wierności** – dane wektorowe są zachowane, a tekst pozostaje możliwy do zaznaczenia.  
- **Precyzyjna kontrola** – możesz filtrować encje, ustawiać własne DPI i wybierać formaty rastrowe.  
- **Wieloplatformowość** – działa na każdym systemie operacyjnym obsługującym Java.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz następujące elementy:

1. **Java Development Kit (JDK)** – kompatybilny JDK zainstalowany na twoim komputerze. Najnowszy JDK możesz pobrać z [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Biblioteka Aspose.CAD for Java** – pobierz bibliotekę ze [strony pobierania Aspose.CAD](https://releases.aspose.com/cad/java/).  
3. **IDE według wyboru** – IntelliJ IDEA, Eclipse lub dowolne inne IDE Java, które preferujesz.

## Importowanie pakietów

W swoim projekcie Java zaimportuj niezbędne pakiety Aspose.CAD, aby zapewnić płynną integrację. Dołącz następujący kod do swojego projektu:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Collection;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;
```

## Przewodnik krok po kroku

### Krok 1: Skonfiguruj projekt
Dodaj plik JAR Aspose.CAD do ścieżki klas swojego projektu i zweryfikuj, czy JDK jest poprawnie skonfigurowany w IDE. Dzięki temu klasy `Image` i `CadImage` będą dostępne w czasie kompilacji.

### Krok 2: Określ ścieżkę do pliku DWG
Zdefiniuj lokalizację pliku DWG, który chcesz skonwertować. Zaktualizuj zmienne `dataDir` i `sourceFilePath`, aby wskazywały na własny katalog.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String sourceFilePath = dataDir + "visualization_-_conference_room.dwg";
```

### Krok 3: Filtrowanie encji tekstowych (opcjonalnie)
Jeśli potrzebujesz tylko niektórych encji — na przykład adnotacji tekstowych — możesz je odfiltrować przed renderowaniem. Poniższy kod iteruje po wszystkich encjach DWG, zachowuje tylko te typu `TEXT`, a resztę odrzuca.

```java
CadImage cadImage = (CadImage) (Image.load(sourceFilePath));
CadBaseEntity[] entities = cadImage.getEntities();
List<CadBaseEntity> filteredEntities = new ArrayList<>();
for (CadBaseEntity baseEntity : entities) {
    if ((baseEntity.getTypeName() == CadEntityTypeName.TEXT)) {
        filteredEntities.add(baseEntity);
    }
}
CadBaseEntity[] arr = new CadBaseEntity[filteredEntities.size()];
cadImage.setEntities(filteredEntities.toArray(arr));
```

### Krok 4: Ustaw opcje rasteryzacji – Dostosuj rozdzielczość wyjściową
Utwórz instancję `CadRasterizationOptions` i skonfiguruj jej właściwości. Dostosuj `pageWidth` i `pageHeight`, aby kontrolować rozdzielczość generowanego PDF (lub innego formatu rastrowego).

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Krok 5: Eksport do PDF – Ostateczny zapis
Umieść opcje rasteryzacji w obiekcie `PdfOptions` i zapisz wynik. Plik wyjściowy będzie PDF‑em odzwierciedlającym przefiltrowane encje oraz ustawioną przez Ciebie rozdzielczość.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
String outFile = dataDir + "result_out_generated.pdf";
cadImage.save(outFile, pdfOptions);
```

> **Wskazówka:** Jeśli potrzebujesz innego formatu obrazu (PNG, JPEG, TIFF), zamień `PdfOptions` na odpowiednią klasę opcji obrazu, zachowując te same ustawienia rasteryzacji.

Gratulacje! Pomyślnie przeprowadziłeś konwersję **dwg to pdf java** przy użyciu Aspose.CAD for Java.

## Typowe problemy i rozwiązania

| Problem | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------------------|-------------|
| **Pusty PDF** | Plik DWG nie został poprawnie załadowany (nieprawidłowa ścieżka) | Sprawdź, czy `sourceFilePath` wskazuje istniejący plik DWG. |
| **Brak tekstu** | Logika filtrowania usunęła potrzebne encje | Dostosuj warunek `if` lub pomiń filtrowanie, jeśli chcesz wszystkie encje. |
| **Niska rozdzielczość** | `pageWidth`/`pageHeight` za małe | Zwiększ wartości; 1600 × 1600 to dobry punkt wyjścia dla wysokiej jakości PDF. |
| **OutOfMemoryError** przy dużych plikach DWG | Niewystarczająca pamięć sterty | Uruchom JVM z większą pamięcią sterty (`-Xmx2g` lub więcej). |

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
A: Tak, Aspose.CAD obsługuje szeroką gamę wersji DWG, od wczesnych wydań po najnowsze formaty AutoCAD.

**Q: Czy mogę dostosować rozdzielczość wyjściowego obrazu?**  
A: Absolutnie. Użyj `CadRasterizationOptions.setPageWidth()` i `setPageHeight()`, aby określić pożądane DPI lub wymiary w pikselach.

**Q: Czy konwersja wsadowa jest możliwa?**  
A: Tak. Umieść logikę konwersji w pętli, która iteruje po kolekcji ścieżek do plików DWG.

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?**  
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc od społeczności i inżynierów Aspose.

**Q: Czy mogę wypróbować Aspose.CAD przed zakupem?**  
A: Tak, wypróbuj narzędzie w ramach darmowej wersji próbnej dostępnej pod [tym linkiem](https://releases.aspose.com/).

## Zakończenie

Eksportowanie DWG jako PDF w Java jest proste dzięki Aspose.CAD. Postępując zgodnie z powyższymi krokami, możesz **eksportować dwg jako pdf**, **zapisować dwg jako obraz** i **dostosowywać rozdzielczość wyjścia**, aby spełnić dokładne wymagania swojego projektu. Zintegruj ten przepływ pracy z automatycznymi pipeline’ami, aby zwiększyć wydajność i zapewnić spójną, wysokiej jakości dokumentację.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-12  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

---