---
title: Dodawanie znaków wodnych do rysunków CAD - Przewodnik Aspose.CAD
linktitle: Dodawanie znaków wodnych do rysunków CAD
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Ulepsz swoje rysunki CAD za pomocą profesjonalnych znaków wodnych, korzystając z Aspose.CAD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać spersonalizowane i wciągające projekty.
weight: 11
url: /pl/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodawanie znaków wodnych do rysunków CAD - Przewodnik Aspose.CAD

## Wstęp

Czy chcesz ulepszyć swoje rysunki CAD, dodając profesjonalne znaki wodne? Aspose.CAD dla .NET zapewnia solidne rozwiązanie do płynnej integracji znaków wodnych z plikami CAD. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces dodawania znaków wodnych za pomocą Aspose.CAD, upewniając się, że Twoje rysunki nie tylko przekażą najważniejsze informacje, ale także będą nosić Twój unikalny znak.

## Warunki wstępne

Zanim zagłębisz się w samouczek, upewnij się, że posiadasz następujące informacje:
-  Aspose.CAD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.CAD. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).
- Twój katalog dokumentów: skonfiguruj katalog do przechowywania rysunków CAD.
Teraz zacznijmy dodawać znaki wodne do rysunków CAD!

## Importuj przestrzenie nazw

Rozpocznij od zaimportowania niezbędnych przestrzeni nazw do projektu .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Załaduj rysunek CAD

```csharp
// Ścieżka do katalogu dokumentów.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Krok 2: Dodaj znak wodny jako WTEKST

```csharp
// Dodaj nowy WTEKST
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Krok 3: Lub dodaj znak wodny jako tekst

```csharp
// Alternatywnie dodaj prostszą jednostkę, taką jak Tekst
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Krok 4: Eksportuj do pliku PDF

```csharp
// Eksportuj rysunek CAD ze znakiem wodnym do pliku PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Powtórz te kroki dla różnych rysunków, a w mgnieniu oka otrzymasz profesjonalnie wyglądające pliki CAD ze znakami wodnymi!

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się dodawać znaki wodne do rysunków CAD przy użyciu Aspose.CAD dla .NET. Ten prosty, ale skuteczny proces pozwala na personalizację projektów przy jednoczesnym zachowaniu integralności rysunków technicznych.

## Często zadawane pytania

### P1: Czy mogę dostosować wygląd znaku wodnego?

Odpowiedź 1: Tak, możesz dostosować tekst, czcionkę, rozmiar i położenie znaku wodnego zgodnie ze swoimi preferencjami.

### P2: Czy Aspose.CAD jest kompatybilny z różnymi formatami plików CAD?

O2: Aspose.CAD obsługuje różne formaty plików CAD, w tym DWG i DXF, zapewniając szeroką kompatybilność.

### P3: Czy mogę dodać wiele znaków wodnych do jednego rysunku CAD?

A3: Absolutnie! Możesz dodać tyle znaków wodnych, ile potrzeba, zapewniając elastyczność w różnych przypadkach użycia.

### P4: Czy Aspose.CAD oferuje bezpłatną wersję próbną?

Odpowiedź 4: Tak, możesz poznać funkcje Aspose.CAD w ramach bezpłatnej wersji próbnej. Zdobyć[Tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę znaleźć wsparcie dla Aspose.CAD?

 O5: W przypadku jakichkolwiek pytań lub pomocy odwiedź stronę[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
