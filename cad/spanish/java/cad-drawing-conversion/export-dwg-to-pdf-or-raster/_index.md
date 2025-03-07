---
title: Exporte DWG a PDF o Raster usando Aspose.CAD para Java
linktitle: Exportar DWG a PDF o Raster
second_title: API de Java Aspose.CAD
description: Explore el sencillo proceso de exportar archivos DWG a PDF o imágenes rasterizadas en Java utilizando Aspose.CAD. Esta guía paso a paso garantiza precisión y eficiencia.
weight: 13
url: /es/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporte DWG a PDF o Raster usando Aspose.CAD para Java

## Introducción

En el dinámico mundo del diseño asistido por computadora (CAD), el manejo eficiente de los dibujos es crucial. Aspose.CAD para Java proporciona una poderosa solución para exportar archivos DWG a PDF o imágenes rasterizadas. Este tutorial lo guiará a través del proceso, asegurando que aproveche todo el potencial de Aspose.CAD para Java.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de tener lo siguiente:

- Conocimientos básicos de programación Java.
-  Biblioteca Aspose.CAD para Java instalada. Si no, descárgalo[aquí](https://releases.aspose.com/cad/java/).
- Un archivo DWG para fines de prueba. Puede utilizar el archivo "Bottom_plate.dwg" proporcionado.

## Importar espacios de nombres

En su proyecto Java, importe los espacios de nombres necesarios para iniciar el proceso:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Paso 1: cargue el archivo DWG

 Comience cargando su archivo DWG usando Aspose.CAD.`Image` clase:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Paso 2: determinar el tipo de unidad

A continuación, verifique el tipo de unidad del archivo DWG cargado:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Paso 3: configurar las opciones de rasterización

Según el tipo de unidad, configure las opciones de rasterización:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Unidades metricas
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // unidades imperiales
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Paso 4: configurar las opciones de PDF

Configure las opciones de exportación de PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Paso 5: guardar como PDF

Finalmente, guarde el archivo DWG como PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

¡Y ahí lo tienes! Ha exportado exitosamente un archivo DWG a PDF usando Aspose.CAD para Java.

## Conclusión

Este tutorial proporciona una guía paso a paso sobre cómo aprovechar Aspose.CAD para Java para exportar archivos DWG a PDF o imágenes rasterizadas. Esta biblioteca simplifica el proceso y le permite manejar de manera eficiente dibujos CAD en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.CAD para Java con otros marcos de Java?

R1: Sí, Aspose.CAD para Java se integra perfectamente con los marcos Java populares.

### P2: ¿Hay una licencia temporal disponible para Aspose.CAD para Java?

 R2: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P3: ¿Dónde puedo encontrar soporte para Aspose.CAD para Java?

 A3: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para recibir ayuda de la comunidad.

### P4: ¿Cómo puedo comprar una licencia de Aspose.CAD para Java?

 R4: Puedes comprar una licencia[aquí](https://purchase.aspose.com/buy).

### P5: ¿Qué unidades admite Aspose.CAD para Java?

R5: Aspose.CAD para Java admite unidades métricas e imperiales.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
