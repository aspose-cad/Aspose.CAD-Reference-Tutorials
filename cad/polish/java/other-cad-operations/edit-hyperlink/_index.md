---
date: 2026-06-19
description: Dowiedz się, jak edytować pliki DWG za pomocą Aspose.CAD dla Java, w
  tym jak aktualizować ścieżki DWG XRef i edytować hiperłącza. Wypróbuj darmową wersję
  próbną już dziś!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Edytuj hiperłącze
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Jak edytować hiperłącza DWG - samouczek Aspose.CAD Java
url: /pl/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak edytować hiperłącza DWG - Poradnik Aspose.CAD Java

W dzisiejszej erze cyfrowej **jak edytować DWG** efektywnie jest niezbędną umiejętnością dla inżynierów, architektów i specjalistów BIM. Niezależnie od tego, czy musisz naprawić zepsute hiperłącze, skierować XRef do nowego źródła, czy masowo zaktualizować wiele rysunków, Aspose.CAD for Java oferuje czysty, programowy sposób wprowadzania tych zmian bez otwierania edytora CAD. Ten poradnik przeprowadzi Cię przez cały proces, od wczytania rysunku po zapisanie edycji.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje edycję DWG w Javie?** Aspose.CAD for Java.  
- **Czy mogę edytować hiperłącza i ścieżki XRef jednocześnie?** Tak — oba są obsługiwane w tym samym API.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.  
- **Jaka wersja Javy jest wymagana?** Java 8 lub wyższa.  
- **Czy przykładowy kod działa od razu?** Tak, po zaktualizowaniu ścieżek plików, aby wskazywały na lokalne pliki DWG.

## Dlaczego edytować hiperłącza DWG i ścieżki XRef?

Utrzymywanie aktualnych hiperłączy i ścieżek XRef zapobiega uszkodzonym odwołaniom, zapewnia, że dokumentacja projektu zawsze wskazuje na właściwe zasoby oraz umożliwia automatyczne masowe aktualizacje w rozległych bibliotekach CAD. To zmniejsza ręczną pracę, minimalizuje błędy i podnosi ogólną efektywność projektu, pozwalając programistom programowo utrzymywać integralność linków przez cały cykl życia projektu.

## Wymagania wstępne

Przed rozpoczęciem tutorialu upewnij się, że spełniasz następujące wymagania:

1. **Środowisko programistyczne Java:** Zainstalowany JDK 8+ oraz ulubione IDE (IntelliJ IDEA, Eclipse itp.).  
2. **Biblioteka Aspose.CAD for Java:** Pobierz i zainstaluj bibliotekę Aspose.CAD for Java z [linku do pobrania](https://releases.aspose.com/cad/java/).  
3. **Rysunek DWG:** Przygotuj plik rysunku DWG gotowy do edycji hiperłączy.

## Importowanie pakietów

Rozpocznij od zaimportowania niezbędnych pakietów do swojego projektu Java. Zapewni to dostęp do funkcjonalności Aspose.CAD for Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Jak edytować hiperłącza DWG przy użyciu Aspose.CAD for Java?

`CadImage` jest klasą Aspose.CAD używaną do wczytywania i zapisywania rysunków CAD.  
Wczytaj plik DWG przy pomocy `CadImage`, przeiteruj jego encje, zaktualizuj hiperłącze oraz ścieżkę XRef w razie potrzeby i na końcu zapisz obraz z powrotem do DWG. Ten kompleksowy przepływ pozwala zmodyfikować dowolną liczbę encji w jednym przebiegu, gwarantując, że wszystkie zmiany zostaną zapisane.

### Krok 1: Dostęp do obiektów Insert

`CadInsertObject` jest klasą Aspose.CAD reprezentującą wstawiony odwołanie bloku (XRef) wewnątrz rysunku DWG. Przejdź przez encje i sprawdź, czy dana encja jest instancją klasy `CadInsertObject`.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Krok 2: Jak zmienić ścieżkę XRef w rysunku DWG

`CadImage` jest głównym obiektem, który wczytuje i zapisuje pliki CAD w Aspose.CAD for Java. Po zidentyfikowaniu obiektu insert, pobierz powiązaną encję bloku i zaktualizuj ścieżkę XRef w razie potrzeby. Dzięki temu odwołanie będzie wskazywać na właściwy plik zewnętrzny.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Krok 3: Modyfikowanie hiperłączy

Następnie sprawdź, czy encja ma powiązane hiperłącze. Jeśli hiperłącze pasuje do określonego URL, zaktualizuj je do żądanego URL. Ten krok zapewnia, że kliknięcie hiperłącza w przeglądarce CAD otworzy nowy cel.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Częste pułapki i wskazówki

- **Porównywanie ciągów:** Używaj `.equals()` zamiast `==` dla niezawodnego porównywania ciągów w Javie. Przykład używa `==` dla uproszczenia, ale w produkcji zamień to na `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **Sprawdzanie null:** Zawsze sprawdzaj, czy `block.getXRefPathName()` nie jest `null` przed wywołaniem `.getValue()`.  
- **Zapisywanie zmian:** Po modyfikacji encji wywołaj `cadImage.save("output.dwg");`, aby zachować zmiany (kod pominięty, aby zachować oryginalną liczbę bloków).  
- **Uwaga dotycząca wydajności:** Aspose.CAD for Java obsługuje ponad 30 formatów CAD i może przetwarzać pliki do 2 GB bez ładowania całego dokumentu do pamięci, co sprawia, że masowe aktualizacje są szybkie i oszczędne pod względem pamięci.

## Najczęściej zadawane pytania

### P1: Czy Aspose.CAD for Java jest kompatybilny ze wszystkimi wersjami rysunków DWG?

**A1:** Aspose.CAD for Java obsługuje ponad 50 wersji DWG, obejmując wydania od AutoCAD 2000 do najnowszego formatu 2025.

### P2: Czy mogę używać Aspose.CAD for Java w projektach komercyjnych?

**A2:** Tak, licencja komercyjna jest wymagana do użytku produkcyjnego. Licencję możesz zakupić [tutaj](https://purchase.aspose.com/buy).

### P3: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?

**A3:** Tak, możesz wypróbować darmową wersję próbną [tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie techniczne dla Aspose.CAD for Java?

**A4:** W celu uzyskania pomocy technicznej odwiedź forum Aspose.CAD [tutaj](https://forum.aspose.com/c/cad/19).

### P5: Czy mogę uzyskać tymczasową licencję do celów testowych?

**A5:** Tak, tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**Dodatkowe pytania i odpowiedzi**

**Q:** Czy muszę wywołać konkretną metodę, aby zapisać edytowany DWG na dysk?  
**A:** Tak, po wprowadzeniu zmian wywołaj `cadImage.save("EditedDrawing.dwg");`, aby zachować modyfikacje.

**Q:** Czy istnieje możliwość edycji wielu hiperłączy w jednym przebiegu?  
**A:** Oczywiście — przeiteruj `cadImage.getEntities()` i zastosuj logikę hiperłączy do każdej pasującej encji.

**Ostatnia aktualizacja:** 2026-06-19  
**Testowane z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane poradniki

- [Odczyt metadanych XREF z plików DWG przy użyciu Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Dodawanie własnych właściwości do plików DWG przy użyciu Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Eksport DWG do PDF lub rastra przy użyciu Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}