---
date: 2026-04-06
description: Dowiedz się, jak konwertować pliki DWG na PDF i dodawać własny tekst
  przy użyciu C# i Aspose.CAD. Ten przewodnik krok po kroku obejmuje generowanie PDF
  z DWG, wstawianie encji tekstowej oraz zmianę czcionki tekstu w DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Dodawanie tekstu do plików DWG w C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DWG na PDF i dodaj tekst w C# – Poradnik Aspose.CAD
url: /pl/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PDF i Dodaj Tekst w C# – Aspose.CAD Samouczek

## Wprowadzenie

W szybko zmieniającym się świecie CAD i programowania .NET, **konwertowanie DWG do PDF** przy jednoczesnym wstawianiu własnych adnotacji jest częstym wymaganiem. Niezależnie od tego, czy potrzebujesz generować wydrukowalne rysunki dla klientów, czy osadzać dynamiczne notatki bezpośrednio w pliku DWG, Aspose.CAD ułatwia to zadanie. W tym samouczku nauczysz się, jak **konwertować DWG do PDF**, **dodać encję tekstową** oraz nawet **zmienić czcionkę tekstu w DWG** przy użyciu C#.

## Szybkie Odpowiedzi
- **Jaka biblioteka jest najlepsza do konwersji DWG‑do‑PDF?** Aspose.CAD for .NET  
- **Czy mogę dodać własny tekst podczas konwersji?** Tak – utwórz encję `CadText` i dodaj ją przed zapisem.  
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest licencja komercyjna; dostępna jest darmowa wersja próbna.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy można zmienić czcionkę tekstu?** Tak, dostosuj właściwości `CadText`, takie jak `StyleType` i `TextHeight`.

## Co to jest „konwersja dwg do pdf”?

Konwersja pliku DWG do PDF przekształca wektorowy rysunek CAD w powszechnie udostępniany, niezależny od urządzenia dokument. PDF zachowuje oryginalną geometrię i warstwy, jednocześnie umożliwiając osadzanie adnotacji, tekstu lub innych metadanych. Aspose.CAD automatycznie obsługuje rasteryzację i renderowanie wektorowe, więc nie potrzebujesz żadnego zewnętrznego oprogramowania CAD na serwerze.

## Dlaczego dodać tekst do DWG przed konwersją?

Osadzenie tekstu bezpośrednio w pliku DWG daje pełną kontrolę nad pozycjonowaniem, stylizacją i przypisaniem do warstwy. Gdy plik zostanie później skonwertowany do PDF, tekst pojawia się dokładnie tam, gdzie został umieszczony, zachowując zamierzenia projektowe i eliminując potrzebę późniejszej obróbki w edytorze PDF.

## Wymagania wstępne

