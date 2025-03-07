---
title: Importowanie obrazów do plików DWG za pomocą C# - Przewodnik Aspose.CAD
linktitle: Importowanie obrazów do plików DWG za pomocą C#
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak importować obrazy do plików DWG przy użyciu C# z Aspose.CAD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
weight: 11
url: /pl/net/image-manipulation-and-rendering/importing-images-into-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Importowanie obrazów do plików DWG za pomocą C# - Przewodnik Aspose.CAD

## Wstęp

W dziedzinie projektowania wspomaganego komputerowo (CAD) włączanie obrazów do plików DWG jest powszechnym i kluczowym zadaniem. Aspose.CAD dla .NET zapewnia potężny zestaw narzędzi usprawniających ten proces, dzięki czemu jest dostępny dla programistów C#. W tym samouczku omówimy krok po kroku, jak importować obrazy do plików DWG.

## Warunki wstępne

Zanim zagłębisz się w przewodnik, upewnij się, że masz następujące informacje:

- Podstawowa znajomość programowania w języku C#.
-  Zainstalowany Aspose.CAD dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/cad/net/).
- Skonfigurowano środowisko programistyczne.

## Importuj przestrzenie nazw

Pamiętaj o uwzględnieniu niezbędnych przestrzeni nazw w projekcie C#:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Skonfiguruj katalog dokumentów

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Załaduj plik DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Krok 3: Zdefiniuj właściwości obrazu

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Krok 4: Ustaw punkt wstawienia i wektory

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Krok 5: Utwórz i skonfiguruj obraz rastrowy

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Krok 6: Dodaj obraz do pliku DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Krok 7: Zapisz jako plik PDF

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

## Wniosek

Integrowanie obrazów z plikami DWG przy użyciu C# i Aspose.CAD dla .NET to płynny proces, umożliwiający programistom łatwe ulepszanie swoich projektów CAD o elementy wizualne.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET z innymi językami programowania?

Odpowiedź 1: Aspose.CAD jest przeznaczony głównie dla .NET, ale Aspose udostępnia biblioteki dla różnych języków programowania.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD dla .NET?

 Odpowiedź 2: Tak, możesz skorzystać z bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć szczegółową dokumentację dla Aspose.CAD?

 A3: Dokumentacja jest dostępna[Tutaj](https://reference.aspose.com/cad/net/).

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.CAD dla .NET?

 A4: Odwiedź[ten link](https://purchase.aspose.com/temporary-license/) aby uzyskać licencję tymczasową.

### P5: Czy istnieją fora społeczności dotyczące wsparcia Aspose.CAD?

 Odpowiedź 5: Tak, możesz szukać wsparcia i nawiązywać kontakt ze społecznością[Tutaj](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
