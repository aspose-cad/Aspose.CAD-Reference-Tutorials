---
date: 2026-05-20
description: Dowiedz się, jak dodać obraz do plików DWG przy użyciu Aspose.CAD dla
  Java oraz jak konwertować DWG na PDF. Postępuj zgodnie z naszym przewodnikiem krok
  po kroku, aby uzyskać efektywny rozwój.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Importuj obraz do pliku DWG przy użyciu Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Dodaj obraz do plików DWG bez wysiłku przy użyciu Aspose.CAD Java
url: /pl/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj obraz do plików DWG bez wysiłku przy użyciu Aspose.CAD Java

W nowoczesnych aplikacjach Java, **dodawanie obrazu do DWG** jest powszechnym wymaganiem — niezależnie od tego, czy tworzysz przeglądarkę CAD, automatyzujesz aktualizacje rysunków, czy generujesz dokumentację. Aspose.CAD for Java zapewnia prosty, wysokowydajny sposób na osadzenie obrazów rastrowych bezpośrednio w rysunkach DWG bez konieczności posiadania pełnoprawnego silnika CAD. W tym samouczku przeprowadzimy Cię przez cały proces, od wczytania pliku DWG po wyeksportowanie wyniku jako PDF, a także omówimy, jak **importować obraz do dwg** i **konwertować dwg na pdf** w jednym przepływie pracy.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.CAD for Java  
- **Czy mogę również eksportować do PDF?** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **Czy potrzebuję licencji do rozwoju?** A free trial works for testing; a commercial license is required for production  
- **Która wersja Java jest obsługiwana?** Java 8 and higher  
- **Jak długo trwa implementacja?** About 10‑15 minutes for a basic image import  

## Co to jest „dodawanie obrazu do dwg”?
Dodanie obrazu do pliku DWG oznacza osadzenie obrazu rastrowego (PNG, JPEG itp.) jako jednostki **CadRasterImage** w przestrzeni modelu rysunku, gdzie może być pozycjonowany, skalowany i opcjonalnie przycinany tak jak każdy inny obiekt CAD. Jest przechowywany w tabeli obiektów rysunku i wyświetlany przez standardowe przeglądarki CAD.

## Dlaczego używać Aspose.CAD for Java do dodawania obrazu do dwg?
Możesz osadzać grafiki rastrowe w plikach DWG bez instalowania jakiegokolwiek zewnętrznego oprogramowania CAD, a API zapewnia precyzyjną kontrolę nad punktem wstawienia, wektorami skalowania i granicami przycinania. Aspose.CAD przetwarza pliki o rozmiarze do 2 GB, obsługuje **ponad 50 formatów wejściowych i wyjściowych** oraz działa na Windows, Linux i macOS, umożliwiając integrację manipulacji CAD w dowolnym backendzie opartym na Javie.

## Wymagania wstępne
- **Aspose.CAD for Java** – pobierz najnowszy JAR z oficjalnej strony **[tutaj](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 lub nowszy, z wybranym IDE (IntelliJ IDEA, Eclipse, VS Code itp.).  
- Ważna **licencja Aspose.CAD** do użytku produkcyjnego (wersja próbna działa do eksperymentów).  

## Importowanie pakietów
Poniższe importy wprowadzają niezbędne klasy Aspose.CAD używane do manipulacji obrazem i konwersji do PDF.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Przewodnik krok po kroku

### Krok 1: Wczytaj plik DWG
Najpierw wskaż folder zawierający Twój rysunek DWG i wczytaj go za pomocą `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Krok 2: Zdefiniuj definicję obrazu rastrowego
Klasa `CadRasterImageDef` definiuje zewnętrzny zasób obrazu rastrowego, który ma być osadzony w rysunku.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Krok 3: Ustaw punkt wstawienia i wektory skalowania
Punkt wstawienia określa, gdzie pojawi się lewy dolny róg obrazu. Wektory **U** i **V** kontrolują skalowanie w poziomie i w pionie.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Krok 4: Utwórz obiekt CadRasterImage
Jednostka `CadRasterImage` reprezentuje obraz rastrowy umieszczony w przestrzeni modelu DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Krok 5: Dodaj obraz do przestrzeni modelu
Wstaw obraz rastrowy do bloku `*Model_Space`, a następnie zaktualizuj kolekcję obiektów rysunku, aby definicja została zapisana.  
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Krok 6: Skonfiguruj opcje eksportu PDF (opcjonalnie)
`PdfOptions` określa ustawienia zapisu rysunku CAD jako pliku PDF. `CadRasterizationOptions` definiuje sposób rastrowania zawartości CAD podczas konwersji do PDF.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Krok 7: Zapisz wynikowy PDF
Na koniec wyeksportuj zmodyfikowany rysunek jako plik PDF. Używana jest ta sama instancja `image`, więc PDF odzwierciedla nowo dodany obraz rastrowy.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Postępując zgodnie z tymi krokami, możesz szybko **dodać obraz do dwg** oraz **zapisać dwg jako pdf**, gdy zajdzie taka potrzeba, obejmując najczęstsze **operacje na plikach dwg** w jednej, zwięzłej procedurze.

## Typowe problemy i rozwiązania
- **Obraz się nie wyświetla** – Sprawdź, czy ścieżka do pliku obrazu (`road-sign-custom.png`) jest poprawna i czy wymiary obrazu odpowiadają wartościom przekazanym do `CadRasterImageDef`.  
- **Nieprawidłowe skalowanie** – Dostosuj wektory U i V; reprezentują one jednostki rysunku na piksel.  
- **PDF jest pusty** – Upewnij się, że `CadRasterizationOptions.setDrawType` jest ustawione na `UseObjectColor` lub inny odpowiedni tryb.  

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD for Java jest kompatybilny ze wszystkimi środowiskami programistycznymi Java?**  
O: Tak, Aspose.CAD for Java działa z dowolnym IDE obsługującym JDK 8+, w tym IntelliJ IDEA, Eclipse i VS Code.

**P: Czy mogę używać Aspose.CAD for Java w projektach komercyjnych?**  
O: Tak, możesz używać Aspose.CAD for Java w projektach komercyjnych. Odwiedź **[tutaj](https://purchase.aspose.com/buy)**, aby uzyskać szczegóły licencjonowania.

**P: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
O: Tak, możesz uzyskać dostęp do darmowej wersji próbnej **[tutaj](https://releases.aspose.com/)**.

**P: Jak mogę uzyskać wsparcie dla Aspose.CAD for Java?**  
O: Możesz uzyskać wsparcie na **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**P: Czy mogę uzyskać tymczasową licencję na Aspose.CAD for Java?**  
O: Tak, możesz uzyskać tymczasową licencję **[tutaj](https://purchase.aspose.com/temporary-license/)**.

---

**Ostatnia aktualizacja:** 2026-05-20  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksportuj DWG do PDF lub rastra przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Dodaj własne właściwości do plików DWG przy użyciu Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Zapisz CAD jako PNG – konwertuj rysunek CAD do formatu obrazu rastrowego przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}