---
date: 2026-06-24
description: Dowiedz się, jak utworzyć PDF z DXF i wyeksportować DXF do PDF przy użyciu
  Aspose.CAD for Java, ustawić rozmiar strony PDF oraz generować PDF z CAD z precyzyjną
  kontrolą.
keywords:
- create pdf from dxf
- export dxf to pdf
- set pdf page size
- convert dwg to pdf
- export cad drawing pdf
linktitle: Eksportuj określony układ DXF do PDF przy użyciu Java
schemas:
- author: Aspose
  dateModified: '2026-06-24'
  description: Learn how to create pdf from dxf and export dxf to pdf using Aspose.CAD
    for Java, set pdf page size, and generate pdf from cad with precise control.
  headline: Create pdf from dxf Layout to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create pdf from dxf and export dxf to pdf using Aspose.CAD
    for Java, set pdf page size, and generate pdf from cad with precise control.
  name: Create pdf from dxf Layout to PDF with Aspose.CAD for Java
  steps:
  - name: Set the Resource Directory
    text: Define the folder that contains your DXF files. Replace the placeholder
      with the actual path on your machine. > **Pro tip:** Use `System.getProperty("user.dir")`
      to build a relative path that works across environments.
  - name: Load the DXF File
    text: Load the source DXF using `Image.load()`. `Image.load()` reads a CAD file
      and returns an `Image` object representing its contents. The `Image.load()`
      method parses the DXF structure and creates an in‑memory representation that
      can be rasterized or saved directly.
  - name: Configure Rasterization Options (Set PDF Page Width in Java)
    text: Here we create `CadRasterizationOptions` and define the output page size.
      `CadRasterizationOptions` specifies how CAD data is rasterized, including page
      size, DPI, and layout selection. `CadRasterizationOptions` controls how the
      CAD data is rendered—page size, DPI, background color, and which layout
  - name: Create PDF Options (Java Convert CAD PDF)
    text: Link the rasterization settings to a `PdfOptions` instance. `PdfOptions`
      tells Aspose.CAD to generate a PDF file using the provided rasterization settings.
      `PdfOptions` is the container that tells the library to produce a PDF file,
      applying the rasterization settings defined earlier.
  - name: Export DXF to PDF (Create PDF from DXF)
    text: Finally, save the image as a PDF. `Image.save()` writes the rendered content
      to a file in the format specified by the options. The `save` call writes the
      rendered content to disk using the PDF options, producing a vector‑preserving
      PDF. After execution, you’ll find `conic_pyramid_layout_out_.pdf` in
  type: HowTo
- questions:
  - answer: Absolutely. The API is straightforward for newcomers while offering deep
      customization for power users.
    question: Is Aspose.CAD for Java suitable for both beginners and experienced developers?
  - answer: Yes. Adjust `CadRasterizationOptions` (page size, DPI, background color)
      per layout as needed.
    question: Can I customize the rasterization options for different layouts?
  - answer: Detailed docs are available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find comprehensive documentation for Aspose.CAD for Java?
  - answer: Yes, you can download a trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19) for
      community and staff assistance.
    question: How can I get support for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Utwórz PDF z układu DXF do PDF przy użyciu Aspose.CAD for Java
url: /pl/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz PDF z układu DXF do PDF przy użyciu Aspose.CAD dla Java

## Wprowadzenie

Jeśli jesteś programistą Java pracującym z rysunkami CAD, wiesz, że **jak eksportować dxf** pliki dokładnie może zadecydować o sukcesie projektu. Niezależnie od tego, czy generujesz raporty inżynierskie, udostępniasz projekty klientom, czy automatyzujesz konwersje wsadowe, niezawodna biblioteka Java do konwersji PDF jest niezbędna. W tym samouczku przeprowadzimy Cię przez **tworzenie pdf z dxf** plików układu, kontrolowanie wymiarów stron i zachowanie jakości wektorowej przy użyciu **Aspose.CAD for Java**.

## Szybkie odpowiedzi
- **Jaka jest główna biblioteka?** Aspose.CAD for Java, dedykowana biblioteka Java do konwersji PDF dla CAD.
- **Czy mogę wybrać konkretny układ?** Tak – użyj `CadRasterizationOptions.setLayouts()`, aby wskazać nazwę układu.
- **Jak ustawić rozmiar strony?** Dostosuj `setPageWidth()` i `setPageHeight()` w opcjach rasteryzacji (np. 1600 × 1600).
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna do użytku produkcyjnego; dostępna jest darmowa wersja próbna.
- **Jaką wersję Javy obsługuje?** Java 8 i wyższe (JDK 1.8+).

