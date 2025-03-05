---
title: Konwersja Java DGN do JPEG za pomocą samouczka Aspose.CAD
linktitle: Eksportowanie DGN w formacie AutoCAD do formatu obrazu rastrowego
second_title: Aspose.CAD API Java
description: Dowiedz się, jak eksportować pliki DGN do obrazów JPEG w Javie przy użyciu Aspose.CAD. Ten samouczek krok po kroku poprowadzi Cię przez ten proces bez wysiłku.
type: docs
weight: 13
url: /pl/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Wstęp

Witamy w tym kompleksowym samouczku na temat eksportowania plików DGN (projektu) do formatu obrazu rastrowego przy użyciu Aspose.CAD dla Java. Aspose.CAD to potężna biblioteka, która umożliwia programistom Java płynną pracę z plikami CAD. W tym samouczku przeprowadzimy Cię przez proces konwersji plików DGN na obrazy JPEG, dostarczając instrukcje krok po kroku i przykłady kodu.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
1.  Biblioteka Aspose.CAD: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD for Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/java/).
2. Zestaw Java Development Kit (JDK): Upewnij się, że na komputerze jest zainstalowana Java.
3. Zintegrowane środowisko programistyczne (IDE): Użyj środowiska IDE zgodnego z Javą, takiego jak IntelliJ lub Eclipse.

## Importuj pakiety

W swoim projekcie Java zaimportuj niezbędne pakiety dla Aspose.CAD. Dodaj następujące linie do swojego kodu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Krok 1: Załaduj plik DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Krok 2: Utwórz obiekt JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Krok 3: Przypisz opcje rasteryzacji

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Krok 4: Zapisz przekonwertowany obraz

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Powtórz te kroki dla określonych plików DGN, odpowiednio dostosowując ścieżki plików.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się eksportować pliki DGN do formatu obrazu rastrowego przy użyciu Aspose.CAD dla Java. Ten samouczek wyposażył Cię w wiedzę niezbędną do włączenia tej funkcjonalności do aplikacji Java.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD, zapewniając wszechstronne rozwiązanie dla programistów Java.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla Java?

 Odpowiedź 2: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć dokumentację Aspose.CAD dla Java?

 Odpowiedź 3: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/cad/java/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.CAD dla Java?

 Odpowiedź 4: Odwiedź forum pomocy technicznej[Tutaj](https://forum.aspose.com/c/cad/19).

### P5: Gdzie mogę kupić licencję na Aspose.CAD dla Java?

 Odpowiedź 5: Możesz kupić licencję[Tutaj](https://purchase.aspose.com/buy).