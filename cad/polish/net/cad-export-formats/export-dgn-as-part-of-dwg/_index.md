---
date: 2026-03-21
description: Dowiedz się, jak tworzyć pliki PDF z DWG oraz eksportować DGN jako część
  DWG przy użyciu Aspose.CAD dla .NET. Ten przewodnik pokazuje również, jak konwertować
  DWG na PDF i ustawiać opcje PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Utwórz PDF z DWG i wyeksportuj DGN jako część DWG – Aspose.CAD dla .NET
url: /pl/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz PDF z DWG i wyeksportuj DGN jako część DWG – Aspose.CAD dla .NET

## Wstęp

Jeśli potrzebujesz **utworzyć PDF z plików DWG**, jednocześnie osadzając projekt DGN jako część DWG, Aspose.CAD dla .NET czyni to prostym. W tym samouczku przeprowadzimy Cię przez cały proces: wczytanie DWG, odnalezienie osadzonego podkładu DGN, skonfigurowanie opcji rasteryzacji oraz ostateczny eksport wyniku do dokumentu PDF. Niezależnie od tego, czy tworzysz narzędzie do konwersji wsadowej, silnik raportujący, czy usługę integracji CAD‑BIM, poniższe kroki zapewnią solidną, gotową do produkcji podstawę.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje konwersję DWG → PDF?** Aspose.CAD dla .NET  
- **Czy mogę wyeksportować podkład DGN podczas tworzenia PDF?** Tak – podkład jest dostępny poprzez `CadDgnUnderlay`.  
- **Która metoda ustawia opcje PDF?** `PdfOptions` wraz z `CadRasterizationOptions`.  
- **Czy potrzebna jest licencja do użytku komercyjnego?** Tak, wymagana jest ważna licencja Aspose.CAD.  
- **Obsługiwane wersje .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co to jest „utworzyć PDF z DWG”?

Utworzenie PDF z pliku DWG oznacza renderowanie rysunku wektorowego do dokumentu PDF o charakterze rastrowym lub wektorowym. Proces ten jest przydatny do udostępniania rysunków interesariuszom, którzy nie posiadają oprogramowania CAD, archiwizacji lub generowania drukowalnych raportów. Aspose.CAD upraszcza to zadanie, zajmując się parsowaniem encji DWG i zapewniając precyzyjną kontrolę nad wyjściem za pomocą `PdfOptions`.

## Dlaczego wyeksportować DGN jako część DWG?

Podkład DGN często reprezentuje geometrię referencyjną z projektów MicroStation. Eksportując DGN razem z DWG, zachowujesz oryginalny kontekst projektu, zapewniając, że odbiorcy zobaczą kompletny zestaw rysunków. Jest to szczególnie cenne w projektach multidyscyplinarnych, w których jednocześnie istnieją pliki DWG i DGN.

## Wymagania wstępne

- **Aspose.CAD dla .NET** – pobierz go [tutaj](https://releases.aspose.com/cad/net/).  
- **Środowisko programistyczne** – Visual Studio (dowolna aktualna wersja) lub ulubione IDE .NET.  
- **Podstawowa znajomość C#** – powinieneś być zaznajomiony ze składnią C# i strukturą projektu .NET.

## Importowanie przestrzeni nazw

Dodaj wymagane dyrektywy `using` na początku pliku źródłowego C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Przewodnik krok po kroku

### Krok 1: Zdefiniuj ścieżki plików

Ustaw plik wejściowy DWG oraz nazwę wyjściowego PDF.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Krok 2: Utwórz instancję `PdfOptions` (ustaw opcje PDF)

`PdfOptions` pozwala kontrolować sposób generowania PDF, np. rozmiar strony, kompresję i metadane.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Krok 3: Wczytaj plik DWG

Wczytaj DWG jako `CadImage`, aby móc przeglądać jego encje.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Krok 4: Przejdź przez encje

Iteruj po każdej encji w rysunku, aby odnaleźć podkład DGN.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Krok 5: Sprawdź typ encji (jak wyeksportować dgn)

Zidentyfikuj, czy bieżąca encja jest podkładem DGN.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Krok 6: Pobierz ścieżkę podkładu

Odczytaj ścieżkę zewnętrznego odniesienia do pliku DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Krok 7: Zdefiniuj opcje rasteryzacji (konwersja dwg do pdf)

Skonfiguruj, jak DWG ma być rasteryzowany przed umieszczeniem w PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Krok 8: Eksportuj DWG do PDF

Na koniec zapisz wyrenderowany obraz jako plik PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| **`Image.Load` zgłasza „File not found”** | Nieprawidłowa ścieżka lub brak pliku. | Użyj ścieżki bezwzględnej lub upewnij się, że DWG został skopiowany do folderu wyjściowego. |
| **Ścieżka podkładu jest pusta** | Podkład DGN nie jest osadzony lub odwołanie jest uszkodzone. | Zweryfikuj, czy DWG faktycznie zawiera podkład DGN i czy plik DGN jest dostępny. |
| **Wyjściowy PDF jest pusty** | Opcje rasteryzacji ustawione na zerowy rozmiar. | Dostosuj `PageWidth`/`PageHeight` lub ustaw `NoScaling = false`. |
| **Wyjątek licencyjny** | Uruchomiono bez ważnej licencji Aspose.CAD. | Zastosuj licencję przed wczytaniem obrazu: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla .NET w projektach komercyjnych?
Odp: Tak. Odwiedź [tutaj](https://purchase.aspose.com/buy), aby zapoznać się z opcjami licencjonowania.

### P2: Czy istnieją ograniczenia co do rozmiaru plików DWG, które mogę przetwarzać?
Odp: Aspose.CAD obsługuje duże pliki DWG, ale mogą obowiązywać ograniczenia sprzętowe.

### P3: Czy dostępna jest wersja próbna?
Odp: Tak, darmową wersję próbną można pobrać [tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać licencje tymczasowe?
Odp: Licencje tymczasowe są dostępne [tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę uzyskać pomoc, jeśli napotkam problemy?
Odp: Forum Aspose.CAD znajdziesz [tutaj](https://forum.aspose.com/c/cad/19).

**P: Jak ustawić dodatkowe metadane PDF (autor, tytuł itp.)?**  
O: Użyj właściwości `exportOptions.Metadata` przed wywołaniem `Save`.

**P: Czy mogę wyeksportować wiele układów na osobne strony PDF?**  
O: Tak – ustaw `Layouts = new string[] { "Layout1", "Layout2" }` w `CadRasterizationOptions`.

**P: Czy Aspose.CAD obsługuje konwersję DWG do innych formatów obrazu?**  
O: Oczywiście. Możesz eksportować do PNG, JPEG, SVG i innych, korzystając z odpowiednich przeciążeń `Image.Save`.

---

**Ostatnia aktualizacja:** 2026-03-21  
**Testowano z:** Aspose.CAD 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}