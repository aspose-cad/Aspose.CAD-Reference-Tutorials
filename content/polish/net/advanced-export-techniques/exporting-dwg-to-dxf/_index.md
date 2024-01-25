---
title: Eksportowanie DWG do formatu DXF w C# - poradnik Aspose.CAD
linktitle: Eksportowanie DWG do formatu DXF w C#
second_title: Aspose.CAD .NET - Format plików CAD i BIM
description: Odblokuj manipulację plikami CAD w C# za pomocą Aspose.CAD. Dowiedz się, jak bez wysiłku eksportować plik DWG do formatu DXF. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową integrację.
type: docs
weight: 10
url: /pl/net/advanced-export-techniques/exporting-dwg-to-dxf/
---
## Wstęp

Jeśli jesteś programistą .NET i szukasz potężnego rozwiązania do manipulowania plikami CAD, Aspose.CAD będzie Twoim ulubionym narzędziem. W tym samouczku krok po kroku przeprowadzimy Cię przez proces eksportowania pliku DWG do formatu DXF przy użyciu C# z Aspose.CAD.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

1.  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD z[ten link](https://releases.aspose.com/cad/net/).

2. Środowisko programistyczne: Skonfiguruj środowisko programistyczne języka C#, takie jak Visual Studio.

3. Przykładowy plik DWG: Przygotuj przykładowy plik DWG, który chcesz wyeksportować. W tym samouczku użyjemy pliku o nazwie „Line.dwg” w katalogu „Twój katalog dokumentów”.

## Importuj przestrzenie nazw

W swoim projekcie C# uwzględnij przestrzenie nazw niezbędne do pracy z Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Załaduj plik DWG

Rozpocznij od załadowania pliku DWG do aplikacji C#. Oto fragment kodu umożliwiający osiągnięcie tego celu:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //Twój kod dalszych kroków będzie tutaj
}
```

## Krok 2: Zapisz jako DXF

Następnym krokiem po załadowaniu pliku DWG jest zapisanie go jako pliku DXF. Dodaj następujący kod w poprzednim bloku using:

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## Wniosek

Gratulacje! Pomyślnie wyeksportowałeś plik DWG do formatu DXF przy użyciu Aspose.CAD w C#. Ten prosty, ale potężny proces otwiera świat możliwości manipulacji plikami CAD w Twoich aplikacjach.

## Często zadawane pytania

### P1: Czy Aspose.CAD jest kompatybilny z najnowszymi formatami plików CAD?

Odpowiedź 1: Tak, Aspose.CAD jest regularnie aktualizowany, aby zapewnić kompatybilność z najnowszymi formatami plików CAD.

### P2: Czy mogę używać Aspose.CAD w moich projektach komercyjnych?

 A2: Absolutnie! Aspose.CAD zawiera opcje licencjonowania zarówno do użytku osobistego, jak i komercyjnego. Odwiedzać[ten link](https://purchase.aspose.com/buy) dla szczegółów.

### P3: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 3: Tak, możesz eksplorować Aspose.CAD w ramach bezpłatnej wersji próbnej. Odwiedzać[ten link](https://releases.aspose.com/) rozpocząć.

### P4: Gdzie mogę znaleźć szczegółową dokumentację dla Aspose.CAD?

 A4: Zapoznaj się z dokumentacją pod adresem[ten link](https://reference.aspose.com/cad/net/) w celu uzyskania kompleksowych wskazówek.

### P5: Potrzebujesz pomocy lub masz konkretne pytania?

 A5: Odwiedź forum społeczności Aspose.CAD[Tutaj](https://forum.aspose.com/c/cad/19)za pomoc ekspertów i wsparcie społeczne.