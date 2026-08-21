---
date: 2026-05-04
description: Dowiedz się, jak konwertować pliki CAD PDF, eksportując DGN do PDF AutoCAD
  przy użyciu Aspose.CAD dla Javy. Przewodnik krok po kroku z możliwością dostosowania
  rozmiaru i opcji PDF.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Eksportowanie DGN w formacie AutoCAD do PDF
second_title: Aspose.CAD Java API
title: Konwertuj PDF CAD – Łatwy eksport DGN do PDF AutoCAD przy użyciu Aspose.CAD
  dla Javy
url: /pl/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj CAD PDF: Bezproblemowy eksport DGN do PDF AutoCAD przy użyciu Aspose.CAD dla Java

## Wprowadzenie

Jeśli potrzebujesz **konwertować CAD PDF** bezpośrednio ze źródeł DGN, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię krok po kroku przez użycie Aspose.CAD dla Java do eksportu plików DGN do PDF kompatybilnego z AutoCAD. Zobaczysz, jak ustawić własne wymiary strony, wybrać konkretne układy i dopracować wyjście PDF — wszystko przy użyciu przejrzystego kodu, który możesz wstawić do własnego projektu.

## Szybkie odpowiedzi
- **Co oznacza „konwertować CAD PDF”?** Odnosi się do przekształcania plików źródłowych CAD (takich jak DGN) w PDF zachowujący dane wektorowe i wierność układu.  
- **Która biblioteka obsługuje konwersję?** Aspose.CAD dla Java zapewnia niezawodny, bezpłatny trial do tego zadania.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowy trial działa w testach; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Czy mogę dostosować rozmiar PDF?** Tak – `CadRasterizationOptions` umożliwiają ustawienie szerokości, wysokości i skalowania strony.  
- **Ile linii kodu jest potrzebnych?** Mniej niż 20 linii kodu Java, aby załadować, skonfigurować i zapisać PDF.

## Czym jest „konwertować CAD PDF”?
Konwersja CAD PDF polega na wzięciu natywnego rysunku CAD (np. DGN) i wygenerowaniu PDF, który zachowuje oryginalną grafikę wektorową, warstwy i informacje o układzie. Powstały PDF można otworzyć na dowolnym urządzeniu bez potrzeby oprogramowania CAD, co czyni go idealnym do udostępniania, drukowania lub archiwizacji.

## Dlaczego używać Aspose.CAD dla Java do konwersji CAD PDF?
- **Pełne wsparcie formatów** – DGN, DWG, DXF i wiele innych.  
- **Brak zewnętrznych zależności** – czysta Java, bez natywnych DLL‑ów.  
- **Precyzyjna kontrola** – możesz wybrać, które układy eksportować, ustawić własne rozmiary stron i kontrolować jakość rasteryzacji.  
- **Skalowalność dla zadań wsadowych** – ładowanie i zapisywanie dziesiątek plików w pętli przy minimalnym narzucie.

## Wymagania wstępne
Zanim zaczniemy, upewnij się, że masz następujące elementy:

