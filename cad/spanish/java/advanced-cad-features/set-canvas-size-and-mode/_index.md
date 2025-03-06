---
title: Establecer tamaño y modo del lienzo
linktitle: Establecer tamaño y modo del lienzo
second_title: API de Java Aspose.CAD
description: Explore el poder de Aspose.CAD para Java con nuestra guía paso a paso sobre cómo configurar el tamaño y el modo del lienzo. Convierta archivos CAD a formatos PDF y TIFF sin esfuerzo.
weight: 16
url: /es/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer tamaño y modo del lienzo

## Introducción

¿Está buscando aprovechar el poder de Aspose.CAD para Java para mejorar su proceso de conversión de CAD? Esta guía completa lo guiará a través de los pasos para configurar el tamaño y el modo del lienzo usando Aspose.CAD para Java. Si es un desarrollador experimentado o recién está comenzando, este tutorial le brindará la información que necesita.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.CAD para Java: asegúrese de tener la biblioteca Aspose.CAD instalada en su entorno Java. Puedes descargarlo[aquí](https://releases.aspose.com/cad/java/).

- Directorio de documentos: configure un directorio de documentos para almacenar sus archivos CAD. Se hará referencia a este directorio en los pasos del tutorial.

Ahora comencemos con la guía paso a paso.

## Importar espacios de nombres

En este paso, importaremos los espacios de nombres necesarios para iniciar su proyecto Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Paso 1: Importar clases de Aspose.CAD

```java
// La ruta al directorio de recursos.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 En este fragmento, configuramos la ruta al directorio de recursos y cargamos un archivo DXF usando Aspose.CAD.`Image` clase.

## Paso 2: Establecer las propiedades de CadRasterizationOptions

```java
// Cree una instancia de CadRasterizationOptions y establezca sus diversas propiedades
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Aquí creamos una instancia de`CadRasterizationOptions` y configurar propiedades como el ancho de la página, el alto de la página y las opciones de escala.

## Paso 3: crear PdfOptions y configurar VectorRasterizationOptions

```java
// Crear una instancia de PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Establecer la propiedad VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Ahora, creamos un`PdfOptions` instancia y establecer su`VectorRasterizationOptions` propiedad a la previamente configurada`CadRasterizationOptions`.

## Paso 4: exportar a PDF

```java
// Exportar CAD a PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finalmente, guardamos la imagen CAD en un archivo PDF usando las opciones especificadas.

## Paso 5: cree TiffOptions y configure VectorRasterizationOptions

```java
// Crear una instancia de TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Establecer la propiedad VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

En este paso, configuramos un`TiffOptions` instancia y configurar su`VectorRasterizationOptions` propiedad.

## Paso 6: Exportar a TIFF

```java
// Exportar CAD a TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Finalmente, guardamos la imagen CAD en un archivo TIFF usando las opciones especificadas.

## Conclusión

 ¡Felicidades! Ha configurado correctamente el tamaño y el modo del lienzo utilizando Aspose.CAD para Java. Este tutorial proporciona una base sólida para sus proyectos de conversión CAD. Explora más características y posibilidades en el[Documentación de Aspose.CAD](https://reference.aspose.com/cad/java/).

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.CAD para Java con otros marcos de Java?

R1: Sí, Aspose.CAD está diseñado para integrarse perfectamente con varios marcos de Java.

### P2: ¿Hay una licencia temporal disponible para Aspose.CAD?

 R2: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P3: ¿Dónde puedo obtener soporte comunitario para Aspose.CAD?

 A3: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoyo y debates de la comunidad.

### P4: ¿Puedo probar Aspose.CAD gratis?

 R4: ¡Absolutamente! Obtenga una prueba gratuita[aquí](https://releases.aspose.com/).

### P5: ¿Cómo compro Aspose.CAD para Java?

 A5: comprar el producto[aquí](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
