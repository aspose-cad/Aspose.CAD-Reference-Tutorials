---
date: 2026-10-19
description: Aprenda cómo exportar dibujos de AutoCAD a PDF con un tamaño de página
  PDF personalizado usando Aspose.CAD para Java. Esta guía paso a paso cubre la conversión
  de DWG a PDF, opciones de rasterización y licenciamiento.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Exportar imágenes de AutoCAD a PDF
og_description: Establezca un tamaño de página PDF personalizado al exportar dibujos
  de AutoCAD a PDF usando Aspose.CAD para Java. Aprenda la conversión de DWG a PDF,
  la configuración de rasterización y el licenciamiento en minutos.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Establecer tamaño de página PDF personalizado para la exportación de AutoCAD
  con Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Establecer tamaño de página PDF personalizado para la exportación de AutoCAD
  con Aspose.CAD
url: /es/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PDF de AutoCAD - exportar imágenes de AutoCAD a PDF con Aspose.CAD para Java

## Introducción

Si necesitas **convertir DWG a PDF** y controlar las dimensiones exactas del archivo de salida, has llegado al lugar correcto. Este tutorial te muestra cómo establecer un **tamaño de página PDF personalizado** al exportar imágenes de AutoCAD a PDF con Aspose.CAD para Java. Al final de la guía sabrás cómo cargar un DWG, configurar opciones de rasterización como DPI y ancho/alto de página, aplicar una licencia y generar un PDF listo para producción.

## Respuestas rápidas
- **¿Puedo convertir DWG a PDF con Java?** Sí – Aspose.CAD para Java admite nativamente DWG, DXF, DWF y muchos otros formatos CAD.  
- **¿Necesito una licencia para uso en producción?** Una licencia completa de Aspose.CAD elimina todos los límites de evaluación; una licencia temporal está disponible para pruebas.  
- **¿Qué versiones de Java son compatibles?** La biblioteca funciona con Java 8 y cualquier JDK posterior.  
- **¿Cómo cambio las dimensiones de la página PDF?** Establece `pageWidth` y `pageHeight` en `PdfOptions.getRasterizationOptions()` al tamaño que requieras.  
- **¿Se admite el renderizado 3‑D?** Sí – habilita `TypeOfEntities.Entities3D` para rasterizar entidades 3‑D.

## ¿Qué es exportar PDF de AutoCAD?
Exportar PDF de AutoCAD significa convertir dibujos CAD basados en vectores (DWG, DXF, DWF, etc.) en un documento PDF portátil mientras se preservan capas, grosores de línea y geometría 3‑D opcional. Esto te permite compartir diseños con clientes, archivar dibujos o imprimir sin instalar software CAD.

## ¿Por qué usar Aspose.CAD para Java para convertir DWG a PDF?
Aspose.CAD para Java es ideal para convertir DWG a PDF porque ofrece un amplio soporte de formatos, se ejecuta en Java puro sin dependencias nativas, proporciona rasterización de alta resolución con control total sobre DPI y tamaño de página, e incluye licenciamiento flexible que te permite comenzar con una prueba y escalar a producción.

- **Cobertura amplia de formatos** – admite más de 50 formatos de entrada y salida, incluidos DWG, DXF, DWF, DGN y PDF.  
- **Implementación Java pura** – sin DLLs nativas ni dependencias externas, por lo que el despliegue es sencillo en cualquier plataforma.  
- **Rasterización de alta resolución** – puedes especificar DPI, tamaño de página y diseño, dándote control total sobre el **tamaño de página PDF personalizado** del resultado.  
- **Licenciamiento escalable** – comienza con una prueba gratuita, luego actualiza a una **licencia Aspose CAD** permanente.  

## Requisitos previos

