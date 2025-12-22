---
date: 2025-12-22
description: Dowiedz się, jak wczytać plik DWG i wyodrębnić informacje o podkładkach
  za pomocą Aspose.CAD dla Javy – krok po kroku przewodnik obejmujący flagi podkładek.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Wczytaj plik DWG i uzyskaj dostęp do flag podkładów – Aspose.CAD for Java
url: /pl/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ładowanie pliku DWG i dostęp do flag podkładki – Aspose.CAD dla Javy

W nowoczesnych przepływach pracy CAD **ładowanie pliku DWG** szybko i wyciąganie szczegółów podkładki jest powszechnym wymaganiem. Niezależnie od tego, czy tworzysz przeglądarkę, automatyzujesz przetwarzanie wsadowe, czy wyodrębniasz metadane do integracji z GIS, Aspose.CAD dla Javy zapewnia czysty, kod‑pierwszy sposób realizacji. W tym samouczku przejdziemy krok po kroku przez **ładowanie pliku DWG**, iterację jego encji oraz odczyt flag podkładki, które wielu programistów pomija.

## Szybkie odpowiedzi
- **Jaka jest podstawowa klasa do otwierania DWG?** `com.aspose.cad.Image.load()` zwraca `CadImage`.
- **Który obiekt przechowuje informacje o podkładce?** `CadUnderlay` (lub jego typy pochodne, takie jak `CadDgnUnderlay`).
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.
- **Czy mogę przetwarzać wiele plików DWG w pętli?** Tak – wystarczy powtarzać wzorzec ładowania‑i‑iteracji.
- **Czy to podejście jest kompatybilne z Java 11+?** Absolutnie, Aspose.CAD obsługuje Java 8 aż po najnowsze wersje LTS.

## Co oznacza „load dwg file” w Aspose.CAD?
`Image.load()` odczytuje binarną zawartość DWG i tworzy w pamięci obiekt `CadImage`. Od tego momentu możesz przeglądać warstwy, bloki i encje podkładki bez konieczności samodzielnego zajmowania się formatem DWG.

## Dlaczego wyodrębniać flagi podkładki z DWG?
Flagi podkładki informują, jak zewnętrzne odniesienie (np. podkładka DGN lub PDF) jest pozycjonowane, skalowane i obracane w rysunku. Znajomość tych wartości pozwala:

- Odtworzyć dokładny układ wizualny w własnej przeglądarce.
- Przekonwertować podkładki na natywne encje CAD do dalszej edycji.
- Generować raporty zawierające metadane podkładki dla zgodności lub dokumentacji.

## Wymagania wstępne
- **Biblioteka Aspose.CAD** – pobierz ze strony [releases](https://releases.aspose.com/cad/java/).
- **Java Development Kit** – JDK 8 lub nowszy.
- **Folder** zawierający pliki DWG, które chcesz analizować. Zastąp `"Your Document Directory"` w kodzie rzeczywistą ścieżką.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog zasobów
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Zdefiniuj, gdzie znajdują się Twoje pliki DWG. Użycie dedykowanego folderu utrzymuje przykład w czystości i przenośności.

### Krok 2: Ładuj plik DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Tutaj **ładowany jest plik dwg** `BlockRefDgn.dwg` do instancji `CadImage`, gotowej do inspekcji.

### Krok 3: Iteruj przez encje DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Pętla przechodzi przez każdą encję – linie, okręgi, bloki i podkładki – aby móc wybrać te, które nas interesują.

### Krok 4: Zidentyfikuj encje CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Tylko obiekty `CadDgnUnderlay` zawierają flagi podkładki, których szukamy, więc filtrujemy właśnie je.

### Krok 5: Uzyskaj dostęp do informacji o podkładce
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Gdy mamy już `CadUnderlay`, możemy odczytać jego ścieżkę, nazwę, punkt wstawienia, obrót, współczynniki skali oraz wyliczenie `UnderlayFlags`, które wskazuje widoczność, przycinanie i inne opcje renderowania.

## Typowe problemy i wskazówki
- **Pusta ścieżka podkładki** – Upewnij się, że DWG rzeczywiście odwołuje się do zewnętrznego pliku; w przeciwnym razie ścieżka będzie pusta.
- **Nieobsługiwany typ podkładki** – Aspose.CAD obecnie obsługuje podkładki DGN; podkładki PDF nie są jeszcze udostępnione w API.
- **Wyjątki licencyjne** – Uruchomienie kodu bez ważnej licencji doda znak wodny do wszelkich eksportowanych obrazów.

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.CAD dla Javy z innymi formatami plików CAD?**  
O: Aspose.CAD koncentruje się głównie na formacie DWG, ale obsługuje także DXF, DWF i inne formaty CAD.

**P: Czy dostępna jest wersja próbna Aspose.CAD dla Javy?**  
O: Tak, funkcje możesz wypróbować za darmo [tutaj](https://releases.aspose.com/).

**P: Jak mogę uzyskać wsparcie lub pomoc w sprawie Aspose.CAD dla Javy?**  
O: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy społeczności i dyskusji.

**P: Czy dostępne są tymczasowe licencje dla Aspose.CAD dla Javy?**  
O: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**P: Gdzie znajdę pełną dokumentację Aspose.CAD dla Javy?**  
O: Zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/java/) dla szczegółowych informacji.

---

**Ostatnia aktualizacja:** 2025-12-22  
**Testowane z:** Aspose.CAD 24.12 dla Javy  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}