---
title: Guía de conversión de DGN a PDF - Aspose.CAD para Java
linktitle: Soporte para DGN V7
second_title: API de Java Aspose.CAD
description: Convierta archivos DGN a PDF sin esfuerzo utilizando Aspose.CAD para Java. Siga nuestra guía paso a paso para una integración perfecta y un flujo de trabajo eficiente.
type: docs
weight: 11
url: /es/java/other-cad-operations/support-for-dgn-v7/
---
## Introducción

En el dinámico mundo del CAD (diseño asistido por computadora), la conversión eficiente de archivos DGN (diseño) a PDF (formato de documento portátil) es un requisito crucial. Aspose.CAD para Java surge como una solución poderosa que ofrece una integración perfecta y capacidades sólidas. Esta guía paso a paso tiene como objetivo guiarlo a través del proceso de exportación de archivos DGN a PDF usando Aspose.CAD para Java, garantizando un flujo de trabajo fluido y eficiente.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
-  Biblioteca Aspose.CAD para Java: descargue e instale la biblioteca desde[Página de descarga de Aspose.CAD para Java](https://releases.aspose.com/cad/java/).
- Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java configurado en su máquina.

## Importar paquetes

Comience importando los paquetes necesarios a su proyecto Java:

## Paso 1: importar los paquetes necesarios

En su proyecto Java, importe los paquetes necesarios para Aspose.CAD para Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Paso 2: establecer rutas de archivos

Defina las rutas para su archivo DGN de entrada y el archivo PDF de salida.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Paso 3: cargar la imagen DGN

Cargue la imagen DGN usando la biblioteca Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Paso 4: configurar las opciones de exportación de PDF

Configure opciones para exportar a PDF, incluidas las dimensiones de la página, el escalado automático del diseño, el color de fondo y los diseños específicos para exportar.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //solo exporta 4 (1,2,3 y 9) vistas
options.setVectorRasterizationOptions(vectorOptions);
```

## Paso 5: guarde el archivo PDF

Guarde la imagen DGN como un archivo PDF con las opciones especificadas.

```java
objImage.save(outFile, options);
```

Repita estos pasos para diferentes archivos DGN, ajustando las rutas de archivo y las opciones según sea necesario.

## Conclusión

Con Aspose.CAD para Java, convertir archivos DGN a PDF se convierte en un proceso sencillo. Esta guía le brinda el conocimiento para integrar perfectamente la biblioteca en sus proyectos Java, facilitando conversiones eficientes de archivos CAD.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para Java con otros formatos de archivos CAD?

R1: Sí, Aspose.CAD admite varios formatos CAD, lo que proporciona una funcionalidad versátil más allá de la conversión de DGN a PDF.

### P2: ¿Hay una licencia temporal disponible para Aspose.CAD para Java?

 R2: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/) con fines de prueba.

### P3: ¿Cómo puedo buscar soporte o hacer preguntas sobre Aspose.CAD para Java?

 A3: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19)para conectarse con la comunidad y buscar ayuda.

### P4: ¿Qué diseños puedo exportar al convertir DGN a PDF?

 R4: Puede especificar los diseños para exportar personalizando el`setLayouts` matriz en el código.

### P5: ¿Dónde puedo encontrar documentación completa sobre Aspose.CAD para Java?

 R5: Consulte el[Documentación de Aspose.CAD para Java](https://reference.aspose.com/cad/java/) para obtener información detallada.