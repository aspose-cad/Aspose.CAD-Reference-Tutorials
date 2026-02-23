---
date: 2026-02-23
description: Erfahren Sie, wie Sie DWG‑Dateien mit Aspose.CAD.DWG für Java laden und
  Unterlage‑Flags extrahieren – ein Schritt‑für‑Schritt‑Leitfaden für Entwickler.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG laden & Unterlage‑Flags zugreifen (Java)
url: /de/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-Datei laden & Unterlage-Flags abrufen – Aspose.CAD für Java

In modernen CAD‑Workflows können Sie **mit aspose cad dwg schnell eine DWG‑Datei laden** und Unterlage‑Details extrahieren, die häufig für Gelegenheitsbetrachter verborgen bleiben. Ob Sie einen Java DWG‑Viewer bauen, einen Batch‑Prozess‑dwg‑Pipeline automatisieren oder Metadaten für die GIS‑Integration extrahieren – Aspose.CAD für Java bietet Ihnen einen sauberen, code‑first Ansatz. In diesem Tutorial führen wir Sie Schritt für Schritt durch das **Laden einer DWG‑Datei**, das Durchlaufen ihrer Entitäten und das Auslesen der Unterlage‑Flags, die vielen Entwicklern entgehen.

## Schnellantworten
- **Welche Hauptklasse wird zum Öffnen einer DWG verwendet?** `com.aspose.cad.Image.load()` liefert ein `CadImage`.
- **Welches Objekt enthält Unterlage‑Informationen?** `CadUnderlay` (oder abgeleitete Typen wie `CadDgnUnderlay`).
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert für Tests; für die Produktion ist eine kommerzielle Lizenz erforderlich.
- **Kann ich mehrere DWG‑Dateien in einer Schleife verarbeiten?** Ja – wiederholen Sie einfach das Laden‑und‑Iterieren‑Muster.
- **Ist dieser Ansatz mit Java 11+ kompatibel?** Absolut, Aspose.CAD unterstützt Java 8 bis zu den neuesten LTS‑Versionen.

## aspose cad dwg – Laden einer DWG‑Datei (Java)

`Image.load()` liest den binären DWG‑Inhalt und erzeugt ein `CadImage`‑Objekt im Speicher. Von dort aus können Sie Ebenen, Blöcke und Unterlage‑Entitäten erkunden, ohne sich selbst mit dem DWG‑Dateiformat auseinandersetzen zu müssen.

## Warum Unterlage‑Flags aus einer DWG extrahieren?

Unterlage‑Flags geben an, wie ein externes Referenzobjekt (wie ein DGN‑ oder PDF‑Unterlage) innerhalb der Zeichnung positioniert, skaliert und rotiert ist. Das Wissen um diese Werte ermöglicht Ihnen:

- Das exakte visuelle Layout in einem eigenen **java dwg viewer** nachzubilden.
- Unterlagen in native CAD‑Entitäten zu konvertieren für weitere Bearbeitung.
- Berichte zu erstellen, die Unterlage‑Metadaten für Compliance oder Dokumentation enthalten.
- **Batch‑Verarbeitung von dwg**‑Dateien und das Speichern ihrer Unterlage‑Metadaten in einer Datenbank für spätere Analysen.

## Voraussetzungen
- **Aspose.CAD Bibliothek** – Download von der [releases](https://releases.aspose.com/cad/java/) Seite.  
- **Java Development Kit** – JDK 8 oder neuer.  
- **Ein Ordner**, der die DWG‑Dateien enthält, die Sie analysieren möchten. Ersetzen Sie `"Your Document Directory"` im Code durch Ihren tatsächlichen Pfad.

## Namespaces importieren

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Ressourcenverzeichnis festlegen
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Definieren Sie, wo Ihre DWG‑Dateien liegen. Die Verwendung eines dedizierten Ordners hält das Beispiel sauber und portabel.

### Schritt 2: DWG‑Datei laden
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Hier **laden wir die dwg‑Datei** `BlockRefDgn.dwg` in eine `CadImage`‑Instanz, bereit zur Inspektion.

### Schritt 3: Durch DWG‑Entitäten iterieren
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Die Schleife durchläuft jede Entität – Linien, Kreise, Blöcke und Unterlagen – sodass wir die benötigten herausfiltern können.

### Schritt 4: CadDgnUnderlay‑Entitäten identifizieren
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Nur `CadDgnUnderlay`‑Objekte enthalten die gesuchten Unterlage‑Flags, daher filtern wir gezielt danach.

### Schritt 5: Unterlage‑Informationen abrufen
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Sobald wir ein `CadUnderlay` haben, können wir Pfad, Name, Einfügepunkt, Rotation, Skalierungsfaktoren und das `UnderlayFlags`‑Enum auslesen, das Sichtbarkeit, Clipping und weitere Rendering‑Optionen angibt.

## Wie man DWG‑Dateien in einem Batch‑Prozess lädt

Wenn Sie **dwg‑Dateien batchweise** verarbeiten müssen, verpacken Sie die obigen Schritte in eine einfache `for`‑Schleife, die über alle Dateien in `dataDir` iteriert. Der gleiche `Image.load()`‑Aufruf funktioniert für jede Datei, und Sie können die extrahierten Flags in einer CSV‑Datei oder einer Datenbank für nachgelagerte Berichte speichern.

## Häufige Probleme & Tipps
- **Null‑Unterlage‑Pfad** – Stellen Sie sicher, dass die DWG tatsächlich eine externe Datei referenziert; andernfalls bleibt der Pfad leer.
- **Nicht unterstützter Unterlage‑Typ** – Aspose.CAD unterstützt derzeit DGN‑Unterlagen; PDF‑Unterlagen sind über die API noch nicht verfügbar.
- **Lizenz‑Ausnahmen** – Das Ausführen des Codes ohne gültige Lizenz fügt jedem exportierten Bild ein Wasserzeichen hinzu.
- **Performance‑Tipp:** Wiederverwenden Sie eine einzelne `Image`‑Instanz, wenn Sie viele Dateien in einem Batch verarbeiten, um den GC‑Druck zu reduzieren.

## Häufig gestellte Fragen

**F: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?**  
A: Aspose.CAD konzentriert sich hauptsächlich auf das DWG‑Format, unterstützt aber auch DXF, DWF und weitere CAD‑Formate.

**F: Gibt es eine Testversion von Aspose.CAD für Java?**  
A: Ja, Sie können die Funktionen mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) ausprobieren.

**F: Wie erhalte ich Support oder Hilfe zu Aspose.CAD für Java?**  
A: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

**F: Gibt es temporäre Lizenzen für Aspose.CAD für Java?**  
A: Ja, eine temporäre Lizenz können Sie [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**F: Wo finde ich die umfassende Dokumentation zu Aspose.CAD für Java?**  
A: Siehe die [Dokumentation](https://reference.aspose.com/cad/java/) für detaillierte Informationen.

---

**Zuletzt aktualisiert:** 2026-02-23  
**Getestet mit:** Aspose.CAD 24.12 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}