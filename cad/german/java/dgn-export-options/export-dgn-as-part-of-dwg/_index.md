---
title: Exportieren Sie DGN in DWG mit Aspose.CAD für Java
linktitle: Exportieren Sie DGN als Teil von DWG
second_title: Aspose.CAD Java API
description: Erfahren Sie, wie Sie DGN als Teil von DWG mit Aspose.CAD für Java exportieren. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine effiziente Bearbeitung von CAD-Dateien.
weight: 10
url: /de/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren Sie DGN in DWG mit Aspose.CAD für Java

## Einführung

In diesem Tutorial erfahren Sie, wie Sie mit Aspose.CAD für Java eine DGN-Datei (MicroStation Design) als Teil einer DWG-Datei (AutoCAD Drawing) exportieren. Aspose.CAD ist eine leistungsstarke Bibliothek, die umfassende Funktionalität für die Arbeit mit CAD-Dateiformaten bietet. Diese Schritt-für-Schritt-Anleitung hilft Ihnen, den Prozess des DGN-Exports als Teil von DWG mit Java zu verstehen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
1. Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek für Java herunter und installieren Sie sie. Sie finden die Bibliothek[Hier](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Stellen Sie sicher, dass Java auf Ihrem System installiert ist.
3. Integrierte Entwicklungsumgebung (IDE): Wählen Sie eine Java-IDE wie Eclipse oder IntelliJ für eine reibungslosere Entwicklungserfahrung.

## Pakete importieren

Importieren Sie in Ihr Java-Projekt die erforderlichen Aspose.CAD-Pakete, um die Bearbeitung von CAD-Dateien zu ermöglichen. Hier ist ein Beispiel:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Schritt 1: Dateipfade festlegen

 Definieren Sie die Eingabe- und Ausgabedateipfade für die DWG-Datei. Aktualisieren Sie die`dataDir`, `fileName` , Und`outPath` Variablen entsprechend.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Schritt 2: Erstellen Sie eine PdfOptions-Instanz

 Erstellen Sie eine Instanz von`PdfOptions` Klasse, da wir die DWG-Datei in das PDF-Format exportieren.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Schritt 3: DWG-Datei laden

 Laden Sie die vorhandene DWG-Datei als Bild und konvertieren Sie sie in das`CadImage` Typ.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Schritt 4: Durch Entitäten iterieren

Gehen Sie jedes Element in der DWG-Datei durch und prüfen Sie, ob es sich um eine Bilddefinition handelt. Wenn dies der Fall ist, rufen Sie den externen Verweis auf das Objekt ab.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Schritt 5: Rasterisierungsoptionen definieren

 Definieren Sie Einstellungen für`CadRasterizationOptions`Objekt, einschließlich Seitenbreite, Höhe, Layouts und Hintergrundfarbe.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Schritt 6: Legen Sie die Optionen für die Vektorrasterung fest

Legen Sie die Optionen für die Vektorrasterung für den Export fest.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Schritt 7: DWG in PDF exportieren

 Exportieren Sie abschließend die DWG-Datei in eine PDF-Datei, indem Sie die Datei aufrufen`save` Methode.

```java
cadImage.save(outPath, exportOptions);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.CAD für Java eine DGN-Datei als Teil einer DWG-Datei exportieren. Diese leistungsstarke Bibliothek bietet umfangreiche Funktionen für die Arbeit mit CAD-Dateien und macht Ihre CAD-Dateibearbeitungsaufgaben effizient und unkompliziert.

## FAQs

### F1: Wo finde ich die Dokumentation für Aspose.CAD für Java?

 A1: Die Dokumentation kann gefunden werden[Hier](https://reference.aspose.com/cad/java/).

### F2: Wie kann ich die Aspose.CAD-Bibliothek für Java herunterladen?

 A2: Sie können die Bibliothek herunterladen unter[dieser Link](https://releases.aspose.com/cad/java/).

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?

 A3: Ja, Sie können die kostenlose Testversion finden[Hier](https://releases.aspose.com/).

### F4: Wo kann ich eine temporäre Lizenz für Aspose.CAD für Java erhalten?

 A4: Besorgen Sie sich eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Benötigen Sie Hilfe oder haben Sie Fragen?

 A5: Besuchen Sie das Aspose.CAD-Community-Supportforum[Hier](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
