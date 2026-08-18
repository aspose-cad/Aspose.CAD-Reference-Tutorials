---
date: 2026-02-23
description: Dowiedz się, jak konwertować DWFX na PDF i zapisywać CAD jako PDF przy
  użyciu Aspose.CAD dla Javy. Szybki przewodnik, jak otwierać pliki DWFX i generować
  PDF‑y.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: Konwertuj DWFX do PDF za pomocą Aspose.CAD dla Javy
url: /pl/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

 We kept them.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWFX do PDF przy użyciu Aspose.CAD dla Javy

## Introduction

W dzisiejszym szybkim świecie projektowania programiści często muszą **konwertować DWFX do PDF**, aby rysunki CAD mogły być udostępniane osobom nietechnicznym. Aspose.CAD dla Javy upraszcza to zadanie, umożliwiając otwarcie pliku DWFX, rasteryzację i **zapis CAD jako PDF** przy użyciu kilku linii kodu. W tym samouczku przeprowadzimy Cię przez cały proces — od konfiguracji środowiska po weryfikację końcowego PDF — abyś mógł pewnie obsługiwać pliki DWFX w aplikacjach Java.

## Quick Answers
- **Jaki jest główny cel tego przewodnika?** Pokazać, jak konwertować DWFX do PDF przy użyciu Aspose.CAD dla Javy.  
- **Która biblioteka jest wymagana?** Aspose.CAD dla Javy (pobierz ze strony oficjalnej Aspose).  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarcza do rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę otwierać pliki DWFX bezpośrednio?** Tak, użyj `Image.load` do otwierania plików DWFX.  
- **Jaki format wyjściowy generuje przykład?** Plik PDF zapisany w określonym katalogu wyjściowym.

## What is “convert DWFX to PDF”?

Konwertowanie DWFX do PDF oznacza pobranie wektorowego rysunku DWFX — powszechnie używanego w produktach Autodesk — i przekształcenie go w przenośny, szeroko wspierany dokument PDF. Umożliwia to łatwe przeglądanie, drukowanie i udostępnianie bez konieczności posiadania oprogramowania CAD po stronie odbiorcy.

## Why use Aspose.CAD for Java to **save CAD as PDF**?

- **Brak zewnętrznych zależności:** Czyste API Java, nie wymaga natywnych silników CAD.  
- **Renderowanie o wysokiej wierności:** Zachowuje grubości linii, kolory i warstwy.  
- **Przyjazne przetwarzanie wsadowe:** Idealne do automatyzacji po stronie serwera lub usług w chmurze.  
- **Wieloplatformowe:** Działa na Windows, Linux i macOS.

## Prerequisites

- **Biblioteka Aspose.CAD dla Javy** – Pobierz ją ze [strony pobierania Aspose.CAD dla Javy](https://releases.aspose.com/cad/java/).  
- **Środowisko programistyczne Java** – JDK 8 lub nowszy, z ulubionym IDE lub narzędziem budującym.  
- **Plik DWFX** – Przykładowy plik DWFX (np. `Tyrannosaurus.dwfx`) do przetestowania konwersji.

## Import Namespaces

First, import the classes we’ll need:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to Convert DWFX to PDF using Aspose.CAD for Java

Poniżej znajduje się szczegółowy podział krok po kroku. Każdy krok zawiera krótkie wyjaśnienie oraz dokładny kod, który należy uruchomić.

### Step 1: Load the DWFX File  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

Metoda `Image.load` odczytuje plik DWFX do pamięci, dając nam obiekt `CadImage` gotowy do rasteryzacji.

### Step 2: Set Rasterization Options  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

Te opcje definiują rozmiar strony wyjściowej, zapewniając, że PDF będzie odpowiadał wymiarom oryginalnego rysunku.

### Step 3: Configure PDF Options  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

Tutaj łączymy ustawienia rasteryzacji z konfiguracją eksportu PDF.

### Step 4: Save as PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Wywołanie `save` zapisuje wyrenderowany obraz do pliku PDF w folderze wyjściowym.

### Step 5: Verify Success  

```java
System.out.println("OpenDwfxFile executed successfully");
```

Prosta wiadomość w konsoli potwierdza, że konwersja zakończyła się bez błędów.

## Common Issues and Solutions

| Problem | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------|----------|
| **Pusty plik PDF** | Szerokość/wysokość rasteryzacji ustawiona na 0 | Upewnij się, że `cadImageDwf.getSize()` zwraca prawidłowe wymiary przed ustawieniem opcji. |
| **Błąd braku pamięci** | Bardzo duży plik DWFX | Zwiększ rozmiar sterty JVM (`-Xmx2g`) lub przetwarzaj plik w mniejszych sekcjach. |
| **Brakujące czcionki** | Czcionka nie jest osadzona w źródłowym pliku DWFX | Zainstaluj wymagane czcionki na serwerze lub użyj `CadRasterizationOptions.setFontName`, aby określić zapasową czcionkę. |

## Frequently Asked Questions

### Q1: Czy mogę używać Aspose.CAD dla Javy z innymi formatami plików CAD?  
A1: Tak, Aspose.CAD dla Javy obsługuje szeroką gamę formatów CAD, oferując wszechstronne rozwiązanie dla programistów.

### Q2: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Javy?  
A2: Tak, możesz przetestować możliwości Aspose.CAD dla Javy w wersji próbnej. Odwiedź [ten link](https://releases.aspose.com/), aby rozpocząć.

### Q3: Jak mogę uzyskać wsparcie dla Aspose.CAD dla Javy?  
A3: Dołącz do społeczności Aspose.CAD na [forum wsparcia](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i współpracować.

### Q4: Czy dostępne są tymczasowe licencje dla Aspose.CAD dla Javy?  
A4: Tak, możesz uzyskać tymczasową licencję dla Aspose.CAD dla Javy. Odwiedź [ten link](https://purchase.aspose.com/temporary-license/), aby uzyskać więcej szczegółów.

### Q5: Gdzie mogę znaleźć dokumentację Aspose.CAD dla Javy?  
A5: Kompleksowa dokumentacja jest dostępna [tutaj](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}