## Co to jest tworzenie PDF z DXF?
Tworzenie PDF z DXF oznacza konwersję rysunku CAD zapisanego w formacie DXF do dokumentu PDF przy zachowaniu danych wektorowych, warstw i informacji o układzie. **Aspose.CAD for Java** wykonuje tę konwersję w jednym wywołaniu, eliminując potrzebę pośrednich kroków rasteryzacji.

## Dlaczego warto używać Aspose.CAD for Java?
Aspose.CAD for Java zapewnia kompleksowe wsparcie CAD, obsługując ponad 30 formatów bez zewnętrznych zależności, oraz oferuje precyzyjną rasteryzację z konfigurowalnym DPI, rozmiarem strony i wyborem układu. Jego wysokowydajny silnik umożliwia szybkie konwersje wsadowe przy zachowaniu wierności wektorów, co czyni go idealnym do wdrożeń po stronie serwera i w chmurze.

- **Pełna obsługa CAD** – Obsługuje **ponad 30** formatów CAD, w tym DWG, DXF, DWF, DGN i DWT.  
- **Brak zewnętrznych zależności** – Czysta Java, nie wymaga natywnych DLL‑ów, co upraszcza wdrażanie na Linuxie, Windowsie lub w środowiskach kontenerowych.  
- **Precyzyjna rasteryzacja** – Wybierz wyjście wektorowe lub rastrowe, ustaw DPI, rozmiar strony i układ. Na przykład biblioteka może wyrenderować 500‑stronnicowy DXF w mniej niż 5 sekund na standardowym serwerze dwurdzeniowym.  
- **Wysoka wydajność** – Zoptymalizowane do przetwarzania wsadowego; może konwertować 1 000 plików w jednym wątku przy zużyciu pamięci heap poniżej 200 MB.  
- **Export dxf to pdf** w jednej linii kodu, co czyni go idealnym dla przepływów pracy **java convert cad pdf**.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Kit (JDK)** – Java 8 lub nowszą. Pobierz go z [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.CAD for Java** – Pobierz najnowszy plik JAR ze [strony pobierania Aspose.CAD](https://releases.aspose.com/cad/java/).  
3. IDE lub narzędzie budujące (Maven/Gradle), aby dodać plik JAR Aspose.CAD do classpathu projektu.

## Importowanie przestrzeni nazw

Najpierw zaimportuj klasy, które będą potrzebne. Te importy dają dostęp do ładowania obrazów, opcji rasteryzacji i ustawień wyjścia PDF.

Klasa `Image` jest podstawowym obiektem Aspose.CAD, który reprezentuje wczytany plik CAD w pamięci. Udostępnia metody renderowania i zapisywania zawartości w różnych formatach.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog zasobów

Zdefiniuj folder zawierający pliki DXF. Zastąp placeholder rzeczywistą ścieżką na swoim komputerze.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **Wskazówka:** Użyj `System.getProperty("user.dir")`, aby zbudować ścieżkę względną działającą w różnych środowiskach.

### Krok 2: Załaduj plik DXF

Załaduj źródłowy DXF używając `Image.load()`.  
`Image.load()` odczytuje plik CAD i zwraca obiekt `Image` reprezentujący jego zawartość.

Metoda `Image.load()` analizuje strukturę DXF i tworzy reprezentację w pamięci, którą można rasteryzować lub zapisać bezpośrednio.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### Krok 3: Skonfiguruj opcje rasteryzacji (Ustaw szerokość strony PDF w Javie)

Tutaj tworzymy `CadRasterizationOptions` i definiujemy rozmiar strony wyjściowej.  
`CadRasterizationOptions` określa, jak dane CAD są rasteryzowane, w tym rozmiar strony, DPI i wybór układu.

`CadRasterizationOptions` kontroluje sposób renderowania danych CAD — rozmiar strony, DPI, kolor tła oraz które układy mają być rasteryzowane.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – kontrolują **szerokość strony PDF** (i wysokość) dla PDF.  
- `setLayouts` – określa, które układy mają być renderowane; `"Model"` jest domyślną przestrzenią modelu w wielu plikach DXF.

### Krok 4: Utwórz opcje PDF (Java Convert CAD PDF)

Połącz ustawienia rasteryzacji z instancją `PdfOptions`.  
`PdfOptions` instruuje Aspose.CAD, aby wygenerował plik PDF przy użyciu podanych ustawień rasteryzacji.

`PdfOptions` jest kontenerem, który informuje bibliotekę, aby wyprodukowała plik PDF, stosując wcześniej zdefiniowane ustawienia rasteryzacji.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Eksportuj DXF do PDF (Utwórz PDF z DXF)

Na koniec zapisz obraz jako PDF.  
`Image.save()` zapisuje wyrenderowaną zawartość do pliku w formacie określonym przez opcje.

Wywołanie `save` zapisuje wyrenderowaną zawartość na dysk przy użyciu opcji PDF, tworząc PDF zachowujący wektory.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

Po wykonaniu znajdziesz plik `conic_pyramid_layout_out_.pdf` w tym samym katalogu, zawierający tylko układ **Model** wyrenderowany w ustawionych wymiarach.

## Typowe przypadki użycia

| Scenariusz | Dlaczego ta metoda pomaga |
|------------|---------------------------|
| **Automatyczne generowanie raportów** | Gwarantuje, że każdy rysunek jest eksportowany z tym samym rozmiarem strony, co sprawia, że PDF‑y wsadowe są jednolite. |
| **Podglądy projektów dla klienta** | Eksportowanie jednego układu (np. „Model” lub „Sheet1”) zmniejsza rozmiar pliku przy zachowaniu wierności wektorowej. |
| **Migracja starszych DWG do PDF** | Mimo że przykład używa DXF, to samo API działa dla **convert dwg to pdf** przy minimalnych zmianach kodu. |
| **Osadzanie rysunków CAD w portalach internetowych** | Wygenerowany PDF może być strumieniowany bezpośrednio do przeglądarek bez dodatkowych narzędzi konwersji. |

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| **Pusty PDF** | Niepasująca nazwa układu | Zweryfikuj dokładną nazwę układu w DXF (użyj przeglądarki CAD). |
| **Nieprawidłowy rozmiar strony** | `setPageWidth/Height` nie zastosowane | Upewnij się, że ustawiasz opcje rasteryzacji **przed** utworzeniem `PdfOptions`. |
| **Brak pamięci przy dużych plikach** | Ładowanie ogromnego DXF do pamięci | Użyj strumieniowania lub zwiększ pamięć heap JVM (`-Xmx2g`). |
| **Brak czcionek** | Elementy tekstowe używają niedostępnych czcionek | Zainstaluj wymagane czcionki na serwerze lub osadź je poprzez `CadRasterizationOptions`. |
| **Potrzeba eksportu wielu układów** | Wywołanie tylko jednego układu | Wywołaj `setLayouts` z tablicą nazw układów i powtórz krok `save` dla każdego z nich. |

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD for Java jest odpowiedni zarówno dla początkujących, jak i doświadczonych programistów?**  
O: Zdecydowanie. API jest proste dla nowicjuszy, a jednocześnie oferuje głęboką personalizację dla zaawansowanych użytkowników.

**P: Czy mogę dostosować opcje rasteryzacji dla różnych układów?**  
O: Tak. Dostosuj `CadRasterizationOptions` (rozmiar strony, DPI, kolor tła) dla każdego układu w razie potrzeby.

**P: Gdzie mogę znaleźć pełną dokumentację Aspose.CAD for Java?**  
O: Szczegółowa dokumentacja jest dostępna [tutaj](https://reference.aspose.com/cad/java/).

**P: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
O: Tak, wersję próbną można pobrać [tutaj](https://releases.aspose.com/).

**P: Jak mogę uzyskać wsparcie dla Aspose.CAD for Java?**  
O: Odwiedź forum wsparcia [tutaj](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc od społeczności i zespołu.

## Podsumowanie

W tym przewodniku pokazaliśmy **jak utworzyć PDF z układów DXF** przy użyciu Aspose.CAD for Java, obejmując wszystko od konfiguracji środowiska po precyzyjne dopasowanie wymiarów stron. Korzystając z tej **biblioteki Java do konwersji PDF**, możesz automatyzować przepływy pracy CAD‑do‑PDF, zachować wierność wektorów i zintegrować płynne generowanie PDF w swoich aplikacjach Java. Niezależnie od tego, czy potrzebujesz **eksportować dxf do pdf**, **konwertować dwg do pdf**, czy **generować pdf z cad** do dalszego przetwarzania, powyższe kroki zapewniają solidną podstawę.

---

**Ostatnia aktualizacja:** 2026-06-24  
**Testowano z:** Aspose.CAD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Utwórz PDF z CAD – Eksportuj DXF do PDF przy użyciu Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Utwórz PDF z DXF: Eksportuj warstwę przy użyciu Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Konwertuj CAD do PDF – Ustaw rozmiar płótna i tryb (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}