---
date: 2026-02-28
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

# Tworzenie PDF z DWG i dodawanie tekstu przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **utworzyć PDF z plików DWG**, jednocześnie wstawiając własny tekst, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię przez cały proces — wczytanie rysunku DWG, dodanie adnotacji tekstowej oraz zapisanie wyniku jako PDF przy użyciu Aspose.CAD dla Javy. Po zakończeniu zrozumiesz, jak **zapisać DWG jako PDF**, dostosować wysokość tekstu i dodać podstawowe adnotacje.

## Szybkie odpowiedzi
- **Czy mogę konwertować DWG na PDF w Javie?** Tak, Aspose.CAD dla Javy udostępnia prostą API.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest licencja komercyjna; dostępna jest wersja próbna.  
- **Która metoda dodaje tekst do DWG?** Użyj obiektu `CadText` i dodaj go do przestrzeni modelu.  
- **Czy mogę ustawić wysokość tekstu?** Oczywiście — użyj `setTextHeight()` na instancji `CadText`.  
- **Czy wynik jest wektorowy?** Gdy opcje rasteryzacji są ustawione na `UseObjectColor`, PDF zachowuje wysokiej jakości dane wektorowe.

## Co oznacza „tworzenie PDF z DWG”?
Utworzenie PDF z rysunku DWG oznacza konwersję natywnego formatu CAD do powszechnie obsługiwanego, tylko do odczytu dokumentu, przy zachowaniu oryginalnej geometrii. Konwersja ta jest niezbędna, gdy musisz udostępnić projekty interesariuszom, którzy nie posiadają oprogramowania CAD.

## Dlaczego warto używać Aspose.CAD dla Javy do konwersji DWG na PDF?
Aspose.CAD oferuje rozwiązanie czysto‑Java, które nie wymaga instalacji zewnętrznego oprogramowania CAD. Obsługuje **konwersję DWG na PDF**, zachowuje wierność wektorów i pozwala programowo dodawać adnotacje, takie jak tekst, wymiarowanie czy własne grafiki przed konwersją.

## Wymagania wstępne

Przed rozpoczęciem samouczka upewnij się, że spełniasz następujące wymagania:

- Biblioteka Aspose.CAD dla Javy: Pobierz i zainstaluj bibliotekę ze [strony Aspose.CAD dla Javy](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Upewnij się, że masz zainstalowaną najnowszą wersję JDK.

- Rysunek DWG: Przygotuj plik DWG, do którego chcesz dodać tekst.

## Importowanie przestrzeni nazw

W swoim kodzie Java zaimportuj niezbędne przestrzenie nazw dla Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Teraz rozbijmy podany fragment kodu na kilka kroków:

## Krok 1: Ustaw katalog dokumentu i ścieżkę pliku DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Krok 2: Wczytaj obraz DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Krok 3: Utwórz obiekt CadText (dodaj tekst do DWG)

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

## Krok 4: Dodaj tekst do CadImage (wstaw adnotację)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Krok 5: Skonfiguruj opcje PDF (przygotowanie do tworzenia PDF z DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 6: Skonfiguruj CadRasterizationOptions (kontrola renderowania PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 7: Zapisz zmodyfikowany DWG jako PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Postępując zgodnie z tymi krokami, będziesz w stanie **utworzyć PDF z DWG**, dodać własny tekst i kontrolować wysokość tekstu — wszystko przy użyciu kilku linii kodu Java.

## Jak konwertować DWG na PDF w Javie na dużą skalę?
Jeśli potrzebujesz **konwertować wsadowo pliki DWG na PDF**, otocz powyższy kod pętlą iterującą po folderze z rysunkami DWG. Dostosuj `pageHeight`/`pageWidth` tylko w razie konieczności, aby utrzymać niskie zużycie pamięci, i ponownie używaj tej samej instancji `PdfOptions` dla każdego pliku, aby zwiększyć wydajność.

## Typowe problemy i wskazówki

- **Tekst się nie wyświetla?** Sprawdź, czy współrzędne X/Y mieszczą się w granicach rysunku i czy warstwa jest widoczna.
- **Nieprawidłowa wysokość tekstu?** Dostosuj `setTextHeight()`; wartość jest podawana w jednostkach rysunku.
- **PDF wygląda jak raster?** Upewnij się, że `CadDrawTypeMode.UseObjectColor` jest ustawiony, aby zachować informacje wektorowe.
- **Wydajność przy dużych plikach?** Zwiększaj `pageHeight`/`pageWidth` tylko w razie potrzeby; większe wartości zużywają więcej pamięci.

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
O: Aspose.CAD obsługuje różne wersje plików DWG, zapewniając kompatybilność z szerokim zakresem oprogramowania CAD.

**P: Czy mogę dostosować czcionkę i formatowanie dodawanego tekstu?**  
O: Tak, możesz dostosować czcionkę, styl i inne opcje formatowania tekstu dodawanego do plików DWG przy użyciu Aspose.CAD.

**P: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Javy?**  
O: Tak, możesz wypróbować funkcje Aspose.CAD, pobierając darmową wersję próbną [tutaj](https://releases.aspose.com/).

**P: Gdzie znajdę szczegółową dokumentację Aspose.CAD dla Javy?**  
O: Zapoznaj się z dokumentacją [tutaj](https://reference.aspose.com/cad/java/), aby uzyskać szczegółowe informacje i przykłady.

**P: Jak mogę uzyskać wsparcie lub pomoc w sprawie Aspose.CAD?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i połączyć się ze społecznością.

---

**Ostatnia aktualizacja:** 2026-02-28  
**Testowano z:** Aspose.CAD dla Javy 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}