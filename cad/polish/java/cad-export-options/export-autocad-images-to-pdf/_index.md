---
date: 2026-02-20
description: Dowiedz się, jak eksportować pliki PDF z AutoCAD przy użyciu Aspose.CAD
  dla Javy. Ten przewodnik krok po kroku pokazuje, jak **konwertować DWG na PDF**,
  **zapisać CAD jako PDF** oraz obsługiwać licencjonowanie.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Konwertuj DWG do PDF – eksportuj obrazy AutoCAD do PDF z Aspose.CAD dla Javy
url: /pl/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport PDF z AutoCAD - Eksport obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Javy

## Introduction

Czy szukasz sposobu na **konwersję DWG do PDF** przy użyciu Javy? Nie szukaj dalej! W tym samouczku przeprowadzimy Cię krok po kroku przez konwersję obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Javy, potężnej biblioteki, która sprawia, że proces **konwersji DWG do PDF** jest prosty. Po zakończeniu zrozumiesz, jak **zapisać CAD jako PDF**, zastosować własne ustawienia rasteryzacji oraz pracować z licencją Aspose.CAD w środowisku produkcyjnym.

## Quick Answers
- **Czy mogę konwertować DWG do PDF przy użyciu Javy?** Tak, Aspose.CAD dla Javy obsługuje DWG, DXF i wiele innych formatów.  
- **Czy potrzebna jest licencja?** Wymagana jest **licencja Aspose CAD** do nieograniczonego użycia; tymczasowa licencja jest dostępna do oceny.  
- **Jaką wersję Javy obsługuje?** Java 8+ (biblioteka jest kompatybilna ze wszystkimi nowoczesnymi JDK).  
- **Czy mogę dostosować rozmiar strony PDF?** Oczywiście – dostosuj `pageWidth` i `pageHeight` w opcjach rasteryzacji.  
- **Czy rasteryzacja 3‑D jest możliwa?** Tak, włącz `TypeOfEntities.Entities3D` aby uzyskać pełne renderowanie 3‑D.

## What is **export autocad pdf**?
Eksportowanie AutoCAD PDF oznacza konwersję wektorowych rysunków CAD (DWG, DXF, DWF itp.) do przenośnego dokumentu PDF przy zachowaniu warstw, grubości linii i opcjonalnie geometrii 3‑D. Jest to przydatne do udostępniania projektów klientom, archiwizacji lub drukowania bez konieczności posiadania oprogramowania CAD.

## Why Convert DWG to PDF with Aspose.CAD for Java?
- **Pełne wsparcie formatów** – działa z DWG, DXF, DWF i wieloma innymi.  
- **Brak zewnętrznych zależności** – czysta biblioteka Java, bez natywnych DLL.  
- **Wysokiej jakości rasteryzacja** – kontrola nad DPI, rozmiarem strony i układem, dzięki czemu możesz **dostosować rozmiar strony PDF** do wymagań projektu.  
- **Elastyczność licencji** – rozpocznij od darmowej wersji próbnej, a następnie przejdź na stałą **licencję Aspose CAD**.  

## Prerequisites

- **Środowisko programistyczne Java** – zainstalowany JDK 8 lub nowszy.  
- **Biblioteka Aspose.CAD dla Javy** – pobierz z [linku do pobrania](https://releases.aspose.com/cad/java/).  
- **Katalog dokumentów** – folder na Twoim komputerze, w którym będą przechowywane pliki CAD źródłowe oraz wygenerowane pliki PDF.

## Import Namespaces

W swoim projekcie Java zaimportuj niezbędne klasy do pracy z Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Teraz przejdźmy krok po kroku przez kod.

## How to convert DWG to PDF with Aspose.CAD for Java

### Step 1: Set the Resource Directory Path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Wskazówka:** Zastąp `"Your Document Directory"` absolutną ścieżką do folderu, który utworzyłeś w sekcji wymagań.

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

- Dostosuj `pageWidth` i `pageHeight`, aby **dostosować rozmiar strony PDF**.  
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

Powstały plik, `Export3DImagestoPDF_out_.pdf`, jest **save cad as pdf** reprezentacją Twojego pierwotnego rysunku AutoCAD.

## Common Issues & Solutions

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|--------------------------|-------------|
| Pusty plik PDF | Opcje rasteryzacji nie ustawione lub niezgodność układu | Sprawdź, czy `setLayouts` odpowiada nazwie układu w Twoim pliku CAD. |
| Obraz o niskiej rozdzielczości | `pageWidth`/`pageHeight` za małe | Zwiększ wymiary lub ustaw wyższą DPI za pomocą `rasterizationOptions.setResolution(...)`. |
| Wyjątek licencyjny | Nie zastosowano ważnej licencji | Zastosuj **licencję Aspose CAD** lub użyj tymczasowej licencji do testów. |

## Frequently Asked Questions

### Q1: Czy mogę używać Aspose.CAD dla Javy z innymi formatami plików CAD?
A1: Tak, Aspose.CAD obsługuje szeroką gamę formatów, w tym DWG, DWF, DGN i inne, dając Ci elastyczność w projektach.

### Q2: Jak mogę uzyskać tymczasową licencję dla Aspose.CAD dla Javy?
A2: Odwiedź [tutaj](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję do oceny.

### Q3: Czy istnieją opcje układów dla rasteryzacji?
A3: Tak, możesz dostosować układy (np. `"Model"`, `"Layout1"`) za pomocą metody `setLayouts`, aby kontrolować, który widok jest renderowany.

### Q4: Czy mogę dostosować rozmiar wyjściowego pliku PDF?
A4: Oczywiście! Dostosuj parametry `pageWidth` i `pageHeight` w opcjach rasteryzacji, aby dopasować je do żądanych wymiarów.

### Q5: Gdzie mogę uzyskać pomoc lub dyskutować o problemach związanych z Aspose.CAD dla Javy?
A5: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać dedykowane wsparcie i dyskusje społeczności.

---

**Ostatnia aktualizacja:** 2026-02-20  
**Testowano z:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}