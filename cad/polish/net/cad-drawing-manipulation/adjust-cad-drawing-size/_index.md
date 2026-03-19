---
date: 2026-03-19
description: Dowiedz się, jak zmieniać rozmiar rysunków CAD w .NET przy użyciu Aspose.CAD,
  w tym jak skalować jednostki rysunku CAD i dostosowywać rozmiar układu. Postępuj
  zgodnie z naszym przewodnikiem krok po kroku.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak zmienić rozmiar rysunków CAD przy użyciu Aspose.CAD dla .NET
url: /pl/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zmienić rozmiar rysunków CAD przy użyciu Aspose.CAD dla .NET

## Wprowadzenie

Jeśli potrzebujesz **jak zmienić rozmiar CAD** plików bezpośrednio z aplikacji .NET, trafiłeś we właściwe miejsce. W tym samouczku pokażemy, jak zmienić ustawienia jednostek CAD, skalować wymiary rysunku CAD oraz programowo dostosować rozmiar CAD przy użyciu Aspose.CAD dla .NET. Po zakończeniu przewodnika będziesz mieć solidne, gotowe do produkcji rozwiązanie do zmiany rozmiaru dowolnego obsługiwanego formatu CAD.

## Quick Answers
- **Jakiej biblioteki wymaga?** Aspose.CAD for .NET  
- **Czy mogę zmienić typ jednostki?** Tak – ustaw `UnitType` w `CadRasterizationOptions`  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.CAD do użytku nie‑trial  
- **Do jakiego formatu obrazu eksportuje przykład?** BMP (ale działa każdy obsługiwany format rastrowy)  
- **Ile linii kodu?** Mniej niż 30 linii dla pełnej operacji zmiany rozmiaru  

## What is “how to resize CAD” in practice?
Zmiana rozmiaru rysunku CAD oznacza konwersję danych wektorowych na obraz rastrowy w określonej skali lub jednostce (np. centymetry, cale). Jest to przydatne, gdy trzeba osadzić rysunki w raportach, generować miniatury lub integrować wizualizacje CAD na stronach internetowych.

## Why adjust CAD size with Aspose.CAD?
- **Brak zewnętrznego oprogramowania CAD** – wszystko działa wewnątrz Twojego kodu .NET.  
- **Precyzyjna kontrola** nad jednostkami, układami i opcjami rasteryzacji.  
- **Obsługa wielu formatów** – ten sam kod działa dla DWG, DXF, DWF i innych.  

## Prerequisites

Zanim zaczniemy, upewnij się, że masz:

- Biblioteka Aspose.CAD for .NET: Pobierz i zainstaluj bibliotekę ze [strony pobierania Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).  
- Przykładowy rysunek CAD: Plik taki jak `sample.dwg` umieszczony w katalogu dokumentów Twojego projektu.  

## Import Namespaces

Najpierw zaimportuj przestrzenie nazw, które dają dostęp do klas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the CAD Drawing

Wczytaj plik źródłowy do obiektu `Image`. Ten obiekt reprezentuje rysunek CAD w pamięci i będzie podstawą dla wszystkich dalszych operacji.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Step 2: Create BmpOptions (or any other raster format)

`BmpOptions` informuje Aspose.CAD, jak renderować dane wektorowe przy zapisie jako bitmapa. Możesz zamienić to na `PngOptions`, `JpegOptions` itp., w zależności od docelowego formatu.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Step 3: Set CadRasterizationOptions

`CadRasterizationOptions` zawiera podstawowe ustawienia skalowania, konwersji jednostek i wyboru układu. Powiązanie go z właściwością `VectorRasterizationOptions` w `BmpOptions` zapewnia, że rasteryzator użyje Twoich niestandardowych ustawień.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Step 4: Set UnitType (change CAD unit)

Tutaj zmieniamy jednostkę CAD z domyślnej na centymetry. To miejsce, w którym znajduje się słowo kluczowe **change cad unit**, i bezpośrednio wpływa na ostateczny rozmiar obrazu.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Step 5: Choose Layouts (set CAD layouts)

Jeśli Twój rysunek zawiera wiele układów (np. Model, Sheet1), określ, które chcesz rasteryzować. Wybranie właściwego układu jest kluczowe, gdy **set cad layouts** dla zmienionego rozmiaru wyjścia.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 6: Export to BMP (resize CAD drawing)

Na koniec zapisz rasteryzowany obraz. Plik wyjściowy odzwierciedla nowy rozmiar, jednostkę i układ, które skonfigurowałeś — skutecznie kończąc operację **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Masz teraz plik BMP, który reprezentuje zmieniony rozmiar rysunku CAD, gotowy do dalszego przetwarzania lub wyświetlania.

## Common Issues and Solutions

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| Wyjście jest rozmyte | Niska domyślna rozdzielczość DPI | Ustaw `cadRasterizationOptions.Resolution = 300;` przed zapisem |
| Pojawia się niewłaściwy układ | Błąd w nazwie układu | Sprawdź dokładną nazwę układu używając przeglądarki CAD lub kolekcji `Layouts` |
| Konwersja jednostek jest niepoprawna | Mieszanie jednostek metrycznych i imperialnych | Upewnij się, że `UnitType` odpowiada pożądanemu systemowi pomiarowemu |

## FAQs

### Q1: Czy Aspose.CAD for .NET jest kompatybilny ze wszystkimi formatami CAD?

A1: Aspose.CAD for .NET obsługuje szeroką gamę formatów CAD, w tym DWG, DXF, DWF i inne. Sprawdź [dokumentację](https://reference.aspose.com/cad/net/) po pełną listę.

### Q2: Czy mogę zmienić rozmiar wielu układów jednocześnie?

A2: Tak, możesz zmienić rozmiar wielu układów, modyfikując tablicę `Layouts` w `CadRasterizationOptions`.

### Q3: Gdzie mogę uzyskać wsparcie dla Aspose.CAD for .NET?

A3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) aby uzyskać wsparcie społeczności i pomoc.

### Q4: Czy dostępna jest darmowa wersja próbna?

A4: Tak, możesz wypróbować [darmową wersję próbną](https://releases.aspose.com/), aby ocenić funkcje Aspose.CAD for .NET.

### Q5: Jak mogę uzyskać tymczasową licencję dla Aspose.CAD for .NET?

A5: Uzyskaj tymczasową licencję do celów testowych [tutaj](https://purchase.aspose.com/temporary-license/).

## Frequently Asked Questions

**P: Jak skalować rysunek CAD bez zmiany typu jednostki?**  
O: Dostosuj właściwość `Zoom` w `CadRasterizationOptions` (np. `cadRasterizationOptions.Zoom = 2.0;`), aby podwoić rozmiar przy zachowaniu oryginalnej jednostki.

**P: Czy mogę eksportować do formatów innych niż BMP?**  
O: Oczywiście. Zamień `BmpOptions` na `PngOptions`, `JpegOptions` lub dowolną inną obsługiwaną klasę formatu rastrowego.

**P: Czy można przetwarzać wsadowo folder rysunków?**  
O: Tak. Przejdź pętlą po plikach w katalogu, zastosuj tę samą logikę rasteryzacji i zapisz każdy wynik pod unikalną nazwą.

---

**Ostatnia aktualizacja:** 2026-03-19  
**Testowano z:** Aspose.CAD for .NET 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}