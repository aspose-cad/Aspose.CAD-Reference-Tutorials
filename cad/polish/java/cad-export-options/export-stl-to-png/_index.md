---
date: 2026-02-20
description: Dowiedz się, jak konwertować STL na PNG przy użyciu Aspose.CAD dla Javy.
  Ten przewodnik krok po kroku pokazuje, jak efektywnie eksportować pliki STL.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Jak przekonwertować STL na PNG przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie STL do PNG przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

## Szybkie odpowiedzi
- **Co robi biblioteka?** Konwertuje formaty CAD (w tym STL) na obrazy rastrowe, takie jak PNG.  
- **Jakiego języka użyto?** Java, z API Aspose.CAD.  
- **Czy potrzebna jest licencja?** Tymczasowa lub pełna licencja jest wymagana do użytku produkcyjnego.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowej konwersji.  
- **Czy mogę dostosować rozmiar obrazu?** Tak, za pomocą `CadRasterizationOptions`.

## Co to jest konwersja STL do PNG?

Konwersja STL do PNG przekształca plik siatki 3‑D (STL) w dwuwymiarowy obraz rastrowy (PNG). Jest to przydatne, gdy potrzebny jest szybki podgląd wizualny, generowanie miniatur lub osadzenie modelu na stronach internetowych bez konieczności używania przeglądarki 3‑D.

## Dlaczego warto używać Aspose.CAD dla Javy?

- **Full‑featured API** – Obsługuje wiele formatów CAD, nie tylko STL.  
- **No external dependencies** – Czysta Java, łatwa do dodania do każdego projektu Maven/Gradle.  
- **High‑quality raster output** – Kontrola nad rozdzielczością, tłem i antyaliasingiem.  
- **Supports “how to export STL” scenarios** – Idealne do przetwarzania wsadowego lub konwersji w locie.

## Wymagania wstępne

- Zainstalowany Java Development Kit (JDK) na komputerze.  
- Biblioteka Aspose.CAD for Java pobrana. Możesz ją uzyskać [tutaj](https://releases.aspose.com/cad/java/).  
- Ważna licencja lub tymczasowa licencja z [tutaj](https://purchase.aspose.com/temporary-license/).

## Importowanie przestrzeni nazw

W swoim projekcie Java zaimportuj niezbędne klasy:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Teraz rozbijmy przykład na kilka kroków.

## Krok 1: Konfiguracja projektu

Utwórz nowy projekt Java i dodaj bibliotekę Aspose.CAD for Java do zależności projektu (Maven, Gradle lub ręczne dołączenie pliku JAR).

## Krok 2: Określenie pliku STL

Zdefiniuj ścieżkę do pliku STL, który chcesz skonwertować:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Krok 3: Wczytanie pliku STL

Wczytaj plik STL przy użyciu metody `Image.load`. Tworzy to obiekt **CAD image**, który możesz rasteryzować:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Krok 4: Konfiguracja opcji rasteryzacji

Skonfiguruj opcje rasteryzacji, aby kontrolować rozmiar i jakość wyjściowego pliku PNG. Opcje te są częścią procesu konwersji **cad image to png**:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Krok 5: Konfiguracja opcji PNG

Utwórz instancję `PngOptions`. Jeśli chcesz zastosować ustawienia rasteryzacji, odkomentuj poniższą linię:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Krok 6: Zapisz jako PNG

Na koniec wyeksportuj obraz CAD do pliku PNG — to jest krok **save PNG Java**:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **Wskazówka:** Dostosuj `PageWidth` i `PageHeight`, aby odpowiadały żądanym wymiarom miniatury, co przyspieszy przetwarzanie.

Gratulacje! Pomyślnie **przekonwertowałeś plik STL na PNG** przy użyciu Aspose.CAD for Java.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| Pusty obraz PNG | Nie ustawiono opcji rasteryzacji | Odkomentuj `pngOptions.setVectorRasterizationOptions(vectorOptions);` lub określ kolor tła |
| OutOfMemoryError przy dużych plikach STL | Niewystarczająca pamięć sterty | Zwiększ pamięć sterty JVM (`-Xmx2g`) lub przetwarzaj plik w fragmentach |
| LicenseException | Brak ważnej licencji | Zastosuj tymczasową lub zakupioną licencję przed wczytaniem obrazu |

## Najczęściej zadawane pytania

### Q1: Czy Aspose.CAD for Java jest kompatybilny ze wszystkimi wersjami plików STL?
A1: Aspose.CAD for Java obsługuje różne wersje plików STL, zapewniając kompatybilność z większością popularnych formatów.

### Q2: Czy mogę używać Aspose.CAD for Java w projekcie komercyjnym?
A2: Tak, możesz. Po prostu uzyskaj ważną licencję z [tutaj](https://purchase.aspose.com/buy).

### Q3: Czy potrzebna jest tymczasowa licencja do wersji próbnej?
A3: Nie, tymczasowa licencja nie jest wymagana dla wersji próbnej. Możesz od razu rozpocząć pracę z wersją próbną [tutaj](https://releases.aspose.com/).

### Q4: Gdzie mogę znaleźć dodatkowe wsparcie lub zadać pytania?
A4: Odwiedź forum Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia lub zapytań.

### Q5: Czy dostępna jest pełna dokumentacja?
A5: Tak, dokumentację można znaleźć [tutaj](https://reference.aspose.com/cad/java/).

## Podsumowanie

W tym przewodniku pokazaliśmy, jak efektywnie **konwertować STL na PNG** przy użyciu Aspose.CAD for Java. Postępując zgodnie z powyższymi krokami, możesz zintegrować konwersję STL‑do‑PNG w dowolnym potoku opartym na Javie, niezależnie od tego, czy tworzysz narzędzie desktopowe, usługę internetową, czy zautomatyzowane narzędzie raportujące.

---

**Ostatnia aktualizacja:** 2026-02-20  
**Testowano z:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}