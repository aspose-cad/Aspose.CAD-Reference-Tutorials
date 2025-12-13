---
date: 2025-12-13
description: Dowiedz się, jak zapisać plik CAD jako JPEG w Javie przy użyciu Aspose.CAD,
  dodać wiele warstw oraz dostosować wymiary CAD dla precyzyjnej konwersji obrazu.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Zapisz CAD jako JPEG z obsługą warstw w Javie
url: /pl/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz CAD jako JPEG z obsługą warstw w Javie

## Wprowadzenie

W tym samouczku dowiesz się, jak **zapisz CAD jako JPEG** wykorzystując pełną obsługę warstw w Aspose.CAD for Java. Warstwy pozwalają izolować konkretne części rysunku, co ułatwia eksportowanie tylko tego, co jest potrzebne. Przejdziemy przez każdy krok, od konfiguracji środowiska po eksport JPEG zawierającego wyłącznie wybrane warstwy.

## Szybkie odpowiedzi
- **Co oznacza „save CAD as JPEG”?** Konwertuje rysunek CAD na rastrowy obraz JPEG.
- **Czy mogę uwzględnić tylko wybrane warstwy?** Tak – użyj metody `setLayers`, aby określić, które warstwy mają być renderowane.
- **Jak zmienić rozmiar obrazu?** Dostosuj `setPageWidth` i `setPageHeight` w `CadRasterizationOptions`.
- **Czy jest to rozwiązanie wyłącznie dla Javy?** Przykład używa Aspose.CAD for Java, ale te same koncepcje mają zastosowanie w innych językach.
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.

## Wymagania wstępne

Zanim zanurzysz się w temat, upewnij się, że masz następujące:

1. **Aspose.CAD for Java Library** – pobierz ją ze [strony internetowej](https://releases.aspose.com/cad/java/). Postępuj zgodnie z przewodnikiem instalacji, aby dodać pliki JAR do classpathu projektu.  
2. **Java Development Environment** – zainstalowane na komputerze aktualne JDK (8 lub nowsze).

Teraz, gdy wszystko jest gotowe, przyjrzyjmy się kodowi potrzebnemu do **zapisz CAD jako JPEG** z selektywnym renderowaniem warstw.

## Importowanie przestrzeni nazw

Rozpocznij od zaimportowania wymaganych klas Aspose.CAD oraz standardowych narzędzi Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw ścieżki plików

Zdefiniuj, gdzie znajduje się źródłowy plik DWF oraz gdzie zostanie zapisany wyjściowy plik JPEG.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Krok 2: Załaduj obraz DWF

Użyj metody `Image.load` z Aspose.CAD, aby odczytać rysunek CAD.

```java
Image image = Image.load(srcFile);
```

### Krok 3: Skonfiguruj opcje rasteryzacji (Dostosuj wymiary CAD)

Utwórz instancję `CadRasterizationOptions` i ustaw pożądany rozmiar wyjścia. Zmiana tych wartości pozwala **dostosować wymiary CAD** dla ostatecznego JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Krok 4: Określ warstwy (Dodaj wiele warstw)

Jeśli chcesz renderować więcej niż jedną warstwę, po prostu dodaj ich nazwy do listy. Tutaj zaczynamy od pojedynczej warstwy o nazwie „LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Wskazówka:* Aby **dodać wiele warstw**, rozwiń wywołanie `Arrays.asList`, np. `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Krok 5: Skonfiguruj opcje JPEG (Java Convert CAD Image)

Połącz ustawienia rasteryzacji z formatem wyjściowym JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 6: Eksportuj do JPG (Save CAD as JPEG)

Na koniec zapisz obraz na dysku. Ten krok **zapisuje rysunek CAD jako plik JPEG**, który zawiera tylko wybrane warstwy.

```java
image.save(outFile, jpegOptions);
```

Postępując zgodnie z tymi krokami, pomyślnie **zapisano CAD jako JPEG**, kontrolując, które warstwy się pojawiają i dostosowując wymiary obrazu.

## Częste problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Warstwy nie pojawiają się** | Sprawdź, czy nazwy warstw dokładnie odpowiadają tym zapisanym w pliku DWF (uwzględniając wielkość liter). |
| **Wyjściowy obraz jest pusty** | Upewnij się, że `setPageWidth` i `setPageHeight` są wystarczająco duże dla wymiarów rysunku. |
| **Wyjątek licencyjny** | Użyj licencji próbnej do testów; uzyskaj pełną licencję w środowisku produkcyjnym. |

## Najczęściej zadawane pytania

**Q: Czy mogę dodać wiele warstw do opcji rasteryzacji?**  
A: Oczywiście. Rozszerz `stringList` o dodatkowe nazwy warstw, np. `Arrays.asList("LayerA", "LayerB")`.

**Q: Czy Aspose.CAD jest kompatybilny z innymi formatami CAD?**  
A: Tak, obsługuje DWG, DXF, DWF i wiele innych formatów.

**Q: Jak mogę zmienić wymiary wyjściowego obrazu?**  
A: Zmień `setPageWidth` i `setPageHeight` w instancji `CadRasterizationOptions`.

**Q: Gdzie mogę kupić licencję na Aspose.CAD?**  
A: Opcje licencjonowania możesz przeglądać [tutaj](https://purchase.aspose.com/buy).

**Q: Gdzie mogę uzyskać wsparcie społeczności?**  
A: Dołącz do społeczności Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i dyskusje.

---

**Ostatnia aktualizacja:** 2025-12-13  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}