---
title: Dodawanie tekstu do plików DWG w C# - poradnik Aspose.CAD
linktitle: Dodawanie tekstu do plików DWG w C#
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Dowiedz się, jak dodawać tekst do plików DWG przy użyciu C# i Aspose.CAD. Postępuj zgodnie z tym samouczkiem krok po kroku, aby zapewnić bezproblemową integrację. Zapoznaj się z dokumentacją Aspose.CAD, aby uzyskać kompleksowe wskazówki.
type: docs
weight: 14
url: /pl/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Wstęp

W dynamicznej dziedzinie projektowania wspomaganego komputerowo (CAD) i programowania .NET, Aspose.CAD wyróżnia się jako potężne narzędzie do manipulowania plikami DWG. Dodawanie tekstu do plików DWG jest częstym wymaganiem i w tym samouczku przyjrzymy się, jak to osiągnąć za pomocą C# i Aspose.CAD.

## Warunki wstępne

Zanim zagłębisz się w samouczek, upewnij się, że masz przygotowane następujące elementy:

-  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD z[link do pobrania](https://releases.aspose.com/cad/net/).

-  Katalog dokumentów: skonfiguruj katalog dla swoich dokumentów i zanotuj jego ścieżkę jako`MyDir`.

Podzielmy teraz proces na łatwe do wykonania etapy.

## Importuj przestrzenie nazw

W swoim kodzie C# uwzględnij niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Załaduj plik DWG

 Załaduj plik DWG do pliku`Image` obiekt przy użyciu biblioteki Aspose.CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Twój kod kolejnych kroków znajduje się tutaj
}
```

## Krok 2: Utwórz obiekt CadText

 Utwórz instancję a`CadText` obiekt reprezentujący tekst, który chcesz dodać do pliku DWG.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## Krok 3: Dodaj tekst do pliku DWG

 Dodaj utworzone`CadText` obiekt do pliku DWG przy użyciu Aspose.CAD.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Krok 4: Skonfiguruj opcje PDF

Skonfiguruj opcje PDF w celu zapisania zmodyfikowanego pliku DWG jako pliku PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 5: Zapisz jako plik PDF

Zapisz zmodyfikowany plik DWG jako plik PDF z dodanym tekstem.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Teraz pomyślnie dodałeś tekst do pliku DWG przy użyciu C# i Aspose.CAD. Zachęcamy do zapoznania się z większą liczbą funkcji i funkcjonalności Aspose.CAD dla potrzeb manipulacji CAD.

## Wniosek

tym samouczku omówiliśmy podstawowe kroki dodawania tekstu do plików DWG przy użyciu C# i Aspose.CAD. Ta potężna kombinacja otwiera możliwości dynamicznego i dostosowanego do potrzeb generowania dokumentów CAD.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?

Odpowiedź 1: Aspose.CAD obsługuje szeroką gamę wersji plików DWG, zapewniając kompatybilność z różnymi programami CAD.

### P2: Czy mogę dodać wiele elementów tekstowych do jednego pliku DWG przy użyciu Aspose.CAD?

O2: Tak, możesz dodać wiele elementów tekstowych do pliku DWG, powtarzając proces opisany w samouczku.

### P3: Jak mogę zmienić czcionkę i styl tekstu w Aspose.CAD?

 O3: Aby zmodyfikować czcionkę i styl tekstu, dostosuj właściwości pliku`CadText` obiekt przed dodaniem go do pliku DWG.

### P4: Czy istnieją jakieś uwagi licencyjne dotyczące używania Aspose.CAD w projekcie komercyjnym?

 Odpowiedź 4: Tak, zapewnij zgodność z warunkami licencji Aspose.CAD. Odnosić się do[Zakup Aspose.CAD](https://purchase.aspose.com/buy) dla szczegółów.

### P5: Gdzie mogę szukać pomocy lub omówić zapytania związane z Aspose.CAD?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)aby nawiązać kontakt ze społecznością i uzyskać wsparcie.