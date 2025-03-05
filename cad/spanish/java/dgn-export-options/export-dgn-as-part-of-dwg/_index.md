---
title: Exporte DGN a DWG con Aspose.CAD para Java
linktitle: Exportar DGN como parte de DWG
second_title: API de Java Aspose.CAD
description: Explore cómo exportar DGN como parte de DWG usando Aspose.CAD para Java. Siga nuestra guía paso a paso para una manipulación eficiente de archivos CAD.
type: docs
weight: 10
url: /es/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Introducción

En este tutorial, exploraremos cómo usar Aspose.CAD para Java para exportar un archivo DGN (MicroStation Design) como parte de un archivo DWG (AutoCAD Drawing). Aspose.CAD es una poderosa biblioteca que proporciona una funcionalidad integral para trabajar con formatos de archivos CAD. Esta guía paso a paso le ayudará a comprender el proceso de exportación de DGN como parte de DWG utilizando Java.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
1. Biblioteca Aspose.CAD: descargue e instale la biblioteca Aspose.CAD para Java. Puedes encontrar la biblioteca.[aquí](https://releases.aspose.com/cad/java/).
2. Kit de desarrollo de Java (JDK): asegúrese de tener Java instalado en su sistema.
3. Entorno de desarrollo integrado (IDE): elija un IDE de Java como Eclipse o IntelliJ para una experiencia de desarrollo más fluida.

## Importar paquetes

En su proyecto Java, importe los paquetes Aspose.CAD necesarios para permitir la manipulación de archivos CAD. He aquí un ejemplo:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Paso 1: establecer rutas de archivo

 Defina las rutas de los archivos de entrada y salida para el archivo DWG. Actualizar el`dataDir`, `fileName` , y`outPath` variables en consecuencia.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Paso 2: crear una instancia de PdfOptions

 Crear una instancia del`PdfOptions` clase, ya que estamos exportando el archivo DWG a formato PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Paso 3: cargar el archivo DWG

 Cargue el archivo DWG existente como una imagen y conviértalo al formato`CadImage` tipo.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Paso 4: iterar a través de entidades

Revise cada entidad dentro del archivo DWG y verifique si es una definición de imagen. Si es así, recupere la referencia externa al objeto.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Paso 5: definir las opciones de rasterización

 Definir ajustes para el`CadRasterizationOptions`objeto, incluido el ancho y alto de la página, los diseños y el color de fondo.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Paso 6: configurar las opciones de rasterización vectorial

Establezca las opciones de rasterización vectorial para la exportación.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Paso 7: exportar DWG a PDF

 Finalmente, exporte el DWG a PDF llamando al`save` método.

```java
cadImage.save(outPath, exportOptions);
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo exportar un archivo DGN como parte de un archivo DWG usando Aspose.CAD para Java. Esta poderosa biblioteca proporciona amplias capacidades para trabajar con archivos CAD, lo que hace que sus tareas de manipulación de archivos CAD sean eficientes y sencillas.

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.CAD para Java?

 A1: La documentación se puede encontrar[aquí](https://reference.aspose.com/cad/java/).

### P2: ¿Cómo puedo descargar la biblioteca Aspose.CAD para Java?

 A2: Puede descargar la biblioteca desde[este enlace](https://releases.aspose.com/cad/java/).

### P3: ¿Existe una prueba gratuita de Aspose.CAD para Java?

 R3: Sí, puedes encontrar la prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener una licencia temporal de Aspose.CAD para Java?

 A4: Obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Necesita ayuda o tiene preguntas?

 R5: Visite el foro de soporte de la comunidad Aspose.CAD[aquí](https://forum.aspose.com/c/cad/19).