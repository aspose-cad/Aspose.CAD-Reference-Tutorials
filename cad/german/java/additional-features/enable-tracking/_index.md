---
date: 2026-02-10
description: Schritt‑für‑Schritt‑Anleitung, wie man das Tracking in DWG‑Dateien mit
  Aspose.CAD für Java aktiviert und wie man DXF in PDF mit einem benutzerdefinierten
  Fehlerbehandler konvertiert.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Wie man das Tracking in DWG-Dateien mit Aspose.CAD in Java aktiviert
url: /de/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man das Tracking in DWG-Dateien mit Aspose.CAD in Java aktiviert

## Einleitung

Wenn Sie an kollaborativen CAD‑Projekten arbeiten, ist das **Aktivieren von Tracking** in Ihrem DWG‑Workflow ein echter Wendepunkt. Es liefert Echtzeit‑Einblicke in Render‑Probleme, ermöglicht das frühe Erkennen von Konvertierungsfehlern und hält alle Beteiligten informiert. In diesem Tutorial gehen wir Schritt für Schritt durch das Aktivieren von Tracking mit Aspose.CAD für Java und zeigen zudem **wie man DXF in PDF** im selben Durchlauf konvertiert. Am Ende verfügen Sie über ein vollständiges, produktionsreifes Snippet, das Fehler über eine **benutzerdefinierte Error‑Handler‑Java‑Klasse** meldet, während Ihre Zeichnungen exportiert werden.

## Schnelle Antworten
- **Was bewirkt “enable dwg tracking java”?** Es aktiviert die Error‑Handling‑Callbacks von Aspose.CAD, sodass Sie Render‑Probleme während des Exports sehen können.  
- **Brauche ich eine Lizenz?** Eine Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich auch DXF in PDF konvertieren?** Ja – dieselben `PdfOptions`, die für DWG verwendet werden, funktionieren auch für DXF und decken das *java convert dxf pdf*‑Szenario ab.  
- **Welche JDK‑Version wird benötigt?** Java 8 oder höher.  
- **Wo finde ich weitere Beispiele?** Siehe die Aspose.CAD Java‑Dokumentation über den untenstehenden Link.

## Wie man das Tracking in DWG-Dateien mit Aspose.CAD aktiviert

Das Aktivieren von DWG‑Tracking in einer Java‑Anwendung bedeutet, einen benutzerdefinierten Render‑Handler anzuhängen, der Warnungen, Fehler und andere Diagnoseinformationen erfasst, während die CAD‑Datei gerastert oder exportiert wird. Diese Transparenz hilft Entwicklern, Konvertierungspipelines zu debuggen und sorgt für qualitativ hochwertigere Ergebnisse.

## Warum Aspose.CAD für Java verwenden?

- **Vollständige CAD‑Unterstützung** – DWG, DXF, DGN und mehr.  
- **Keine externen Abhängigkeiten** – reine Java‑Bibliothek, ideal für serverseitige Automatisierung.  
- **Integriertes Tracking** – detaillierte Render‑Ergebnisse über `CadRenderHandler`.  
- **Einfache PDF‑Export** – Ein‑Zeilen‑Konvertierung bei gleichzeitiger Beibehaltung von Vektordaten.  

## Voraussetzungen

