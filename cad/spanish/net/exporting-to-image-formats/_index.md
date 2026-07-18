---
date: 2026-07-18
description: La conversión de Aspose CAD le permite exportar fácilmente IFC a PNG
  e IGES a PDF. Aprenda paso a paso cómo convertir archivos CAD con Aspose.CAD for
  .NET en minutos.
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: Exportación a formatos de imagen
og_description: La conversión de Aspose CAD permite una exportación rápida de IFC
  a PNG e IGES a PDF. Siga esta guía para un manejo sin problemas de archivos CAD
  con Aspose.CAD for .NET.
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: 'Conversión de Aspose CAD: Exportación a formatos de imagen'
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: 'Conversión de Aspose CAD: Exportación a formatos de imagen'
url: /es/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversión de Aspose CAD: Exportación a formatos de imagen

En los flujos de trabajo modernos de ingeniería y diseño, **aspose cad conversion** es esencial para convertir archivos CAD y BIM complejos en formatos de imagen visualizables universalmente. Ya sea que necesite compartir una vista previa rápida de un modelo IFC o generar un PDF imprimible a partir de un dibujo IGES, este tutorial le guía paso a paso usando Aspose.CAD para .NET. Verá cómo mantener la geometría, los colores y las capas intactas al exportar a PNG, PDF y otros formatos raster.

## Respuestas rápidas
- **¿Qué formatos puede exportar Aspose.CAD?** Más de 30 formatos CAD/BIM a más de 20 tipos de imagen, incluidos PNG, JPEG, PDF y TIFF.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita sirve para evaluación; se requiere una licencia comercial para producción.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **¿Se pueden procesar archivos grandes?** Sí – Aspose.CAD maneja archivos de hasta 2 GB sin cargar todo el documento en memoria.  
- **¿Se requiere software adicional?** No se necesitan herramientas CAD externas; la biblioteca realiza todas las conversiones internamente.

## ¿Qué es la Conversión de Aspose CAD?
La clase `Image` representa un documento CAD cargado en memoria y proporciona métodos para guardarlo en varios formatos. La Conversión de Aspose CAD transforma archivos CAD/BIM a otros formatos usando Aspose.CAD para .NET. Cargue la fuente con `Image`, elija el formato de destino y llame a `Save`. Este patrón de dos pasos preserva capas, grosores de línea y texturas, coincidiendo con la intención de diseño original.

## ¿Cómo exportar archivos IFC a PNG?
La clase `Image` representa un documento CAD cargado en memoria y proporciona métodos para guardarlo en varios formatos. Cargue el archivo IFC con `new Image("model.ifc")` y llame a `image.Save("model.png", ImageFormat.Png)`. Aspose.CAD lee la geometría 3‑D, la aplana a una imagen raster y escribe un PNG de alta resolución que conserva la profundidad de color y la transparencia. Para procesamiento por lotes, recorra una carpeta y guarde cada archivo.

## ¿Cómo exportar archivos IGES a PDF?
La clase `Image` representa un documento CAD cargado en memoria y proporciona métodos para guardarlo en varios formatos. Cree una instancia `Image` a partir del archivo IGES y llame a `image.Save("drawing.pdf", ImageFormat.Pdf)`. La conversión preserva la información vectorial, los estilos de línea y las anotaciones, produciendo un PDF que puede abrirse en cualquier visor sin pérdida de detalle. Use la propiedad opcional `Resolution` para aumentar DPI en PDFs listos para impresión.

## ¿Por qué usar Aspose.CAD para .NET?
Aspose.CAD admite **más de 30 formatos de entrada** (incluidos IFC, IGES, DWG, DWF y STL) y puede generar **más de 20 tipos de imagen**. Procesa dibujos de cientos de páginas en menos de 5 segundos en un servidor típico, y funciona completamente sin conexión—no se necesita instalaciones CAD nativas. Estos beneficios cuantificados lo convierten en una opción rentable y de alto rendimiento tanto para empresas como para desarrolladores independientes.

## Errores comunes y consejos profesionales
La clase `LoadOptions` le permite personalizar cómo se carga un archivo CAD, como establecer límites de memoria o especificar capas.  
El objeto `FontSettings` define reglas de sustitución e incrustación de fuentes usadas durante la conversión.  

- **Error:** Ignorar el DPI predeterminado puede producir imágenes de baja resolución.  
  **Consejo:** Establezca `image.DpiX` y `image.DpiY` a 300 para PNG de calidad de impresión.  
- **Error:** Los archivos IGES grandes pueden superar los límites de memoria.  
  **Consejo:** Use `LoadOptions` con `MemoryLimit` para transmitir el archivo en fragmentos.  
- **Error:** Falta de fuentes en modelos IFC genera texto de marcador de posición.  
  **Consejo:** Incruste las fuentes requeridas usando el objeto `FontSettings` antes de la conversión.

## Tutoriales de exportación a formatos de imagen
### [Exportando archivos IFC a PNG - Tutorial Aspose.CAD](./exporting-ifc-files-to-png/)
Explore Aspose.CAD para .NET, una solución robusta para la conversión fluida de IFC a PNG. Descargue ahora para un procesamiento eficiente de archivos CAD.
### [Exportando archivos IGES a PDF - Guía Aspose.CAD](./exporting-iges-files-to-pdf/)
Aprenda cómo exportar fácilmente archivos IGES a PDF usando Aspose.CAD para .NET. Siga nuestra guía paso a paso para una manipulación precisa de archivos CAD.

## Preguntas frecuentes

**P: ¿Puedo convertir varios archivos CAD en un solo lote?**  
R: Sí, itere sobre una carpeta con `foreach (var file in Directory.GetFiles(path, "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"), ImageFormat.Png); }`.  
El método `Directory.GetFiles` devuelve los nombres de los archivos (incluyendo sus rutas) que coinciden con un patrón especificado en un directorio.

**P: ¿Aspose.CAD preserva la información de capas en la imagen exportada?**  
R: La visibilidad de capas se respeta; puede alternar capas mediante `LoadOptions` antes de guardar, asegurando que solo las capas seleccionadas aparezcan en la salida.

**P: ¿Cuál es el tamaño máximo de archivo que Aspose.CAD puede manejar?**  
R: La biblioteca procesa cómodamente archivos de hasta **2 GB**; los archivos más grandes deben dividirse o transmitirse usando `LoadOptions.MemoryLimit`.

**P: ¿Hay soporte para convertir CAD a PDFs basados en vectores?**  
R: Sí—al guardar como `ImageFormat.Pdf` la salida conserva datos vectoriales, permitiendo escalado infinito sin pérdida de calidad.

**P: ¿Necesito una licencia separada para cada plataforma .NET?**  
R: Una única licencia de Aspose.CAD cubre todos los runtimes .NET compatibles (Framework, Core y .NET 5+).

---

**Última actualización:** 2026-07-18  
**Probado con:** Aspose.CAD 24.12 para .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Exportando archivos IFC a PNG - Tutorial Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-ifc-files-to-png/)
- [Exportando archivos IGES a PDF - Guía Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Exportar diseños CAD a formatos de imagen raster en Aspose.CAD para .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}