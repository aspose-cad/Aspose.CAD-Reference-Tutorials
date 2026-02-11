---
date: 2026-01-20
description: Dowiedz się, jak tworzyć pliki PDF z rysunków CAD i dodawać znak wodny
  do rysunku CAD przy użyciu Aspose.CAD dla Javy. Postępuj zgodnie z naszym przewodnikiem
  krok po kroku, aby uzyskać płynną integrację.
linktitle: Add Watermark
second_title: Aspose.CAD Java API
title: Utwórz PDF z CAD i dodaj znaki wodne – Aspose.CAD dla Javy
url: /pl/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie PDF z CAD i Dodawanie znaków wodnych – Aspose.CAD dla Javy

## Wprowadzenie

W tym obszernym samouczku **utworzysz PDF z rysunków CAD** i dowiesz się **jak dodać znak wodny do rysunku CAD** przy użyciu Aspose.CAD dla Javy. Niezależnie od tego, czy potrzebujesz oznaczyć swoje plić własność intelektualną, czy po prostu opatrzyć projekt etykietą, ten przewodnik poprowadzi Cię przez każdy krok – od konfiguracji środowiska po eksport gotowego PDF‑a.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Dodanie tekstowego znaku wodnego do pliku CAD i wyeksportowanie go jako PDF.  
- **Jakiej biblioteki potrzebujesz?** Aspose.CAD dla Javy ( wystarczy do testów; licencja komercyjna jest wymagana w produkcji.  
- **Jaką wersję Javy obsługuje?ywnego DXF itp.) do przenośnego dokumentu PDF. Powstały PDF zachowuje wizualną wierność oryginalnego rysunku, jednocześnie ułatwiając udostępnianie, drukowanie lub osadzanie w innych procesach.

## Dlaczego dodać znak wodny do rysunku CAD?

- **Ochrona marki:** Wyświetl logo firmy lub poufną informację.  
- **Kontrola wersji:** Oznacz szkice, rewizje lub status „Poufne”.  
- **Zgodność:** Spełnij wymogi branżowe, które wymagają etykietowania dokumentów.

## Wymagania wstępne

Zanim przejdziesz dalej, upewnij się, że masz:

- **Aspose.CAD dla Javy** – pobierz ją [tutaj](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – najnowszy JDK zainstalowany na Twoim komputerze.  

## Importowanie pakietów

W projekcie Java zaimportuj niezbędne przestrzenie nazw Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak tworzyć PDF z CAD ze znakiem wodnym

### Krok 1: Dodaj nowy znak wodny MTEXT

Najpierw tworzymy encję `MTEXT`, która będzie widocznym znakiem wodnym na rysunku.

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

*Wskazówka:* Dostosuj współrzędne w `setInsertionPoint`, aby umieścić znak wodny w najbardziej odpowiednim miejscu.

### Krok 2: Dodaj prostą encję Text (opcjonalnie)

Jeśli wolisz znak wodny w postaci zwykłego tekstu, możesz dodać encję `Text` zamiast `MTEXT`.

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### Krok 3: Eksportuj rysunek CAD do PDF

Po osadzeniu znaku wodnego rasteryzuj rysunek i zapisz go jako plik PDF.

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);
```

`CadRasterizationOptions` pozwala kontrolować rozmiar i układ wyjścia, zapewniając wyraźny znak wodny w finalnym PDF‑ie.

## Typowe problemy i wskazówki

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| Znak wodny nie jest widoczny | Warstwa może być ukryta lub kolor zlewa się z tłem. | Ustaw kontrastowy kolor przy pomocy `watermark.getColor().setValue(Color.RED);` (dodaj po utworzeniu). |
| Tekst jest obcięty | Punkt wstawienia znajduje się poza granicami rysunku. | Sprawdź współrzędne za pomocą `cadImage.getSize()` lub użyj `cadImage.getHeader().getLimits()` do obliczenia bezpiecznych granic. |
| Plik PDF jest duży | Rasteryzacja w bardzo wysokiej rozdzielczości. | Zmniejsz `PageWidth`/`PageHeight` lub włącz wektorową rasteryzację (`rasterizationOptions.setVectorRasterizationOptions(true);`). |

## FAQ

### P1: Czy Aspose.CAD jest kompatybilny ze wszystkimi formatami plików CAD?

O1: Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWT i DWF.

### P2: Czy mogę dostosować wygląd tekstu znaku wodnego?

O2: Tak, masz pełną kontrolę nad wyglądem znaku wodnego, w tym rozmiar, kolor i pozycję tekstu.

### P3: Czy dostępna jest wersja próbna Aspose.CAD dla Javy?

O3: Tak, wersję próbną możesz pobrać [tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.CAD?

O4: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) w celu uzyskania pomocy od społeczności.

### P5: Gdzie znajdę pełną dokumentację Aspose.CAD dla Javy?

O5: Zapoznaj się z [dokumentacją](https://reference.aspose.com/cad/java/) poświęconą szczegółowym informacjom.

**Dodatkowe pytania**

**P: Czy mogę dodać znak wodny w postaci obrazu zamiast tekstu?**  
O: Tak. Użyj `CadImage`, aby zaimportować zewnętrzny obraz i dodać go jako encję rastrową przed eksportem.

**P: Jak zastosować ten sam znak wodny do wielu plików CAD w trybie wsadowym?**  
O: Umieść kod tworzący znak wodny wewnątrz pętli, która wczytuje każdy plik CAD, dodaje encję i zapisuje PDF.

**P: Czy istnieje możliwość zachowania PDF‑a jako wektorowego zamiast rasteryzowanego?**  
O: Ustaw `rasterizationOptions.setVectorRasterizationOptions(true);`, aby zachować dane wektorowe tam, gdzie jest to wspierane.

## Zakończenie

Teraz opanowałeś, jak **twor** oraz **dodawać znak wodny do rysunku CAD** przy użyciu Aspose.CADć markę i udostępniać dopracowane PDF‑y z pełnym przekonaniem.

---

**Ostatnia aktualizacja:** 2026-01-20  
**Testowano z:** Aspose.CAD dla Javy 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}