---
date: 2026-05-20
description: Dowiedz się, jak konwertować DWG na PDF, zastępując automatyczne wykrywanie
  strony kodowej przy użyciu Aspose.CAD for Java. Zawiera kroki eksportu DWG do PDF,
  wskazówki dotyczące kodowania oraz rozwiązywanie problemów.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Zastąp automatyczne wykrywanie strony kodowej w plikach DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konwertuj DWG na PDF – Zastąp wykrywanie strony kodowej w Javie
url: /pl/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG na PDF – Nadpisz wykrywanie strony kodowej w Javie

W tym obszernej samouczku dowiesz się **jak konwertować DWG na PDF**, jednocześnie nadpisując automatyczne wykrywanie strony kodowej, które może psuć tekst. Aspose.CAD dla Javy zapewnia precyzyjną kontrolę nad kodowaniem znaków, umożliwiając odzyskanie uszkodzonych danych CIF/MIF i generowanie niezawodnego wyjścia PDF. Niezależnie od tego, czy tworzysz konwerter wsadowy, czy dodajesz przetwarzanie CAD do większej usługi Java, poniższe kroki przeprowadzą Cię przez cały przepływ pracy — od konfiguracji projektu po weryfikację.

## Szybkie odpowiedzi
- **Co oznacza „override code page”?** Wymusza to, aby Aspose.CAD używał określonego kodowania znaków zamiast zgadywać.
- **Czy mogę wyeksportować DWG bezpośrednio do PDF?** Tak – po ustawieniu właściwej strony kodowej możesz zapisać obraz CAD jako PDF.
- **Jakie kodowanie działa dla tekstu japońskiego?** `CodePages.Japanese` i `MifCodePages.Japanese` są właściwymi wyborami.
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest licencja komercyjna; licencja tymczasowa jest dostępna do testów.
- **Jakiej wersji Aspose.CAD potrzebuję?** Dowolna aktualna wersja obsługująca `LoadOptions` i `PdfOptions`.

## Co to jest „export CAD to PDF”?
Eksportowanie CAD do PDF przekształca wektorowy rysunek DWG w uniwersalny, stały dokument PDF, który można przeglądać wszędzie. Konwersja zachowuje wszystkie elementy geometryczne, linie, warstwy i osadzony tekst, jednocześnie spłaszczając rysunek do formatu, który można łatwo udostępniać, drukować, archiwizować lub osadzać w innych aplikacjach bez konieczności posiadania oprogramowania CAD.

## Dlaczego nadpisać automatyczne wykrywanie strony kodowej?
Ręczne określenie strony kodowej zapewnia prawidłową interpretację bajtów tekstu, eliminując zniekształcone znaki, które często pojawiają się, gdy automatyczne wykrywanie Aspose.CAD zgaduje niewłaściwe starsze kodowanie. Jest to niezbędne dla skryptów nielatynowych, takich jak japoński, cyrylica czy arabski, i zapewnia, że wyeksportowany PDF odpowiada oryginalnemu projektowi.

## Wymagania wstępne
- **Środowisko programistyczne Java** – JDK 8+ oraz ulubione IDE.  
- **Aspose.CAD for Java** – Pobierz bibliotekę z oficjalnej strony [tutaj](https://releases.aspose.com/cad/java/).  
- **Plik przykładowy DWG** – Użyj dostarczonego `SimpleEntities.dwg` lub dowolnego DWG, który chcesz przekonwertować.

## Importowanie pakietów
Klasy `Document`, `LoadOptions` i `PdfOptions` są rdzeniem procesu konwersji.

Klasa `Document` reprezentuje rysunek CAD w pamięci, udostępniając metody do ładowania, manipulacji i zapisywania pliku w różnych formatach.  
Klasa `LoadOptions` pozwala określić stronę kodową i opcje odzyskiwania przy ładowaniu pliku DWG.  
Klasa `PdfOptions` kontroluje ustawienia specyficzne dla PDF, takie jak kompresja, rasteryzacja i metadane.

W swoim projekcie Java zaimportuj niezbędne klasy Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Jak przekonwertować DWG na PDF z nadpisaniem strony kodowej?
Załaduj plik DWG przy użyciu `LoadOptions`, aby określić dokładną stronę kodową, a następnie wywołaj metodę `save` na uzyskanym obiekcie `CadImage` z skonfigurowaną instancją `PdfOptions`. To dwustopniowe podejście zapewnia prawidłową interpretację tekstu oraz zachowanie w wygenerowanym PDF dokładności oryginalnego rysunku, warstw i jakości wektorowej.

### Krok 1: Skonfiguruj projekt Java
Utwórz projekt Maven lub Gradle i dodaj plik JAR Aspose.CAD do classpath. Dzięki temu IDE będzie mogło rozwiązać importowane klasy, a środowisko uruchomieniowe znajdzie bibliotekę.

### Krok 2: Załaduj plik DWG z określoną stroną kodową
Powiedz Aspose.CAD, jakiego kodowania użyć i czy próbować odzyskać uszkodzone dane CIF/MIF.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Krok 3: Eksportuj obraz CAD do PDF
Po zastosowaniu właściwej strony kodowej możesz bezpiecznie wyeksportować rysunek. Obiekt `PdfOptions` pozwala precyzyjnie dostosować wyjście PDF (kompresję, rasteryzację itp.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Krok 4: Zweryfikuj powodzenie
Prosta wiadomość w konsoli potwierdza, że proces zakończył się bez wyjątków.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Możesz powtórzyć te kroki dla wielu plików DWG, dostosowując ścieżkę źródłową i nazwę wyjściową w razie potrzeby.

## Typowe problemy i rozwiązania
- **Wciąż pojawiają się nieczytelne znaki:** Sprawdź, czy `specifiedEncoding` odpowiada stronie kodowej oryginalnego pliku DWG. W razie potrzeby użyj innego wyliczenia `CodePages`.  
- **`NullPointerException` przy `cadImage.save`:** Upewnij się, że plik DWG został poprawnie załadowany; sprawdź ścieżkę i uprawnienia do pliku.  
- **Rozmiar PDF jest duży:** Włącz kompresję w `PdfOptions` (np. `pdfOptions.setCompress(true)`), aby zmniejszyć rozmiar pliku bez utraty jakości.

## Najczęściej zadawane pytania

**Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
A1: Aspose.CAD obsługuje ponad 30 wersji DWG, w tym AutoCAD 2018 i wcześniejsze wydania.

**Q2: Czy mogę używać Aspose.CAD w projektach komercyjnych?**  
A2: Tak, wymagana jest licencja komercyjna do użytku produkcyjnego. Licencję możesz uzyskać [tutaj](https://purchase.aspose.com/buy).

**Q3: Are there any limitations in the free trial version?**  
A1: Wersja próbna nakłada ograniczenia dotyczące rozmiaru i funkcji; zapoznaj się z oficjalną dokumentacją po szczegóły.

**Q4: Jak mogę uzyskać wsparcie dla Aspose.CAD?**  
A4: Odwiedź społeczność [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy i dyskusji.

**Q5: Czy dostępna jest tymczasowa licencja do celów testowych?**  
A5: Tak, tymczasową licencję można zamówić [tutaj](https://purchase.aspose.com/temporary-license/).

---

**Ostatnia aktualizacja:** 2026-05-20  
**Testowano z:** Aspose.CAD for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose

## Powiązane samouczki

- [Eksportuj DWG do PDF i konwertuj rysunki CAD – Samouczek Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Eksportuj konkretny układ DWG do PDF przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Eksportuj DWG do PDF lub rastra przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}