---
date: 2026-06-19
description: Bezproblemowo konwertuj pliki DGN na PDF przy użyciu Aspose.CAD for Java.
  Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby wyeksportować DGN do
  PDF, zapisać CAD jako PDF i usprawnić swój przepływ pracy.
keywords:
- convert dgn to pdf
- save cad as pdf
- export dgn to pdf
linktitle: Obsługa DGN V7
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  headline: Convert DGN to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  name: Convert DGN to PDF with Aspose.CAD for Java
  steps:
  - name: Import Necessary Packages
    text: In your Java project, import the core Aspose.CAD classes that enable file
      loading and export.
  - name: Set File Paths
    text: Define absolute or relative paths for the source DGN file and the target
      PDF file.
  - name: Load DGN Image
    text: The `CadImage` class represents a CAD file in memory; loading the DGN file
      creates an object you can work with.
  - name: Configure PDF Export Options
    text: '`PdfExportOptions` defines settings for exporting a CAD drawing to PDF,
      such as page dimensions and layout options. Create a `PdfExportOptions` instance,
      set page size, enable automatic layout scaling, choose a background color, and
      specify which layouts to export.'
  - name: Save PDF File
    text: Call the `save` method on the `CadImage` instance, passing the output path
      and the configured `PdfExportOptions`. Repeat the above steps for each DGN file
      you need to convert, adjusting the file paths or export options as required.
  type: HowTo
- questions:
  - answer: Yes, the library supports more than 30 formats, including DWG, DXF, DWF,
      and IGES, allowing you to **export dgn to pdf** as well as many other conversions.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Is a temporary license available for testing?
  - answer: Refer to the [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)
      for full method signatures and usage examples.
    question: Where can I find detailed API documentation?
  - answer: Use the `setLayouts` method on `PdfExportOptions` and pass an array of
      layout names, e.g., `new String[] {"Model", "Layout1"}`.
    question: How do I specify which layouts to export?
  - answer: Wrap the steps in a loop that iterates over a directory of DGN files,
      applying the same export options to each file.
    question: What if I need to batch‑convert many DGN files?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konwertuj DGN na PDF przy użyciu Aspose.CAD for Java
url: /pl/java/other-cad-operations/support-for-dgn-v7/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DGN do PDF przy użyciu Aspose.CAD dla Javy

W nowoczesnych środowiskach CAD możliwość **convert dgn to pdf** szybko i niezawodnie jest niezbędna do udostępniania projektów interesariuszom niebędącym użytkownikami CAD. Aspose.CAD for Java udostępnia czysto‑Java API, które pozwala eksportować pliki DGN do wysokiej jakości dokumentów PDF bez żadnych zewnętrznych zależności. Ten samouczek przeprowadzi Cię przez cały proces, od konfiguracji biblioteki po precyzyjne dostosowanie opcji eksportu PDF, abyś mógł zintegrować konwersję w swoich aplikacjach Java z pełnym zaufaniem.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje konwersję DGN?** Aspose.CAD for Java.
- **Czy mogę eksportować wiele układów?** Tak, określ tablicę układów w opcjach eksportu.
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.CAD do nieograniczonego użycia.
- **Jakie wersje Javy są obsługiwane?** Java 8 i nowsze.
- **Czy konwersja jest bezstratna?** PDF zachowuje grafikę wektorową, warstwy i dokładność tekstu.

## Co to jest konwersja dgn do pdf?
Konwersja dgn do pdf to proces przekształcania pliku projektowego DGN (MicroStation) do formatu Portable Document Format (PDF) w celu łatwego przeglądania, drukowania i dystrybucji. Aspose.CAD for Java odczytuje natywną strukturę DGN, renderuje każdy układ jako grafikę wektorową i zapisuje wynik do pliku PDF, zachowując dokładność geometrii i tekstu.

