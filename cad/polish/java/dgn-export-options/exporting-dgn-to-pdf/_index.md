---
title: Bezproblemowy eksport DGN do AutoCAD PDF za pomocą Aspose.CAD dla Java
linktitle: Eksportowanie DGN w formacie AutoCAD do pliku PDF
second_title: Aspose.CAD API Java
description: Zapoznaj się z przewodnikiem krok po kroku dotyczącym eksportowania plików DGN do formatu AutoCAD w formacie PDF przy użyciu Aspose.CAD dla Java. Bez wysiłku zwiększ możliwości obsługi CAD aplikacji Java.
weight: 12
url: /pl/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bezproblemowy eksport DGN do AutoCAD PDF za pomocą Aspose.CAD dla Java

## Wstęp

Witamy w tym kompleksowym samouczku dotyczącym używania Aspose.CAD dla Java do eksportowania plików DGN w formacie AutoCAD do formatu PDF. Jeśli chcesz zwiększyć możliwości swojej aplikacji Java w zakresie obsługi plików CAD, Aspose.CAD będzie doskonałym wyborem. W tym samouczku przeprowadzimy Cię krok po kroku przez proces eksportowania plików DGN.


## Warunki wstępne
Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
-  Biblioteka Aspose.CAD: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD dla Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/java/).
- Katalog dokumentów: skonfiguruj katalog dokumentów, w którym będą przechowywane pliki wejściowe i wyjściowe.

## Importuj pakiety

W swoim projekcie Java zaimportuj niezbędne pakiety, aby uzyskać dostęp do funkcjonalności Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Podzielmy teraz przykładowy kod na kilka kroków:

## Krok 1: Zdefiniuj ścieżki plików

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Pamiętaj, aby zastąpić „Katalog Twoich dokumentów” rzeczywistą ścieżką, w której znajdują się Twoje pliki.

## Krok 2: Załaduj obraz DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Załaduj plik DGN przy użyciu Aspose.CAD.

## Krok 3: Ustaw opcje eksportu PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Eksportuj określone widoki
options.setVectorRasterizationOptions(vectorOptions);
```

Zdefiniuj opcje eksportu do pliku PDF, w tym wymiary strony i preferencje układu.

## Krok 4: Zapisz plik PDF

```java
objImage.save(outFile, options);
```

Zapisz wyeksportowany plik PDF.

Powtórz te kroki dla wszystkich dodatkowych plików DGN, które chcesz przekonwertować. Gratulacje! Pomyślnie wyeksportowałeś pliki DGN do formatu AutoCAD w formacie PDF przy użyciu Aspose.CAD dla Java.

## Wniosek

tym samouczku zbadaliśmy, jak wykorzystać Aspose.CAD dla Java, aby zwiększyć możliwości obsługi plików CAD w aplikacji. Dzięki łatwym do wykonania krokom i przykładom kodu możesz teraz bezproblemowo eksportować pliki DGN do formatu AutoCAD w formacie PDF.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje szeroką gamę formatów CAD, zapewniając wszechstronność w obsłudze różnych typów plików.

### P2: Czy mogę dostosować ustawienia eksportu PDF?

A2: Absolutnie. Jak pokazano w samouczku, możesz dostosować opcje, takie jak wymiary i układy strony, do swoich wymagań.

### P3: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?

 A3: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności i dyskusje.

### P4: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 4: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P5: Jak mogę uzyskać licencję tymczasową?

 A5: Uzyskaj tymczasową licencję[Tutaj](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
