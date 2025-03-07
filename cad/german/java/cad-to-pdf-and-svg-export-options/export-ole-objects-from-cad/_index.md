---
title: Exportieren Sie OLE-Objekte aus CAD mit Aspose.CAD für Java
linktitle: Exportieren Sie OLE-Objekte aus CAD
second_title: Aspose.CAD Java API
description: Nutzen Sie das Potenzial von Aspose.CAD für Java. Exportieren Sie mühelos OLE-Objekte aus CAD-Dateien. Laden Sie es jetzt herunter und profitieren Sie von einer nahtlosen CAD-Datenverwaltung.
weight: 10
url: /de/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren Sie OLE-Objekte aus CAD mit Aspose.CAD für Java

## Einführung

In der dynamischen Welt des Computer-Aided Design (CAD) ist die effiziente Verwaltung und Extraktion von OLE-Objekten (Object Linking and Embedding) von entscheidender Bedeutung. Aspose.CAD für Java bietet eine leistungsstarke Lösung zum Exportieren von OLE-Objekten aus CAD-Dateien. Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess und stellt sicher, dass Sie das volle Potenzial dieses Tools nutzen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Umgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.
-  Aspose.CAD für Java: Laden Sie die Aspose.CAD für Java-Bibliothek herunter und installieren Sie sie. Sie finden die Bibliothek im[Download-Link](https://releases.aspose.com/cad/java/).
- CAD-Dateien: Bereiten Sie die CAD-Dateien mit den OLE-Objekten vor, die Sie exportieren möchten.

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces in Ihr Java-Projekt. Diese Namespaces stellen die wesentlichen Klassen und Funktionalitäten bereit, die für die Arbeit mit CAD-Dateien mit Aspose.CAD erforderlich sind.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Lassen Sie uns nun den Prozess des Exportierens von OLE-Objekten aus CAD in mehrere Schritte unterteilen:

## Schritt 1: Legen Sie Ihr Dokumentenverzeichnis fest

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Stellen Sie sicher, dass Sie „Ihr Dokumentverzeichnis“ durch den Pfad zu dem Verzeichnis ersetzen, das Ihre CAD-Dateien enthält.

## Schritt 2: Definieren Sie CAD-Dateinamen

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Geben Sie die Namen der CAD-Dateien an, die Sie im bearbeiten möchten`files` Array.

## Schritt 3: Legen Sie die PNG-Exportoptionen fest

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurieren Sie die PNG-Exportoptionen, einschließlich Vektorrasterung und Layouteinstellungen.

## Schritt 4: Durchlaufen Sie CAD-Dateien

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Durchlaufen Sie jede angegebene CAD-Datei, laden Sie sie mit Aspose.CAD und speichern Sie die OLE-Objekte als PNG-Bilder.

## Abschluss

Mit diesen einfachen, aber leistungsstarken Schritten können Sie mit Aspose.CAD für Java nahtlos OLE-Objekte aus CAD-Dateien exportieren. Dieses vielseitige Tool ermöglicht Entwicklern die effiziente Verwaltung von CAD-Daten und eröffnet neue Möglichkeiten bei der Entwicklung von CAD-Anwendungen.

## FAQs

### F1: Ist Aspose.CAD mit allen CAD-Dateiformaten kompatibel?

 A1: Aspose.CAD unterstützt verschiedene CAD-Formate, einschließlich DWG, DXF und DGN. Siehe die[Dokumentation](https://reference.aspose.com/cad/java/) für die vollständige Liste.

### F2: Kann ich die Exporteinstellungen für OLE-Objekte anpassen?

A2: Ja, Aspose.CAD bietet umfangreiche Optionen zum Anpassen der Exporteinstellungen, sodass Sie die Ausgabe an Ihre spezifischen Anforderungen anpassen können.

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD?

 A3: Ja, Sie können die Funktionen von Aspose.CAD erkunden, indem Sie eine kostenlose Testversion von erhalten[Hier](https://releases.aspose.com/).

### F4: Wo kann ich Community-Support für Aspose.CAD erhalten?

 A4: Treten Sie der Aspose.CAD-Community bei[Forum](https://forum.aspose.com/c/cad/19) um Hilfe zu suchen und Ihre Erfahrungen auszutauschen.

### F5: Wie kann ich eine Lizenz für Aspose.CAD erwerben?

A5: Besuchen Sie die[Kaufseite](https://purchase.aspose.com/buy) um eine Lizenz zu erwerben, die Ihren Entwicklungsanforderungen entspricht.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
