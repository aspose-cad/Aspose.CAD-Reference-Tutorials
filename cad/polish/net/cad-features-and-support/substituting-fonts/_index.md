---
date: 2026-03-29
description: Dowiedz się, jak szybko wymienić czcionki w Aspose.CAD dla .NET. Ten
  przewodnik krok po kroku pokazuje, jak ustawić nazwę głównej czcionki i efektywnie
  dostosować rysunki CAD.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak zastąpić czcionki w Aspose.CAD dla .NET
url: /pl/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zamienić czcionki w Aspose.CAD dla .NET

## Wprowadzenie

W dziedzinie tworzenia aplikacji CAD przy użyciu .NET, nauka **jak zamienić czcionki** jest kluczową umiejętnością, która może znacząco poprawić jakość wizualną Twoich rysunków. Aspose.CAD dla .NET oferuje prostą API, która pozwala **ustawić nazwę podstawowej czcionki** dla dowolnego stylu, co umożliwia łatwą globalną lub selektywną zamianę czcionek. W tym samouczku przeprowadzimy Cię przez cały proces — od wczytania rysunku po wymianę czcionek globalnie lub według konkretnej nazwy stylu.

## Szybkie odpowiedzi
- **Jaka jest główna klasa do manipulacji CAD?** `Aspose.CAD.Image` (lub jej pochodna `CadImage`).
- **Która właściwość zmienia czcionkę?** `PrimaryFontName` w `CadStyleTableObject`.
- **Czy mogę zamienić czcionki we wszystkich stylach jednocześnie?** Tak, iteruj przez `cadImage.Styles` i ustaw właściwość.
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.CAD do użytku nie‑trial.
- **Obsługiwane wersje .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Czym jest zamiana czcionek w CAD?
Zamiana czcionek oznacza zastąpienie pierwotnego kroju pisma używanego w rysunku CAD innym, dostępnym w systemie docelowym. Jest to szczególnie przydatne, gdy oryginalna czcionka jest nieobecna, gdy potrzebny jest spójny styl firmowy lub przy przygotowywaniu rysunków do druku na urządzeniach obsługujących jedynie ograniczony zestaw czcionek.

## Dlaczego zamieniać czcionki przy użyciu Aspose.CAD?
- **Brak zewnętrznych zależności** – biblioteka obsługuje mapowanie czcionek wewnętrznie.
- **Działa z wieloma formatami** – DXF, DWG, DGN i inne.
- **Programowa kontrola** – automatyzuj proces konwersji wsadowych lub w pipeline CI.
- **Zachowuje geometrię rysunku** – zmienia się jedynie wizualna reprezentacja tekstu.

## Wymagania wstępne

- Podstawowa znajomość programowania w .NET.
- Zainstalowany Aspose.CAD dla .NET. Jeśli jeszcze go nie zainstalowałeś, pobierz go [tutaj](https://releases.aspose.com/cad/net/).
- Plik rysunku CAD (DXF, DWG, itp.) do eksperymentów.

## Importowanie przestrzeni nazw

Zanim rozpoczniesz, zaimportuj niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.CAD w swojej aplikacji .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Krok 1: Wczytaj rysunek CAD

Rozpocznij od wczytania rysunku CAD do instancji `CadImage`. Upewnij się, że podajesz prawidłową ścieżkę do katalogu dokumentu.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Krok 2: Iteracja po stylach

Następnie iteruj po stylach w rysunku CAD używając pętli `foreach`. Pozwala to na dostęp i manipulację poszczególnymi stylami czcionek.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Jak ustawić nazwę podstawowej czcionki dla zamiany czcionek

Właściwość `PrimaryFontName` w każdym `CadStyleTableObject` kontroluje, która czcionka jest używana podczas renderowania rysunku. Ustawiając tę właściwość, skutecznie zastępujesz oryginalną czcionkę.

### Krok 3: Globalna zamiana czcionek

Aby zamienić czcionki we **wszystkich** stylach, ustaw właściwość `PrimaryFontName` dla każdego stylu na żądaną nazwę czcionki, na przykład `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Krok 4: Zamiana czcionki według nazwy stylu

Jeśli potrzebujesz zamienić czcionkę tylko dla konkretnego stylu (np. styl o nazwie `"Roman"`), dodaj warunkowe sprawdzenie wewnątrz pętli.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Typowe problemy i rozwiązywanie

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| Czcionka nie zmienia się po uruchomieniu kodu | Rysunek jest buforowany lub otwarty w trybie tylko do odczytu | Upewnij się, że zapisujesz obraz po modyfikacji (`cadImage.Save(...)`) lub ponownie wczytaj plik w celu weryfikacji. |
| Żądana czcionka nie została znaleziona w systemie | Czcionka nie jest zainstalowana na maszynie uruchamiającej kod | Zainstaluj wymaganą czcionkę TrueType/OpenType lub osadź ją w zasobach aplikacji. |
| Tekst jest zniekształcony | Nieprawidłowe kodowanie lub brak wsparcia Unicode | Użyj czcionki obsługującej wymagany zestaw znaków (np. Arial Unicode MS). |

## Najczęściej zadawane pytania

**Q: Czy mogę cofnąć zmiany czcionek w Aspose.CAD dla .NET?**  
A: Tak, możesz cofnąć zmiany, ponownie wczytując oryginalny rysunek CAD lub zachowując kopię zapasową przed wprowadzeniem modyfikacji.

**Q: Czy istnieją inne właściwości czcionek, które mogę modyfikować?**  
A: Oczywiście. Oprócz `PrimaryFontName` możesz pracować z `SecondaryFontName`, `FontFamily` oraz innymi atrybutami związanymi ze stylem w celu zaawansowanej personalizacji.

**Q: Czy Aspose.CAD jest kompatybilny z różnymi formatami CAD?**  
A: Tak, Aspose.CAD obsługuje szeroką gamę formatów, takich jak DXF, DWG, DGN, DWF i inne, zapewniając elastyczność w różnych projektach.

**Q: Czy mogę automatyzować zamianę czcionek w przetwarzaniu wsadowym?**  
A: Oczywiście. Umieść logikę wczytywania i zamiany w pętli iterującej po folderze plików CAD lub zintegrować ją z pipeline CI/CD.

**Q: Gdzie mogę znaleźć dodatkowe wsparcie dla Aspose.CAD dla .NET?**  
A: Aby uzyskać dodatkowe wsparcie i dyskusje społeczności, odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Ostatnia aktualizacja:** 2026-03-29  
**Testowano z:** Aspose.CAD for .NET (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}