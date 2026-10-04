---
date: 2026-10-04
description: Aprenda cómo convertir rápidamente DWG a PNG y exportar CAD como PNG
  u otros formatos raster usando Aspose.CAD for Java. Obtenga resultados de alta calidad
  rápidamente.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Convertir diseño CAD a formato de imagen raster
og_description: Convierta DWG a PNG rápidamente con Aspose.CAD for Java. Aprenda paso
  a paso cómo exportar CAD como PNG, JPEG, TIFF y más.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Convertir DWG a PNG y otros formatos raster usando Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Convertir DWG a PNG y otros formatos raster usando Aspose.CAD for Java
url: /es/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG a PNG y otros formatos raster con Aspose.CAD para Java

## Introducción

`Aspose.CAD for Java` es una biblioteca que permite la conversión programática de archivos CAD a imágenes raster como PNG, JPEG y TIFF. Convertir DWG a PNG (u otros formatos de imagen raster) es un requisito común cuando necesitas compartir dibujos CAD con compañeros que no tienen un visor CAD, incrustar diseños en documentación o generar miniaturas para galerías web. En esta guía aprenderás a convertir dwg a png de forma rápida y fiable, ya sea que trabajes con un archivo de dibujo completo o solo con un diseño específico. También puede que necesites **convertir CAD a raster** para vistas previas web, herramientas de informes o aplicaciones móviles.

## Respuestas rápidas
- **¿Qué biblioteca maneja DWG a PNG?** Aspose.CAD for Java proporciona el motor de conversión.  
- **¿Qué formatos raster puedo exportar?** PNG, JPEG, TIFF, PDF, BMP y más de 30 formatos adicionales.  
- **¿Necesito una licencia para pruebas?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Puedo elegir un diseño específico?** Sí – usa `setLayouts` para apuntar a “Model”, “Layout1”, etc.  
- **¿Es posible obtener salida de alta resolución?** Absolutamente – ajusta `setPageWidth` y `setPageHeight` (o `setResolution`) para controlar DPI.

## ¿Qué significa “convert dwg to png”?

Convertir dwg a png implica transformar un dibujo vectorial DWG en una imagen PNG basada en píxeles que puede ser mostrada por cualquier visor de imágenes estándar. Este proceso rasteriza las entidades vectoriales, conservando el grosor de línea, colores y capas mientras las traduce a un mapa de bits de resolución fija. El resultado es ideal para incrustar en PDFs, documentos Word o páginas web donde el soporte vectorial es limitado.

## ¿Por qué exportar CAD como PNG (u otros formatos raster)?

Exportar CAD como PNG te brinda compatibilidad universal, carga rápida y fácil incrustación en todas las plataformas principales. Las imágenes raster se cargan al instante comparado con abrir un archivo DWG pesado, y la compresión sin pérdida de PNG garantiza fidelidad visual. Al controlar la resolución, el color de fondo y el diseño, garantizas que cada interesado vea la misma apariencia, ya sea que el archivo se visualice en escritorio, dispositivo móvil o dentro de un navegador.

## Casos de uso comunes

| Escenario | Por qué la salida raster ayuda |
|----------|------------------------|
| **Documentación de proyecto** | Incrustar PNG en PDFs o documentos Word evita requerir software CAD para los revisores. |
| **Portales web** | Las miniaturas generadas a partir de archivos DWG se cargan al instante y mejoran la experiencia del usuario. |
| **Aplicaciones móviles** | Las imágenes raster se muestran correctamente en dispositivos que no disponen de visores CAD. |
| **Informes automatizados** | Convertir por lotes varios diseños a PNG/JPEG para incluirlos en gráficos o paneles. |

## Requisitos previos

Antes de comenzar, asegúrate de tener:

