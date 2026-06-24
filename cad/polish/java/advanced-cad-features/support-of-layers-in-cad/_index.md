---
date: 2026-02-17
description: Dowiedz się, jak zapisać DWG jako JPEG w Javie przy użyciu Aspose.CAD,
  dodać wiele warstw i dostosować wymiary CAD dla precyzyjnej konwersji obrazu.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Zapisz DWG jako JPEG z obsługą warstw w Javie
url: /pl/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz DWG jako JPEG z obsługą warstw w Javie

## Introduction

W tym samouczku dowiesz się, jak **zapisz DWG jako JPEG** wykorzystując pełne możliwości obsługi warstw w Aspose.CAD dla Javy. Warstwy pozwalają izolować konkretne części rysunku, co ułatwia eksport tylko tego, co potrzebne. Przejdziemy krok po kroku, od konfiguracji środowiska po eksport JPEG zawierającego wybrane warstwy.

## Quick Answers
- **Co oznacza „zapisz DWG jako JPEG”?** Konwertuje rysunek DWG (lub inny CAD) na rastrowy obraz JPEG.  
- **Czy mogę uwzględnić tylko wybrane warstwy?** Tak – użyj metody `setLayers`, aby określić, które warstwy mają być renderowane.  
- **Jak zmienić rozmiar obrazu?** Dostosuj `setPageWidth` i `setPageHeight` w `CadRasterizationOptions`.  
- **Czy to rozwiązanie tylko dla Javy?** Przykład używa Aspose.CAD dla Javy, ale te same koncepcje mają zastosowanie w innych językach.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.

## What is “save DWG as JPEG”?
Zapisanie DWG jako JPEG oznacza rasteryzację wektorowego pliku CAD (DWG, DWF, DXF itp.) do standardowego bitmapowego obrazu JPEG. Jest to przydatne, gdy trzeba osadzić rysunki CAD w stronach internetowych, e‑mailach lub raportach, które obsługują wyłącznie obrazy rastrowe.

## Why use layer‑aware JPEG conversion?
- **Skup się na istotnych danych:** Eksportuj tylko potrzebne warstwy, zmniejszając rozmiar pliku i bałagan wizualny.  
- **Zachowaj zamysł projektu:** Warstwy utrzymują logiczne grupowanie obiektów, dzięki czemu możesz ponownie używać tego samego pliku źródłowego do różnych wyjść.  
- **Pełna kontrola nad wymiarami:** Dostosowując opcje rasteryzacji, możesz tworzyć obrazy wysokiej rozdzielczości, które spełniają wymagania publikacji.

## Prerequisites

Zanim zanurzysz się w temat, upewnij się, że masz następujące elementy:

1. **Aspose.CAD for Java Library** – pobierz ją ze [strony internetowej](https://releases.aspose.com/cad/java/). Postępuj zgodnie z przewodnikiem instalacji, aby dodać pliki JAR do classpathu projektu.  
2. **Środowisko programistyczne Java** – zainstalowane na komputerze aktualne JDK (8 lub nowsze).

Teraz, gdy wszystko jest gotowe, przyjrzyjmy się kodowi potrzebnemu do **zapisania DWG jako JPEG** z selektywnym renderowaniem warstw.

## Import Namespaces

Rozpocznij od zaimportowania wymaganych klas Aspose.CAD oraz standardowych narzędzi Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

Zdefiniuj, gdzie znajduje się źródłowy plik DWF i gdzie zostanie zapisany wynikowy plik JPEG.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

Użyj metody `Image.load` z Aspose.CAD, aby wczytać rysunek CAD.

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

Utwórz instancję `CadRasterizationOptions` i ustaw pożądany rozmiar wyjścia. Zmiana tych wartości pozwala **dostosować wymiary CAD** dla ostatecznego JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

Jeśli chcesz renderować więcej niż jedną warstwę, po prostu dodaj ich nazwy do listy. Tutaj zaczynamy od jednej warstwy o nazwie „LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Wskazówka:* Aby **dodać wiele warstw**, rozbuduj wywołanie `Arrays.asList`, np. `Arrays.asList("LayerA", "LayerB", "LayerC")`. To pozwala **wybrać konkretne warstwy CAD** do konwersji.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

Połącz ustawienia rasteryzacji z formatem wyjściowym JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save DWG as JPEG)

Na koniec zapisz obraz na dysku. Ten krok **zapisuje rysunek CAD jako plik JPEG**, który zawiera tylko wybrane warstwy.

```java
image.save(outFile, jpegOptions);
```

Postępując zgodnie z tymi krokami, pomyślnie **zapisano DWG jako JPEG**, kontrolując, które warstwy są wyświetlane i dostosowując wymiary obrazu.

## How to Convert DWF to JPEG with Layer Selection

Jak przekonwertować DWF na JPEG z wyborem warstw

Chociaż przykład używa źródła DWF, ten sam potok rasteryzacji działa dla każdego obsługiwanego formatu CAD (DWG, DXF, DGN itp.). Wystarczy zmienić rozszerzenie pliku w `srcFile`, a biblioteka automatycznie wykona operację **konwersji DWF na JPEG** (lub inny format).

## Common Issues and Solutions

| Problem | Rozwiązanie |
|-------|----------|
| **Warstwy nie pojawiają się** | Sprawdź, czy nazwy warstw dokładnie odpowiadają tym zapisanym w pliku DWF (uwzględniając wielkość liter). |
| **Obraz wyjściowy jest pusty** | Upewnij się, że `setPageWidth` i `setPageHeight` są wystarczająco duże dla rozmiaru rysunku. |
| **Wyjątek licencyjny** | Użyj licencji próbnej do testów; uzyskaj pełną licencję do środowisk produkcyjnych. |

## Frequently Asked Questions

**P:** Czy mogę dodać wiele warstw do opcji rasteryzacji?  
**O:** Oczywiście. Rozszerz `stringList` o dodatkowe nazwy warstw, np. `Arrays.asList("LayerA", "LayerB")`.

**P:** Czy Aspose.CAD jest kompatybilny z innymi formatami CAD?  
**O:** Tak, obsługuje DWG, DXF, DWF i wiele innych formatów.

**P:** Jak mogę zmienić wymiary obrazu wyjściowego?  
**O:** Zmodyfikuj `setPageWidth` i `setPageHeight` w instancji `CadRasterizationOptions`.

**P:** Gdzie mogę kupić licencję na Aspose.CAD?  
**O:** Opcje licencjonowania możesz przeglądać [tutaj](https://purchase.aspose.com/buy).

**P:** Gdzie mogę uzyskać wsparcie społeczności?  
**O:** Dołącz do społeczności Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i dyskusje.

---

**Ostatnia aktualizacja:** 2026-02-17  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}