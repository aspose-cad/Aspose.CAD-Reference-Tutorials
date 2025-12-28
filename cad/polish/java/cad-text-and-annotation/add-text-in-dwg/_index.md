---
date: 2025-12-28
description: Dowiedz się, jak tworzyć PDF z plików DWG, zapisywać DWG jako PDF oraz
  dodawać tekst do rysunków DWG przy użyciu Aspose.CAD for Java — przewodnik krok
  po kroku.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Utwórz PDF z DWG i dodaj tekst przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie PDF z DWG i dodawanie tekstu przy użyciu Aspose.CAD for Java

## Wprowadzenie

Jeśli potrzebujesz **tworzyć PDF z plików DWG** i jednocześnie wstawiać własny tekst, jesteś we właściwym miejscu. W tym tutorialu przeprowadzimy Cię przez cały proces — wczytanie rysunku DWG, dodanie adnotacji tekstowej oraz ostateczne zapisanie wyniku jako PDF przy użyciu Aspose.CAD for Java. Po zakończeniu zrozumiesz, jak **zapisać DWG jako PDF**, dostosować wysokość tekstu i nawet dodać podstawowe adnotacje.

## Szybkie odpowiedzi
- **Czy mogę konwertować DWG na PDF w Javie?** Tak, Aspose.CAD for Java udostępnia prosty interfejs API.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest licencja komercyjna; dostępna jest darmowa wersja próbna.  
- **Która metoda dodaje tekst do DWG?** Użyj obiektu `CadText` i dodaj go do przestrzeni modelu.  
- **Czy mogę ustawić wysokość tekstu?** Oczywiście — użyj `setTextHeight()` na instancji `CadText`.  
- **Czy wynik jest wektorowy?** Gdy opcje rasteryzacji są ustawione na `UseObjectColor`, PDF zachowuje wysokiej jakości dane wektorowe.

## Wymagania wstępne

Zanim rozpoczniesz tutorial, upewnij się, że spełniasz następujące wymagania:

- Aspose.CAD for Java Library: Pobierz i zainstaluj bibliotekę z [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Upewnij się, że masz zainstalowaną najnowszą wersję JDK na swoim systemie.

- Rysunek DWG: Przygotuj plik rysunku DWG, do którego chcesz dodać tekst.

## Importowanie przestrzeni nazw

W kodzie Java zaimportuj niezbędne przestrzenie nazw dla Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Teraz rozbijmy podany fragment kodu na kilka kroków:

## Krok 1: Ustawienie katalogu dokumentu i ścieżki pliku DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Krok 2: Załadowanie obrazu DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Krok 3: Utworzenie obiektu CadText (dodanie tekstu do DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Krok 4: Dodanie tekstu do CadImage (wstawienie adnotacji)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Krok 5: Konfiguracja opcji PDF (przygotowanie do tworzenia PDF z DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 6: Konfiguracja CadRasterizationOptions (kontrola renderowania PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 7: Zapis zmodyfikowanego DWG jako PDF (dwg do pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Postępując zgodnie z tymi krokami, będziesz w stanie **tworzyć PDF z DWG**, dodawać własny tekst i kontrolować wysokość tekstu — wszystko przy użyciu kilku linii kodu Java.

## Dlaczego dodawać tekst do DWG i konwertować na PDF?

Dodawanie tekstu bezpośrednio do pliku DWG jest przydatne do:

- **Oznaczania projektów** notatkami lub numerami części.
- **Tworzenia dokumentacji do druku**, gdzie PDF jest formatem tylko do odczytu, szeroko wspieranym.
- **Automatyzacji przetwarzania wsadowego** dużych bibliotek CAD bez ręcznej edycji.

## Częste problemy i wskazówki

- **Tekst się nie wyświetla?** Sprawdź, czy współrzędne X/Y znajdują się w granicach rysunku i czy warstwa jest widoczna.
- **Nieprawidłowa wysokość tekstu?** Dostosuj `setTextHeight()`; wartość jest w jednostkach rysunku.
- **PDF wygląda jak raster?** Upewnij się, że `CadDrawTypeMode.UseObjectColor` jest ustawiony, aby zachować informacje wektorowe.
- **Wydajność przy dużych plikach?** Zwiększaj `pageHeight`/`pageWidth` tylko w razie potrzeby; większe wartości zużywają więcej pamięci.

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
A: Aspose.CAD obsługuje różne wersje plików DWG, zapewniając kompatybilność z szeroką gamą oprogramowania CAD.

**Q: Czy mogę dostosować czcionkę i formatowanie dodanego tekstu?**  
A: Tak, możesz dostosować czcionkę, styl i inne opcje formatowania tekstu dodawanego do plików DWG przy użyciu Aspose.CAD.

**Q: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
A: Tak, możesz poznać funkcje Aspose.CAD, uzyskując darmową wersję próbną [tutaj](https://releases.aspose.com/).

**Q: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD for Java?**  
A: Odwiedź dokumentację [tutaj](https://reference.aspose.com/cad/java/) po szczegółowe informacje i przykłady.

**Q: Jak mogę uzyskać wsparcie lub pomoc w sprawie Aspose.CAD?**  
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i połączyć się ze społecznością.

---

**Ostatnia aktualizacja:** 2025-12-28  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}