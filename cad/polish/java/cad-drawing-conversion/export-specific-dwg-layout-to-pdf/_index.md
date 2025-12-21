---
date: 2025-12-21
description: Naucz się konwertować pliki DWG na PDF, eksportując konkretny układ DWG
  do PDF przy użyciu Aspose.CAD dla Javy. Skorzystaj z tego krok po kroku poradnika
  DWG‑do‑PDF, aby usprawnić swój przepływ pracy CAD.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: Konwertuj DWG na PDF – Eksportuj układ przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PDF – Eksportuj określony układ przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

W dynamicznym świecie Computer‑Aided Design (CAD) **convert DWG to PDF** jest częstym wymaganiem przy udostępnianiu rysunków klientom, wykonawcom lub osobom nietechnicznym. Aspose.CAD for Java ułatwia tę konwersję i pozwala wybrać pojedynczy układ z pliku DWG zawierającego wiele układów. W tym samouczku pokażemy **jak wyeksportować określone układy DWG** do PDF, aby dostarczyć dokładnie to, czego potrzebuje Twój projekt, bez dodatkowych stron czy ręcznego przycinania.

## Szybkie odpowiedzi
- **Co oznacza „convert DWG to PDF”?** Przekształca rysunek DWG w dokument PDF, zachowując dane wektorowe i wierność układu.  
- **Która biblioteka obsługuje konwersję?** Aspose.CAD for Java zapewnia gotowe do użycia API.  
- **Czy potrzebuję licencji do produkcji?** Tak, wymagana jest licencja komercyjna; wersja próbna działa w celach oceny.  
- **Czy mogę wybrać pojedynczy układ?** Oczywiście – ustaw właściwość `Layouts` na nazwę żądanego układu.  
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze są w pełni kompatybilne.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- **Środowisko programistyczne Java** – JDK 8+ oraz ulubione IDE.  
- **Aspose.CAD Library** – Pobierz najnowszy JAR z oficjalnej strony **[tutaj](https://releases.aspose.com/cad/java/)**.  
- **DWG File** – Rysunek zawierający przynajmniej jeden układ (np. *visualization_-_conference_room.dwg*).  

## Dlaczego eksportować określony układ DWG do PDF?

Wiele plików DWG zawiera wiele przestrzeni papieru (układów). Eksport całego pliku może wygenerować obszerny PDF z niechcianymi stronami. Wybranie pojedynczego układu:

- Zmniejsza rozmiar pliku.  
- Skupia uwagę odbiorcy na odpowiedniej kartce rysunku.  
- Zgodny ze standardami dokumentacji projektowej.  

## Przewodnik krok po kroku

### Krok 1: Skonfiguruj środowisko projektu

Utwórz nowy projekt Java (Maven, Gradle lub zwykłe IDE) i dodaj JAR Aspose.CAD do ścieżki klas. Możesz go pobrać **[tutaj](https://releases.aspose.com/cad/java/)**.

### Krok 2: Zaimportuj niezbędne pakiety

Dodaj wymagane przestrzenie nazw Aspose.CAD do swojej klasy Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Krok 3: Załaduj plik DWG

Wskaż plik DWG, który chcesz skonwertować i załaduj go do obiektu `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Krok 4: Skonfiguruj opcje rasteryzacji

Zdefiniuj rozmiar strony oraz, co najważniejsze, układ, który chcesz wyeksportować.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Krok 5: Ustaw opcje eksportu PDF

Połącz ustawienia rasteryzacji z eksporterem PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 6: Eksportuj DWG do PDF

Zapisz wynik jako plik PDF. Wyjście będzie zawierało tylko **Layout1**, co zapewnia czystą operację **convert DWG to PDF**.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Layout not found** | Nazwa układu jest źle napisana lub nie istnieje w pliku DWG. | Użyj `image.getLayoutNames()`, aby wyświetlić dostępne układy, a następnie wybierz właściwy. |
| **Low resolution PDF** | `PageWidth`/`PageHeight` są zbyt małe. | Zwiększ wymiary (np. 2000 × 2000) lub ustaw `rasterizationOptions.setResolution(300);`. |
| **License exception** | Uruchamianie bez ważnej licencji w środowisku nie‑testowym. | Zastosuj licencję Aspose.CAD przed załadowaniem obrazu: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Najczęściej zadawane pytania

**Q1: Czy mogę używać Aspose.CAD for Java z innymi bibliotekami CAD opartymi na Javie?**  
A: Aspose.CAD for Java jest biblioteką samodzielną, ale może być zintegrowana z innymi bibliotekami opartymi na Javie w celu rozszerzenia funkcjonalności.

**Q2: Czy istnieją opcje licencjonowania Aspose.CAD?**  
A: Tak, możesz zapoznać się z opcjami licencjonowania i szczegółami zakupu **[tutaj](https://purchase.aspose.com/buy)**.

**Q3: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?**  
A: Odwiedź **[ten link](https://purchase.aspose.com/temporary-license/)**, aby poprosić o tymczasową licencję.

**Q4: Gdzie mogę znaleźć wsparcie dla Aspose.CAD?**  
A: W razie pytań lub potrzeb pomocy, odwiedź **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**Q5: Czy dostępna jest darmowa wersja próbna Aspose.CAD?**  
A: Tak, możesz uzyskać dostęp do darmowej wersji próbnej **[tutaj](https://releases.aspose.com/)**.

## Zakończenie

Postępując zgodnie z tym **dwg to pdf tutorial**, masz teraz niezawodny sposób na **convert DWG to PDF** przy wyborze pojedynczego układu. To podejście oszczędza miejsce, przyspiesza udostępnianie dokumentów i utrzymuje porządek w Twoim procesie CAD. Śmiało eksperymentuj z różnymi ustawieniami rasteryzacji lub łącz wiele układów w jeden PDF w miarę rozwoju projektu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2025-12-21  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose