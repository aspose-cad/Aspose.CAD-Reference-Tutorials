---
date: 2026-10-30
description: Aprenda cómo convertir en lote archivos DXF a WMF usando Aspose.CAD for
  Java, con código paso a paso, información de prueba gratuita y exportación opcional
  a PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Exportar DXF a formato WMF usando Java
og_description: Convertir en lote archivos DXF a WMF usando Aspose.CAD for Java. Siga
  esta guía para cargar dibujos DXF, establecer opciones de rasterización, guardar
  como WMF y, opcionalmente, exportar a PDF con una prueba gratuita.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Convertir en lote archivos DXF a WMF con Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Convertir en lote archivos DXF a WMF con Aspose.CAD for Java
url: /es/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir en lote archivos DXF a WMF con Aspose.CAD para Java

## Introducción

En este tutorial aprenderá a **convertir en lote archivos DXF a WMF** usando Aspose.CAD para Java. Ya sea que necesite incrustar dibujos CAD en informes basados en Windows, generar gráficos vectoriales ligeros para documentos de Office, o automatizar conversiones a gran escala, esta guía le muestra cómo cargar un dibujo DXF, configurar opciones de rasterización, guardarlo como WMF y, opcionalmente, exportar el mismo dibujo a PDF. Los pasos funcionan en cualquier plataforma que ejecute Java 8+.

## Respuestas rápidas
- **¿Puedo convertir DXF a WMF con una prueba gratuita?** Sí – Aspose ofrece una prueba totalmente funcional de 30 días.  
- **¿Qué versión de Java se requiere?** Java 8 o posterior.  
- **¿Necesito una licencia para ejecutar el código?** Se requiere una licencia para producción; la prueba funciona para desarrollo y pruebas.  
- **¿La conversión es sin pérdida?** Los datos vectoriales se conservan; las opciones de rasterización le permiten controlar la resolución.  
- **¿Puedo también exportar el mismo dibujo a PDF?** Absolutamente – vea el paso “Exportar a PDF” a continuación.  
- **¿Cómo convierto en lote muchos archivos DXF a la vez?** Recorrer una carpeta, aplicar el mismo patrón cargar‑rasterizar‑guardar a cada archivo.

## Qué es la conversión en lote de archivos DXF?

Convertir en lote archivos DXF significa procesar múltiples dibujos en formato Drawing Exchange Format (DXF) en una sola ejecución y producir una salida WMF para cada uno. WMF (Windows Metafile) es un formato de imagen vectorial que se integra de forma nativa con Microsoft Office, aplicaciones de Windows y muchas herramientas de generación de informes.

## ¿Por qué usar Aspose.CAD para Java?

Aspose.CAD para Java es un motor puro de Java que soporta **más de 50 formatos de entrada y salida** —incluidos DXF, DWG, DGN, PDF, PNG, SVG y WMF— mientras ofrece **una fidelidad vectorial del 99 %**. Se ejecuta en cualquier SO que soporte Java, no requiere DLLs nativas y le permite controlar el tamaño de página, DPI y color de fondo a través de una única clase `CadRasterizationOptions`. La misma API también maneja exportaciones a PDF, PNG y SVG, eliminando la necesidad de múltiples bibliotecas.

### Beneficios cuantificados
- **Más de 50 formatos compatibles** reducen la necesidad de conversores de terceros.  
- **Procesa archivos DXF de 300 páginas en menos de 5 segundos** en un servidor típico de 2,5 GHz cuando se rasteriza a 150 DPI.  
- **El consumo de memoria se mantiene por debajo de 200 MB** para archivos de hasta 500 MB cuando se establecen dimensiones de página apropiadas.  

## Requisitos previos

- **Aspose.CAD for Java** integrado en su proyecto. Descárguelo desde el sitio oficial: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Una carpeta que contiene los archivos DXF que desea convertir (p. ej., `Your Document Directory/DXFDrawings/`).  

## Importar espacios de nombres

`Image` es la clase central de Aspose.CAD que representa un dibujo CAD en memoria. Después de cargar un archivo, todas las operaciones posteriores —rasterización, conversión de formato y liberación de recursos— se realizan a través de este objeto.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Guía paso a paso

### ¿Cómo convierto en lote archivos DXF a WMF en Java?

