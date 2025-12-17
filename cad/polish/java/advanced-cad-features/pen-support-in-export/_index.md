---
date: 2025-12-10
description: Naucz się, jak tworzyć pliki PDF z CAD przy użyciu Aspose.CAD dla Javy,
  dostosowując pióro. Ten krok‑po‑kroku przewodnik pokazuje, jak efektywnie eksportować
  CAD do PDF.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Jak utworzyć PDF z CAD z obsługą pióra przy eksporcie
url: /pl/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obsługa pióra przy eksporcie

## Wprowadzenie

W szybko zmieniającym się świecie konwersji CAD programiści często muszą **tworzyć PDF z plików CAD**, zachowując wysoką jakość wizualną. Aspose.CAD for Java upraszcza to zadanie, oferując bogate opcje, takie jak dostosowywanie pióra, które pozwalają precyzyjnie regulować style linii podczas procesu eksportu. W tym przewodniku przeprowadzimy kompletny, praktyczny przykład pokazujący, jak **wyeksportować CAD do PDF** z własnymi ustawieniami pióra, abyś mógł generować eleganckie pliki PDF bezpośrednio z rysunków DXF.

## Szybkie odpowiedzi
- **Co oznacza „tworzyć PDF z CAD”?** Konwersja rysunku CAD (np. DXF) do dokumentu PDF przy zachowaniu jakości wektorowej.  
- **Która biblioteka obsługuje dostosowywanie pióra?** Klasa `PenOptions` w Aspose.CAD for Java.  
- **Czy mogę używać tego dla innych formatów?** Tak – te same ustawienia pióra działają dla PNG, BMP, TIFF itp.  
- **Czy potrzebna jest licencja?** Do użytku produkcyjnego wymagana jest ważna licencja Aspose.CAD.  
- **Jaka jest minimalna wersja Javy?** Java 8 lub nowsza.

## Co oznacza „tworzyć PDF z CAD”?
Tworzenie PDF z CAD oznacza rasteryzację lub renderowanie wektorowe rysunku CAD do pliku PDF. Umożliwia to łatwe udostępnianie, drukowanie i archiwizację projektów inżynieryjnych bez konieczności posiadania oprogramowania CAD po stronie odbiorcy.

## Dlaczego warto używać obsługi pióra przy eksporcie CAD do PDF?
Obsługa pióra pozwala kontrolować zakończenia linii, połączenia i grubość, dając możliwość dopasowania do identyfikacji wizualnej firmy lub standardów rysunków technicznych. Jest to szczególnie przydatne, gdy domyślne renderowanie linii nie spełnia Twoich wymagań wizualnych.

## Wymagania wstępne

- **Środowisko programistyczne Java** – działające JDK (8 lub nowsze) oraz wybrane IDE lub narzędzie do budowania.  
- **Biblioteka Aspose.CAD** – pobierz najnowszy plik JAR z oficjalnej strony [tutaj](https://releases.aspose.com/cad/java/).  
- **Przykładowy plik DXF** – w tym samouczku użyjemy `conic_pyramid.dxf`.

Teraz, gdy wszystko jest gotowe, przejdźmy do kodu.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Krok 1: Zdefiniuj katalog dokumentów

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Wskazówka:** Zamień `"Your Document Directory"` na pełną ścieżkę, w której znajdują się Twoje pliki DXF.

## Krok 2: Załaduj plik CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Metoda `Image.load` odczytuje plik DXF i tworzy obiekt `CadImage`, którym możemy dalej manipulować.

## Krok 3: Skonfiguruj opcje rasteryzacji

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Dostosuj wymiary strony, aby kontrolować rozdzielczość wynikowego PDF. Mnożenie przez 100 daje wysokiej rozdzielczości wyjście odpowiednie do druku.

## Krok 4: Dostosuj opcje pióra

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Tutaj ustawiamy zarówno początkowe, jak i końcowe zakończenia pióra na `Flat`. Możesz eksperymentować z innymi wartościami `LineCap` (np. `Round`, `Square`), aby uzyskać różne efekty wizualne.

## Krok 5: Skonfiguruj opcje eksportu PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Obiekt `PdfOptions` łączy ustawienia rasteryzacji z procesem eksportu do PDF.

## Krok 6: Zapisz wyeksportowany PDF

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Uruchomienie tej linii zapisuje plik PDF o nazwie `9LHATT-A56_generated.pdf` w folderze `dataDir`, zawierający niestandardowe stylizacje pióra, które zdefiniowałeś.

## Typowe przypadki użycia

- **Dokumentacja techniczna** – wstaw precyzyjne rysunki inżynieryjne do podręczników PDF.  
- **Automatyczne raportowanie** – generuj PDF-y z danych CAD w locie w usługach internetowych.  
- **Kontrola jakości** – zastosuj niestandardowe zakończenia linii, aby podkreślić linie pomiarowe lub tolerancje.

## Rozwiązywanie problemów i wskazówki

- **Nieprawidłowa ścieżka pliku** – upewnij się, że `dataDir` kończy się separatorem plików (`/` lub `\\`).  
- **Brak licencji** – bez ważnej licencji biblioteka działa w trybie ewaluacyjnym, co może dodawać znaki wodne.  
- **Nieoczekiwane style linii** – sprawdź, czy `PenOptions` zostały ustawione przed wywołaniem `save`; w przeciwnym razie użyte zostaną ustawienia domyślne.

## Najczęściej zadawane pytania

### Q1: Czy mogę dostosować opcje pióra dla formatów innych niż PDF?

A1: Tak, prezentowane w tym samouczku dostosowanie pióra ma zastosowanie do różnych formatów obrazów, w tym PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF i WMF.

### Q2: Jak obsłużyć różne zakończenia początkowe i końcowe dla piór?

A2: Skorzystaj z klasy `PenOptions`, aby ustawić pożądane zakończenia początkowe i końcowe, co daje elastyczność w definiowaniu wyglądu linii.

### Q3: Co się stanie, jeśli nie określę opcji pióra?

A3: Jeśli opcje pióra nie zostaną wyraźnie ustawione, system użyje domyślnych piór, które mogą się różnić w zależności od kontekstu.

### Q4: Czy są szczególne uwagi dotyczące opcji rasteryzacji?

A4: Dostosuj szerokość i wysokość strony w opcjach rasteryzacji, aby kontrolować wymiary eksportowanego obrazu.

### Q5: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społeczności?

A5: Odwiedź forum społeczności Aspose.CAD pod adresem [here](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i uczestniczyć w dyskusjach.

---

**Ostatnia aktualizacja:** 2025-12-10  
**Testowane z:** Aspose.CAD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}