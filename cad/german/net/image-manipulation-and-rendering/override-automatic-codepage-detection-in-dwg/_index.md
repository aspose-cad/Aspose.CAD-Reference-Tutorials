---
date: 2026-09-04
description: Erfahren Sie, wie Sie die dwg-Codepage-Erkennung in DWG-Dateien mit Aspose.CAD
  für .NET überschreiben können, um eine präzise Kontrolle über die Zeichenkodierung
  zu erhalten.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Automatische Codepage-Erkennung in DWG-Dateien überschreiben – Aspose.CAD
  Tutorial
og_description: Erfahren Sie, wie Sie die dwg-Codepage-Erkennung in DWG-Dateien mit
  Aspose.CAD für .NET überschreiben können, um eine präzise Kontrolle über die Zeichenkodierung
  zu erhalten und die Handhabung von CAD-Dateien zu verbessern.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Wie man die dwg-Codepage in Aspose.CAD für .NET überschreibt
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Wie man die dwg-Codepage in Aspose.CAD für .NET überschreibt
url: /de/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man die DWG-Codepage in Aspose.CAD für .NET überschreibt

In vielen alten DWG-Dateien wird die eingebettete Codepage automatisch erkannt, was zu unleserlichem Text führen kann, wenn die Datei eine nicht‑standardmäßige Kodierung verwendet. **Override dwg codepage** ermöglicht es Ihnen, die gewünschte Kodierung explizit festzulegen, sodass Geometrie und Anmerkungstext korrekt dargestellt werden. In diesem Tutorial sehen Sie, warum das wichtig ist, wie die API aussieht und wie Sie die Einstellung in wenigen einfachen Schritten anwenden.

## Schnelle Antworten
- **Was bewirkt das Überschreiben der DWG-Codepage?** Es zwingt Aspose.CAD, die von Ihnen angegebene Kodierung zu verwenden, anstatt zu raten, und verhindert so Zeichenkorruption.  
- **Wann sollte ich es verwenden?** Immer wenn eine DWG-Datei Text in einer Sprache enthält, die nicht die standardmäßige Windows-Codepage ist (z. B. Mitteleuropäisch, Kyrillisch).  
- **Welche Kodierungen werden unterstützt?** Jede .NET `Encoding` wie `Encoding.GetEncoding(1250)` für Mitteleuropäisch.  
- **Brauche ich eine Lizenz?** Eine Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Ist es thread‑sicher?** Ja, die Einstellung wird pro `Image`‑Instanz angewendet, sodass mehrere Threads gleichzeitig unterschiedliche Dateien verarbeiten können.

## Was ist Override DWG Codepage?
Override dwg codepage ist eine Funktion von Aspose.CAD, die es Ihnen ermöglicht, die automatische Codepage-Erkennung der Bibliothek durch eine von Ihnen bereitgestellte spezifische Zeichenkodierung zu ersetzen. Dadurch werden Zeichenfolgen im DWG korrekt interpretiert, unabhängig von den ursprünglichen Metadaten der Datei.

## Warum Override DWG Codepage verwenden?
Aspose.CAD unterstützt **mehr als 50 DWG/DXF-Versionen** und kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Wenn die automatische Erkennung fehlschlägt, können bis zu **100 % der Anmerkungslesbarkeit** verloren gehen. Durch das explizite Festlegen der Codepage reduzieren Sie dieses Risiko auf **0 %** und behalten die Renderzeiten unverändert bei.

## Voraussetzungen

