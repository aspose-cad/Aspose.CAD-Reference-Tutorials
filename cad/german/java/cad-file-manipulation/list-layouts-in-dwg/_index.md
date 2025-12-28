---
date: 2025-12-28
description: Erfahren Sie, wie Sie DWG-Dateien mit Aspose.CAD für Java lesen und mühelos
  Layouts in DWG-Dateien auflisten können. Integrieren Sie leistungsstarke CAD‑Funktionen
  in Ihre Java‑Anwendungen.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Wie man DWG liest und Layouts in DWG mit Aspose.CAD für Java auflistet
url: /de/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man DWG liest und Layouts in DWG auflistet mit Aspose.CAD für Java

## Einführung

Wenn Sie **DWG**-Dateien programmgesteuert lesen und Informationen wie Layoutnamen extrahieren müssen, macht Aspose.CAD für Java das unkompliziert. In diesem Schritt‑für‑Schritt‑Tutorial zeigen wir Ihnen **wie man DWG liest** und alle in einer DWG‑ (oder DXF‑)Datei enthaltenen Layouts auflistet. Am Ende des Leitfadens können Sie diese Fähigkeit zu jeder Java‑Anwendung hinzufügen, die mit CAD‑Daten arbeitet.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.CAD for Java.
- **Kann ich DWG‑Dateien auf jedem Betriebssystem lesen?** Ja – Java ist plattformübergreifend.
- **Benötige ich eine Lizenz, um das Beispiel auszuführen?** Eine kostenlose Testversion funktioniert für die Evaluierung; für die Produktion ist eine Lizenz erforderlich.
- **Welche CAD‑Formate werden unterstützt?** DWG, DXF, DWF und weitere.
- **Ist der Code mit Java 8+ kompatibel?** Absolut.

## Was bedeutet „how to read dwg“ in Java?

Das Lesen einer DWG‑Datei bedeutet, die binären CAD‑Daten in ein Objektmodell zu laden, das Sie abfragen können. Aspose.CAD abstrahiert die komplexe DWG‑Struktur hinter einfachen .NET/Java‑Klassen, sodass Sie sich auf die Informationen konzentrieren können, die Sie benötigen – in diesem Fall die Layoutnamen.

## Warum Layouts in einer DWG‑Datei auflisten?

Eine DWG kann mehrere Layouts enthalten (Papierbereich, Modellbereich, benutzerdefinierte Blätter). Das Kennen der Layoutnamen ermöglicht Ihnen:
- Berichte pro Layout zu erstellen.
- Bestimmte Layouts in Bilder oder PDFs zu exportieren.
- Die Stapelverarbeitung von Zeichnungen zu automatisieren.

## Voraussetzungen

Bevor wir in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD for Java Library** – laden Sie die neueste JAR von der [Website](https://releases.aspose.com/cad/java/) herunter.
- **Java Development Environment** – JDK 8 oder höher sowie eine IDE oder ein Build‑Tool Ihrer Wahl.

## Namespaces importieren

Importieren Sie in Ihrer Java‑Quelldatei die erforderlichen Aspose.CAD‑Klassen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Schritt 1: Richten Sie Ihr Dokumentenverzeichnis ein

Ersetzen Sie **„Your Document Directory“** durch den absoluten Pfad, in dem Ihre CAD‑Dateien liegen.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## Schritt 2: Laden Sie die DWG‑Datei

Die Methode `Image.load` erkennt das Dateiformat automatisch, sodass Sie denselben Code sowohl für **DWG**‑ als auch **DXF**‑Dateien verwenden können.

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

## Schritt 3: Layouts abrufen und Namen ausgeben

Die Schleife iteriert über jedes Layout‑Objekt und gibt dessen Namen in der Konsole aus – ein einfacher Weg, um zu überprüfen, dass Sie **DWG erfolgreich gelesen** und Layout‑Informationen extrahiert haben.

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

## Häufige Fallstricke & Tipps

- **Falscher Dateipfad** – Überprüfen Sie, dass `dataDir` mit einem für Ihr Betriebssystem geeigneten Trennzeichen (`/` oder `\\`) endet.
- **Nicht unterstützte DWG‑Version** – Stellen Sie sicher, dass Sie eine aktuelle Aspose.CAD‑Version verwenden; ältere DWG‑Versionen benötigen möglicherweise eine Konvertierung.
- **Speichernutzung** – Große Zeichnungen können erheblichen Speicher verbrauchen. Entsorgen Sie das `CadImage`‑Objekt nach Gebrauch: `cadImage.dispose();`.

## Fazit

Herzlichen Glückwunsch! Sie wissen jetzt **wie man DWG liest** und dessen Layouts mit Aspose.CAD für Java auflistet. Diese Technik bildet die Grundlage für weiterführende CAD‑Automatisierung, wie das Exportieren bestimmter Layouts in Bilder oder PDFs. Für weiterführende Informationen lesen Sie die offizielle [Dokumentation](https://reference.aspose.com/cad/java/).

## FAQ's

### Q1: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate, einschließlich DWG, DXF, DWF und mehr.

### Q2: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?

A2: Ja, Sie können eine kostenlose Testversion von [hier](https://releases.aspose.com/) erhalten.

### Q3: Wo kann ich Community‑Support für Aspose.CAD für Java erhalten?

A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

### Q4: Wie kaufe ich eine Lizenz für Aspose.CAD für Java?

A4: Sie können eine Lizenz über die [Kaufseite](https://purchase.aspose.com/buy) erwerben.

### Q5: Kann ich eine temporäre Lizenz für Testzwecke verwenden?

A5: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**Zusätzliche Fragen**

**Q: Funktioniert dieser Ansatz zum Lesen von DWG‑Dateien unter Linux?**  
A: Absolut. Da die Lösung reines Java ist, läuft sie auf jedem Betriebssystem mit einem kompatiblen JDK.

**Q: Kann ich eine DWG‑Datei lesen, ohne das gesamte Drawing in den Speicher zu laden?**  
A: Aspose.CAD lädt das Drawing in den Speicher; bei sehr großen Dateien sollten Sie eine Verarbeitung in separaten Threads oder die Verwendung von Streaming‑APIs in Betracht ziehen, falls diese in zukünftigen Releases verfügbar werden.

**Q: Gibt es eine Möglichkeit, Layouts nach Namen zu filtern?**  
A: Ja – nachdem Sie das `CadLayoutDictionary` abgerufen haben, können Sie `layout.getLayoutName().equalsIgnoreCase("MyLayout")` prüfen, bevor Sie weiterverarbeiten.

---

**Zuletzt aktualisiert:** 2025-12-28  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}