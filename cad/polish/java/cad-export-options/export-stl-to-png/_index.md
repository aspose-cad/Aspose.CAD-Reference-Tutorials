---
title: Eksportuj STL do PNG za pomocą Aspose.CAD dla Java
linktitle: Eksportuj STL do PNG
second_title: Aspose.CAD API Java
description: Poznaj bezproblemowy proces eksportowania plików STL do formatu PNG w Javie za pomocą Aspose.CAD. Uprość przepływ pracy i bez wysiłku ulepszaj swoje projekty Java.
type: docs
weight: 20
url: /pl/java/cad-export-options/export-stl-to-png/
---
## Wstęp

Czy chcesz wyeksportować pliki STL do formatu PNG przy użyciu języka Java? Aspose.CAD dla Java to rozwiązanie, którego potrzebujesz! W tym samouczku przeprowadzimy Cię przez ten proces krok po kroku. Jako biegły autor tekstów SEO zadbam o to, aby treść była nie tylko informacyjna, ale także zoptymalizowana pod kątem wyszukiwarek.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Zestaw Java Development Kit (JDK) zainstalowany na komputerze.
-  Pobrano bibliotekę Aspose.CAD dla Java. Możesz to dostać[Tutaj](https://releases.aspose.com/cad/java/).
-  Ważna licencja lub licencja tymczasowa od[Tutaj](https://purchase.aspose.com/temporary-license/).

## Importuj przestrzenie nazw

W projekcie Java zaimportuj niezbędne przestrzenie nazw:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Podzielmy teraz przykład na wiele kroków.

## Krok 1: Skonfiguruj swój projekt

Utwórz nowy projekt Java i dodaj bibliotekę Aspose.CAD for Java do zależności swojego projektu.

## Krok 2: Określ swój plik STL

Zdefiniuj ścieżkę do pliku STL. Na przykład:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Krok 3: Załaduj plik STL

 Załaduj plik STL za pomocą`Image.load` metoda:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Krok 4: Skonfiguruj opcje rasteryzacji

Skonfiguruj opcje rasteryzacji dla wektoryzacji:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Krok 5: Skonfiguruj opcje PNG

Określ opcje eksportu PNG:

```java
PngOptions pngOptions = new PngOptions();
// Odkomentuj poniższą linię, jeśli chcesz ustawić opcje rasteryzacji wektorów
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Krok 6: Zapisz jako PNG

Zapisz obraz CAD jako plik PNG:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Gratulacje! Pomyślnie wyeksportowałeś plik STL do PNG przy użyciu Aspose.CAD dla Java.

## Wniosek

W tym samouczku omówiliśmy, jak wykorzystać Aspose.CAD dla Java do bezproblemowego eksportowania plików STL do formatu PNG. Ta potężna biblioteka upraszcza złożone zadania, co czyni ją cennym zasobem dla projektów Java.

## Często zadawane pytania

### P1: Czy Aspose.CAD dla Java jest kompatybilny ze wszystkimi wersjami plików STL?

O1: Aspose.CAD dla Java obsługuje różne wersje plików STL, zapewniając kompatybilność z większością popularnych formatów.

### P2: Czy mogę używać Aspose.CAD dla Java w projekcie komercyjnym?

 A2: Tak, możesz. Wystarczy uzyskać ważną licencję od[Tutaj](https://purchase.aspose.com/buy).

### P3: Czy potrzebuję tymczasowej licencji na bezpłatny okres próbny?

 Odpowiedź 3: Nie, do bezpłatnego okresu próbnego nie jest wymagana licencja tymczasowa. Możesz zacząć od razu, korzystając z wersji próbnej[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć dodatkowe wsparcie lub zadać pytania?

 A4: Odwiedź forum Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia lub zapytań.

### P5: Czy dostępna jest obszerna dokumentacja?

 Odpowiedź 5: Tak, można znaleźć dokumentację[Tutaj](https://reference.aspose.com/cad/java/).