---
date: 2025-12-28
description: Dowiedz się, jak ładować pliki DWG w projektach Java i ustawiać nazwę
  podstawowej czcionki przy użyciu Aspose.CAD dla Javy. Przewodnik krok po kroku do
  perfekcyjnych wizualizacji CAD.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Jak wczytać plik DWG w Javie i zamienić czcionkę przy użyciu Aspose.CAD
url: /pl/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wczytać plik DWG w Javie i zamienić czcionkę przy użyciu Aspose.CAD

## Wprowadzenie

Jeśli potrzebujesz **wczytać plik DWG w aplikacjach Java** i nadać swoim rysunkom profesjonalny wygląd, zamiana czcionki jest szybkim rozwiązaniem. Dzięki Aspose.CAD dla Javy możesz zastąpić domyślny styl tekstu dowolną czcionką zainstalowaną w systemie, zapewniając, że każda adnotacja będzie wyświetlana dokładnie tak, jak tego oczekujesz. W tym samouczku przeprowadzimy Cię przez cały proces – od wczytania pliku DWG w Javie po użycie metody `setPrimaryFontName` w celu zmiany czcionki.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.CAD dla Javy.
- **Czy mogę wczytać plik DWG w Javie?** Tak, wystarczy wywołać `Image.load()` z ścieżką do pliku DWG.
- **Która metoda zmienia czcionkę?** `setPrimaryFontName`.
- **Czy potrzebna jest licencja do produkcji?** Tak, wymagana jest licencja komercyjna.
- **Czy możliwe jest przetwarzanie wsadowe?** Oczywiście – można pętlić po wielu plikach przy użyciu tego samego kodu.

## Co to jest „load dwg file java”?

Wczytanie pliku DWG w środowisku Java oznacza odczytanie binarnych danych CAD do obiektu `Image`, którym Aspose.CAD może zarządzać. Po załadowaniu pliku masz pełny programowy dostęp do warstw, stylów i obiektów tekstowych.

## Dlaczego zamieniać czcionki w pliku DWG?

- **Spójność:** Gwarantuje, że wszyscy współpracownicy zobaczą tę samą czcionkę, niezależnie od ich lokalnych ustawień czcionek.  
- **Czytelność:** Niektóre domyślne czcionki CAD są trudne do odczytania na ekranie; zamiana na czystą czcionkę, taką jak Arial, poprawia przejrzystość.  
- **Branding:** Dostosowuje rysunki techniczne do wytycznych korporacyjnych.

## Wymagania wstępne

- **Java Development Kit (JDK)** – dowolna aktualna wersja (zalecane 8+).  
- **Aspose.CAD dla Javy** – pobierz ze [strony internetowej](https://releases.aspose.com/cad/java/).  
- **Przykładowy plik DWG** – rysunek, który chcesz zmodyfikować (do testów możesz użyć dowolnego pliku DWG lub DXF).

## Importowanie przestrzeni nazw

W swoim projekcie Java zaimportuj niezbędne klasy do pracy z Aspose.CAD. Te importy dają dostęp do ładowania obrazów, obiektów specyficznych dla CAD oraz manipulacji stylami.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Przewodnik krok po kroku – zamiana czcionki

### Krok 1: Wczytaj swój plik DWG (load dwg file java)

Najpierw wskaż API lokalizację pliku DWG (lub DXF) i wczytaj go do obiektu `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Wskazówka:** Jeśli pracujesz bezpośrednio z plikami DWG, zamień rozszerzenie `.dxf` na `.dwg` w zmiennej `srcFile`.

### Krok 2: Przejdź po tabeli stylów i ustaw nazwę podstawowej czcionki

Każdy rysunek CAD zawiera kolekcję obiektów stylu. Przejdź przez nie i użyj metody `setPrimaryFontName` (wywołania API, które **ustawia nazwę podstawowej czcionki**) aby zamienić czcionkę.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Możesz zmienić `"Arial"` na dowolną czcionkę zainstalowaną na maszynie uruchamiającej kod.

### Krok 3: Zapisz zmodyfikowany rysunek

Po zaktualizowaniu czcionki zapisz zmiany do nowego pliku DWG (lub nadpisz oryginał).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Zapisany plik używa teraz wskazanej czcionki, a wszystkie adnotacje tekstowe będą renderowane z tym krojem.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Czcionka nie została zastosowana** | Sprawdź, czy czcionka jest zainstalowana w systemie operacyjnym i czy jej nazwa jest wpisana dokładnie. |
| **`Image.load` zgłasza wyjątek** | Upewnij się, że ścieżka do pliku jest prawidłowa i że plik jest w obsługiwanym formacie DWG/DXF. |
| **Spowolnienie przy dużych plikach** | Przetwarzaj pliki w osobnym wątku lub partiami, aby uniknąć blokowania interfejsu użytkownika. |

## Najczęściej zadawane pytania

**P: Czy metoda `setPrimaryFontName` wpływa tylko na obiekty tekstowe?**  
O: Aktualizuje ona podstawową czcionkę w tabeli stylów, co z kolei wpływa na wszystkie obiekty tekstowe odwołujące się do tego stylu.

**P: Czy mogę użyć własnej czcionki, która nie jest zainstalowana w systemie?**  
O: Aspose.CAD korzysta z rejestru czcionek systemu operacyjnego. Aby użyć własnej czcionki, zainstaluj ją na maszynie uruchamiającej kod.

**P: Czy można zmienić czcionkę tylko dla jednej warstwy?**  
O: Tak, możesz filtrować style według nazwy warstwy przed wywołaniem `setPrimaryFontName`.

**P: Jakiej wersji Aspose.CAD potrzebuję do plików DWG 2022?**  
O: Najnowsze wydanie (stan na 2025) w pełni obsługuje DWG 2022. Zawsze sprawdzaj notatki wydania pod kątem wsparcia konkretnych formatów.

**P: Jak obsłużyć licencjonowanie w środowisku deweloperskim?**  
O: Użyj tymczasowej licencji ewaluacyjnej do testów. W produkcji osadź zakupiony plik licencji przy pomocy `License.setLicense("Aspose.Total.Java.lic");`.

---

**Ostatnia aktualizacja:** 2025-12-28  
**Testowano z:** Aspose.CAD dla Javy 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}