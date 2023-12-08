---
title: STL-zu-PNG-Konvertierung leicht gemacht mit Aspose.CAD für .NET
linktitle: STL-Dateien nach PNG exportieren
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Konvertieren Sie STL-Dateien mühelos in PNG mit Aspose.CAD für .NET. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration. Jetzt downloaden!
type: docs
weight: 10
url: /de/net/stl-file-export/exporting-stl-files-to-png/
---
## Einführung
In der dynamischen Welt des computergestützten Designs (CAD) ist eine effiziente Dateikonvertierung von entscheidender Bedeutung. Aspose.CAD für .NET ist ein leistungsstarkes Toolkit, das den Export von STL-Dateien nach PNG vereinfacht und Entwicklern die Flexibilität und Funktionalität bietet, die sie benötigen. Dieses Tutorial führt Sie Schritt für Schritt durch den Prozess und gewährleistet einen reibungslosen Übergang von STL zu PNG mit Aspose.CAD.
## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie Folgendes eingerichtet haben:
1.  Aspose.CAD für .NET: Laden Sie die Aspose.CAD-Bibliothek herunter und installieren Sie sie. Du kannst es finden[Hier](https://releases.aspose.com/cad/net/).
2. Entwicklungsumgebung: Richten Sie Ihre bevorzugte .NET-Entwicklungsumgebung ein.
3. STL-Datei: Halten Sie eine STL-Datei zur Konvertierung bereit. Für dieses Tutorial verwenden wir eine Beispieldatei mit dem Namen „galeon.stl“.
## Namespaces importieren
Um den Prozess zu starten, importieren Sie die erforderlichen Namespaces in Ihre .NET-Anwendung. Dadurch wird sichergestellt, dass Sie Zugriff auf die Klassen und Methoden haben, die für die Konvertierung von STL in PNG erforderlich sind.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## Schritt 1: Definieren Sie das Verzeichnis und den Quelldateipfad
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
Stellen Sie sicher, dass Sie „Ihr Dokumentverzeichnis“ durch den tatsächlichen Verzeichnispfad ersetzen, in dem sich Ihre STL-Datei befindet.
## Schritt 2: Laden Sie das CAD-Bild
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Innerhalb dieses Blocks werden weitere Schritte ausgeführt
}
```
In diesem Schritt wird die STL-Datei als CAD-Bild geladen, sodass Sie sie bearbeiten und exportieren können.
## Schritt 3: Rasterisierungsoptionen festlegen
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
Passen Sie die Seitenbreite und -höhe entsprechend Ihren Vorlieben und Anforderungen an. Diese Einstellungen bestimmen die Abmessungen des exportierten PNG.
## Schritt 4: PNG-Optionen konfigurieren
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
Erstellen Sie PNG-Optionen und integrieren Sie dabei die im vorherigen Schritt definierten Rasterungseinstellungen.
## Schritt 5: Speichern Sie die PNG-Datei
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
Geben Sie den Ausgabepfad für die PNG-Datei an und speichern Sie das CAD-Bild mithilfe der bereitgestellten Optionen im PNG-Format.
Wiederholen Sie diese Schritte nach Bedarf für Ihren spezifischen Anwendungsfall, und Sie werden STL-Dateien mit Aspose.CAD für .NET erfolgreich in PNG exportieren.
## Abschluss
Aspose.CAD für .NET vereinfacht die komplizierte Aufgabe der Konvertierung von STL-Dateien in PNG und stellt Entwicklern ein zuverlässiges Toolkit zur Verfügung. Wenn Sie dieser Schritt-für-Schritt-Anleitung folgen, können Sie diese Funktionalität nahtlos in Ihre Anwendungen integrieren.
## FAQs
### F: Kann ich die Abmessungen des exportierten PNG anpassen?
 Absolut! Passen Sie in Schritt 3 an`PageWidth` Und`PageHeight` Werte entsprechend Ihren spezifischen Anforderungen.
### F: Ist zu Testzwecken eine temporäre Lizenz verfügbar?
 Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/) zum Testen und Bewerten.
### F: Wo finde ich zusätzlichen Support oder Community-Diskussionen?
 Besuche den[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Unterstützung und gemeinsame Diskussionen.
### F: Werden andere Dateiformate für die Konvertierung unterstützt?
 Ja, Aspose.CAD unterstützt verschiedene CAD-Formate über STL hinaus. Siehe die[Dokumentation](https://reference.aspose.com/cad/net/) für eine umfassende Liste.
### F: Kann ich mehrere STL-Dateien stapelweise verarbeiten?
Sicherlich! Implementieren Sie eine Schleife basierend auf den bereitgestellten Schritten, um mehrere STL-Dateien stapelweise zu verarbeiten.