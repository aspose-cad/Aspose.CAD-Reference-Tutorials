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

# Eksport PDF z AutoCAD - Eksport obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Java

## Wstęp

Czy chcesz płynnie **eksportować PDF z AutoCAD** przy użyciu Javy? Nie szukaj dalej! W tym samouczku przeprowadziliśmy Cię przez konwersję obrazów AutoCAD do PDF przy użyciu Aspose.CAD dla Java, udostępniaj bibliotekę, która sprawia, że ​​proces **konwersji DWG do PDF** jest prosty. Po ujawnieniu, jak **zapisz CAD jako PDF**, własne ustawienia rasteryzacji oraz wykonaj z licencją Aspose.CAD w środowisku produkcyjnym.

## Szybkie odpowiedzi
- **Czy mogę konwertować DWG do PDF przy użyciu Javy?** Tak, Aspose.CAD dla Java obsługuje DWG, DXF i wiele innych formatów.
- **Czy oprogramowanie jest licencjatem?** Wymagana jest **licencja Aspose CAD** do niezbędnego użycia; tymczasowa licencja jest dostępna do oceny.
- **Jaka wersja Javy jest obsługiwana?** Java8+ (biblioteka jest kompatybilna ze zgodnością JDK).
- **Czy można dostosować rozmiar strony PDF?** Oczywiście – zmień `pageWidth` i `pageHeight` w opcjich rasteryzacji.
- **Czy rasteryzacja 3‑D jest ograniczona?** Tak, włącz `TypeOfEntities.Entities3D` dla pełnego renderowania 3-D.

## Co to jest **eksport programu AutoCAD pdf**?
Eksport PDF z AutoCAD oznacza konwersję wektorowych wyników CAD (DWG, DXF, DWF itp.) do zauważenia dokumentu PDF przy zachowaniu warstw, grubości linii oraz opcji geometrii 3-D. Jest to udostępnianie użytkownikom, archiwizacji lub konieczności posiadania oprogramowania CAD.

## Po co używać Aspose.CAD dla Java do **eksportowania programu AutoCAD pdf**?
- **Pełne wsparcie formatów** – działa z DWG, DXF, DWF i wieloma innymi.
- **Brak zewnętrznych zależności** – czysta biblioteka Java, bez natywnych plików DLL.
- **Wysokiej jakości rasteryzacja** – kontrola DPI, oddzielne strony i konfiguracja.
- **Elastyczność licencji** – rozpocznij od darmowej wersji próbnej, a następnie przejdź do **licencji Aspose CAD**.

## Warunki wstępne

- **Środowisko programistyczne Java** – gotowe JDK8 lub nowszy.
- **Biblioteka Aspose.CAD dla Java** – pobierz z [link do pobrania](https://releases.aspose.com/cad/java/).
- **Katalog dokumentów** – folder dotyczący komputera, w którym znajdują się pliki źródłowe CAD oraz wygenerowane pliki PDF.

## Importuj przestrzenie nazw

W swoim projekcie Java zaimportuj niezbędne klasy do pracy z Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Teraz omówmy kod krok po kroku.

## Przewodnik krok po kroku

### Krok 1: Ustaw ścieżkę do katalogu zasobów

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Wskazówka:** Zastąp `"Your Document Directory"` pełną ścieżką do folderu, który utworzyłeś w sekcji wymagań.

### Krok 2: Załaduj obraz CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Dlaczego to ważne:** Załadowanie pliku CAD do obiektu `Image` daje pełny dostęp do silnika rasteryzacji Aspose.CAD.

### Krok 3: Ustaw opcje rasteryzacji

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

### Krok 4: Skonfiguruj opcje PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Łączy ustawienia rasteryzacji z wyjściem PDF, zapewniając prawidłową konwersję danych wektorowych.

### Krok 5: Zapisz plik PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Wynikowy plik, `Export3DImagestoPDF_out_.pdf`, jest **save cad as pdf** reprezentacją Twojego pierwotnego rysunku AutoCAD.

## Typowe problemy i rozwiązania

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|-------|-------------------------------|------------|
| Pusty plik PDF | Opcje rasteryzacji nie ustalają lub niezgodność konfiguracji | Sprawdź, czy `setLayouts` odpowiada na nazwę struktury w pliku CAD. |
| Obraz o rozdzielczości | `pageWidth`/`pageHeight` za małe | Zwiększone wymiary lub ustaw wyższy DPI za pomocą `rasterizationOptions.setResolution(...)`. |
| Wyjątek licencyjny | Nie ważnej licencji | Zastosuj **licencję Aspose CAD** lub dodatkową licencję do testów. |

## Często zadawane pytania

### Q1: Czy mogę zainstalować Aspose.CAD dla Java z innymi formatami plików CAD?
A1: Tak, Aspose.CAD obsługuje grę formatów, w tym DWG, DWF, DGN i inne, gdy wystąpią w projektach.

### Q2: Jak mogę uzyskać tymczasową wydajność dla Aspose.CAD dla Java?
A2: Odwiedź [tutaj](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową uwagę do oceny.

### Q3: Czy istnieje możliwość wyłączenia dla rasteryzacji?
A3: Tak, można dostosować układy (np. `"Model"`, `"Layout1") za pomocą metod `setLayouts`, aby kontrolować, który widok zostanie wyrenderowany.

### Q4: Czy można dostosować rozmiar pliku źródłowego PDF?
A4: Oczywiście! Dostosuj parametry `pageWidth` i `pageHeight` w opcjach rasteryzacji, aby uzyskać parametry.

### Q5: Gdzie mogę uzyskać pomoc lub debatować o problemach związanych z Aspose.CAD dla Java?
A5: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby zapewnić odpowiednie wsparcie i kontrolę społeczności.

---

**Ostatnia aktualizacja:** 19.12.2025
**Testowano z:** Aspose.CAD dla Java 24.10
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}