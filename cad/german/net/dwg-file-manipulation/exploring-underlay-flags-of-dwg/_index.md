---
date: 2026-04-09
description: Erfahren Sie, wie Sie DWG in ein Bild konvertieren und wie Sie Unterlage‑Flags
  mit Aspose.CAD für .NET in dieser Schritt‑für‑Schritt‑Anleitung lesen.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Erkundung der Unterlagekennzeichen von DWG-Dateien
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG in Bild konvertieren – Untersuchung der Underlay‑Flags von DWG‑Dateien
  – Aspose.CAD‑Tutorial
url: /de/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Untersuchung von Underlay-Flags in DWG-Dateien – Aspose.CAD‑Tutorial

## Einführung

Wenn Sie in die komplexe Welt der CAD‑Dateien, insbesondere DWG‑Dateien, eintauchen und **DWG in Bild konvertieren** möchten, während Sie gleichzeitig **erfahren, wie Underlay‑Flags gelesen** werden, sind Sie hier genau richtig. Dieses Tutorial führt Sie Schritt für Schritt mit der leistungsstarken Aspose.CAD für .NET‑Bibliothek, sodass Sie Underlay‑Informationen extrahieren und die Zeichnung sicher als Bild rendern können.

## Schnelle Antworten
- **Was bedeutet „DWG in Bild konvertieren“?**  
  Es bedeutet, eine DWG‑Zeichnung mit Aspose.CAD in ein Rasterformat (PNG, JPEG usw.) zu rendern.
- **Welche Methode zeigt Underlay‑Flags?**  
  Greifen Sie nach dem Laden der DWG auf die `Flags`‑Eigenschaft des `CadUnderlay`‑Objekts zu.
- **Benötige ich eine Lizenz für Aspose.CAD?**  
  Eine temporäre Lizenz ist für die Evaluierung verfügbar; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.
- **Welche .NET‑Versionen werden unterstützt?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 und später.
- **Kann ich Underlay‑Geometrie extrahieren?**  
  Ja – Pfad, Einfügepunkt, Skalierung, Rotation und Flag‑Zustände des Underlays sind alle zugänglich.

## Was bedeutet „DWG in Bild konvertieren“ und warum ist das wichtig?

Das Konvertieren einer DWG‑Datei in ein Bild ermöglicht es Ihnen, CAD‑Zeichnungen in Browsern anzuzeigen, in Berichten einzubetten oder sie mit Stakeholdern zu teilen, die keinen CAD‑Viewer besitzen. Beim Rendern müssen Sie häufig **Underlay**‑Objekte (z. B. DGN‑Referenzen) prüfen, um sicherzustellen, dass sie korrekt dargestellt werden. Das Verständnis der Underlay‑Flags hilft Ihnen, Clipping-, Monochrom‑Render‑ und Sichtbarkeitsprobleme zu beheben, bevor Sie das endgültige Bild erzeugen.

## Voraussetzungen