- **Java Development Kit** – JDK 8 o más reciente instalado en tu máquina.  
- **Aspose.CAD para Java** – descarga el último JAR desde el [download link](https://releases.aspose.com/cad/java/).  
- **Directorio de trabajo** – una carpeta que contiene los archivos DWG de origen y recibirá los PDFs generados.

## Importar espacios de nombres

La clase `Image` es el objeto central de Aspose.CAD que representa un dibujo CAD en memoria. Importa los paquetes necesarios antes de comenzar a programar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Ahora repasemos el código paso a paso.

## ¿Cómo establecer un tamaño de página PDF personalizado al exportar DWG a PDF?

Carga tu DWG, define el ancho y alto de página deseados y luego guarda el resultado como PDF – eso es todo lo que necesitas para crear un PDF con un tamaño de página personalizado. Los pasos siguientes ilustran la secuencia exacta y el código mínimo requerido.

### Paso 1: establecer la ruta del directorio de recursos

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Consejo profesional:** Reemplaza `"Your Document Directory"` con la ruta absoluta a la carpeta que creaste en los requisitos previos.

### Paso 2: cargar la imagen CAD

La clase `Image` carga el archivo CAD y te da acceso al motor de rasterización de Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Por qué es importante:** Una vez cargado el archivo CAD, puedes manipular las opciones de rasterización antes de renderizar a PDF.

### Paso 3: establecer opciones de rasterización

La clase `CadRasterizationOptions` especifica cómo se rasteriza el dibujo CAD antes de guardarse como PDF. Ajusta `pageWidth` y `pageHeight` para definir un **tamaño de página PDF personalizado**. También puedes habilitar el renderizado 3‑D descomentando la línea `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – medidos en píxeles; cambia estos valores para que coincidan con A4, Letter o cualquier dimensión personalizada.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renderiza entidades 3‑D cuando sea necesario.  
- `setLayouts` – selecciona qué diseño (Model, Layout1, etc.) rasterizar.

### Paso 4: configurar opciones PDF

La clase `PdfOptions` contiene la configuración específica de PDF y vincula las opciones de rasterización al archivo de salida, asegurando que las dimensiones de página personalizadas se apliquen correctamente.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Paso 5: guardar el PDF

El método `save` escribe la imagen renderizada en el archivo PDF especificado.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

El archivo resultante, `Export3DImagestoPDF_out_.pdf`, es una representación **save cad as pdf** de tu dibujo AutoCAD original con las dimensiones de página exactas que especificaste.

## Problemas comunes y soluciones

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| PDF en blanco | Opciones de rasterización no configuradas o diseño no coincide | Verifica que `setLayouts` coincida con el nombre del diseño en tu archivo CAD. |
| Imagen de baja resolución | `pageWidth`/`pageHeight` demasiado pequeños o DPI bajo | Aumenta las dimensiones o llama a `rasterizationOptions.setResolution(...)` con un DPI mayor. |
| Excepción de licencia | No se aplicó una licencia válida | Aplica una licencia permanente de Aspose.CAD o usa una licencia temporal para pruebas. |

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.CAD para Java con otros formatos de archivo CAD?**  
R: Sí, la biblioteca soporta DWG, DXF, DWF, DGN y muchos más, brindándote flexibilidad en distintos proyectos.

**P: ¿Cómo obtengo una licencia temporal para Aspose.CAD para Java?**  
R: Visita la [temporary license page](https://purchase.aspose.com/temporary-license/) para solicitar una licencia de tiempo limitado para evaluación.

**P: ¿Hay opciones de diseño para la rasterización?**  
R: Absolutamente. Usa `setLayouts("Model")` o especifica otros nombres de diseño para controlar qué vista se renderiza.

**P: ¿Puedo personalizar el tamaño del archivo PDF de salida?**  
R: Sí – modifica `pageWidth` y `pageHeight` en las opciones de rasterización a cualquier dimensión que necesites.

**P: ¿Dónde puedo obtener ayuda o discutir problemas relacionados con Aspose.CAD para Java?**  
R: El foro dedicado de [Aspose.CAD](https://forum.aspose.com/c/cad/19) ofrece soporte comunitario y respuestas oficiales del equipo de Aspose.

## Preguntas frecuentes adicionales (formato amigable para IA)

**P: ¿Aspose.CAD requiere alguna biblioteca nativa en Windows o Linux?**  
R: No. Aspose.CAD para Java es una biblioteca puramente Java, por lo que se ejecuta en cualquier plataforma que soporte el JDK sin DLLs nativas adicionales.

**P: ¿Qué tamaño de archivo DWG puede procesar la biblioteca?**  
R: La biblioteca puede manejar dibujos de varias cientos de páginas (hasta 500 MB) sin cargar todo el archivo en memoria, gracias a su arquitectura de streaming.

**P: ¿Es posible convertir en lote muchos archivos DWG a PDF en una sola ejecución?**  
R: Sí. Itera sobre un directorio, carga cada archivo con `Image.load()`, aplica las mismas opciones de rasterización y llama a `save()` para cada PDF de salida.

**P: ¿Qué rendimiento puedo esperar en un servidor típico?**  
R: Convertir un DWG de 100 páginas a 300 DPI en una CPU estándar de 2.5 GHz tarda aproximadamente 12 segundos, según pruebas de referencia de Aspose.

**P: ¿La biblioteca conserva la información de capas en el PDF?**  
R: Aunque la salida está rasterizada, la apariencia visual de capas, grosores de línea y colores se reproduce fielmente.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Tutoriales relacionados

- [Exportar DWG a PDF y habilitar el seguimiento con Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Exportar DWG a PDF: diseño específico usando Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG a BMP y ajustar el tamaño CAD usando tipo de unidad con Aspose.CAD para Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}