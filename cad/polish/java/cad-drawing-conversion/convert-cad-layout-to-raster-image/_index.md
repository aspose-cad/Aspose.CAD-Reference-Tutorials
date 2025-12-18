---
date: 2025-12-18
description: Naucz się konwertować DWG na PNG i inne formaty obrazów rastrowych za
  pomocą Aspose.CAD dla Javy. Eksportuj CAD jako PNG z wysoką jakością.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Konwertuj DWG na PNG i inne formaty rastrowe przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PNG i innych formatów rastrowych przy użyciu Aspose.CAD for Java

## Wprowadzenie

Konwersja DWG do PNG (lub innych formatów obrazu rastrowego) jest powszechnym wymaganiem, gdy musisz udostępnić rysunki CAD współpracownikom, którzy nie mają przeglądarki CAD, osadzić projekty w dokumentacji lub wygenerować miniatury do galerii internetowych. Aspose.CAD for Java upraszcza tę konwersję, niezależnie od tego, czy pracujesz z pełnym plikiem rysunku, czy tylko z konkretnym układem. W tym samouczku przeprowadzimy Cię przez dokładne kroki, aby **przekształcić układ CAD na obraz rastrowy** — tę samą technikę, którą możesz zastosować do generowania wyjść PNG, JPEG, TIFF lub PDF.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje DWG do PNG?** Aspose.CAD for Java  
- **Jakie formaty mogą być eksportowane?** PNG, JPEG, TIFF, PDF, BMP i inne  
- **Czy potrzebna jest licencja do testowania?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja jest wymagana w produkcji  
- **Czy mogę wybrać konkretny układ?** Tak, użyj `setLayouts`, aby wybrać „Model”, „Layout1” itp.  
- **Czy możliwy jest output w wysokiej rozdzielczości?** Oczywiście — dostosuj `setPageWidth` i `setPageHeight`, aby kontrolować DPI  

## Co to jest „convert dwg to png”?

Wyrażenie „convert dwg to png” opisuje proces przekształcenia wektorowego pliku DWG (rodzimego formatu wielu aplikacji CAD) w obraz rastrowy PNG oparty na pikselach. Obrazy rastrowe są idealne do wyświetlania w sieci, udostępniania e‑mailami i integracji z oprogramowaniem nie‑CAD.

## Dlaczego eksportować CAD jako PNG (lub inne formaty rastrowe)?

- **Uniwersalna kompatybilność:** PNG i JPEG są obsługiwane praktycznie przez każdy przeglądarkę i program do wyświetlania obrazów.  
- **Szybkie ładowanie:** Obrazy rastrowe ładują się natychmiast w porównaniu do otwierania dużego pliku DWG.  
- **Łatwe osadzanie:** Wstaw PNG bezpośrednio do Worda, PowerPointa lub HTML bez dodatkowych wtyczek.  
- **Spójny wygląd:** Kontrolujesz rozdzielczość, tło i układ, zapewniając, że każdy interesariusz widzi tę samą wizualizację.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Java Development Environment** – JDK 8 lub nowszy zainstalowany i skonfigurowany.  
2. **Aspose.CAD for Java** – Pobierz najnowszy plik JAR z [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Importowanie przestrzeni nazw

Najpierw zaimportuj klasy, które będą potrzebne. Te importy dają dostęp do ładowania obrazu, opcji rasteryzacji oraz ustawień wyjścia TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** Jeśli planujesz eksport do PNG zamiast TIFF, zamień `TiffOptions` na `PngOptions` (znajduje się w `com.aspose.cad.imageoptions.PngOptions`).

## Przewodnik krok po kroku

### Krok 1: Skonfiguruj katalog zasobów

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Zastąp `"Your Document Directory"` absolutną ścieżką, w której znajdują się Twoje pliki CAD.

### Krok 2: Załaduj plik CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Możesz załadować dowolny obsługiwany format (DWG, DXF, DGN itp.). To jest część **jak konwertować CAD** — po prostu wskaż plik i pozwól Aspose obsłużyć parsowanie.

### Krok 3: Skonfiguruj opcje rasteryzacji

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` kontrolują rozdzielczość wyjściową (większe wartości = wyższe DPI).  
- `setLayouts` pozwala **przekształcić CAD na raster** dla konkretnych układów; pomiń, aby rasteryzować cały rysunek.

### Krok 4: Ustaw opcje obrazu

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Jeśli wolisz PNG, utwórz instancję `PngOptions` zamiast `TiffOptions`. To miejsce, w którym **eksportujesz CAD jako PNG**.

### Krok 5: Zapisz wynikowy obraz

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Zmień rozszerzenie pliku na `.png` (oraz obiekt opcji na `PngOptions`), aby **zapisać CAD jako JPEG/PNG**.

> **Common Pitfall:** Zapomnienie dopasowania rozszerzenia pliku do klasy opcji spowoduje `UnsupportedFormatException`. Zawsze utrzymuj je w zgodzie.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Blank output image** | Sprawdź, czy nazwy układów w `setLayouts` dokładnie odpowiadają tym w źródłowym pliku CAD. |
| **Low‑resolution PNG** | Zwiększ `setPageWidth` / `setPageHeight` lub ustaw `setResolution` w opcjach rasteryzacji. |
| **Unsupported DWG version** | Upewnij się, że używasz najnowszej wersji Aspose.CAD; starsze wersje mogą nie obsługiwać nowszych wydań DWG. |
| **Memory errors on large files** | Przetwarzaj strony pojedynczo lub zwiększ przydział pamięci JVM (`-Xmx2g`). |

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny z różnymi formatami plików CAD?**  
A: Tak, obsługuje DWG, DXF, DGN i wiele innych.

**Q: Czy mogę dostosować rozdzielczość wyjściowego obrazu rastrowego?**  
A: Oczywiście. Dostosuj `setPageWidth`, `setPageHeight` lub `setResolution` w `CadRasterizationOptions`.

**Q: Jak mogę konwertować wiele układów CAD w jednym uruchomieniu?**  
A: Przekaż tablicę ze wszystkimi nazwami układów do `setLayouts`, np. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Czy oprócz TIFF dostępne są inne formaty wyjściowe?**  
A: Tak — PNG, JPEG, BMP, PDF i inne są dostępne poprzez ich odpowiednie klasy `*Options`.

**Q: Gdzie mogę uzyskać pomoc lub podzielić się doświadczeniami z Aspose.CAD?**  
A: Odwiedź [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) dla wsparcia społeczności i pomocy oficjalnej.

## Zakończenie

Postępując zgodnie z tymi krokami, możesz **konwertować DWG do PNG**, **eksportować CAD jako PNG**, **zapisać CAD jako JPEG** lub wygenerować dowolny inny potrzebny format rastrowy. Aspose.CAD for Java zajmuje się ciężką pracą, pozwalając Ci skupić się na integracji wysokiej jakości obrazów w aplikacjach, dokumentacji lub portalach internetowych.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}