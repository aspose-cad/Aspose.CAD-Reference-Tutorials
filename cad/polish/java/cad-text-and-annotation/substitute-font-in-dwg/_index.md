---
date: 2026-05-04
description: Dowiedz się, jak konwertować pliki dxf na dwg i ustawiać podstawową czcionkę
  w Javie przy użyciu Aspose.CAD. Przewodnik krok po kroku do perfekcyjnych wizualizacji
  CAD.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Zastąp czcionkę w DWG
second_title: Aspose.CAD Java API
title: Konwertuj dxf na dwg i zmień czcionkę w DWG przy użyciu Aspose.CAD Java
url: /pl/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak załadować plik DWG w Javie i zamienić czcionkę przy użyciu Aspose.CAD

## Wprowadzenie

Jeśli potrzebujesz **convert dxf to dwg** w aplikacjach Java i chcesz nadać swoim rysunkom profesjonalny wygląd, zamiana czcionki to szybkie rozwiązanie. Dzięki Aspose.CAD dla Javy możesz zastąpić domyślny styl tekstu dowolną czcionką zainstalowaną w systemie, zapewniając, że każda adnotacja będzie wyświetlana dokładnie tak, jak tego oczekujesz. W tym samouczku przeprowadzimy Cię przez cały proces — od załadowania pliku DWG w Javie po użycie metody `setPrimaryFontName` do zmiany czcionki.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.CAD for Java.  
- **Czy mogę załadować plik DWG w Javie?** Tak, po prostu wywołaj `Image.load()` na ścieżce do pliku DWG.  
- **Która metoda zmienia czcionkę?** `setPrimaryFontName`.  
- **Czy potrzebuję licencji do produkcji?** Tak, wymagana jest licencja komercyjna.  
- **Czy przetwarzanie wsadowe jest możliwe?** Absolutnie – możesz pętlić przez wiele plików przy użyciu tego samego kodu.

## Co to jest **convert dxf to dwg**?

„Convert dxf to dwg” odnosi się do przekształcania pliku DXF (Drawing Exchange Format) do natywnego formatu DWG używanego przez wiele aplikacji CAD. Konwersja pozwala wziąć powszechnie obsługiwany rysunek DXF, wprowadzić go do przepływu pracy DWG, a następnie zastosować zaawansowane formatowanie — takie jak zamiana czcionki — przy użyciu Aspose.CAD.

## Dlaczego zamieniać czcionki w pliku DWG?

- **Consistency:** Gwarantuje, że wszyscy współpracownicy widzą tę samą czcionkę, niezależnie od ich lokalnych ustawień czcionek.  
- **Readability:** Niektóre domyślne czcionki CAD są trudne do odczytania na ekranach; zamiana na czystą czcionkę, taką jak Arial, poprawia przejrzystość.  
- **Branding:** Dopasowuje rysunki techniczne do korporacyjnych wytycznych stylu.  

## Typowe przypadki użycia

| Scenariusz | Dlaczego to ważne |
|------------|-------------------|
| **Masowa konwersja starszych rysunków DXF** | Możesz je przekonwertować do DWG i wymusić korporacyjną czcionkę w jednym przebiegu. |
| **Przygotowywanie rysunków do prezentacji klienta** | Spójne, czytelne czcionki sprawiają, że dokumenty wyglądają profesjonalnie. |
| **Zautomatyzowane potoki CAD** | Wbudowanie zamiany czcionki eliminuje ręczne kroki post‑procesingu. |

## Wymagania wstępne

- **Java Development Kit (JDK)** – dowolna aktualna wersja (zalecana 8+).  
- **Aspose.CAD for Java** – pobierz ze [strony internetowej](https://releases.aspose.com/cad/java/).  
- **Sample DWG/DXF file** – rysunek, który chcesz zmodyfikować (możesz użyć dowolnego pliku DWG lub DXF do testów).

## Importowanie przestrzeni nazw

W swoim projekcie Java zaimportuj niezbędne klasy do pracy z Aspose.CAD. Te importy dają dostęp do ładowania obrazów, obiektów specyficznych dla CAD oraz manipulacji stylami.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Przewodnik krok po kroku, jak zamienić czcionkę

### Krok 1: Załaduj swój plik DWG (load dwg file java)

Najpierw wskaż API na lokalizację swojego pliku DWG (lub DXF) i załaduj go do obiektu `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Jeśli pracujesz bezpośrednio z plikami DWG, zamień rozszerzenie `.dxf` na `.dwg` w zmiennej `srcFile`.

### Krok 2: Przejdź przez tabelę stylów i ustaw nazwę głównej czcionki

Każdy rysunek CAD zawiera kolekcję obiektów stylu. Przejdź przez nie w pętli i użyj metody `setPrimaryFontName` (wywołanie API, które **ustawia nazwę głównej czcionki**) aby zamienić czcionkę.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Możesz zmienić `"Arial"` na dowolną czcionkę zainstalowaną na maszynie, na której uruchamiany jest kod.

### Krok 3: Zapisz zmodyfikowany rysunek

Po zaktualizowaniu czcionki zapisz zmiany do nowego pliku DWG (lub nadpisz oryginał).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Zapisany plik teraz używa określonej czcionki, a wszystkie adnotacje tekstowe będą renderowane tą czcionką.

## Częste problemy i rozwiązania

| Problem | Rozwiązanie |
|---------|-------------|
| **Czcionka nie zastosowana** | Sprawdź, czy czcionka jest zainstalowana w systemie operacyjnym i czy jej nazwa jest dokładnie taka sama. |
| **`Image.load` zgłasza wyjątek** | Upewnij się, że ścieżka do pliku jest poprawna i że plik jest w obsługiwanym formacie DWG/DXF. |
| **Spowolnienie wydajności przy dużych plikach** | Przetwarzaj pliki w osobnym wątku lub grupuj je, aby uniknąć blokowania interfejsu użytkownika. |

## Najczęściej zadawane pytania

**P: Czy metoda `setPrimaryFontName` wpływa tylko na obiekty tekstowe?**  
A: Aktualizuje główną czcionkę w tabeli stylów, co z kolei wpływa na wszystkie obiekty tekstowe odwołujące się do tego stylu.

**P: Czy mogę użyć własnej czcionki, która nie jest zainstalowana w systemie?**  
A: Aspose.CAD korzysta z rejestru czcionek systemu operacyjnego. Aby użyć własnej czcionki, zainstaluj ją na maszynie, na której uruchamiany jest kod.

**P: Czy można zmienić czcionkę tylko dla jednej warstwy?**  
A: Tak, możesz przefiltrować style według nazwy warstwy przed wywołaniem `setPrimaryFontName`.

**P: Jaka wersja Aspose.CAD jest wymagana dla plików DWG 2022?**  
A: Najnowsza wersja (stan na 2025) w pełni obsługuje DWG 2022. Zawsze sprawdzaj notatki wydania pod kątem wsparcia konkretnych formatów.

**P: Jak obsługiwać licencjonowanie w środowisku deweloperskim?**  
A: Użyj tymczasowej licencji ewaluacyjnej do testów. W produkcji osadź zakupiony plik licencji używając `License.setLicense("Aspose.Total.Java.lic");`.

---

**Ostatnia aktualizacja:** 2026-05-04  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}