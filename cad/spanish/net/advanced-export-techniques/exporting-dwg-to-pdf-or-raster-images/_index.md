---
date: 2026-03-16
description: Aprenda a convertir DWG a PDF o imágenes rasterizadas con Aspose.CAD
  para .NET. Este tutorial paso a paso de CAD a PDF cubre la exportación de DWG a
  formatos de imagen como PNG y muestra cómo exportar archivos DWG a imágenes de manera
  eficiente.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cómo convertir DWG a PDF e imágenes rasterizadas usando Aspose.CAD para .NET
url: /es/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

Last Updated", "Tested With", "Author". Keep dates.

Also translate "Exporting DWG to PDF or Raster Images - Aspose.CAD Guide" title.

Let's produce.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG a PDF o Imágenes Raster - Guía de Aspose.CAD

## Introducción

Si necesitas **convertir DWG a PDF** (o a formatos raster como PNG) directamente desde una aplicación .NET, estás en el lugar correcto. En este tutorial recorreremos paso a paso los pasos exactos necesarios para usar Aspose.CAD para .NET y realizar la conversión, explicaremos por qué la biblioteca es una opción sólida y te mostraremos cómo manejar tanto la salida PDF como la de imagen con solo unas pocas líneas de código.

## Respuestas rápidas
- **¿Qué biblioteca maneja la conversión de DWG?** Aspose.CAD para .NET  
- **¿Puedo exportar DWG a PNG además de PDF?** Sí – las mismas opciones de rasterización funcionan para ambos formatos.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **¿Se maneja la conversión de unidades automáticamente?** Puedes definir el sistema de unidades manualmente (métrico o imperial) como se muestra en el código.

## ¿Qué significa “convertir DWG a PDF”?
Convertir DWG a PDF implica tomar un dibujo CAD (DWG) y renderizarlo en un documento portátil de solo lectura (PDF). Esto es útil para compartir diseños con partes interesadas que no disponen de software CAD, crear documentación imprimible o archivar dibujos en un formato universalmente legible.

## ¿Por qué usar Aspose.CAD para esta conversión?
- **Sin dependencias externas** – la biblioteca funciona completamente en código administrado.  
- **Alta fidelidad** – conserva capas, grosores de línea e información de diseño.  
- **Opciones de rasterización integradas** – permite exportar a PNG, JPEG, BMP, etc., con un único objeto de configuración.  
- **Multiplataforma** – funciona en Windows, Linux y macOS con .NET Core.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrate de contar con lo siguiente:

- Un conocimiento básico de programación en .NET.  
- Biblioteca Aspose.CAD para .NET instalada. Si no la tienes, descárgala [aquí](https://releases.aspose.com/cad/net/).  
- Tu entorno de desarrollo integrado (IDE) favorito configurado para desarrollo .NET.

## Importar espacios de nombres

Comencemos importando los espacios de nombres necesarios en tu proyecto .NET. Esto garantiza que tengas acceso a la funcionalidad de Aspose.CAD en tu código.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Paso 1: Cargar el archivo DWG

Comienza cargando el archivo DWG que deseas convertir. Reemplaza `"Your Document Directory"` con la ruta a tu archivo DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Paso 2: Configurar la exportación a PDF (Cómo exportar DWG a PDF)

Ahora, configuremos las opciones de exportación a PDF. Este ejemplo muestra cómo establecer el diseño y manejar la conversión de unidades.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Paso 3: Exportar a PDF

Ejecuta la exportación a PDF utilizando la configuración definida.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Paso 4: Exportar a Imágenes Raster (exportar dwg a imagen)

Amplía la funcionalidad para exportar a imágenes raster, como PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Cómo solucionarlo |
|----------|----------------|-------------------|
| **Páginas en blanco en el PDF** | El diseño no se especificó correctamente | Asegúrate de que `rasterizationOptions.Layouts` incluya el nombre de diseño correcto (p. ej., `"Model"`). |
| **Dimensiones incorrectas** | Desajuste de DPI o tamaño de página | Ajusta los valores `PageHeight`, `PageWidth` y DPI en `CadRasterizationOptions`. |
| **Las unidades aparecen incorrectas** | No se definió la conversión de unidades | Usa `DefineUnitSystem` para establecer `currentUnitIsMetric` y `currentUnitCoefficient` según `cadImage.UnitType`. |
| **Excepción de licencia** | Limitaciones de la versión de prueba | Aplica una licencia temporal o permanente antes de llamar a `Image.Load`. |

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD para .NET en mis proyectos comerciales?
A1: Sí, puedes. Visita [purchase.aspose.com/buy](https://purchase.aspose.com/buy) para obtener detalles de licenciamiento.

### Q2: ¿Hay una prueba gratuita disponible?
A2: ¡Claro! Obtén tu prueba gratuita [aquí](https://releases.aspose.com/).

### Q3: ¿Cómo puedo obtener soporte para Aspose.CAD para .NET?
A3: Dirígete al [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte de la comunidad.

### Q4: ¿Puedo obtener una licencia temporal para propósitos de prueba?
A4: Sí, puedes obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q5: ¿Dónde puedo encontrar la documentación detallada?
A5: La documentación está disponible en [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: ¿Cómo **guardar CAD como PNG** con alta calidad?
A6: Establece `PageHeight` y `PageWidth` a las dimensiones de píxel deseadas y elige un DPI de 300 o superior en `CadRasterizationOptions`.

### Q7: ¿Cuál es la mejor manera de **convertir dwg** cuando el archivo fuente contiene varios diseños?
A7: Rellena `rasterizationOptions.Layouts` con todos los nombres de diseño que deseas exportar, luego recorre cada diseño y llama a `Save` para cada formato de salida.

---

**Última actualización:** 2026-03-16  
**Probado con:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}