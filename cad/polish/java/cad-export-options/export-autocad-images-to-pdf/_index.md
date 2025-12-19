---
date: 2025-12-19
description: Dowiedz się, jak eksportować plik PDF z AutoCAD przy użyciu Aspose.CAD
  dla Javy. Ten przewodnik krok po kroku pokazuje, jak konwertować DWG na PDF, zapisywać
  CAD jako PDF oraz obsługiwać licencjonowanie.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Eksport AutoCAD PDF - Eksportowanie obrazów AutoCAD do PDF przy użyciu Aspose.CAD
  dla Javy – samouczek
url: /pl/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport PDF z AutoCAD - Eksport obrazów AutoCAD do PDF przy użyciu Aspose.CAD for Java

## Introduction

Czy chcesz płynnie **eksportować PDF z AutoCAD** przy użyciu Javy? Nie szukaj dalej! W tym samouczku przeprowadzimy Cię przez konwersję obrazów AutoCAD do PDF przy użyciu Aspose.CAD for Java, potężnej biblioteki, która sprawia, że proces **konwersji DWG do PDF** jest prosty. Po zakończeniu zrozumiesz, jak **zapisać CAD jako PDF**, zastosować własne ustawienia rasteryzacji oraz pracować z licencją Aspose.CAD w środowisku produkcyjnym.

## Quick Answers
- **Czy mogę konwertować DWG do PDF przy użyciu Javy?** Tak, Aspose.CAD for Java obsługuje DWG, DXF i wiele innych formatów.  
- **Czy potrzebna jest licencja?** Wymagana jest **licencja Aspose CAD** do nieograniczonego użycia; tymczasowa licencja jest dostępna do oceny.  
- **Jaką wersję Javy obsługuje?** Java 8+ (biblioteka jest kompatybilna ze wszystkimi nowoczesnymi JDK).  
- **Czy mogę dostosować rozmiar strony PDF?** Oczywiście – zmień `pageWidth` i `pageHeight` w opcjach rasteryzacji.  
- **Czy rasteryzacja 3‑D jest możliwa?** Tak, włącz `TypeOfEntities.Entities3D` dla pełnego renderowania 3‑D.

## What is **export autocad pdf**?
Eksport PDF z AutoCAD oznacza konwersję wektorowych rysunków CAD (DWG, DXF, DWF itp.) do przenośnego dokumentu PDF przy zachowaniu warstw, grubości linii oraz opcjonalnie geometrii 3‑D. Jest to przydatne do udostępniania projektów klientom, archiwizacji lub drukowania bez konieczności posiadania oprogramowania CAD.

## Why use Aspose.CAD for Java to **export autocad pdf**?
- **Pełne wsparcie formatów** – działa z DWG, DXF, DWF i wieloma innymi.  
- **Brak zewnętrznych zależności** – czysta biblioteka Java, bez natywnych plików DLL.  
- **Wysokiej jakości rasteryzacja** – kontrola DPI, rozmiaru strony i układu.  
- **Elastyczność licencji** – rozpocznij od darmowej wersji próbnej, a następnie przejdź na stałą **licencję Aspose CAD**.  

## Prerequisites

- **Środowisko programistyczne Java** – zainstalowany JDK 8 lub nowszy.  
- **Biblioteka Aspose.CAD for Java** – pobierz z [linku do pobrania](https://releases.aspose.com/cad/java/).  
- **Katalog dokumentów** – folder na Twoim komputerze, w którym będą przechowywane pliki CAD źródłowe oraz wygenerowane pliki PDF.

## Import Namespaces

W swoim projekcie Java zaimportuj niezbędne klasy do pracy z Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Now let’s walk through the code step‑by‑step.

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory Path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Wskazówka:** Zastąp `"Your Document Directory"` pełną ścieżką do folderu, który utworzyłeś w sekcji wymagań.

### Step 2: Load the CAD Image

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Dlaczego to ważne:** Załadowanie pliku CAD do obiektu `Image` daje pełny dostęp do silnika rasteryzacji Aspose.CAD.

### Step 3: Set Rasterization Options

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Dostosuj `pageWidth` i `pageHeight`, aby zmienić rozmiar wyjściowego PDF.  
- Odkomentuj linię `setTypeOfEntities`, jeśli potrzebujesz **java convert cad pdf** dla obiektów 3‑D.  
- Wywołanie `setLayouts` wybiera, który układ (Model, Layout1 itp.) ma być renderowany.

### Step 4: Configure PDF Options

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Łączy ustawienia rasteryzacji z wyjściem PDF, zapewniając prawidłową konwersję danych wektorowych.

### Step 5: Save the PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Wynikowy plik, `Export3DImagestoPDF_out_.pdf`, jest **save cad as pdf** reprezentacją Twojego pierwotnego rysunku AutoCAD.

## Common Issues & Solutions

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| Pusty plik PDF | Opcje rasteryzacji nie ustawione lub niezgodność układu | Sprawdź, czy `setLayouts` odpowiada nazwie układu w pliku CAD. |
| Obraz o niskiej rozdzielczości | `pageWidth`/`pageHeight` za małe | Zwiększ wymiary lub ustaw wyższe DPI za pomocą `rasterizationOptions.setResolution(...)`. |
| Wyjątek licencyjny | Nie zastosowano ważnej licencji | Zastosuj **licencję Aspose CAD** lub użyj tymczasowej licencji do testów. |

## Frequently Asked Questions

### Q1: Czy mogę używać Aspose.CAD for Java z innymi formatami plików CAD?
A1: Tak, Aspose.CAD obsługuje szeroką gamę formatów, w tym DWG, DWF, DGN i inne, dając Ci elastyczność w projektach.

### Q2: Jak mogę uzyskać tymczasową licencję dla Aspose.CAD for Java?
A2: Odwiedź [tutaj](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję do oceny.

### Q3: Czy istnieją opcje układów dla rasteryzacji?
A3: Tak, możesz dostosować układy (np. `"Model"`, `"Layout1"`) za pomocą metody `setLayouts`, aby kontrolować, który widok zostanie wyrenderowany.

### Q4: Czy mogę dostosować rozmiar wyjściowego pliku PDF?
A4: Oczywiście! Dostosuj parametry `pageWidth` i `pageHeight` w opcjach rasteryzacji, aby uzyskać pożądane wymiary.

### Q5: Gdzie mogę uzyskać pomoc lub dyskutować o problemach związanych z Aspose.CAD for Java?
A5: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać dedykowane wsparcie i dyskusje społeczności.

---

**Last Updated:** 2025-12-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}