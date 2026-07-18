---
date: 2026-07-18
description: Cómo exportar CAD a PNG usando Aspose.CAD para .NET. Convierta archivos
  IFC a imágenes PNG de alta calidad de forma rápida y fiable.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Exportación de archivos IFC a PNG
og_description: Cómo exportar CAD a PNG usando Aspose.CAD para .NET. Aprenda la conversión
  paso a paso de archivos IFC en imágenes PNG con una configuración sin código.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Cómo exportar CAD a PNG – Guía Aspose.CAD .NET
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Cómo exportar CAD a PNG – Exportación de archivos IFC con Aspose.CAD
url: /es/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo exportar CAD a PNG – Exportando archivos IFC con Aspose.CAD

## Introducción

Si necesita **cómo exportar CAD a PNG**, Aspose.CAD para .NET ofrece una forma fiable y sin código de convertir modelos IFC (Industry Foundation Classes) en imágenes raster PNG nítidas. En este tutorial recorreremos todo el flujo de trabajo —desde la instalación de la biblioteca hasta guardar el PNG final— para que pueda integrar la conversión en cualquier aplicación .NET con confianza.

## Respuestas rápidas
- **¿Qué biblioteca maneja la conversión?** Aspose.CAD for .NET.
- **¿Formato de origen compatible?** IFC (Industry Foundation Classes) files.
- **¿Formato de imagen de destino?** PNG, con control total sobre el tamaño y la resolución.
- **¿Versión mínima de .NET?** .NET Framework 4.5+ o .NET Core 3.1+.
- **¿Requisito de licencia?** Una licencia válida de Aspose.CAD para uso en producción.

## Qué es “cómo exportar CAD a PNG”?

La frase se refiere al proceso de convertir formatos de archivo basados en CAD, como IFC, a imágenes raster Portable Network Graphics (PNG). Esta conversión permite una visualización, compartición e inserción fáciles de los visuales CAD en páginas web, documentación o informes, proporcionando un formato ligero y ampliamente compatible que preserva la fidelidad visual sin requerir visores CAD especializados.

## ¿Por qué usar Aspose.CAD para esta conversión?

Aspose.CAD admite **más de 50 formatos CAD y BIM** y puede procesar modelos IFC de cientos de páginas sin cargar todo el archivo en memoria. Ofrece conversiones rápidas y eficientes en memoria en hardware de servidor estándar, manejando automáticamente capas, grosores de línea y mapeo de colores, al tiempo que brinda amplias opciones de configuración para la calidad y el tamaño de salida.

## Requisitos previos

### 1. Instalación de Aspose.CAD
Asegúrese de que tiene Aspose.CAD para .NET instalado. Puede descargarlo desde la página de lanzamientos [aquí](https://releases.aspose.com/cad/net/).

### 2. Directorio de documentos
Cree un directorio designado para sus documentos. En el ejemplo proporcionado, la variable `MyDir` representa el directorio de documentos.

## Importar espacios de nombres
Ahora que los requisitos están listos, importe los espacios de nombres necesarios para trabajar con Aspose.CAD en su proyecto .NET.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## ¿Cómo exportar CAD a PNG?

`IfcImage` representa una imagen CAD IFC que puede rasterizarse en formatos raster como PNG. Cargue su archivo IFC con `new IfcImage("source.ifc")`, configure la rasterización mediante `RasterizationOptions`, establezca los ajustes específicos de PNG con `PngOptions` y, finalmente, llame a `Save(outputPath, pngOptions)`. Este flujo de extremo a extremo convierte el modelo CAD en un PNG de alta resolución en solo unas pocas líneas de código, manejando automáticamente capas, colores y grosores de línea.

## Paso 1: Cargar archivo IFC
La clase `IfcImage` carga un modelo IFC y lo prepara para la rasterización.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

En este paso inicializamos el objeto `IfcImage` de Aspose.CAD y cargamos el archivo IFC en él.

## Paso 2: Establecer opciones de rasterización
La clase `RasterizationOptions` define cómo los datos vectoriales se convierten en imágenes raster, incluyendo el ancho, la altura y el color de fondo de la página.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Defina las opciones de rasterización para configurar el ancho y la altura de la página para la salida PNG.

## Paso 3: Establecer opciones PNG
La clase `PngOptions` contiene configuraciones específicas para la salida PNG, como el nivel de compresión y la profundidad de color.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Cree opciones PNG y asocie las opciones de rasterización definidas previamente.

## Paso 4: Especificar ruta de salida
La ruta de salida determina dónde se guardará el archivo PNG generado.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Defina la ruta de salida para el archivo PNG, asegurándose de que tenga el mismo nombre que el archivo de origen con la extensión ".png". Finalmente, guarde la imagen convertida.

## Problemas comunes y soluciones
- **Fuentes o estilos de línea faltantes:** Asegúrese de que el IFC de origen haga referencia a todos los recursos necesarios; Aspose.CAD incrusta los recursos faltantes cuando es posible.
- **Los archivos grandes provocan picos de memoria:** Use la propiedad `MemoryLimit` en `RasterizationOptions` para limitar el uso de memoria.
- **Colores incorrectos:** Verifique que las definiciones de color del IFC de origen cumplan con el esquema IFC; Aspose.CAD respeta el mapeo de colores estándar.

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.CAD para .NET en macOS o Linux?**  
R: No, Aspose.CAD para .NET está específicamente diseñado para entornos Windows.

**P: ¿Está disponible una licencia temporal para propósitos de prueba?**  
R: Sí, puede obtener una licencia temporal desde [aquí](https://purchase.aspose.com/temporary-license/) para evaluación.

**P: ¿Cómo puedo obtener soporte para Aspose.CAD?**  
R: Visite el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte comunitario y discusiones.

**P: ¿Dónde puedo encontrar documentación completa?**  
R: Consulte la [documentación de Aspose.CAD](https://reference.aspose.com/cad/net/) para información detallada y ejemplos.

**P: ¿Qué hago si encuentro problemas durante la instalación?**  
R: Revise la documentación o solicite ayuda en el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Última actualización:** 2026-07-18  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Convertir dibujo CAD a imagen raster en Aspose.CAD para .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Conversión de STL a PNG fácil con Aspose.CAD para .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Exportar diseños CAD a formatos de imagen raster en Aspose.CAD para .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}