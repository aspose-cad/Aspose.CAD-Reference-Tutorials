---
date: 2026-02-28
description: Erfahren Sie, wie Sie DWG‑Dateien mit Aspose.CAD für Java lesen und mühelos
  Layouts in DWG‑Dateien auflisten können. Integrieren Sie leistungsstarke CAD‑Funktionen
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

# Wie man DWG‑Dateien liest und Layouts in DWG mit Aspose.CAD für Java auflistet

## Einführung

Wenn Sie nach einer zuverlässigen Methode **wie man DWG**‑Dateien programmgesteuert liest, bietet Aspose.CAD für Java eine saubere, plattformübergreifende API, mit der Sie eine Zeichnung laden und jede benötigte Information extrahieren können – zum Beispiel die Namen aller Layouts in der Datei. In diesem Schritt‑für‑Schritt‑Tutorial zeigen wir Ihnen **wie man DWG** liest und jedes in einer DWG‑ (oder DXF‑) Datei enthaltene Layout auflistet, sodass Sie diese Fähigkeit in jede Java‑Anwendung integrieren können, die mit CAD‑Daten arbeitet.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.CAD für Java.  
- **Kann ich DWG‑Dateien auf jedem Betriebssystem lesen?** Ja – Java ist plattformübergreifend, sodass Sie **DWG unter Linux** genauso einfach lesen können wie unter Windows.  
- **Benötige ich eine Lizenz, um das Beispiel auszuführen?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine Lizenz erforderlich.  
- **Welche CAD‑Formate werden unterstützt?** DWG, DXF, DWF und weitere.  
- **Ist der Code mit Java 8+ kompatibel?** Absolut.

## Was bedeutet „wie man DWG liest“ in Java?

Eine DWG‑Datei zu lesen bedeutet, die binären CAD‑Daten in ein Objektmodell zu laden, das Sie abfragen können. Aspose.CAD abstrahiert die komplexe DWG‑Struktur hinter einfachen Java‑Klassen, sodass Sie sich auf die Informationen konzentrieren können, die Sie benötigen – in diesem Fall die Layout‑Namen.

## Warum Layouts in einer DWG‑Datei auflisten?

Eine DWG kann mehrere Layouts enthalten (Papier‑Space, Modell‑Space, benutzerdefinierte Blätter). Das Wissen um die Layout‑Namen ermöglicht Ihnen:

- Berichte pro Layout zu erstellen.  
- Bestimmte Layouts in Bilder oder PDFs zu exportieren.  
- Die Stapelverarbeitung von Zeichnungen zu automatisieren.  

## Voraussetzungen

Bevor wir zum Code kommen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD für Java Bibliothek** – laden Sie die neueste JAR von der [Website](https://releases.aspose.com/cad/java/) herunter.  
- **Java‑Entwicklungsumgebung** – JDK 8 oder höher sowie eine IDE oder ein Build‑Tool Ihrer Wahl.

## Namespaces importieren

Importieren Sie in Ihrer Java‑Quelldatei die benötigten Aspose.CAD‑Klassen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Schritt 1: Ihr Dokumentenverzeichnis einrichten

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ersetzen Sie **„Your Document Directory“** durch den absoluten Pfad, in dem Ihre CAD‑Dateien liegen. Unter Linux könnte das zum Beispiel `/home/user/cad/` sein.

## Schritt 2: Die DWG‑Datei laden

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Die Methode `Image.load` erkennt das Dateiformat automatisch, sodass derselbe Code sowohl für **DWG**‑ als auch **DXF**‑Dateien funktioniert.

## Schritt 3: Layouts abrufen und Namen ausgeben

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Die Schleife iteriert über jedes Layout‑Objekt und gibt dessen Namen in der Konsole aus – ein einfacher Weg, zu überprüfen, dass Sie **DWG gelesen** und Layout‑Informationen extrahiert haben.

## Wie man DWG unter Linux in PDF konvertiert

Falls Sie später ein bestimmtes Layout in ein PDF umwandeln möchten, kann Aspose.CAD das Layout in ein Bild rendern und Sie können anschließend Aspose.PDF (oder eine andere PDF‑Bibliothek) verwenden, um dieses Bild in ein PDF‑Dokument einzubetten. Der Konvertierungscode ist unter Linux identisch, da die API reines Java ist.

## Häufige Stolperfallen & Tipps

- **Falscher Dateipfad** – Stellen Sie sicher, dass `dataDir` mit einem Trennzeichen (`/` oder `\\`) endet, das zu Ihrem Betriebssystem passt.  
- **Nicht unterstützte DWG‑Version** – Verwenden Sie eine aktuelle Aspose.CAD‑Version; ältere DWG‑Versionen benötigen möglicherweise eine Konvertierung.  
- **Speicherverbrauch** – Große Zeichnungen können viel Speicher beanspruchen. Entsorgen Sie das `CadImage`‑Objekt nach Gebrauch: `cadImage.dispose();`.  
- **Ausführung auf headless Servern** – Es werden keine UI‑Komponenten benötigt, sodass der Code auf Linux‑Servern ohne grafische Umgebung funktioniert.

## Fazit

Herzlichen Glückwunsch! Sie wissen jetzt **wie man DWG liest** und die Layouts mit Aspose.CAD für Java auflistet. Diese Technik bildet die Grundlage für weiterführende CAD‑Automatisierung, etwa das Exportieren bestimmter Layouts in Bilder, PDFs oder sogar das Konvertieren von DWG nach PDF unter Linux. Für weiterführende Informationen lesen Sie die offizielle [Dokumentation](https://reference.aspose.com/cad/java/).

## Häufig gestellte Fragen

**F1: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?**  
A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF, DWF und mehr.

**F2: Gibt es eine kostenlose Testversion von Aspose.CAD für Java?**  
A2: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

**F3: Wo finde ich Community‑Support für Aspose.CAD für Java?**  
A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

**F4: Wie kaufe ich eine Lizenz für Aspose.CAD für Java?**  
A4: Sie können eine Lizenz auf der [Kaufseite](https://purchase.aspose.com/buy) erwerben.

**F5: Kann ich eine temporäre Lizenz für Testzwecke verwenden?**  
A5: Ja, eine temporäre Lizenz erhalten Sie [hier](https://purchase.aspose.com/temporary-license/).

**Weitere Fragen**

**F: Funktioniert dieser Ansatz zum Lesen von DWG‑Dateien unter Linux?**  
A: Absolut. Da die Lösung reines Java ist, läuft sie auf jedem OS mit kompatiblem JDK.

**F: Kann ich eine DWG‑Datei lesen, ohne die gesamte Zeichnung in den Speicher zu laden?**  
A: Aspose.CAD lädt die Zeichnung in den Speicher; bei sehr großen Dateien sollten Sie eine Verarbeitung in separaten Threads oder zukünftige Streaming‑APIs in Betracht ziehen, sofern verfügbar.

**F: Gibt es eine Möglichkeit, Layouts nach Namen zu filtern?**  
A: Ja – nachdem Sie das `CadLayoutDictionary` erhalten haben, können Sie `layout.getLayoutName().equalsIgnoreCase("MyLayout")` prüfen, bevor Sie weiterverarbeiten.

---

**Zuletzt aktualisiert:** 2026-02-28  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}