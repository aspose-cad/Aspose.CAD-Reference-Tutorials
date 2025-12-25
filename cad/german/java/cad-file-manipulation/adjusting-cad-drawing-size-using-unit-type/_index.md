---
date: 2025-12-25
description: Erfahren Sie, wie Sie DWG mit Aspose.CAD für Java nach BMP exportieren.
  Diese Schritt‑für‑Schritt‑Anleitung zeigt, wie Sie die Größe von CAD‑Zeichnungen
  anpassen und CAD effizient nach BMP konvertieren.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG nach BMP exportieren – CAD-Größe mit Einheitstyp anpassen (Java)
url: /de/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG nach BMP exportieren – CAD-Zeichnungsgröße mit Unit Type in Aspose.CAD für Java anpassen

## Introduction

Wenn Sie **DWG nach BMP exportieren** müssen, ist die Kontrolle der Ausgabengröße und der Maßeinheit für die nachgelagerte Verarbeitung oder den Druck entscheidend. In diesem Tutorial lernen Sie, wie Sie die CAD-Zeichnungsgröße anpassen und CAD nach BMP mit Aspose.CAD für Java konvertieren, wobei die Eigenschaft `UnitType` zur Definition der Maßeinheit verwendet wird. Die Schritte werden in einfacher Sprache erklärt, sodass Sie ihnen folgen können, selbst wenn Sie neu in der Bibliothek sind.

## Quick Answers
- **Was bedeutet „DWG nach BMP exportieren“?** Umwandlung einer DWG‑Zeichnung in ein BMP‑Rasterbild.  
- **Welche Eigenschaft steuert die Ausgabengröße?** `CadRasterizationOptions.setUnitType()` legt die Einheit fest (z. B. Zentimeter).  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Eine kostenlose Testversion reicht für die Evaluierung; für die Produktion ist eine Lizenz erforderlich.  
- **Kann ich andere Layouts wählen?** Ja, verwenden Sie `setLayouts()`, um Modell‑ oder Papier‑Space‑Layouts anzugeben.  
- **Welche Ausgabeformate werden unterstützt?** Neben BMP können Sie durch Ändern der Optionsklasse zu PNG, JPEG, TIFF usw. exportieren.

## What is **export DWG to BMP**?

Exportieren von DWG nach BMP bedeutet, eine vektorbasierte DWG‑Datei in ein Bitmap‑Bild (BMP) zu rasterisieren. Dies ist nützlich, wenn Sie eine pixelgenaue Darstellung für Altsysteme, Bildverarbeitungspipelines oder einfache Anzeige‑Szenarien benötigen.

## Why adjust CAD drawing size with **Unit Type**?

Durch das Festlegen des Unit Types können Sie die physischen Abmessungen des exportierten Bildes steuern, ohne Skalierungsfaktoren manuell berechnen zu müssen. Dadurch entspricht das Bitmap den realen Maßen (z. B. Zentimeter), was für technische Zeichnungen und gedruckte Dokumentationen entscheidend ist.

## Prerequisites

Bevor Sie in das Tutorial einsteigen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- **Java-Entwicklungsumgebung** – Ein funktionierendes JDK (8 oder neuer) sowie eine IDE oder ein Build‑Tool (Maven/Gradle).  
- **Aspose.CAD für Java Bibliothek** – Laden Sie die Aspose.CAD‑Bibliothek herunter und integrieren Sie sie in Ihr Java‑Projekt. Sie können die Bibliothek [hier](https://releases.aspose.com/cad/java/) erhalten.

## Import Namespaces

Fügen Sie in Ihrem Java‑Code die erforderlichen Namespaces hinzu, um auf die Aspose.CAD‑Funktionen zuzugreifen. Ergänzen Sie die folgenden Importe:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nun zerlegen wir den Vorgang zum Anpassen der CAD‑Zeichnungsgröße mit Unit Type in überschaubare Schritte:

## Step 1: Define Data Directory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Legen Sie den Pfad zu dem Verzeichnis fest, in dem sich Ihre CAD‑Dateien befinden.

## Step 2: Load CAD Drawing

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Laden Sie die CAD‑Zeichnung mit der `Image`‑Klasse von Aspose.CAD.

## Step 3: Create BMP Options

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instanziieren Sie die Klasse `BmpOptions`, um das CAD‑Layout im BMP‑Format zu exportieren.

## Step 4: Configure Rasterization Options

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Erstellen Sie eine Instanz von `CadRasterizationOptions` und verknüpfen Sie sie mit den `BmpOptions` für die Vektor‑Rasterisierung.

## Step 5: Set Unit Type

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Geben Sie den gewünschten Unit Type für die CAD‑Zeichnung an. In diesem Beispiel haben wir ihn auf **Centimeter** gesetzt, was die exportierte Bildgröße direkt beeinflusst, wenn Sie die **CAD‑Zeichnungsgröße anpassen**.

## Step 6: Set Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definieren Sie die Layouts, die beim Export berücksichtigt werden sollen. In diesem Fall haben wir das **"Model"**‑Layout ausgewählt, Sie können jedoch bei Bedarf zu Papier‑Space‑Layouts wechseln.

## Step 7: Export to BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Speichern Sie schließlich die modifizierte CAD‑Zeichnung im BMP‑Format. Dieser Schritt schließt den **DWG nach BMP exportieren**‑Workflow ab und bewahrt die von Ihnen vorgenommenen Größeneinstellungen.

## Common Issues and Solutions

| Problem | Ursache | Lösung |
|-------|--------|-----|
| **Ausgabebild ist zu klein** | Unit Type nicht gesetzt oder Standard (Pixel) verwendet | Rufen Sie `setUnitType()` mit der gewünschten Maßeinheit auf (z. B. `UnitType.Centimeter`). |
| **Falsches Layout exportiert** | Tippfehler im Layoutnamen | Überprüfen Sie die Layoutnamen mit einem CAD‑Viewer; verwenden Sie den genauen String in `setLayouts()`. |
| **Lizenzausnahme** | Ausführung ohne gültige Lizenz in der Produktion | Wenden Sie eine temporäre oder permanente Lizenz an, wie im FAQ beschrieben. |

## Frequently Asked Questions (Extended)

**F: Kann ich Aspose.CAD für Java mit anderen Programmiersprachen verwenden?**  
A: Aspose.CAD unterstützt hauptsächlich Java, es gibt jedoch Versionen für andere Sprachen wie .NET.

**F: Gibt es Lizenzoptionen für Aspose.CAD?**  
A: Ja, Sie können Lizenzoptionen prüfen und Aspose.CAD [hier](https://purchase.aspose.com/buy) erwerben.

**F: Gibt es eine kostenlose Testversion für Aspose.CAD?**  
A: Natürlich, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

**F: Wie kann ich Support für Aspose.CAD für Java erhalten?**  
A: Besuchen Sie das Aspose.CAD‑Forum [hier](https://forum.aspose.com/c/cad/19) für umfassenden Support.

**F: Kann ich eine temporäre Lizenz für Aspose.CAD erhalten?**  
A: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erwerben.

---

**Zuletzt aktualisiert:** 2025-12-25  
**Getestet mit:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}