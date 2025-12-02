---
date: 2025-11-30
description: Erfahren Sie, wie Sie benutzerdefinierte Eigenschaften zu DWG‑Dateien
  in Java mit Aspose.CAD hinzufügen. Verbessern Sie die Organisation und die Informationsbeschaffung
  in CAD‑Zeichnungen mühelos.
language: de
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: Benutzerdefinierte Eigenschaften zu DWG‑Dateien hinzufügen mit Aspose.CAD für
  Java
url: /java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Benutzerdefinierte Eigenschaften zu DWG-Dateien hinzufügen mit Aspose.CAD für Java

Das programmgesteuerte Manipulieren von CAD-Zeichnungen ist für viele Java‑Entwickler ein täglicher Bedarf. In diesem Tutorial erfahren Sie **wie man benutzerdefinierte Eigenschaften zu DWG‑Dateien** mit der leistungsstarken Aspose.CAD‑Bibliothek für Java hinzufügt. Am Ende der Anleitung besitzen Sie ein wiederverwendbares Code‑Snippet, das Metadaten direkt in den Header einer DWG‑Datei einfügt, sodass Ihre Zeichnungen leichter zu katalogisieren, zu durchsuchen und zu verwalten sind.

## Einführung

Aspose.CAD für Java ist eine vollständig verwaltete, .NET‑freie Bibliothek, die es Ihnen ermöglicht, eine Vielzahl von CAD‑Formaten zu lesen, zu bearbeiten und zu schreiben, ohne AutoCAD zu benötigen. Das Hinzufügen benutzerdefinierter Eigenschaften zu einer DWG‑Datei bietet Ihnen eine leichte Möglichkeit, zusätzliche Informationen – wie Projekt‑Codes, Revisions‑Notizen oder Eigentümer‑Details – direkt in der Zeichnungsdatei zu speichern.

## Schnelle Antworten
- **Was bedeutet “add custom properties dwg”?** Es bedeutet, benutzerdefinierte Name/Wert‑Paare in die Header‑Metadaten einer DWG‑Datei einzufügen.  
- **Welche Bibliothek übernimmt das?** Aspose.CAD für Java bietet eine einfache API zum Lesen und Schreiben dieser Eigenschaften.  
- **Wie lange dauert die Implementierung?** Typischerweise 5‑10 Minuten für ein einfaches Beispiel.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Ist sie mit anderen CAD‑Formaten kompatibel?** Ja – DXF, DWF und weitere werden unterstützt.

## Was bedeutet das Hinzufügen benutzerdefinierter Eigenschaften zu DWG‑Dateien?

Benutzerdefinierte Eigenschaften sind Schlüssel‑Wert‑Paare, die im DWG‑Header gespeichert werden. Sie werden nicht in der Geometrie der Zeichnung angezeigt, können jedoch von jeder CAD‑fähigen Anwendung abgerufen werden, was ein besseres Datenmanagement, automatisierte Berichte und die Integration mit PLM‑Systemen ermöglicht.

## Warum Aspose.CAD für diese Aufgabe verwenden?

