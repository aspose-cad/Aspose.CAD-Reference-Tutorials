---
date: 2026-10-19
description: Dowiedz się, jak tworzyć pliki miniatur PNG IFC przy użyciu Aspose.CAD
  for Java w kilku linijkach kodu.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Eksportuj IFC do PNG
og_description: Twórz pliki miniatur PNG IFC bez wysiłku przy użyciu Aspose.CAD for
  Java. Ten przewodnik krok po kroku pokazuje, jak wczytać, rasteryzować i zapisać
  modele IFC jako obrazy PNG wysokiej jakości.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Utwórz miniaturę PNG IFC przy użyciu Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Jak utworzyć miniaturę PNG IFC przy użyciu Aspose.CAD for Java
url: /pl/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj IFC do PNG przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

W tym samouczku dowiesz się, jak **tworzyć miniatury PNG IFC** przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz szybkich podglądów dla portalu BIM, generujesz miniatury dla systemu zarządzania dokumentami, czy automatyzujesz konwersje wsadowe, poniższe kroki pozwolą Ci rasteryzować model 3‑D IFC do wyraźnego obrazu 2‑D PNG w zaledwie kilku linijkach kodu Java.

## Szybkie odpowiedzi
- **Jakiej biblioteki wymaga?** Aspose.CAD for Java.  
- **Czy mogę stworzyć miniaturę PNG IFC w kilku linijkach kodu?** Tak – cały przepływ mieści się w mniej niż 20 linijkach.  
- **Czy potrzebuję licencji do produkcji?** Tymczasowa licencja działa w testach; pełna licencja jest wymagana do komercyjnego wdrożenia.  
- **Czy wynik jest skalowalny?** Możesz ustawić dowolne wymiary w pikselach, więc PNG skaluje się do dowolnego potrzebnego rozmiaru.  
- **Jaką wersję Javy obsługuje?** Java 8 lub wyższą.

## Co to jest „convert IFC to PNG”?
Konwersja IFC (Industry Foundation Classes) do PNG oznacza rasteryzację trójwymiarowego modelu budynku do dwuwymiarowego obrazu bitmapowego. Ten proces tworzy wizualną miniaturę, którą można wyświetlać w przeglądarkach, raportach lub aplikacjach mobilnych bez konieczności posiadania pełnego przeglądarki CAD.

## Dlaczego warto używać Aspose.CAD dla Javy?
Aspose.CAD obsługuje **ponad 30 formatów CAD i BIM**, w tym IFC, DWG, DXF i DGN, i może przetwarzać pliki do **2 GB** bez wczytywania całego dokumentu do pamięci. Biblioteka jest czystą Javą, ma **zero zewnętrznych zależności** i działa na Windows, Linux oraz macOS, co czyni ją idealną do generowania obrazów po stronie serwera.  
Zapewnia wysokowydajną rasteryzację, szerokie wsparcie formatów i łatwą integrację z aplikacjami Java.

