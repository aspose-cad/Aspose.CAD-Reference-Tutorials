---
date: 2025-12-22
description: Dowiedz się, jak eksportować rysunki CAD i konwertować pliki DWG na BMP
  w Javie przy użyciu Aspose.CAD. Postępuj zgodnie z tym przewodnikiem krok po kroku,
  aby efektywnie manipulować plikami CAD.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Jak wyeksportować rysunek CAD do BMP przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak wyeksportować rysunek CAD do BMP przy użyciu Aspose.CAD dla Java

## Introduction

Jeśli szukasz jasnego, niezawodnego sposobu na **how to export cad** pliki z Java, trafiłeś we właściwe miejsce. Z Aspose.CAD dla Java możesz nie tylko automatycznie dopasowywać rozmiary rysunków, ale także **convert DWG to BMP** w kilku linijkach kodu. Ten samouczek przeprowadzi Cię przez cały proces, od konfiguracji środowiska po wygenerowanie obrazu BMP zachowującego oryginalny układ CAD.

## Quick Answers
- **Co oznacza „how to export cad”?** Odnosi się do konwertowania plików CAD (DWG, DXF itp.) do innego formatu, takiego jak BMP, PNG lub PDF.  
- **Która biblioteka obsługuje konwersję?** Aspose.CAD dla Java udostępnia prostą API do tego zadania.  
- **Czy potrzebna jest licencja?** Tymczasowa licencja działa w testach; pełna licencja jest wymagana w produkcji.  
- **Czy mogę wyeksportować wiele układów jednocześnie?** Tak – ustawiając właściwość `Layouts`, możesz określić, które układy mają być renderowane.  
- **Czy BMP jest jedynym formatem wyjściowym?** Nie – możesz także eksportować do PNG, JPEG, TIFF i innych.

## What is “how to export cad” with Aspose.CAD?
Co oznacza „how to export cad” przy użyciu Aspose.CAD?  
Eksportowanie CAD oznacza pobranie natywnego rysunku CAD (np. pliku DWG) i przekształcenie go w obraz rastrowy lub inny format wektorowy. Aspose.CAD zajmuje się całą ciężką pracą: parsowaniem struktury CAD, rasteryzacją elementów wektorowych oraz zapisem wyniku w wybranym formacie obrazu.

## Why use Aspose.CAD for Java to **convert DWG to BMP**?
- **Brak zewnętrznych zależności** – czysta Java, bez natywnych DLL.  
- **Pełne wsparcie dla DWG, DXF, DGN i innych formatów**.  
- **Precyzyjna kontrola** nad opcjami rasteryzacji, takimi jak wybór układu, skalowanie i kolor tła.  
- **Wysoka wydajność** odpowiednia do przetwarzania wsadowego na serwerach.

## Prerequisites

Zanim rozpoczniesz, upewnij się, że masz następujące:

1. **Java Development Kit** – pobierz go [tutaj](https://www.java.com/en/download/).  
2. **Biblioteka Aspose.CAD dla Java** – pobierz najnowszy JAR [tutaj](https://releases.aspose.com/cad/java/).  
3. **Przykładowy plik CAD** – plik DWG (np. `sample.dwg`) umieszczony w katalogu dokumentów Twojego projektu.

## Import Namespaces

W swojej aplikacji Java, dołącz niezbędne przestrzenie nazw, aby korzystać z funkcjonalności Aspose.CAD. Oto przykład:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Teraz rozbijmy proces **how to export cad** na przystępne kroki.

## Step‑by‑Step Guide

### Step 1: Load the CAD Drawing

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Ładujemy źródłowy plik DWG do obiektu `Image`, który służy jako punkt wejścia dla wszystkich dalszych operacji.

### Step 2: Create `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` będzie przechowywać ustawienia rasteryzacji specyficzne dla wyjścia BMP.

### Step 3: Configure Rasterization Settings

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Tutaj łączymy opcje rasteryzacji z opcjami BMP, co pozwala kontrolować, jak elementy CAD są renderowane.

### Step 4: Set the Layout(s) to Export

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Właściwość `Layouts` informuje Aspose.CAD, które układy rysunku mają zostać uwzględnione. W większości przypadków, `"Model"` jest głównym układem, który chcesz przekonwertować.

### Step 5: Export to BMP Format

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Wywołanie `save` z skonfigurowanymi `BmpOptions` zapisuje plik BMP na dysku. To kończy przepływ pracy **convert DWG to BMP**.

## Common Issues and Solutions

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| Obraz wyjściowy jest pusty | Nieprawidłowa nazwa układu lub brak układu | Zweryfikuj, czy nazwa układu odpowiada plikowi CAD (np. `"Model"`). |
| Niska rozdzielczość | Domyślne DPI jest niskie | Ustaw `cadRasterizationOptions.setResolution(300);` przed zapisem. |
| Błąd braku pamięci przy dużych plikach | Duże rysunki wymagają więcej pamięci heap | Zwiększ rozmiar pamięci JVM (`-Xmx2g`) lub przetwarzaj strony pojedynczo. |

## Frequently Asked Questions

**P: Czy Aspose.CAD jest kompatybilny z różnymi formatami plików CAD?**  
O: Tak, Aspose.CAD obsługuje DWG, DXF, DGN i wiele innych formatów.

**P: Czy mogę używać Aspose.CAD w projektach komercyjnych?**  
O: Oczywiście. Kup licencję [tutaj](https://purchase.aspose.com/buy) do użytku produkcyjnego.

**P: Jak uzyskać tymczasową licencję do testów?**  
O: Tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**P: Gdzie mogę znaleźć wsparcie społeczności?**  
O: Dołącz do forum społeczności Aspose.CAD pod adresem [forum](https://forum.aspose.com/c/cad/19).

**P: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Java?**  
O: Tak, pobierz darmową wersję próbną [tutaj](https://releases.aspose.com/).

## Conclusion

W tym przewodniku pokazaliśmy **how to export cad** pliki z Java oraz **convert DWG to BMP** przy użyciu Aspose.CAD. Postępując zgodnie z pięcioma powyższymi krokami, możesz zintegrować konwersję CAD‑do‑obrazu w dowolnej aplikacji Java, niezależnie od tego, czy jest to narzędzie desktopowe, usługa webowa, czy potok przetwarzania wsadowego. Odkryj inne formaty wyjściowe (PNG, JPEG, PDF), zamieniając klasę opcji, i skorzystaj z bogatego zestawu funkcji Aspose.CAD, aby spełnić wszystkie potrzeby manipulacji CAD.

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}