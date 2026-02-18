---
date: 2026-01-07
description: Dowiedz się, jak eksportować CAD do SVG przy użyciu Aspose.CAD dla Javy.
  Ten przewodnik krok po kroku pokazuje, jak konwertować DWG na SVG, ustawiać tryb
  kolorów SVG oraz integrować bibliotekę w swoim projekcie Java.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Eksport CAD do SVG przy użyciu Aspose.CAD dla Javy
url: /pl/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportowanie CAD do SVG przy użyciu Aspose.CAD dla Javy

## Wprowadzenie

Witamy w świecie Aspose.CAD dla Javy, potężnej biblioteki, która umożliwia programistom łatwe manipulowanie rysunkami CAD. Niezależnie od tego, czy jesteś doświadczonym programistą, czy nowicjuszem w dziedzinie CAD, ten kompleksowy przewodnik poprowadzi Cię krok po kroku przez **eksport CAD do SVG**, pokazując, jak konwertować DWG na SVG, ustawiać tryb kolorów SVG oraz integrować API w swoim projekcie Java.

## Szybkie odpowiedzi
- **Co oznacza „eksport CAD do SVG”?** Konwertuje rysunek CAD (np. DWG) do pliku Scalable Vector Graphics, który może być wyświetlany w przeglądarkach.  
- **Która biblioteka obsługuje konwersję?** Aspose.CAD dla Javy udostępnia prostą API do tego zadania.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę kontrolować wyjściowy kolor SVG?** Tak, możesz ustawić tryb kolorów SVG (np. odcienie szarości).  
- **Czy wymagana jest dodatkowa oprogramowanie?** Tylko środowisko uruchomieniowe Java i plik JAR Aspose.CAD.

## Wymagania wstępne

Before diving into the tutorial, ensure you have the following prerequisites:

- Środowisko programistyczne Java: Upewnij się, że Java jest zainstalowana w Twoim systemie.  
- Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Javy z [linku do pobrania](https://releases.aspose.com/cad/java/).  
- Katalog dokumentów: Utwórz katalog dla swoich rysunków CAD i zanotuj jego ścieżkę.

## Importowanie przestrzeni nazw

In this step, we'll import the necessary namespaces to kickstart our Aspose.CAD journey. Follow these steps:

### Krok 1: Otwórz swój projekt Java
Otwórz swój projekt Java w wybranym IDE.

### Krok 2: Dodaj bibliotekę Aspose.CAD
Dodaj bibliotekę Aspose.CAD do swojego projektu. Możesz to zrobić, dołączając plik JAR do zależności projektu.

### Krok 3: Importuj przestrzenie nazw
In your Java class, import the required namespaces:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Eksportowanie CAD do SVG

Now that we've set the stage, let's dive into the step‑by‑step process of **export CAD to SVG** using Aspose.CAD for Java.

### Krok 1: Określ katalog zasobów
Define the path to your resource directory, where your CAD drawings are located:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Krok 2: Załaduj rysunek CAD
Load the CAD drawing using the Aspose.CAD library:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Krok 3: Skonfiguruj opcje eksportu SVG
Configure the SVG export options to customize the output. Here we **set SVG color mode** to grayscale and tell the exporter to convert text to shapes:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Krok 4: Zapisz jako SVG
Save the CAD drawing as an SVG file:

```java
image.save(dataDir + "meshes.svg");
```

> **Wskazówka:** Jeśli potrzebujesz **konwertować DWG na SVG** zachowując kolory, zmień `SvgColorMode.Grayscale` na `SvgColorMode.FullColor`.

Congratulations! You've successfully exported a CAD drawing to SVG using Aspose.CAD for Java.

## Dlaczego używać Aspose.CAD do eksportu CAD do SVG?
- **Wysoka wierność:** Dane wektorowe są zachowane, co zapewnia, że SVG wygląda dokładnie tak jak oryginalny rysunek CAD.  
- **Brak zewnętrznych zależności:** Konwersja odbywa się w pełni w Javie, eliminując potrzebę dodatkowych narzędzi.  
- **Dostosowywalny wynik:** Opcje takie jak `setColorType` pozwalają kontrolować, czy SVG będzie w odcieniach szarości czy w pełnym kolorze.

## Typowe problemy i rozwiązania
- **Plik nie znaleziony:** Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku DWG jest prawidłowa.  
- **Pusty wynik SVG:** Upewnij się, że ustawiłeś `options.setTextAsShapes(true)`, jeśli rysunek zawiera tekst, który ma być wyświetlany jako kształty.  
- **Nieobsługiwany format CAD:** Aspose.CAD obsługuje DWG, DXF, DWF i kilka innych formatów; sprawdź dokumentację, aby poznać pełną listę.

## Zakończenie

In this tutorial, we've explored the seamless process of leveraging Aspose.CAD for Java to **export CAD to SVG**. With its intuitive API and robust features, Aspose.CAD simplifies complex tasks, providing developers with a versatile tool for CAD manipulation.

## FAQ

### P1: Czy mogę używać Aspose.CAD dla Javy z innymi formatami CAD?
O1: Tak, Aspose.CAD obsługuje różne formaty CAD, w tym DWG, DXF, DWF i inne.

### P2: Czy Aspose.CAD jest odpowiedni zarówno dla początkujących, jak i doświadczonych programistów?
O2: Zdecydowanie! Aspose.CAD oferuje przyjazne dla użytkownika API, co czyni go dostępnym dla początkujących, a jednocześnie zapewnia zaawansowane funkcje dla doświadczonych programistów.

### P3: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społecznościowe?
O3: Odwiedź [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), aby uzyskać wsparcie i uczestniczyć w dyskusjach.

### P4: Czy dostępna jest darmowa wersja próbna?
O4: Tak, możesz wypróbować Aspose.CAD korzystając z [darmowej wersji próbnej](https://releases.aspose.com/).

### P5: Jak mogę zakupić licencję na Aspose.CAD dla Javy?
O5: Licencję możesz kupić na [stronie zakupu](https://purchase.aspose.com/buy).

## Często zadawane pytania

**P:** Czy mogę konwertować plik DXF na SVG używając tego samego kodu?  
**O:** Tak, po prostu zamień nazwę pliku na plik DXF; API obsługuje oba formaty.

**P:** Jak zmienić wyjście na pełnokolorowy SVG?  
**O:** Ustaw `options.setColorType(SvgColorMode.FullColor);` przed zapisem.

**P:** Czy można osadzić czcionki w wygenerowanym SVG?  
**O:** Aspose.CAD obecnie konwertuje tekst na kształty; osadzanie czcionek nie jest wymagane.

**P:** Czy biblioteka działa na Linux i macOS?  
**O:** Biblioteka Java jest niezależna od platformy i działa wszędzie tam, gdzie dostępna jest kompatybilna JVM.

**P:** Jakiej wersji Aspose.CAD użyto w tym poradniku?  
**O:** Przykład został przetestowany z Aspose.CAD dla Javy 24.10.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-07  
**Testowano z:** Aspose.CAD dla Javy 24.10  
**Autor:** Aspose