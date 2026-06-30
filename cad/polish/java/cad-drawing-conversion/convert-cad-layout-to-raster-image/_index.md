---
date: 2026-02-17
description: Dowiedz się, jak konwertować pliki DWG na PNG i eksportować CAD jako
  PNG lub inne formaty rastrowe przy użyciu Aspose.CAD for Java. Uzyskaj wysokiej
  jakości wyniki szybko.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Konwertuj DWG na PNG i inne formaty rastrowe przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PNG i innych formatów rastrowych przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

Konwersja DWG do PNG (lub innych formatów obrazu rastrowego) jest częstym wymogiem, gdy trzeba udostępnić rysunki CAD współpracownikom, którzy nie mają przeglądarki CAD, osadzić projekty w dokumentacji lub wygenerować miniatury do galerii internetowych. **W tym przewodniku dowiesz się, jak szybko i niezawodnie konwertować dwg do png**, niezależnie od tego, czy pracujesz z pełnym plikiem rysunku, czy tylko z określonym układem. Możesz także potrzebować **konwertować CAD do rastrowego** w celu podglądów internetowych, narzędzi raportowych lub aplikacji mobilnych. Aspose.CAD dla Javy upraszcza tę konwersję i daje pełną kontrolę nad rozdzielczością, wyborem układu i formatem wyjściowym.

## Szybkie odpowiedzi
- **Jaką bibliotekę używać do DWG → PNG?** Aspose.CAD dla Javy  
- **Jakie formaty można eksportować?** PNG, JPEG, TIFF, PDF, BMP i inne  
- **Czy potrzebna jest licencja do testów?** Darmowa wersja próbna wystarcza do rozwoju; licencja jest wymagana w produkcji  
- **Czy mogę wybrać konkretny układ?** Tak, użyj `setLayouts`, aby wybrać „Model”, „Layout1” itp.  
- **Czy możliwe jest wyjście w wysokiej rozdzielczości?** Oczywiście — dostosuj `setPageWidth` i `setPageHeight`, aby kontrolować DPI  

## Co to jest „convert dwg to png”?

Wyrażenie „convert dwg to png” opisuje proces pobrania wektorowego pliku DWG (rodzimego formatu wielu aplikacji CAD) i przekształcenia go w obraz pikselowy PNG. Obrazy rastrowe są idealne do wyświetlania w sieci, udostępniania e‑mailami i integracji z oprogramowaniem nie‑CAD.

## Dlaczego eksportować CAD jako PNG (lub inne formaty rastrowe)?

- **Uniwersalna kompatybilność:** PNG i JPEG są obsługiwane praktycznie przez każdy podgląd obrazu i przeglądarkę.  
- **Szybkie ładowanie:** Obrazy rastrowe ładują się natychmiast w porównaniu z otwieraniem ciężkiego pliku DWG.  
- **Łatwe osadzanie:** Wstaw PNG bezpośrednio do Worda, PowerPointa lub HTML bez dodatkowych wtyczek.  
- **Spójny wygląd:** Ty kontrolujesz rozdzielczość, tło i układ, zapewniając, że każdy interesariusz widzi tę samą wizualizację.  

## Typowe scenariusze użycia

