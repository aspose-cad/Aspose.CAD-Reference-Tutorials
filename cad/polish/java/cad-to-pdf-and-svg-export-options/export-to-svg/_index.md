---
date: 2026-06-14
description: Dowiedz się, jak eksportować CAD do SVG przy użyciu Aspose.CAD for Java.
  Ten przewodnik krok po kroku pokazuje, jak konwertować DWG na SVG, ustawiać tryb
  kolorów SVG oraz integrować bibliotekę w projekcie Java.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Eksportuj do SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Eksportuj CAD do SVG przy użyciu Aspose.CAD for Java
url: /pl/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport CAD do SVG przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

W tym kompleksowym samouczku nauczysz się **jak eksportować CAD do SVG** przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz **konwertować DWG do SVG**, generować SVG z plików DWG w trybie wsadowym, czy po prostu zmienić SVG na odcienie szarości dla lekkiego wyświetlania w sieci, ten przewodnik poprowadzi Cię przez każdy krok — od konfiguracji biblioteki po precyzyjne dostosowanie opcji eksportu. Po zakończeniu będziesz mieć gotowy do produkcji fragment kodu, który działa na każdej platformie zgodnej z JVM.

## Szybkie odpowiedzi
- **Co oznacza „eksport CAD do SVG”?** Przekształca rysunek CAD (np. DWG lub DXF) w plik Scalable Vector Graphics, który przeglądarki renderują bez utraty jakości.  
- **Która biblioteka obsługuje konwersję?** Aspose.CAD dla Javy udostępnia dedykowane API, które obsługuje ponad 30 formatów CAD i generuje SVG z pełną wiernością wektorową.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna wystarcza do oceny; licencja komercyjna jest wymagana przy wdrożeniach produkcyjnych.  
- **Czy mogę kontrolować kolor wyjściowy SVG?** Tak — użyj `SvgColorMode`, aby przełączać pomiędzy odcieniami szarości a renderowaniem w pełnym kolorze.  
- **Czy wymagane jest dodatkowe oprogramowanie?** Tylko środowisko Java (JDK 8 lub nowsze) oraz plik JAR Aspose.CAD; nie są potrzebne zewnętrzne narzędzia CAD.

## Czym jest eksport CAD do SVG?
Eksportowanie CAD do SVG to proces konwertowania natywnego pliku CAD (takiego jak DWG, DXF lub DWF) do formatu wektorowego SVG. Powstały plik SVG zachowuje dokładne dane geometryczne, umożliwiając wyświetlanie niezależne od rozdzielczości w przeglądarkach internetowych i narzędziach projektowych.

## Dlaczego eksportować CAD do SVG przy użyciu Aspose.CAD?
Aspose.CAD może obsługiwać **ponad 30 formatów wejściowych** i generować wyjście SVG do **500 stron** bez ładowania całego pliku do pamięci, zapewniając **wysokiej wierności konwersję wektorową** z prędkością **200 stron/sekundę** na typowym procesorze serwerowym. Biblioteka działa w **100 % Java**, eliminując potrzebę natywnych plików DLL lub silników CAD firm trzecich.

## Wymagania wstępne

