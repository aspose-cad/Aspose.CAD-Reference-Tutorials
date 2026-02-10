---
date: 2025-12-18
description: Poznaj sposób eksportowania plików DWG do formatu PDF lub obrazów rastrowych
  w Javie przy użyciu Aspose.CAD. Ten przewodnik krok po kroku zapewnia precyzję,
  wydajność i łatwą konwersję plików DWG.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Eksportuj DWG do PDF lub obrazu rastrowego przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport DWG do PDF lub Raster przy użyciu Aspose.CAD dla Java

## Wstęp

W dynamicznym świecie projektowania wspomaganego komputerowo (CAD) poza zarządzaniem rysunkami jest kluczowe. Z **Aspose.CAD for Java** możesz **eksportować dwg do formatu pdf**—lub obrazy rastrowe—w zaledwie kilku linijkach kodu. Ten samouczek przeprowadzi Cię przez cały proces, od wczytania pliku DWG po wygenerowanie wysokiej jakości PDF, z powodu przyczyny Aspose.CAD Java jest biblioteką numer jeden do zadań występujących w CAD.

## Szybkie odpowiedzi
- **Co dodaje ten samouczek?** Eksportowanie plików DWG do PDF lub obrazów rastrowych przy użyciu Aspose.CAD dla Java.
- **Czy istnieje licencjat?** Dostępna jest licencja tymczasowa do oceny; pełny licencjat jest wymagany w produkcji.
- **Jaką wersję Java obsługuje?** Każde uruchomienie uruchomieniowe Java8+ działa z wydaniem API Aspose.CAD Java.
- **Czy mogę konwertować DWG na inne formaty obrazów?** Tak – te same opcje rasteryzacji funkcji na wyjściu PNG, JPEG, BMP itd.
- **Jak długo trwa konwersja?** poniżej sekundy dla parametrów wykonawczych; większe pliki mogą być kilka sekund.

## Co to jest „eksport dwg do pdf”?

Eksportowanie DWG do PDF oznacza konwersję natywnego rysunku AutoCAD, uwzględniającego, niezależne od urządzenia dokumentu PDF. Powstały w formacie PDF dane, funkcje i skalowanie, co stanowi rozwiązanie umożliwiające udostępnienie, udostępnienie lub archiwizację.

## Po co używać Aspose.CAD Java do tej konwersji?
- **Brak zewnętrznych zależności** – czysta Java, bez natywnych bibliotek DLL.
- **Precyzyjne obsługa jednostek** – automatycznie respektuje jednostki metryczne lub imperialne.
- **Wysokiej jakości wyjście rastrowe** – szczegółowe wyniki DPI i kontrola kontrolna strony.
- **Pełne PDF** – generowanie PDF wspierającego wektory bez dodatkowych bibliotek.

## Warunki wstępne

Zanim zagłębisz się w kod, zastosuj się, że masz:

- Podstawową przyjemność programowania w Javie.
- Zainstalowaną bibliotekę Aspose.CAD dla Java. Jeśli jeszcze jej nie pobrałeś, pobierz ją **[tutaj](https://releases.aspose.com/cad/java/)**.
- Plik DWG do testów – w tym przewodniku używany jest przykładowy **Bottom_plate.dwg**.

## Importuj przestrzenie nazw

W swoim projekcie Java zaimportuj niezbędne klasy, aby rozpocząć konwersję:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj plik DWG

Najpierw wczytaj swój rysunek DWG przy użyciu klasy `Image`. Tworzy to reprezentację w pamięci, z którą Aspose.CAD może pracować.

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

Na podstawie systemu jednostek skonfiguruj rozmiar strony, skalowanie i docelowy typ jednostki. Te opcje określają, jak DWG jest rasteryzowany przed umieszczeniem w PDF.

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

### Krok 4: Skonfiguruj opcje PDF

Utwórz instancję `PdfOptions` i dołącz ustawienia rasteryzacji. To informuje Aspose.CAD, jak osadzić rasteryzowaną zawartość w ostatecznym PDF.

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

## Typowe problemy i wskazówki

- **Nieprawidłowy rozmiar strony** – Sprawdź ponownie logikę jednostek; niepasujące ilości mogą być zbyt duże strony.
- **Brak czcionek lub grubości linii** – zastosowanie, że DWG jest dostępny do wszystkich zewnętrznych zasobów przed konwersją.
- **Wydajność przy dużych rysunkach** – Zwiększ ustawienie `DPI` w `CadRasterizationOptions` tylko wtedy, gdy wymagana jest wyższa jakość; włączenie DPI przyspieszanie.

## Często zadawane pytania

**P: Czy można zainstalować Aspose.CAD for Java z innymi frameworkami Java?**
O: Tak, Aspose.CAD dla Java bezproblemowo integruje się z zużytymi frameworkami Java, wtyczkami jak Spring, Jakarta EE i Android.

**P: Czy dostępna jest tymczasowa licencjat dla Aspose.CAD dla Java?**
O: Tak, tymczasowo możesz uzyskać **[tutaj](https://purchase.aspose.com/temporary-license/)**.

**P: Gdzie mogę znaleźć wsparcie dla Aspose.CAD dla Java?**
O: Odwiedź **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**, aby uzyskać pomoc społeczności i inżynierów Aspose.

**P: Jak mogę kupić na Aspose.CAD dla Java?**
O: Licencję możesz kupić **[tutaj](https://purchase.aspose.com/buy)**.

**P: Jaki jednostka obsługuje Aspose.CAD for Java?**
O: Aspose.CAD for Java obsługuje jednostki fizyczne, jak i imperialne, automatycznie wykrywając jednostki rysunkowe.

**P: Czy mogę konwertować DWG na inne formaty obrazów (np. PNG, JPEG) przy użyciu tego samego API?**
O: Oczywiście. Zastąp `PdfOptions` adecydowanych i opcji obrazu rastrowego (np. `PngOptions`) i ponownie administratorów tych samych `CadRasterizationOptions`.

## Wniosek

Dziesięć samouczków pokazanych, jak **export dwg to pdf** oraz obrazy rastrowe przy użyciu Aspose.CAD dla Java. Po wykonaniu kroku po kroku, możliwe jest niezawodną konwersję CAD w aplikacji Java, uruchomienie od tego, czy też PDF-ów do dokumentacji, czy obrazów rastrowych do aplikacji w sieci.

---

**Ostatnia aktualizacja:** 18.12.2025 r
**Testowano z:** Aspose.CAD dla Java 24.10
**Autor:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}