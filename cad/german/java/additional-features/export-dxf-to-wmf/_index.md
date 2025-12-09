---
date: 2025-11-29
description: Erfahren Sie, wie Sie DXF mit Aspose.CAD für Java in WMF konvertieren,
  DXF‑Zeichnungen laden und optional den Aspose‑Export nach PDF verwenden. Schritt‑für‑Schritt‑Anleitung
  mit Codebeispielen.
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: DXF in WMF mit Aspose.CAD in Java konvertieren
url: /de/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF in WMF mit Aspose.CAD in Java konvertieren

## Einführung

In diesem Tutorial erfahren Sie, wie Sie **DXF in WMF** mit Aspose.CAD für Java **konvertieren**. Egal, ob Sie CAD‑Zeichnungen in einem Windows‑basierten Bericht einbetten müssen oder einfach ein leichtgewichtiges Vektorformat benötigen, die Konvertierung von DXF nach WMF ist ein häufiges Anliegen. Wir führen Sie durch das Laden einer DXF‑Zeichnung, das Konfigurieren von Rasterisierungsoptionen, das Speichern des Ergebnisses als WMF und sogar die optionale Verwendung von Aspose zum Export nach PDF.

## Schnelle Antworten
- **Kann ich DXF mit einer kostenlosen Testversion in WMF konvertieren?** Ja – Aspose bietet eine voll funktionsfähige 30‑tägige Testversion.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Für den Produktionseinsatz ist eine Lizenz erforderlich; die Testversion funktioniert für Entwicklung und Tests.  
- **Ist die Konvertierung verlustfrei?** Vektordaten werden erhalten; Rasterisierungsoptionen ermöglichen die Kontrolle der Auflösung.  
- **Kann ich dieselbe Zeichnung auch nach PDF exportieren?** Absolut – siehe den Schritt „Export nach PDF“ unten.

## Was bedeutet „DXF in WMF konvertieren“?

Die Konvertierung von DXF nach WMF bedeutet, dass eine Drawing Exchange Format (DXF)‑Datei – ein weit verbreitetes CAD‑Format – in ein Windows Metafile (WMF) umgewandelt wird. WMF ist ein Vektor‑Bildformat, das sich nahtlos in Microsoft Office, Windows‑Anwendungen und viele Reporting‑Tools integrieren lässt.

## Warum Aspose.CAD für Java verwenden?

- **Keine externen Abhängigkeiten** – reines Java, keine nativen DLLs.  
- **Hohe Treue** – erhält Ebenen, Farben und Linienstile.  
- **Eingebaute Rasterisierung** – feine Einstellung von Seitengröße, Auflösung und Hintergrund.  
- **All-in-One‑Lösung** – dieselbe API unterstützt ebenfalls den Export nach PDF, PNG, SVG und mehr.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie:

- **Aspose.CAD für Java** in Ihr Projekt integriert. Laden Sie es von der offiziellen Seite herunter: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Dokumentverzeichnis**, in dem Ihre DXF‑Dateien gespeichert sind (z. B. `Your Document Directory/DXFDrawings/`).

## Namespaces importieren

In Ihrer Java‑Quelldatei importieren Sie die Aspose.CAD‑Klassen, die Sie benötigen:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: DXF‑Zeichnung laden

Zuerst **laden Sie die DXF‑Zeichnung**, die Sie konvertieren möchten. Die Methode `Image.load` liest die Datei in den Speicher.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Schritt 2: Rasterisierungsoptionen konfigurieren

Richten Sie die Rasterisierungsparameter ein, die die Größe des Ausgabe‑WMF steuern. In diesem Beispiel verwenden wir eine Seite von 100 × 100 Einheiten.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### Schritt 3: Als WMF speichern

Speichern Sie nun die geladene Zeichnung als WMF‑Datei unter Verwendung der oben definierten Optionen.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### Schritt 4: Ressourcen freigeben