## Dlaczego warto używać Aspose.CAD for Java do zapisywania CAD jako PDF?
Aspose.CAD może **zapisować CAD jako PDF** dla ponad 30 formatów CAD, przetwarza pliki do 2 GB bez ładowania całego dokumentu do pamięci i zapewnia prędkość konwersji do 5 × szybszą niż konkurencyjne biblioteki na typowym sprzęcie serwerowym. API nie wymaga natywnych binarek, co umożliwia płynne wdrażanie w środowiskach chmurowych lub kontenerowych.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- **Aspose.CAD for Java Library** – pobierz ją ze [strony pobierania Aspose.CAD for Java](https://releases.aspose.com/cad/java/).
- **Java Development Environment** – zainstalowany i skonfigurowany JDK 8 lub nowszy na Twoim komputerze.
- Ważna **licencja Aspose.CAD** do użytku produkcyjnego (tymczasowa licencja jest dostępna do oceny).

Aby uzyskać wsparcie społeczności, odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

## Jak wyeksportować dgn do pdf krok po kroku?

Załaduj swój plik DGN, skonfiguruj opcje eksportu PDF i zapisz wynik w kilku linijkach kodu. Poniższe kroki pokazują dokładną kolejność, którą należy wykonać, a każdy krok zawiera krótki placeholder kodu, który zastąpisz rzeczywistą implementacją z dokumentacji Aspose.CAD.

### Krok 1: Importuj niezbędne pakiety

W swoim projekcie Java zaimportuj podstawowe klasy Aspose.CAD, które umożliwiają ładowanie plików i eksport.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

### Krok 2: Ustaw ścieżki plików

Zdefiniuj bezwzględne lub względne ścieżki do pliku źródłowego DGN oraz docelowego pliku PDF.  
```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

### Krok 3: Załaduj obraz DGN

Klasa `CadImage` reprezentuje plik CAD w pamięci; załadowanie pliku DGN tworzy obiekt, z którym możesz pracować.  
```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

### Krok 4: Skonfiguruj opcje eksportu PDF

`PdfExportOptions` definiuje ustawienia eksportu rysunku CAD do PDF, takie jak wymiary strony i opcje układu.

Utwórz instancję `PdfExportOptions`, ustaw rozmiar strony, włącz automatyczne skalowanie układu, wybierz kolor tła i określ, które układy mają być eksportowane.  
```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //only export 4 (1,2,3 and 9) views
options.setVectorRasterizationOptions(vectorOptions);
```

### Krok 5: Zapisz plik PDF

Wywołaj metodę `save` na instancji `CadImage`, przekazując ścieżkę wyjściową oraz skonfigurowane `PdfExportOptions`.  
```java
objImage.save(outFile, options);
```

Powtórz powyższe kroki dla każdego pliku DGN, który musisz przekonwertować, dostosowując ścieżki plików lub opcje eksportu w razie potrzeby.

## Typowe problemy i rozwiązania

- **Missing layouts** – Upewnij się, że nazwy układów przekazywane do `setLayouts` dokładnie odpowiadają tym w źródłowym pliku DGN; nazwy układów są rozróżniane pod względem wielkości liter.
- **Out‑of‑memory errors** – W przypadku bardzo dużych rysunków włącz strumieniowanie, ustawiając `PdfExportOptions.setUseMemoryCache(true)`.
- **Incorrect colors** – Zweryfikuj, że kolor tła jest ustawiony na `Color.WHITE` (lub wybrany przez Ciebie kolor), aby uniknąć nieoczekiwanych ciemnych tła w PDF.

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD for Java z innymi formatami plików CAD?**  
O: Tak, biblioteka obsługuje ponad 30 formatów, w tym DWG, DXF, DWF i IGES, co pozwala na **export dgn to pdf** oraz wiele innych konwersji.

**P: Czy dostępna jest tymczasowa licencja do testów?**  
O: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/) do celów ewaluacyjnych.

**P: Gdzie mogę znaleźć szczegółową dokumentację API?**  
O: Odwołaj się do [dokumentacji Aspose.CAD for Java](https://reference.aspose.com/cad/java/), aby uzyskać pełne sygnatury metod i przykłady użycia.

**P: Jak określić, które układy mają być eksportowane?**  
O: Użyj metody `setLayouts` na `PdfExportOptions` i przekaż tablicę nazw układów, np. `new String[] {"Model", "Layout1"}`.

**P: Co zrobić, jeśli muszę konwertować wsadowo wiele plików DGN?**  
O: Umieść kroki w pętli, która iteruje po katalogu plików DGN, stosując te same opcje eksportu do każdego pliku.

---

**Ostatnia aktualizacja:** 2026-06-19  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksportuj DWG do PDF i konwertuj rysunki CAD – Samouczek Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [dwg do pdf java – Eksportuj CAD do PDF przy użyciu Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Eksportuj układy CAD do PDF przy użyciu Aspose.CAD for Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}