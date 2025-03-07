---
title: Agregar marcas de agua a dibujos CAD - Tutorial de Aspose.CAD para Java
linktitle: Agregar marca de agua
second_title: API de Java Aspose.CAD
description: Mejore sus dibujos CAD con marcas de agua personalizadas utilizando Aspose.CAD para Java. Siga nuestra guía paso a paso para una integración perfecta.
weight: 12
url: /es/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Agregar marcas de agua a dibujos CAD - Tutorial de Aspose.CAD para Java

## Introducción

Bienvenido a esta guía completa sobre cómo agregar marcas de agua a dibujos CAD usando Aspose.CAD para Java. En este tutorial, aprenderá cómo integrar marcas de agua de manera eficiente, mejorando sus documentos CAD con mensajes o marcas personalizados. Aspose.CAD para Java proporciona un potente conjunto de funciones que simplifican el proceso de adición de marcas de agua.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de tener los siguientes requisitos previos:

-  Aspose.CAD para Java: asegúrese de tener la biblioteca Aspose.CAD instalada en su entorno Java. Puedes descargarlo[aquí](https://releases.aspose.com/cad/java/).
- Kit de desarrollo de Java (JDK): asegúrese de tener instalada la última versión de JDK en su sistema.

## Importar paquetes

En su proyecto Java, importe los paquetes Aspose.CAD necesarios para comenzar:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Paso 1: agregar nuevo TEXTO M

```java
//agregar nuevo TEXTO M
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Paso 2: agregue una entidad simple como texto

También puedes agregar una entidad más sencilla como texto:

```java
// o agregue una entidad más simple como Texto
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Paso 3: exportar a PDF

Exporte el dibujo CAD con la marca de agua agregada a un archivo PDF:

```java
// exportar a pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Conclusión

¡Felicidades! Ha agregado con éxito marcas de agua a sus dibujos CAD utilizando Aspose.CAD para Java. Este proceso simple pero poderoso le permite personalizar sus diseños o protegerlos con su marca.

## Preguntas frecuentes

### P1: ¿Aspose.CAD es compatible con todos los formatos de archivos CAD?

R1: Aspose.CAD admite varios formatos CAD, incluidos DWG, DXF, DWT y DWF.

### P2: ¿Puedo personalizar la apariencia del texto de la marca de agua?

R2: Sí, tienes control total sobre la apariencia de la marca de agua, incluido el tamaño, el color y la posición del texto.

### P3: ¿Existe una versión de prueba disponible de Aspose.CAD para Java?

 R3: Sí, puedes descargar la versión de prueba.[aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener soporte para Aspose.CAD?

 A4: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para el apoyo de la comunidad.

### P5: ¿Dónde puedo encontrar la documentación completa de Aspose.CAD para Java?

 R5: Consulte el[documentación](https://reference.aspose.com/cad/java/) para obtener información detallada.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
