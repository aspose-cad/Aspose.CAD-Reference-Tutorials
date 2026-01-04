---
date: 2026-01-04
description: Dowiedz się, jak **zapisać CAD jako PNG** i bez wysiłku eksportować obiekty
  OLE z plików CAD przy użyciu Aspose.CAD dla Javy. Szybka konfiguracja, pełny przykład
  kodu i wskazówki najlepszych praktyk.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Zapisz CAD jako PNG i eksportuj obiekty OLE przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz CAD jako PNG i eksportuj obiekty OLE przy użyciu Aspose.CAD dla Java

## Wprowadzenie

W szybko zmieniającym się świecie Computer‑Aided Design (CAD), możliwość **zapisania CAD jako PNG** przy jednoczesnym wyodrębnianiu osadzonych obiektów OLE (Object Linking and Embedding) może znacząco usprawnić Twój przepływ pracy. Niezależnie od tego, czy tworzysz narzędzie do konwersji wsadowej, generujesz miniatury dla portalu internetowego, czy po prostu potrzebujesz archiwizować zawartość OLE, Aspose.CAD dla Java zapewnia czysty, programowy sposób realizacji tego zadania. W tym samouczku przeprowadzimy Cię przez cały proces, od konfiguracji projektu po eksport każdego obiektu OLE jako obrazu PNG.

## Szybkie odpowiedzi
- **Czy mogę eksportować obiekty OLE bezpośrednio do PNG?** Tak – Aspose.CAD ładuje plik CAD i pozwala rasteryzować każdy układ do PNG.  
- **Jaką wersję Javy wymaga?** Java 8 lub nowsza.  
- **Czy potrzebna jest licencja na tę funkcję?** Darmowa wersja próbna działa w ocenie; licencja jest wymagana w środowisku produkcyjnym.  
- **Czy dane wektorowe zostaną zachowane?** Rasteryzacja PNG zachowuje wierność wizualną, ale wynik jest rastrem, nie wektorem.  
- **Czy obsługiwane jest przetwarzanie wsadowe?** Absolutnie – iteruj po tablicy plików, jak pokazano w przykładzie kodu.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz następujące elementy:

- **Java Development Kit (JDK)** – Java 8+ zainstalowana i skonfigurowana.  
- **Aspose.CAD for Java** – Pobierz najnowszą bibliotekę z [download link](https://releases.aspose.com/cad/java/).  
- **Pliki źródłowe CAD** – Dowolne pliki DWG/DXF/DGN zawierające obiekty OLE, które chcesz wyeksportować.

## Importowanie przestrzeni nazw

Aby pracować z plikami CAD, musisz zaimportować podstawowe klasy Aspose.CAD. Zachowaj blok importu dokładnie tak, jak pokazano – dostarcza on klasy używane później w samouczku.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Jak zapisać CAD jako PNG

Poniżej znajduje się zwięzły przewodnik krok po kroku, który pokazuje **jak eksportować obiekty OLE i zapisać CAD jako PNG**. Każdy krok zawiera krótkie wyjaśnienie oraz dokładny kod, który należy skopiować do projektu.

### Krok 1: Ustaw katalog dokumentów

Zdefiniuj folder, w którym znajdują się Twoje rysunki CAD. Zastąp placeholder rzeczywistą ścieżką na swoim komputerze.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Krok 2: Zdefiniuj nazwy plików CAD

Wypisz wszystkie pliki CAD, które chcesz przetworzyć. Możesz dodać dowolną liczbę wpisów.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Krok 3: Ustaw opcje eksportu PNG

Skonfiguruj ustawienia rasteryzacji. Tutaj wybieramy konkretny układ (`Layout1`) i używamy domyślnych opcji PNG.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Krok 4: Iteruj po plikach CAD i zapisz jako PNG

Wczytaj każdy plik CAD, rasteryzuj obiekty OLE i zapisz wynikowy plik PNG. Suffix `_out.png` pomaga zidentyfikować wygenerowane obrazy.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **`Image.load` throws `FileNotFoundException`** | Ścieżka `dataDir` jest niepoprawna lub nazwa pliku zawiera literówkę. | Sprawdź ponownie ciąg katalogu i upewnij się, że nazwy plików dokładnie się zgadzają, łącznie ze spacjami. |
| **Output PNG is blank** | Nazwa układu nie istnieje w źródłowym pliku CAD. | Użyj `cadImage.getLayouts()`, aby wyświetlić dostępne układy, a następnie zaktualizuj `rasterizationOptions.setLayouts(...)`. |
| **Large CAD files cause OutOfMemoryError** | Rasteryzacja obrazów wysokiej rozdzielczości zużywa dużo pamięci sterty. | Zwiększ pamięć sterty JVM (`-Xmx2g`) lub obniż rozdzielczość rasteryzacji za pomocą `rasterizationOptions.setResolution(...)`. |

## FAQ

### Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

Tak – Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF i DGN. Zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/java/), aby zobaczyć pełną listę.

### Q2: Czy mogę dostosować ustawienia eksportu dla obiektów OLE?

Tak, Aspose.CAD oferuje rozbudowane opcje dostosowywania ustawień eksportu, umożliwiając dopasowanie wyniku do Twoich konkretnych wymagań.

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.CAD?

Tak, możesz zapoznać się z możliwościami Aspose.CAD, pobierając darmową wersję próbną [tutaj](https://releases.aspose.com/).

### Q4: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD?

Dołącz do społeczności Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i podzielić się doświadczeniami.

### Q5: Jak mogę zakupić licencję na Aspose.CAD?

Odwiedź [stronę zakupu](https://purchase.aspose.com/buy), aby nabyć licencję odpowiadającą Twoim potrzebom programistycznym.

## Podsumowanie

Postępując zgodnie z tymi pięcioma prostymi krokami, możesz **zapisać CAD jako PNG** i wyodrębnić każdy osadzony obiekt OLE przy użyciu kilku linii kodu Java. To podejście jest idealne do konwersji wsadowych, automatycznych raportów lub każdego scenariusza, w którym potrzebne są obrazy rastrowe zawartości CAD bez ręcznego eksportu. Śmiało eksperymentuj z różnymi opcjami rasteryzacji, aby dopasować je do wymagań jakości i wydajności.

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}