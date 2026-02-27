---
date: 2026-01-17
description: Dowiedz się, jak włączyć obsługę siatek dla plików DWG i konwertować
  DWG na PDF w Javie przy użyciu Aspose.CAD. Przewodnik krok po kroku umożliwiający
  płynną manipulację rysunkami 3D.
linktitle: Convert DWG to PDF with Mesh Support in Java
second_title: Aspose.CAD Java API
title: Konwertuj DWG na PDF z obsługą siatek w Javie
url: /pl/java/dwg-file-operations/mesh-support-for-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj DWG do PDF z obsługą siatek w Javie

## Wprowadzenie

Praca z plikami DWG w Javie często oznacza, że musisz **convert DWG to PDF** zachowując złożoną geometrię 3‑D. Włączenie obsługi siatek jest kluczowym krokiem, ponieważ zapewnia prawidłową interpretację jednostek 3‑D, takich jak PolyFaceMesh i PolygonMesh, przed konwersją. W tym samouczku przeprowadzimy Cię przez włączanie obsługi siatek przy użyciu Aspose.CAD for Java i pokażemy, jak to przygotowanie sprawia, że późniejsza operacja *convert DWG to PDF* jest niezawodna i dokładna.

## Szybkie odpowiedzi
- **Czy mogę bezpośrednio konwertować DWG do PDF?** Tak, po włączeniu obsługi siatek możesz rasteryzować lub wyeksportować DWG do PDF.
- **Czy potrzebna jest licencja na Aspose.CAD?** Darmowa wersja próbna działa w celach oceny; licencja komercyjna jest wymagana w produkcji.
- **Jaka wersja Javy jest wymagana?** Java 8 lub nowsza.
- **Czy jednostki siatek będą zachowane w PDF?** Włączenie obsługi siatek zapewnia przetworzenie wierzchołków, więc PDF odzwierciedla oryginalną geometrię 3‑D.
- **Czy potrzebna jest dodatkowa konfiguracja?** Tylko standardowa konfiguracja Aspose.CAD i prawidłowe zwalnianie zasobów.

## Czym jest obsługa siatek dla DWG?

Obsługa siatek pozwala Aspose.CAD rozpoznawać i obsługiwać jednostki oparte na siatkach (PolyFaceMesh i PolygonMesh), które definiują powierzchnie 3‑D. Bez tej obsługi jednostki te mogą być pomijane lub renderowane niepoprawnie, gdy później **convert DWG to PDF**.

## Dlaczego włączyć obsługę siatek przed konwersją DWG do PDF?

- **Dokładna reprezentacja 3‑D** – Wierzchołki siatek są zachowane, więc PDF pokazuje zamierzoną geometrię.
- **Zmniejszone post‑przetwarzanie** – Mniej ręcznych poprawek po konwersji.
- **Lepsza wydajność** – Aspose.CAD przetwarza siatki efektywnie, gdy są wyraźnie włączone.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

- Zainstalowany Java Development Kit (JDK).
- Bibliotekę Aspose.CAD for Java pobraną i dodaną do projektu. Bibliotekę znajdziesz [tutaj](https://releases.aspose.com/cad/java/).
- Podstawową znajomość programowania w Javie.

## Importowanie pakietów

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. Pakiety te zapewnią dostęp do funkcjonalności Aspose.CAD for Java.

```java
import com.aspose.cad.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import java.awt.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.polylines.CadPolyFaceMesh;
import com.aspose.cad.fileformats.cad.cadobjects.polylines.CadPolygonMesh;
import java.util.ArrayList;
import java.util.List;
```

## Krok 1: Załaduj plik DWG

Załaduj plik DWG przy użyciu Aspose.CAD for Java. Upewnij się, że podana ścieżka do pliku jest prawidłowa i że plik istnieje.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "meshes.dwg";
// com.aspose.cad. objImage = com.aspose.cad.CImage.load(srcFile);
CadImage cadImage =(CadImage) com.aspose.cad.Image.load(srcFile);;
```

## Krok 2: Iteruj przez jednostki

Iteruj przez jednostki w załadowanym pliku DWG. Aspose.CAD udostępnia różnorodne klasy jednostek reprezentujące różne elementy CAD.

```java
for (CadBaseEntity entity : cadImage.getEntities())
{
    // Check if the entity is a PolyFaceMesh
    if (entity instanceof CadPolyFaceMesh)
    {
        CadPolyFaceMesh asFaceMesh = (CadPolyFaceMesh)entity;
        if (asFaceMesh != null)
        {
            System.out.println("Vertices count: " + asFaceMesh.getMeshMVertexCount());
        }
    }
    // Check if the entity is a PolygonMesh
    else if (entity instanceof CadPolygonMesh)
    {
        CadPolygonMesh asPolygonMesh = (CadPolygonMesh)entity;
        if (asPolygonMesh != null)
        {
            System.out.println("Vertices count: " + asPolygonMesh.getMeshMVertexCount());
        }
    }
}
```

## Krok 3: Zwolnij zasoby

Zadbaj o prawidłowe zarządzanie zasobami, zwalniając obiekt CadImage po użyciu.

```java
finally
{
    cadImage.dispose();
}
```

## Jak konwertować DWG do PDF po włączeniu obsługi siatek

Po włączeniu obsługi siatek i zweryfikowaniu jednostek siatek, konwersja DWG do PDF jest prosta:

1. **Skonfiguruj opcje rasteryzacji** (np. rozmiar strony, kolor tła).  
2. **Utwórz instancję `PdfOptions`** i przypisz ustawienia rasteryzacji.  
3. **Wywołaj `cadImage.save(outputPath, pdfOptions)`**, aby wygenerować PDF.

*Uwaga:* Faktyczny kod konwersji został pominięty, aby skupić się na obsłudze siatek, ale powyższe kroki ilustrują, gdzie konwersja wpasowuje się w przepływ pracy.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| Brak wydrukowanych wierzchołków | Jednostki siatek nie rozpoznane | Upewnij się, że używasz najnowszej wersji Aspose.CAD i żeik DWG rzeczywiście zawiera dane siatek. |
| `cadImage` is null | Nieprawidłowa ścieżka pliku | Sprawdź, czy `srcFile` wskazuje prawidłowy plik DWG. |
| W wyniku PDF nie zawiera danych 3‑D | Obsługa siatek nie została włączona | Postępuj zgodnie z powyższymi krokami, aby iterować i potwierdzić jednostki siatek przed konwersją. |

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.CAD for Java z innymi formatami plików CAD?**  
A: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DGN i inne.

**Q: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD for Java?**  
A: Dokumentację znajdziesz [tutaj](https://reference.aspose.com/cad/java/).

**Q: Czy dostępna jest darmowa wersja próbna Aspose.CAD for Java?**  
A: Tak, darmową wersję próbną znajdziesz [tutaj](https://releases.aspose.com/).

**Q: Jak mogę uzyskać tymczasową licencję na Aspose.CAD for Java?**  
A: Tymczasową licencję można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**Q: Potrzebujesz pomocy lub masz pytania?**  
A: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) aby uzyskać wsparcie.

---

**Ostatnia aktualizacja:** 2026-01-17  
**Testowano z:** Aspose.CAD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}