- Grundlegendes Verständnis von C#‑ und .NET‑Programmierung.  
- **Aspose.CAD für .NET** Bibliothek installiert. Falls Sie sie noch nicht haben, laden Sie sie **[hier](https://releases.aspose.com/cad/net/)** herunter.  
- Eine DWG‑Datei zum Testen – die Beispieldatei **„BlockRefDgn.dwg“** wird in diesem Leitfaden durchgehend verwendet.

## Namespaces importieren

Um zu beginnen, importieren Sie die notwendigen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DWG‑Datei laden und in `CadImage` konvertieren

Laden Sie zunächst die DWG‑Datei und casten Sie sie zu einem `CadImage`. Dieses Objekt gibt Ihnen Zugriff auf alle Zeichen‑Entitäten, einschließlich Underlays.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Schritt 2: Durch Entitäten iterieren

Als Nächstes durchlaufen Sie jede Entität in der Zeichnung. Hier finden Sie die Underlay‑Objekte.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Schritt 3: Auf den Typ `CadDgnUnderlay` prüfen

Identifizieren Sie Underlay‑Entitäten, indem Sie deren Laufzeittyp prüfen. Die Klasse `CadDgnUnderlay` repräsentiert in einer DWG eingebettete DGN‑Underlays.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Schritt 4: Underlay‑Flags auslesen

Sobald Sie ein `CadDgnUnderlay` haben, casten Sie es zu `CadUnderlay`, um dessen Eigenschaften und Flag‑Zustände zu lesen. Die Flags geben an, ob das Underlay sichtbar, beschnitten oder in Monochrom dargestellt wird.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Was die Ausgabe aussagt

- **UnderlayPath / UnderlayName** – wo sich die externe DGN‑Datei befindet.  
- **InsertionPoint (X, Y)** – Koordinaten, an denen das Underlay im DWG‑Raum platziert ist.  
- **RotationAngle** – auf das Underlay angewandte Rotation.  
- **ScaleX / ScaleY / ScaleZ** – Skalierungsfaktoren für jede Achse.  
- **Flags** – boolesche Werte, die Sichtbarkeit (`UnderlayIsOn`), Clipping (`ClippingIsOn`) und monochrome Darstellung (`Monochrome`) anzeigen.

## Häufige Probleme & Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| Keine Ausgabe bei Flag‑Überprüfungen | Underlay‑Flags werden standardmäßig auf 0 gesetzt, wenn das Underlay deaktiviert ist. | Stellen Sie sicher, dass die DWG tatsächlich ein aktives Underlay enthält oder schalten Sie die Sichtbarkeit in der Quell‑CAD‑Datei ein. |
| `Invalid cast`‑Ausnahme | Die Entität ist kein `CadDgnUnderlay`. | Überprüfen Sie die Bedingung `if (entity is CadDgnUnderlay)` bevor Sie casten. |
| Bildrendering schlägt nach Flag‑Extraktion fehl | Das Underlay könnte beschnitten oder deaktiviert sein, was zu einem leeren Bereich führt. | Passen Sie die Flags (`UnderlayIsOn = true`, `ClippingIsOn = false`) vor dem Rendern des endgültigen Bildes an. |

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für .NET mit anderen CAD‑Dateiformaten verwenden?

A1: Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF, DGN und mehr. Prüfen Sie die Dokumentation für die vollständige Liste.

### Q2: Ist eine temporäre Lizenz für Aspose.CAD für .NET verfügbar?

A2: Ja, Sie können eine temporäre Lizenz **[hier](https://purchase.aspose.com/temporary-license/)** erhalten.

### Q3: Wo finde ich Support für Aspose.CAD für .NET?

A3: Besuchen Sie das Support‑Forum **[hier](https://forum.aspose.com/c/cad/19)** für Hilfe.

### Q4: Wie kaufe ich Aspose.CAD für .NET?

A4: Kaufen Sie die Bibliothek **[hier](https://purchase.aspose.com/buy)**.

### Q5: Gibt es eine kostenlose Testversion?

A5: Ja, Sie können die kostenlose Testversion **[hier](https://releases.aspose.com/)** nutzen.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, **DWG in Bild zu konvertieren** und gleichzeitig **Underlay‑Flags** mit Aspose.CAD für .NET zu lesen. Mit diesem Wissen können Sie:

- DWG‑Zeichnungen als Rasterbilder für Web‑ oder Reporting‑Szenarien rendern.  
- Underlay‑Eigenschaften prüfen und manipulieren, um eine korrekte Anzeige sicherzustellen.  
- Sichtbarkeits-, Clipping‑ und Monochrom‑Probleme vor der endgültigen Bildgenerierung debuggen.

Erkunden Sie gerne weitere Aspose.CAD‑Funktionen wie Ebenenverwaltung, Textextraktion und Batch‑Konvertierung, um Ihre CAD‑Automatisierungs‑Workflows weiter zu erweitern.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}