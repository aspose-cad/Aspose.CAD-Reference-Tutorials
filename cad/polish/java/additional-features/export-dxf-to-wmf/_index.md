---
date: 2026-06-09
description: Dowiedz się, jak konwertować DXF do WMF przy użyciu Aspose.CAD dla Javy,
  w tym darmowa wersja próbna, wsparcie Java 8+ oraz opcjonalny eksport do PDF. Przewodnik
  krok po kroku z przykładami kodu.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Eksportuj DXF do formatu WMF przy użyciu Javy
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konwertuj DXF do WMF przy użyciu Aspose.CAD w Javie
url: /pl/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie DXF do WMF przy użyciu Aspose.CAD w Javie

## Wprowadzenie

W tym samouczku dowiesz się, jak **konwertować DXF do WMF** przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz osadzić rysunki CAD w raporcie opartym na Windows, generować lekkie grafiki wektorowe do dokumentów Office, czy automatyzować konwersje wsadowe, konwertowanie DXF do WMF jest częstym wymogiem w inżynierii i pipeline'ach raportowania. Przeprowadzimy Cię przez ładowanie rysunku DXF, konfigurowanie opcji rasteryzacji, zapisywanie wyniku jako WMF oraz opcjonalny eksport tego samego rysunku do PDF.

## Szybkie odpowiedzi
- **Czy mogę konwertować DXF do WMF w wersji próbnej?** Tak – Aspose oferuje w pełni funkcjonalną 30‑dniową wersję próbną.  
- **Jakiej wersji Javy wymaga?** Java 8 lub nowsza.  
- **Czy potrzebna jest licencja do uruchomienia kodu?** Licencja jest wymagana w środowisku produkcyjnym; wersja próbna działa w fazie rozwoju i testowania.  
- **Czy konwersja jest bezstratna?** Dane wektorowe są zachowane; opcje rasteryzacji pozwalają kontrolować rozdzielczość.  
- **Czy mogę również wyeksportować ten sam rysunek do PDF?** Oczywiście – zobacz krok „Eksport do PDF” poniżej.

## Co to jest „konwertować DXF do WMF”?

Konwertowanie DXF do WMF oznacza wzięcie pliku w formacie Drawing Exchange Format (DXF) — powszechnie używanego formatu CAD — i przekształcenie go w Windows Metafile (WMF). WMF jest formatem obrazu wektorowego, który płynnie integruje się z Microsoft Office, aplikacjami Windows oraz wieloma narzędziami raportującymi.

## Dlaczego używać Aspose.CAD dla Javy?

Aspose.CAD dla Javy zapewnia czysto‑Java, bez natywnych DLL silnik, który konwertuje pliki CAD z **ponad 99 % wiernością wektorową**, zachowując warstwy, kolory, style linii i wzory kreskowania. Obsługuje **ponad 50 formatów wejściowych i wyjściowych** — w tym DXF, DWG, DGN, PDF, PNG, SVG i WMF — umożliwiając precyzyjne dostosowanie rozmiaru strony, DPI i koloru tła za pomocą wbudowanych opcji rasteryzacji. To samo API obsługuje eksport do PDF, PNG i SVG, eliminując potrzebę wielu bibliotek.

### Kluczowe zalety
- **Brak zewnętrznych zależności** – czysta Java, działa na każdym systemie operacyjnym obsługującym Javę.  
- **Renderowanie o wysokiej wierności** – zachowuje grubość linii, kolor i szczegóły kreskowania.  
- **Wbudowana rasteryzacja** – kontrola wymiarów strony, rozdzielczości i tła.  
- **Jedno‑stopniowa konwersja** – te same klasy eksportują do WMF, PDF, PNG, SVG itp.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- **Aspose.CAD dla Javy** zintegrowany w swoim projekcie. Pobierz go z oficjalnej strony: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Katalog dokumentów**, w którym przechowywane są pliki DXF (np. `Your Document Directory/DXFDrawings/`).

## Importowanie przestrzeni nazw

Następujące importy wprowadzają klasy Aspose.CAD niezbędne do ładowania, rasteryzacji i zapisywania plików CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Przewodnik krok po kroku

### Jak konwertować DXF do WMF w Javie?

