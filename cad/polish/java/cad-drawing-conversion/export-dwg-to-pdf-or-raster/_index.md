---
date: 2026-10-14
description: Dowiedz się, jak biblioteka Java CAD Aspose.CAD dla Javy może szybko
  i dokładnie eksportować DWG do PDF lub obrazów rastrowych.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Eksport DWG, PDF i obrazów rastrowych
og_description: Szybko eksportuj DWG do PDF przy użyciu Aspose.CAD dla Javy. Poznaj
  konwersję PDF wysokiej jakości, opcje rastrowe oraz licencjonowanie w tym przewodniku
  krok po kroku.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Eksportuj DWG do PDF i obrazów rastrowych przy użyciu biblioteki Java CAD
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Eksportuj DWG do PDF i obrazów rastrowych przy użyciu biblioteki Java CAD Aspose.CAD
url: /pl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj DWG PDF i obrazy rastrowe przy użyciu biblioteki Java CAD Aspose.CAD

## Wprowadzenie

Exportowanie DWG do PDF jest częstym wymaganiem dla inżynierów, architektów i każdego, kto musi udostępniać rysunki CAD bez ujawniania natywnego formatu pliku. Dzięki **Aspose.CAD for Java** możesz **export dwg pdf** — lub obrazy rastrowe — w zaledwie kilku linijkach kodu Java, zachowując wierność wektorów i precyzję układu. Ten samouczek przeprowadzi Cię przez ładowanie pliku DWG, konfigurowanie rasteryzacji i zapisywanie wyniku jako wysokiej jakości PDF lub obraz. Zobaczysz również, dlaczego Aspose.CAD jest preferowaną biblioteką Java CAD do niezawodnej, wieloplatformowej konwersji.