Bevor wir mit der Implementierung beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java Development Kit (JDK): Stellen Sie sicher, dass Java auf Ihrem System installiert ist.  
- Aspose.CAD für Java: Laden Sie Aspose.CAD für Java von dem [Download‑Link](https://releases.aspose.com/cad/java/) herunter und installieren Sie es.  
- Dokumenten‑Verzeichnis: Legen Sie ein Verzeichnis an, in dem Ihre DWG‑Dateien gespeichert sind.

## Namespaces importieren

Importieren Sie in Ihrem Java‑Projekt die notwendigen Namespaces, um die Funktionen von Aspose.CAD zu nutzen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Schritt 1: DWG‑Datei laden

Laden Sie die DWG‑ (oder DXF‑) Datei in Ihre Java‑Anwendung. Passen Sie den Dateipfad entsprechend an:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Schritt 2: PDF‑Exportoptionen konfigurieren (Wie man DXF in PDF konvertiert)

Richten Sie die PDF‑Exportoptionen ein und geben Sie die Vektor‑Rasterisierungsoptionen für CAD an. Dies demonstriert ebenfalls die *java convert dxf pdf*‑Fähigkeit:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Schritt 3: Tracking implementieren (Custom Error Handler Java)

Implementieren Sie das Tracking mithilfe einer benutzerdefinierten Error‑Handler‑Klasse. Diese Klasse erfasst Render‑Probleme und gibt sie in der Konsole aus:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Schritt 4: Export nach PDF

Starten Sie den Exportvorgang, um die DWG/DXF‑Datei mit aktiviertem Tracking in ein PDF zu konvertieren:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Schritt 5: CadRenderHandler‑Klasse

Definieren Sie die `ErrorHandler`‑Klasse (erweitert `CadRenderHandler`), um Render‑Ergebnisse zu verarbeiten und Tracking‑Informationen auszugeben:

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Warum das wichtig ist

Durch das Aktivieren von Tracking erhalten Sie eine klare Audit‑Trail aller Konvertierungsschritte. Das ist besonders wertvoll in regulierten Branchen (Architektur, Ingenieurwesen, Bauwesen), wo der Nachweis einer genauen Renderung für Compliance‑Audits erforderlich ist. Der benutzerdefinierte Error‑Handler bietet zudem einen Hook, um Probleme in ein Monitoring‑System zu protokollieren oder automatisierte Wiederholungen auszulösen.

## Häufige Probleme und Lösungen

- **`NullPointerException` bei `RenderResult`** – Stellen Sie sicher, dass Sie Aspose.CAD Version 23.10 oder neuer verwenden; ältere Versionen besitzen die `RenderResult`‑API nicht.  
- **Datei nicht gefunden** – Prüfen Sie, ob `dataDir` auf das richtige Verzeichnis zeigt und der Dateiname exakt (inklusive Groß‑/Kleinschreibung) übereinstimmt.  
- **Kein Tracking‑Output** – Vergewissern Sie sich, dass der benutzerdefinierte `ErrorHandler` korrekt `cadRasterizationOptions.RenderResult` zugewiesen wurde.

## Häufig gestellte Fragen

**F:** Kann ich das Tracking für andere CAD‑Dateiformate mit Aspose.CAD für Java aktivieren?  
**A:** Aspose.CAD unterstützt primär DWG‑Tracking. Für andere Formate siehe die offizielle Dokumentation.

**F:** Wie kann ich zusätzliche Export‑Optionen in Aspose.CAD für Java handhaben?  
**A:** Erkunden Sie die umfangreiche Dokumentation unter [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**F:** Gibt es eine Testversion von Aspose.CAD für Java?  
**A:** Ja, die Testversion erhalten Sie unter [Aspose.CAD Free Trial](https://releases.aspose.com/).

**F:** Wo kann ich Unterstützung erhalten oder Probleme zu Aspose.CAD für Java diskutieren?  
**A:** Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support.

**F:** Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für Java?  
**A:** Folgen Sie dem Prozess unter [Temporary License](https://purchase.aspose.com/temporary-license/).

## Fazit

Das Aktivieren von DWG‑Tracking in Java mit Aspose.CAD liefert nicht nur Einblick in Konvertierungsprobleme, sondern optimiert auch kollaborative Design‑Workflows. Mit den oben beschriebenen Schritten können Sie **Tracking aktivieren**, DXF nach PDF konvertieren und Render‑Probleme elegant handhaben.

---

**Zuletzt aktualisiert:** 2026-02-10  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}