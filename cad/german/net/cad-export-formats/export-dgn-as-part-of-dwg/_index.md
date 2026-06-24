---
date: 2026-03-21
description: Erfahren Sie, wie Sie PDF aus DWG erstellen und DGN als Teil von DWG
  mit Aspose.CAD für .NET exportieren. Dieser Leitfaden zeigt außerdem, wie Sie DWG
  in PDF konvertieren und PDF‑Optionen festlegen.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF aus DWG erstellen und DGN als Teil von DWG exportieren – Aspose.CAD für
  .NET
url: /de/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF aus DWG erstellen und DGN als Teil von DWG exportieren – Aspose.CAD für .NET

## Einführung

Wenn Sie **PDF aus DWG**‑Dateien erstellen müssen und gleichzeitig ein DGN‑Design als Teil des DWG einbetten möchten, macht Aspose.CAD für .NET das ganz einfach. In diesem Tutorial führen wir Sie durch den gesamten Workflow: Laden eines DWG, Auffinden des eingebetteten DGN‑Underlays, Konfigurieren der Rasterisierungsoptionen und schließlich Export des Ergebnisses in ein PDF‑Dokument. Egal, ob Sie ein Batch‑Konvertierungstool, eine Reporting‑Engine oder einen CAD‑BIM‑Integrationsservice bauen – die nachfolgenden Schritte geben Ihnen ein solides, produktionsreifes Fundament.

## Schnelle Antworten
- **Welche Bibliothek übernimmt die DWG → PDF‑Konvertierung?** Aspose.CAD für .NET  
- **Kann ich ein DGN‑Underlay exportieren, während ich das PDF erstelle?** Ja – das Underlay wird über `CadDgnUnderlay` zugegriffen.  
- **Welche Methode legt PDF‑Optionen fest?** `PdfOptions` zusammen mit `CadRasterizationOptions`.  
- **Benötige ich eine Lizenz für die kommerzielle Nutzung?** Ja, eine gültige Aspose.CAD‑Lizenz ist erforderlich.  
- **Unterstützte .NET‑Versionen?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Was bedeutet „PDF aus DWG erstellen“?

Ein PDF aus einer DWG‑Datei zu erstellen bedeutet, die Vektorgezeichnung in ein raster‑ oder vektor‑basiertes PDF‑Dokument zu rendern. Dieser Vorgang ist nützlich, um Zeichnungen mit Stakeholdern zu teilen, die keine CAD‑Software besitzen, für die Archivierung oder zur Erstellung druckbarer Berichte. Aspose.CAD vereinfacht die Aufgabe, indem es das aufwändige Parsen von DWG‑Entitäten übernimmt und über `PdfOptions` eine feinkörnige Kontrolle über die Ausgabe ermöglicht.

## Warum DGN als Teil eines DWG exportieren?

Ein DGN‑Underlay stellt häufig Referenzgeometrie aus MicroStation‑Projekten dar. Durch den Export des DGN zusammen mit dem DWG bewahren Sie den ursprünglichen Design‑Kontext und stellen sicher, dass nachgelagerte Nutzer den kompletten Zeichnungssatz sehen. Das ist besonders wertvoll in multidisziplinären Projekten, in denen sowohl DWG‑ als auch DGN‑Dateien koexistieren.

## Voraussetzungen

- **Aspose.CAD für .NET** – laden Sie es [hier](https://releases.aspose.com/cad/net/) herunter.  
- **Entwicklungsumgebung** – Visual Studio (jede aktuelle Version) oder Ihre bevorzugte .NET‑IDE.  
- **Grundkenntnisse in C#** – Sie sollten mit der C#‑Syntax und der .NET‑Projektstruktur vertraut sein.

## Namespaces importieren

Fügen Sie die erforderlichen `using`‑Direktiven am Anfang Ihrer C#‑Quelldatei hinzu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dateipfade festlegen

Legen Sie die Eingabe‑DWG‑Datei und den Namen der Ausgabedatei (PDF) fest.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Schritt 2: `PdfOptions`‑Instanz erstellen (PDF‑Optionen festlegen)

`PdfOptions` ermöglicht es Ihnen, zu steuern, wie das PDF erzeugt wird, z. B. Seitengröße, Kompression und Metadaten.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Schritt 3: DWG‑Datei laden

Laden Sie das DWG als `CadImage`, damit Sie dessen Entitäten inspizieren können.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Schritt 4: Durch Entitäten iterieren

Durchlaufen Sie jede Entität in der Zeichnung, um das DGN‑Underlay zu finden.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Schritt 5: Entitätstyp prüfen (wie DGN exportieren)

Identifizieren Sie, ob die aktuelle Entität ein DGN‑Underlay ist.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Schritt 6: Unterlage‑Pfad abrufen

Rufen Sie den externen Referenzpfad der DGN‑Datei ab.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Schritt 7: Rasterisierungsoptionen festlegen (DWG zu PDF konvertieren)

Konfigurieren Sie, wie das DWG rasterisiert wird, bevor es in das PDF eingefügt wird.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Schritt 8: DWG nach PDF exportieren

Speichern Sie schließlich das gerenderte Bild als PDF‑Datei.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| **`Image.Load` wirft „File not found“** | Falscher Pfad oder fehlende Datei. | Verwenden Sie einen absoluten Pfad oder stellen Sie sicher, dass das DWG in den Ausgabepfad kopiert wird. |
| **Underlay‑Pfad ist leer** | DGN‑Underlay nicht eingebettet oder Referenz defekt. | Prüfen Sie, ob das DWG tatsächlich ein DGN‑Underlay enthält und ob die externe DGN‑Datei zugänglich ist. |
| **PDF‑Ausgabe ist leer** | Rasterisierungsoptionen auf Größe 0 gesetzt. | Passen Sie `PageWidth`/`PageHeight` an oder setzen Sie `NoScaling = false`. |
| **Lizenzausnahme** | Ausführung ohne gültige Aspose.CAD‑Lizenz. | Lizenz vor dem Laden des Bildes anwenden: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für .NET in meinen kommerziellen Projekten verwenden?
A1: Ja, das können Sie. Besuchen Sie [hier](https://purchase.aspose.com/buy), um Lizenzoptionen zu prüfen.

### Q2: Gibt es Beschränkungen hinsichtlich der Größe von DWG‑Dateien, die ich verarbeiten kann?
A2: Aspose.CAD unterstützt die Verarbeitung großer DWG‑Dateien, jedoch können hardwareseitige Grenzen gelten.

### Q3: Gibt es eine Testversion?
A3: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Wie erhalte ich temporäre Lizenzen?
A4: Temporäre Lizenzen können Sie [hier](https://purchase.aspose.com/temporary-license/) beziehen.

### Q5: Wo finde ich Unterstützung, wenn ich auf Probleme stoße?
A5: Sie können das Aspose.CAD‑Forum [hier](https://forum.aspose.com/c/cad/19) für Support besuchen.

**F: Wie setze ich zusätzliche PDF‑Metadaten (Autor, Titel usw.)?**  
A: Verwenden Sie die Eigenschaften `exportOptions.Metadata` bevor Sie `Save` aufrufen.

**F: Kann ich mehrere Layouts in separate PDF‑Seiten exportieren?**  
A: Ja – setzen Sie `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**F: Unterstützt Aspose.CAD die Konvertierung von DWG in andere Bildformate?**  
A: Absolut. Sie können zu PNG, JPEG, SVG und mehr exportieren, indem Sie die entsprechenden `Image.Save`‑Überladungen nutzen.

---

**Zuletzt aktualisiert:** 2026-03-21  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}