---
date: 2025-12-25
description: Dowiedz się, jak wyeksportować plik DWG do BMP przy użyciu Aspose.CAD
  dla Javy. Ten przewodnik krok po kroku pokazuje, jak dostosować rozmiar rysunku
  CAD i efektywnie konwertować CAD na BMP.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Eksport DWG do BMP – Dostosuj rozmiar CAD przy użyciu typu jednostki (Java)
url: /pl/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport DWG do BMP – Dostosowywanie Rozmiaru Rysunku CAD przy użyciu Typu Jednostki w Aspose.CAD for Java

## Wstęp

Kiedy potrzebujesz **eksportować DWG do BMP**, kontrola rozmiaru wyjściowego i jednostki miary jest niezbędna dla dalszego przetwarzania lub drukowania. W tym samouczku dowiesz się, jak dostosować rozmiar rysunku CAD i przekonwertować CAD na BMP przy użyciu Aspose.CAD for Java, wykorzystując właściwość `UnitType` do określenia jednostki miary. Kroki są wyjaśnione prostym językiem, więc możesz je śledzić nawet jeśli dopiero zaczynasz pracę z tą biblioteką.

## Szybkie odpowiedzi
- **Co oznacza „eksport DWG do BMP”?** Konwersja rysunku DWG na rastrowy obraz BMP.  
- **Która właściwość kontroluje rozmiar wyjściowy?** `CadRasterizationOptions.setUnitType()` ustawia jednostkę (np. centymetr).  
- **Czy potrzebna jest licencja do uruchomienia kodu?** Darmowa wersja próbna wystarczy do oceny; licencja jest wymagana w środowisku produkcyjnym.  
- **Czy mogę wybrać inne układy?** Tak, użyj `setLayouts()`, aby określić układy modelu lub przestrzeni papieru.  
- **Jakie formaty wyjściowe są obsługiwane?** Oprócz BMP możesz eksportować do PNG, JPEG, TIFF itp., zmieniając klasę opcji.

## Co to jest **eksport DWG do BMP**?

Eksport DWG do BMP oznacza rasteryzację wektorowego pliku DWG do obrazu bitmapowego (BMP). Jest to przydatne, gdy potrzebujesz dokładnej reprezentacji pikselowej dla starszych systemów, potoków przetwarzania obrazu lub prostych scenariuszy wyświetlania.

## Dlaczego warto dostosować rozmiar rysunku CAD przy użyciu **Typu Jednostki**?

Ustawienie typu jednostki pozwala kontrolować fizyczne wymiary eksportowanego obrazu bez ręcznego obliczania współczynników skalowania. Dzięki temu bitmapa odzwierciedla rzeczywiste wymiary (np. centymetry), co jest kluczowe przy rysunkach inżynierskich i dokumentacji drukowanej.

## Wymagania wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania:

- **Środowisko programistyczne Java** – działająca JDK (8 lub nowsza) oraz IDE lub narzędzie budujące (Maven/Gradle).  
- **Biblioteka Aspose.CAD for Java** – pobierz i zintegrować bibliotekę Aspose.CAD w swoim projekcie Java. Bibliotekę możesz uzyskać [tutaj](https://releases.aspose.com/cad/java/).

## Importowanie przestrzeni nazw

W kodzie Java dołącz niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcji Aspose.CAD. Dodaj następujące importy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Teraz przeanalizujemy proces dostosowywania rozmiaru rysunku CAD przy użyciu typu jednostki w przystępnych krokach:

## Krok 1: Definiowanie katalogu danych

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ustaw ścieżkę do katalogu, w którym znajdują się Twoje pliki CAD.

## Krok 2: Ładowanie rysunku CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Wczytaj rysunek CAD przy użyciu klasy `Image` z Aspose.CAD.

## Krok 3: Tworzenie opcji BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Zainicjuj klasę `BmpOptions` do eksportu układu CAD do formatu BMP.

## Krok 4: Konfiguracja opcji rasteryzacji

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Utwórz instancję `CadRasterizationOptions` i powiąż ją z `BmpOptions` w celu rasteryzacji wektorów.

## Krok 5: Ustawienie typu jednostki

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Określ żądany typ jednostki dla rysunku CAD. W tym przykładzie ustawiliśmy **Centymetr**, co bezpośrednio wpływa na rozmiar eksportowanego obrazu przy **dostosowywaniu rozmiaru rysunku CAD**.

## Krok 6: Ustawienie układów

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Zdefiniuj układy, które mają być brane pod uwagę podczas eksportu. W tym przypadku wybraliśmy układ **„Model”**, ale w razie potrzeby możesz przełączyć się na układy przestrzeni papieru.

## Krok 7: Eksport do BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Na koniec zapisz zmodyfikowany rysunek CAD w formacie BMP. Ten krok kończy **eksport DWG do BMP** z zachowaniem wprowadzonych korekt rozmiaru.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| **Obraz wyjściowy jest za mały** | Nie ustawiono typu jednostki lub użyto domyślnego (piksel) | Wywołaj `setUnitType()` z żądaną jednostką (np. `UnitType.Centimeter`). |
| **Wyeksportowano niewłaściwy układ** | Błąd w nazwie układu | Sprawdź nazwy układów w przeglądarce CAD; użyj dokładnego ciągu w `setLayouts()`. |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji w produkcji | Zastosuj tymczasową lub stałą licencję zgodnie z opisem w FAQ. |

## Najczęściej zadawane pytania (rozszerzone)

**P: Czy mogę używać Aspose.CAD for Java z innymi językami programowania?**  
O: Aspose.CAD głównie obsługuje Javę, ale dostępne są wersje dla innych języków, takich jak .NET.

**P: Czy istnieją różne opcje licencjonowania Aspose.CAD?**  
O: Tak, możesz zapoznać się z opcjami licencjonowania i zakupić Aspose.CAD [tutaj](https://purchase.aspose.com/buy).

**P: Czy dostępna jest darmowa wersja próbna Aspose.CAD?**  
O: Oczywiście, darmową wersję próbną znajdziesz [tutaj](https://releases.aspose.com/).

**P: Jak mogę uzyskać wsparcie dla Aspose.CAD for Java?**  
O: Odwiedź forum Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19) po kompleksową pomoc.

**P: Czy mogę uzyskać tymczasową licencję na Aspose.CAD?**  
O: Tak, tymczasową licencję można nabyć [tutaj](https://purchase.aspose.com/temporary-license/).

---

**Ostatnia aktualizacja:** 2025-12-25  
**Testowane z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}