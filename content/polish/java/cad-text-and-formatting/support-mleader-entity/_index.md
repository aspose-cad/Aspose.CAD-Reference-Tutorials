---
title: Obsługa encji MLeader dla formatu DWG za pomocą Aspose.CAD dla Java
linktitle: Obsługa encji MLeader dla formatu DWG w języku Java
second_title: Aspose.CAD API Java
description: Odblokuj moc Aspose.CAD dla Java dzięki naszemu samouczkowi krok po kroku dotyczącemu obsługi obiektów MLeader w formacie DWG.
type: docs
weight: 12
url: /pl/java/cad-text-and-formatting/support-mleader-entity/
---
## Wstęp

W dziedzinie projektowania wspomaganego komputerowo (CAD) z wykorzystaniem języka Java zrozumienie i wdrożenie obsługi jednostek MLeader w formacie DWG jest cenną umiejętnością. Aspose.CAD dla Java zapewnia solidne rozwiązanie do takich zadań, oferując zestaw potężnych narzędzi i funkcjonalności. Ten samouczek poprowadzi Cię przez proces obsługi obiektów MLeader w plikach DWG przy użyciu Java z Aspose.CAD.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

1. Środowisko programistyczne Java: Upewnij się, że w systemie skonfigurowano środowisko programistyczne Java.

2.  Biblioteka Aspose.CAD: Pobierz i zainstaluj bibliotekę Aspose.CAD dla Java z[link do pobrania](https://releases.aspose.com/cad/java/).

## Importuj przestrzenie nazw

W swoim projekcie Java zaimportuj niezbędne przestrzenie nazw, aby efektywnie wykorzystać możliwości Aspose.CAD. Dołącz następujące wiersze do swojego kodu:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

Podzielmy teraz kod na przewodnik krok po kroku dotyczący obsługi jednostek MLeader w formacie DWG przy użyciu języka Java w programie Aspose.CAD.

## 1. Załaduj plik DWG i uzyskaj dostęp do CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Zatwierdź podmioty MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Sprawdź styl i atrybuty MLeadera

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Uzyskaj dostęp do danych kontekstowych MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Sprawdź atrybuty kontekstu

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Uzyskaj dostęp do węzła MLeader i linii odniesienia

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## 7. Sprawdź dodatkowe atrybuty MLeadera

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Sprawdź atrybuty tekstu

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Dodatkowe atrybuty MLeadera

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Wniosek

Gratulacje! Udało Ci się przejść przez obszerny przewodnik dotyczący obsługi jednostek MLeader w formacie DWG przy użyciu języka Java i Aspose.CAD. Ta możliwość otwiera drzwi do zaawansowanych manipulacji CAD i ulepsza zestaw narzędzi programistycznych Java.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.CAD dla Java z innymi formatami CAD?

Odpowiedź 1: Tak, Aspose.CAD obsługuje różne formaty CAD poza DWG, zapewniając wszechstronność w twoich projektach.

### P2: Gdzie mogę znaleźć szczegółową dokumentację Aspose.CAD dla Java?

 Odpowiedź 2: Patrz[dokumentacja](https://reference.aspose.com/cad/java/) aby uzyskać dogłębny wgląd w możliwości Aspose.CAD.

### P3: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 3: Tak, zapoznaj się z funkcjonalnościami z pierwszej ręki[bezpłatna wersja próbna](https://releases.aspose.com/).

### P4: Jak mogę uzyskać tymczasową licencję na Aspose.CAD?

A4: Uzyskaj tymczasową licencję za pośrednictwem[ten link](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę szukać wsparcia i pomocy społeczności?

A5: Odwiedź[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) aby nawiązać kontakt ze społecznością i uzyskać pomoc.