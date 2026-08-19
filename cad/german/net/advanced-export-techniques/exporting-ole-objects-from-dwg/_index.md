---
description: Erfahren Sie, wie Sie DWG in PNG konvertieren und OLE‑Objekte aus DWG‑Dateien
  mit Aspose.CAD für .NET extrahieren – ein kurzer, code‑zentrierter Leitfaden.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG in PNG konvertieren & OLE‑Objekte exportieren – Aspose.CAD‑Tutorial
url: /de/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

 elements.

Check code block placeholders: they are not fenced code blocks, but placeholders. The requirement says preserve code blocks. There are no actual fenced code blocks except placeholders. So fine.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von OLE-Objekten aus DWG-Dateien – Aspose.CAD Tutorial

## Einführung

Wenn Sie **DWG zu PNG konvertieren** müssen, während Sie eingebettete OLE‑Objekte extrahieren, sind Sie hier genau richtig. Aspose.CAD für .NET macht diesen zweistufigen Prozess unkompliziert und ermöglicht Ihnen die Automatisierung von Extraktion und Rasterisierung mit nur wenigen Zeilen C#. In den nächsten Minuten führen wir Sie durch den gesamten Workflow, von der Einrichtung Ihrer Umgebung bis zum Speichern jeder DWG als PNG, das die extrahierten OLE‑Daten enthält.

## Schnelle Antworten
- **Worum geht es in diesem Tutorial?** Konvertierung von DWG zu PNG und Extraktion von OLE‑Objekten mit Aspose.CAD für .NET.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Entwicklung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Kann ich mehrere DWG‑Dateien gleichzeitig verarbeiten?** Ja – das Beispiel durchläuft ein Array von Dateinamen.  
- **Wo finde ich weitere Beispiele?** Siehe die offizielle Aspose.CAD‑Dokumentation und die Forum‑Links unten.

## Was ist **convert DWG to PNG**?
Die Konvertierung einer DWG (AutoCAD‑Zeichnung) in ein PNG‑Bild rastert die Vektordaten, sodass sie leicht in Webseiten, Berichten oder anderen Anwendungen angezeigt oder eingebettet werden können, die DWG nicht nativ unterstützen. Wenn OLE‑Objekte vorhanden sind, können sie während der Konvertierung extrahiert und als separate Assets gespeichert werden.

## Warum OLE‑Objekte aus CAD‑Dateien extrahieren?
Viele DWG‑Zeichnungen betten Tabellenkalkulationen, Diagramme oder andere Office‑Dokumente als OLE‑Objekte ein. Durch deren Extraktion können Sie die Originaldaten wiederverwenden, Berichte automatisieren oder Inhalte in neuere Formate migrieren, ohne eingebettete Informationen zu verlieren.

## Voraussetzungen

- Aspose.CAD für .NET Bibliothek: Stellen Sie sicher, dass die Bibliothek installiert ist. Sie können sie von der [Aspose.CAD für .NET Download‑Seite](https://releases.aspose.com/cad/net/) herunterladen.
- Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre DWG‑Dateien gespeichert sind. Ersetzen Sie `"Your Document Directory"` im bereitgestellten Code‑Snippet durch den tatsächlichen Pfad.

## Namespaces importieren

In Ihrem .NET‑Projekt importieren Sie die erforderlichen Namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Dokumentverzeichnis festlegen

```csharp
string MyDir = "Your Document Directory";
```

Ersetzen Sie `"Your Document Directory"` durch den Pfad, in dem sich Ihre DWG‑Dateien befinden.

### Schritt 2: Auflisten der DWG‑Dateien, die Sie verarbeiten möchten

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Schritt 3: Exportoptionen für die PNG‑Konvertierung konfigurieren

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Sie können `CadRasterizationOptions` (z. B. `PageWidth`, `PageHeight`, `BackgroundColor`) anpassen, um die gewünschte Ausgaberesolution zu erreichen.

### Schritt 4: Durch jede DWG iterieren und die Konvertierung durchführen

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Während dieser Schleife extrahiert die Bibliothek automatisch **OLE‑Objekte**, die in jeder Zeichnung eingebettet sind, und fügt sie dem erzeugten PNG hinzu. Wenn Sie die rohen OLE‑Streams benötigen, können Sie auf die Sammlung `cadImage.OleObjects` zugreifen – ein praktischer Weg, um **how to extract ole** Daten programmgesteuert zu erhalten.

## Häufige Probleme & Fehlersuche

- **Fehlender Layout‑Name** – Stellen Sie sicher, dass das von Ihnen angegebene Layout (`"Layout1"` im Beispiel) in der Quell‑DWG existiert; andernfalls greift der Rasterizer auf den Standard‑Modellraum zurück.
- **Große Dateien verursachen Speicherbelastung** – Verarbeiten Sie Dateien einzeln (wie gezeigt) und geben Sie `CadImage`‑Objekte sofort mit `using` frei.
- **Unerwartete Farben** – Setzen Sie `rasterizationOptions.BackgroundColor` auf die Hintergrundfarbe der Zeichnung, falls Transparenz benötigt wird.

## Häufig gestellte Fragen

### Q1: Ist Aspose.CAD für .NET sowohl für Junior‑ als auch Senior‑CAD‑Dateien geeignet?

A1: Ja, Aspose.CAD für .NET ist vielseitig und kann ein breites Spektrum an CAD‑Dateien verarbeiten, einschließlich sowohl Junior‑ als auch Senior‑Varianten.

### Q2: Kann ich Exportoptionen für verschiedene Layouts anpassen?

A2: Auf jeden Fall! Wie im Tutorial gezeigt, können Sie Exportoptionen, einschließlich Layouts, an Ihre spezifischen Anforderungen anpassen.

### Q3: Wo finde ich die ausführliche Dokumentation für Aspose.CAD für .NET?

A3: Durchsuchen Sie die [Aspose.CAD für .NET Dokumentation](https://reference.aspose.com/cad/net/) für ausführliche Informationen und Beispiele.

### Q4: Gibt es eine kostenlose Testversion?

A4: Ja, Sie können die Funktionen von Aspose.CAD für .NET mit einer kostenlosen Testversion ausprobieren. Besuchen Sie [diesen Link](https://releases.aspose.com/), um zu beginnen.

### Q5: Wie kann ich Support erhalten oder mich mit der Community vernetzen?

A5: Für Support und Community‑Austausch besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19).

### Q6: Wie extrahiere ich **OLE aus CAD**‑Dateien, ohne zu PNG zu konvertieren?

A6: Verwenden Sie nach dem Laden der DWG die Sammlung `CadImage.OleObjects`; Sie können durch jedes `OleObject` iterieren und dessen Rohdaten in einer Datei speichern.

## Fazit

Sie haben nun gesehen, wie Sie **DWG zu PNG konvertieren** und dabei nahtlos **OLE‑Objekte extrahieren** können, indem Sie Aspose.CAD für .NET verwenden. Dieser Ansatz spart Zeit, eliminiert manuelle Kopier‑ und Einfüge‑Schritte und lässt sich sauber in automatisierte Pipelines integrieren. Experimentieren Sie gern mit anderen Rasterformaten (JPEG, BMP) oder erkunden Sie das umfangreiche Set an CAD‑Manipulationsfunktionen, das Aspose bietet.

---

**Zuletzt aktualisiert:** 2026-03-13  
**Getestet mit:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}