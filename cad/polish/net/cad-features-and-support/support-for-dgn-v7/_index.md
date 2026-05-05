---
date: 2026-03-29
description: Dowiedz się, jak konwertować DGN na JPEG za pomocą Aspose.CAD dla .NET,
  zapewniając pełne wsparcie dla DGN V7 i umożliwiając łatwą konwersję CAD na obrazy
  rastrowe.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DGN na JPEG przy użyciu Aspose.CAD dla .NET – wsparcie V7
url: /pl/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DGN do JPEG przy użyciu Aspose.CAD dla .NET – Obsługa V7

## Wprowadzenie

W tym tutorialu dowiesz się, jak **konwertować DGN do JPEG** przy użyciu Aspose.CAD dla .NET, wykorzystując pełne wsparcie biblioteki dla DGN V7. Konwersja plików DGN na obrazy rastrowe, takie jak JPEG, jest powszechnym wymogiem, gdy trzeba osadzić rysunki CAD na stronach internetowych, w aplikacjach mobilnych lub w narzędziach raportujących. Aspose.CAD umożliwia także **konwertowanie CAD do formatu rastrowego** w sposób efektywny, dając elastyczność w prezentacji danych projektowych.

## Szybkie odpowiedzi
- **Co obejmuje tutorial?** Konwersja pliku DGN V7 do obrazu rastrowego JPEG przy użyciu Aspose.CAD dla .NET.  
- **Która wersja biblioteki jest wymagana?** Dowolna aktualna wersja Aspose.CAD dla .NET, która zawiera wsparcie dla DGN V7.  
- **Czy potrzebuję licencji?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę zmienić rozmiar wyjściowy?** Tak – opcje rasteryzacji pozwalają ustawić szerokość, wysokość i skalowanie strony.  
- **Czy JPEG jest jedynym formatem wyjściowym?** Nie – Aspose.CAD obsługuje wiele formatów rastrowych (PNG, BMP, TIFF itp.).

## Co to jest DGN V7?
DGN (Design) to format pliku pierwotnie stworzony przez Bentley Systems dla MicroStation. Wersja 7 wprowadza bogatszą geometrię i metadane, co czyni go popularnym wyborem w projektach inżynierii lądowej i infrastruktury. Aspose.CAD dla .NET potrafi odczytać pliki DGN V7 bezpośrednio, udostępniając ich zawartość jako obiekty `CadImage`, które można rasteryzować lub konwertować na inne formaty.

## Dlaczego konwertować DGN do JPEG?
- **Gotowe do sieci:** Obrazy JPEG są lekkie i wyświetlają się natychmiast w przeglądarkach, nie wymagając specjalnych wtyczek.  
- **Wieloplatformowość:** JPEG można oglądać na dowolnym urządzeniu, co czyni go idealnym do udostępniania rysunków CAD osobom nietechnicznym.  
- **Uproszczone przepływy pracy:** Konwersja do formatu rastrowego eliminuje potrzebę używania przeglądarek CAD w kolejnych etapach przetwarzania.

## Wymagania wstępne

Zanim przejdziesz do implementacji, upewnij się, że masz następujące elementy:

- **Aspose.CAD dla .NET** – pobierz go ze [strony](https://releases.aspose.com/cad/net/).  
- **Środowisko programistyczne** – Visual Studio (lub dowolne IDE obsługujące .NET).  

Posiadanie tych elementów pozwoli Ci podążać za krokami bez przerw.

## Importuj przestrzenie nazw

Rozpocznij od zaimportowania przestrzeni nazw niezbędnych do obsługi `CadImage` i rasteryzacji.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DGN

Załaduj źródłowy plik DGN do obiektu `CadImage`. Zastąp ścieżkę zastępczą folderem, w którym znajduje się Twój plik DGN.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Krok 2: Skonfiguruj opcje rasteryzacji

Zdefiniuj, w jaki sposób rysunek DGN ma być rasteryzowany. Możesz kontrolować wymiary wyjściowe oraz zachowanie skalowania.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Krok 3: Ustaw opcje rasteryzacji wektorowej

Utwórz obiekt `JpegOptions` (lub inny obiekt opcji formatu rastrowego) i dołącz ustawienia rasteryzacji.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Krok 4: Zapisz rasteryzowany obraz

Na koniec wyeksportuj rysunek DGN do pliku JPEG przy użyciu metody `Save`.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Po pomyślnym uruchomieniu kodu znajdziesz reprezentację JPEG oryginalnego rysunku DGN V7 w określonym folderze.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Plik nie znaleziony** | Zweryfikuj, czy `MyDir` kończy się separatorem ścieżki (`\\` lub `/`) oraz czy nazwa pliku jest poprawna. |
| **Pusty obraz wyjściowy** | Upewnij się, że `NoScaling` jest ustawione odpowiednio; ustaw na `false`, jeśli chcesz, aby rysunek wypełnił stronę. |
| **Nieobsługiwane elementy** | Aspose.CAD obsługuje większość elementów DGN, ale bardzo stare lub niestandardowe obiekty mogą być pominięte. Sprawdź dziennik konwersji pod kątem ostrzeżeń. |

## Najczęściej zadawane pytania

### Q1: Czy Aspose.CAD jest kompatybilny z najnowszymi specyfikacjami DGN V7?
**A:** Tak, Aspose.CAD w pełni obsługuje DGN V7, przetwarzając zarówno geometrię, jak i metadane zgodnie z najnowszymi standardami.

### Q2: Czy mogę dostosować opcje rasteryzacji przy konwersji pliku DGN?
**A:** Oczywiście. Klasa `CadRasterizationOptions` pozwala regulować rozmiar strony, skalowanie, grubość linii, kolor tła i wiele innych parametrów.

### Q3: Czy istnieją inne obsługiwane formaty wyjściowe oprócz JPEG?
**A:** Tak, Aspose.CAD może eksportować do PNG, BMP, TIFF i kilku innych formatów rastrowych. Wystarczy użyć odpowiedniej klasy `*Options` (np. `PngOptions`).

### Q4: Jak mogę uzyskać pomoc w kwestiach związanych z Aspose.CAD?
**A:** Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania wsparcia społeczności i oficjalnych odpowiedzi.

### Q5: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla .NET?
**A:** Tak, możesz pobrać wersję próbną [tutaj](https://releases.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-03-29  
**Testowano z:** Aspose.CAD 24.12 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}