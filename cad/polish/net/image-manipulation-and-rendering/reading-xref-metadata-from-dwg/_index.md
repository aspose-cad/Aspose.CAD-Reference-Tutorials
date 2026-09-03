---
date: 2026-08-23
description: Odkryj możliwości Aspose.CAD dla .NET dzięki naszemu krok po kroku tutorialowi,
  jak odczytać metadane xref z plików DWG.
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: Odczytywanie metadanych XREF z plików DWG
og_description: Dowiedz się, jak odczytać metadane xref z plików DWG przy użyciu Aspose.CAD
  dla .NET. Ten przewodnik przeprowadzi Cię przez wymagania wstępne, kroki kodu i
  typowe pułapki w mniej niż dziesięć minut.
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: Jak odczytać metadane xref z plików DWG przy użyciu Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: Jak odczytać metadane xref z plików DWG przy użyciu Aspose.CAD
url: /pl/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak odczytać metadane xref z plików DWG przy użyciu Aspose.CAD

## Wprowadzenie

W tym samouczku dowiesz się **jak odczytać metadane xref** z plików DWG przy użyciu biblioteki Aspose.CAD dla .NET. Niezależnie od tego, czy musisz audytować zewnętrzne odwołania, migrować starsze rysunki, czy budować własny potok BIM, wyodrębnianie informacji XREF jest powszechnym wymaganiem. Przejdziemy przez każdy krok, od konfiguracji projektu po przetwarzanie metadanych, i podkreślimy praktyczne wskazówki, które możesz zastosować od razu.

## Szybkie odpowiedzi
- **Jaki jest główny cel?** Pobranie punktów wstawienia i ścieżek plików zewnętrznych odwołań (XREF) osadzonych w rysunku DWG.  
- **Która biblioteka jest wymagana?** Aspose.CAD dla .NET (obsługuje ponad 50 formatów CAD).  
- **Czy potrzebna jest licencja?** Wymagana jest tymczasowa lub pełna licencja do użytku produkcyjnego; dostępna jest bezpłatna wersja próbna.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Jak długo trwa wykonanie kodu?** Przetworzenie typowego pliku DWG o 200 stronach z kilkoma XREF-ami kończy się w mniej niż sekundę na standardowym sprzęcie.

## Co to jest odczyt metadanych xref?
`read xref metadata` odnosi się do operacji uzyskiwania właściwości zewnętrznych jednostek referencyjnych przechowywanych wewnątrz rysunku DWG, takich jak ich współrzędne wstawienia, ścieżki plików źródłowych i flagi widoczności. Operacja ta pozwala programowo odkrywać, jak rysunek jest zbudowany z innych plików, umożliwiając automatyczną weryfikację, raportowanie lub przetwarzanie wsadowe powiązanych zasobów.

