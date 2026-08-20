---
date: 2026-04-06
description: Erfahren Sie, wie Sie DWG in PDF konvertieren und benutzerdefinierten
  Text mit C# und Aspose.CAD hinzufügen. Diese Schritt‑für‑Schritt‑Anleitung behandelt
  das Erzeugen von PDF aus DWG, das Einfügen einer Textelement und das Ändern der
  DWG‑Textschriftart.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Text zu DWG-Dateien in C# hinzufügen
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG zu PDF konvertieren und Text in C# hinzufügen – Aspose.CAD‑Tutorial
url: /de/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG in PDF konvertieren und Text in C# hinzufügen – Aspose.CAD Tutorial

## Einführung

In der schnelllebigen Welt von CAD und .NET-Entwicklung ist **die Konvertierung von DWG zu PDF** bei gleichzeitiger Einfügung benutzerdefinierter Anmerkungen ein häufiges Anliegen. Ob Sie druckbare Zeichnungen für Kunden erzeugen oder dynamische Notizen direkt in ein DWG einbetten müssen, Aspose.CAD macht die Arbeit unkompliziert. In diesem Tutorial lernen Sie, wie Sie **DWG zu PDF konvertieren**, **ein Textelement hinzufügen** und sogar **die DWG‑Textschriftart ändern** können – alles mit C#.

## Schnelle Antworten
- **Welche Bibliothek ist am besten für die DWG‑zu‑PDF-Konvertierung?** Aspose.CAD für .NET  
- **Kann ich beim Konvertieren benutzerdefinierten Text hinzufügen?** Ja – erstellen Sie ein `CadText`‑Objekt und fügen Sie es vor dem Speichern hinzu.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Eine kommerzielle Lizenz ist erforderlich; eine kostenlose Testversion ist verfügbar.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Ist es möglich, die Schriftart des Textes zu ändern?** Ja, passen Sie die `CadText`‑Eigenschaften wie `StyleType` und `TextHeight` an.

## Was bedeutet „DWG in PDF konvertieren“?

Das Konvertieren einer DWG‑Datei zu PDF wandelt eine vektorbasierte CAD‑Zeichnung in ein weit verbreitetes, geräteunabhängiges Dokument um. Das PDF behält die ursprüngliche Geometrie und die Ebenen bei, ermöglicht jedoch das Einbetten von Anmerkungen, Text oder anderen Metadaten. Aspose.CAD übernimmt die Rasterisierung und Vektorrechnung automatisch, sodass Sie keine Drittanbieter‑CAD‑Software auf dem Server benötigen.

## Warum Text zu einem DWG vor der Konvertierung hinzufügen?

