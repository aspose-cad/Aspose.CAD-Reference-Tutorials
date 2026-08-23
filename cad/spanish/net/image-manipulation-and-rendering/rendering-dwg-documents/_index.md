---
date: 2026-08-23
description: Aprenda cómo crear un viewport dwg c# usando Aspose.CAD. Esta guía cubre
  la carga de un archivo DWG, la configuración de la rasterización, la definición
  de un viewport y el guardado del resultado como PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Renderizado de documentos DWG en C#
og_description: Aprenda cómo crear un viewport dwg c# usando Aspose.CAD en .NET. Esta
  guía paso a paso muestra la carga, la rasterización, la definición de viewports
  y el guardado en PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Cómo crear un viewport dwg c# con Aspose.CAD para .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Cómo crear un viewport dwg c# con Aspose.CAD para .NET
url: /es/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderizando documentos DWG en C# – tutorial de crear viewport dwg c# tutorial

## Introducción

En este tutorial integral aprenderá a **create viewport dwg c#** con Aspose.CAD y a renderizar un archivo DWG a PDF. Ya sea que necesite extraer un layout específico, generar una hoja imprimible o incrustar una vista CAD en un informe, controlar el viewport le brinda un control preciso del renderizado. Aspose.CAD admite **más de 20 formatos CAD** y puede procesar archivos con miles de entidades sin cargar todo el documento en memoria, lo que lo hace ideal para aplicaciones .NET de alto rendimiento.

## Respuestas rápidas
- **¿Cuál es el primer paso?** Cargue el archivo DWG con `CadImage.Load`.
- **¿Qué clase define el área de vista?** `Viewport` dentro de `CadRasterizationOptions`.
- **¿Puedo exportar a PDF?** Sí, usando `PdfOptions` después de la rasterización.
- **¿Necesito una licencia para producción?** Se requiere una licencia comercial; una prueba gratuita funciona para evaluación.
- **¿Se admite .NET Core?** Absolutamente – Aspose.CAD funciona con .NET Framework, .NET Core y .NET 5/6.

## Requisitos previos

Antes de sumergirse en el código, asegúrese de contar con:

- Conocimientos básicos de programación en C#.
- Visual Studio (cualquier edición reciente) instalado.
- Biblioteca Aspose.CAD añadida a su proyecto. Puede descargarla desde [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- Un archivo DWG de ejemplo, como **Bottom_plate.dwg**, para seguir el tutorial.

## Importar espacios de nombres

Agregue las directivas `using` requeridas al inicio de su archivo C# para que el compilador pueda localizar los tipos de Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Ahora que el entorno está listo, recorramos la implementación paso a paso.

## ¿Cómo crear viewport dwg c#?

Para crear un viewport personalizado, primero cargue el archivo DWG en un objeto `CadImage`, luego configure `CadRasterizationOptions` con el layout y la escala deseados. Defina la región que desea mostrar, instancie un `CadVportTableObject` con el centro, altura y relación de aspecto calculados, reemplace el viewport activo, establezca las opciones de PDF y, finalmente, guarde el resultado.

## Paso 1: cargar el archivo dwg

`CadImage.Load` carga un archivo DWG en un objeto `CadImage`, que representa el dibujo CAD en memoria.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Paso 2: configurar opciones de rasterización

`CadRasterizationOptions` especifica cómo se rasteriza el dibujo CAD, incluida la selección de layout, escala y tamaño de salida.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Paso 3: definir la región a dibujar

`Point` define las coordenadas X e Y de la esquina superior izquierda de la región a renderizar.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Paso 4: crear un nuevo viewport

`CadVportTableObject` representa un objeto viewport que controla el área visible y la relación de aspecto del dibujo renderizado.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Paso 5: reemplazar el viewport activo

El bucle reemplaza el viewport activo con el recién creado para aplicar la configuración de vista personalizada.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Paso 6: configurar opciones de PDF

`PdfOptions` configura los parámetros de salida PDF, como compresión y metadatos.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 7: guardar el dwg renderizado como PDF

`image.Save` escribe la imagen renderizada en un archivo usando las opciones de formato especificadas.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## ¿Por qué usar un viewport personalizado al renderizar DWG?

Un viewport personalizado le permite aislar un layout o región específica, reduciendo el tamaño del archivo y mejorando la velocidad de renderizado. Aspose.CAD puede renderizar un DWG de 300 páginas en menos de 2 segundos cuando se utiliza un viewport enfocado, comparado con el renderizado completo del dibujo que puede tardar varios segundos más.

## Problemas comunes y soluciones

- **Salida en blanco** – Asegúrese de que las coordenadas del viewport estén dentro de los límites del dibujo; use `CadImage.Size` para verificar los bordes.
- **Capas faltantes** – Establezca `CadRasterizationOptions.Layouts` al nombre de layout correcto; de lo contrario, el layout predeterminado puede estar vacío.
- **Ralentización del rendimiento** – Desactive el anti‑aliasing en `CadRasterizationOptions` si solo necesita una vista previa rápida.

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD con otros formatos de archivo CAD?

A1: Sí, Aspose.CAD admite varios formatos, incluidos DWG, DXF, DWF y más de 20 tipos adicionales de CAD.

### Q2: ¿Aspose.CAD es compatible con .NET Core?

A2: Sí, Aspose.CAD funciona con .NET Framework, .NET Core y las últimas versiones de .NET.

### Q3: ¿Cómo puedo manejar diferentes layouts en un archivo DWG?

A3: Especifique el layout deseado usando la propiedad `Layouts` de `CadRasterizationOptions` antes de renderizar.

### Q4: ¿Hay consideraciones de licencia para usar Aspose.CAD?

A4: Para detalles de licenciamiento, visite [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: ¿Dónde puedo encontrar soporte adicional?

A5: Visite el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para obtener ayuda de la comunidad y discusiones.

### Q6: ¿Puedo renderizar directamente a PNG en lugar de PDF?

A6: Sí, cambie `PdfOptions` a `PngOptions` y llame a `image.Save("output.png", pngOptions)`.

### Q7: ¿Cómo incrusto la imagen renderizada en una aplicación Windows Forms?

A7: Cargue la imagen guardada en un control `PictureBox` usando `Image.FromFile("output.png")`.

## Conclusión

Ahora sabe cómo **create viewport dwg c#** y renderizar un archivo DWG a PDF (u otros formatos raster) usando Aspose.CAD. Al dominar la manipulación del viewport obtiene un control fino sobre la salida visual, esencial para generar dibujos de ingeniería precisos, informes o miniaturas. Explore configuraciones adicionales de rasterización, experimente con diferentes formatos de salida e integre el código en servicios .NET más grandes o utilidades de escritorio.

---

**Última actualización:** 2026-08-23  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo establecer el viewport al convertir DWG a PDF con coordenadas en C# - Tutorial de Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Aprenda a establecer opciones de rasterización CAD – Exportar layouts específicos a PDF con Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Cómo convertir DWG a PDF e imágenes rasterizadas usando Aspose.CAD para .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}