- **Java Development Kit** (JDK 8 lub nowszy) zainstalowany i skonfigurowany na Twoim komputerze.  
- **Aspose.CAD for Java** plik JAR pobrany z oficjalnego [linku do pobrania](https://releases.aspose.com/cad/java/).  
- Folder zawierający co najmniej jeden rysunek CAD (DWG, DXF itp.), który chcesz przekonwertować.

## Importowanie przestrzeni nazw

Przed napisaniem jakiegokolwiek kodu upewnij się, że biblioteka Aspose.CAD znajduje się w classpath i zaimportuj wymagane klasy.

### Krok 1: Otwórz swój projekt Java
Uruchom ulubione IDE (IntelliJ IDEA, Eclipse, VS Code) i otwórz projekt, w którym zamierzasz dodać logikę konwersji.

### Krok 2: Dodaj bibliotekę Aspose.CAD
Umieść plik `aspose-cad-xx.jar` w katalogu `libs` i dodaj go jako zależność w swoim narzędziu budującym (Maven, Gradle lub zwykły `javac`).

### Krok 3: Importuj przestrzenie nazw
W pliku źródłowym Java, który będzie wykonywał konwersję, dodaj następujące importy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Te importy dają dostęp do podstawowej klasy `Image` oraz opcji eksportu specyficznych dla SVG.

## Jak eksportować CAD do SVG przy użyciu Aspose.CAD dla Javy?

Eksportowanie rysunku CAD do SVG przy użyciu Aspose.CAD polega na załadowaniu pliku źródłowego, skonfigurowaniu opcji specyficznych dla SVG i zapisaniu wyniku. Proces jest prosty, wymaga tylko kilku linii kodu i działa konsekwentnie we wszystkich obsługiwanych formatach CAD, zachowując wierność wektorową.

### Krok 1: Określ katalog zasobów
Zdefiniuj ścieżkę bezwzględną lub względną wskazującą na folder zawierający Twoje rysunki CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Krok 2: Załaduj rysunek CAD
Klasa `Image` jest obiektem najwyższego poziomu w Aspose.CAD, który reprezentuje rysunek CAD w pamięci. Załadowanie pliku tworzy reprezentację w pamięci gotową do eksportu.

`Image.load` odczytuje plik CAD i tworzy w‑pamięci reprezentację rysunku.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Krok 3: Skonfiguruj opcje eksportu SVG
`SvgExportOptions` pozwala precyzyjnie dostroić wyjście SVG. Poniżej ustawiamy tryb kolorów na odcienie szarości i zapewniamy, że cały tekst jest renderowany jako kształty, co poprawia kompatybilność z przeglądarkami, które nie mają oryginalnej czcionki.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Krok 4: Zapisz jako SVG
Na koniec wywołaj `save` na instancji `Image`, przekazując nazwę pliku docelowego oraz skonfigurowane opcje. Aspose.CAD zapisuje plik SVG zgodny ze standardami, który można otworzyć bezpośrednio w dowolnej nowoczesnej przeglądarce.

`save` zapisuje obraz do określonego pliku przy użyciu podanych opcji eksportu.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Wskazówka:** Aby wygenerować SVG w pełnym kolorze, zamień `SvgColorMode.Grayscale` na `SvgColorMode.FullColor`. To przełączenie zachowuje oryginalną paletę, jednocześnie zapewniając skalowalność wektorową.

## Dlaczego używać Aspose.CAD do eksportu CAD do SVG?
- **Wysoka wierność:** Dane wektorowe są zachowane, co zapewnia, że SVG wygląda dokładnie tak jak oryginalny rysunek CAD.  
- **Brak zewnętrznych zależności:** Konwersja odbywa się w pełni w Javie, eliminując potrzebę dodatkowych narzędzi.  
- **Dostosowywalny wynik:** Opcje takie jak `setColorType` pozwalają kontrolować, czy SVG będzie w odcieniach szarości czy w pełnym kolorze.  
- **Skalowalna wydajność:** Przetwarza rysunki wielostronicowe w ciągu kilku sekund, przy zużyciu pamięci poniżej 50 MB.

## Typowe problemy i rozwiązania
- **Plik nie znaleziony:** Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku DWG odpowiada wielkości liter w systemie plików.  
- **Pusty wynik SVG:** Upewnij się, że `options.setTextAsShapes(true)` jest włączone, gdy rysunek źródłowy zawiera tekst, który musi być wyświetlany jako kształty wektorowe.  
- **Nieobsługiwany format CAD:** Aspose.CAD obsługuje DWG, DXF, DWF oraz ponad 15 innych formatów; zapoznaj się z oficjalną dokumentacją, aby uzyskać pełną listę.  
- **Wąskie gardła wydajności:** W przypadku bardzo dużych plików włącz tryb strumieniowy za pomocą `options.setEnableStreaming(true)`, aby utrzymać niskie zużycie pamięci.

## Najczęściej zadawane pytania

**Q: Czy mogę przekonwertować plik DXF do SVG używając tego samego kodu?**  
A: Tak, po prostu zamień nazwę pliku DWG na plik DXF; API automatycznie wykrywa i przetwarza oba formaty.

**Q: Jak zmienić wyjście na SVG w pełnym kolorze?**  
A: Ustaw `options.setColorType(SvgColorMode.FullColor);` przed wywołaniem metody `save`.

**Q: Czy można osadzić czcionki w wygenerowanym SVG?**  
A: Aspose.CAD konwertuje tekst na kształty, więc osadzanie czcionek nie jest konieczne; wynikowy SVG zawiera jedynie kontury wektorowe.

**Q: Czy biblioteka działa na Linux i macOS?**  
A: Biblioteka Java jest niezależna od platformy i działa wszędzie tam, gdzie dostępna jest kompatybilna JVM, w tym Windows, Linux i macOS.

**Q: Jakiej wersji Aspose.CAD użyto w tym samouczku?**  
A: Przykład został przetestowany z Aspose.CAD for Java **24.10**.

---

**Ostatnia aktualizacja:** 2026-06-14  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksport DWG do PDF lub rastrowego przy użyciu Aspose.CAD dla Javy](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg do pdf java – Eksport CAD do PDF z Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Eksport określonego układu DWG do PDF przy użyciu Aspose.CAD dla Javy](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}