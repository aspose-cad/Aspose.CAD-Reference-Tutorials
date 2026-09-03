---
date: 2026-08-23
description: Dowiedz się, jak utworzyć viewport dwg c# przy użyciu Aspose.CAD. Ten
  przewodnik obejmuje loading pliku DWG, configuring rasterization, defining viewport
  oraz saving wyniku jako PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Renderowanie dokumentów DWG w C#
og_description: Dowiedz się, jak utworzyć viewport dwg c# przy użyciu Aspose.CAD w
  .NET. Ten przewodnik krok po kroku pokazuje loading, rasterizing, defining viewports
  oraz saving do PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Jak utworzyć viewport dwg c# przy użyciu Aspose.CAD dla .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Jak utworzyć viewport dwg c# przy użyciu Aspose.CAD dla .NET
url: /pl/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderowanie dokumentów DWG w C# – samouczek tworzenia viewport dwg c#

## Wprowadzenie

W tym obszernej samouczku dowiesz się, jak **tworzyć viewport dwg c#** przy użyciu Aspose.CAD i renderować plik DWG do PDF. Niezależnie od tego, czy potrzebujesz wyodrębnić konkretny układ, wygenerować drukowalny arkusz, czy osadzić widok CAD w raporcie, kontrola viewportu daje precyzyjną kontrolę renderowania. Aspose.CAD obsługuje **ponad 20 formatów CAD** i może przetwarzać pliki z tysiącami elementów bez ładowania całego dokumentu do pamięci, co czyni go idealnym dla wydajnych aplikacji .NET.

## Szybkie odpowiedzi
- **Jaki jest pierwszy krok?** Załaduj plik DWG za pomocą `CadImage.Load`.
- **Która klasa definiuje obszar widoku?** `Viewport` wewnątrz `CadRasterizationOptions`.
- **Czy mogę wyeksportować do PDF?** Tak, używając `PdfOptions` po rasteryzacji.
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna; darmowa wersja próbna działa w celach oceny.
- **Czy .NET Core jest obsługiwany?** Absolutnie – Aspose.CAD działa z .NET Framework, .NET Core oraz .NET 5/6.

## Wymagania wstępne