## Wymagania wstępne
- **Aspose.CAD Library** – pobierz najnowszy JAR z [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 lub nowszy zainstalowany na Twoim komputerze.  
- **Plik źródłowy IFC** – umieść plik w folderze, do którego możesz odwoływać się w kodzie.

## Importuj przestrzenie nazw

Pakiet `com.aspose.cad` dostarcza wszystkie potrzebne klasy. `CadImage` jest punktem wejścia do ładowania plików CAD, natomiast `PngOptions` konfiguruje ustawienia rasteryzacji.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Jak stworzyć miniaturę PNG IFC w Javie?

Załaduj plik IFC, zdefiniuj opcje rasteryzacji i zapisz wynik jako obraz PNG – to kompletny przepływ konwersji. Poniższe sekcje rozkładają każdy krok, abyś mógł skopiować‑wkleić fragmenty do swojego projektu i uruchomić je od razu.

### Krok 1: załaduj plik IFC
Najpierw wskaż folder, w którym znajduje się Twój plik IFC i załaduj go za pomocą `CadImage.load`.  
`CadImage.load` odczytuje plik CAD i zwraca obiekt obrazu, który może być rasteryzowany.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Dlaczego to ważne:** Ładowanie pliku jako `CadImage` daje dostęp do opcji konwersji wektor‑raster, które kontrolują rozdzielczość, kolor tła i grubość linii.

### Krok 2: ustaw opcje rasteryzacji
Zdefiniuj wymiary wyjściowe oraz inne ustawienia związane z wektorem za pomocą `VectorRasterizationOptions`.  
`VectorRasterizationOptions` pozwala określić rozmiar wyjścia, kolor tła i inne parametry rasteryzacji.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Dostosuj `PageWidth` i `PageHeight`, aby kontrolować ostateczną rozdzielczość PNG, co jest niezbędne, gdy **zapisujesz pliki PNG java** dla wysokiej jakości wydruków lub miniatur internetowych.

### Krok 3: skonfiguruj opcje PNG
Połącz opcje rasteryzacji z eksporterem PNG, tworząc instancję `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Krok 4: zapisz obraz jako PNG
Na koniec zapisz rasteryzowany obraz na dysku przy użyciu metody `save`.  
`save` zapisuje rasteryzowany obraz do określonej ścieżki pliku w wybranym formacie.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Po tym kroku pomyślnie **utworzyłeś miniaturę PNG IFC** i możesz używać powstałego `example.png` wszędzie tam, gdzie potrzebny jest obraz rastrowy.

## Typowe przypadki użycia
- **Generowanie miniatur** dla modeli BIM w portalach internetowych.  
- **Wstawianie zrzutów planów pięter** do raportów PDF lub Word.  
- **Automatyczna konwersja wsadowa** dużych bibliotek IFC w celach archiwizacji lub migracji.

## Rozwiązywanie problemów i wskazówki
- **Problemy z pamięcią:** Dla bardzo dużych plików IFC zwiększ przydział pamięci JVM (`-Xmx2g` lub wyższy).  
- **Brakujące tekstury:** Upewnij się, że zewnętrzne zasoby pliku IFC są dostępne z `dataDir`.  
- **Pro tip:** Użyj `vectorOptions.setBackgroundColor(Color.getWhite())`, jeśli wolisz białe tło zamiast domyślnego przezroczystego PNG.

## FAQ

### Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików IFC?
A1: Aspose.CAD obsługuje różne wersje IFC. Odwołaj się do [documentation](https://reference.aspose.com/cad/java/) po szczegółowe informacje o kompatybilności.

### Q2: Czy mogę dalej dostosować opcje rasteryzacji?
A2: Oczywiście! Przejrzyj [documentation](https://reference.aspose.com/cad/java/) po zaawansowane ustawienia, takie jak kontrola DPI, antyaliasing i grubość linii.

### Q3: Czy dostępna jest wersja próbna?
A3: Tak, możesz pobrać darmową wersję próbną z [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: Jak mogę uzyskać tymczasową licencję do testów?
A4: Uzyskaj tymczasową licencję na [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: Gdzie mogę zadawać pytania lub zgłaszać problemy?
A5: Dołącz do społeczności na [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie od inżynierów Aspose oraz innych programistów.

## Często zadawane pytania

**Q: Czy mogę użyć tego podejścia do konwersji innych formatów CAD do PNG?**  
A: Tak, Aspose.CAD obsługuje wiele formatów (DWG, DXF, DGN itp.). Po prostu zmień rozszerzenie pliku i załaduj odpowiednią klasę obrazu.

**Q: Czy biblioteka pozwala ustawić własne DPI?**  
A: DPI jest kontrolowane pośrednio przez `PageWidth`/`PageHeight`. Dostosuj te wartości względem pożądanego rozmiaru fizycznego, aby uzyskać wymaganą rozdzielczość DPI.

**Q: Czy wyjście PNG jest bezstratne?**  
A: PNG jest formatem bezstratnym, więc rasteryzowany obraz zachowuje pełną wierność wizualną oryginalnych danych wektorowych.

## Podsumowanie

Masz teraz kompletną, gotową do produkcji metodę **tworzenia miniatur PNG IFC** przy użyciu Aspose.CAD dla Javy. Zintegruj te kroki z narzędziami desktopowymi, usługami po stronie serwera lub funkcjami w chmurze, aby automatyzować pipeline'y wizualizacji BIM i dostarczać szybkie, wysokiej jakości miniatury użytkownikom końcowym.

---

**Ostatnia aktualizacja:** 2026-10-19  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

## Powiązane samouczki

- [Jak przekonwertować STL do PNG przy użyciu Aspose.CAD dla Javy](/cad/java/cad-export-options/export-stl-to-png/)
- [Konwersja DWG do PNG – Zapisz CAD jako PNG przy użyciu Aspose.CAD dla Javy](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Eksport DWG do PDF w Javie – Ustaw rozmiar strony PDF przy użyciu Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}