---
title: Anpassen der CAD-Zeichnungsgröße mithilfe des Einheitentyps mit Aspose.CAD für Java
linktitle: Anpassen der CAD-Zeichnungsgröße mithilfe des Einheitentyps
second_title: Aspose.CAD Java API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.CAD für Java bei der mühelosen Anpassung der CAD-Zeichnungsgrößen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für Präzision und Anpassungsfähigkeit.
weight: 14
url: /de/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Anpassen der CAD-Zeichnungsgröße mithilfe des Einheitentyps mit Aspose.CAD für Java

## Einführung

Im sich ständig weiterentwickelnden Bereich des computergestützten Designs (CAD) sind Präzision und Anpassungsfähigkeit von größter Bedeutung. Eine häufige Anforderung besteht darin, die Größe von CAD-Zeichnungen basierend auf bestimmten Einheitentypen anzupassen. Aspose.CAD für Java erweist sich als leistungsstarker Verbündeter und bietet nahtlose Funktionen für die programmgesteuerte Bearbeitung von CAD-Dateien.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine funktionsfähige Java-Entwicklungsumgebung eingerichtet ist.

-  Aspose.CAD für Java-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek herunter und integrieren Sie sie in Ihr Java-Projekt. Sie können die Bibliothek beziehen[Hier](https://releases.aspose.com/cad/java/).

## Namespaces importieren

Fügen Sie in Ihren Java-Code die erforderlichen Namespaces ein, um auf Aspose.CAD-Funktionen zuzugreifen. Fügen Sie die folgenden Importe hinzu:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Lassen Sie uns nun den Prozess der Anpassung der CAD-Zeichnungsgröße mithilfe des Einheitentyps in überschaubare Schritte unterteilen:

## Schritt 1: Datenverzeichnis definieren

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Legen Sie den Pfad für das Verzeichnis fest, in dem sich Ihre CAD-Dateien befinden.

## Schritt 2: CAD-Zeichnung laden

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Laden Sie die CAD-Zeichnung mit Aspose.CAD`Image` Klasse.

## Schritt 3: Erstellen Sie BMP-Optionen

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instanziieren Sie die`BmpOptions` Klasse zum Exportieren des CAD-Layouts in das BMP-Format.

## Schritt 4: Rasterisierungsoptionen konfigurieren

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Erstellen Sie eine Instanz von`CadRasterizationOptions` und assoziiere es mit dem`BmpOptions` zur Vektorrasterung.

## Schritt 5: Einheitentyp festlegen

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Geben Sie den gewünschten Einheitentyp für die CAD-Zeichnung an. In diesem Beispiel haben wir es auf Zentimeter eingestellt.

## Schritt 6: Layouts festlegen

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definieren Sie die Layouts, die beim Export berücksichtigt werden sollen. In diesem Fall haben wir das Layout „Modell“ ausgewählt.

## Schritt 7: Export nach BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Speichern Sie abschließend die geänderte CAD-Zeichnung im BMP-Format.

## Abschluss

Mit Aspose.CAD für Java wird die Anpassung der CAD-Zeichnungsgrößen zum Kinderspiel. Dieses Tutorial hat Sie durch den Prozess geführt und die Bedeutung jedes Schritts für das Erreichen präziser Ergebnisse hervorgehoben.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen Programmiersprachen verwenden?

A1: Aspose.CAD unterstützt hauptsächlich Java, es sind jedoch Versionen für andere Sprachen wie .NET verfügbar.

### F2: Gibt es Lizenzoptionen für Aspose.CAD?

 A2: Ja, Sie können Lizenzoptionen erkunden und Aspose.CAD erwerben[Hier](https://purchase.aspose.com/buy).

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD?

 A3: Natürlich können Sie auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wie erhalte ich Unterstützung für Aspose.CAD für Java?

 A4: Besuchen Sie das Aspose.CAD-Forum[Hier](https://forum.aspose.com/c/cad/19) für eine umfassende Betreuung.

### F5: Kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

 A5: Ja, Sie können eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
