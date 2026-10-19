---
date: 2026-10-19
description: Dowiedz się, jak konwertować DWG na PDF w Javie z Aspose.CAD. Ten krok
  po kroku przewodnik pokazuje, jak eksportować AutoCAD PDF, zapisywać CAD jako PDF
  i zastosować licencję.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Eksportuj obrazy AutoCAD do PDF
og_description: Dowiedz się, jak konwertować DWG na PDF w Javie z Aspose.CAD. Ten
  przewodnik prowadzi Cię przez eksportowanie AutoCAD PDF, zapisywanie CAD jako PDF
  i licencjonowanie.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Konwertuj DWG na PDF w Javie przy użyciu Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Konwertuj DWG na PDF w Javie przy użyciu Aspose.CAD
url: /pl/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport AutoCAD PDF – eksportowanie obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **konwertować DWG do PDF w Javie**, jesteś we właściwym miejscu. Ten samouczek pokazuje, jak eksportować obrazy AutoCAD do PDF przy użyciu Aspose.CAD dla Javy, czystej biblioteki Java, która obsługuje formaty DWG, DXF, DWF i wiele innych formatów CAD bez zależności natywnych. Po zakończeniu będziesz w stanie **zapisać CAD jako PDF**, dostosować opcje rasteryzacji, takie jak rozmiar strony, oraz poprawnie zastosować **licencję Aspose CAD** do użytku produkcyjnego.

## Szybkie odpowiedzi
- **Czy mogę konwertować DWG do PDF w Javie?** Tak – Aspose.CAD for Java natywnie obsługuje DWG, DXF i dziesiątki innych formatów CAD.  
- **Czy potrzebuję licencji?** Stała **licencja Aspose CAD** usuwa wszystkie ograniczenia wersji próbnej; tymczasowa licencja jest dostępna do testów.  
- **Jakie wersje Javy są obsługiwane?** Java 8 i wyższe są w pełni wspierane.  
- **Czy mogę kontrolować wymiary strony PDF?** Oczywiście – ustaw `pageWidth` i `pageHeight` w opcjach rasteryzacji.  
- **Czy renderowanie 3‑D jest możliwe?** Tak – włącz `TypeOfEntities.Entities3D`, aby rasteryzować obiekty 3‑D.

## Co to jest eksport AutoCAD PDF?

Eksportowanie AutoCAD PDF to proces przekształcania wektorowych rysunków CAD w przenośny dokument PDF. Zachowuje warstwy, grubości linii, kolory oraz opcjonalnie geometrię 3‑D, co ułatwia udostępnianie projektów klientom lub ich archiwizację bez konieczności posiadania oprogramowania CAD.

## Dlaczego konwertować DWG do PDF przy użyciu Aspose.CAD dla Javy?

Aspose.CAD obsługuje **ponad 50 formatów wejściowych i wyjściowych**, przetwarza rysunki o setkach stron bez ładowania całego pliku do pamięci i działa na każdej platformie wspierającej Java 8+. Biblioteka daje pełną kontrolę nad DPI, rozmiarem strony i układem, dzięki czemu możesz **dostosować rozmiar strony PDF** do dokładnych specyfikacji projektu, wszystko bez instalowania natywnych bibliotek DLL.

## Wymagania wstępne

