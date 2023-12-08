---
title: Exporte DGN incrustado a PDF con Aspose.CAD para Java
linktitle: Exportar DGN integrado
second_title: API de Java Aspose.CAD
description: Explore la guía paso a paso sobre cómo exportar archivos DGN incrustados a PDF usando Aspose.CAD para Java. Mejore sus aplicaciones Java con una manipulación perfecta de archivos CAD.
type: docs
weight: 11
url: /es/java/dgn-export-options/export-embedded-dgn/
---
## Introducción

Bienvenido a este tutorial completo sobre cómo exportar archivos DGN incrustados usando Aspose.CAD para Java. Aspose.CAD es una potente biblioteca que permite a los desarrolladores de Java trabajar con archivos CAD sin problemas. En este tutorial, lo guiaremos a través del proceso de exportar archivos DGN incrustados a PDF siguiendo instrucciones paso a paso. Si es un desarrollador experimentado o recién comienza, este tutorial lo ayudará a aprovechar las capacidades de Aspose.CAD para mejorar sus aplicaciones Java.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de tener los siguientes requisitos previos:
- Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java configurado en su máquina.
-  Aspose.CAD para Java: descargue e instale la biblioteca Aspose.CAD para Java desde[aquí](https://releases.aspose.com/cad/java/).

## Importar paquetes

Para comenzar, necesita importar los paquetes necesarios en su proyecto Java. Agregue las siguientes declaraciones de importación a su código:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ahora, dividamos el código de ejemplo en varios pasos:

## Paso 1: configurar rutas de entrada y salida

Defina la ruta del directorio donde se encuentra su documento y especifique el nombre del archivo DWG de entrada.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Paso 2: cargar el archivo DWG

 Cargue el archivo DWG en un`Image` objeto usando Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Paso 3: configurar las opciones de rasterización

Configure las opciones de rasterización, como los diseños que se incluirán en la exportación.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Paso 4: configurar las opciones de PDF

Configure las opciones de PDF, incluidas las opciones de rasterización vectorial.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Paso 5: guarde el archivo PDF

Guarde el archivo PDF con las opciones configuradas.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Conclusión

¡Felicidades! Ha exportado exitosamente un archivo DGN incrustado a PDF usando Aspose.CAD para Java. Este tutorial cubrió los pasos esenciales para integrar Aspose.CAD en su aplicación Java para una manipulación eficiente de archivos CAD.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para Java en un proyecto comercial?

 R1: Sí, Aspose.CAD para Java es una biblioteca comercial. Puede obtener una licencia de[aquí](https://purchase.aspose.com/buy).

### P2: ¿Hay una prueba gratuita disponible?

 R2:Sí, puede acceder a una prueba gratuita de Aspose.CAD para Java[aquí](https://releases.aspose.com/).

### P3: ¿Cómo puedo obtener soporte para Aspose.CAD para Java?

R3: Puede buscar ayuda de la comunidad Aspose.CAD en el[foro](https://forum.aspose.com/c/cad/19).

### P4: ¿Qué pasa si necesito una licencia temporal?

 R4: Puede obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo encontrar la documentación?

 A5: La documentación está disponible.[aquí](https://reference.aspose.com/cad/java/).