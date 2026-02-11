---
date: 2026-01-02
description: Dowiedz się, jak wyeksportować plik DWG do formatu PDF, włączyć linie
  ukryte i przekonwertować DWG na PDF przy użyciu Aspose.CAD dla Javy w tym samouczku
  krok po kroku.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Eksportuj DWG jako PDF z ukrytymi liniami – Aspose.CAD dla Javy
url: /pl/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj DWG jako PDF z ukrytymi liniami – Aspose.CAD dla Javy

## Wprowadzenie

W tym samouczku dowiesz się, jak **eksportować DWG jako PDF** zachowując ukryte linie przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz **konwertować DWG do PDF**, stworzyć przewodnik w stylu **dwg to pdf tutorial**, czy po prostu **zapisać DWG jako PDF** z obsługą ukrytych linii, przeprowadzimy Cię przez każdy krok. Po zakończeniu będziesz mieć gotowe rozwiązanie, które możesz wstawić do dowolnego projektu Javy.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Włączenie renderowania ukrytych linii podczas eksportu DWG do PDF przy użyciu Aspose.CAD dla Javy.  
- **Jakie główne działanie jest wykonywane?** `export dwg as pdf`.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Jakie są wymagania wstępne?** Środowisko programistyczne Java, biblioteka Aspose.CAD dla Javy oraz pliki DWG.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowej konfiguracji.

## Co to jest „export dwg as pdf”?

Eksportowanie pliku DWG do PDF konwertuje wektorowy rysunek CAD do formatu dokumentu przenośnego, zachowując warstwy, typy linii oraz opcjonalne renderowanie ukrytych linii. Dzięki temu łatwo udostępnić projekty CAD interesariuszom, którzy nie posiadają oprogramowania CAD.

## Dlaczego włączać ukryte linie przy eksporcie?

Ukryte linie zapewniają czytelniejszą wizualizację złożonych modeli 3D na dwuwymiarowej stronie, podkreślając tylko widoczne krawędzie. Poprawia to czytelność i często jest wymagane w dokumentacji inżynierskiej.

## Wymagania wstępne

1. **Aspose.CAD for Java** – pobierz bibliotekę z oficjalnej strony [tutaj](https://releases.aspose.com/cad/java/).  
2. **Pliki DWG** – przechowuj źródłowe rysunki DWG w znanym katalogu.  
3. **Środowisko programistyczne Java** – JDK 8+ oraz ulubione IDE (Eclipse, IntelliJ, itp.).  

Teraz, gdy wszystko jest gotowe, przejdźmy do kodu.

## Importowanie przestrzeni nazw

Rozpocznij od zaimportowania niezbędnych klas, aby móc pracować z obrazami CAD i opcjami PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Krok 1: Konfiguracja projektu

Utwórz projekt Java i dodaj plik JAR Aspose.CAD do ścieżki kompilacji. Następnie określ katalog, w którym znajdują się Twoje pliki DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Wskazówka:** Użyj ścieżki bezwzględnej lub skonfiguruj ścieżkę względną w oparciu o folder zasobów Twojego projektu.

## Krok 2: Załaduj plik DWG

Załaduj źródłowy plik DWG do obiektu `CadImage`, aby móc go manipulować.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Krok 3: Skonfiguruj opcje rasteryzacji

Wybierz warstwy, które chcesz uwzględnić, i ustaw rozmiar strony tak, aby odpowiadał oryginalnemu rysunkowi. To miejsce, w którym włączamy renderowanie ukrytych linii, określając układ.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Krok 4: Ustaw opcje PDF

Poleć Aspose.CAD rasteryzować dane wektorowe do PDF, używając układu „Model”, aby ukryte linie pozostały ukryte.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Zapisz wynik

Na koniec wyeksportuj DWG jako plik PDF. Ukryte linie będą respektowane zgodnie z ustawionym układem.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Częsty błąd:** Zapomnienie o ustawieniu układu na `"Model"` spowoduje, że wszystkie linie (w tym ukryte) będą wyświetlane jako pełne w PDF.

## Zakończenie

Masz teraz kompletną, gotową do produkcji metodę **eksportowania DWG jako PDF** z obsługą ukrytych linii przy użyciu Aspose.CAD dla Javy. Podejście to może być zintegrowane z narzędziami przetwarzania wsadowego, usługami sieciowymi lub aplikacjami desktopowymi w celu automatyzacji konwersji CAD‑do‑PDF.

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Javy z innymi formatami plików CAD?
A1: Tak, Aspose.CAD obsługuje różne formaty CAD, takie jak DWG, DXF, DWF i inne.

### P2: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Javy?
A2: Tak, darmową wersję próbną znajdziesz [tutaj](https://releases.aspose.com/).

### P3: Jak uzyskać wsparcie dla Aspose.CAD dla Javy?
A3: Odwiedź forum Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie społeczności.

### P4: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla Javy?
A4: Zapoznaj się z dokumentacją [tutaj](https://referencepose.com/cad/java/).

### P5: Czy mogę kupić tymczasową licencję na Aspose.CAD dla Javy?
A5: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

### P6: Czy ta metoda działa również przy konwersji DWG do PDF w środowisku serwera bez interfejsu graficznego?
A6: Zdecydowanie. Ponieważ kod używa wyłącznie API Aspose.CAD, działa bez żadnych zależności UI, co czyni go idealnym do automatyzacji po stronie serwera.

---

**Ostatnia aktualizacja:** 2026-01-02  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}