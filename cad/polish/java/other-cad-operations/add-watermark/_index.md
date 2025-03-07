---
title: Dodaj znaki wodne do rysunków CAD - samouczek Aspose.CAD dla Java
linktitle: Dodaj znak wodny
second_title: Aspose.CAD API Java
description: Ulepsz swoje rysunki CAD za pomocą spersonalizowanych znaków wodnych za pomocą Aspose.CAD dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
weight: 12
url: /pl/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodaj znaki wodne do rysunków CAD - samouczek Aspose.CAD dla Java

## Wstęp

Witamy w tym obszernym przewodniku na temat dodawania znaków wodnych do rysunków CAD przy użyciu Aspose.CAD dla Java. W tym samouczku dowiesz się, jak efektywnie integrować znaki wodne, wzbogacając dokumenty CAD o spersonalizowane komunikaty lub branding. Aspose.CAD dla Java zapewnia potężny zestaw funkcji, dzięki którym proces dodawania znaku wodnego jest prosty.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.CAD dla Java: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD w swoim środowisku Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/java/).
- Zestaw Java Development Kit (JDK): Upewnij się, że w systemie zainstalowana jest najnowsza wersja pakietu JDK.

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety Aspose.CAD do swojego projektu Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Dodaj nowy WTEKST

```java
//dodaj nowy WTEKST
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Krok 2: Dodaj prostą jednostkę, taką jak tekst

Możesz także dodać prostszy element, taki jak tekst:

```java
// lub dodaj prostszy element, taki jak Tekst
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Krok 3: Eksportuj do pliku PDF

Eksportuj rysunek CAD z dodanym znakiem wodnym do pliku PDF:

```java
// eksport do pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Wniosek

Gratulacje! Pomyślnie dodałeś znaki wodne do swoich rysunków CAD przy użyciu Aspose.CAD dla Java. Ten prosty, ale skuteczny proces pozwala personalizować projekty lub chronić je za pomocą brandingu.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

O1: Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWT i DWF.

### P2: Czy mogę dostosować wygląd tekstu znaku wodnego?

Odpowiedź 2: Tak, masz pełną kontrolę nad wyglądem znaku wodnego, w tym nad rozmiarem, kolorem i położeniem tekstu.

### P3: Czy dostępna jest wersja próbna Aspose.CAD dla Java?

 Odpowiedź 3: Tak, możesz pobrać wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.CAD?

 A4: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) za wsparcie społeczności.

### P5: Gdzie mogę znaleźć pełną dokumentację Aspose.CAD dla Java?

 Odpowiedź 5: Patrz[dokumentacja](https://reference.aspose.com/cad/java/) aby uzyskać szczegółowe informacje.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
