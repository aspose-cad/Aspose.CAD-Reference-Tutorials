---
date: 2025-12-28
description: Dowiedz się, jak odczytywać pliki DWG przy użyciu Aspose.CAD dla Javy
  i bez wysiłku wyświetlać układy w plikach DWG. Zintegruj potężną funkcjonalność
  CAD w swoich aplikacjach Java.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Jak odczytać plik DWG i wyświetlić układy w DWG przy użyciu Aspose.CAD dla
  Javy
url: /pl/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak odczytać pliki DWG i wyświetlić układy w DWG przy użyciu Aspose.CAD dla Java

## Wprowadzenie

Jeśli potrzebujesz **odczytywać pliki DWG** programowo i wyodrębniać informacje takie jak nazwy układów, Aspose.CAD dla Java ułatwia to zadanie. W tym samouczku krok po kroku pokażemy Ci **jak odczytać DWG** i wyświetlić wszystkie układy zawarte w pliku DWG (lub DXF). Po zakończeniu przewodnika będziesz mógł dodać tę funkcjonalność do dowolnej aplikacji Java pracującej z danymi CAD.

## Szybkie odpowiedzi
- **Jaka biblioteka jest wymagana?** Aspose.CAD for Java.
- **Czy mogę odczytywać pliki DWG na dowolnym systemie operacyjnym?** Tak – Java jest wieloplatformowa.
- **Czy potrzebuję licencji, aby uruchomić przykład?** Darmowa wersja próbna działa w celach ewaluacyjnych; licencja jest wymagana w produkcji.
- **Jakie formaty CAD są obsługiwane?** DWG, DXF, DWF i inne.
- **Czy kod jest kompatybilny z Java 8+?** Absolutnie.

## Co oznacza „jak odczytać dwg” w Javie?

Odczytanie pliku DWG oznacza załadowanie binarnych danych CAD do modelu obiektowego, który można przeszukiwać. Aspose.CAD ukrywa złożoną strukturę DWG za prostymi klasami .NET/Java, umożliwiając skupienie się na potrzebnych informacjach – w tym przypadku na nazwach układów.

## Dlaczego wyświetlać układy w pliku DWG?

Plik DWG może zawierać wiele układów (paper space, model space, niestandardowe arkusze). Znajomość nazw układów pozwala:
- Generować raporty dla każdego układu.
- Eksportować wybrane układy do obrazów lub PDF‑ów.
- Automatyzować przetwarzanie wsadowe rysunków.

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:

- **Aspose.CAD for Java Library** – pobierz najnowszy plik JAR ze [strony internetowej](https://releases.aspose.com/cad/java/).
- **Java Development Environment** – JDK 8 lub wyższy oraz wybrane IDE lub narzędzie do budowania.

## Importowanie przestrzeni nazw

W swoim pliku źródłowym Java zaimportuj wymagane klasy Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Krok 1: Skonfiguruj katalog dokumentów

Zastąp **„Your Document Directory”** bezwzględną ścieżką do katalogu, w którym znajdują się Twoje pliki CAD.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## Krok 2: Załaduj plik DWG

Metoda `Image.load` automatycznie wykrywa format pliku, więc możesz używać tego samego kodu zarówno dla plików **DWG**, jak i **DXF**.

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

## Krok 3: Pobierz układy i wypisz ich nazwy

Pętla iteruje po każdym obiekcie układu i wypisuje jego nazwę w konsoli – prosty sposób, aby zweryfikować, że udało Ci się **odczytać DWG** i wyodrębnić informacje o układach.

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

## Typowe pułapki i wskazówki

- **Nieprawidłowa ścieżka do pliku** – Sprawdź, czy `dataDir` kończy się separatorem (`/` lub `\\`) odpowiednim dla Twojego systemu operacyjnego.
- **Nieobsługiwana wersja DWG** – Upewnij się, że używasz najnowszej wersji Aspose.CAD; starsze wersje DWG mogą wymagać konwersji.
- **Zużycie pamięci** – Duże rysunki mogą zajmować znaczną ilość pamięci. Zwolnij obiekt `CadImage` po zakończeniu: `cadImage.dispose();`.

## Podsumowanie

Gratulacje! Teraz wiesz **jak odczytać DWG** i wyświetlić jego układy przy użyciu Aspose.CAD dla Java. Ta technika stanowi podstawę bardziej zaawansowanej automatyzacji CAD, takiej jak eksport wybranych układów do obrazów lub PDF‑ów. Aby zgłębić temat, zapoznaj się z oficjalną [dokumentacją](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Czy mogę używać Aspose.CAD dla Java z innymi formatami plików CAD?

A1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne.

### Q2: Czy dostępna jest darmowa wersja próbna Aspose.CAD dla Java?

A2: Tak, możesz uzyskać darmową wersję próbną [tutaj](https://releases.aspose.com/).

### Q3: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD dla Java?

A3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) aby uzyskać wsparcie społeczności.

### Q4: Jak mogę zakupić licencję na Aspose.CAD dla Java?

A4: Licencję możesz kupić na [stronie zakupu](https://purchase.aspose.com/buy).

### Q5: Czy mogę używać tymczasowej licencji do celów testowych?

A5: Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**Dodatkowe pytania**

**Q: Czy to podejście działa przy odczytywaniu plików DWG na Linuksie?**  
A: Absolutnie. Ponieważ rozwiązanie jest czystą Javą, działa na każdym systemie operacyjnym z kompatybilnym JDK.

**Q: Czy mogę odczytać plik DWG bez ładowania całego rysunku do pamięci?**  
A: Aspose.CAD ładuje rysunek do pamięci; w przypadku bardzo dużych plików rozważ przetwarzanie ich w osobnych wątkach lub użycie API strumieniowego, jeśli będzie dostępne w przyszłych wersjach.

**Q: Czy istnieje sposób na filtrowanie układów po nazwie?**  
A: Tak – po pobraniu `CadLayoutDictionary` możesz sprawdzić `layout.getLayoutName().equalsIgnoreCase("MyLayout")` przed przetworzeniem.

---

**Ostatnia aktualizacja:** 2025-12-28  
**Testowano z:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}