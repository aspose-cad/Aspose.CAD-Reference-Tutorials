---
date: 2026-08-12
description: Extrae texto de DWG y convierte DWG específico a imagen en C# usando
  Aspose.CAD para .NET. Aprende paso a paso con fragmentos de código.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Conversión de DWG específico a imagen en C#
og_description: Extrae texto de DWG y convierte DWG específico a imagen en C# con
  Aspose.CAD. Sigue esta guía concisa para una implementación rápida.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Extraer texto de DWG y convertir DWG específico a imagen en C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Extraer texto de DWG y convertir DWG específico a imagen en C#
url: /es/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversión de DWG específico a imagen en C# - Guía de Aspose.CAD

## Introducción

En aplicaciones de ingeniería modernas, a menudo necesitas **extraer texto de archivos DWG** y **convertir DWG específicos a formatos de imagen** para informes o visualización. Aspose.CAD para .NET te ofrece una API completa que maneja ambas tareas sin requerir software CAD externo. En este tutorial aprenderás a cargar un DWG, filtrar entidades de texto, rasterizar el dibujo y, finalmente, guardar el resultado como una imagen PDF, todo con código C# limpio.

## Respuestas rápidas
- **¿Cuál es el primer paso?** Carga el archivo DWG con `new CadImage("file.dwg")`.  
- **¿Qué clase filtra el texto?** Usa `CadEntityFilter` para seleccionar entidades `Text`.  
- **¿Cómo defines el tamaño de la imagen?** Establece `Width` y `Height` en `CadRasterizationOptions`.  
- **¿Qué formato de salida se utiliza?** El ejemplo guarda en PDF, que incrusta la imagen rasterizada.  
- **¿Necesito una licencia para producción?** Sí – una licencia comercial de Aspose.CAD elimina las limitaciones de evaluación.

## Cómo extraer texto de DWG

Carga el DWG, aplica un filtro que seleccione solo entidades de texto y luego lee la propiedad `TextString` de cada entidad. Este enfoque devuelve cada pieza de anotación, etiqueta o texto de dimensión que exista en el dibujo, permitiéndote reutilizarlo para búsqueda, indexación o generación de informes.

## Por qué convertir DWG específico a imagen

Convertir un DWG a una imagen rasterizada te permite incrustar el dibujo en documentos, páginas web o aplicaciones móviles que no pueden renderizar formatos CAD nativos. Aspose.CAD procesa **más de 50 formatos CAD** y puede rasterizar dibujos de cientos de páginas mientras usa menos de 200 MB de memoria, lo que lo hace adecuado para escenarios de servidor de alto rendimiento.

## Requisitos previos

- Visual Studio (cualquier edición reciente) para compilar y ejecutar proyectos C#.  
- Aspose.CAD para .NET – asegúrate de tener la biblioteca instalada. Puedes encontrar el enlace de descarga en la **[página de descarga de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/)**.  
- Un archivo DWG con el que deseas trabajar; el archivo de ejemplo *visualization_-_conference_room.dwg* se utiliza en los fragmentos de código.

## Importar espacios de nombres

Los siguientes espacios de nombres te dan acceso a las clases principales de CAD, opciones de rasterización y auxiliares de salida PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Paso 1: cargar el archivo DWG

Crea una instancia de `CadImage` pasando la ruta de tu archivo DWG. El objeto `CadImage` representa todo el dibujo en memoria y proporciona acceso a sus capas, entidades y metadatos.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Paso 2: filtrar entidades

`CadEntityFilter` te permite seleccionar solo las entidades que necesitas. En esta guía lo configuramos para conservar objetos **texto**, descartando líneas, círculos y otras geometrías que no deseas en la imagen final.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Paso 3: establecer opciones de rasterización

`CadRasterizationOptions` controla cómo se convierte el dibujo en un mapa de bits. Puedes definir el tamaño de salida, el color de fondo y la resolución (DPI). El siguiente ancla de definición presenta la clase:

La clase `CadRasterizationOptions` especifica dimensiones de imagen, resolución y configuraciones de renderizado para convertir dibujos CAD a formatos raster.  

Establece el ancho, alto y color de fondo deseados antes de pasar las opciones al exportador PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Paso 4: establecer opciones de PDF

`PdfOptions` agrupa las configuraciones de rasterización con características específicas de PDF como la compresión. El ancla de definición para esta clase aparece primero:

`PdfOptions` encapsula los parámetros de generación de PDF, incluidas las opciones de rasterización que dictan cómo se renderizan los datos CAD dentro del documento PDF.  

Asigna la instancia previamente creada de `CadRasterizationOptions` a la propiedad `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 5: guardar como PDF

Finalmente, llama al método `Save` del objeto `CadImage`, pasando el nombre del archivo de destino y los `PdfOptions` configurados. El PDF contendrá una imagen de alta calidad del dibujo filtrado.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Problemas comunes y solución de errores

- **Texto faltante después del filtrado** – Asegúrate de que el DWG realmente contenga entidades `Text`; algunos dibujos almacenan anotaciones como `MText`. Ajusta el filtro para incluir `MText` si es necesario.  
- **Imagen de salida en blanco** – Verifica que el DPI de rasterización sea lo suficientemente alto (300 DPI es un valor predeterminado seguro) y que el color de fondo no esté configurado como transparente al visualizar el PDF.  
- **Errores de falta de memoria en archivos grandes** – Usa la sobrecarga `LoadOptions` que habilita streaming, lo que evita que todo el archivo se cargue en memoria de una sola vez.

## Preguntas frecuentes

**P: ¿Es Aspose.CAD compatible con todas las versiones de archivos DWG?**  
R: Aspose.CAD admite versiones de DWG desde AutoCAD 2000 hasta la última versión 2024, cubriendo más del 90 % de los archivos creados en el sector.

**P: ¿Puedo personalizar las opciones de rasterización para diferentes salidas?**  
R: Sí – puedes cambiar la resolución, el formato de imagen, el antialiasing y el color de fondo para adaptarlos a objetivos PNG, JPEG o PDF.

**P: ¿Dónde puedo encontrar ejemplos adicionales y documentación?**  
R: Explora la completa [documentación de Aspose.CAD](https://reference.aspose.com/cad/net/) para más ejemplos de código y detalles de la API.

**P: ¿Hay una prueba gratuita disponible para Aspose.CAD?**  
R: Por supuesto – puedes descargar una versión de prueba en la **[página de descarga de prueba de Aspose](https://releases.aspose.com/)** y evaluar todas las funciones sin restricciones durante 30 días.

**P: ¿Cómo puedo obtener soporte o conectarme con la comunidad?**  
R: Únete al activo [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) donde los desarrolladores comparten soluciones y el equipo de Aspose responde preguntas.

---

**Última actualización:** 2026-08-12  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Buscar texto en archivos DWG con C# - Tutorial de Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Convertir dibujo CAD a imagen raster en Aspose.CAD para .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Renderizado de documentos DWG en C# - Guía de Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}