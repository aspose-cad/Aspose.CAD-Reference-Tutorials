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

## Introduction

W dynamicznym świecie projektowania wspomaganego komputerowo (CAD) efektywne zarządzanie rysunkami jest kluczowe. Z **Aspose.CAD for Java** możesz **export dwg to pdf** — lub obrazy rastrowe — w zaledwie kilku linijkach kodu. Ten samouczek przeprowadzi Cię przez cały proces, od wczytania pliku DWG po wygenerowanie wysokiej jakości PDF, podkreślając dlaczego Aspose.CAD Java jest biblioteką numer jeden do zadań konwersji CAD.

## Quick Answers
- **Co obejmuje ten samouczek?** Eksportowanie plików DWG do PDF lub obrazów rastrowych przy użyciu Aspose.CAD for Java.  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa licencja tymczasowa do oceny; pełna licencja jest wymagana w produkcji.  
- **Jaką wersję Java obsługuje?** Każde środowisko uruchomieniowe Java 8+ działa z najnowszym API Aspose.CAD Java.  
- **Czy mogę konwertować DWG na inne formaty obrazów?** Tak – te same opcje rasteryzacji pozwalają na wyjście PNG, JPEG, BMP itd.  
- **Jak długo trwa konwersja?** Zwykle poniżej sekundy dla standardowych rysunków; większe pliki mogą zająć kilka sekund.

## What is “export dwg to pdf”?

Eksportowanie DWG do PDF oznacza konwersję natywnego rysunku AutoCAD do przenośnego, niezależnego od urządzenia dokumentu PDF. Powstały PDF zachowuje dane wektorowe, warstwy i skalowanie, co czyni go idealnym do udostępniania, drukowania lub archiwizacji.

## Why use Aspose.CAD Java for this conversion?
- **Brak zewnętrznych zależności** – czysta Java, bez natywnych DLL.  
- **Precyzyjne obsługiwanie jednostek** – automatycznie respektuje jednostki metryczne lub imperialne.  
- **Wysokiej jakości wyjście rastrowe** – precyzyjnie dostosowane DPI i kontrola rozmiaru strony.  
- **Pełne wsparcie PDF** – generowanie PDF zachowującego wektory bez dodatkowych bibliotek.

## Prerequisites

Zanim zagłębisz się w kod, upewnij się, że masz:

- Podstawową znajomość programowania w Javie.  
- Zainstalowaną bibliotekę Aspose.CAD for Java. Jeśli jeszcze jej nie pobrałeś, pobierz ją **[here](https://releases.aspose.com/cad/java/)**.  
- Plik DWG do testów – w tym przewodniku używany jest przykładowy **Bottom_plate.dwg**.

## Import Namespaces

W swoim projekcie Java zaimportuj niezbędne klasy, aby rozpocząć konwersję:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

Najpierw wczytaj swój rysunek DWG przy użyciu klasy `Image`. Tworzy to reprezentację w pamięci, z którą Aspose.CAD może pracować.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

Zrozumienie, czy rysunek używa jednostek metrycznych czy imperialnych, jest niezbędne do prawidłowego skalowania. Metoda pomocnicza `IsMetric` (implementacja pominięta dla zwięzłości) zwraca wartość boolowską.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

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

### Step 4: Configure PDF Options

Utwórz instancję `PdfOptions` i dołącz ustawienia rasteryzacji. To informuje Aspose.CAD, jak osadzić rasteryzowaną zawartość w ostatecznym PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

Na koniec wyeksportuj rysunek do pliku PDF. Metoda `save` przyjmuje ścieżkę wyjściową oraz skonfigurowane `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Po zakończeniu działania kodu znajdziesz **Saved.pdf** w folderze `DWGDrawings`, gotowy do dystrybucji lub archiwizacji.

## Common Issues & Tips

- **Nieprawidłowy rozmiar strony** – Sprawdź ponownie logikę konwersji jednostek; niepasujące współczynniki mogą powodować zbyt duże strony.  
- **Brak czcionek lub grubości linii** – Upewnij się, że DWG odwołuje się do wszystkich zewnętrznych zasobów przed konwersją.  
- **Wydajność przy dużych rysunkach** – Zwiększ ustawienie `DPI` w `CadRasterizationOptions` tylko wtedy, gdy wymagana jest wyższa jakość; niższe DPI przyspiesza przetwarzanie.

## Frequently Asked Questions

**P: Czy mogę używać Aspose.CAD for Java z innymi frameworkami Java?**  
O: Tak, Aspose.CAD for Java bezproblemowo integruje się z popularnymi frameworkami Java, takimi jak Spring, Jakarta EE i Android.

**P: Czy dostępna jest tymczasowa licencja dla Aspose.CAD for Java?**  
O: Tak, tymczasową licencję możesz uzyskać **[here](https://purchase.aspose.com/temporary-license/)**.

**P: Gdzie mogę znaleźć wsparcie dla Aspose.CAD for Java?**  
O: Odwiedź **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**, aby uzyskać pomoc od społeczności i inżynierów Aspose.

**P: Jak mogę kupić licencję na Aspose.CAD for Java?**  
O: Licencję możesz zakupić **[here](https://purchase.aspose.com/buy)**.

**P: Jakie jednostki obsługuje Aspose.CAD for Java?**  
O: Aspose.CAD for Java obsługuje zarówno jednostki metryczne, jak i imperialne, automatycznie wykrywając system jednostek rysunku.

**P: Czy mogę konwertować DWG na inne formaty obrazów (np. PNG, JPEG) przy użyciu tego samego API?**  
O: Oczywiście. Zastąp `PdfOptions` odpowiednimi opcjami obrazu rastrowego (np. `PngOptions`) i ponownie użyj tych samych `CadRasterizationOptions`.

## Conclusion

Ten samouczek pokazał, jak **export dwg to pdf** oraz obrazy rastrowe przy użyciu Aspose.CAD for Java. Postępując zgodnie ze wskazówkami krok po kroku, możesz zintegrować niezawodną konwersję CAD w dowolnej aplikacji Java, niezależnie od tego, czy potrzebujesz PDF‑ów do dokumentacji, czy obrazów rastrowych do wyświetlania w sieci.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}