Zobacz [samouczek Eksport DWG do PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Eksportowanie plików DWG do PDF lub obrazów rastrowych przy użyciu Aspose.CAD for Java.  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa licencja tymczasowa do oceny; pełna licencja jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Każde środowisko uruchomieniowe Java 8+ działa z najnowszym API Aspose.CAD Java.  
- **Czy mogę konwertować DWG na inne formaty obrazów?** Tak – te same opcje rasteryzacji pozwalają na wyjście w formatach PNG, JPEG, BMP itp.  
- **Jak długo trwa konwersja?** Zwykle poniżej sekundy dla standardowych rysunków; większe pliki mogą zająć kilka sekund.

## Dlaczego biblioteka Java CAD jest najlepszym wyborem do konwersji DWG?

Aspose.CAD for Java jest najlepszym wyborem, ponieważ zapewnia czystą implementację w Javie, nie wymaga natywnych plików DLL, automatycznie wykrywa jednostki metryczne lub imperialne, dostarcza wyjście rastrowe do 1200 DPI oraz generuje PDF‑y zachowujące wektory bez zewnętrznych zależności. Biblioteka oferuje także elastyczny model licencjonowania, który pozwala rozpocząć od licencji tymczasowej i skalować do użytku korporacyjnego.

## Co to jest „export dwg to pdf”?

`Export dwg pdf` to proces konwertowania natywnego pliku rysunku DWG na dokument PDF przy zachowaniu danych wektorowych, warstw i skalowania. Ta konwersja tworzy plik niezależny od urządzenia, który może być wyświetlany na dowolnej platformie bez potrzeby AutoCAD. Ponieważ PDF zachowuje informacje wektorowe, tekst pozostaje przeszukiwalny, a grafika wyraźna przy dowolnym poziomie powiększenia, co czyni go idealnym do dokumentacji, przeglądu przez klienta i archiwizacji.

## Dlaczego używać Aspose.CAD Java do tej konwersji?

Powinieneś używać Aspose.CAD Java, ponieważ biblioteka obsługuje konwersję jednostek, rasteryzację i osadzanie PDF wewnętrznie, eliminując potrzebę narzędzi zewnętrznych lub skomplikowanych potoków wiersza poleceń. Jej API jest zaprojektowane dla programistów: pojedynczy obiekt `Image` reprezentuje rysunek, a kilka obiektów konfiguracyjnych pozwala precyzyjnie dostroić DPI, rozmiar strony i kompresję. Wynik to spójny, powtarzalny output na platformach Windows, Linux i macOS.

## Wymagania wstępne

- Podstawowa znajomość programowania w Javie.  
- Zainstalowana biblioteka Aspose.CAD for Java. Jeśli jeszcze jej nie pobrałeś, pobierz **[pobierz Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Plik DWG do testów – w tym przewodniku używany jest przykładowy **Bottom_plate.dwg**.

## Importowanie przestrzeni nazw

W swoim projekcie Java zaimportuj niezbędne klasy, aby rozpocząć konwersję:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj plik DWG

Najpierw załaduj swój rysunek DWG przy użyciu klasy `Image`. Tworzy to reprezentację w pamięci, z którą Aspose.CAD może pracować.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Krok 2: Określ typ jednostki

Zrozumienie, czy rysunek używa jednostek metrycznych czy imperialnych, jest niezbędne do prawidłowego skalowania. Metoda pomocnicza `IsMetric` (implementacja pominięta dla zwięzłości) zwraca wartość boolowską.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Krok 3: Ustaw opcje rasteryzacji

Klasa `CadRasterizationOptions` definiuje parametry rasteryzacji, takie jak DPI, rozmiar strony i konwersję jednostek. W zależności od systemu jednostek, skonfiguruj rozmiar strony, skalowanie i docelowy typ jednostki. Te opcje określają, jak DWG jest rasteryzowany przed umieszczeniem w PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Krok 4: Skonfiguruj opcje PDF (pdf options cad)

Klasa `PdfOptions` określa ustawienia specyficzne dla PDF, w tym kompresję i metadane. Utwórz instancję `PdfOptions` i dołącz ustawienia rasteryzacji. To informuje Aspose.CAD, jak osadzić rasteryzowaną zawartość w ostatecznym PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Krok 5: Zapisz jako PDF

Metoda `save` zapisuje obraz do podanej ścieżki pliku, używając dostarczonych opcji. Na koniec wyeksportuj rysunek do pliku PDF. Metoda `save` przyjmuje ścieżkę wyjściową oraz skonfigurowane `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Po zakończeniu działania kodu znajdziesz **Saved.pdf** w folderze `DWGDrawings`, gotowy do dystrybucji lub archiwizacji.

## Jak konwertować obrazy rastrowe DWG przy użyciu biblioteki Java CAD?

Możesz konwertować DWG na formaty rastrowe, zamieniając `PdfOptions` na klasę opcji specyficzną dla rastera, taką jak `PngOptions` lub `JpegOptions`. Ponownie użyj tej samej instancji `CadRasterizationOptions`, dostosuj format wyjściowy i wywołaj metodę `save` z nowym obiektem opcji. To podejście pozwala generować pliki PNG, JPEG, BMP lub TIFF przy zmianie jednego wiersza kodu, zachowując spójny przepływ pracy.

## Jak generować PDF DWG przy użyciu opcji PDF CAD?

Powyższy przykład już **generuje pdf dwg**. Aby precyzyjnie dostroić rozmiar PDF, włącz kompresję, wywołując `pdfOptions.setCompress(true)`. Możesz także osadzić własne metadane, ustawić wersję PDF lub dodać ochronę hasłem poprzez dodatkowe właściwości `PdfOptions`. Te modyfikacje dają pełną kontrolę nad ostatecznym PDF bez opuszczania kodu Java.

## Typowe problemy i wskazówki

- **Nieprawidłowy rozmiar strony** – Sprawdź ponownie logikę konwersji jednostek; niepasujące współczynniki mogą powodować zbyt duże strony.  
- **Brak czcionek lub grubości linii** – Upewnij się, że DWG odwołuje się do wszystkich zewnętrznych zasobów przed konwersją.  
- **Wydajność przy dużych rysunkach** – Zwiększ ustawienie `DPI` w `CadRasterizationOptions` tylko wtedy, gdy wymagana jest wyższa jakość; niższe DPI przyspiesza przetwarzanie.  
- **Kwestie licencyjne** – Do oceny możesz użyć **tymczasowej licencji Aspose**; pełna licencja jest wymagana w środowiskach produkcyjnych.

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD for Java z innymi frameworkami Java?**  
O: Tak, Aspose.CAD for Java bezproblemowo integruje się z popularnymi frameworkami Java, takimi jak Spring, Jakarta EE i Android.

**P: Czy dostępna jest tymczasowa licencja dla Aspose.CAD for Java?**  
O: Tak, możesz uzyskać tymczasową licencję **[uzyskaj tymczasową licencję](https://purchase.aspose.com/temporary-license/)**.

**P: Gdzie mogę znaleźć wsparcie dla Aspose.CAD for Java?**  
O: Odwiedź **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**, aby uzyskać pomoc od społeczności i inżynierów Aspose.

**P: Jak mogę kupić licencję na Aspose.CAD for Java?**  
O: Możesz zakupić licencję **[zakup licencję](https://purchase.aspose.com/buy)**.

**P: Jakie jednostki obsługuje Aspose.CAD for Java?**  
O: Aspose.CAD for Java obsługuje zarówno jednostki metryczne, jak i imperialne, automatycznie wykrywając system jednostek rysunku.

**P: Czy mogę konwertować DWG na inne formaty obrazów (np. PNG, JPEG) używając tego samego API?**  
O: Oczywiście. Zastąp `PdfOptions` odpowiednimi opcjami obrazu rastrowego (np. `PngOptions`) i ponownie użyj tej samej `CadRasterizationOptions`.

## Podsumowanie

Ten samouczek pokazał, jak **export dwg pdf** i obrazy rastrowe przy użyciu **java cad library** Aspose.CAD for Java. Postępując zgodnie z przewodnikiem krok po kroku, możesz zintegrować niezawodną konwersję CAD w dowolnej aplikacji Java, niezależnie od tego, czy potrzebujesz PDF‑ów do dokumentacji, czy obrazów rastrowych do wyświetlania w sieci. Czysta natura biblioteki Java, wysokiej jakości output i elastyczne licencjonowanie czynią ją solidnym wyborem zarówno dla małych narzędzi, jak i dużych przepływów przedsiębiorstw.

---

**Last Updated:** 2026-10-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Powiązane samouczki

- [Eksport DWG do PDF: Specyficzny układ przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Eksport DWG do PDF w Javie – Ustaw rozmiar strony PDF przy użyciu Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Eksport DWG do PDF z ukrytymi liniami – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}