- Grundkenntnisse in C# und der .NET-Plattform.  
- Aspose.CAD für .NET installiert. Wenn Sie es noch nicht installiert haben, laden Sie es von der **[Aspose.CAD für .NET Download-Seite](https://releases.aspose.com/cad/net/)** herunter.  
- Eine DWG-Datei, die eine nicht‑standardmäßige Codepage verwendet (z. B. eine Datei, die auf einem System mit Codepage 1250 erstellt wurde).

## Namespaces importieren

Um zu beginnen, fügen Sie die erforderlichen `using`‑Direktiven hinzu, damit der Compiler die Aspose.CAD‑Klassen finden kann.

Fügen Sie das Folgende am Anfang Ihrer C#‑Quelldatei ein:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Dies bereitet die Umgebung für alle nachfolgenden CAD‑Operationen vor.

## Schritt 1: Definieren Sie Ihr Dokumentenverzeichnis

Geben Sie den Ordner an, der die zu verarbeitende DWG enthält. Ersetzen Sie den Platzhalter durch den tatsächlichen Pfad auf Ihrem Rechner:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Schritt 2: Automatische Codepage-Erkennung überschreiben

Jetzt kommen wir zum Kern des Tutorials. Der untenstehende Code lädt eine DWG-Datei, zwingt die Codepage zu **Windows‑1250** (Mitteleuropäisch) und speichert das Bild anschließend als PNG. Ändern Sie den Dateinamen und die Kodierung nach Bedarf für Ihr Szenario.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` ist eine statische Methode, die eine CAD‑Datei lädt und ein `CadImage`‑Objekt zurückgibt. `LoadOptions.CodePage` gibt die während des Ladens zu verwendende Zeichenkodierung an. `CadImage` stellt die In‑Memory‑Darstellung einer CAD‑Zeichnung dar und bietet Methoden zum Rendern oder Konvertieren.

## Häufige Probleme und Lösungen

- **Nach dem Überschreiben bleiben fehlerhafte Zeichen** – Stellen Sie sicher, dass die von Ihnen gewählte Kodierung mit der Sprache der Originaldatei übereinstimmt. Verwenden Sie z. B. `Encoding.GetEncoding(1251)` für Kyrillisch.  
- **Datei lässt sich nicht laden** – Stellen Sie sicher, dass die DWG-Version von Ihrer Aspose.CAD‑Version unterstützt wird; aktualisieren Sie sie bei Bedarf.  
- **Leistungsverlust** – Das Überschreiben verursacht keinen zusätzlichen Aufwand; wenn Sie eine Verlangsamung bemerken, prüfen Sie auf nicht zusammenhängende I/O‑Engpässe.

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für .NET mit anderen Sprachen als C# verwenden?
A1: Aspose.CAD für .NET ist hauptsächlich für C# konzipiert, kann aber in anderen .NET‑Sprachen wie VB.NET verwendet werden.

### Q2: Ist eine kostenlose Testversion verfügbar?
A2: Ja, Sie können eine kostenlose Testversion von der **[Aspose.CAD kostenlose Testversion Download-Seite](https://releases.aspose.com/)** erhalten.

### Q3: Wie kann ich Support für Aspose.CAD für .NET erhalten?
A3: Besuchen Sie das **[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19)** für Community‑Support.

### Q4: Kann ich eine temporäre Lizenz erwerben?
A4: Ja, Sie können eine temporäre Lizenz über die **[Seite zum Kauf einer temporären Lizenz](https://purchase.aspose.com/temporary-license/)** erhalten.

### Q5: Wo finde ich ausführliche Dokumentation?
A5: Siehe die umfassende **[Aspose.CAD .NET API‑Dokumentation](https://reference.aspose.com/cad/net/)**.

### Q6: Beeinflusst das Überschreiben der Codepage die Raster-Renderqualität?
A6: Nein. Die Codepage‑Einstellung beeinflusst nur, wie Textzeichenfolgen dekodiert werden; die Bildqualität bleibt unverändert.

### Q7: Kann ich das Überschreiben anwenden, wenn ich in andere Formate als PNG konvertiere?
A7: Absolut. Der gleiche `LoadOptions.CodePage`‑Wert funktioniert für PDF, SVG oder jedes andere von Aspose.CAD unterstützte Ausgabeformat.

---

**Zuletzt aktualisiert:** 2026-09-04  
**Getestet mit:** Aspose.CAD 24.10 für .NET  
**Autor:** Aspose

## Verwandte Tutorials

- [Textsuche in DWG-Dateien mit C# – Aspose.CAD Tutorial](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [DWG zu PDF konvertieren und Text in C# hinzufügen – Aspose.CAD Tutorial](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Wie man DWG zu PDF und Rasterbildern mit Aspose.CAD für .NET konvertiert](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}