- **Java Development Kit** – JDK 8 lub nowszy zainstalowany na Twoim komputerze.  
- **Aspose.CAD for Java** – pobierz najnowszy plik JAR z [download link](https://releases.aspose.com/cad/java/).  
- **Katalog roboczy** – folder, w którym będą przechowywane Twoje pliki DWG oraz wygenerowane pliki PDF.

## Importowanie przestrzeni nazw

Klasa `Image` reprezentuje dowolny rysunek CAD, który można rasteryzować, natomiast `RasterizationOptions` i `PdfOptions` pozwalają precyzyjnie dostosować konwersję.

Klasa `Image` jest obiektem najwyższego poziomu w Aspose.CAD, który przechowuje rysunek CAD w pamięci.  
Klasa `RasterizationOptions` definiuje sposób rasteryzacji danych wektorowych przed zapisaniem ich do PDF.  
Klasa `PdfOptions` łączy ustawienia rasteryzacji z parametrami wyjściowymi specyficznymi dla PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Teraz przejdźmy krok po kroku przez kod.

## Jak konwertować DWG do PDF przy użyciu Aspose.CAD dla Javy?

Aby skonwertować plik DWG do PDF przy użyciu Aspose.CAD dla Javy, wczytaj rysunek za pomocą klasy Image, skonfiguruj CadRasterizationOptions (takie jak DPI, rozmiar strony i typy obiektów), opakuj te opcje w PdfOptions, a następnie wywołaj metodę save, podając nazwę pliku .pdf. Ta sekwencja zapewnia prawidłową rasteryzację danych wektorowych i że wynikowy PDF spełnia wymagania układu.

### Krok 1: ustaw ścieżkę katalogu zasobów

Zastąp `"Your Document Directory"` absolutną ścieżką do folderu, który utworzyłeś w wymaganiach wstępnych.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Wskazówka:** Użyj `Paths.get(...).toAbsolutePath()`, aby uniknąć błędów związanych ze ścieżkami na różnych systemach operacyjnych.

### Krok 2: wczytaj obraz CAD

Wczytanie pliku CAD do obiektu `Image` daje pełny dostęp do silnika rasteryzacji Aspose.CAD.

Klasa `Image` wczytuje plik DWG i przygotowuje go do konwersji.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Dlaczego to ważne:** Gdy rysunek znajduje się w pamięci, możesz zapytać o jego układy, warstwy i metadane przed rasteryzacją.

### Krok 3: ustaw opcje rasteryzacji

Dostosuj `pageWidth` i `pageHeight`, aby **dostosować rozmiar strony PDF**. Włączenie `setTypeOfEntities(TypeOfEntities.Entities3D)` umożliwia pełne renderowanie 3‑D w razie potrzeby.

Obiekt `RasterizationOptions` kontroluje DPI, wymiary strony i typy obiektów wyjściowych.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` są mierzone w punktach (1 pt = 1/72 in).  
- Odkomentuj linię `setTypeOfEntities`, aby rasteryzować 3‑D.  
- `setLayouts` wybiera, który układ (Model, Layout1, itp.) ma zostać wyrenderowany.

### Krok 4: skonfiguruj opcje PDF

Połącz ustawienia rasteryzacji z wyjściem PDF, zapewniając prawidłową konwersję danych wektorowych.

Klasa `PdfOptions` łączy konfigurację rasteryzacji z końcowym plikiem PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: zapisz PDF

Wynikowy plik, `Export3DImagestoPDF_out_.pdf`, jest **zapisem CAD jako PDF** reprezentującym Twój oryginalny rysunek AutoCAD.

Metoda `save` zapisuje rasteryzowany obraz do pliku PDF na dysku.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Typowe problemy i rozwiązania

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| Pusty plik PDF | Opcje rasteryzacji nie ustawione lub niezgodność układu | Sprawdź, czy `setLayouts` odpowiada nazwie układu w Twoim pliku CAD. |
| Obraz o niskiej rozdzielczości | `pageWidth`/`pageHeight` za małe | Zwiększ wymiary lub ustaw wyższą wartość DPI za pomocą `rasterizationOptions.setResolution(...)`. |
| Wyjątek licencyjny | Nie zastosowano ważnej licencji | Zastosuj **licencję Aspose CAD** lub użyj tymczasowej licencji do testów. |

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.CAD dla Javy z innymi formatami plików CAD?**  
A: Tak – biblioteka obsługuje DWG, DXF, DWF, DGN oraz ponad 30 dodatkowych formatów, zapewniając elastyczność w różnych projektach.

**Q: Jak uzyskać tymczasową licencję dla Aspose.CAD dla Javy?**  
A: Odwiedź [temporary license page](https://purchase.aspose.com/temporary-license/), aby złożyć wniosek o licencję czasowo ograniczoną do oceny.

**Q: Czy istnieją opcje układu dla rasteryzacji?**  
A: Oczywiście. Użyj `setLayouts("Model")`, `setLayouts("Layout1")` itp., aby wybrać, który widok ma być renderowany do PDF.

**Q: Czy mogę zmienić rozmiar wyjściowego pliku PDF?**  
A: Tak – zmodyfikuj `pageWidth` i `pageHeight` w opcjach rasteryzacji, aby dopasować je do wymaganych wymiarów strony.

**Q: Gdzie mogę uzyskać pomoc, jeśli napotkam problemy?**  
A: Dedykowana społeczność jest dostępna na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), gdzie możesz zadawać pytania i dzielić się rozwiązaniami.

---

**Ostatnia aktualizacja:** 2026-10-19  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose

## Powiązane samouczki

- [Eksport DWG do PDF w Javie – ustaw rozmiar strony PDF przy użyciu Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Eksport DWG do PDF: określony układ przy użyciu Aspose.CAD dla Javy](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Eksport DWG do PDF i włącz śledzenie przy użyciu Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}