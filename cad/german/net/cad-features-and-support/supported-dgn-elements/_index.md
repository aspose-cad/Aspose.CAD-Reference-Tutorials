---
date: 2026-03-29
description: Erfahren Sie, wie Sie DGN mit Aspose.CAD für .NET in PNG konvertieren.
  Dieser Leitfaden behandelt außerdem die Unterstützung von CAD‑Dateiformaten und
  das vollständige Set unterstützter DGN‑Elemente.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN in PNG konvertieren mit Aspose.CAD für .NET
url: /de/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert DGN to PNG mit Aspose.CAD für .NET

## Einführung

Sind Sie ein .NET‑Entwickler, der **DGN in PNG** nahtlos konvertieren möchte? Aspose.CAD für .NET bietet eine robuste Lösung zum effizienten Umgang mit DGN‑Dateien. In diesem Tutorial gehen wir auf die unterstützten DGN‑Elemente ein, führen Sie durch den Prozess der Arbeit mit Aspose.CAD für .NET und zeigen Ihnen genau, wie Sie diese Elemente in PNG‑Bilder exportieren.

## Schnelle Antworten
- **Was macht Aspose.CAD?** Es liest, ändert und konvertiert CAD/BIM‑Dateien (einschließlich DGN) in Rasterformate wie PNG.  
- **Kann ich 2D‑ und 3D‑DGN‑Elemente konvertieren?** Ja – sowohl 2‑D‑ als auch 3‑D‑Entitäten werden unterstützt.  
- **Welche .NET‑Versionen werden benötigt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Benötige ich eine Lizenz für Tests?** Eine kostenlose Testversion ist verfügbar; für die Produktion ist eine Lizenz erforderlich.  
- **Wo bekomme ich die Bibliothek?** Laden Sie sie von der offiziellen Aspose‑Website herunter (Link unten).

## Was bedeutet „DGN in PNG konvertieren“?
Das Konvertieren von DGN in PNG bedeutet, die vektorbasierte DGN‑Zeichnung (2‑D oder 3‑D) in ein Rasterbildformat (PNG) zu rendern. Dies ist nützlich, wenn Sie CAD‑Zeichnungen im Web anzeigen, in Berichte einbetten oder Miniaturansichten erzeugen möchten, ohne einen CAD‑Viewer zu benötigen.

## Warum Aspose.CAD für .NET für die Unterstützung von CAD‑Dateiformaten verwenden?
- **Vollständige CAD‑Dateiformatunterstützung** – DGN, DWG, DXF, DWF und mehr.  
- **Keine externen Abhängigkeiten** – reine .NET‑Bibliothek, keine nativen CAD‑Installationen.  
- **Hochpräzises Rendering** – bewahrt Linienstärken, Farben und 3‑D‑Geometrie.  
- **Batch‑Verarbeitung** – einfach viele Dateien in einer serverseitigen Anwendung durchlaufen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- Grundkenntnisse in .NET‑Programmierung.  
- Visual Studio auf Ihrem Rechner installiert.  
- Aspose.CAD für .NET Bibliothek, die Sie [hier](https://releases.aspose.com/cad/net/) herunterladen können.

## Namespaces importieren

Um Ihr Projekt zu starten, importieren Sie die erforderlichen Namespaces in Ihre .NET‑Anwendung. Dieser Schritt stellt sicher, dass Sie Zugriff auf die von Aspose.CAD für .NET bereitgestellten Funktionen haben.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Wie man DGN in PNG konvertiert

Im Folgenden finden Sie eine Schritt‑für‑Schritt‑Anleitung, die Sie durch das Laden einer DGN‑Datei, das Durchlaufen ihrer Elemente, die Behandlung von 2‑D‑ und 3‑D‑Entitäten und schließlich den Export des Ergebnisses in ein PNG‑Rasterbild führt.

### Schritt 1: DGN‑Datei laden

Beginnen Sie damit, eine vorhandene DGN‑Datei als `DgnImage` in Ihrer .NET‑Anwendung zu laden.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Schritt 2: Durch DGN‑Elemente iterieren

Iterieren Sie durch die DGN‑Elemente mit einer `foreach`‑Schleife. Aspose.CAD für .NET bietet eine Vielzahl von DGN‑Elementtypen, mit denen Sie arbeiten können.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Schritt 3: Früher unterstützte 2‑D‑Entitäten verarbeiten

Diese Entitäten werden jetzt auch für das 3‑D‑Rendering unterstützt. Die Switch‑Anweisung ermöglicht es Ihnen, die Logik basierend auf dem Elementtyp zu verzweigen.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Schritt 4: Unterstützte 3‑D‑Entitäten verarbeiten

Aspose.CAD fügt volle Unterstützung für mehrere 3‑D‑DGN‑Elemente hinzu. Erweitern Sie die Switch‑Anweisung, um sie bei Bedarf zu verarbeiten.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Schritt 5: Exportieren und als PNG speichern

Nach allen erforderlichen Manipulationen exportieren Sie die DGN‑Zeichnung in ein PNG‑Rasterbild und speichern sie im angegebenen Verzeichnis.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro Tipp:** Verwenden Sie `Image.Save` mit `new PngOptions()`, um Auflösung, Hintergrundfarbe und weitere PNG‑spezifische Einstellungen zu steuern.

## Übersicht der CAD‑Dateiformatunterstützung

Aspose.CAD für .NET ist nicht nur auf DGN beschränkt. Es unterstützt auch DWG, DXF, DWF und viele andere CAD‑Formate und bietet Ihnen eine einheitliche API zur Handhabung eines breiten Spektrums von Konstruktionszeichnungen. Das macht es ideal für Projekte, die **CAD‑Dateiformatunterstützung** über mehrere Standards hinweg benötigen.

## Häufige Probleme & Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| **Bild erscheint leer** | Exportiert mit 0 DPI | Geben Sie `ResolutionX` und `ResolutionY` in `PngOptions` an. |
| **Fehlende 3‑D‑Geometrie** | Elementtyp im Switch nicht behandelt | Fügen Sie den fehlenden `DgnElementType`‑Fall hinzu und rendern Sie entsprechend. |
| **Speicherüberlauf bei großen Dateien** | Laden der gesamten Datei auf einmal | Verarbeiten Sie Elemente in Batches oder verwenden Sie nach Möglichkeit Streaming. |

## Häufig gestellte Fragen

### Q1: Wo finde ich die Dokumentation für Aspose.CAD für .NET?
A1: Sie finden die Dokumentation [hier](https://reference.aspose.com/cad/net/).

### Q2: Wie lade ich Aspose.CAD für .NET herunter?
A2: Sie können die Bibliothek [hier](https://releases.aspose.com/cad/net/) herunterladen.

### Q3: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?
A3: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) nutzen.

### Q4: Wo kann ich temporäre Lizenzen für Aspose.CAD für .NET erhalten?
A4: Temporäre Lizenzen sind [hier](https://purchase.aspose.com/temporary-license/) verfügbar.

### Q5: Brauchen Sie Hilfe oder haben Sie Fragen?
A5: Besuchen Sie das Aspose.CAD für .NET Community‑[Support‑Forum](https://forum.aspose.com/c/cad/19).

---

**Zuletzt aktualisiert:** 2026-03-29  
**Getestet mit:** Aspose.CAD für .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}