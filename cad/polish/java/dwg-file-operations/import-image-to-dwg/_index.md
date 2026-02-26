---
date: 2026-01-12
description: Dowiedz się, jak dodać obraz do plików DWG przy użyciu Aspose.CAD dla
  Javy oraz jak konwertować DWG na PDF. Postępuj zgodnie z naszym przewodnikiem krok
  po kroku, aby efektywnie rozwijać aplikacje.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Dodaj obraz do plików DWG z łatwością przy użyciu Aspose.CAD Java
url: /pl/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj obraz do plików DWG bez wysiłku przy użyciu Aspose.CAD Java

W nowoczesnych aplikacjach Java **dodawanie obrazu do DWG** jest powszechnym wymaganiem — niezależnie od tego, czy tworzysz przeglądarkę CAD, automatyzujesz aktualizacje rysunków, czy generujesz dokumentację. Aspose.CAD for Java zapewnia prosty, wysokowydajny sposób osadzania obrazów rastrowych bezpośrednio w rysunkach DWG, bez potrzeby pełnoprawnego silnika CAD. W tym samouczku przeprowadzimy Cię przez cały proces, od wczytania pliku DWG po wyeksportowanie wyniku jako PDF.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.CAD for Java  
- **Czy mogę także eksportować do PDF?** Tak – użyj `PdfOptions` wraz z `CadRasterizationOptions`  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji  
- **Jaką wersję Java obsługuje?** Java 8 i wyższe  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego importu obrazu  

## Co to jest „add image to dwg”?
Dodanie obrazu do pliku DWG oznacza wstawienie obrazu rastrowego (PNG, JPEG itp.) jako obiektu `CadRasterImage` w przestrzeni modelu rysunku. Obraz staje się częścią drzewa encji CAD i może być pozycjonowany, skalowany oraz przycinany tak jak każdy inny obiekt CAD.

## Dlaczego używać Aspose.CAD for Java do dodawania obrazu do dwg?
- **Bez wymogu posiadania oprogramowania CAD** – API samodzielnie parsuje pliki DWG.  
- **Precyzyjna kontrola** nad punktem wstawienia, wektorami skalowania i przycinaniem.  
- **Wbudowana konwersja do PDF** umożliwiająca generowanie drukowalnego PDF w tym samym przepływie pracy.  
- **Wieloplatformowość** – działa na Windows, Linux i macOS.  

## Wymagania wstępne
- Aspose.CAD for Java: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Możesz ją pobrać [tutaj](https://releases.aspose.com/cad/java/).  
- Środowisko programistyczne Java: JDK 8+ oraz ulubione IDE (IntelliJ, Eclipse, VS Code itp.).

## Importowanie pakietów
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj plik DWG
Najpierw wskaż folder zawierający rysunek DWG i wczytaj go przy pomocy `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Krok 2: Zdefiniuj definicję obrazu rastrowego
Utwórz `CadRasterImageDef`, który odwołuje się do zewnętrznego pliku PNG, który chcesz osadzić. Konstruktor przyjmuje nazwę pliku obrazu oraz jego wymiary w pikselach.
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
Połącz definicję, punkt wstawienia i wektory w obiekt `CadRasterImage`. Możesz także ustawić granice przycinania, jeśli chcesz, aby widoczna była tylko część obrazu.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Krok 5: Dodaj obraz do Model Space
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
Jeśli potrzebujesz także wersji PDF rysunku, skonfiguruj `PdfOptions` razem z `CadRasterizationOptions`. Ten krok pokazuje, jak **convert dwg to pdf** w tym samym przepływie.
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
Na koniec wyeksportuj zmodyfikowany rysunek jako plik PDF. To samo wystąpienie `image` jest używane, więc PDF odzwierciedla nowo dodany obraz rastrowy.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Postępując zgodnie z tymi krokami, możesz szybko **add image to dwg** oraz w razie potrzeby **save dwg as pdf**.

## Typowe problemy i rozwiązania
- **Obraz się nie wyświetla** – Sprawdź, czy ścieżka do pliku obrazu (`road-sign-custom.png`) jest prawidłowa i czy wymiary obrazu odpowiadają wartościom przekazanym do `CadRasterImageDef`.  
- **Nieprawidłowe skalowanie** – Dostosuj wektory U i V; reprezentują one jednostki rysunku na piksel.  
- **PDF jest pusty** – Upewnij się, że `CadRasterizationOptions.setDrawType` jest ustawione na `UseObjectColor` lub inny odpowiedni tryb.  

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD for Java jest kompatybilny ze wszystkimi środowiskami programistycznymi Java?**  
A: Tak, Aspose.CAD for Java jest kompatybilny z większością środowisk programistycznych Java.

**Q: Czy mogę używać Aspose.CAD for Java w projektach komercyjnych?**  
A: Tak, możesz używać Aspose.CAD for Java w projektach komercyjnych. Odwiedź [tutaj](https://purchase.aspose.com/buy) po szczegóły licencjonowania.

**Q: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
A: Tak, darmową wersję próbną możesz uzyskać [tutaj](https://releases.aspose.com/).

**Q: Jak mogę uzyskać wsparcie dla Aspose.CAD for Java?**  
A: Wsparcie możesz uzyskać na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

**Q: Czy mogę otrzymać tymczasową licencję dla Aspose.CAD for Java?**  
A: Tak, tymczasową licencję możesz pobrać [tutaj](https://purchase.aspose.com/temporary-license/).

**Ostatnia aktualizacja:** 2026-01-12  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}