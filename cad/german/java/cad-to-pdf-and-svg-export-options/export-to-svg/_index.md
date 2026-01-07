---
date: 2026-01-07
description: Erfahren Sie, wie Sie CAD mit Aspose.CAD für Java nach SVG exportieren.
  Diese Schritt‑für‑Schritt‑Anleitung zeigt Ihnen, wie Sie DWG in SVG konvertieren,
  den SVG‑Farbmodus festlegen und die Bibliothek in Ihr Java‑Projekt integrieren.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Exportieren von CAD nach SVG mit Aspose.CAD für Java
url: /de/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD nach SVG exportieren mit Aspose.CAD für Java

## Einführung

Willkommen in der Welt von Aspose.CAD für Java, einer leistungsstarken Bibliothek, die Entwicklern ermöglicht, CAD-Zeichnungen mühelos zu manipulieren. Egal, ob Sie ein erfahrener Entwickler oder ein Neuling im CAD-Bereich sind, führt Sie dieser umfassende Leitfaden Schritt für Schritt durch **export CAD to SVG**, zeigt Ihnen, wie Sie DWG nach SVG konvertieren, den SVG-Farbmodus einstellen und die API in Ihr Java-Projekt integrieren.

## Schnelle Antworten
- **Was bedeutet „export CAD to SVG“?** Es konvertiert eine CAD-Zeichnung (z. B. DWG) in eine Scalable Vector Graphics‑Datei, die in Browsern angezeigt werden kann.  
- **Welche Bibliothek übernimmt die Konvertierung?** Aspose.CAD für Java stellt eine einfache API für diese Aufgabe bereit.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert zum Testen; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich die SVG-Farbausgabe steuern?** Ja, Sie können den SVG-Farbmodus festlegen (z. B. Graustufen).  
- **Ist zusätzliche Software erforderlich?** Nur eine Java-Laufzeitumgebung und die Aspose.CAD‑JAR‑Datei.

## Voraussetzungen