1. **Entorno de desarrollo Java** – JDK 8 o superior instalado y configurado.  
2. **Aspose.CAD for Java** – Descarga el JAR más reciente desde la [documentación de Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Importar espacios de nombres

`com.aspose.cad.Image` es la clase central que representa cualquier archivo CAD en memoria. `com.aspose.cad.imageoptions.*` proporciona objetos de opción para cada formato raster. Importa las clases que necesitarás para cargar un dibujo, configurar la rasterización y guardar la salida.

> **Consejo profesional:** Si planeas **exportar CAD como PNG** en lugar de TIFF, reemplaza `TiffOptions` por `PngOptions` (ubicado en `com.aspose.cad.imageoptions.PngOptions`).

## Guía paso a paso

### Paso 1: configurar el directorio de recursos

Reemplaza `"Your Document Directory"` con la ruta absoluta donde se encuentran tus archivos CAD. Este directorio se usará tanto para los archivos de entrada como de salida.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Paso 2: cargar el archivo CAD

`Image.load` analiza el archivo fuente y crea una representación en memoria que puedes rasterizar. Puedes cargar cualquier formato compatible (DWG, DXF, DGN, etc.) – esta es la parte **cómo convertir cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Paso 3: configurar las opciones de rasterización

`CadRasterizationOptions` define cómo los datos vectoriales se convierten en píxeles. `setPageWidth` y `setPageHeight` controlan la resolución de salida (valores mayores = DPI más alto). `setLayouts` te permite **convertir CAD a raster** para diseños específicos; omítelo para rasterizar todo el dibujo.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Paso 4: establecer las opciones de imagen

`TiffOptions` (o `PngOptions` para PNG) indica a Aspose qué formato raster generar y te permite afinar la compresión, profundidad de color y otras configuraciones específicas del formato. Elige la clase de opciones que coincida con la salida deseada.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Paso 5: guardar la imagen resultante

Llama a `save` en la instancia `Image`, pasando el nombre del archivo de salida y el objeto de opciones. Cambia la extensión del archivo a `.png` (y usa `PngOptions`) para **guardar CAD como PNG**. El mismo patrón funciona para JPEG, BMP o PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Trampa común:** Olvidar que la extensión del archivo coincida con la clase de opciones provocará una `UnsupportedFormatException`. Mantén siempre ambas cosas sincronizadas.

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **Imagen de salida en blanco** | Verifica que los nombres de diseño en `setLayouts` coincidan exactamente con los del archivo CAD fuente. |
| **PNG de baja resolución** | Incrementa `setPageWidth` / `setPageHeight` o establece `setResolution` en las opciones de rasterización. |
| **Versión DWG no compatible** | Asegúrate de usar la última versión de Aspose.CAD; versiones anteriores pueden no soportar versiones DWG más recientes. |
| **Errores de memoria en archivos grandes** | Procesa las páginas una a una o aumenta el heap de JVM (`-Xmx2g`). |

## Preguntas frecuentes

**P: ¿Aspose.CAD es compatible con diferentes formatos de archivo CAD?**  
R: Sí, soporta más de 30 formatos CAD y raster, incluidos DWG, DXF, DGN y SVG.

**P: ¿Puedo personalizar la resolución de la imagen raster de salida?**  
R: Absolutamente. Ajusta `setPageWidth`, `setPageHeight` o `setResolution` en `CadRasterizationOptions` para lograr el DPI deseado.

**P: ¿Cómo puedo convertir varios diseños CAD en una sola ejecución?**  
R: Proporciona un arreglo con todos los nombres de diseño a `setLayouts`, por ejemplo `new String[]{"Model","Layout1","Layout2"}`.

**P: ¿Existen formatos de salida además de TIFF?**  
R: Sí—PNG, JPEG, BMP, PDF y más están disponibles a través de sus respectivas clases `*Options`.

**P: ¿Dónde puedo obtener ayuda o compartir mi experiencia con Aspose.CAD?**  
R: Visita el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte comunitario y asistencia oficial.

## Conclusión

Siguiendo estos pasos puedes **convertir DWG a PNG**, **exportar CAD como PNG**, **guardar CAD como JPEG** o generar cualquier otro formato raster que necesites. Aspose.CAD for Java se encarga del trabajo pesado, permitiéndote centrarte en integrar imágenes de alta calidad en tus aplicaciones, documentación o portales web. El soporte de la biblioteca para más de 30 formatos y su capacidad para renderizar dibujos de cientos de páginas sin cargar todo el archivo en memoria la convierten en una opción robusta para rasterización CAD de nivel empresarial.

---

**Última actualización:** 2026-10-04  
**Probado con:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Tutoriales relacionados

- [Exportar rápidamente DWG a PDF o Raster usando la biblioteca java cad Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Convertir DWG a BMP con Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Exportar DWG a PDF: Diseño específico usando Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}