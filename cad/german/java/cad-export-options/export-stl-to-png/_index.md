---
title: Exportieren Sie STL nach PNG mit Aspose.CAD für Java
linktitle: STL nach PNG exportieren
second_title: Aspose.CAD Java API
description: Entdecken Sie den nahtlosen Prozess des Exports von STL-Dateien nach PNG in Java mit Aspose.CAD. Vereinfachen Sie Ihren Arbeitsablauf und verbessern Sie Ihre Java-Projekte mühelos.
weight: 20
url: /de/java/cad-export-options/export-stl-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren Sie STL nach PNG mit Aspose.CAD für Java

## Einführung

Möchten Sie STL-Dateien mit Java nach PNG exportieren? Aspose.CAD für Java ist die Lösung, die Sie brauchen! In diesem Tutorial führen wir Sie Schritt für Schritt durch den Prozess. Als erfahrener SEO-Autor sorge ich dafür, dass der Inhalt nicht nur informativ, sondern auch für Suchmaschinen optimiert ist.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java Development Kit (JDK) ist auf Ihrem Computer installiert.
-  Aspose.CAD für Java-Bibliothek heruntergeladen. Du kannst es bekommen[Hier](https://releases.aspose.com/cad/java/).
-  Eine gültige Lizenz oder eine temporäre Lizenz von[Hier](https://purchase.aspose.com/temporary-license/).

## Namespaces importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Namespaces:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Lassen Sie uns das Beispiel nun in mehrere Schritte unterteilen.

## Schritt 1: Richten Sie Ihr Projekt ein

Erstellen Sie ein neues Java-Projekt und fügen Sie die Aspose.CAD for Java-Bibliothek zu den Abhängigkeiten Ihres Projekts hinzu.

## Schritt 2: Geben Sie Ihre STL-Datei an

Definieren Sie den Pfad zu Ihrer STL-Datei. Zum Beispiel:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Schritt 3: STL-Datei laden

 Laden Sie die STL-Datei mit`Image.load` Methode:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Schritt 4: Rasterisierungsoptionen konfigurieren

Richten Sie Rasterisierungsoptionen für die Vektorisierung ein:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Schritt 5: PNG-Optionen konfigurieren

Geben Sie Optionen für den PNG-Export an:

```java
PngOptions pngOptions = new PngOptions();
// Kommentieren Sie die Zeile unten aus, wenn Sie Optionen für die Vektorrasterung festlegen möchten
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Schritt 6: Als PNG speichern

Speichern Sie das CAD-Bild als PNG-Datei:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Glückwunsch! Sie haben mit Aspose.CAD für Java erfolgreich eine STL-Datei nach PNG exportiert.

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie Aspose.CAD für Java nutzen können, um STL-Dateien mühelos in PNG zu exportieren. Diese leistungsstarke Bibliothek vereinfacht komplexe Aufgaben und ist somit eine wertvolle Bereicherung für Ihre Java-Projekte.

## FAQs

### F1: Ist Aspose.CAD für Java mit allen STL-Dateiversionen kompatibel?

A1: Aspose.CAD für Java unterstützt verschiedene STL-Dateiversionen und gewährleistet so die Kompatibilität mit den gängigsten Formaten.

### F2: Kann ich Aspose.CAD für Java in einem kommerziellen Projekt verwenden?

 A2: Ja, das können Sie. Besorgen Sie sich einfach eine gültige Lizenz von[Hier](https://purchase.aspose.com/buy).

### F3: Benötige ich eine temporäre Lizenz für die kostenlose Testversion?

 A3: Nein, für die kostenlose Testversion ist keine temporäre Lizenz erforderlich. Mit der Testversion können Sie sofort loslegen[Hier](https://releases.aspose.com/).

### F4: Wo kann ich zusätzliche Unterstützung finden oder Fragen stellen?

 A4: Besuchen Sie das Aspose.CAD-Forum[Hier](https://forum.aspose.com/c/cad/19) für jegliche Unterstützung oder Fragen.

### F5: Gibt es eine umfassende Dokumentation?

 A5: Ja, die Dokumentation kann gefunden werden[Hier](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
