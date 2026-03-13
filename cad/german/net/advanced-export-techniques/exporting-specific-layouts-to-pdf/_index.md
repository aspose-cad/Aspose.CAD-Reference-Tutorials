---
date: 2026-03-13
description: Erfahren Sie, wie Sie CAD‑Rasterisierungsoptionen festlegen und bestimmte
  DWG‑Layouts mit Aspose.CAD für .NET in PDF exportieren – der ultimative Leitfaden
  zur Erstellung von PDFs aus CAD‑Dateien.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD-Rasterisierungsoptionen festlegen – Bestimmte Layouts als PDF exportieren
  – Aspose.CAD‑Leitfaden
url: /de/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren spezifischer Layouts nach PDF – Aspose.CAD‑Leitfaden

## Einleitung

In diesem Tutorial erfahren Sie **wie man CAD‑Rasterisierungsoptionen festlegt**, sodass Sie ein einzelnes Layout – oder mehrere Layouts – aus einer DWG‑Datei direkt nach PDF exportieren können. Aspose.CAD für .NET macht den *dwg to pdf conversion c#* Prozess unkompliziert und gibt Ihnen die volle Kontrolle über Seitengröße, Auflösung und Layoutauswahl. Am Ende des Leitfadens können Sie **PDF aus CAD‑Datei erstellen** mit nur wenigen Codezeilen.

## Schnelle Antworten
- **Was bewirkt „set cad rasterization options“?**  
  Es teilt Aspose.CAD mit, wie Vektordaten (Layouts, Ebenen, Linienstärken) in gerasterte PDF‑Seiten gerendert werden.  
- **Welche Methode exportiert ein DWG‑Layout nach PDF?**  
  Verwenden Sie `Image.Save` mit konfigurierten `PdfOptions`, die Ihre `CadRasterizationOptions` enthalten.  
- **Kann ich mehr als ein Layout gleichzeitig exportieren?**  
  Ja – geben Sie ein Array von Layout‑Namen in der Eigenschaft `Layouts` an.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?**  
  Eine kommerzielle Lizenz ist erforderlich; ein kostenloser Testzeitraum steht zur Evaluierung bereit.  
- **Welche .NET‑Versionen werden unterstützt?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 und später.

## Was bedeutet „set cad rasterization options“?

`CadRasterizationOptions` ist die Klasse, die steuert, wie CAD‑Entitäten beim Konvertieren in rasterbasierte Formate wie PDF gerastert werden. Durch das Konfigurieren ihrer Eigenschaften – Seitengrößen, Layoutauswahl, Hintergrundfarbe usw. – bestimmen Sie das visuelle Ergebnis der **export dwg layout to pdf**‑Operation.

## Warum CAD‑Rasterisierungsoptionen festlegen?

- **Präzision** – Bewahren Sie Linienstärken und Maßstäbe exakt so, wie sie in der ursprünglichen CAD‑Zeichnung erscheinen.  
- **Leistung** – Rendern Sie nur die Layouts, die Sie benötigen, wodurch Dateigröße und Verarbeitungszeit reduziert werden.  
- **Flexibilität** – Passen Sie Seitenbreite/Höhe, DPI und Hintergrund an Ihre Berichtsstandards an.  

## Voraussetzungen

