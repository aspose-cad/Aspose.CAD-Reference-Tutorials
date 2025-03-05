---
title: Eksportuj DGN do DWG za pomocą Aspose.CAD dla Java
linktitle: Eksportuj DGN jako część DWG
second_title: Aspose.CAD API Java
description: Dowiedz się, jak eksportować DGN jako część DWG przy użyciu Aspose.CAD dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby efektywnie manipulować plikami CAD.
type: docs
weight: 10
url: /pl/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Wstęp

W tym samouczku odkryjemy, jak używać Aspose.CAD dla Java do eksportowania pliku DGN (MicroStation Design) jako części pliku DWG (rysunek AutoCAD). Aspose.CAD to potężna biblioteka zapewniająca wszechstronną funkcjonalność do pracy z formatami plików CAD. Ten przewodnik krok po kroku pomoże Ci zrozumieć proces eksportowania DGN jako części DWG przy użyciu Java.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
1. Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla języka Java. Możesz znaleźć drogę do biblioteki[Tutaj](https://releases.aspose.com/cad/java/).
2. Zestaw Java Development Kit (JDK): Upewnij się, że w systemie jest zainstalowana Java.
3. Zintegrowane środowisko programistyczne (IDE): wybierz środowisko Java IDE, takie jak Eclipse lub IntelliJ, aby zapewnić płynniejsze środowisko programistyczne.

## Importuj pakiety

W projekcie Java zaimportuj niezbędne pakiety Aspose.CAD, aby umożliwić manipulowanie plikami CAD. Oto przykład:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Krok 1: Ustaw ścieżki plików

 Zdefiniuj ścieżki plików wejściowych i wyjściowych dla pliku DWG. Zaktualizuj`dataDir`, `fileName` , I`outPath` odpowiednio zmienne.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Krok 2: Utwórz instancję PdfOptions

 Utwórz instancję`PdfOptions` class, ponieważ eksportujemy plik DWG do formatu PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Krok 3: Załaduj plik DWG

 Załaduj istniejący plik DWG jako obraz i przekonwertuj go na format`CadImage` typ.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Krok 4: Iteruj po elementach

Przejrzyj każdy element w pliku DWG i sprawdź, czy jest to definicja obrazu. Jeśli tak, pobierz zewnętrzne odniesienie do obiektu.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Krok 5: Zdefiniuj opcje rasteryzacji

 Zdefiniuj ustawienia dla`CadRasterizationOptions`obiektu, w tym szerokość strony, wysokość, układ i kolor tła.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Krok 6: Ustaw opcje rasteryzacji wektora

Ustaw opcje rasteryzacji wektora dla eksportu.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Krok 7: Eksportuj DWG do formatu PDF

 Na koniec wyeksportuj plik DWG do formatu PDF, wywołując metodę`save` metoda.

```java
cadImage.save(outPath, exportOptions);
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się eksportować plik DGN jako część pliku DWG przy użyciu Aspose.CAD dla Java. Ta potężna biblioteka zapewnia szerokie możliwości pracy z plikami CAD, dzięki czemu zadania manipulacji plikami CAD są wydajne i proste.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.CAD dla Java?

 Odpowiedź 1: Można znaleźć dokumentację[Tutaj](https://reference.aspose.com/cad/java/).

### P2: Jak mogę pobrać bibliotekę Aspose.CAD dla Java?

 O2: Możesz pobrać bibliotekę z[ten link](https://releases.aspose.com/cad/java/).

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla Java?

 A3: Tak, możesz znaleźć bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę uzyskać tymczasową licencję na Aspose.CAD dla Java?

 A4: Uzyskaj tymczasową licencję[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Potrzebujesz pomocy lub masz pytania?

 A5: Odwiedź forum wsparcia społeczności Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19).