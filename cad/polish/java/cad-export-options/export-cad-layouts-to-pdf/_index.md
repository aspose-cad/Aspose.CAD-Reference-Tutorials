---
date: 2025-12-21
description: Dowiedz się, jak eksportować układy CAD do formatu PDF przy użyciu Aspose.CAD
  dla Javy – szybki i niezawodny sposób generowania PDF z plików CAD.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: Jak wyeksportować układy CAD do PDF przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wyeksportować układy CAD do PDF przy użyciu Aspose.CAD for Java

## Wprowadzenie

W tym samouczku pokażemy Ci **jak wyeksportować układy CAD** do PDF przy użyciu Aspose.CAD for Java. Niezależnie od tego, czy pracujesz z DWG, DXF czy innymi formatami CAD, ten przewodnik prowadzi Cię krok po kroku przez czyste, programistyczne podejście do szybkiego i niezawodnego generowania PDF z plików CAD.

## Szybkie odpowiedzi
- **Co robi biblioteka?** Konwertuje rysunki CAD (DWG, DXF, DWF itp.) na PDF, obrazy rastrowe i inne formaty.  
- **Jakiego języka użyto?** Java – kod działa na każdej platformie zgodnej z JVM.  
- **Czy potrzebna jest licencja?** Dostępna jest bezpłatna wersja próbna; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę konwertować DWG do PDF w Javie?** Tak – to samo API obsługuje **dwg to pdf java** konwersje.  
- **Jakie są główne kroki?** Załaduj plik CAD, ustaw opcje rasteryzacji, skonfiguruj opcje PDF i zapisz wynik.

## Wymagania wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania:

- Aspose.CAD for Java: Upewnij się, że masz zainstalowaną bibliotekę. Możesz ją pobrać ze strony Aspose [tutaj](https://releases.aspose.com/cad/java/).
- Środowisko programistyczne Java: Upewnij się, że masz skonfigurowane środowisko programistyczne Java na swoim komputerze.

Teraz, gdy wszystko jest gotowe, przejdźmy do samouczka.

## Co to jest „jak wyeksportować CAD”?

Eksportowanie CAD oznacza konwersję natywnych danych rysunku CAD (takich jak DWG, DXF lub DWF) do bardziej uniwersalnego formatu, takiego jak PDF. Ten proces jest niezbędny do udostępniania projektów interesariuszom, którzy mogą nie mieć zainstalowanego oprogramowania CAD.

## Dlaczego warto używać Aspose.CAD for Java do eksportu CAD do PDF?

- **Wysoka wierność** – grafika wektorowa jest zachowywana, a opcje rasteryzacji pozwalają precyzyjnie dostosować jakość.  
- **Brak zewnętrznych zależności** – czysta Java, bez natywnych DLL‑ów ani komponentów COM.  
- **Obsługa wielu formatów** – możesz także **generate pdf from cad** plików utworzonych w DWG, DWF lub innych formatach.  
- **Skalowalny dla zadań wsadowych** – idealny do automatyzacji po stronie serwera, potoków CI lub narzędzi desktopowych.

## Importowanie przestrzeni nazw

W swoim kodzie Java rozpocznij od zaimportowania niezbędnych przestrzeni nazw. Te importy zapewniają dostęp do klas i metod potrzebnych do pracy z Aspose.CAD for Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Krok 1: Załaduj plik CAD

Rozpocznij od załadowania pliku CAD do aplikacji Java przy użyciu metody `Image.load`. Zastąp `"conic_pyramid.dxf"` ścieżką do swojego pliku CAD.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Krok 2: Ustaw opcje rasteryzacji

Utwórz instancję `CadRasterizationOptions`, aby określić, jak jednostki CAD mają być rasteryzowane. Dostosuj parametry takie jak szerokość strony, wysokość strony oraz skalowanie układu zgodnie z wymaganiami.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Krok 3: Ustaw opcje PDF

Utwórz instancję `PdfOptions` i powiąż ją z opcjami rasteryzacji. Dodatkowo ustaw opcje graficzne dla eksportu PDF, takie jak tryb wygładzania, wskazówka renderowania tekstu i tryb interpolacji.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Krok 4: Eksportuj do PDF

Na koniec wyeksportuj układy CAD do pliku PDF, używając metody `save` obiektu `cadImage`.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| **Pusty plik PDF** | Opcje rasteryzacji nie są poprawnie ustawione (np. niezgodność nazwy układu) | Sprawdź, czy `rasterizationOptions.setLayouts()` odpowiada nazwom układów w Twoim pliku CAD. |
| **Obrazy o niskiej rozdzielczości** | `PageWidth`/`PageHeight` za małe | Zwiększ wymiary strony lub ustaw wyższą DPI za pomocą `rasterizationOptions.setResolution()`. |
| **Nieobsługiwana wersja CAD** | Starsze wersje DWG/DXF mogą wymagać nowszej wersji Aspose.CAD | Pobierz najnowszą wersję biblioteki ze strony Aspose. |

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.CAD for Java z innymi formatami plików CAD?

A1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne. Sprawdź dokumentację [tutaj](https://reference.aspose.com/cad/java/) po pełną listę.

### Q2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD for Java?

A2: Tak, możesz przetestować funkcje Aspose.CAD w ramach bezpłatnej wersji próbnej [tutaj](https://releases.aspose.com/).

### Q3: Jak mogę uzyskać wsparcie dla Aspose.CAD for Java?

A3: Odwiedź forum Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19) po wsparcie społeczności. Dla wsparcia premium rozważ zakup licencji [tutaj](https://purchase.aspose.com/buy).

### Q4: Jaka jest różnica między automatycznym a ręcznym skalowaniem układu?

A4: Automatyczne skalowanie układu dostosowuje rozmiar układu na podstawie określonych wymiarów strony, podczas gdy ręczne skalowanie pozwala ustawić własne wartości skalowania.

### Q5: Czy mogę dostosować wygląd wyeksportowanych plików PDF?

A5: Tak, możesz dostosować opcje graficzne w kodzie, aby kontrolować jakość i wygląd wyeksportowanego PDF.

### Q6: Czy Aspose.CAD obsługuje bezpośrednio konwersję **dwg to pdf java**?

A6: Absolutnie. Te same opcje rasteryzacji i PDF działają dla plików DWG, umożliwiając płynne konwersje **dwg to pdf java**.

### Q7: Czy istnieje sposób na **generate pdf from cad** bez rasteryzacji do bitmapy?

A7: Ustawiając `rasterizationOptions.setContentAsBitmap(false)`, możesz zachować dane wektorowe tam, gdzie to możliwe, co skutkuje prawdziwym wektorowym PDF.

**Ostatnia aktualizacja:** 2025-12-21  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}