- **Biblioteka Aspose.CAD** – pobierz ją z [download link](https://releases.aspose.com/cad/net/).  
- **Działające środowisko .NET** (Visual Studio 2022, .NET 6 lub dowolna kompatybilna wersja).  
- **Folder na pliki testowe** – będziemy odnosić się do niego jako `MyDir` w całym przewodniku.

Teraz przejdźmy krok po kroku przez proces.

## Importowanie przestrzeni nazw

Dodaj wymagane instrukcje `using`, aby uzyskać dostęp do klas Aspose.CAD.

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

Załaduj swój źródłowy plik DWG do obiektu `Image`. Ten obiekt zapewnia dostęp do leżących u podstaw encji CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Krok 2: Utwórz obiekt CadText (Wstaw encję tekstową)

Klasa `CadText` reprezentuje pojedynczą linię tekstu w DWG. Tutaj ustawiamy jej styl, wartość, kolor, warstwę i pozycję. Dostosuj `StyleType` lub `TextHeight`, aby **zmienić czcionkę tekstu w DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Krok 3: Dodaj encję tekstową do Model Space

Model Space w DWG zawiera większość encji rysunkowych. Dodając nasz `CadText` do bloku `*Model_Space`, tekst staje się częścią rysunku.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Krok 4: Skonfiguruj opcje PDF (Generowanie PDF z DWG)

Ustaw opcje rasteryzacji, które kontrolują, jak DWG jest renderowany do PDF. Możesz dostosować rozmiar strony, typ rysowania i układ.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 5: Zapisz zmodyfikowany DWG jako PDF

Na koniec wyeksportuj zmodyfikowany rysunek. Powstały PDF zawiera nowo wstawiony tekst.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Wskazówka:** Jeśli potrzebujesz PDF o wyższej rozdzielczości, zwiększ proporcjonalnie `PageHeight` i `PageWidth`.

## Częste problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| Tekst nie pojawia się w PDF | Nieprawidłowa warstwa lub identyfikator koloru | Upewnij się, że `LayerName` istnieje i `ColorId` jest ustawiony na widoczny kolor (np. 7 dla białego). |
| Tekst jest nieprawidłowo umieszczony | Niepoprawne współrzędne wyrównania | Sprawdź wartości `FirstAlignment.X/Y` względem jednostek rysunku. |
| PDF jest pusty | Nie ustawiono opcji rasteryzacji | Ustaw `DrawType` na `UseObjectColor` lub `UseObjectLineWeight`. |

## Najczęściej zadawane pytania (istniejące)

### Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?
A1: Aspose.CAD obsługuje szeroki zakres wersji plików DWG, zapewniając kompatybilność z różnym oprogramowaniem CAD.

### Q2: Czy mogę dodać wiele encji tekstowych do jednego pliku DWG przy użyciu Aspose.CAD?
A2: Tak, możesz dodać wiele encji tekstowych do pliku DWG, powtarzając proces opisany w samouczku.

### Q3: Jak mogę zmienić czcionkę i styl tekstu w Aspose.CAD?
A3: Aby zmodyfikować czcionkę i styl tekstu, dostosuj właściwości obiektu `CadText` przed dodaniem go do pliku DWG.

### Q4: Czy istnieją kwestie licencyjne przy używaniu Aspose.CAD w projekcie komercyjnym?
A5: Tak, zapewnij zgodność z warunkami licencjonowania Aspose.CAD. Szczegóły znajdziesz w [Aspose.CAD Purchase](https://purchase.aspose.com/buy).

### Q5: Gdzie mogę uzyskać pomoc lub dyskutować o zapytaniach związanych z Aspose.CAD?
A5: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby połączyć się ze społecznością i uzyskać wsparcie.

## Dodatkowe FAQ

**P:** Jak wygenerować PDF z DWG bez dodawania tekstu?  
**A:** Pomiń krok tworzenia `CadText` i bezpośrednio skonfiguruj `PdfOptions` przed wywołaniem `image.Save(...)`.

**P:** Czy mogę zmienić kolor tekstu programowo?  
**A:** Tak, ustaw `cadText.ColorId` na konkretny numer koloru ACI (np. 1 dla czerwonego).

**P:** Czy można wstawić tekst wieloliniowy?  
**A:** Użyj `CadMText` dla bloków tekstu wieloliniowego; podejście jest podobne do `CadText`.

**P:** Czy Aspose.CAD obsługuje konwersję wsadową wielu plików DWG?  
**A:** Zdecydowanie – przeiteruj katalog z plikami DWG, zastosuj te same kroki i zapisz każdy jako PDF.

## Zakończenie

Masz teraz kompletny, gotowy do produkcji przepływ pracy, aby **konwertować DWG do PDF**, **dodawać własny tekst** i **dostosowywać wygląd tekstu** przy użyciu C# i Aspose.CAD. Ta technika jest idealna do automatycznego generowania rysunków, pipeline'ów raportowania lub dowolnego scenariusza, w którym trzeba na bieżąco wzbogacać pliki CAD.

---

**Ostatnia aktualizacja:** 2026-04-06  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}