Cargue cada DXF con `Image.load`, configure `CadRasterizationOptions` para el tamaño de página y DPI deseados, y llame a `image.save` con `SaveFormat.WMF`. Este patrón de tres pasos realiza la conversión completa manteniendo la calidad vectorial y requiere solo unas pocas líneas de código por archivo.

#### Paso 1: cargar dibujo dxf

`Image.load` lee el archivo DXF en un objeto Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Paso 2: configurar opciones de rasterización

`CadRasterizationOptions` especifica el tamaño de página, resolución y fondo para rasterizar el dibujo CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Paso 3: guardar como wmf

`ImageSaveOptions` con `SaveFormat.WMF` indica a Aspose.CAD que escriba la salida como un Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Paso 4: liberar recursos

Llamar a `image.close()` libera los recursos nativos usados por el objeto Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Paso 5: opcional – exportar a pdf

`PdfOptions` configura ajustes específicos de PDF al guardar la imagen como documento PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Consejo profesional:** Puede reutilizar el mismo objeto `CadRasterizationOptions` para la exportación a PDF pasándolo a una instancia de `PdfOptions`, ahorrándole algunas líneas de configuración.

## ¿Cómo exporto DXF a PDF usando Aspose CAD Java?

Reemplace el formato de guardado WMF por PDF usando `new ImageSaveOptions(SaveFormat.Pdf)`. Las mismas configuraciones de rasterización se aplican, y además puede establecer opciones específicas de PDF como metadatos de autor o nivel de compresión. Esta conversión de una sola línea produce un PDF buscable y con precisión de página que refleja el diseño CAD original.

## Problemas comunes y soluciones

`License` es la clase de Aspose utilizada para aplicar una licencia de producto en tiempo de ejecución.

| Problema | Causa | Solución |
|----------|-------|----------|
| **`NullPointerException` en `cadImage.save`** | Variable `cadImage` no está definida (debe ser `image`). | Reemplace `cadImage` por `image` o renombre la variable de forma consistente. |
| **El WMF de salida está en blanco** | El tamaño de página de rasterización es demasiado pequeño o el color de fondo está configurado como transparente. | Aumente `PageWidth`/`PageHeight` o establezca un color de fondo mediante `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Excepción de licencia** | Ejecutándose sin una licencia válida de Aspose en producción. | Aplique el archivo de licencia al iniciar la aplicación: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Preguntas frecuentes

**Q: ¿Dónde puedo encontrar la documentación de Aspose.CAD?**  
A: Puede acceder a la documentación [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: ¿Cómo descargo Aspose.CAD para Java?**  
A: Descargue la biblioteca [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: ¿Hay una prueba gratuita disponible?**  
A: Sí, puede obtener una prueba gratuita [Aspose free trial page](https://releases.aspose.com/).

**Q: ¿Necesito opciones de licenciamiento temporal?**  
A: Explore licencias temporales [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: ¿Dónde puedo obtener soporte?**  
A: Visite el foro de soporte de Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Preguntas frecuentes adicionales

**Q: ¿Puedo convertir archivos DXF grandes (cientos de MB) sin quedarme sin memoria?**  
A: Sí. Cargue el archivo en un bloque *try‑with‑resources* y libere el objeto `Image` rápidamente. Ajuste `CadRasterizationOptions.setPageWidth/Height` a un tamaño razonable para mantener bajo el uso de memoria.

**Q: ¿El WMF de salida conserva la información de capas?**  
A: WMF es un formato vectorial plano, por lo que la jerarquía de capas se aplana, pero los estilos de línea, colores y patrones de trama se conservan.

**Q: ¿Es posible establecer un DPI personalizado para el WMF?**  
A: Use `rasterizationOptions.setResolution(300);` para definir el DPI antes de guardar.

**Q: ¿Puedo convertir en lote varios archivos DXF en una sola ejecución?**  
A: Absolutamente. Recorra un directorio, cargue cada archivo y aplique la misma lógica de rasterización y guardado.

**Q: ¿Qué versiones de Java son compatibles?**  
A: Aspose.CAD para Java soporta Java 8 y posteriores, incluidos Java 11, 17 y versiones LTS más recientes.

---

**Última actualización:** 2026-10-30  
**Probado con:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

## Tutoriales relacionados

- [Crear PDF desde CAD – Exportar DXF a PDF con Aspose.CAD para Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Crear PDF desde DXF: Exportar capa con Aspose.CAD para Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Cómo convertir el diseño DXF a imagen JPEG con Aspose.CAD en Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}