Das ordnungsgemäße Freigeben von Ressourcen verhindert Speicherlecks, insbesondere beim Verarbeiten vieler Zeichnungen.

```java
finally
{
  cadImage.dispose();
}
```

### Schritt 5: Optional – Aspose‑Export nach PDF

Falls Sie zusätzlich eine PDF‑Version derselben Zeichnung benötigen, ermöglicht Aspose.CAD dies mit einer einzigen Zeile.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **Pro‑Tipp:** Sie können dasselbe `CadRasterizationOptions`‑Objekt für den PDF‑Export wiederverwenden, indem Sie es an eine `PdfOptions`‑Instanz übergeben.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Variable `cadImage` ist nicht definiert (sollte `image` sein). | Ersetzen Sie `cadImage` durch `image` oder benennen Sie die Variable konsistent um. |
| **Output WMF is blank** | Seitengröße der Rasterisierung zu klein oder Hintergrundfarbe ist transparent eingestellt. | Erhöhen Sie `PageWidth`/`PageHeight` oder setzen Sie eine Hintergrundfarbe via `rasterizationOptions.setBackgroundColor(Color.getWhite());`. |
| **License exception** | Ausführung ohne gültige Aspose‑Lizenz in der Produktion. | Laden Sie die Lizenzdatei beim Anwendungsstart: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Fazit

Sie haben nun einen vollständigen, produktionsbereiten Workflow, um **DXF in WMF** mit Aspose.CAD für Java zu **konvertieren**, mit einem optionalen Schritt zum **Aspose‑Export nach PDF**. Dieser Ansatz liefert Ihnen hochwertige Vektorausgaben, die sich nahtlos in Windows‑basierte Reporting‑ und Dokumentations‑Tools integrieren.

## FAQ

### Q1: Wo finde ich die Aspose.CAD‑Dokumentation?

A1: Sie können die Dokumentation [hier](https://reference.aspose.com/cad/java/) aufrufen.

### Q2: Wie lade ich Aspose.CAD für Java herunter?

A2: Laden Sie die Bibliothek [hier](https://releases.aspose.com/cad/java/) herunter.

### Q3: Gibt es eine kostenlose Testversion?

A3: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Benötigen Sie temporäre Lizenzoptionen?

A4: Erkunden Sie temporäre Lizenzen [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Wo kann ich Support erhalten?

A5: Besuchen Sie das Aspose.CAD‑Support‑Forum [hier](https://forum.aspose.com/c/cad/19).

## Häufig gestellte Fragen

**Q: Kann ich große DXF‑Dateien (Hunderte MB) konvertieren, ohne dass der Speicher ausgeht?**  
A: Ja. Laden Sie die Datei in einem `try‑with‑resources`‑Block und geben Sie das `Image`‑Objekt umgehend frei. Passen Sie `CadRasterizationOptions.setPageWidth/Height` auf eine angemessene Größe an, um den Speicherverbrauch gering zu halten.

**Q: Behält die WMF‑Ausgabe Ebeneninformationen bei?**  
A: WMF ist ein flaches Vektorformat, sodass die Ebenenhierarchie abgeflacht wird, aber Linienstile und Farben erhalten bleiben.

**Q: Ist es möglich, eine benutzerdefinierte DPI für das WMF festzulegen?**  
A: Verwenden Sie `rasterizationOptions.setResolution(300);`, um die DPI vor dem Speichern festzulegen.

**Q: Kann ich mehrere DXF‑Dateien in einem Durchlauf stapelweise konvertieren?**  
A: Absolut. Durchlaufen Sie ein Verzeichnis, laden Sie jede Datei und wenden Sie dieselbe Rasterisierungs‑ und Speicherlogik an.

**Q: Welche Java‑Versionen werden unterstützt?**  
A: Aspose.CAD für Java unterstützt Java 8 und höher (einschließlich Java 11, 17 und neuere LTS‑Versionen).

---

**Zuletzt aktualisiert:** 2025-11-29  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}