Załaduj swój plik DXF przy użyciu `Image.load("yourFile.dxf")`, skonfiguruj `CadRasterizationOptions` dla żądanego rozmiaru strony i DPI, a następnie wywołaj `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Ten trzyetapowy schemat wykonuje pełną konwersję, zachowując jakość wektorową i wymaga tylko kilku linii kodu.

#### Krok 1: Załaduj rysunek DXF

`Image.load` odczytuje plik DXF do obiektu Aspose.CAD Image.

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Krok 2: Skonfiguruj opcje rasteryzacji

`CadRasterizationOptions` określa rozmiar strony, rozdzielczość i tło przy rasteryzacji rysunku CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Krok 3: Zapisz jako WMF

`ImageSaveOptions` z `SaveFormat.WMF` instruuje Aspose.CAD, aby zapisał wynik jako Windows Metafile.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Krok 4: Zwolnij zasoby

Wywołanie `image.close()` zwalnia natywne zasoby używane przez obiekt Aspose.CAD Image.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Krok 5: Opcjonalnie – Eksport do PDF

`PdfOptions` konfiguruje ustawienia specyficzne dla PDF przy zapisywaniu obrazu jako dokument PDF.

```java
finally
{
  cadImage.dispose();
}
```

> **Wskazówka:** Możesz ponownie użyć tego samego obiektu `CadRasterizationOptions` przy eksporcie do PDF, przekazując go do instancji `PdfOptions`, co zaoszczędzi kilka linii konfiguracji.

## Jak wyeksportować DXF do PDF przy użyciu Aspose CAD Java?

Eksport do PDF odbywa się według tych samych kroków ładowania i rasteryzacji; wystarczy zamienić format zapisu WMF na PDF. Użyj `new ImageSaveOptions(SaveFormat.Pdf)` i opcjonalnie ustaw opcje specyficzne dla PDF, takie jak poziom kompresji czy metadane autora. Ta jednowierszowa konwersja tworzy przeszukiwalny, dokładny pod względem stron PDF, który odzwierciedla oryginalny układ CAD.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **`NullPointerException` przy `cadImage.save`** | Zmienna `cadImage` nie jest zdefiniowana (powinna być `image`). | Zastąp `cadImage` przez `image` lub konsekwentnie zmień nazwę zmiennej. |
| **Wyjściowy WMF jest pusty** | Rozmiar strony rasteryzacji jest zbyt mały lub kolor tła ustawiony na przezroczysty. | Zwiększ `PageWidth`/`PageHeight` lub ustaw kolor tła za pomocą `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji Aspose w środowisku produkcyjnym. | Zastosuj plik licencji przy starcie aplikacji: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Podsumowanie

Masz teraz kompletny, gotowy do produkcji przepływ pracy, aby **konwertować DXF do WMF** przy użyciu Aspose.CAD dla Javy, z opcjonalnym krokiem **eksportu tego samego rysunku do PDF**. To podejście zapewnia wysokiej jakości wyjście wektorowe, które płynnie integruje się z narzędziami raportowania i dokumentacji opartymi na Windows, jednocześnie utrzymując bazę kodu prostą i wolną od zależności.

## Najczęściej zadawane pytania

### Q1: Gdzie mogę znaleźć dokumentację Aspose.CAD?
A1: Dokumentację można uzyskać [tutaj](https://reference.aspose.com/cad/java/).

### Q2: Jak pobrać Aspose.CAD dla Javy?
A2: Pobierz bibliotekę [tutaj](https://releases.aspose.com/cad/java/).

### Q3: Czy dostępna jest wersja próbna?
A3: Tak, darmową wersję próbną można uzyskać [tutaj](https://releases.aspose.com/).

### Q4: Potrzebujesz tymczasowych opcji licencjonowania?
A4: Zapoznaj się z tymczasowymi licencjami [tutaj](https://purchase.aspose.com/temporary-license/).

### Q5: Gdzie mogę uzyskać wsparcie?
A5: Odwiedź forum wsparcia Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19).

## Często zadawane pytania

**Q: Czy mogę konwertować duże pliki DXF (setki MB) bez wyczerpania pamięci?**  
A: Tak. Ładuj plik w bloku try‑with‑resources i szybko zwalniaj obiekt `Image`. Dostosuj `CadRasterizationOptions.setPageWidth/Height` do rozsądnego rozmiaru, aby utrzymać niskie zużycie pamięci.

**Q: Czy wyjście WMF zachowuje informacje o warstwach?**  
A: WMF jest płaskim formatem wektorowym, więc hierarchia warstw jest spłaszczona, ale style linii, kolory i wzory kreskowania są zachowane.

**Q: Czy można ustawić własne DPI dla WMF?**  
A: Użyj `rasterizationOptions.setResolution(300);`, aby określić DPI przed zapisem.

**Q: Czy mogę konwertować wsadowo wiele plików DXF w jednym uruchomieniu?**  
A: Oczywiście. Przejdź pętlą po katalogu, załaduj każdy plik i zastosuj tę samą logikę rasteryzacji i zapisu.

**Q: Jakie wersje Javy są obsługiwane?**  
A: Aspose.CAD dla Javy obsługuje Javę 8 i nowsze, w tym Java 11, 17 oraz nowsze wydania LTS.

---

**Ostatnia aktualizacja:** 2026-06-09  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Powiązane samouczki

- [Utwórz PDF z CAD – Eksportuj DXF do PDF przy użyciu Aspose.CAD dla Javy](/cad/java/additional-features/export-dxf-to-pdf/)
- [Utwórz PDF z DXF: Eksportuj warstwę przy użyciu Aspose.CAD dla Javy](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Jak konwertować układ DXF na obraz JPEG przy użyciu Aspose.CAD w Javie](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}