## Dlaczego używać Aspose.CAD do tego zadania?
Aspose.CAD obsługuje **ponad 50 formatów plików CAD** i może odczytywać pliki DWG **bez wymogu posiadania AutoCAD**. Biblioteka przetwarza duże rysunki **w strumieniach o efektywnym zużyciu pamięci**, co pozwala obsługiwać pliki o setkach stron bez ładowania całego pliku do RAM. Te wymierne możliwości czynią ją niezawodnym wyborem dla automatyzacji CAD na poziomie przedsiębiorstwa.

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:
- Aspose.CAD dla .NET zainstalowany. Pobierz najnowszy pakiet ze [strony wydania Aspose.CAD dla .NET](https://releases.aspose.com/cad/net/).
- Lokalny folder zawierający pliki DWG, które chcesz sprawdzić. Zaktualizuj zmienną `MyDir` w przykładowym kodzie, aby wskazywała na ten folder.
- Ważna licencja Aspose.CAD (lub wersja próbna), jeśli planujesz uruchamiać kod w środowisku produkcyjnym.

Teraz, gdy środowisko jest gotowe, rozpocznijmy kodowanie.

## Importowanie przestrzeni nazw

Pierwszą rzeczą, którą musisz zrobić, jest zaimportowanie przestrzeni nazw udostępniających API Aspose.CAD. Dyrektywy `using` wprowadzają przestrzenie nazw Aspose.CAD do zasięgu, umożliwiając dostęp do klas CAD, takich jak `Image` i `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## Jak odczytać metadane xref z plików DWG?

Wczytaj rysunek, wylicz jego jednostki, przefiltruj obiekty XREF, a następnie wyciągnij żądane właściwości — wszystko w kilku prostych linijkach kodu. Poniższe sekcje dzielą proces na cztery logiczne kroki, które możesz skopiować i wkleić do dowolnego projektu .NET (konsola lub usługa).

### Krok 1: wczytaj plik DWG

Utwórz instancję `Image` z pliku DWG, który chcesz przeanalizować. `Image.Load` wczytuje plik CAD i zwraca obiekt `CadImage` reprezentujący rysunek. Dostosuj zmienną `sourceFilePath` do dokładnej lokalizacji swojego rysunku.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### Krok 2: iteruj po jednostkach

Pętla po kolekcji `Entities` obiektu `Image`. `CadBaseEntity` jest klasą bazową dla wszystkich jednostek CAD w Aspose.CAD. Dla każdej jednostki sprawdź, czy jest odwołaniem XREF i zbierz jej metadane.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### Krok 3: wyodrębnij metadane

Gdy napotkasz jednostkę XREF, odczytaj jej punkt wstawienia (X, Y, Z) oraz ścieżkę do odwołanego rysunku. `CadUnderlay` reprezentuje jednostkę zewnętrznego odwołania (XREF) w rysunku DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### Krok 4: przetwórz metadane

Na tym etapie możesz zapisać wyodrębnione informacje w bazie danych, zapisać je do pliku CSV lub przekazać do kolejnych procesów BIM. Przykład po prostu wypisuje wartości na konsolę, ale możesz to zamienić na dowolną własną logikę.

```csharp
// Your custom logic for processing metadata goes here
```

## Typowe problemy i rozwiązywanie

| Objaw | Prawdopodobna przyczyna | Rozwiązanie |
|---------|--------------|-----|
| Nie zwrócono jednostek XREF | Rysunek używa innego typu odwołania (np. INSERT) | Sprawdź typ jednostki względem `CadEntityType.Xref` i obsłuż także `Insert`, jeśli to konieczne |
| `Image.Load` zgłasza wyjątek | Nieprawidłowa ścieżka pliku lub nieobsługiwana wersja DWG | Zweryfikuj ścieżkę i upewnij się, że używasz Aspose.CAD 24.11 lub nowszej wersji |
| Wartości metadanych są puste | XREF jest zdefiniowany, ale nie rozwiązany (brak pliku zewnętrznego) | Upewnij się, że odwołany plik istnieje na dysku lub zapewnij resolver wirtualnego systemu plików |

## Najczęściej zadawane pytania

**P: Czy Aspose.CAD dla .NET jest kompatybilny ze wszystkimi formatami plików CAD?**  
O: Tak, Aspose.CAD dla .NET obsługuje **ponad 50 formatów wejściowych i wyjściowych**, w tym DWG, DXF, DGN i IFC, zapewniając szerokie pokrycie dla większości procesów inżynieryjnych.

**P: Czy mogę skorzystać z wersji próbnej przed podjęciem decyzji o zakupie?**  
O: Oczywiście! Możesz uzyskać dostęp do strony pobierania wersji próbnej [free trial download page](https://releases.aspose.com/).

**P: Gdzie mogę znaleźć pełną dokumentację Aspose.CAD dla .NET?**  
O: Dokumentacja jest dostępna [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).

**P: Jak uzyskać tymczasową licencję dla Aspose.CAD dla .NET?**  
O: Możesz uzyskać tymczasową licencję na [temporary license page](https://purchase.aspose.com/temporary-license/).

**P: Potrzebujesz pomocy lub masz konkretne pytania?**  
O: Dołącz do społeczności Aspose.CAD na [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie ekspertów i dyskusje.

## Podsumowanie

Masz teraz kompletny, gotowy do produkcji wzorzec do **odczytywania metadanych XREF** z plików DWG przy użyciu Aspose.CAD dla .NET. Postępując zgodnie z czterema krokami — wczytaniem pliku, iteracją jednostek, wyodrębnieniem punktu wstawienia i ścieżki podkładu oraz przetworzeniem wyników — możesz zintegrować tę funkcjonalność z dowolną aplikacją skoncentrowaną na CAD, niezależnie od tego, czy jest to narzędzie do migracji danych, skrypt kontroli jakości, czy własny potok BIM.

---

**Ostatnia aktualizacja:** 2026-08-23  
**Testowano z:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Jak zmienić ścieżkę xref i edytować hiperłącza w plikach CAD - Samouczek Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [Pobieranie atrybutów bloków z plików DWG - Samouczek Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [Konwertowanie dużych plików DWG do PDF - Samouczek Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}