---
date: 2026-10-04
description: Dowiedz się, jak szybko konwertować DWG na PNG i eksportować CAD jako
  PNG lub inne formaty rastrowe przy użyciu Aspose.CAD for Java. Uzyskaj wysokiej
  jakości wyniki w krótkim czasie.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Konwertuj układ CAD na format obrazu rastrowego
og_description: Szybko konwertuj DWG na PNG przy użyciu Aspose.CAD for Java. Dowiedz
  się krok po kroku, jak eksportować CAD jako PNG, JPEG, TIFF i inne.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Konwertuj DWG na PNG i inne formaty rastrowe przy użyciu Aspose.CAD for
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Konwertuj DWG na PNG i inne formaty rastrowe przy użyciu Aspose.CAD for Java
url: /pl/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PNG i innych formatów rastrowych przy użyciu Aspose.CAD for Java

## Wprowadzenie

`Aspose.CAD for Java` to biblioteka umożliwiająca programową konwersję plików CAD do obrazów rastrowych, takich jak PNG, JPEG i TIFF. Konwersja DWG do PNG (lub innych formatów obrazów rastrowych) jest powszechnym wymaganiem, gdy trzeba udostępnić rysunki CAD współpracownikom, którzy nie mają przeglądarki CAD, osadzić projekty w dokumentacji lub wygenerować miniatury do galerii internetowych. W tym przewodniku nauczysz się, jak szybko i niezawodnie konwertować dwg do png, niezależnie od tego, czy pracujesz z pełnym plikiem rysunku, czy tylko z określonym układem. Możesz także potrzebować **konwertować CAD do formatu rastrowego** do podglądów w sieci, narzędzi raportujących lub aplikacji mobilnych.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje konwersję DWG do PNG?** Aspose.CAD for Java zapewnia silnik konwersji.  
- **Jakie formaty rastrowe mogę wyeksportować?** PNG, JPEG, TIFF, PDF, BMP oraz ponad 30 dodatkowych formatów.  
- **Czy potrzebna jest licencja do testowania?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę wybrać konkretny układ?** Tak – użyj `setLayouts`, aby wybrać „Model”, „Layout1” itp.  
- **Czy możliwe jest wyjście w wysokiej rozdzielczości?** Oczywiście – dostosuj `setPageWidth` i `setPageHeight` (lub `setResolution`), aby kontrolować DPI.

## Co to jest „convert dwg to png”?

Convert dwg to png oznacza przekształcenie wektorowego rysunku DWG w obraz PNG oparty na pikselach, który może być wyświetlany w dowolnym standardowym przeglądarce obrazów. Ten proces rasteryzuje elementy wektorowe, zachowując grubość linii, kolory i warstwy, jednocześnie przekształcając je w bitmapę o stałej rozdzielczości. Wynik jest idealny do osadzania w plikach PDF, dokumentach Word lub stronach internetowych, gdzie obsługa wektorów jest ograniczona.

## Dlaczego eksportować CAD jako PNG (lub inne formaty rastrowe)?

Eksportowanie CAD jako PNG zapewnia uniwersalną kompatybilność, szybkie ładowanie i łatwe osadzanie na wszystkich głównych platformach. Obrazy rastrowe ładują się natychmiast w porównaniu do otwierania ciężkiego pliku DWG, a bezstratna kompresja PNG zapewnia wysoką wierność wizualną. Kontrolując rozdzielczość, kolor tła i układ, zapewniasz, że każdy interesariusz zobaczy ten sam wygląd, niezależnie od tego, czy plik jest przeglądany na komputerze, urządzeniu mobilnym czy w przeglądarce.

## Typowe przypadki użycia

| Scenariusz | Dlaczego wyjście rastrowe pomaga |
|------------|-----------------------------------|
| **Project documentation** | Osadzanie PNG w plikach PDF lub dokumentach Word eliminuje konieczność posiadania oprogramowania CAD przez recenzentów. |
| **Web portals** | Miniatury generowane z plików DWG ładują się natychmiast i poprawiają doświadczenie użytkownika. |
| **Mobile apps** | Obrazy rastrowe wyświetlają się poprawnie na urządzeniach, które nie posiadają przeglądarki CAD. |
| **Automated reporting** | Wsadowa konwersja wielu układów do PNG/JPEG w celu włączenia ich do wykresów lub pulpitów nawigacyjnych. |

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

