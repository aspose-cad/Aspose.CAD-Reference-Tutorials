---
date: 2026-08-29
description: Aprenda cómo establecer el tamaño de página PDF y convertir CAD a PDF
  usando Aspose.CAD para Java, con escalado automático del diseño y exportación a
  TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Establecer tamaño de página PDF – convertir CAD a PDF
og_description: Aprenda cómo establecer el tamaño de página PDF al convertir dibujos
  CAD a PDF en Java usando Aspose.CAD. Esta guía cubre dimensiones del lienzo, escalado
  automático del diseño y exportación a TIFF de alta resolución.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Establecer tamaño de página PDF – convertir CAD a PDF con Aspose en Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Establecer tamaño de página PDF – convertir CAD a PDF (Java)
url: /es/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer tamaño de página PDF – convertir CAD a PDF (Java)

## Introducción

Si necesitas **establecer el tamaño de página PDF** al convertir dibujos CAD a PDF, has llegado al lugar correcto. En este tutorial te mostraremos cómo usar Aspose.CAD para Java para definir dimensiones exactas del lienzo, habilitar el escalado automático del diseño y luego exportar el resultado tanto a PDF como a TIFF. Ya sea que estés preparando esquemas de ingeniería para impresión o generando miniaturas para una galería web, controlar el tamaño de la página y la resolución de salida es esencial.

## Respuestas rápidas
- **¿Qué significa “convertir CAD a PDF”?** Transformar un dibujo CAD (p. ej., DXF, DWG) en un documento PDF que puede visualizarse en cualquier plataforma.  
- **¿Puedo también exportar a TIFF?** Sí—usa `TiffOptions` para crear imágenes rasterizadas de alta resolución.  
- **¿Qué opción controla el tamaño del lienzo en Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **¿Qué es el escalado automático del diseño?** Una bandera (`setAutomaticLayoutsScaling(true)`) que preserva las proporciones originales del diseño cuando el tamaño del lienzo cambia.  
- **¿Necesito una licencia para Aspose.CAD?** Se requiere una licencia temporal o permanente para uso en producción.

## Cómo establecer el tamaño de página PDF al convertir CAD a PDF en Java

Carga tu archivo CAD, configura `CadRasterizationOptions` con el ancho y alto deseados, habilita el escalado automático del diseño y luego guarda el resultado como PDF. Este enfoque de dos pasos te permite controlar las dimensiones exactas de la página de salida sin sacrificar la calidad vectorial.

## Qué es convertir CAD a PDF?

Convertir CAD a PDF significa tomar dibujos de ingeniería basados en vectores y renderizarlos como páginas PDF, preservando líneas, capas y geometría mientras se hace el archivo universalmente accesible. El proceso rasteriza el dibujo según las opciones especificadas, produciendo un PDF que puede abrirse en cualquier dispositivo sin requerir software CAD, y mantiene la fidelidad visual del diseño original.

## Por qué establecer el tamaño del lienzo en Java?

Establecer el tamaño del lienzo en Java te permite definir la resolución de salida y las dimensiones de la página, asegurando que el PDF o TIFF resultante coincida con tus requisitos de impresión o visualización. También te brinda control sobre el comportamiento de escalado, lo cual es esencial para dibujos de gran formato.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de que tienes los siguientes requisitos:

- Aspose.CAD para Java: Asegúrate de que tienes la biblioteca Aspose.CAD instalada en tu entorno Java. Puedes descargar la biblioteca Aspose.CAD para Java [aquí](https://releases.aspose.com/cad/java/).
- Directorio de documentos: Configura un directorio de documentos para almacenar tus archivos CAD. Este directorio será referenciado en los pasos del tutorial.

Ahora, comencemos con la guía paso a paso.

## Importar espacios de nombres

En este paso, importaremos los espacios de nombres necesarios para iniciar tu proyecto Aspose.CAD.

`Image` es la clase principal utilizada para cargar archivos CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Paso 1: importar clases de Aspose.CAD

La clase `Image` proporciona métodos para cargar y guardar dibujos CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

En este fragmento, configuramos la ruta al directorio de recursos y cargamos un archivo DXF usando la clase `Image` de Aspose.CAD.

## Paso 2: establecer propiedades de CadRasterizationOptions (establecer tamaño del lienzo en Java)

`CadRasterizationOptions` especifica la configuración de rasterización, como el tamaño de página y el escalado para la conversión de CAD a raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Aquí, creamos una instancia de `CadRasterizationOptions` y configuramos propiedades como el ancho de página, la altura de página y **el escalado automático del diseño**. Esto es el núcleo de **configurar el modo de lienzo** para tu conversión.

## Paso 3: crear PdfOptions y establecer vectorRasterizationOptions

`PdfOptions` define la configuración de salida PDF para la conversión.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ahora, creamos una instancia de `PdfOptions` y establecemos su propiedad `VectorRasterizationOptions` a la `CadRasterizationOptions` configurada previamente.

## Paso 4: exportar a PDF (convertir CAD a PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finalmente, guardamos la imagen CAD en un archivo PDF usando las opciones especificadas, completando el proceso de **convertir CAD a PDF**.

## Paso 5: crear TiffOptions y establecer vectorRasterizationOptions (exportar CAD a TIFF)

`TiffOptions` configura los parámetros de salida TIFF, como compresión y resolución.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

En este paso, configuramos una instancia de `TiffOptions` y establecemos su propiedad `VectorRasterizationOptions`.

## Paso 6: exportar a TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Finalmente, guardamos la imagen CAD en un archivo TIFF usando las opciones especificadas, demostrando cómo **exportar CAD a TIFF** después de configurar el tamaño del lienzo.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| PDF de salida en blanco | `setNoScaling(true)` deshabilita el renderizado para algunos dibujos | Elimina `setNoScaling(true)` o establécelo en `false`. |
| La resolución del TIFF parece baja | Ancho/alto de página demasiado pequeño | Incrementa los valores de `setPageWidth` / `setPageHeight`. |
| El diseño se ve distorsionado | El escalado automático del diseño está deshabilitado | Asegúrate de que `setAutomaticLayoutsScaling(true)` esté habilitado. |

## Por qué ajustar el tamaño del lienzo y DPI?

Cambiar el tamaño del lienzo influye directamente en la resolución de rasterización de la salida. Si necesitas **incrementar la resolución del TIFF**, simplemente aumenta los valores de `setPageWidth` / `setPageHeight` o llama a `rasterizationOptions.setResolution(300)` antes de crear el `TiffOptions`. Esto te brinda imágenes rasterizadas de alta calidad adecuadas para impresión o inspección detallada.

## Preguntas frecuentes

**Q1: ¿puedo usar Aspose.CAD para Java con otros frameworks Java?**  
R: Sí, Aspose.CAD está diseñado para integrarse sin problemas con varios frameworks Java.

**Q2: ¿está disponible una licencia temporal para Aspose.CAD?**  
R: Sí, puedes obtener una licencia temporal en la página [aquí](https://purchase.aspose.com/temporary-license/).

**Q3: ¿dónde puedo obtener soporte comunitario para Aspose.CAD?**  
R: Visita el foro de Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para soporte y discusiones de la comunidad.

**Q4: ¿puedo probar Aspose.CAD gratis?**  
R: ¡Por supuesto! Obtén una página de descarga de prueba gratuita [aquí](https://releases.aspose.com/).

**Q5: ¿cómo compro Aspose.CAD para Java?**  
R: Compra Aspose.CAD para Java [aquí](https://purchase.aspose.com/buy).

**Q: ¿el tamaño del lienzo afecta la calidad vectorial en el PDF?**  
R: No. El tamaño del lienzo controla las dimensiones de la página; los datos vectoriales siguen siendo independientes de la resolución, garantizando un renderizado nítido a cualquier nivel de zoom.

**Q: ¿puedo establecer un DPI diferente para la salida TIFF?**  
R: Sí. Ajusta `rasterizationOptions.setResolution(dpiValue)` antes de crear `TiffOptions`.

**Q: ¿cómo puedo cambiar las dimensiones del PDF para un PDF existente sin volver a renderizar el CAD?**  
R: Usa Aspose.PDF para cargar el PDF generado y llama a `pdf.getPages().setPageSize(PageSize.A4)` o a un tamaño personalizado.

**Q: ¿cuál es la mejor manera de convertir dxf a pdf preservando capas?**  
R: Mantén `setAutomaticLayoutsScaling(true)` y evita `setNoScaling(true)`; esto conserva la visibilidad de capas y la fidelidad del diseño.

## Conclusión

¡Felicidades! Has convertido con éxito **CAD a PDF** y **exportado CAD a TIFF** mientras **establecías el tamaño del lienzo en Java**, habilitando **el escalado automático del diseño**, y aprendiendo a **configurar el modo de lienzo** para salidas de alta calidad. Este tutorial brinda una base sólida para tus proyectos de conversión CAD. Explora más funciones y posibilidades en la [documentación de Aspose.CAD](https://reference.aspose.com/cad/java/).

**Última actualización:** 2026-08-29  
**Probado con:** Aspose.CAD for Java 24.12  
**Autor:** Aspose

## Tutoriales relacionados

- [Establecer tamaño del lienzo – Funciones CAD avanzadas con Aspose.CAD para Java](/cad/java/advanced-cad-features/)
- [Exportar DWG a PDF en Java – Establecer tamaño de página PDF con Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Establecer tamaño de página personalizado – PDF desde CAD con escalado automático del diseño](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}