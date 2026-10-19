---
date: 2026-10-19
description: Dowiedz się, jak wyeksportować rysunki AutoCAD do formatu PDF z niestandardowym
  rozmiarem strony PDF przy użyciu Aspose.CAD for Java. Ten przewodnik krok po kroku
  opisuje konwersję DWG do PDF, opcje rasteryzacji oraz licencjonowanie.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Eksportuj obrazy AutoCAD do PDF
og_description: Ustaw niestandardowy rozmiar strony PDF podczas eksportu rysunków
  AutoCAD do PDF przy użyciu Aspose.CAD for Java. Dowiedz się, jak w kilka minut wykonać
  konwersję DWG do PDF, ustawić opcje rasteryzacji i zarządzać licencjonowaniem.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Ustaw niestandardowy rozmiar strony PDF przy eksporcie AutoCAD przy użyciu
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Ustaw niestandardowy rozmiar strony PDF przy eksporcie AutoCAD przy użyciu
  Aspose.CAD
url: /pl/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport AutoCAD PDF - eksportowanie obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **konwertować DWG do PDF** i kontrolować dokładne wymiary pliku wyjściowego, trafiłeś we właściwe miejsce. Ten samouczek pokazuje, jak ustawić **niestandardowy rozmiar strony PDF** podczas eksportowania obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Javy. Po zakończeniu przewodnika będziesz wiedział, jak załadować plik DWG, skonfigurować opcje rasteryzacji takie jak DPI oraz szerokość/wysokość strony, zastosować licencję i wygenerować gotowy do produkcji PDF.

## Szybkie odpowiedzi
- **Czy mogę konwertować DWG do PDF przy użyciu Javy?** Tak – Aspose.CAD dla Javy natywnie obsługuje formaty DWG, DXF, DWF i wiele innych formatów CAD.  
- **Czy potrzebuję licencji do użytku produkcyjnego?** Pełna licencja Aspose.CAD usuwa wszystkie ograniczenia wersji ewaluacyjnej; tymczasowa licencja jest dostępna do testów.  
- **Które wersje Javy są kompatybilne?** Biblioteka działa z Java 8 i dowolnym późniejszym JDK.  
- **Jak zmienić wymiary strony PDF?** Ustaw `pageWidth` i `pageHeight` w `PdfOptions.getRasterizationOptions()` na dowolny wymagany rozmiar.  
- **Czy renderowanie 3‑D jest wspierane?** Tak – włącz `TypeOfEntities.Entities3D`, aby rasteryzować obiekty 3‑D.

## Co to jest eksport AutoCAD PDF?
Eksportowanie AutoCAD PDF oznacza konwersję wektorowych rysunków CAD (DWG, DXF, DWF itp.) do przenośnego dokumentu PDF przy zachowaniu warstw, grubości linii oraz opcjonalnej geometrii 3‑D. Umożliwia to udostępnianie projektów klientom, archiwizowanie rysunków lub drukowanie bez instalacji oprogramowania CAD.

## Dlaczego warto używać Aspose.CAD dla Javy do konwersji DWG do PDF?
Aspose.CAD dla Javy jest idealny do konwersji DWG do PDF, ponieważ oferuje szerokie wsparcie formatów, działa w czystej Javie bez zależności natywnych, zapewnia wysokiej rozdzielczości rasteryzację z pełną kontrolą nad DPI i rozmiarem strony oraz zawiera elastyczne licencjonowanie, które pozwala rozpocząć od wersji próbnej i przejść do produkcji.

- **Szerokie pokrycie formatów** – obsługuje ponad 50 formatów wejściowych i wyjściowych, w tym DWG, DXF, DWF, DGN i PDF.  
- **Czysta implementacja w Javie** – brak natywnych DLL‑ów ani zewnętrznych zależności, więc wdrożenie jest proste na każdej platformie.  
- **Rasteryzacja wysokiej rozdzielczości** – możesz określić DPI, rozmiar strony i układ, dając pełną kontrolę nad **niestandardowym rozmiarem strony PDF** wyniku.  
- **Skalowalne licencjonowanie** – rozpocznij od darmowej wersji próbnej, a następnie przejdź do stałej **licencji Aspose CAD**.  

## Wymagania wstępne

