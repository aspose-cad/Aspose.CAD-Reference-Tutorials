---
date: 2026-04-09
description: Dowiedz się, jak wczytać plik DWFX w C# i konwertować CAD na PDF przy
  użyciu Aspose.CAD dla .NET. Przewodnik krok po kroku zapewniający płynną integrację.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: Otwieranie i uzyskiwanie dostępu do plików DWFX w C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak wczytać plik DWFX w C# z przewodnikiem Aspose.CAD
url: /pl/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak załadować plik DWFX w C# z przewodnikiem Aspose.CAD

## Wprowadzenie

Jeśli potrzebujesz **load DWFX file C#** i przekształcić go w PDF, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię krok po kroku przez dokładne czynności potrzebne do otwarcia rysunku DWFX przy użyciu Aspose.CAD dla .NET, skonfigurowania rasteryzacji i w końcu **c# convert CAD to PDF**. Niezależnie od tego, czy tworzysz narzędzie desktopowe, czy usługę webową, podejście pozostaje takie samo i działa z każdą wersją .NET obsługiwaną przez Aspose.CAD.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.CAD for .NET  
- **Czy mogę konwertować DWFX na PDF?** Tak – wystarczy skonfigurować `CadRasterizationOptions` i użyć `PdfOptions`.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy potrzebna jest licencja do testów?** Darmowa wersja próbna działa w trakcie rozwoju; stała licencja jest wymagana w produkcji.  
- **Jak długo trwa wykonanie kodu?** Ładowanie i konwersja typowego pliku DWFX kończy się w mniej niż sekundę na nowoczesnym procesorze.

## Co to jest plik DWFX?

DWFX (Design Web Format XPS) jest reprezentacją rysunku CAD opartą na XML, którą można renderować w przeglądarkach i innych przeglądarkach plików. Ponieważ przechowuje dane wektorowe, jest idealny do wysokiej jakości konwersji do PDF bez utraty szczegółów.

## Dlaczego używać Aspose.CAD do ładowania plików DWFX w C#?

* **Pełne wsparcie formatów** – Aspose.CAD rozumie DWFX oraz dziesiątki innych formatów CAD.  
* **Brak zewnętrznych zależności** – Czysty .NET, bez potrzeby AutoCADa czy innych natywnych komponentów.  
* **Łatwa konwersja raster‑wektor** – Przełączaj się między obrazami rastrowymi a wektorowymi PDF za pomocą kilku linii kodu.  

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz:

1. **Aspose.CAD for .NET** zainstalowany. Możesz go pobrać [tutaj](https://releases.aspose.com/cad/net/).  
2. Folder zawierający pliki DWFX, które chcesz przetworzyć. Zanotuj pełną ścieżkę zarówno dla źródła, jak i miejsca docelowego.

## Jak załadować plik DWFX w C#

Poniżej znajduje się przewodnik krok po kroku. Każdy krok jest opatrzony krótkim wyjaśnieniem, a następnie dokładnym blokiem kodu, który należy skopiować.

### Importowanie przestrzeni nazw

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

Te przestrzenie nazw dają dostęp do klasy `Image` służącej do ładowania plików CAD oraz opcji niezbędnych do rasteryzacji i wyjścia PDF.

### Krok 1: Ustaw katalogi źródłowy i wyjściowy

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` ścieżką, w której znajduje się Twój plik DWFX oraz miejscem, w którym ma zostać zapisany PDF.

### Krok 2: Załaduj plik DWFX

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` odczytuje plik DWFX do obiektu `Image`, z którym Aspose.CAD może pracować. Zmień `"Tyrannosaurus.dwfx"` na nazwę własnego rysunku.

### Krok 3: Skonfiguruj opcje rasteryzacji

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

Opcje rasteryzacji określają, jak duża ma być wynikowa strona. Użycie oryginalnych wymiarów rysunku zachowuje dokładną skalę.

### Krok 4: Zapisz jako PDF (c# convert CAD to PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Tutaj **c# convert CAD to PDF** poprzez dołączenie ustawień rasteryzacji do obiektu `PdfOptions` i wywołanie `Save`. Plik wyjściowy zostanie umieszczony w określonym folderze.

### Krok 5: Wyświetl komunikat o sukcesie

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

Prosty komunikat w konsoli informuje, że konwersja zakończyła się bez błędów.

## Typowe problemy i wskazówki

* **Plik nie znaleziony** – Sprawdź ponownie ścieżkę `SourceDir` i upewnij się, że nazwa pliku jest dokładnie taka sama, łącznie z wielkością liter.  
* **Pusty PDF** – Upewnij się, że plik DWFX rzeczywiście zawiera dane wektorowe; niektóre narzędzia eksportujące generują puste rysunki.  
* **Wydajność** – W przypadku bardzo dużych rysunków rozważ zmniejszenie `PageWidth`/`PageHeight` lub ustawienie niższej `Resolution` w `CadRasterizationOptions`.

## Najczęściej zadawane pytania

### P1: Czy Aspose.CAD dla .NET jest kompatybilny ze wszystkimi plikami DWFX?

A1: Aspose.CAD for .NET obsługuje szeroką gamę formatów CAD, w tym DWFX. Jednak zaleca się sprawdzenie dokumentacji pod kątem szczegółowych informacji o kompatybilności.

### P2: Gdzie mogę znaleźć dokumentację Aspose.CAD dla .NET?

A2: Dokumentacja jest dostępna [tutaj](https://reference.aspose.com/cad/net/).

### P3: Czy mogę wypróbować Aspose.CAD dla .NET przed zakupem?

A3: Tak, możesz pobrać darmową wersję próbną [tutaj](https://releases.aspose.com/).

### P4: Jak uzyskać tymczasową licencję dla Aspose.CAD dla .NET?

A4: Tymczasowe licencje można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Potrzebujesz wsparcia lub masz więcej pytań?

A5: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy.

### P6: Czy mogę przetwarzać wsadowo wiele plików DWFX?

A6: Absolutnie. Umieść logikę ładowania i zapisywania wewnątrz pętli `foreach`, która iteruje po plikach w katalogu.

### P7: Czy konwersja zachowuje warstwy i kolory?

A7: Informacje wektorowe, takie jak warstwy i kolory, są zachowywane w PDF, gdy źródłowy plik DWFX zawiera te dane.

**Ostatnia aktualizacja:** 2026-04-09  
**Testowane z:** Aspose.CAD for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}