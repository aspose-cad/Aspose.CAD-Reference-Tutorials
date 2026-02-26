---
date: 2026-01-10
description: Erfahren Sie, wie Sie DGN nach DWG exportieren und MicroStation DGN in
  AutoCAD DWG mit Aspose.CAD für Java konvertieren. Schritt‑für‑Schritt‑Anleitung.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: DGN nach DWG exportieren mit Aspose.CAD für Java
url: /de/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN nach DWG mit Aspose.CAD für Java

## Einführung

In diesem Tutorial lernen Sie, wie Sie **DGN nach DWG exportieren** und ein MicroStation‑DGN‑Design in einer AutoCAD‑DWG‑Datei mithilfe der Aspose.CAD‑Bibliothek für Java einbetten. Egal, ob Sie Legacy‑MicroStation‑Zeichnungen migrieren oder DGN‑Unterlagen mit DWG‑Layouts kombinieren möchten, dieser Leitfaden führt Sie durch jeden Schritt – von der Einrichtung der Umgebung bis zur Erstellung einer PDF‑Vorschau der finalen DWG‑Datei.

## Schnelle Antworten
- **Was bewirkt “export dgn to dwg”?** Es bettet ein DGN‑Unterlage in ein DWG ein und ermöglicht nahtloses Betrachten in AutoCAD.
- **In welches Format kann ich das Ergebnis für eine schnelle Vorschau exportieren?** Sie können die **CAD‑Datei mit `PdfOptions` nach PDF exportieren**.
- **Benötige ich eine Lizenz, um den Code auszuführen?** Für den Produktionseinsatz ist eine temporäre oder kostenpflichtige Aspose.CAD‑Lizenz erforderlich.
- **Welche Java‑Version wird unterstützt?** Java 8 oder höher funktioniert mit der neuesten Aspose.CAD‑Version für Java.
- **Ist ein kostenloser Test verfügbar?** Ja – laden Sie eine Testversion von der Aspose‑Website herunter.

## Was ist “export dgn to dwg”?
Das Exportieren von DGN nach DWG bedeutet, ein MicroStation‑DGN‑Design in ein AutoCAD‑DWG‑Zeichnung als Unterlage zu konvertieren oder einzubetten. Dadurch können CAD‑Fachleute vorhandene DGN‑Assets nutzen, ohne die Geometrie von Grund auf neu zu erstellen.

## Warum MicroStation DGN nach AutoCAD DWG konvertieren?
- **Zusammenarbeit:** Teams, die AutoCAD verwenden, können DGN‑Inhalte direkt ansehen und bearbeiten.
- **Standardisierung:** DWG ist das de‑facto‑Format für viele nachgelagerte Workflows (z. B. PDF‑Erstellung, 3D‑Rendering).
- **Erhaltung:** Bewahrt die ursprünglichen DGN‑Referenzen, wodurch Datenverlust reduziert wird.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:
1. **Aspose.CAD‑Bibliothek:** Laden Sie die Aspose.CAD‑Bibliothek für Java herunter und installieren Sie sie. Die Bibliothek finden Sie [hier](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Stellen Sie sicher, dass Java auf Ihrem System installiert ist.
3. **Integrierte Entwicklungsumgebung (IDE):** Wählen Sie eine Java‑IDE wie Eclipse oder IntelliJ für ein reibungsloses Entwicklungserlebnis.

## Pakete importieren

Importieren Sie in Ihrem Java‑Projekt die erforderlichen Aspose.CAD‑Pakete, um die CAD‑Dateiverarbeitung zu ermöglichen. Hier ein Beispiel:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Schritt 1: Dateipfade festlegen

Definieren Sie die Eingabe‑ und Ausgabe‑Dateipfade für die DWG‑Datei. Aktualisieren Sie die Variablen `dataDir`, `fileName` und `outPath` entsprechend.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Schritt 2: PdfOptions‑Instanz erstellen

Erstellen Sie eine Instanz der Klasse `PdfOptions`, da wir die CAD‑Datei **nach PDF exportieren** für eine schnelle Überprüfung.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Schritt 3: DWG‑Datei laden

Laden Sie die vorhandene DWG‑Datei als Bild und konvertieren Sie sie in den Typ `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Schritt 4: Durch Entitäten iterieren

Durchlaufen Sie jede Entität in der DWG‑Datei und prüfen Sie, ob es sich um eine Bilddefinition handelt. Falls ja, holen Sie die externe Referenz zum Objekt.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Schritt 5: Rasterisierungsoptionen definieren

Definieren Sie die Einstellungen für das Objekt `CadRasterizationOptions`, einschließlich Seitenbreite, -höhe, Layouts und Hintergrundfarbe.

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

## Schritt 6: Vektor‑Rasterisierungsoptionen festlegen

Legen Sie die Vektor‑Rasterisierungsoptionen für den Export fest.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Schritt 7: DWG nach PDF exportieren

Exportieren Sie schließlich die DWG‑Datei nach PDF, indem Sie die Methode `save` aufrufen.

```java
cadImage.save(outPath, exportOptions);
```

## Allgemeine Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|-------|----------|
| **Keine DGN‑Unterlage sichtbar** | Die DWG‑Datei enthält keine `DGNUNDERLAY`‑Entität. | Stellen Sie sicher, dass die Quell‑DWG eine DGN‑Referenz enthält. |
| **PDF ist leer** | Rasterisierungsoptionen sind auf Nullgröße oder falsches Layout gesetzt. | Stellen Sie sicher, dass `setPageWidth`/`setPageHeight` positiv sind und `setLayouts` dem DWG‑Layoutnamen entspricht. |
| **Lizenzausnahme** | Ausführung ohne gültige Aspose.CAD‑Lizenz. | Wenden Sie vor dem Aufruf von API‑Methoden eine temporäre oder gekaufte Lizenz an. |

## Häufig gestellte Fragen

### Q1: Wo finde ich die Dokumentation für Aspose.CAD für Java?

Die Dokumentation finden Sie [hier](https://reference.aspose.com/cad/java/).

### Q2: Wie kann ich die Aspose.CAD‑Bibliothek für Java herunterladen?

Sie können die Bibliothek über [diesen Link](https://releases.aspose.com/cad/java/) herunterladen.

### Q3: Ist ein kostenloser Test für Aspose.CAD für Java verfügbar?

Ja, den kostenlosen Test finden Sie [hier](https://releases.aspose.com/).

### Q4: Wo kann ich eine temporäre Lizenz für Aspose.CAD für Java erhalten?

Erhalten Sie eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Brauchen Sie Hilfe oder haben Sie Fragen?

Besuchen Sie das Aspose.CAD‑Community‑Support‑Forum [hier](https://forum.aspose.com/c/cad/19).

### Q6: Kann ich das resultierende PDF zurück nach DWG konvertieren?

Das PDF ist eine Rastervorschau; die Rückkonvertierung nach DWG erfordert ein separates Reverse‑Engineering‑Tool.

### Q7: Funktioniert dieser Ansatz mit anderen CAD‑Formaten wie DWF oder DXF?

Ja, Aspose.CAD unterstützt viele Formate; Sie müssen lediglich die Dateierweiterungen und Rasterisierungseinstellungen entsprechend anpassen.

**Zuletzt aktualisiert:** 2026-01-10  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}