---
title: Conversión de Java DGN a JPEG con el tutorial Aspose.CAD
linktitle: Exportación de DGN en formato AutoCAD a formato de imagen rasterizada
second_title: API de Java Aspose.CAD
description: Aprenda a exportar archivos DGN a imágenes JPEG en Java usando Aspose.CAD. Este tutorial paso a paso lo guiará a través del proceso sin esfuerzo.
weight: 13
url: /es/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversión de Java DGN a JPEG con el tutorial Aspose.CAD

## Introducción

Bienvenido a este completo tutorial sobre cómo exportar archivos DGN (diseño) a formato de imagen rasterizada utilizando Aspose.CAD para Java. Aspose.CAD es una potente biblioteca que permite a los desarrolladores de Java trabajar con archivos CAD sin problemas. En este tutorial, lo guiaremos a través del proceso de conversión de archivos DGN a imágenes JPEG, brindándole instrucciones paso a paso y ejemplos de código.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
1.  Biblioteca Aspose.CAD: asegúrese de tener instalada la biblioteca Aspose.CAD para Java. Puedes descargarlo[aquí](https://releases.aspose.com/cad/java/).
2. Kit de desarrollo de Java (JDK): asegúrese de tener Java instalado en su máquina.
3. Entorno de desarrollo integrado (IDE): utilice un IDE compatible con Java como IntelliJ o Eclipse.

## Importar paquetes

En su proyecto Java, importe los paquetes necesarios para Aspose.CAD. Agregue las siguientes líneas a su código:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Paso 1: cargar el archivo DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Paso 2: crear el objeto JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Paso 3: asignar opciones de rasterización

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Paso 4: guarde la imagen convertida

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Repita estos pasos para sus archivos DGN específicos, ajustando las rutas de los archivos en consecuencia.

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo exportar archivos DGN a formato de imagen rasterizada utilizando Aspose.CAD para Java. Este tutorial le ha proporcionado el conocimiento para incorporar esta funcionalidad en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para Java con otros formatos de archivos CAD?

R1: Sí, Aspose.CAD admite varios formatos CAD, lo que proporciona una solución versátil para los desarrolladores de Java.

### P2: ¿Hay una prueba gratuita disponible de Aspose.CAD para Java?

 R2: Sí, puedes acceder a una prueba gratuita[aquí](https://releases.aspose.com/).

### P3: ¿Dónde puedo encontrar documentación para Aspose.CAD para Java?

 A3: consulte la documentación[aquí](https://reference.aspose.com/cad/java/).

### P4: ¿Cómo puedo obtener soporte para Aspose.CAD para Java?

 A4: Visita el foro de soporte[aquí](https://forum.aspose.com/c/cad/19).

### P5: ¿Dónde puedo comprar una licencia de Aspose.CAD para Java?

 R5: Puedes comprar una licencia[aquí](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