| Scenariusz | Dlaczego wyjście rastrowe pomaga |
|------------|-----------------------------------|
| **Dokumentacja projektowa** | Osadzanie PNG w PDF‑ach lub dokumentach Word eliminuje konieczność posiadania oprogramowania CAD przez recenzentów. |
| **Portale internetowe** | Miniatury generowane z plików DWG ładują się natychmiast i poprawiają doświadczenie użytkownika. |
| **Aplikacje mobilne** | Obrazy rastrowe wyświetlają się poprawnie na urządzeniach, które nie mają przeglądarki CAD. |
| **Automatyczne raportowanie** | Konwersja wsadowa wielu układów do PNG/JPEG w celu wstawienia ich do wykresów lub pulpitów nawigacyjnych. |

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Środowisko programistyczne Java** – zainstalowany i skonfigurowany JDK 8 lub nowszy.  
2. **Aspose.CAD dla Javy** – pobierz najnowszy plik JAR z [dokumentacji Aspose.CAD dla Javy](https://reference.aspose.com/cad/java/).  

## Importowanie przestrzeni nazw

Najpierw zaimportuj potrzebne klasy. Te importy dają dostęp do ładowania obrazu, opcji rasteryzacji oraz ustawień wyjściowych TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Wskazówka:** Jeśli zamierzasz **eksportować CAD jako PNG** zamiast TIFF, zamień `TiffOptions` na `PngOptions` (znajdujące się w `com.aspose.cad.imageoptions.PngOptions`).

## Przewodnik krok po kroku

### Krok 1: Skonfiguruj katalog zasobów

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Zastąp `"Your Document Directory"` pełną ścieżką, w której znajdują się Twoje pliki CAD.

### Krok 2: Załaduj plik CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Możesz załadować dowolny obsługiwany format (DWG, DXF, DGN itp.). To jest część **how to convert cad** – po prostu wskaż plik i pozwól Aspose zająć się parsowaniem.

### Krok 3: Skonfiguruj opcje rasteryzacji

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` kontrolują rozdzielczość wyjściową (większe wartości = wyższe DPI).  
- `setLayouts` pozwala **convert CAD to raster** dla wybranych układów; pomiń tę metodę, aby rasteryzować cały rysunek.

### Krok 4: Ustaw opcje obrazu

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Jeśli wolisz PNG, utwórz `PngOptions` zamiast `TiffOptions`. Tutaj odbywa się **export CAD as PNG**.

### Krok 5: Zapisz wynikowy obraz

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Zmień rozszerzenie pliku na `.png` (i obiekt opcji na `PngOptions`), aby **save CAD as JPEG/PNG**.

> **Typowy błąd:** Nie dopasowanie rozszerzenia pliku do klasy opcji spowoduje `UnsupportedFormatException`. Zawsze utrzymuj je w zgodzie.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|---------|-------------|
| **Pusty obraz wyjściowy** | Sprawdź, czy nazwy układów w `setLayouts` dokładnie odpowiadają tym w źródłowym pliku CAD. |
| **Niska rozdzielczość PNG** | Zwiększ `setPageWidth` / `setPageHeight` lub ustaw `setResolution` w opcjach rasteryzacji. |
| **Nieobsługiwana wersja DWG** | Upewnij się, że używasz najnowszej wersji Aspose.CAD; starsze wersje mogą nie obsługiwać nowszych wydań DWG. |
| **Błędy pamięci przy dużych plikach** | Przetwarzaj strony po jednej lub zwiększ pamięć JVM (`-Xmx2g`). |

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD jest kompatybilny z różnymi formatami plików CAD?**  
O: Tak, obsługuje DWG, DXF, DGN i wiele innych.

**P: Czy mogę dostosować rozdzielczość wyjściowego obrazu rastrowego?**  
O: Oczywiście. Dostosuj `setPageWidth`, `setPageHeight` lub `setResolution` w `CadRasterizationOptions`.

**P: Jak mogę konwertować wiele układów CAD w jednym uruchomieniu?**  
O: Przekaż tablicę z nazwami wszystkich układów do `setLayouts`, np. `new String[]{"Model","Layout1","Layout2"}`.

**P: Czy oprócz TIFF dostępne są inne formaty wyjściowe?**  
O: Tak — PNG, JPEG, BMP, PDF i inne są dostępne poprzez ich odpowiednie klasy `*Options`.

**P: Gdzie mogę uzyskać pomoc lub podzielić się doświadczeniami z Aspose.CAD?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) dla wsparcia społeczności i pomocy oficjalnej.

## Zakończenie

Postępując zgodnie z tymi krokami, możesz **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG** lub wygenerować dowolny inny potrzebny format rastrowy. Aspose.CAD dla Javy zajmuje się ciężką pracą, pozwalając Ci skupić się na integracji wysokiej jakości obrazów w aplikacjach, dokumentacji lub portalach internetowych.

---

**Ostatnia aktualizacja:** 2026-02-17  
**Testowano z:** Aspose.CAD dla Javy 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}