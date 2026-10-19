---
date: 2026-10-19
description: Aprenda cómo convertir DWG a PDF en Java con Aspose.CAD. Esta guía paso
  a paso le muestra cómo exportar PDF de AutoCAD, guardar CAD como PDF y aplicar una
  licencia.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Exportar imágenes de AutoCAD a PDF
og_description: Aprenda cómo convertir DWG a PDF en Java con Aspose.CAD. Esta guía
  le lleva a través de la exportación de PDF de AutoCAD, el guardado de CAD como PDF
  y la gestión de licencias.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Convertir DWG a PDF en Java usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Convertir DWG a PDF en Java usando Aspose.CAD
url: /es/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PDF de AutoCAD – exportar imágenes de AutoCAD a PDF con Aspose.CAD para Java

## Introducción

## Respuestas rápidas
- **¿Puedo convertir DWG a PDF con Java?** Sí – Aspose.CAD for Java admite nativamente DWG, DXF y docenas de otros formatos CAD.  
- **¿Necesito una licencia?** Una **licencia Aspose CAD** permanente elimina todas las restricciones de evaluación; una licencia temporal está disponible para pruebas.  
- **¿Qué versiones de Java son compatibles?** Java 8 y superiores son totalmente compatibles.  
- **¿Puedo controlar las dimensiones de la página PDF?** Absolutamente – establezca `pageWidth` y `pageHeight` en las opciones de rasterización.  
- **¿Es posible el renderizado 3‑D?** Sí – habilite `TypeOfEntities.Entities3D` para rasterizar entidades 3‑D.

## ¿Qué es exportar PDF de AutoCAD?
Exportar PDF de AutoCAD es el proceso de convertir dibujos CAD vectoriales en un documento PDF portátil. Conserva capas, grosores de línea, colores y, opcionalmente, geometría 3‑D, facilitando compartir diseños con clientes o archivarlos sin necesidad de software CAD.

## ¿Por qué convertir DWG a PDF con Aspose.CAD para Java?
Aspose.CAD admite **más de 50 formatos de entrada y salida**, procesa dibujos de cientos de páginas sin cargar todo el archivo en memoria y se ejecuta en cualquier plataforma que soporte Java 8+. La biblioteca le brinda control total sobre DPI, tamaño de página y diseño, de modo que puede **personalizar el tamaño de página PDF** para que coincida con las especificaciones exactas del proyecto, todo sin instalar DLLs nativas.

## Requisitos previos

- **Java Development Kit** – JDK 8 o posterior instalado en su estación de trabajo.  
- **Aspose.CAD for Java** – descargue el último JAR desde el [download link](https://releases.aspose.com/cad/java/).  
- **Directorio de trabajo** – una carpeta donde se almacenarán sus archivos DWG de origen y los PDFs generados.

## Importar espacios de nombres

La clase `Image` representa cualquier dibujo CAD rasterizable, mientras que `RasterizationOptions` y `PdfOptions` le permiten afinar la conversión.

La clase `Image` es el objeto de nivel superior de Aspose.CAD que mantiene un dibujo CAD en memoria.  
La clase `RasterizationOptions` define cómo se rasteriza los datos vectoriales antes de escribirlos en PDF.  
La clase `PdfOptions` agrupa la configuración de rasterización con los parámetros de salida específicos de PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Ahora repasemos el código paso a paso.

## ¿Cómo convertir DWG a PDF con Aspose.CAD para Java?

Para convertir un archivo DWG a PDF con Aspose.CAD para Java, cargue el dibujo usando la clase Image, configure CadRasterizationOptions (como DPI, tamaño de página y tipos de entidad), envuelva esas opciones en PdfOptions y luego llame al método save especificando un nombre de archivo .pdf. Esta secuencia garantiza que los datos vectoriales se rastericen correctamente y que el PDF resultante coincida con los requisitos de su diseño.

### Paso 1: establecer la ruta del directorio de recursos

Reemplace `"Your Document Directory"` con la ruta absoluta a la carpeta que creó en los requisitos previos.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Consejo profesional:** Use `Paths.get(...).toAbsolutePath()` para evitar errores relacionados con rutas en diferentes sistemas operativos.

### Paso 2: cargar la imagen CAD

Cargar el archivo CAD en un objeto `Image` le brinda acceso completo al motor de rasterización de Aspose.CAD.

La clase `Image` carga el archivo DWG y lo prepara para la conversión.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Por qué es importante:** Una vez que el dibujo está en memoria, puede consultar sus diseños, capas y metadatos antes de rasterizar.

### Paso 3: establecer opciones de rasterización

Ajuste `pageWidth` y `pageHeight` para **personalizar el tamaño de página PDF**. Habilitar `setTypeOfEntities(TypeOfEntities.Entities3D)` permite renderizado 3‑D completo cuando sea necesario.

El objeto `RasterizationOptions` controla DPI, dimensiones de página y tipos de entidad para la salida.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` se miden en puntos (1 pt = 1/72 in).  
- Descomente la línea `setTypeOfEntities` para rasterización 3‑D.  
- `setLayouts` selecciona qué diseño (Model, Layout1, etc.) renderizar.

### Paso 4: configurar opciones PDF

Vincule la configuración de rasterización a la salida PDF, asegurando que los datos vectoriales se transformen correctamente.

La clase `PdfOptions` enlaza la configuración de rasterización con el archivo PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Paso 5: guardar el PDF

El archivo resultante, `Export3DImagestoPDF_out_.pdf`, es una representación **guardar CAD como PDF** de su dibujo AutoCAD original.

El método `save` escribe la imagen rasterizada en un archivo PDF en el disco.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Problemas comunes y soluciones

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| Salida PDF en blanco | Opciones de rasterización no configuradas o desajuste de diseño | Verifique que `setLayouts` coincida con el nombre del diseño en su archivo CAD. |
| Imagen de baja resolución | `pageWidth`/`pageHeight` demasiado pequeños | Aumente las dimensiones o establezca un DPI más alto mediante `rasterizationOptions.setResolution(...)`. |
| Excepción de licencia | No se aplicó una licencia válida | Aplique una **licencia Aspose CAD** o use una licencia temporal para pruebas. |

## Preguntas frecuentes

**Q: ¿Puedo usar Aspose.CAD para Java con otros formatos de archivo CAD?**  
A: Sí – la biblioteca admite DWG, DXF, DWF, DGN y más de 30 formatos adicionales, brindándole flexibilidad en distintos proyectos.

**Q: ¿Cómo obtengo una licencia temporal para Aspose.CAD para Java?**  
A: Visite la [temporary license page](https://purchase.aspose.com/temporary-license/) para solicitar una licencia de tiempo limitado para evaluación.

**Q: ¿Hay opciones de diseño para la rasterización?**  
A: Absolutamente. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc., para elegir qué vista se renderiza en el PDF.

**Q: ¿Puedo cambiar el tamaño del archivo PDF de salida?**  
A: Sí – modifique `pageWidth` y `pageHeight` en las opciones de rasterización para que coincidan con cualquier dimensión de página requerida.

**Q: ¿Dónde puedo obtener ayuda si tengo problemas?**  
A: La comunidad dedicada está disponible en el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) donde puede hacer preguntas y compartir soluciones.

---

**Última actualización:** 2026-10-19  
**Probado con:** Aspose.CAD for Java 24.10  
**Autor:** Aspose

## Tutoriales relacionados

- [Exportar DWG a PDF en Java – Establecer tamaño de página PDF con Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportar DWG a PDF: Diseño específico usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG a PDF y habilitar seguimiento con Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}