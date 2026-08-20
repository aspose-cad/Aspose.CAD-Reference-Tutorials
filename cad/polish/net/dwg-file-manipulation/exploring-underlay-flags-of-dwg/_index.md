---
date: 2026-04-09
description: Dowiedz się, jak konwertować pliki DWG na obraz oraz jak odczytywać flagi
  podkładów przy użyciu Aspose.CAD dla .NET w tym przewodniku krok po kroku.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Badanie flag podkładów plików DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konwertuj DWG na obraz – Badanie flag podkładów plików DWG – Poradnik Aspose.CAD
url: /pl/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksploracja flag podkładów plików DWG - Aspose.CAD Samouczek

## Wprowadzenie

Jeśli zagłębiasz się w złożony świat plików CAD, konkretnie plików DWG, i chcesz **konwertować DWG na obraz** oraz odkryć **jak odczytać flagi podkładów**, jesteś we właściwym miejscu. Ten samouczek przeprowadzi Cię krok po kroku przy użyciu potężnej biblioteki Aspose.CAD for .NET, dzięki czemu możesz wyodrębnić informacje o podkładach i renderować rysunek jako obraz z pełnym przekonaniem.

## Szybkie odpowiedzi
- **Co oznacza „konwertować DWG na obraz”?**  
  Oznacza to renderowanie rysunku DWG do formatu rastrowego (PNG, JPEG itp.) przy użyciu Aspose.CAD.
- **Która metoda ujawnia flagi podkładów?**  
  Uzyskaj dostęp do właściwości `Flags` obiektu `CadUnderlay` po załadowaniu pliku DWG.
- **Czy potrzebna jest licencja na Aspose.CAD?**  
  Dostępna jest tymczasowa licencja do oceny; pełna licencja jest wymagana w środowisku produkcyjnym.
- **Jakie wersje .NET są wspierane?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 i nowsze.
- **Czy mogę wyodrębnić geometrię podkładu?**  
  Tak – ścieżka podkładu, punkt wstawienia, skalowanie, rotacja i stany flag są dostępne.

## Co to jest „konwertować DWG na obraz” i dlaczego ma to znaczenie?

Konwersja pliku DWG na obraz pozwala wyświetlać rysunki CAD w przeglądarkach, osadzać je w raportach lub udostępniać interesariuszom, którzy nie mają przeglądarki CAD. Podczas renderowania często trzeba sprawdzić obiekty **podkładów** (np. odwołania DGN), aby upewnić się, że wyświetlają się prawidłowo. Zrozumienie flag podkładów pomaga rozwiązywać problemy z przycinaniem, renderowaniem w monochromie i widocznością przed wygenerowaniem ostatecznego obrazu.

## Wymagania wstępne

- Podstawowa znajomość programowania w C# i .NET.  
- **Aspose.CAD for .NET** library installed. If you don’t have it yet, download it **[here](https://releases.aspose.com/cad/net/)**.  
- Plik DWG do testów – przykładowy plik **„BlockRefDgn.dwg”** jest używany w całym przewodniku.

## Importowanie przestrzeni nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Załaduj plik DWG i skonwertuj do `CadImage`

Najpierw załaduj plik DWG i rzutuj go na `CadImage`. Ten obiekt zapewnia dostęp do wszystkich encji rysunku, w tym podkładów.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Krok 2: Iteracja przez encje

Następnie przeiteruj wszystkie encje w rysunku. To tutaj znajdziesz obiekty podkładów.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Krok 3: Sprawdź typ `CadDgnUnderlay`

Zidentyfikuj encje podkładów, sprawdzając ich typ w czasie wykonywania. Klasa `CadDgnUnderlay` reprezentuje podkłady DGN osadzone w pliku DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Krok 4: Dostęp do flag podkładów

Gdy masz już obiekt `CadDgnUnderlay`, rzutuj go na `CadUnderlay`, aby odczytać jego właściwości i stany flag. Flag określają, czy podkład jest widoczny, przycięty lub renderowany w monochromie.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Co mówi wyjście

- **UnderlayPath / UnderlayName** – miejsce, w którym znajduje się zewnętrzny plik DGN.  
- **InsertionPoint (X, Y)** – współrzędne, w których podkład jest umieszczony w przestrzeni DWG.  
- **RotationAngle** – rotacja zastosowana do podkładu.  
- **ScaleX / ScaleY / ScaleZ** – czynniki skalowania dla każdej osi.  
- **Flags** – wartości logiczne wskazujące widoczność (`UnderlayIsOn`), przycięcie (`ClippingIsOn`) oraz renderowanie w monochromie (`Monochrome`).

## Częste problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|-------|--------|-----|
| Brak wyjścia przy sprawdzaniu flag | Flagi podkładu są domyślnie ustawione na 0, gdy podkład jest wyłączony. | Upewnij się, że DWG rzeczywiście zawiera aktywny podkład lub przełącz widoczność w źródłowym pliku CAD. |
| Wyjątek `Invalid cast` | Encja nie jest typu `CadDgnUnderlay`. | Sprawdź warunek `if (entity is CadDgnUnderlay)` przed rzutowaniem. |
| Renderowanie obrazu nie powodzi się po wyodrębnieniu flag | Podkład może być przycięty lub wyłączony, co prowadzi do pustego obszaru. | Dostosuj flagi (`UnderlayIsOn = true`, `ClippingIsOn = false`) przed renderowaniem ostatecznego obrazu. |

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.CAD for .NET z innymi formatami plików CAD?

A1: Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DGN i inne. Sprawdź dokumentację, aby zobaczyć pełną listę.

### Q2: Czy dostępna jest tymczasowa licencja na Aspose.CAD for .NET?

A2: Tak, możesz uzyskać tymczasową licencję **[tutaj](https://purchase.aspose.com/temporary-license/)**.

### Q3: Gdzie mogę znaleźć wsparcie dla Aspose.CAD for .NET?

A3: Odwiedź forum wsparcia **[tutaj](https://forum.aspose.com/c/cad/19)**, aby uzyskać pomoc.

### Q4: Jak mogę kupić Aspose.CAD for .NET?

A4: Zakup bibliotekę **[tutaj](https://purchase.aspose.com/buy)**.

### Q5: Czy dostępna jest darmowa wersja próbna?

A5: Tak, możesz uzyskać dostęp do wersji próbnej **[tutaj](https://releases.aspose.com/)**.

## Zakończenie

Gratulacje! Pomyślnie nauczyłeś się **konwertować DWG na obraz** oraz opanowałeś **odczytywanie flag podkładów** przy użyciu Aspose.CAD for .NET. Dzięki tej wiedzy możesz:

- Renderować rysunki DWG jako obrazy rastrowe w scenariuszach webowych lub raportowych.  
- Inspekować i manipulować właściwościami podkładów, aby zapewnić prawidłowe wyświetlanie.  
- Debugować problemy z widocznością, przycinaniem i monochromem przed generacją ostatecznego obrazu.

Śmiało eksploruj inne funkcje Aspose.CAD, takie jak zarządzanie warstwami, wyodrębnianie tekstu i konwersja wsadowa, aby dalej rozwijać swoje przepływy automatyzacji CAD.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}