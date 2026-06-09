---
date: 2026-06-09
description: Aprenda cómo convertir DXF a WMF con Aspose.CAD para Java, incluyendo
  una prueba gratuita, compatibilidad con Java 8+ y exportación opcional a PDF. Guía
  paso a paso con ejemplos de código.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Exportar DXF a formato WMF usando Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Convertir DXF a WMF usando Aspose.CAD en Java
url: /es/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DXF a WMF usando Aspose.CAD en Java

## Introducción

En este tutorial descubrirás cómo **convertir DXF a WMF** con Aspose.CAD para Java. Ya sea que necesites incrustar dibujos CAD en un informe basado en Windows, generar gráficos vectoriales ligeros para documentos de Office, o automatizar conversiones por lotes, convertir DXF a WMF es un requisito frecuente en pipelines de ingeniería e informes. Recorreremos la carga de un dibujo DXF, la configuración de opciones de rasterización, el guardado del resultado como WMF y, opcionalmente, la exportación del mismo dibujo a PDF.

## Respuestas rápidas
- **¿Puedo convertir DXF a WMF con una prueba gratuita?** Sí – Aspose ofrece una prueba totalmente funcional de 30 días.  
- **¿Qué versión de Java se requiere?** Java 8 o posterior.  
- **¿Necesito una licencia para ejecutar el código?** Se requiere licencia para producción; la prueba funciona para desarrollo y pruebas.  
- **¿La conversión es sin pérdida?** Los datos vectoriales se conservan; las opciones de rasterización permiten controlar la resolución.  
- **¿Puedo también exportar el mismo dibujo a PDF?** Por supuesto – consulta el paso “Exportar a PDF” a continuación.

## ¿Qué es “convertir DXF a WMF”?

Convertir DXF a WMF significa tomar un archivo Drawing Exchange Format (DXF) —un formato CAD ampliamente usado— y transformarlo en un Windows Metafile (WMF). WMF es un formato de imagen vectorial que se integra sin problemas con Microsoft Office, aplicaciones de Windows y muchas herramientas de generación de informes.

## ¿Por qué usar Aspose.CAD para Java?

Aspose.CAD para Java ofrece un motor puro‑Java, sin DLLs nativas, que convierte archivos CAD con **más del 99 % de fidelidad vectorial**, preservando capas, colores, estilos de línea y patrones de trama. Soporta **más de 50 formatos de entrada y salida** —incluidos DXF, DWG, DGN, PDF, PNG, SVG y WMF— y permite afinar el tamaño de página, DPI y color de fondo mediante opciones de rasterización integradas. La misma API también gestiona exportaciones a PDF, PNG y SVG, eliminando la necesidad de múltiples bibliotecas.

