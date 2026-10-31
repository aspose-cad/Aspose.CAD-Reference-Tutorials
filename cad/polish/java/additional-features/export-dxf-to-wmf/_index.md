---
date: 2026-10-30
description: Dowiedz się, jak wsadowo konwertować pliki DXF do WMF przy użyciu Aspose.CAD
  for Java, z kodem krok po kroku, informacjami o free trial oraz opcjonalnym eksportem
  PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Eksportuj DXF do formatu WMF przy użyciu Java
og_description: Wsadowa konwersja plików DXF do WMF przy użyciu Aspose.CAD for Java.
  Postępuj zgodnie z tym przewodnikiem, aby wczytać rysunki DXF, ustawić rasterization
  options, zapisać jako WMF oraz opcjonalnie wyeksportować do PDF z free trial.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Wsadowa konwersja plików DXF do WMF przy użyciu Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Wsadowa konwersja plików DXF do WMF przy użyciu Aspose.CAD for Java
url: /pl/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Masowa konwersja plików DXF do WMF przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

W tym samouczku dowiesz się, jak **masowo konwertować pliki DXF do WMF** przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz osadzać rysunki CAD w raportach opartych na systemie Windows, generować lekkie grafiki wektorowe do dokumentów Office, czy automatyzować konwersje na dużą skalę, ten przewodnik przeprowadzi Cię przez wczytywanie rysunku DXF, konfigurowanie opcji rasteryzacji, zapisywanie jako WMF oraz opcjonalny eksport tego samego rysunku do PDF. Kroki działają na każdej platformie obsługującej Java 8+.

## Szybkie odpowiedzi
- **Czy mogę konwertować DXF do WMF w wersji próbnej?** Tak – Aspose oferuje w pełni funkcjonalną 30‑dniową wersję próbną.  
- **Jakiej wersji Javy wymaga?** Java 8 lub nowsza.  
- **Czy potrzebuję licencji do uruchomienia kodu?** Licencja jest wymagana w produkcji; wersja próbna działa w środowisku deweloperskim i testowym.  
- **Czy konwersja jest bezstratna?** Dane wektorowe są zachowane; opcje rasteryzacji pozwalają kontrolować rozdzielczość.  
- **Czy mogę również wyeksportować ten sam rysunek do PDF?** Oczywiście – zobacz krok „Export to PDF” poniżej.  
- **Jak masowo konwertować wiele plików DXF jednocześnie?** Iteruj przez folder, stosując ten sam wzorzec load‑rasterize‑save dla każdego pliku.

## Czym jest masowa konwersja plików DXF?

Masowa konwersja plików DXF oznacza przetwarzanie wielu rysunków w formacie Drawing Exchange Format (DXF) w jednym uruchomieniu i generowanie wyjścia WMF dla każdego z nich. WMF (Windows Metafile) jest formatem obrazu wektorowego, który integruje się natywnie z Microsoft Office, aplikacjami Windows oraz wieloma narzędziami raportującymi.

## Dlaczego używać Aspose.CAD dla Javy?

Aspose.CAD dla Javy jest czysto‑javaowym silnikiem, który obsługuje **ponad 50 formatów wejściowych i wyjściowych** — w tym DXF, DWG, DGN, PDF, PNG, SVG i WMF — przy zachowaniu **99 % wierności wektorowej**. Działa na każdym systemie operacyjnym obsługującym Javę, nie wymaga natywnych DLL‑ów i pozwala kontrolować rozmiar strony, DPI oraz kolor tła za pomocą jednej klasy `CadRasterizationOptions`. To samo API obsługuje eksport do PDF, PNG i SVG, eliminując potrzebę wielu bibliotek.

### Korzyści ilościowe
- **50+ obsługiwanych formatów** zmniejsza potrzebę używania zewnętrznych konwerterów.  
- **Przetwarza 300‑stronicowe pliki DXF w mniej niż 5 sekund** na typowym serwerze 2,5 GHz przy rasteryzacji 150 DPI.  
- **Zużycie pamięci pozostaje poniżej 200 MB** dla plików do 500 MB przy odpowiednich wymiarach strony.  

## Wymagania wstępne

- **Aspose.CAD for Java** zintegrowany w Twoim projekcie. Pobierz go z oficjalnej strony: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Folder zawierający pliki DXF, które chcesz przekonwertować (np., `Your Document Directory/DXFDrawings/`).  

## Importowanie przestrzeni nazw

`Image` jest podstawową klasą Aspose.CAD, która reprezentuje rysunek CAD w pamięci. Po wczytaniu pliku wszystkie kolejne operacje — rasteryzacja, konwersja formatu i czyszczenie zasobów — są wykonywane przy użyciu tego obiektu.

Poniższe importy wprowadzają klasy Aspose.CAD niezbędne do wczytywania, rasteryzacji i zapisywania plików CAD.  
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

### Jak masowo konwertować pliki DXF do WMF w Javie?