- **Java Development Kit** – JDK 8 lub nowszy zainstalowany na Twoim komputerze.  
- **Aspose.CAD for Java** – pobierz najnowszy plik JAR z [download link](https://releases.aspose.com/cad/java/).  
- **Katalog roboczy** – folder zawierający pliki DWG źródłowe i będący miejscem docelowym dla wygenerowanych plików PDF.

## Importowanie przestrzeni nazw

Klasa `Image` jest podstawowym obiektem Aspose.CAD, który reprezentuje rysunek CAD w pamięci. Zaimportuj wymagane pakiety przed rozpoczęciem kodowania.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Teraz przejdźmy krok po kroku przez kod.

## Jak ustawić niestandardowy rozmiar strony PDF podczas eksportowania DWG do PDF?

Załaduj swój plik DWG, określ żądaną szerokość i wysokość strony, a następnie zapisz wynik jako PDF – to wszystko, czego potrzebujesz, aby stworzyć PDF o niestandardowym rozmiarze strony. Poniższe kroki ilustrują dokładną kolejność i minimalny wymagany kod.

### Krok 1: ustaw ścieżkę katalogu zasobów

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Wskazówka:** Zastąp `"Your Document Directory"` absolutną ścieżką do folderu, który utworzyłeś w wymaganiach wstępnych.

### Krok 2: załaduj obraz CAD

Klasa `Image` ładuje plik CAD i zapewnia dostęp do silnika rasteryzacji Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Dlaczego to ważne:** Po załadowaniu pliku CAD możesz modyfikować opcje rasteryzacji przed renderowaniem do PDF.

### Krok 3: ustaw opcje rasteryzacji

Klasa `CadRasterizationOptions` określa, jak rysunek CAD jest rasteryzowany przed zapisaniem jako PDF. Dostosuj `pageWidth` i `pageHeight`, aby zdefiniować **niestandardowy rozmiar strony PDF**. Możesz także włączyć renderowanie 3‑D, odkomentowując linię `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – mierzone w pikselach; zmień te wartości, aby dopasować do formatu A4, Letter lub dowolnego niestandardowego wymiaru.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renderuje obiekty 3‑D w razie potrzeby.  
- `setLayouts` – wybiera, który układ (Model, Layout1 itp.) ma zostać rasteryzowany.

### Krok 4: skonfiguruj opcje PDF

Klasa `PdfOptions` zawiera ustawienia specyficzne dla PDF i łączy opcje rasteryzacji z plikiem wyjściowym, zapewniając prawidłowe zastosowanie niestandardowych wymiarów strony.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: zapisz PDF

Metoda `save` zapisuje wyrenderowany obraz do określonego pliku PDF.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Wynikowy plik, `Export3DImagestoPDF_out_.pdf`, jest **zapisanym CAD jako PDF** reprezentacją Twojego oryginalnego rysunku AutoCAD z dokładnie określonymi wymiarami strony.

## Typowe problemy i rozwiązania

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------|-----|
| Pusty plik PDF | Opcje rasteryzacji nie ustawione lub niezgodność układu | Sprawdź, czy `setLayouts` odpowiada nazwie układu w Twoim pliku CAD. |
| Obraz o niskiej rozdzielczości | `pageWidth`/`pageHeight` za małe lub DPI niskie | Zwiększ wymiary lub wywołaj `rasterizationOptions.setResolution(...)` z wyższym DPI. |
| Wyjątek licencyjny | Nie zastosowano ważnej licencji | Zastosuj stałą licencję Aspose.CAD lub użyj tymczasowej licencji do testów. |

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD dla Javy z innymi formatami plików CAD?**  
O: Tak, biblioteka obsługuje DWG, DXF, DWF, DGN i wiele innych, dając elastyczność w różnych projektach.

**P: Jak uzyskać tymczasową licencję dla Aspose.CAD dla Javy?**  
O: Odwiedź [temporary license page](https://purchase.aspose.com/temporary-license/), aby poprosić o czasowo ograniczoną licencję do oceny.

**P: Czy istnieją opcje układu dla rasteryzacji?**  
O: Oczywiście. Użyj `setLayouts("Model")` lub podaj inne nazwy układów, aby kontrolować, który widok jest renderowany.

**P: Czy mogę dostosować rozmiar wyjściowego pliku PDF?**  
O: Tak – zmodyfikuj `pageWidth` i `pageHeight` w opcjach rasteryzacji na dowolne potrzebne wymiary.

**P: Gdzie mogę uzyskać pomoc lub dyskutować problemy związane z Aspose.CAD dla Javy?**  
O: Dedykowane [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) oferuje wsparcie społeczności oraz oficjalne odpowiedzi zespołu Aspose.

## Dodatkowe FAQ (format przyjazny AI)

**P: Czy Aspose.CAD wymaga jakichkolwiek natywnych bibliotek na Windows lub Linux?**  
O: Nie. Aspose.CAD dla Javy jest biblioteką czysto‑Java, więc działa na każdej platformie obsługującej JDK bez dodatkowych natywnych DLL‑ów.

**P: Jak duży plik DWG może przetworzyć biblioteka?**  
O: Biblioteka może obsłużyć rysunki wielostronicowe (do 500 MB) bez wczytywania całego pliku do pamięci, dzięki architekturze strumieniowej.

**P: Czy można wsadowo konwertować wiele plików DWG do PDF w jednym uruchomieniu?**  
O: Tak. Iteruj po katalogu, ładuj każdy plik za pomocą `Image.load()`, zastosuj te same opcje rasteryzacji i wywołaj `save()` dla każdego wyjściowego PDF.

**P: Jaką wydajność mogę oczekiwać na typowym serwerze?**  
O: Konwersja 100‑stronnicowego DWG przy 300 DPI na standardowym procesorze 2,5 GHz zajmuje około 12 sekund, według testów wydajnościowych Aspose.

**P: Czy biblioteka zachowuje informacje o warstwach w PDF?**  
O: Choć wynik jest rasteryzowany, wizualny wygląd warstw, grubości linii i kolorów jest wiernie odtworzony.

---

**Ostatnia aktualizacja:** 2026-10-19  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose

## Powiązane samouczki

- [Eksport DWG do PDF i włączenie śledzenia przy użyciu Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Eksport DWG do PDF: określony układ przy użyciu Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Eksport DWG do BMP i dostosowanie rozmiaru CAD przy użyciu typu jednostki z Aspose.CAD dla Javy](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}