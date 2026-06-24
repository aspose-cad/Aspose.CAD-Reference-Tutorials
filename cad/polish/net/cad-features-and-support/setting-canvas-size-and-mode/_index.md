---
date: 2026-03-29
description: Dowiedz się, jak tworzyć PDF z CAD, ustawiać rozmiar płótna oraz eksportować
  CAD do PDF lub TIFF przy użyciu Aspose.CAD dla .NET w tym przewodniku krok po kroku.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Jak utworzyć PDF z CAD: ustaw rozmiar płótna i tryb w Aspose.CAD dla .NET'
url: /pl/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ustawianie rozmiaru płótna i trybu w Aspose.CAD dla .NET

## Wprowadzenie

Gotowy, aby **tworzyć PDF z plików CAD** kontrolując wymiary wyjściowe? W tym samouczku przeprowadzimy Cię przez ustawianie rozmiaru płótna i trybu, wczytywanie pliku CAD oraz eksportowanie go do PDF lub TIFF przy użyciu Aspose.CAD dla .NET. Niezależnie od tego, czy musisz **konwertować DXF na PDF**, generować rysunki wysokiej rozdzielczości, czy po prostu dostosować obszar rasteryzacji, poniższe kroki zapewnią solidne, gotowe do produkcji rozwiązanie.

## Szybkie odpowiedzi
- **Co oznacza „tworzyć PDF z CAD”?** Konwertowanie rysunku CAD (np. DXF, DWG) na dokument PDF, który zachowuje szczegóły wektorowe i rastrowe.  
- **Która opcja kontroluje rozmiar wyjścia?** `CadRasterizationOptions.PageWidth` i `PageHeight` (rozmiar płótna).  
- **Czy mogę również eksportować do TIFF?** Tak – użyj `TiffOptions` z tymi samymi ustawieniami rasteryzacji.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna; dostępna jest wersja próbna.  
- **Obsługiwane wersje .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co to jest „tworzyć PDF z CAD”?
Tworzenie PDF z CAD oznacza renderowanie rysunku CAD do formatu ukierunkowanego na stronę (PDF), który może być przeglądany, drukowany lub udostępniany bez konieczności posiadania oprogramowania CAD. Aspose.CAD zajmuje się trudnym procesem, pozwalając zdefiniować rozmiar płótna, skalowanie i format wyjściowy.

## Dlaczego ustawiać rozmiar płótna przy tworzeniu PDF z CAD?
Ustawienie rozmiaru płótna daje precyzyjną kontrolę nad rozdzielczością i wymiarami powstałego PDF lub TIFF. Jest to szczególnie przydatne, gdy:
- Przygotowywanie rysunków do druku na określonych rozmiarach papieru.  
- Generowanie miniatur lub obrazów wysokiej rozdzielczości do podglądu w sieci.  
- Zapewnienie spójnego układu w wielu dokumentach.

## Wymagania wstępne

- Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD ze [strony Aspose.CAD](https://releases.aspose.com/cad/net/).
- Środowisko programistyczne: Upewnij się, że masz skonfigurowane środowisko .NET na swoim komputerze.
- Przykładowy plik CAD: W tym samouczku użyjemy przykładowego pliku DXF. Możesz go znaleźć w [dokumentacji Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importowanie przestrzeni nazw

Najpierw zaimportuj przestrzenie nazw wymagane do przetwarzania CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Jak stworzyć PDF z CAD z niestandardowym rozmiarem płótna

### Krok 1: Wczytaj plik CAD

Zaczynamy od **wczytania pliku CAD** (np. DXF) do obiektu `Image`. To jest moment, w którym **wczytujesz plik CAD** do pamięci.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Krok 2: Utwórz CadRasterizationOptions

Utwórz instancję `CadRasterizationOptions` i określ rozmiar płótna. Właściwości `PageWidth` i `PageHeight` pozwalają **ustawić rozmiar płótna** na dokładne wymiary, które potrzebujesz.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Krok 3: Utwórz PdfOptions (Eksport CAD do PDF)

Połącz ustawienia rasteryzacji z obiektem `PdfOptions`. Ta konfiguracja umożliwia **eksport CAD do PDF** z niestandardowym płótnem, które zdefiniowałeś.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 4: Eksportuj do PDF (Konwertuj DXF na PDF)

Teraz zapisz obraz jako PDF. Ten krok **tworzy PDF z CAD** przy użyciu ustawionych opcji.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Krok 5: Utwórz TiffOptions (Eksport CAD do TIFF)

Jeśli potrzebujesz również obrazu rastrowego, skonfiguruj `TiffOptions`. Te same opcje rasteryzacji są ponownie użyte, więc **eksport CAD do TIFF** zachowuje rozmiar płótna.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 6: Eksportuj do TIFF

Na koniec zapisz rysunek jako plik TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Typowe problemy i rozwiązania

- **Płótno jest przycięte** – sprawdź, czy `AutomaticLayoutsScaling` jest ustawione na `true`, a `NoScaling` na `false`, aby rysunek skalował się do rozmiaru płótna.  
- **PDF o niskiej rozdzielczości** – zwiększ `PageWidth`/`PageHeight` lub ustaw `Resolution` w `CadRasterizationOptions`.  
- **Błąd pliku nie znaleziono** – upewnij się, że `MyDir` wskazuje prawidłowy katalog i nazwa pliku DXF jest dokładnie zgodna.

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.CAD z innymi bibliotekami .NET?
O1: Tak, Aspose.CAD bezproblemowo integruje się z innymi bibliotekami .NET, zapewniając rozszerzone możliwości manipulacji CAD.

### P2: Czy dostępna jest darmowa wersja próbna Aspose.CAD?
O2: Tak, możesz wypróbować funkcje Aspose.CAD w wersji próbnej. Odwiedź [tutaj](https://releases.aspose.com/), aby rozpocząć.

### P3: Jak mogę uzyskać wsparcie dla Aspose.CAD?
O3: W celu uzyskania wsparcia i dyskusji, odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P4: Gdzie mogę znaleźć pełną dokumentację Aspose.CAD?
O4: Zapoznaj się z [dokumentacją Aspose.CAD](https://reference.aspose.com/cad/net/), aby uzyskać szczegółowe informacje i przykłady.

### P5: Jak mogę kupić Aspose.CAD dla .NET?
O5: Aby zakupić Aspose.CAD, odwiedź [stronę zakupu](https://purchase.aspose.com/buy).

**Dodatkowe pytania i odpowiedzi**

**P: Czy mogę wyeksportować rysunek CAD wielostronicowy do jednego PDF?**  
O: Tak. Ustaw `PageCount` w `CadRasterizationOptions`, a biblioteka połączy strony w jeden PDF.

**P: Czy rozmiar płótna wpływa na jakość danych wektorowych?**  
O: Dane wektorowe pozostają niezależne od rozdzielczości; rozmiar płótna wpływa jedynie na elementy rastrowe i rozdzielczość obrazu.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}