Durch das direkte Einbetten von Text in das DWG erhalten Sie volle Kontrolle über Position, Stil und Ebenenzuweisung. Wenn die Datei später zu PDF konvertiert wird, erscheint der Text exakt dort, wo Sie ihn platziert haben, bewahrt die Design‑Intention und eliminiert Nachbearbeitungen in einem PDF‑Editor.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Aspose.CAD Bibliothek** – laden Sie sie von dem [download link](https://releases.aspose.com/cad/net/) herunter.  
- **Eine funktionierende .NET‑Umgebung** (Visual Studio 2022, .NET 6 oder eine kompatible Version).  
- **Ein Ordner für Ihre Testdateien** – wir werden im gesamten Leitfaden darauf als `MyDir` verweisen.

Jetzt gehen wir den Prozess Schritt für Schritt durch.

## Namespaces importieren

Fügen Sie die erforderlichen `using`‑Anweisungen hinzu, damit Sie auf die Aspose.CAD‑Klassen zugreifen können.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: DWG‑Datei laden

Laden Sie Ihre Quell‑DWG‑Datei in ein `Image`‑Objekt. Dieses Objekt gibt Ihnen Zugriff auf die zugrunde liegenden CAD‑Entitäten.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Schritt 2: CadText‑Objekt erstellen (Text‑Entität einfügen)

Die Klasse `CadText` stellt eine einzelne Textzeile in einem DWG dar. Hier setzen wir Stil, Wert, Farbe, Ebene und Position. Passen Sie `StyleType` oder `TextHeight` an, um die **DWG‑Textschriftart zu ändern**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Schritt 3: Text‑Entität zum Model Space hinzufügen

Der DWG‑Model‑Space enthält die meisten Zeichen‑Entitäten. Durch das Hinzufügen unseres `CadText` zum `*Model_Space`‑Block wird der Text Teil der Zeichnung.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Schritt 4: PDF‑Optionen konfigurieren (PDF aus DWG erzeugen)

Richten Sie Rasterisierungsoptionen ein, die steuern, wie das DWG in ein PDF gerendert wird. Sie können Seitengröße, Zeichentyp und Layout anpassen.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Schritt 5: Modifiziertes DWG als PDF speichern

Exportieren Sie schließlich die modifizierte Zeichnung. Das resultierende PDF enthält den neu eingefügten Text.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro Tipp:** Wenn Sie ein PDF mit höherer Auflösung benötigen, erhöhen Sie `PageHeight` und `PageWidth` proportional.

## Häufige Probleme & Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| Text erscheint nicht im PDF | Falsche Ebene oder Farb‑ID | Stellen Sie sicher, dass `LayerName` existiert und `ColorId` auf eine sichtbare Farbe (z. B. 7 für Weiß) gesetzt ist. |
| Text ist falsch positioniert | Falsche Ausrichtungskoordinaten | Überprüfen Sie die Werte von `FirstAlignment.X/Y` relativ zu den Einheiten der Zeichnung. |
| PDF ist leer | Rasterisierungsoptionen nicht gesetzt | Setzen Sie `DrawType` auf `UseObjectColor` oder `UseObjectLineWeight`. |

## Häufig gestellte Fragen (Vorhanden)

### Q1: Ist Aspose.CAD mit allen Versionen von DWG‑Dateien kompatibel?

A1: Aspose.CAD unterstützt eine breite Palette von DWG‑Dateiversionen und gewährleistet die Kompatibilität mit verschiedener CAD‑Software.

### Q2: Kann ich mit Aspose.CAD mehrere Text‑Entitäten zu einer einzelnen DWG‑Datei hinzufügen?

A2: Ja, Sie können mehrere Text‑Entitäten zu einer DWG‑Datei hinzufügen, indem Sie den im Tutorial beschriebenen Vorgang wiederholen.

### Q3: Wie kann ich die Textschriftart und den Stil in Aspose.CAD ändern?

A3: Um Schriftart und Stil zu ändern, passen Sie die Eigenschaften des `CadText`‑Objekts an, bevor Sie es zur DWG‑Datei hinzufügen.

### Q4: Gibt es Lizenzüberlegungen bei der Verwendung von Aspose.CAD in einem kommerziellen Projekt?

A5: Ja, stellen Sie die Einhaltung der Aspose.CAD‑Lizenzbedingungen sicher. Weitere Details finden Sie unter [Aspose.CAD Purchase](https://purchase.aspose.com/buy).

### Q5: Wo kann ich Hilfe erhalten oder Aspose.CAD‑bezogene Fragen diskutieren?

A5: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19), um mit der Community in Kontakt zu treten und Unterstützung zu erhalten.

## Zusätzliche FAQs

**F: Wie erstelle ich ein PDF aus DWG, ohne Text hinzuzufügen?**  
A: Überspringen Sie den Schritt zur Erstellung von `CadText` und konfigurieren Sie direkt `PdfOptions`, bevor Sie `image.Save(...)` aufrufen.

**F: Kann ich die Textfarbe programmgesteuert ändern?**  
A: Ja, setzen Sie `cadText.ColorId` auf eine bestimmte ACI‑Farbnummer (z. B. 1 für Rot).

**F: Ist das Einfügen von mehrzeiligem Text möglich?**  
A: Verwenden Sie `CadMText` für mehrzeilige Textblöcke; der Ansatz ist ähnlich wie bei `CadText`.

**F: Unterstützt Aspose.CAD die Batch‑Konvertierung mehrerer DWG‑Dateien?**  
A: Absolut – durchlaufen Sie ein Verzeichnis mit DWG‑Dateien, führen Sie dieselben Schritte aus und speichern Sie jede als PDF.

## Fazit

Sie haben nun einen vollständigen, produktionsreifen Workflow, um **DWG zu PDF zu konvertieren**, **benutzerdefinierten Text hinzuzufügen** und **das Erscheinungsbild des Textes** mit C# und Aspose.CAD anzupassen. Diese Technik eignet sich ideal für die automatisierte Zeichnungserstellung, Reporting‑Pipelines oder jedes Szenario, in dem Sie CAD‑Dateien on‑the‑fly anreichern müssen.

---

**Zuletzt aktualisiert:** 2026-04-06  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}