---
date: 2025-12-10
description: Erfahren Sie, wie Sie mit Aspose.CAD für Java PDFs aus CAD erstellen
  und dabei die Stiftanpassung nutzen. Diese Schritt‑für‑Schritt‑Anleitung zeigt,
  wie CAD effizient in PDF exportiert wird.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Wie man aus CAD ein PDF mit Stiftunterstützung beim Export erstellt
url: /de/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stiftunterstützung beim Export

## Einleitung

In der schnelllebigen Welt der CAD‑Konvertierungen müssen Entwickler häufig **PDF aus CAD**‑Dateien erstellen und dabei die visuelle Treue bewahren. Aspose.CAD für Java macht das unkompliziert und bietet umfangreiche Optionen wie die Stiftanpassung, mit der Sie Linienstile beim Exportvorgang feinjustieren können. In diesem Leitfaden führen wir Sie durch ein vollständiges, praxisnahes Beispiel, das zeigt, wie Sie **CAD nach PDF** mit benutzerdefinierten Stifteinstellungen exportieren, sodass Sie polierte PDFs direkt aus DXF‑Zeichnungen erzeugen können.

## Schnelle Antworten
- **Was bedeutet „PDF aus CAD erstellen“?** Konvertieren einer CAD‑Zeichnung (z. B. DXF) in ein PDF‑Dokument bei gleichbleibender Vektorqualität.  
- **Welche Bibliothek übernimmt die Stiftanpassung?** Die `PenOptions`‑Klasse von Aspose.CAD für Java.  
- **Kann ich das für andere Formate verwenden?** Ja – dieselben Stifteinstellungen gelten für PNG, BMP, TIFF usw.  
- **Benötige ich eine Lizenz?** Für den Produktionseinsatz ist eine gültige Aspose.CAD‑Lizenz erforderlich.  
- **Welche minimale Java‑Version wird benötigt?** Java 8 oder höher.

## Was bedeutet „PDF aus CAD erstellen“?
Ein PDF aus CAD zu erstellen bedeutet, eine CAD‑Zeichnung entweder zu rasterisieren oder vektorrezu­rieren und in einer PDF‑Datei zu speichern. Das ermöglicht einfaches Teilen, Drucken und Archivieren von Konstruktionsdaten, ohne dass beim Empfänger CAD‑Software installiert sein muss.

## Warum Stiftunterstützung beim Export von CAD nach PDF nutzen?
Mit der Stiftunterstützung können Sie Enden, Verbindungen und die Dicke von Linien steuern und so das Corporate‑Branding oder technische Zeichenstandards einhalten. Das ist besonders nützlich, wenn die Standard‑Liniendarstellung Ihre visuellen Anforderungen nicht erfüllt.

## Voraussetzungen

- **Java‑Entwicklungsumgebung** – ein funktionierendes JDK (8 oder neuer) sowie eine IDE oder ein Build‑Tool Ihrer Wahl.  
- **Aspose.CAD‑Bibliothek** – laden Sie das aktuelle JAR von der offiziellen Seite [hier](https://releases.aspose.com/cad/java/) herunter.  
- **Eine Beispiel‑DXF‑Datei** – für dieses Tutorial verwenden wir `conic_pyramid.dxf`.

Jetzt, wo wir die Grundlagen geschaffen haben, tauchen wir in den Code ein.

## Namespaces importieren

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Schritt 1: Definieren Sie Ihr Dokumentenverzeichnis

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Pro Tipp:** Ersetzen Sie `"Your Document Directory"` durch den absoluten Pfad, in dem Ihre DXF‑Dateien liegen.

## Schritt 2: Laden Sie die CAD‑Datei

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Die Methode `Image.load` liest die DXF‑Datei ein und erzeugt ein `CadImage`‑Objekt, das wir weiterverarbeiten können.

## Schritt 3: Rasterisierungsoptionen konfigurieren

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Passen Sie die Seitenabmessungen an, um die Auflösung des resultierenden PDFs zu steuern. Das Multiplizieren mit 100 liefert eine hochauflösende Ausgabe, die sich zum Druck eignet.

## Schritt 4: Stiftoptionen anpassen

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Hier setzen wir sowohl den Start‑ als auch den End‑Cap des Stifts auf `Flat`. Sie können mit anderen `LineCap`‑Werten (z. B. `Round`, `Square`) experimentieren, um unterschiedliche visuelle Effekte zu erzielen.

## Schritt 5: PDF‑Exportoptionen konfigurieren

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Das `PdfOptions`‑Objekt verknüpft die Rasterisierungseinstellungen mit dem PDF‑Exportprozess.

## Schritt 6: Exportiertes PDF speichern

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Durch Ausführen dieser Zeile wird eine PDF‑Datei mit dem Namen `9LHATT-A56_generated.pdf` in Ihrem `dataDir`‑Ordner geschrieben, komplett mit der von Ihnen definierten benutzerdefinierten Stiftformatierung.

## Häufige Anwendungsfälle

- **Technische Dokumentation** – präzise Konstruktionszeichnungen in PDF‑Handbüchern einbetten.  
- **Automatisierte Berichterstellung** – PDFs aus CAD‑Daten on‑the‑fly in Web‑Services generieren.  
- **Qualitätskontrolle** – benutzerdefinierte Linienenden verwenden, um Messlinien oder Toleranzen hervorzuheben.

## Fehlerbehebung & Tipps

- **Falscher Dateipfad** – stellen Sie sicher, dass `dataDir` mit einem Dateiseparator endet (`/` oder `\\`).  
- **Fehlende Lizenz** – ohne gültige Lizenz läuft die Bibliothek im Evaluierungsmodus, der Wasserzeichen hinzufügen kann.  
- **Unerwartete Linienstile** – prüfen Sie, ob `PenOptions` vor dem Aufruf von `save` gesetzt wurden; sonst werden Standard‑Stifte verwendet.

## Häufig gestellte Fragen

### Q1: Kann ich Stiftoptionen für andere Formate als PDF anpassen?

A1: Ja, die im Tutorial gezeigte Stiftanpassung ist auf verschiedene Bildformate anwendbar, darunter PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF und WMF.

### Q2: Wie kann ich unterschiedliche Start‑ und End‑Caps für Stifte festlegen?

A2: Nutzen Sie die `PenOptions`‑Klasse, um die gewünschten Start‑ und End‑Caps zu setzen, was Ihnen Flexibilität bei der Darstellung von Linien gibt.

### Q3: Was passiert, wenn ich keine Stiftoptionen angebe?

A3: Ohne explizite Angabe verwendet das System seine Standard‑Stifte, die je nach Kontext variieren können.

### Q4: Gibt es besondere Überlegungen zu den Rasterisierungsoptionen?

A4: Passen Sie die Seitenbreite und -höhe in den Rasterisierungsoptionen an, um die Abmessungen des exportierten Bildes zu steuern.

### Q5: Wo finde ich zusätzliche Unterstützung oder Community‑Diskussionen?

A5: Erkunden Sie das Aspose.CAD‑Community‑Forum unter [hier](https://forum.aspose.com/c/cad/19) für Support und Diskussionen.

---

**Zuletzt aktualisiert:** 2025-12-10  
**Getestet mit:** Aspose.CAD 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}