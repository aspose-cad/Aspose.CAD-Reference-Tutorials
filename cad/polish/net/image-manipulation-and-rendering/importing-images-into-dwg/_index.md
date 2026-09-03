---
date: 2026-08-17
description: Dowiedz się, jak dodać obraz do plików dwg przy użyciu C# i Aspose.CAD
  dla .NET. Ten przewodnik przeprowadzi Cię przez importowanie obrazów, ustawianie
  punktów wstawiania oraz eksport do PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importowanie obrazów do plików DWG przy użyciu C#
og_description: Dowiedz się, jak dodać obraz do plików dwg przy użyciu C#. Ten samouczek
  obejmuje importowanie obrazów, ustawianie punktów wstawiania oraz konwersję dwg
  do PDF przy użyciu Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Jak dodać obraz do plików dwg przy użyciu C# i Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Jak dodać obraz do plików dwg przy użyciu C# i Aspose.CAD
url: /pl/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać obraz do plików DWG przy użyciu C# i Aspose.CAD

## Wprowadzenie

Dodanie obrazu do pliku DWG jest rutynowym wymaganiem, gdy trzeba wzbogacić rysunki CAD o logotypy, zdjęcia lub grafikę rastrową. W tym samouczku nauczysz się, jak **dodać obraz do dwg** programowo przy użyciu C# i Aspose.CAD dla .NET, a następnie opcjonalnie przekonwertować wynik na PDF. Kroki są podzielone tak, abyś mógł kopiować‑wklejać każdą sekcję do własnego projektu.

## Szybkie odpowiedzi
- **Która biblioteka obsługuje to zadanie?** Aspose.CAD for .NET.
- **Czy mogę osadzać pliki PNG?** Tak – obsługiwane są PNG, JPEG, BMP i inne formaty rastrowe.
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.
- **Czy obsługiwany jest eksport do PDF?** Absolutnie – możesz przekonwertować zaktualizowany DWG do PDF w jednej linii.
- **Jakie wersje .NET są kompatybilne?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Czym jest plik DWG?

Plik DWG jest natywnym formatem binarnym dla rysunków Autodesk AutoCAD, przechowującym geometrię wektorową, warstwy i metadane. Jest szeroko stosowany w architekturze, inżynierii i budownictwie, a Aspose.CAD może odczytywać i zapisywać ten format bez konieczności instalacji AutoCAD.

## Dlaczego dodać obraz do dwg przy użyciu Aspose.CAD?

Aspose.CAD obsługuje **ponad 50 formatów wejściowych i wyjściowych**, może przetwarzać pliki większe niż 500 MB bez ładowania całego dokumentu do pamięci oraz zapewnia deterministyczne API działające w środowiskach serwerowych bez interfejsu graficznego. Dzięki temu przetwarzanie wsadowe rysunków DWG jest szybkie i niezawodne.

## Wymagania wstępne
- Podstawowa znajomość programowania w C#.
- Aspose.CAD for .NET zainstalowany. Możesz go pobrać ze [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/). Możesz także przeglądać inne produkty Aspose na [Aspose releases page](https://releases.aspose.com/).
- Środowisko programistyczne, takie jak Visual Studio 2022 lub nowsze.

## Jak dodać obraz do dwg przy użyciu Aspose.CAD?

Załaduj docelowy plik DWG, utwórz obiekt obrazu rastrowego opisujący grafikę, którą chcesz osadzić, ustaw punkt wstawienia i wektory skalowania, a następnie dołącz obraz do rysunku. Na koniec zapisz zmodyfikowany DWG lub wyeksportuj go bezpośrednio do PDF. Cały przepływ wymaga tylko kilku wywołań API i działa w mniej niż sekundę dla typowych rysunków dwustronicowych.

### Importuj przestrzenie nazw
Dołącz przestrzenie nazw, które udostępniają klasy CAD, których będziesz potrzebować.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Krok 1: skonfiguruj katalog dokumentu
Przygotuj folder zawierający źródłowy plik DWG oraz obraz, który chcesz osadzić.

```csharp
string MyDir = "Your Document Directory";
```

### Krok 2: załaduj plik dwg
`Klasa CadImage` reprezentuje rysunek DWG i zapewnia dostęp do jego encji, warstw i metadanych.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Krok 3: zdefiniuj właściwości obrazu
Utwórz obiekt `Image`, który wskazuje na plik rastrowy (np. PNG) i określ jego format.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Krok 4: ustaw punkt wstawienia dwg i wektory
Określ, gdzie obraz ma się pojawić w rysunku i jak ma być skalowany. Punkt wstawienia jest definiowany przez współrzędną 2‑D, a wektory kontrolują szerokość i wysokość.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Krok 5: utwórz i skonfiguruj obraz rastrowy
Zainicjuj obiekt `RasterImage`, przypisz dane obrazu i ustaw dodatkowe opcje renderowania.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Krok 6: dodaj obraz do pliku dwg
Wstaw skonfigurowany obraz rastrowy do kolekcji encji DWG, aby stał się częścią rysunku.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Krok 7: zapisz jako pdf (eksport dwg do pdf)
Po osadzeniu obrazu możesz **convert dwg to pdf** lub **save dwg as pdf** jednym wywołaniem. Jest to przydatne do udostępniania rysunku interesariuszom, którzy nie mają oprogramowania CAD.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Jak przekonwertować dwg do pdf po osadzeniu obrazu?

Wywołaj metodę `Save` na instancji `CadImage`, przekazując `SaveFormat.Pdf` oraz opcjonalnie obiekt `PdfOptions`, aby kontrolować rozmiar strony, rasteryzację i metadane. Aspose.CAD zachowuje osadzony obraz rastrowy, warstwy i grubości linii, tworząc wierną reprezentację PDF, którą można otworzyć w dowolnym przeglądarce. Konwersja odbywa się w jednej linii kodu.

## Typowe problemy i rozwiązania
- **Obraz pojawia się w niewłaściwym miejscu** – sprawdź ponownie współrzędne punktu wstawienia i wektory kierunkowe; są one względem początku rysunku.
- **Duże obrazy powodują skoki pamięci** – użyj opcji `Resize` na obrazie rastrowym przed wstawieniem lub pracuj z kopią o niższej rozdzielczości.
- **Eksport PDF traci jakość wektorów** – upewnij się, że zapisujesz z `PdfOptions`, które zachowują dane wektorowe; obrazy rastrowe są zawsze osadzane w takiej formie.

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.CAD dla .NET w innych językach programowania?**  
A: Biblioteka rdzeniowa jest specyficzna dla .NET, ale Aspose oferuje równoważne API dla Javy, Pythona i innych platform.

**Q: Czy dostępna jest darmowa wersja próbna Aspose.CAD?**  
A: Tak, możesz wypróbować darmową wersję na [Aspose free trial page](https://releases.aspose.com/).

**Q: Gdzie znajdę szczegółową dokumentację Aspose.CAD?**  
A: Dokumentacja jest dostępna w [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Jak uzyskać tymczasową licencję dla Aspose.CAD?**  
A: Odwiedź [temporary license page](https://purchase.aspose.com/temporary-license/), aby uzyskać tymczasową licencję.

**Q: Czy istnieją fora społecznościowe wsparcia Aspose.CAD?**  
A: Tak, możesz szukać pomocy i dyskutować ze społecznością w [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Ostatnia aktualizacja:** 2026-08-17  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Eksportowanie DWG do PDF lub obrazów rastrowych - przewodnik Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Eksportowanie DWG do formatu DXF w C# - samouczek Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Eksportowanie konkretnych układów do PDF - przewodnik Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}