- Podstawowa znajomość programowania w C#.
- Zainstalowany Visual Studio (dowolna aktualna edycja).
- Biblioteka Aspose.CAD dodana do projektu. Możesz ją pobrać ze [strony pobierania Aspose.CAD](https://releases.aspose.com/cad/net/).
- Przykładowy plik DWG, np. **Bottom_plate.dwg**, aby podążać za instrukcją.

## Importowanie przestrzeni nazw

Dodaj wymagane dyrektywy `using` na początku pliku C#, aby kompilator mógł odnaleźć typy Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Teraz, gdy środowisko jest gotowe, przejdźmy krok po kroku przez implementację.

## Jak stworzyć viewport dwg c#?

Aby utworzyć niestandardowy viewport, najpierw załaduj plik DWG do obiektu `CadImage`, a następnie skonfiguruj `CadRasterizationOptions` z żądanym układem i skalowaniem. Zdefiniuj region, który chcesz wyświetlić, utwórz `CadVportTableObject` z obliczonym środkiem, wysokością i współczynnikiem proporcji, zastąp aktywny viewport, ustaw opcje PDF i na końcu zapisz wynik.

## Krok 1: załaduj plik dwg

`CadImage.Load` ładuje plik DWG do obiektu `CadImage`, który reprezentuje rysunek CAD w pamięci.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Krok 2: skonfiguruj opcje rasteryzacji

`CadRasterizationOptions` określa, jak rysunek CAD jest rasteryzowany, w tym wybór układu, skalowanie i rozmiar wyjściowy.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Krok 3: zdefiniuj region do rysowania

`Point` definiuje współrzędne X i Y lewego górnego rogu regionu do renderowania.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Krok 4: utwórz nowy viewport

`CadVportTableObject` reprezentuje obiekt viewportu, który kontroluje widoczny obszar i współczynnik proporcji renderowanego rysunku.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: zastąp aktywny viewport

Pętla zastępuje aktywny viewport nowo utworzonym, aby zastosować niestandardowe ustawienia widoku.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Krok 6: skonfiguruj opcje PDF

`PdfOptions` konfiguruje parametry wyjścia PDF, takie jak kompresja i metadane.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 7: zapisz wyrenderowany dwg jako PDF

`image.Save` zapisuje wyrenderowany obraz do pliku przy użyciu określonych opcji formatu.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Dlaczego używać niestandardowego viewportu przy renderowaniu DWG?

Niestandardowy viewport pozwala wyodrębnić konkretny układ lub region, zmniejszając rozmiar pliku i przyspieszając renderowanie. Aspose.CAD może wyrenderować 300‑stronnicowy DWG w mniej niż 2 sekundy przy użyciu skoncentrowanego viewportu, w porównaniu z renderowaniem całego rysunku, które może trwać kilka sekund dłużej.

## Typowe problemy i rozwiązania

- **Pusty wynik** – Upewnij się, że współrzędne viewportu mieszczą się w granicach rysunku; użyj `CadImage.Size`, aby zweryfikować granice.
- **Brakujące warstwy** – Ustaw `CadRasterizationOptions.Layouts` na właściwą nazwę układu; w przeciwnym razie domyślny układ może być pusty.
- **Spowolnienie wydajności** – Wyłącz anti‑aliasing w `CadRasterizationOptions`, jeśli potrzebujesz tylko szybkiego podglądu.

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.CAD z innymi formatami plików CAD?

A1: Tak, Aspose.CAD obsługuje różne formaty, w tym DWG, DXF, DWF oraz ponad 20 dodatkowych typów CAD.

### P2: Czy Aspose.CAD jest kompatybilny z .NET Core?

A2: Tak, Aspose.CAD działa z .NET Framework, .NET Core oraz najnowszymi wersjami .NET.

### P3: Jak mogę obsługiwać różne układy w pliku DWG?

A3: Określ żądany układ, używając właściwości `Layouts` w `CadRasterizationOptions` przed renderowaniem.

### P4: Czy istnieją kwestie licencyjne związane z używaniem Aspose.CAD?

A4: Aby uzyskać szczegóły dotyczące licencjonowania, odwiedź [stronę licencjonowania Aspose.CAD](https://purchase.aspose.com/buy).

### P5: Gdzie mogę znaleźć dodatkowe wsparcie?

A5: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy i dyskusji społeczności.

### P6: Czy mogę renderować bezpośrednio do PNG zamiast PDF?

A6: Tak, zmień `PdfOptions` na `PngOptions` i wywołaj `image.Save("output.png", pngOptions)`.

### P7: Jak wstawić wyrenderowany obraz do aplikacji Windows Forms?

A7: Załaduj zapisany obraz do kontrolki `PictureBox` używając `Image.FromFile("output.png")`.

## Podsumowanie

Teraz wiesz, jak **tworzyć viewport dwg c#** i renderować plik DWG do PDF (lub innych formatów rastrowych) przy użyciu Aspose.CAD. Opanowując manipulację viewportem, uzyskasz precyzyjną kontrolę nad wyjściem wizualnym, co jest niezbędne do generowania dokładnych rysunków inżynierskich, raportów czy miniatur. Eksploruj dodatkowe ustawienia rasteryzacji, eksperymentuj z różnymi formatami wyjściowymi i integruj kod w większych usługach .NET lub aplikacjach desktopowych.

---

**Ostatnia aktualizacja:** 2026-08-23  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Jak ustawić viewport podczas konwersji DWG do PDF z współrzędnymi w C# – samouczek Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Naucz się ustawiać opcje rasteryzacji CAD – eksportuj konkretne układy do PDF przy użyciu Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Jak konwertować DWG do PDF i obrazów rastrowych przy użyciu Aspose.CAD dla .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}