### Ventajas clave
- **Sin dependencias externas** – puro Java, funciona en cualquier SO que ejecute Java.  
- **Renderizado de alta fidelidad** – conserva grosor de línea, color y detalles de trama.  
- **Rasterización incorporada** – controla dimensiones de página, resolución y fondo.  
- **Conversión todo en uno** – las mismas clases exportan a WMF, PDF, PNG, SVG, etc.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Aspose.CAD para Java** integrado en tu proyecto. Descárgalo desde el sitio oficial: [Descarga Aspose.CAD Java](https://releases.aspose.com/cad/java/).  
- **Directorio de documentos** donde se almacenan tus archivos DXF (p. ej., `Your Document Directory/DXFDrawings/`).  

## Importar espacios de nombres

Los siguientes imports traen las clases de Aspose.CAD necesarias para cargar, rasterizar y guardar archivos CAD.  
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

### ¿Cómo convierto DXF a WMF en Java?

Carga tu archivo DXF con `Image.load("yourFile.dxf")`, configura `CadRasterizationOptions` para el tamaño de página y DPI deseados, y luego llama `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Este patrón de tres pasos realiza la conversión completa manteniendo la calidad vectorial y requiere solo unas pocas líneas de código.

#### Paso 1: Cargar dibujo DXF

Image.load lee el archivo DXF en un objeto Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Paso 2: Configurar opciones de rasterización

CadRasterizationOptions especifica el tamaño de página, resolución y fondo para rasterizar el dibujo CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Paso 3: Guardar como WMF

ImageSaveOptions con SaveFormat.WMF indica a Aspose.CAD que escriba la salida como un Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Paso 4: Liberar recursos

Llamar a image.close() libera los recursos nativos usados por el objeto Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Paso 5: Opcional – Exportar a PDF

PdfOptions configura ajustes específicos de PDF al guardar la imagen como documento PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Consejo profesional:** Puedes reutilizar el mismo objeto `CadRasterizationOptions` para la exportación a PDF pasándolo a una instancia de `PdfOptions`, ahorrándote algunas líneas de configuración.

## ¿Cómo exporto DXF a PDF usando Aspose CAD Java?

Exportar a PDF sigue los mismos pasos de carga y rasterización; simplemente reemplaza el formato de guardado WMF por PDF. Usa `new ImageSaveOptions(SaveFormat.Pdf)` y, opcionalmente, establece opciones específicas de PDF como nivel de compresión o metadatos de autor. Esta conversión de una sola línea produce un PDF buscable y con precisión de página que replica el diseño CAD original.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **`NullPointerException` en `cadImage.save`** | Variable `cadImage` no definida (debería ser `image`). | Reemplaza `cadImage` por `image` o renombra la variable de forma consistente. |
| **El WMF de salida está en blanco** | El tamaño de página de rasterización es demasiado pequeño o el color de fondo está configurado como transparente. | Aumenta `PageWidth`/`PageHeight` o establece un color de fondo mediante `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Excepción de licencia** | Ejecutando sin una licencia válida de Aspose en producción. | Aplica el archivo de licencia al iniciar la aplicación: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusión

Ahora dispones de un flujo de trabajo completo y listo para producción para **convertir DXF a WMF** usando Aspose.CAD para Java, con un paso opcional para **exportar el mismo dibujo a PDF**. Este enfoque te brinda una salida vectorial de alta calidad que se integra sin problemas con herramientas de informes y documentación basadas en Windows, manteniendo tu base de código simple y sin dependencias.

## Preguntas frecuentes

### Q1: ¿Dónde puedo encontrar la documentación de Aspose.CAD?

A1: Puedes acceder a la documentación [aquí](https://reference.aspose.com/cad/java/).

### Q2: ¿Cómo descargo Aspose.CAD para Java?

A2: Descarga la biblioteca [aquí](https://releases.aspose.com/cad/java/).

### Q3: ¿Hay una prueba gratuita disponible?

A3: Sí, puedes obtener una prueba gratuita [aquí](https://releases.aspose.com/).

### Q4: ¿Necesito opciones de licencia temporales?

A4: Explora licencias temporales [aquí](https://purchase.aspose.com/temporary-license/).

### Q5: ¿Dónde puedo obtener soporte?

A5: Visita el foro de soporte de Aspose.CAD [aquí](https://forum.aspose.com/c/cad/19).

## Preguntas frecuentes

**Q: ¿Puedo convertir archivos DXF grandes (cientos de MB) sin quedarme sin memoria?**  
A: Sí. Carga el archivo en un bloque *try‑with‑resources* y libera el objeto `Image` rápidamente. Ajusta `CadRasterizationOptions.setPageWidth/Height` a un tamaño razonable para mantener bajo el uso de memoria.

**Q: ¿El WMF de salida conserva la información de capas?**  
A: WMF es un formato vectorial plano, por lo que la jerarquía de capas se aplana, pero los estilos de línea, colores y patrones de trama se conservan.

**Q: ¿Es posible establecer un DPI personalizado para el WMF?**  
A: Usa `rasterizationOptions.setResolution(300);` para definir el DPI antes de guardar.

**Q: ¿Puedo convertir varios archivos DXF por lotes en una sola ejecución?**  
A: Absolutamente. Recorre un directorio, carga cada archivo y aplica la misma lógica de rasterización y guardado.

**Q: ¿Qué versiones de Java son compatibles?**  
A: Aspose.CAD para Java soporta Java 8 y posteriores, incluyendo Java 11, 17 y versiones LTS más recientes.

---

**Última actualización:** 2026-06-09  
**Probado con:** Aspose.CAD para Java 24.11  
**Autor:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Tutoriales relacionados

- [Crear PDF desde CAD – Exportar DXF a PDF con Aspose.CAD para Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Crear PDF desde DXF: Exportar capa con Aspose.CAD para Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Cómo convertir el diseño DXF a imagen JPEG con Aspose.CAD en Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}