- **Aspose.CAD Library** – pobierz ją [tutaj](https://releases.aspose.com/cad/java/).  
- **Katalog dokumentów** – folder na Twoim komputerze, w którym będą znajdować się pliki wejściowe DGN oraz wyjściowe PDF.

## Importuj pakiety

W projekcie Java zaimportuj niezbędne pakiety, aby uzyskać dostęp do funkcjonalności Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Teraz rozbijmy przykładowy kod na kilka kroków:

## Krok 1: Zdefiniuj ścieżki plików (jak wyeksportować dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Upewnij się, że zamieniłeś `"Your Document Directory"` na rzeczywistą ścieżkę, w której znajdują się Twoje pliki.

## Krok 2: Załaduj obraz DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Załaduj plik DGN przy użyciu Aspose.CAD.

## Krok 3: Ustaw opcje eksportu PDF (dostosuj rozmiar pdf, ustaw opcje pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Tutaj definiujemy opcje eksportu PDF, w tym wymiary strony, automatyczne skalowanie oraz konkretne układy DGN (widoki), które mają zostać uwzględnione w końcowym PDF.

## Krok 4: Zapisz plik PDF

```java
objImage.save(outFile, options);
```

Zapisz wyeksportowany plik PDF. Metoda `save` zastosuje wszystkie opcje skonfigurowane w poprzednim kroku.

Powtórz te kroki dla dowolnych dodatkowych plików DGN, które chcesz przekonwertować. Gratulacje! Pomyślnie **konwertowałeś CAD PDF**, eksportując pliki DGN do formatu AutoCAD w PDF przy użyciu Aspose.CAD dla Java.

## Typowe problemy i rozwiązania
| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Plik nie znaleziony** | Nieprawidłowa ścieżka `dataDir` | Sprawdź dokładnie ścieżkę folderu i upewnij się, że plik DGN istnieje. |
| **Puste strony w PDF** | `AutomaticLayoutsScaling` ustawiony na `false` lub brak identyfikatorów układów | Pozostaw `setAutomaticLayoutsScaling(true)` i zweryfikuj nazwy układów (`"1","2",…`). |
| **Niska rozdzielczość wyjścia** | Domyślna DPI rasteryzacji jest niska | Użyj `vectorOptions.setResolution(300);`, aby zwiększyć jakość (dodaj przed `setVectorRasterizationOptions`). |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji w produkcji | Zastosuj tymczasową lub zakupioną licencję, jak opisano w dokumentacji Aspose. |

## Najczęściej zadawane pytania (dodatkowe)

**Q: Czy mogę wyeksportować tylko pojedynczy układ z pliku DGN zawierającego wiele układów?**  
A: Tak – określ żądane identyfikatory układów w `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: Czy możliwe jest osadzenie czcionek w powstałym PDF?**  
A: Aspose.CAD automatycznie osadza niezbędne czcionki podczas rasteryzacji danych wektorowych; możesz także kontrolować osadzanie czcionek poprzez `PdfOptions`, jeśli zajdzie taka potrzeba.

**Q: Jak przetworzyć wiele plików DGN w trybie wsadowym?**  
A: Umieść kroki w pętli `for`, która iteruje po liście nazw plików, ponownie używając tego samego obiektu `PdfOptions` dla każdej iteracji.

**Q: Czy biblioteka obsługuje PDF‑y zabezpieczone hasłem?**  
A: Tak – możesz ustawić hasło na obiekcie `PdfOptions` za pomocą `options.setPassword("yourPassword");`.

**Q: Gdzie mogę znaleźć więcej przykładów?**  
A: Oficjalna dokumentacja Aspose.CAD oraz repozytorium przykładów zawierają wiele dodatkowych scenariuszy.

## FAQ (Oryginalne)

### Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

A1: Tak, Aspose.CAD obsługuje szeroką gamę formatów CAD, zapewniając wszechstronność w obsłudze różnych typów plików.

### Q2: Czy mogę dostosować ustawienia eksportu PDF?

A2: Oczywiście. Jak pokazano w samouczku, możesz zmieniać opcje takie jak wymiary strony i układy, aby dopasować je do swoich wymagań.

### Q3: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?

A3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia społeczności i dyskusji.

### Q4: Czy dostępna jest darmowa wersja próbna?

A4: Tak, możesz uzyskać darmowy trial [tutaj](https://releases.aspose.com/).

### Q5: Jak mogę uzyskać tymczasową licencję?

A5: Pobierz tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/).

## Zakończenie

W tym samouczku omówiliśmy, jak **konwertować CAD PDF** przy użyciu Aspose.CAD dla Java. Kilka linijek kodu pozwala załadować rysunek DGN, dopracować opcje eksportu PDF i wygenerować wysokiej jakości PDF‑y gotowe do udostępniania lub archiwizacji. Zachęcamy do eksperymentowania z różnymi rozmiarami stron, układami lub przetwarzaniem wsadowym, aby dopasować rozwiązanie do potrzeb projektu.

---

**Ostatnia aktualizacja:** 2026-05-04  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}