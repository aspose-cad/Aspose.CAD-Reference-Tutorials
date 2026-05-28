---
date: 2026-03-02
description: Odkryj potencjał Aspose.CAD dla Javy. Bez wysiłku eksportuj obiekty OLE
  i **zapisz CAD jako PNG**. Pobierz teraz, aby zapewnić płynne zarządzanie danymi
  CAD.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Zapisz CAD jako PNG – Eksportuj obiekty OLE przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz CAD jako PNG – Eksportuj obiekty OLE przy użyciu Aspose.CAD for Java

## Wprowadzenie

W dynamicznym świecie projektowania wspomaganego komputerowo (Computer-Aided Design, CAD) efektywne zarządzanie i wyodrębnianie obiektów OLE (Object Linking and Embedding) — a także możliwość **save CAD as PNG** — jest kluczowe dla dalszych procesów, takich jak raportowanie, podgląd w sieci czy archiwizacja. Aspose.CAD for Java zapewnia potężne rozwiązanie code‑first, które pozwala zarówno eksportować obiekty OLE, jak i konwertować rysunki CAD na wysokiej jakości obrazy PNG w zaledwie kilku linijkach kodu.

## Szybkie odpowiedzi
- **Co robi Aspose.CAD?** Odczytuje, manipuluje i konwertuje pliki CAD (DWG, DXF, DGN itp.) bez konieczności posiadania natywnego oprogramowania CAD.  
- **Czy mogę zapisać CAD jako PNG?** Tak — użyj `PngOptions` razem z `CadRasterizationOptions`, aby rasteryzować dowolny układ.  
- **Jak wyeksportować obiekty OLE?** Załaduj plik CAD przy użyciu `Image.load` i zapisz każdy układ zawierający OLE jako PNG.  
- **Czy potrzebna jest licencja?** Dostępna jest bezpłatna wersja próbna; licencja komercyjna usuwa ograniczenia wersji ewaluacyjnej.  
- **Jakiej wersji Javy wymaga?** Java 8 lub nowsza jest w pełni wspierana.

## Co to jest **save CAD as PNG**?
Zapis CAD jako PNG oznacza rasteryzację wektorowych rysunków CAD do obrazu PNG opartego na pikselach. Ta konwersja jest przydatna, gdy potrzebny jest lekki, uniwersalnie wyświetlany format dla stron internetowych, aplikacji mobilnych lub dokumentacji.

## Dlaczego warto używać Aspose.CAD for Java do **convert CAD to PNG**?
- **Brak wymogu instalacji CAD** – biblioteka działa w pełni w Javie.  
- **Zachowuje wierność układu** – możesz wybrać konkretne układy, kontrolować DPI i zachować jakość linii.  
- **Przetwarzanie wsadowe** – iteruj po wielu plikach przy użyciu prostej pętli.  
- **Eksport obiektów OLE** – zawartość OLE osadzona w plikach DWG/DXF jest automatycznie renderowana w wyjściowym obrazie PNG.

## Wymagania wstępne

Zanim rozpoczniesz tutorial, upewnij się, że spełniasz następujące wymagania wstępne:

- **Środowisko Java** – Upewnij się, że na swoim komputerze masz skonfigurowane środowisko programistyczne Java.  
- **Aspose.CAD for Java** – Pobierz i zainstaluj bibliotekę Aspose.CAD for Java. Bibliotekę znajdziesz pod [download link](https://releases.aspose.com/cad/java/).  
- **Pliki CAD** – Przygotuj pliki CAD zawierające obiekty OLE, które chcesz wyeksportować.

## Importowanie przestrzeni nazw

Aby rozpocząć, zaimportuj niezbędne przestrzenie nazw do swojego projektu Java. Przestrzenie te dostarczają kluczowe klasy i funkcje potrzebne do pracy z plikami CAD przy użyciu Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Teraz rozbijmy proces eksportowania obiektów OLE z CAD na kilka kroków:

## Jak **save CAD as PNG** i wyeksportować obiekty OLE

### Krok 1: Ustaw katalog dokumentów

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Upewnij się, że zamieniłeś `"Your Document Directory"` na ścieżkę do katalogu zawierającego Twoje pliki CAD.

### Krok 2: Zdefiniuj nazwy plików CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Określ nazwy plików CAD, które chcesz przetworzyć w tablicy `files`.

### Krok 3: Ustaw opcje eksportu PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Skonfiguruj opcje eksportu PNG, w tym rasteryzację wektorów i ustawienia układu. Te opcje umożliwiają **convert CAD to PNG** z pożądaną jakością.

### Krok 4: Iteruj po plikach CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iteruj po każdym określonym pliku CAD, załaduj go przy użyciu Aspose.CAD i zapisz obiekty OLE jako obrazy PNG. Ta pętla pokazuje prosty sposób na **convert DWG to PNG** masowo.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| **Pusty obraz PNG** | Niezgodność nazwy układu | Sprawdź, czy nazwa układu (`"Layout1"`) istnieje w źródłowym pliku DWG. |
| **Brak grafiki OLE** | Obiekty OLE są przechowywane w innym układzie | Dołącz wszystkie odpowiednie układy w `rasterizationOptions.setLayouts(...)`. |
| **Błąd braku pamięci przy dużych plikach** | Ustawienia wysokiego DPI | Obniż DPI za pomocą `rasterizationOptions.setResolution(...)` lub przetwarzaj pliki pojedynczo. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?**  
A: Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF i DGN. Zapoznaj się z [documentation](https://reference.aspose.com/cad/java/) po pełną listę.

**Q: Czy mogę dostosować ustawienia eksportu dla obiektów OLE?**  
A: Tak, Aspose.CAD oferuje rozbudowane opcje dostosowywania ustawień eksportu, umożliwiając dopasowanie wyniku do Twoich konkretnych wymagań.

**Q: Czy dostępna jest bezpłatna wersja próbna Aspose.CAD?**  
A: Tak, możesz przetestować możliwości Aspose.CAD, uzyskując bezpłatną wersję próbną z [tutaj](https://releases.aspose.com/).

**Q: Gdzie mogę uzyskać wsparcie społeczności dla Aspose.CAD?**  
A: Dołącz do społeczności Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), aby uzyskać pomoc i podzielić się doświadczeniami.

**Q: Jak mogę kupić licencję na Aspose.CAD?**  
A: Odwiedź [stronę zakupu](https://purchase.aspose.com/buy), aby nabyć licencję odpowiadającą Twoim potrzebom programistycznym.

## Podsumowanie

Dzięki tym prostym, a jednocześnie potężnym krokom, możesz płynnie **save CAD as PNG**, jednocześnie eksportując obiekty OLE z plików CAD przy użyciu Aspose.CAD for Java. To wszechstronne narzędzie umożliwia programistom efektywne zarządzanie danymi CAD, otwierając nowe możliwości w tworzeniu aplikacji CAD oraz w dalszych procesach opartych na obrazach.

---

**Ostatnia aktualizacja:** 2026-03-02  
**Testowano z:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}