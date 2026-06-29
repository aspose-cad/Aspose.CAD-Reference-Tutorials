---
date: 2026-06-29
description: Dowiedz się, jak tworzyć PDF z DWG i dostosowywać układ PDF przy użyciu
  Aspose.CAD for Java. Łatwa integracja dla programistów Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: Pojedynczy PDF z różnymi układami
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Tworzenie PDF z DWG przy użyciu Aspose.CAD for Java
url: /pl/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie PDF z DWG przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

W tym samouczku **utworzysz PDF z plików DWG** i zastosujesz kilka układów o różnych rozmiarach stron przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz generować plany budowlane, schematy inżynieryjne, czy gotowe do marketingu PDF‑y, poniższe kroki pokażą, jak przekonwertować rysunki CAD do PDF, dostosować wymiary każdego układu i stworzyć jeden, wielostronicowy dokument — bez opuszczania środowiska Java.

## Szybkie odpowiedzi
- **Co obejmuje samouczek?** Konwersja rysunku DWG do jednego PDF z wieloma rozmiarami stron.  
- **Jakiej biblioteki wymaga?** Aspose.CAD dla Javy (najnowsza wersja).  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę eksportować inne formaty?** Tak — API obsługuje także eksport do PNG, JPEG i SVG.  
- **Czy Java 8 jest wystarczająca?** Biblioteka działa z Java 8 i nowszymi środowiskami uruchomieniowymi.

## Co to jest „tworzenie pdf z dwg”?

**Create PDF from DWG** oznacza konwersję natywnego pliku AutoCAD DWG do dokumentu PDF przy zachowaniu wierności wektorów, warstw i grubości linii oraz umożliwiając dostosowanie układu. Aspose.CAD wykonuje tę konwersję w całości w pamięci, więc nie jest potrzebne zewnętrzne oprogramowanie CAD, a powstały PDF może być edytowany lub drukowany bezpośrednio.

## Dlaczego dostosować układ PDF z DWG?

Aspose.CAD obsługuje **ponad 30 formatów CAD** i może generować PDF‑y do **500 MB** bez ładowania całego pliku do pamięci. Definiując indywidualne rozmiary stron dla każdego układu, możesz tworzyć arkusze do druku dopasowane do wymiarów ISO, ANSI lub własnych – wymierna korzyść, która oszczędza czas i eliminuje ręczną obróbkę po konwersji.

## Wymagania wstępne

Zanim rozpoczniemy, upewnij się, że masz następujące elementy:
- Środowisko Java: Upewnij się, że Java jest zainstalowana na twoim komputerze.  
- Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Javy z [download link](https://releases.aspose.com/cad/java/).  
- Katalog dokumentów: Utwórz katalog na swoje rysunki DWG.

## Importowanie pakietów

Klasa `CadImage` jest podstawowym obiektem Aspose.CAD, który reprezentuje rysunek CAD w pamięci. Zaimportuj wymagane przestrzenie nazw przed rozpoczęciem:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Krok 1: Załaduj rysunek CAD

`CadImage` ładuje plik DWG i zapewnia dostęp do jego danych wektorowych. Rozpocznij od załadowania swojego rysunku CAD do obiektu `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Krok 2: Skonfiguruj opcje rasteryzacji

`RasterizationOptions` określa, jak wektory CAD są rasteryzowane przed umieszczeniem w PDF. Skonfiguruj opcje rasteryzacji dla obrazu CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Krok 3: Dostosuj rozmiary stron układu

`PdfOptions` pozwala przypisać różne wymiary stron do każdego układu w pliku DWG. Zdefiniuj własne rozmiary dla kilku układów w rysunku CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Krok 4: Ustaw opcje PDF

`PdfOptions` jest kontenerem łączącym ustawienia rasteryzacji i definicje układów. Skonfiguruj opcje PDF, uwzględniając ustawienia rasteryzacji:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Zapisz jako PDF

`PdfSaveOptions` finalizuje konwersję i zapisuje plik wyjściowy. Zapisz przetworzony obraz CAD jako PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Gratulacje! Pomyślnie **utworzyłeś pdf z dwg** o różnych rozmiarach stron przy użyciu Aspose.CAD dla Javy.

## Typowe problemy i rozwiązania

- **Puste strony w wyjściowym PDF** – Upewnij się, że wartości `PageSize` odpowiadają rzeczywistym wymiarom układu w pliku DWG.  
- **Błędy pamięci przy dużych rysunkach** – Użyj `CadImage.load(..., LoadOptions)` z `LoadOptions.setLoadMode(LoadMode.Memory)`, aby strumieniować plik zamiast ładować go w całości.  
- **Nieprawidłowe skalowanie** – Dostosuj `RasterizationOptions.setPageWidth` i `setPageHeight`, aby odpowiadały żądanemu DPI (punktom na cal).

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD dla Javy z innymi bibliotekami Java?**  
O: Tak, Aspose.CAD dla Javy integruje się bezproblemowo z takimi bibliotekami jak Apache POI, Jackson czy Spring Boot.

**P: Czy dostępna jest wersja próbna?**  
O: Oczywiście! Bezpłatną wersję próbną możesz uzyskać [tutaj](https://releases.aspose.com/).

**P: Gdzie mogę znaleźć dodatkowe wsparcie?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia społeczności i dyskusji.

**P: Jak uzyskać tymczasową licencję?**  
O: Tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**P: Gdzie mogę kupić pełną wersję?**  
O: Pełną wersję Aspose.CAD dla Javy możesz kupić [tutaj](https://purchase.aspose.com/buy).

---

**Last Updated:** 2026-06-29  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Powiązane samouczki

- [Eksportuj DWG do PDF lub rastrowego przy użyciu Aspose.CAD dla Javy](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Eksportuj układy CAD do PDF przy użyciu Aspose.CAD dla Javy](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Eksportuj konkretny układ DWG do PDF przy użyciu Aspose.CAD dla Javy](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}