Bevor wir in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD für .NET** installiert. Sie können es [hier](https://releases.aspose.com/cad/net/) herunterladen.  
- Eine .NET‑Entwicklungsumgebung (Visual Studio, VS Code oder eine beliebige IDE Ihrer Wahl).  
- Eine DWG‑Datei, die mindestens ein Layout enthält (die hier verwendete Beispieldatei heißt `visualization_-_conference_room.dwg`).

## Namespaces importieren

Importieren Sie in Ihrem .NET‑Projekt die erforderlichen Namespaces für Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: DWG‑Datei laden

Zuerst geben Sie Aspose.CAD die Quell‑DWG‑Datei an, die Sie konvertieren möchten.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Schritt 2: **CadRasterizationOptions** festlegen

Hier konfigurieren wir die Rasterisierungseinstellungen, die die PDF‑Seitengröße und Auflösung bestimmen.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro‑Tipp:** Passen Sie `PageWidth` und `PageHeight` an die Abmessungen Ihres Ziel‑PDF‑Layouts an. Größere Werte erhöhen die Detailgenauigkeit, vergrößern jedoch auch die Dateigröße.

### Schritt 3: Layout‑Name angeben

Teilen Sie Aspose.CAD mit, welches Layout(s) gerendert werden soll. Ersetzen Sie `"Layout1"` durch den genauen Namen des Layouts in Ihrer DWG‑Datei.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Warum das wichtig ist:** Durch das Begrenzen des `Layouts`‑Arrays vermeiden Sie das Exportieren unerwünschter Blätter, wodurch die **dwg to pdf conversion c#**‑Operation schneller und das resultierende PDF sauberer wird.

### Schritt 4: `PdfOptions` erstellen

Verknüpfen Sie die Rasterisierungseinstellungen mit den PDF‑Exportoptionen.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Schritt 5: Export nach PDF

Speichern Sie schließlich das gerenderte Layout als PDF‑Datei.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Schritt 6: Erfolgsnachricht anzeigen

Eine kurze Konsolenausgabe bestätigt, dass die Operation erfolgreich war.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Häufige Probleme & Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| **Kein PDF erzeugt** | `Layouts`‑Array stimmt mit keinem Layout‑Namen in der DWG überein. | Überprüfen Sie die Layout‑Namen mit einem CAD‑Viewer und aktualisieren Sie die Eigenschaft `Layouts`. |
| **Leere Seiten** | `PageWidth`/`PageHeight` auf 0 oder extrem kleine Werte gesetzt. | Verwenden Sie realistische Abmessungen (z. B. 1600 × 1600) oder lassen Sie Aspose automatisch berechnen, indem Sie diese Eigenschaften weglassen. |
| **Falsche Skalierung** | DPI nicht gesetzt, wenn hochauflösende Ausgabe erforderlich ist. | Setzen Sie `rasterizationOptions.Resolution = 300;` (oder gewünschte DPI) vor dem Export. |

## Häufig gestellte Fragen

**F: Kann ich mehrere Layouts gleichzeitig exportieren?**  
A: Ja, ändern Sie einfach das `Layouts`‑Array in Schritt 3, um alle gewünschten Layout‑Namen einzuschließen, z. B. `new string[] { "Layout1", "Layout2" }`.

**F: Ist Aspose.CAD mit anderen CAD‑Dateiformaten kompatibel?**  
A: Absolut. Es unterstützt DWG, DXF, DWF, DGN und viele weitere Formate.

**F: Wie kann ich die PDF‑Ausgabeeinstellungen über die Seitengröße hinaus anpassen?**  
A: Erkunden Sie zusätzliche Eigenschaften von `CadRasterizationOptions` wie `Resolution`, `BackgroundColor` und `DrawType`, um das Ergebnis fein abzustimmen.

**F: Wo finde ich weitere Aspose.CAD‑Dokumentation?**  
A: Besuchen Sie die [Dokumentation](https://reference.aspose.com/cad/net/) für ausführliche API‑Referenzen und Beispiele.

**F: Gibt es eine kostenlose Testversion?**  
A: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) nutzen.

## Fazit

Sie haben nun gelernt, wie man **CAD‑Rasterisierungsoptionen festlegt** und sie verwendet, um **spezifische DWG‑Layouts nach PDF zu exportieren** mit Aspose.CAD für .NET. Dieser Ansatz gibt Ihnen präzise Kontrolle über den Konvertierungsprozess und ermöglicht es Ihnen, CAD‑zu‑PDF‑Funktionalität schnell und zuverlässig in jede C#‑Anwendung zu integrieren.

---

**Zuletzt aktualisiert:** 2026-03-13  
**Getestet mit:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}