- **Keine AutoCAD‑Abhängigkeit** – funktioniert auf jedem OS oder CI‑Pipeline.  
- **Voll ausgestattete API** – lesen, ändern und speichern ohne Qualitätsverlust.  
- **Hohe Leistung** – verarbeitet große Zeichnungen in Sekunden.  
- **Cross‑Format‑Unterstützung** – derselbe Code funktioniert für DXF, DWF und andere.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java Development Kit (JDK) 8+** installiert und in Ihrer IDE konfiguriert.  
- **Aspose.CAD für Java** Bibliothek – laden Sie das neueste JAR von der [Aspose.CAD Download‑Seite](https://releases.aspose.com/cad/java/) herunter.  
- Eine **Beispiel‑DWG/DXF‑Datei** zum Experimentieren (das Tutorial verwendet `conic_pyramid.dxf`).

## Namespaces importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu, damit Sie mit Aspose.CAD‑Objekten arbeiten können.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Projekt einrichten

Erstellen Sie ein neues Maven/Gradle‑Projekt (oder ein einfaches IDE‑Projekt) und legen Sie das Aspose.CAD‑JAR auf den Klassenpfad. Dadurch sind die `com.aspose.cad.*`‑Pakete zur Compile‑Zeit verfügbar.

### Schritt 2: Dateipfade definieren

Geben Sie an, wo die Quellzeichnung liegt und wohin die modifizierte Datei geschrieben werden soll.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### Schritt 3: DWG‑Datei laden

Verwenden Sie die statische Methode `Image.load`, um die Zeichnung in ein `CadImage`‑Objekt zu laden.

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### Schritt 4: Benutzerdefinierte Eigenschaften hinzufügen

Fügen Sie Ihre Metadaten direkt in den Header der Zeichnung ein. Jeder Aufruf fügt ein neues Name‑Wert‑Paar hinzu.

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **Tipp:** Halten Sie Eigenschaftsnamen kurz (max 31 Zeichen) und vermeiden Sie Leerzeichen, um die Kompatibilität mit älteren CAD‑Betrachtern zu gewährleisten.

### Schritt 5: Modifizierte DWG‑Datei speichern

Speichern Sie die Änderungen, indem Sie `save` aufrufen. Die Ausgabedatei enthält nun die von Ihnen hinzugefügten benutzerdefinierten Eigenschaften.

```java
cadImage.save(outFile);
```

### Schritt 6: Code ausführen

Führen Sie das Programm aus Ihrer IDE oder über die Befehlszeile aus. Wenn alles korrekt eingerichtet ist, sehen Sie eine Bestätigungsnachricht.

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## Häufige Probleme & Lösungen

| Problem | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | Aspose.CAD JAR nicht im Klassenpfad | Fügen Sie das JAR dem `libs`‑Ordner Ihres Projekts hinzu oder deklarieren Sie es in Maven/Gradle. |
| **Properties not appearing in the saved file** | Verwendung einer DWG‑Version, die benutzerdefinierte Eigenschaften nicht unterstützt | Stellen Sie sicher, dass Sie mit DWG/DXF‑Versionen 2000 oder neuer arbeiten; ältere Formate können benutzerdefinierte Header ignorieren. |
| **`OutOfMemoryError` on large files** | Laden einer sehr großen Zeichnung ohne Streaming | Verwenden Sie `Image.load` mit einem `LoadOptions`‑Objekt, das speichereffizientes Laden ermöglicht. |

## Häufig gestellte Fragen

**F: Kann ich benutzerdefinierte Eigenschaften zu anderen CAD‑Dateiformaten hinzufügen?**  
A: Ja. Aspose.CAD für Java unterstützt DXF, DWF, DGN und weitere, und die gleiche `getHeader().getCustomProperties()`‑API funktioniert über diese Formate hinweg.

**F: Ist Aspose.CAD für Java mit allen gängigen IDEs kompatibel?**  
A: Absolut. Es funktioniert mit Eclipse, IntelliJ IDEA, NetBeans und sogar mit einfachen Befehlszeilen‑Builds.

**F: Wo finde ich weitere Beispiele und detaillierte Dokumentation?**  
A: Besuchen Sie die offizielle [Aspose.CAD Java API‑Referenz](https://reference.aspose.com/cad/java/) für eine vollständige Liste von Klassen, Methoden und Beispielprojekten.

**F: Kann ich Aspose.CAD für Java vor dem Kauf testen?**  
A: Ja – laden Sie eine kostenlose 30‑Tage‑Testversion von der [Aspose.CAD Download‑Seite](https://releases.aspose.com/) herunter.

**F: Wie erhalte ich Support, wenn ich auf Schwierigkeiten stoße?**  
A: Das Aspose‑Community‑Forum und das dedizierte [Aspose.CAD Support‑Portal](https://forum.aspose.com/c/cad/19) sind hervorragende Anlaufstellen, um Fragen zu stellen und Lösungen zu teilen.

---

**Zuletzt aktualisiert:** 2025-11-30  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}