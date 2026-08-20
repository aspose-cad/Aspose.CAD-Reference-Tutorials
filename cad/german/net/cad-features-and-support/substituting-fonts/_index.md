---
date: 2026-03-29
description: Erfahren Sie, wie Sie Schriftarten in Aspose.CAD für .NET schnell ersetzen.
  Diese Schritt‑für‑Schritt‑Anleitung zeigt Ihnen, wie Sie den primären Schriftartnamen
  festlegen und CAD‑Zeichnungen effizient anpassen.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Wie man Schriftarten in Aspose.CAD für .NET ersetzt
url: /de/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Schriftarten in Aspose.CAD für .NET ersetzt

## Einführung

Im Bereich der CAD-Entwicklung mit .NET ist das Erlernen **wie man Schriftarten ersetzt** eine entscheidende Fähigkeit, die die visuelle Qualität Ihrer Zeichnungen dramatisch verbessern kann. Aspose.CAD für .NET bietet eine unkomplizierte API, mit der Sie **den primären Schriftnamen** für jeden Stil festlegen können, wodurch globale oder selektive Schriftartensubstitution zum Kinderspiel wird. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden einer Zeichnung bis zum Austauschen von Schriftarten, entweder global oder nach einem bestimmten Stilnamen.

## Schnelle Antworten
- **Was ist die Hauptklasse für die CAD-Manipulation?** `Aspose.CAD.Image` (oder die abgeleitete `CadImage`).
- **Welche Eigenschaft ändert die Schriftart?** `PrimaryFontName` auf `CadStyleTableObject`.
- **Kann ich Schriftarten für alle Stile auf einmal ersetzen?** Ja, iterieren Sie über `cadImage.Styles` und setzen Sie die Eigenschaft.
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.CAD-Lizenz ist für die Nutzung außerhalb der Testphase erforderlich.
- **Unterstützte .NET-Versionen?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Was ist Schriftartensubstitution in CAD?

Schriftartensubstitution bedeutet, den ursprünglichen Schriftschnitt, der in einer CAD-Zeichnung verwendet wird, durch einen anderen zu ersetzen, der auf dem Zielsystem verfügbar ist. Dies ist besonders nützlich, wenn die Originalschrift fehlt, wenn Sie einen einheitlichen Unternehmensstil benötigen oder wenn Sie Zeichnungen für den Druck auf Geräten vorbereiten, die nur einen begrenzten Satz von Schriftarten unterstützen.

## Warum Schriftarten mit Aspose.CAD ersetzen?

- **Keine externen Abhängigkeiten** – die Bibliothek übernimmt das Schriftarten‑Mapping intern.
- **Funktioniert mit vielen Formaten** – DXF, DWG, DGN und mehr.
- **Programmgesteuerte Steuerung** – automatisieren Sie den Vorgang für Batch‑Konvertierungen oder CI‑Pipelines.
- **Erhält die Geometrie der Zeichnung** – nur die visuelle Darstellung des Textes ändert sich.

## Voraussetzungen

- Grundkenntnisse in .NET-Programmierung.
- Aspose.CAD für .NET installiert. Wenn Sie es noch nicht installiert haben, laden Sie es [hier](https://releases.aspose.com/cad/net/) herunter.
- Eine CAD-Zeichnungsdatei (DXF, DWG usw.) zum Experimentieren.

## Namespaces importieren

Bevor Sie beginnen, importieren Sie die erforderlichen Namespaces, um auf die Aspose.CAD‑Funktionalitäten in Ihrer .NET‑Anwendung zuzugreifen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Schritt 1: CAD‑Zeichnung laden

Beginnen Sie damit, die CAD‑Zeichnung in eine Instanz von `CadImage` zu laden. Stellen Sie sicher, dass Sie den korrekten Pfad zu Ihrem Dokumentenverzeichnis angeben.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Schritt 2: Durch Stile iterieren

Als Nächstes iterieren Sie über die Stile in der CAD‑Zeichnung mit einer `foreach`‑Schleife. Dadurch können Sie einzelne Schriftstil‑Objekte zugreifen und manipulieren.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Wie man den primären Schriftnamen für die Schriftartensubstitution festlegt

Die Eigenschaft `PrimaryFontName` jedes `CadStyleTableObject` bestimmt, welche Schriftart beim Rendern der Zeichnung verwendet wird. Durch das Setzen dieser Eigenschaft ersetzen Sie effektiv die Originalschrift.

### Schritt 3: Schriftarten global ersetzen

Um Schriftarten für **alle** Stile zu ersetzen, setzen Sie die Eigenschaft `PrimaryFontName` für jeden Stil auf den gewünschten Schriftnamen, zum Beispiel `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Schritt 4: Schriftart nach Stilnamen ersetzen

Wenn Sie die Schriftart nur für einen bestimmten Stil ersetzen müssen (z. B. den Stil mit dem Namen `"Roman"`), fügen Sie innerhalb der Schleife eine Bedingungsprüfung hinzu.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Häufige Probleme & Fehlerbehebung

| Problem | Ursache | Lösung |
|---------|---------|--------|
| Schrift ändert sich nach Ausführen des Codes nicht | Die Zeichnung ist zwischengespeichert oder im Nur‑Lese‑Modus geöffnet | Stellen Sie sicher, dass Sie das Bild nach der Änderung speichern (`cadImage.Save(...)`) oder die Datei erneut laden, um dies zu überprüfen. |
| Gewünschte Schriftart ist auf dem System nicht gefunden | Schriftart nicht auf dem Rechner installiert, auf dem der Code ausgeführt wird | Installieren Sie die erforderliche TrueType/OpenType‑Schriftart oder betten Sie sie in die Anwendungsressourcen ein. |
| Text erscheint verzerrt | Falsche Kodierung oder fehlende Unicode‑Unterstützung | Verwenden Sie eine Schriftart, die den erforderlichen Zeichensatz unterstützt (z. B. Arial Unicode MS). |

## Häufig gestellte Fragen

**Q: Kann ich Schriftartänderungen in Aspose.CAD für .NET rückgängig machen?**  
A: Ja, Sie können rückgängig machen, indem Sie die ursprüngliche CAD‑Zeichnung erneut laden oder vor den Änderungen eine Sicherungskopie behalten.

**Q: Gibt es weitere Schriftarteigenschaften, die ich ändern kann?**  
A: Absolut. Neben `PrimaryFontName` können Sie mit `SecondaryFontName`, `FontFamily` und anderen stilbezogenen Attributen für erweiterte Anpassungen arbeiten.

**Q: Ist Aspose.CAD mit verschiedenen CAD‑Formaten kompatibel?**  
A: Ja, Aspose.CAD unterstützt eine breite Palette von Formaten wie DXF, DWG, DGN, DWF und mehr, was Ihnen Flexibilität über Projekte hinweg bietet.

**Q: Kann ich die Schriftartensubstitution in der Stapelverarbeitung automatisieren?**  
A: Sicherlich. Verpacken Sie die Lade‑ und Substitutionslogik in einer Schleife, die über einen Ordner mit CAD‑Dateien iteriert, oder integrieren Sie sie in eine CI/CD‑Pipeline.

**Q: Wo finde ich zusätzlichen Support für Aspose.CAD für .NET?**  
A: Für zusätzlichen Support und Community‑Diskussionen besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19).

---

**Zuletzt aktualisiert:** 2026-03-29  
**Getestet mit:** Aspose.CAD für .NET (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}