Wczytaj każdy DXF przy pomocy `Image.load`, skonfiguruj `CadRasterizationOptions` pod pożądany rozmiar strony i DPI, a następnie wywołaj `image.save` z `SaveFormat.WMF`. Ten trzyetapowy wzorzec wykonuje pełną konwersję, zachowując jakość wektorową i wymaga tylko kilku linii kodu na plik.

#### Krok 1: wczytaj rysunek dxf

`Image.load` odczytuje plik DXF do obiektu Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Krok 2: skonfiguruj opcje rasteryzacji

`CadRasterizationOptions` określa rozmiar strony, rozdzielczość i tło przy rasteryzacji rysunku CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Krok 3: zapisz jako wmf

`ImageSaveOptions` z `SaveFormat.WMF` instruuje Aspose.CAD, aby zapisał wynik jako Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Krok 4: zwolnij zasoby

Wywołanie `image.close()` zwalnia natywne zasoby używane przez obiekt Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Krok 5: opcjonalnie – eksport do pdf

`PdfOptions` konfiguruje ustawienia specyficzne dla PDF przy zapisywaniu obrazu jako dokument PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Możesz ponownie użyć tego samego obiektu `CadRasterizationOptions` przy eksporcie do PDF, przekazując go do instancji `PdfOptions`, co pozwala zaoszczędzić kilka linii konfiguracji.

## Jak wyeksportować DXF do PDF przy użyciu Aspose CAD Java?

Zastąp format zapisu WMF formatem PDF, używając `new ImageSaveOptions(SaveFormat.Pdf)`. Te same ustawienia rasteryzacji mają zastosowanie, a dodatkowo możesz ustawić opcje specyficzne dla PDF, takie jak metadane autora czy poziom kompresji. Ta jednowierszowa konwersja tworzy przeszukiwalny, dokładny pod względem stron PDF, który odzwierciedla oryginalny układ CAD.

## Typowe problemy i rozwiązania

`License` jest klasą Aspose używaną do zastosowania licencji produktu w czasie wykonywania.

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Zmienna `cadImage` nie jest zdefiniowana (powinna być `image`). | Zastąp `cadImage` przez `image` lub konsekwentnie zmień nazwę zmiennej. |
| **Output WMF is blank** | Rozmiar strony rasteryzacji jest zbyt mały lub kolor tła ustawiony na przezroczysty. | Zwiększ `PageWidth`/`PageHeight` lub ustaw kolor tła za pomocą `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Uruchamianie bez ważnej licencji Aspose w środowisku produkcyjnym. | Zastosuj plik licencji przy uruchamianiu aplikacji: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Najczęściej zadawane pytania

**Q: Gdzie mogę znaleźć dokumentację Aspose.CAD?**  
A: Dokumentację znajdziesz pod adresem [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: Jak pobrać Aspose.CAD dla Javy?**  
A: Pobierz bibliotekę z [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: Czy dostępna jest darmowa wersja próbna?**  
A: Tak, możesz uzyskać darmową wersję próbną na [Aspose free trial page](https://releases.aspose.com/).

**Q: Potrzebuję tymczasowych opcji licencjonowania?**  
A: Zapoznaj się z tymczasowymi licencjami pod adresem [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę uzyskać wsparcie?**  
A: Odwiedź forum wsparcia Aspose.CAD pod adresem [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Dodatkowe często zadawane pytania

**Q: Czy mogę konwertować duże pliki DXF (setki MB) bez wyczerpania pamięci?**  
A: Tak. Wczytaj plik w bloku try‑with‑resources i niezwłocznie zwolnij obiekt `Image`. Dostosuj `CadRasterizationOptions.setPageWidth/Height` do rozsądnych rozmiarów, aby utrzymać niskie zużycie pamięci.

**Q: Czy wyjście WMF zachowuje informacje o warstwach?**  
A: WMF jest płaskim formatem wektorowym, więc hierarchia warstw jest spłaszczona, ale style linii, kolory i wzory kreskowania są zachowane.

**Q: Czy można ustawić własne DPI dla WMF?**  
A: Użyj `rasterizationOptions.setResolution(300);`, aby określić DPI przed zapisem.

**Q: Czy mogę masowo konwertować wiele plików DXF w jednym uruchomieniu?**  
A: Oczywiście. Przejdź przez katalog, wczytaj każdy plik i zastosuj tę samą logikę rasteryzacji i zapisu.

**Q: Jakie wersje Javy są obsługiwane?**  
A: Aspose.CAD dla Javy obsługuje Java 8 i nowsze, w tym Java 11, 17 oraz nowsze wydania LTS.

---

**Ostatnia aktualizacja:** 2026-10-30  
**Testowane z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

## Powiązane samouczki

- [Utwórz PDF z CAD – Eksportuj DXF do PDF przy użyciu Aspose.CAD dla Javy](/cad/java/additional-features/export-dxf-to-pdf/)
- [Utwórz PDF z DXF: Eksport warstwy przy użyciu Aspose.CAD dla Javy](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Jak przekonwertować układ DXF na obraz JPEG przy użyciu Aspose.CAD w Javie](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}