Bevor Sie in das Tutorial eintauchen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass Java auf Ihrem System installiert ist.  
- Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD für Java‑Bibliothek von dem [download link](https://releases.aspose.com/cad/java/) herunter und installieren Sie sie.  
- Dokumentverzeichnis: Erstellen Sie ein Verzeichnis für Ihre CAD‑Zeichnungen und notieren Sie dessen Pfad.

## Namespaces importieren

In diesem Schritt importieren wir die erforderlichen Namespaces, um unsere Aspose.CAD‑Reise zu starten. Folgen Sie diesen Schritten:

### Schritt 1: Öffnen Sie Ihr Java‑Projekt
Öffnen Sie Ihr Java‑Projekt in der IDE Ihrer Wahl.

### Schritt 2: Aspose.CAD‑Bibliothek hinzufügen
Fügen Sie die Aspose.CAD‑Bibliothek zu Ihrem Projekt hinzu. Sie können dies tun, indem Sie die JAR‑Datei in die Abhängigkeiten Ihres Projekts aufnehmen.

### Schritt 3: Namespaces importieren
Importieren Sie in Ihrer Java‑Klasse die erforderlichen Namespaces:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## CAD nach SVG exportieren

Jetzt, da wir die Grundlagen geschaffen haben, tauchen wir in den Schritt‑für‑Schritt‑Prozess von **export CAD to SVG** mit Aspose.CAD für Java ein.

### Schritt 1: Ressourcenverzeichnis angeben
Definieren Sie den Pfad zu Ihrem Ressourcenverzeichnis, in dem sich Ihre CAD‑Zeichnungen befinden:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Schritt 2: CAD‑Zeichnung laden
Laden Sie die CAD‑Zeichnung mit der Aspose.CAD‑Bibliothek:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Schritt 3: SVG‑Exportoptionen konfigurieren
Konfigurieren Sie die SVG‑Exportoptionen, um die Ausgabe anzupassen. Hier **setzen wir den SVG-Farbmodus** auf Graustufen und weisen den Exporter an, Text in Formen zu konvertieren:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Schritt 4: Als SVG speichern
Speichern Sie die CAD‑Zeichnung als SVG‑Datei:

```java
image.save(dataDir + "meshes.svg");
```

> **Profi‑Tipp:** Wenn Sie **DWG nach SVG** konvertieren möchten und dabei die Farben beibehalten wollen, ändern Sie `SvgColorMode.Grayscale` zu `SvgColorMode.FullColor`.

Herzlichen Glückwunsch! Sie haben erfolgreich eine CAD‑Zeichnung mit Aspose.CAD für Java nach SVG exportiert.

## Warum Aspose.CAD zum Export von CAD nach SVG verwenden?
- **Hohe Treue:** Vektordaten bleiben erhalten, sodass das SVG exakt wie die ursprüngliche CAD‑Zeichnung aussieht.  
- **Keine externen Abhängigkeiten:** Die Konvertierung läuft vollständig in Java und eliminiert die Notwendigkeit zusätzlicher Werkzeuge.  
- **Anpassbare Ausgabe:** Optionen wie `setColorType` ermöglichen es Ihnen zu steuern, ob das SVG in Graustufen oder Vollfarbe vorliegt.

## Häufige Probleme und Lösungen
- **Datei nicht gefunden:** Stellen Sie sicher, dass `dataDir` auf den richtigen Ordner zeigt und der DWG‑Dateiname übereinstimmt.  
- **Leere SVG‑Ausgabe:** Stellen Sie sicher, dass Sie `options.setTextAsShapes(true)` gesetzt haben, wenn die Zeichnung Text enthält, der als Formen erscheinen soll.  
- **Nicht unterstütztes CAD‑Format:** Aspose.CAD unterstützt DWG, DXF, DWF und mehrere andere Formate; prüfen Sie die Dokumentation für die genaue Liste.

## Fazit

In diesem Tutorial haben wir den nahtlosen Prozess untersucht, mit dem Aspose.CAD für Java **CAD nach SVG exportiert** wird. Mit seiner intuitiven API und robusten Funktionen vereinfacht Aspose.CAD komplexe Aufgaben und bietet Entwicklern ein vielseitiges Werkzeug zur CAD‑Manipulation.

## FAQ

### Q1: Kann ich Aspose.CAD für Java mit anderen CAD‑Formaten verwenden?
A1: Ja, Aspose.CAD unterstützt verschiedene CAD‑Formate, darunter DWG, DXF, DWF und weitere.

### Q2: Ist Aspose.CAD sowohl für Anfänger als auch für erfahrene Entwickler geeignet?
A2: Absolut! Aspose.CAD bietet eine benutzerfreundliche API, die für Anfänger zugänglich ist, und gleichzeitig fortgeschrittene Funktionen für erfahrene Entwickler bereitstellt.

### Q3: Wo finde ich zusätzlichen Support oder Community‑Diskussionen?
A3: Besuchen Sie das [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) für Support und Diskussionen.

### Q4: Gibt es eine kostenlose Testversion?
A4: Ja, Sie können Aspose.CAD mit einer [free trial](https://releases.aspose.com/) ausprobieren.

### Q5: Wie kann ich eine Lizenz für Aspose.CAD für Java erwerben?
A5: Sie können eine Lizenz über die [purchase page](https://purchase.aspose.com/buy) erwerben.

## Häufig gestellte Fragen

**Q: Kann ich eine DXF‑Datei mit demselben Code nach SVG konvertieren?**  
A: Ja, ersetzen Sie einfach den Dateinamen durch eine DXF‑Datei; die API unterstützt beide Formate.

**Q: Wie ändere ich die Ausgabe zu einem Vollfarb‑SVG?**  
A: Setzen Sie `options.setColorType(SvgColorMode.FullColor);` vor dem Speichern.

**Q: Ist es möglich, Schriftarten in das erzeugte SVG einzubetten?**  
A: Aspose.CAD konvertiert derzeit Text in Formen; das Einbetten von Schriftarten ist nicht erforderlich.

**Q: Funktioniert die Bibliothek unter Linux und macOS?**  
A: Die Java‑Bibliothek ist plattformunabhängig und läuft überall dort, wo eine kompatible JVM verfügbar ist.

**Q: Welche Version von Aspose.CAD wurde in diesem Tutorial verwendet?**  
A: Das Beispiel wurde mit Aspose.CAD für Java 24.10 getestet.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-01-07  
**Getestet mit:** Aspose.CAD für Java 24.10  
**Autor:** Aspose