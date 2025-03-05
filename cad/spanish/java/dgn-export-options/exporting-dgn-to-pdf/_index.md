---
title: Exportación de PDF de DGN a AutoCAD sin esfuerzo con Aspose.CAD para Java
linktitle: Exportación de DGN en formato AutoCAD a PDF
second_title: API de Java Aspose.CAD
description: Explore la guía paso a paso sobre cómo exportar archivos DGN a formato AutoCAD en PDF usando Aspose.CAD para Java. Aumente las capacidades de manejo de CAD de su aplicación Java sin esfuerzo.
type: docs
weight: 12
url: /es/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Introducción

Bienvenido a este completo tutorial sobre el uso de Aspose.CAD para Java para exportar archivos DGN en formato AutoCAD a PDF. Si busca mejorar la capacidad de su aplicación Java para manejar archivos CAD, Aspose.CAD es una excelente opción. En este tutorial, lo guiaremos a través del proceso de exportación de archivos DGN paso a paso.


## Requisitos previos
Antes de sumergirnos en el tutorial, asegúrese de tener los siguientes requisitos previos:
-  Biblioteca Aspose.CAD: asegúrese de tener instalada la biblioteca Aspose.CAD para Java. Puedes descargarlo[aquí](https://releases.aspose.com/cad/java/).
- Directorio de documentos: configure un directorio de documentos donde se almacenarán sus archivos de entrada y salida.

## Importar paquetes

En su proyecto Java, importe los paquetes necesarios para acceder a las funcionalidades de Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ahora, dividamos el código de ejemplo en varios pasos:

## Paso 1: definir rutas de archivos

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Asegúrese de reemplazar "Su directorio de documentos" con la ruta real donde se encuentran sus archivos.

## Paso 2: cargar la imagen DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Cargue el archivo DGN usando Aspose.CAD.

## Paso 3: configurar las opciones de exportación de PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Exportar vistas específicas
options.setVectorRasterizationOptions(vectorOptions);
```

Defina las opciones de exportación de PDF, incluidas las dimensiones de la página y las preferencias de diseño.

## Paso 4: guarde el archivo PDF

```java
objImage.save(outFile, options);
```

Guarde el archivo PDF exportado.

Repita estos pasos para cualquier archivo DGN adicional que desee convertir. ¡Felicidades! Ha exportado con éxito archivos DGN al formato de AutoCAD en PDF utilizando Aspose.CAD para Java.

## Conclusión

En este tutorial, exploramos cómo aprovechar Aspose.CAD para Java para mejorar las capacidades de manejo de archivos CAD de su aplicación. Con pasos fáciles de seguir y ejemplos de código, ahora puede exportar sin problemas archivos DGN al formato de AutoCAD en PDF.

## Preguntas frecuentes

### P1: ¿Aspose.CAD es compatible con todos los formatos de archivos CAD?

R1: Sí, Aspose.CAD admite una amplia gama de formatos CAD, lo que garantiza versatilidad en el manejo de varios tipos de archivos.

### P2: ¿Puedo personalizar la configuración de exportación de PDF?

R2: Absolutamente. Como se muestra en el tutorial, puede ajustar opciones como las dimensiones de la página y los diseños para adaptarlos a sus necesidades.

### P3: ¿Dónde puedo encontrar soporte o asistencia adicional?

 A3: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoyo y debates de la comunidad.

### P4: ¿Hay una prueba gratuita disponible?

 R4: Sí, puedes acceder a la prueba gratuita[aquí](https://releases.aspose.com/).

### P5: ¿Cómo puedo obtener una licencia temporal?

 R5: Obtenga una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).