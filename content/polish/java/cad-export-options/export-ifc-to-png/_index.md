---
title: Eksportuj IFC do PNG za pomocą Aspose.CAD dla Java
linktitle: Eksportuj IFC do PNG
second_title: Aspose.CAD API Java
description: Konwertuj IFC na PNG bez wysiłku dzięki Aspose.CAD dla Java. Postępuj zgodnie z naszym samouczkiem krok po kroku.
type: docs
weight: 18
url: /pl/java/cad-export-options/export-ifc-to-png/
---
## Wstęp

Witamy w tym samouczku krok po kroku dotyczącym eksportowania IFC (Industry Foundation Classes) do formatu PNG przy użyciu Aspose.CAD dla Java. Aspose.CAD to potężna biblioteka Java, która zapewnia szerokie możliwości pracy z plikami CAD, w tym w formacie IFC. W tym samouczku przeprowadzimy Cię przez proces konwersji pliku IFC na obraz PNG, podając szczegółowe wyjaśnienia na każdym etapie.

## Warunki wstępne

Zanim zaczniemy, upewnij się, że spełnione są następujące wymagania wstępne:

-  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Java z[link do pobrania](https://releases.aspose.com/cad/java/).

- Katalog dokumentów: Przygotuj katalog w swoim systemie, w którym znajduje się plik IFC.

## Importuj przestrzenie nazw

W projekcie Java zaimportuj niezbędne przestrzenie nazw, jak pokazano poniżej:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Krok 1: Załaduj plik IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Ten krok obejmuje załadowanie pliku IFC przy użyciu Aspose.CAD.

## Krok 2: Ustaw opcje wektorowe

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Skonfiguruj opcje wektorów dla rasteryzacji, określając szerokość i wysokość strony.

## Krok 3: Ustaw opcje PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Ustaw opcje PNG, w tym opcje rasteryzacji wektorowej.

## Krok 4: Zapisz jako PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Zapisz przetworzony obraz w formacie PNG.

## Wniosek

Gratulacje! Pomyślnie przekonwertowałeś plik IFC na PNG przy użyciu Aspose.CAD dla Java. Ten samouczek zawiera kompleksowy przewodnik, dzięki któremu możesz bezproblemowo zintegrować tę funkcjonalność ze swoimi projektami.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików IFC?

 O1: Aspose.CAD obsługuje różne wersje plików IFC. Patrz[dokumentacja](https://reference.aspose.com/cad/java/) aby poznać szczegóły dotyczące kompatybilności.

### P2: Czy mogę bardziej dostosować opcje rasteryzacji?

 A2: Absolutnie! Poznaj[dokumentacja](https://reference.aspose.com/cad/java/) dla zaawansowanych opcji dostosowywania.

### P3: Czy dostępna jest wersja próbna?

Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?

 A4: Uzyskaj tymczasową licencję od[ten link](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę szukać pomocy lub omówić problemy?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności.
