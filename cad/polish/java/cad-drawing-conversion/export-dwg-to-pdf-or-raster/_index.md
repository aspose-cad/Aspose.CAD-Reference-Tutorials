---
date: 2026-02-17
description: Dowiedz się, jak biblioteka Java CAD Aspose.CAD for Java może szybko
  i dokładnie eksportować pliki DWG do formatu PDF lub obrazów rastrowych.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Eksportuj DWG do PDF lub formatu rastrowego przy użyciu biblioteki Java CAD
  Aspose.CAD.
url: /pl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie DWG do PDF lub obrazu rastrowego przy użyciu biblioteki Java CAD Aspose.CAD for Java

## Wprowadzenie

W dynamicznym świecie projektowania wspomaganego komputerowo (CAD) efektywne zarządzanie rysunkami ma kluczowe znaczenie. Dzięki **bibliotece java cad** **Aspose.CAD for Java** możesz **eksportować dwg do pdf** — lub obrazy rastrowe — w zaledwie kilku linijkach kodu. Ten samouczek przeprowadzi Cię przez cały proces, od wczytania pliku DWG po wygenerowanie wysokiej jakości PDF, podkreślając, dlaczego Aspose.CAD Java jest najczęściej wybieraną biblioteką do zadań konwersji CAD.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Eksportowanie plików DWG do PDF lub obrazów rastrowych przy użyciu Aspose.CAD for Java.  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa licencja tymczasowa do oceny; pełna licencja jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Każde środowisko Java 8+ działa z najnowszym API Aspose.CAD Java.  
- **Czy mogę konwertować DWG do innych formatów obrazów?** Tak – te same opcje rasteryzacji umożliwiają wyjście w formatach PNG, JPEG, BMP itp.  
- **Jak długo trwa konwersja?** Zazwyczaj poniżej sekundy dla standardowych rysunków; większe pliki mogą wymagać kilku sekund.

## Dlaczego biblioteka java cad jest najlepszym wyborem do konwersji DWG?

- **Czysta implementacja w Javie** – bez natywnych DLL‑ów czy zewnętrznych narzędzi.  
- **Precyzyjna obsługa jednostek** – jednostki metryczne i imperialne są wykrywane automatycznie.  
- **Wysokiej jakości wyjście rastrowe** – precyzyjnie dostosowane DPI i kontrola rozmiaru strony.  
- **Pełne wsparcie PDF** – generowanie PDF zachowującego wektory bez dodatkowych zależności.  
- **Elastyczna licencjonowanie** – rozpocznij od **tymczasowej licencji aspose** do testów, a następnie przejdź na pełną wersję przy wdrożeniu.

## Co to jest „export dwg to pdf”?

Eksportowanie DWG do PDF oznacza konwersję natywnego rysunku AutoCAD do przenośnego, niezależnego od urządzenia dokumentu PDF. Powstały PDF zachowuje dane wektorowe, warstwy i skalowanie, co czyni go idealnym do udostępniania, drukowania lub archiwizacji.

## Dlaczego warto używać Aspose.CAD Java do tej konwersji?

Ponieważ **biblioteka java cad** obsługuje wszystko – od konwersji jednostek po rasteryzację – wewnętrznie, unikając złożoności narzędzi firm trzecich i zapewniając spójne wyniki na wszystkich platformach.

## Wymagania wstępne

Zanim przejdziesz do kodu, upewnij się, że masz:

- Podstawową znajomość programowania w Javie.  
- Zainstalowaną bibliotekę Aspose.CAD for Java. Jeśli jeszcze jej nie pobrałeś, pobierz ją **[tutaj](https://releases.aspose.com/cad/java/)**.  
- Plik DWG do testów – w tym przewodniku używany jest przykładowy **Bottom_plate.dwg**.

## Importowanie przestrzeni nazw

W swoim projekcie Java zaimportuj niezbędne klasy, aby rozpocząć konwersję:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Przewodnik krok po kroku

### Krok 1: Wczytaj plik DWG

Najpierw wczytaj rysunek DWG przy użyciu klasy `Image`. Tworzy to reprezentację w pamięci, z którą Aspose.CAD może pracować.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Krok 2: Określ typ jednostki

Zrozumienie, czy rysunek używa jednostek metrycznych czy imperialnych, jest niezbędne do prawidłowego skalowania. Metoda pomocnicza `IsMetric` (implementacja pominięta dla zwięzłości) zwraca wartość boolowską.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Krok 3: Ustaw opcje rasteryzacji

W zależności od systemu jednostek skonfiguruj rozmiar strony, skalowanie oraz docelowy typ jednostki. Te opcje określają, jak DWG zostanie rasteryzowany przed umieszczeniem w PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Krok 4: Skonfiguruj opcje PDF (pdf options cad)

Utwórz instancję `PdfOptions` i dołącz ustawienia rasteryzacji. Dzięki temu Aspose.CAD wie, jak osadzić rasteryzowaną treść w finalnym PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Krok 5: Zapisz jako PDF

Na koniec wyeksportuj rysunek do pliku PDF. Metoda `save` przyjmuje ścieżkę wyjściową oraz skonfigurowane `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Po zakończeniu działania kodu znajdziesz **Saved.pdf** w folderze `DWGDrawings`, gotowy do dystrybucji lub archiwizacji.

## Jak konwertować obrazy rastrowe DWG przy użyciu biblioteki java cad

Jeśli potrzebujesz obrazów rastrowych zamiast PDF, po prostu zamień `PdfOptions` na odpowiednie opcje obrazu rastrowego (np. `PngOptions`, `JpegOptions`). Ta sama instancja `CadRasterizationOptions` może być ponownie użyta, co pozwala **konwertować dwg raster** przy minimalnych zmianach kodu.

## Jak generować PDF DWG przy użyciu pdf options cad

Powyższy przykład już **generuje pdf dwg**. Modyfikując `pdfOptions`—na przykład ustawiając `pdfOptions.setCompress(true)`—możesz kontrolować rozmiar i jakość PDF. To pokazuje elastyczność API **pdf options cad**.

## Typowe problemy i wskazówki

- **Nieprawidłowy rozmiar strony** – Sprawdź logikę konwersji jednostek; niepasujące współczynniki mogą powodować zbyt duże strony.  
- **Brak czcionek lub grubości linii** – Upewnij się, że DWG odwołuje się do wszystkich zewnętrznych zasobów przed konwersją.  
- **Wydajność przy dużych rysunkach** – Zwiększaj ustawienie `DPI` w `CadRasterizationOptions` tylko wtedy, gdy wymagana jest wyższa jakość; niższe DPI przyspiesza przetwarzanie.  
- **Kwestie licencyjne** – Do oceny możesz użyć **tymczasowej licencji aspose**; pełna licencja jest wymagana w środowisku produkcyjnym.

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD for Java z innymi frameworkami Java?**  
O: Tak, Aspose.CAD for Java bezproblemowo integruje się z popularnymi frameworkami Java, takimi jak Spring, Jakarta EE i Android.

**P: Czy dostępna jest tymczasowa licencja dla Aspose.CAD for Java?**  
O: Tak, tymczasową licencję możesz uzyskać **[tutaj](https://purchase.aspose.com/temporary-license/)**.

**P: Gdzie mogę uzyskać wsparcie dla Aspose.CAD for Java?**  
O: Odwiedź **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**, aby uzyskać pomoc od społeczności i inżynierów Aspose.

**P: Jak mogę kupić licencję na Aspose.CAD for Java?**  
O: Licencję możesz zakupić **[tutaj](https://purchase.aspose.com/buy)**.

**P: Jakie jednostki obsługuje Aspose.CAD for Java?**  
O: Aspose.CAD for Java obsługuje zarówno jednostki metryczne, jak i imperialne, automatycznie wykrywając system jednostek rysunku.

**P: Czy mogę konwertować DWG do innych formatów obrazów (np. PNG, JPEG) przy użyciu tego samego API?**  
O: Oczywiście. Zamień `PdfOptions` na odpowiednie opcje obrazu rastrowego (np. `PngOptions`) i ponownie użyj tej samej `CadRasterizationOptions`.

## Podsumowanie

Ten samouczek pokazał, jak **eksportować dwg do pdf** oraz obrazy rastrowe przy użyciu **biblioteki java cad** Aspose.CAD for Java. Postępując zgodnie z przewodnikiem krok po kroku, możesz zintegrować niezawodną konwersję CAD z dowolną aplikacją Java, niezależnie od tego, czy potrzebujesz PDF‑ów do dokumentacji, czy obrazów rastrowych do wyświetlania w sieci.

---

**Ostatnia aktualizacja:** 2026-02-17  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}