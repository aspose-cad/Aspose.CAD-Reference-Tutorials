---
date: 2025-12-16
description: Dowiedz się, jak konwertować CAD na PNG przy użyciu Aspose.CAD dla Javy,
  obejmując eksport DWG do obrazu, zapisywanie CAD jako PNG oraz opcje konwersji CAD
  na obraz rastrowy.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Jak przekonwertować CAD na PNG przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak przekonwertować CAD na PNG przy użyciu Aspose.CAD dla Javy

We współczesnych przepływach pracy inżynierskiej często trzeba **convert CAD to PNG**, aby rysunki mogły być wyświetlane w przeglądarkach, osadzane w dokumentach lub udostępniane interesariuszom, którzy nie mają oprogramowania CAD. Ten samouczek przeprowadzi Cię przez cały proces — od wczytania pliku CAD po wyeksportowanie wysokiej jakości rastrowego obrazu PNG — przy użyciu potężnej biblioteki Aspose.CAD dla Javy.

## Szybkie odpowiedzi
- **Jaki jest główny cel?** Konwertowanie rysunków CAD na rastrowe obrazy PNG.  
- **Która biblioteka jest używana?** Aspose.CAD for Java.  
- **Czy potrzebna jest licencja?** Dostępna jest darmowa wersja próbna; licencja jest wymagana do użytku produkcyjnego.  
- **Czy mogę dostosować rozmiar obrazu?** Tak, użyj `CadRasterizationOptions`, aby ustawić szerokość i wysokość.  
- **Obsługiwane formaty CAD?** DWG, DXF, DWF i wiele innych.

## Co to jest „convert CAD to PNG”?
Konwertowanie CAD na PNG oznacza rasteryzację wektorowej zawartości CAD (DWG, DXF itp.) do formatu obrazu opartego na pikselach. PNG zachowuje przezroczystość i jakość bezstratną, co czyni go idealnym do podglądów internetowych, dokumentacji i raportowania.

## Dlaczego konwertować CAD na PNG (cad na obraz rastrowy)?
- **Uniwersalne przeglądanie:** PNG działa na każdym urządzeniu bez specjalnych przeglądarek CAD.  
- **Szybkie ładowanie:** Obrazy rastrowe ładują się natychmiast na stronach internetowych.  
- **Łatwe osadzanie:** Wstaw PNG do plików PDF, dokumentów Word lub prezentacji.  
- **Spójny wygląd:** Zachowuje grubości linii, kolory i warstwy dokładnie tak, jak zostały zaprojektowane.

## Wymagania wstępne
1. **Środowisko programistyczne Java** – zainstalowany i skonfigurowany JDK 8 lub nowszy.  
2. **Biblioteka Aspose.CAD** – Pobierz i dodaj bibliotekę do swojego projektu. Bibliotekę znajdziesz **[tutaj](https://releases.aspose.com/cad/java/)**.

## Importowanie przestrzeni nazw
Dodaj wymagane importy do swojej klasy Java, aby móc pracować z obiektami Aspose.CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Przewodnik krok po kroku konwersji CAD na PNG

### Krok 1: Wczytaj rysunek CAD
Najpierw wczytaj źródłowy plik CAD (DXF, DWG itp.) przy użyciu `Image.load()`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **Wskazówka:** Przechowuj pliki CAD w dedykowanym folderze (np. `CADConversion`), aby uniknąć problemów ze ścieżkami.

### Krok 2: Ustaw opcje rasteryzacji (eksport dwg do obrazu)
Zdefiniuj rozmiar wyjściowego obrazu oraz inne ustawienia rasteryzacji.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

Możesz także kontrolować kolor tła, tryb renderowania linii oraz DPI, jeśli jest to potrzebne.

### Krok 3: Utwórz opcje obrazu (zapisz CAD jako PNG)
Utwórz instancję `PngOptions` i dołącz ustawienia rasteryzacji.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 4: Zapisz obraz rastrowy (plik CAD do PNG)
Na koniec zapisz plik PNG na dysku.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Powstały plik `conic_pyramid_raster_image_out.png` jest wysokiej rozdzielczości reprezentacją PNG Twojego pierwotnego rysunku CAD.

### Powtórz dla innych plików
Po prostu zmień `srcFile`, aby wskazywał inny plik CAD i uruchom te same kroki. Ten sam kod działa dla DWG, DWF i innych obsługiwanych formatów.

## Typowe problemy i rozwiązania
| Problem | Rozwiązanie |
|-------|----------|
| **Blank PNG output** | Verify that the source CAD file loads correctly (`Image.load()` should not throw). |
| **Incorrect dimensions** | Adjust `PageWidth` / `PageHeight` or set DPI via `rasterizationOptions.setResolution(...)`. |
| **Missing layers** | Ensure the CAD file’s layers are not hidden; use `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`. |
| **License errors** | Use a valid Aspose.CAD license file (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## Najczęściej zadawane pytania

**Pytanie 1:** Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami CAD?  
A1: Aspose.CAD obsługuje szeroką gamę formatów CAD, w tym DWG, DXF, DWF i inne. Pełną listę znajdziesz w **[dokumentacji](https://reference.aspose.com/cad/java/)**.

**Pytanie 2:** Czy mogę dostosować opcje rasteryzacji do moich konkretnych potrzeb?  
A2: Tak, Aspose.CAD zapewnia elastyczność w ustawianiu opcji rasteryzacji, pozwalając dostosować wyjście do wymagań (rozmiar, DPI, kolor tła itp.).

**Pytanie 3:** Gdzie mogę znaleźć wsparcie w kwestiach związanych z Aspose.CAD?  
A3: Odwiedź **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**, aby uzyskać pomoc i skontaktować się ze społecznością.

**Pytanie 4:** Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Javy?  
A4: Tak, możesz wypróbować funkcje Aspose.CAD, uzyskując darmową wersję próbną **[tutaj](https://releases.aspose.com/)**.

**Pytanie 5:** Jak mogę kupić Aspose.CAD dla Javy?  
A5: Aby zakupić Aspose.CAD dla Javy, odwiedź **[stronę zakupu](https://purchase.aspose.com/buy)**.

**Ostatnia aktualizacja:** 2025-12-16  
**Testowano z:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}