---
date: 2026-01-12
description: Dowiedz się, jak wyeksportować CAD do PDF, pomijając automatyczne wykrywanie
  strony kodowej w plikach DWG przy użyciu Aspose.CAD for Java. Obsługuje kodowanie
  oraz nieprawidłowe pliki CIF/MIF.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Eksport CAD do PDF – Zastąp automatyczne wykrywanie strony kodowej w plikach
  DWG przy użyciu Javy
url: /pl/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksport CAD do PDF – Zastąpienie automatycznego wykrywania strony kodowej w plikach DWG przy użyciu Java

## Wprowadzenie

W tym obszernym przewodniku odkryjesz **jak wyeksportować CAD do PDF**, jednocześnie zastępując automatyczne wykrywanie strony kodowej, które może uszkadzać tekst w plikach DWG. Aspose.CAD for Java daje Ci precyzyjną kontrolę nad kodowaniem, umożliwiając odzyskanie uszkodzonych danych CIF/MIF i generowanie niezawodnego wyjścia PDF. Niezależnie od tego, czy tworzysz konwerter wsadowy, czy integrujesz przetwarzanie CAD w większej aplikacji Java, poniższe kroki przeprowadzą Cię przez cały proces.

## Szybkie odpowiedzi
- **Co oznacza „override code page”?** Wymusza, aby Aspose.CAD używało określonego kodowania znaków zamiast zgadywać.
- **Czy mogę wyeksportować DWG bezpośrednio do PDF?** Tak – po ustawieniu właściwej strony kodowej możesz zapisać obraz CAD jako PDF.
- **Jakie kodowanie działa dla tekstu japońskiego?** `CodePages.Japanese` i `MifCodePages.Japanese` są właściwymi wyborami.
- **Czy potrzebna jest licencja do użytku produkcyjnego?** Wymagana jest licencja komercyjna; tymczasowa licencja jest dostępna do testów.
- **Jakiej wersji Aspose.CAD potrzebuję?** Dowolna aktualna wersja obsługująca `LoadOptions` i `PdfOptions`.

## Co to jest „eksport CAD do PDF”?
Eksportowanie CAD do PDF konwertuje wektorowe rysunki CAD na powszechnie obsługiwany format dokumentu o stałym układzie. Powstały plik PDF zachowuje linie, warstwy i tekst, jednocześnie ułatwiając udostępnianie, drukowanie lub osadzanie rysunku w innych aplikacjach.

## Dlaczego zastąpić automatyczne wykrywanie strony kodowej?
Pliki DWG często przechowują tekst przy użyciu starszych stron kodowych. Automatyczne wykrywanie Aspose.CAD może błędnie interpretować te bajty, prowadząc do zniekształconych znaków. Ręczne określenie strony kodowej zapewnia, że tekst będzie wyświetlany dokładnie tak, jak zamierzono w wyeksportowanym PDF, szczególnie w przypadku skryptów nielatynowych, takich jak japoński, cyrylica czy arabski.

## Wymagania wstępne
- **Środowisko programistyczne Java** – JDK 8+ oraz ulubione IDE.
- **Aspose.CAD for Java** – Pobierz bibliotekę z oficjalnej strony [here](https://releases.aspose.com/cad/java/).
- **Przykładowy plik DWG** – Użyj dostarczonego `SimpleEntities.dwg` lub dowolnego pliku DWG, który chcesz skonwertować.

## Importowanie pakietów
W swoim projekcie Java zaimportuj niezbędne klasy Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Przewodnik krok po kroku

### Krok 1: Konfiguracja projektu Java
Utwórz nowy projekt Maven lub Gradle i dodaj plik JAR Aspose.CAD do ścieżki klas. Ten krok zapewnia, że IDE może rozwiązać zaimportowane klasy.

### Krok 2: Wczytaj plik DWG z określoną stroną kodową
Powiedz Aspose.CAD, którego kodowania użyć i czy próbować odzyskać uszkodzone dane CIF/MIF.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Krok 3: Eksportuj obraz CAD do PDF
Po zastosowaniu właściwej strony kodowej możesz bezpiecznie wyeksportować rysunek. Obiekt `PdfOptions` pozwala precyzyjnie dostosować wyjście PDF (kompresja, rasteryzacja itp.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Krok 4: Zweryfikuj powodzenie
Prosta wiadomość w konsoli potwierdza, że proces zakończył się bez wyjątków.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Możesz powtórzyć te kroki dla wielu plików DWG, dostosowując ścieżkę źródłową i nazwę wyjściową w razie potrzeby.

## Typowe problemy i rozwiązania
- **Wciąż pojawiają się nieczytelne znaki:** Sprawdź, czy `specifiedEncoding` odpowiada oryginalnej stronie kodowej DWG. W razie potrzeby użyj innego wyliczenia `CodePages`.
- **`NullPointerException` przy `cadImage.save`:** Upewnij się, że plik DWG został poprawnie wczytany; sprawdź ścieżkę i uprawnienia do pliku.
- **Rozmiar PDF jest duży:** Włącz kompresję w `PdfOptions` (np. `pdfOptions.setCompress(true)`).

## Najczęściej zadawane pytania

**Q1: Czy Aspose.CAD jest kompatybilny ze wszystkimi wersjami plików DWG?**  
A1: Aspose.CAD obsługuje szeroki zakres wersji DWG, w tym AutoCAD 2018 i wcześniejsze wydania.

**Q2: Czy mogę używać Aspose.CAD w projektach komercyjnych?**  
A2: Tak, wymagana jest licencja komercyjna do użytku produkcyjnego. Licencję można uzyskać [here](https://purchase.aspose.com/buy).

**Q3: Czy w wersji próbnej istnieją ograniczenia?**  
A3: Wersja próbna nakłada ograniczenia rozmiaru i funkcji; zapoznaj się z oficjalną dokumentacją, aby uzyskać szczegóły.

**Q4: Jak mogę uzyskać wsparcie dla Aspose.CAD?**  
A4: Odwiedź społeczność [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy i dyskusji.

**Q5: Czy dostępna jest tymczasowa licencja do celów testowych?**  
A5: Tak, tymczasową licencję można zamówić [here](https://purchase.aspose.com/temporary-license/).

**Ostatnia aktualizacja:** 2026-01-12  
**Testowano z:** Aspose.CAD for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}