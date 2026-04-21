---
date: 2026-03-13
description: Dowiedz się, jak ustawić opcje rasteryzacji CAD i wyeksportować wybrane
  układy DWG do PDF przy użyciu Aspose.CAD dla .NET – definitywny przewodnik tworzenia
  PDF z pliku CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ustaw opcje rasteryzacji CAD – Eksportuj określone układy do PDF - Przewodnik
  Aspose.CAD
url: /pl/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie określonych układów do PDF - Aspose.CAD Guide

## Introduction

W tym samouczku odkryjesz **jak ustawić opcje rasteryzacji CAD**, aby móc wyeksportować pojedynczy układ — lub wiele układów — z pliku DWG bezpośrednio do PDF. Aspose.CAD dla .NET sprawia, że proces *dwg to pdf conversion c#* jest prosty, dając pełną kontrolę nad rozmiarem strony, rozdzielczością i wyborem układu. Po zakończeniu przewodnika będziesz w stanie **tworzyć PDF z pliku CAD** przy użyciu kilku linii kodu.

## Quick Answers
- **Co robi „set cad rasterization options”?**  
  Informuje Aspose.CAD, jak renderować dane wektorowe (układy, warstwy, grubości linii) na rasteryzowane strony PDF.  
- **Która metoda eksportuje układ DWG do PDF?**  
  Użyj `Image.Save` z skonfigurowanym `PdfOptions`, który zawiera Twoje `CadRasterizationOptions`.  
- **Czy mogę wyeksportować więcej niż jeden układ jednocześnie?**  
  Tak — podaj tablicę nazw układów w właściwości `Layouts`.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?**  
  Wymagana jest licencja komercyjna; dostępna jest bezpłatna wersja próbna do oceny.  
- **Jakie wersje .NET są obsługiwane?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 i późniejsze.

## What is “set cad rasterization options”?

`CadRasterizationOptions` jest klasą, która kontroluje, jak jednostki CAD są rasteryzowane przy konwersji do formatów opartych na rastrze, takich jak PDF. Konfigurując jej właściwości — wymiary strony, wybór układu, kolor tła itp. — określasz wizualny rezultat operacji **export dwg layout to pdf**.

## Why set CAD rasterization options?

- **Precyzja** – Zachowuje grubości linii i skale dokładnie tak, jak występują w oryginalnym rysunku CAD.  
- **Wydajność** – Renderuj tylko potrzebne układy, zmniejszając rozmiar pliku i czas przetwarzania.  
- **Elastyczność** – Dostosuj szerokość/wysokość strony, DPI i tło, aby odpowiadały Twoim standardom raportowania.  

## Prerequisites

Before we dive into the code, ensure you have:

- **Aspose.CAD for .NET** zainstalowany. Możesz go pobrać [tutaj](https://releases.aspose.com/cad/net/).  
- Środowisko programistyczne .NET (Visual Studio, VS Code lub dowolne IDE, którego używasz).  
- Plik DWG zawierający przynajmniej jeden układ (przykładowy plik użyty tutaj to `visualization_-_conference_room.dwg`).

## Import Namespaces

In your .NET project, import the necessary namespaces for Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Krok 1: Load the DWG file

Najpierw wskaż Aspose.CAD na źródłowy plik DWG, który chcesz przekonwertować.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Krok 2: Set **CadRasterizationOptions**

Tutaj konfigurujemy ustawienia rasteryzacji, które określają rozmiar strony PDF i rozdzielczość.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** Dostosuj `PageWidth` i `PageHeight`, aby pasowały do wymiarów docelowego układu PDF. Większe wartości zwiększają szczegółowość, ale także rozmiar pliku.

### Krok 3: Specify the layout name

Powiedz Aspose.CAD, które układy mają zostać wyrenderowane. Zastąp `"Layout1"` dokładną nazwą układu w Twoim pliku DWG.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Dlaczego to ważne:** Ograniczając tablicę `Layouts`, unikasz eksportowania niechcianych arkuszy, co sprawia, że operacja **dwg to pdf conversion c#** jest szybsza, a powstały PDF czystszy.

### Krok 4: Create `PdfOptions`

Połącz ustawienia rasteryzacji z opcjami eksportu PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 5: Export to PDF

Na koniec zapisz wyrenderowany układ jako plik PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Krok 6: Display a success message

Krótki komunikat w konsoli potwierdza, że operacja zakończyła się sukcesem.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Common Issues & Solutions

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **Brak wygenerowanego PDF** | Tablica `Layouts` nie odpowiada żadnej nazwie układu w pliku DWG. | Sprawdź nazwy układów przy użyciu przeglądarki CAD i zaktualizuj właściwość `Layouts`. |
| **Puste strony** | `PageWidth`/`PageHeight` ustawione na 0 lub bardzo małe wartości. | Użyj realistycznych wymiarów (np. 1600 × 1600) lub pozwól Aspose obliczyć je automatycznie, pomijając te właściwości. |
| **Nieprawidłowe skalowanie** | DPI nie ustawione, gdy wymagana jest wysokiej rozdzielczości wyjście. | Ustaw `rasterizationOptions.Resolution = 300;` (lub żądane DPI) przed eksportem. |

## Frequently Asked Questions

**P:** Czy mogę eksportować wiele układów jednocześnie?  
**O:** Tak, po prostu zmodyfikuj tablicę `Layouts` w Kroku 3, aby zawierała wszystkie żądane nazwy układów, np. `new string[] { "Layout1", "Layout2" }`.

**P:** Czy Aspose.CAD jest kompatybilny z innymi formatami plików CAD?  
**O:** Zdecydowanie tak. Obsługuje DWG, DXF, DWF, DGN i wiele innych formatów.

**P:** Jak mogę dostosować ustawienia wyjścia PDF poza rozmiarem strony?  
**O:** Zbadaj dodatkowe właściwości `CadRasterizationOptions`, takie jak `Resolution`, `BackgroundColor` i `DrawType`, aby precyzyjnie dostroić wynik.

**P:** Gdzie mogę znaleźć dodatkową dokumentację Aspose.CAD?  
**O:** Odwiedź [dokumentację](https://reference.aspose.com/cad/net/) aby uzyskać szczegółowe odniesienia API i przykłady.

**P:** Czy dostępna jest darmowa wersja próbna?  
**O:** Tak, darmową wersję próbną możesz uzyskać [tutaj](https://releases.aspose.com/).

## Conclusion

Teraz wiesz, jak **ustawiać opcje rasteryzacji CAD** i używać ich do **eksportowania konkretnych układów DWG do PDF** przy użyciu Aspose.CAD dla .NET. To podejście daje precyzyjną kontrolę nad procesem konwersji, umożliwiając szybkie i niezawodne włączenie funkcjonalności CAD‑do‑PDF w dowolnej aplikacji C#.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}