1. **Środowisko programistyczne Java** – zainstalowany i skonfigurowany JDK 8 lub nowszy.  
2. **Aspose.CAD for Java** – Pobierz najnowszy plik JAR z [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Importowanie przestrzeni nazw

`com.aspose.cad.Image` jest klasą podstawową reprezentującą dowolny plik CAD w pamięci. `com.aspose.cad.imageoptions.*` dostarcza obiekty opcji dla każdego formatu rastrowego. Zaimportuj klasy potrzebne do wczytania rysunku, skonfigurowania rasteryzacji i zapisania wyniku.

> **Pro tip:** Jeśli planujesz **eksportować CAD jako PNG** zamiast TIFF, zamień `TiffOptions` na `PngOptions` (znajdujące się w `com.aspose.cad.imageoptions.PngOptions`).

## Przewodnik krok po kroku

### Krok 1: skonfiguruj katalog zasobów

Zastąp `"Your Document Directory"` absolutną ścieżką, w której znajdują się Twoje pliki CAD. Ten katalog będzie używany zarówno do plików wejściowych, jak i wyjściowych.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Krok 2: wczytaj plik CAD

`Image.load` parsuje plik źródłowy i tworzy reprezentację w pamięci, którą możesz rasteryzować. Możesz wczytać dowolny obsługiwany format (DWG, DXF, DGN itp.) – to jest część **how to convert cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Krok 3: skonfiguruj opcje rasteryzacji

`CadRasterizationOptions` określa, jak dane wektorowe są przekształcane w piksele. `setPageWidth` i `setPageHeight` kontrolują rozdzielczość wyjścia (większe wartości = wyższe DPI). `setLayouts` umożliwia **convert CAD to raster** dla konkretnych układów; pomiń ją, aby rasteryzować cały rysunek.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Krok 4: ustaw opcje obrazu

`TiffOptions` (lub `PngOptions` dla PNG) informuje Aspose, jaki format rastrowy wygenerować i pozwala precyzyjnie dostroić kompresję, głębię kolorów oraz inne ustawienia specyficzne dla formatu. Wybierz klasę opcji odpowiadającą pożądanemu wynikowi.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Krok 5: zapisz powstały obraz

Wywołaj `save` na instancji `Image`, przekazując nazwę pliku wyjściowego oraz obiekt opcji. Zmień rozszerzenie pliku na `.png` (i użyj `PngOptions`), aby **save CAD as PNG**. Ten sam schemat działa dla JPEG, BMP lub PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Typowy problem:** Zapomnienie dopasowania rozszerzenia pliku do klasy opcji spowoduje `UnsupportedFormatException`. Zawsze utrzymuj je w synchronizacji.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|---------|-------------|
| **Blank output image** | Sprawdź, czy nazwy układów w `setLayouts` dokładnie odpowiadają tym w źródłowym pliku CAD. |
| **Low‑resolution PNG** | Zwiększ `setPageWidth` / `setPageHeight` lub ustaw `setResolution` w opcjach rasteryzacji. |
| **Unsupported DWG version** | Upewnij się, że używasz najnowszej wersji Aspose.CAD; starsze wydania mogą nie obsługiwać nowszych wersji DWG. |
| **Memory errors on large files** | Przetwarzaj strony pojedynczo lub zwiększ przydział pamięci JVM (`-Xmx2g`). |

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny z różnymi formatami plików CAD?**  
A: Tak, obsługuje ponad 30 formatów CAD i rastrowych, w tym DWG, DXF, DGN i SVG.

**Q: Czy mogę dostosować rozdzielczość wyjściowego obrazu rastrowego?**  
A: Oczywiście. Dostosuj `setPageWidth`, `setPageHeight` lub `setResolution` w `CadRasterizationOptions`, aby uzyskać wymaganą wartość DPI.

**Q: Jak mogę skonwertować wiele układów CAD w jednym uruchomieniu?**  
A: Przekaż tablicę ze wszystkimi nazwami układów do `setLayouts`, np. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Czy obsługiwane są formaty wyjściowe oprócz TIFF?**  
A: Tak — dostępne są PNG, JPEG, BMP, PDF i inne poprzez ich odpowiednie klasy `*Options`.

**Q: Gdzie mogę uzyskać pomoc lub podzielić się doświadczeniami z Aspose.CAD?**  
A: Odwiedź [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) aby uzyskać wsparcie społeczności i oficjalną pomoc.

## Podsumowanie

Postępując zgodnie z tymi krokami, możesz **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, lub generować dowolny inny potrzebny format rastrowy. Aspose.CAD for Java zajmuje się ciężką pracą, pozwalając Ci skupić się na integrowaniu wysokiej jakości obrazów w Twoich aplikacjach, dokumentacji lub portalach internetowych. Obsługa ponad 30 formatów oraz możliwość renderowania rysunków o setkach stron bez ładowania całego pliku do pamięci czynią tę bibliotekę solidnym wyborem dla przedsiębiorstw wymagających rasteryzacji CAD.

---

**Ostatnia aktualizacja:** 2026-10-04  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Powiązane samouczki

- [Szybki eksport DWG do PDF lub formatu rastrowego przy użyciu biblioteki java cad Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Konwertuj DWG do BMP przy użyciu Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Eksport DWG do PDF: konkretny układ przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}