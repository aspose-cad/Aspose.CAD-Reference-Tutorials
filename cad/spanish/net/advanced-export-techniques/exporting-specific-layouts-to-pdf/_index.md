---
date: 2026-03-13
description: Aprenda cómo configurar las opciones de rasterización CAD y exportar
  diseños DWG específicos a PDF usando Aspose.CAD para .NET – la guía definitiva para
  crear PDF a partir de un archivo CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Establecer opciones de rasterización CAD – Exportar diseños específicos a PDF
  - Guía de Aspose.CAD
url: /es/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportando diseños específicos a PDF - Guía de Aspose.CAD

## Introducción

En este tutorial descubrirá **cómo establecer opciones de rasterización CAD** para que pueda exportar un diseño único —o varios diseños— de un archivo DWG directamente a PDF. Aspose.CAD para .NET hace que el proceso de *dwg to pdf conversion c#* sea sencillo, dándole control total sobre el tamaño de página, la resolución y la selección de diseños. Al final de la guía podrá **crear PDF a partir de un archivo CAD** con solo unas pocas líneas de código.

## Respuestas rápidas
- **¿Qué hace “set cad rasterization options”?**  
  Indica a Aspose.CAD cómo renderizar los datos vectoriales (diseños, capas, grosores de línea) en páginas PDF rasterizadas.  
- **¿Qué método exporta un diseño DWG a PDF?**  
  Use `Image.Save` con un `PdfOptions` configurado que contenga su `CadRasterizationOptions`.  
- **¿Puedo exportar más de un diseño a la vez?**  
  Sí – proporcione una matriz de nombres de diseños en la propiedad `Layouts`.  
- **¿Necesito una licencia para uso en producción?**  
  Se requiere una licencia comercial; hay una prueba gratuita disponible para evaluación.  
- **¿Qué versiones de .NET son compatibles?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 y posteriores.

## ¿Qué es “set cad rasterization options”?

`CadRasterizationOptions` es la clase que controla cómo se rasterizan las entidades CAD al convertir a formatos basados en raster como PDF. Al configurar sus propiedades —dimensiones de página, selección de diseño, color de fondo, etc.— usted determina el resultado visual de la operación **export dwg layout to pdf**.

## ¿Por qué establecer opciones de rasterización CAD?

- **Precisión** – Preserve los grosores de línea y escalas exactamente como aparecen en el dibujo CAD original.  
- **Rendimiento** – Renderice solo los diseños que necesita, reduciendo el tamaño del archivo y el tiempo de procesamiento.  
- **Flexibilidad** – Ajuste el ancho/alto de página, DPI y fondo para que coincidan con sus estándares de informes.  

## Requisitos previos

Antes de sumergirnos en el código, asegúrese de tener:

- **Aspose.CAD for .NET** instalado. Puede descargarlo [here](https://releases.aspose.com/cad/net/).  
- Un entorno de desarrollo .NET (Visual Studio, VS Code, o cualquier IDE que prefiera).  
- Un archivo DWG que contenga al menos un diseño (el archivo de ejemplo usado aquí es `visualization_-_conference_room.dwg`).

## Importar espacios de nombres

En su proyecto .NET, importe los espacios de nombres necesarios para Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guía paso a paso

### Paso 1: Cargar el archivo DWG

Primero, apunte Aspose.CAD al archivo DWG de origen que desea convertir.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Paso 2: Establecer **CadRasterizationOptions**

Aquí configuramos los ajustes de rasterización que determinan el tamaño de página y la resolución del PDF.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Consejo profesional:** Ajuste `PageWidth` y `PageHeight` para que coincidan con las dimensiones de su diseño PDF objetivo. Valores mayores aumentan el detalle pero también el tamaño del archivo.

### Paso 3: Especificar el nombre del diseño

Indique a Aspose.CAD qué diseño(es) renderizar. Reemplace `"Layout1"` con el nombre exacto del diseño en su archivo DWG.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Por qué es importante:** Al limitar la matriz `Layouts` evita exportar hojas no deseadas, haciendo que la operación **dwg to pdf conversion c#** sea más rápida y el PDF resultante más limpio.

### Paso 4: Crear `PdfOptions`

Enlace los ajustes de rasterización a las opciones de exportación PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Paso 5: Exportar a PDF

Finalmente, guarde el diseño renderizado como un archivo PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Paso 6: Mostrar un mensaje de éxito

Una salida rápida en la consola confirma que la operación se completó con éxito.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **No se generó PDF** | La matriz `Layouts` no coincide con ningún nombre de diseño en el DWG. | Verifique los nombres de los diseños usando un visor CAD y actualice la propiedad `Layouts`. |
| **Páginas en blanco** | `PageWidth`/`PageHeight` establecidos en 0 o valores extremadamente pequeños. | Utilice dimensiones realistas (p.ej., 1600 × 1600) o permita que Aspose calcule automáticamente omitiendo esas propiedades. |
| **Escalado incorrecto** | DPI no establecido cuando se requiere salida de alta resolución. | Establezca `rasterizationOptions.Resolution = 300;` (o el DPI deseado) antes de exportar. |

## Preguntas frecuentes

**P: ¿Puedo exportar varios diseños simultáneamente?**  
R: Sí, simplemente modifique la matriz `Layouts` en el Paso 3 para incluir todos los nombres de diseño deseados, por ejemplo, `new string[] { "Layout1", "Layout2" }`.

**P: ¿Es Aspose.CAD compatible con otros formatos de archivo CAD?**  
R: Absolutamente. Soporta DWG, DXF, DWF, DGN y muchos más formatos.

**P: ¿Cómo puedo ajustar la configuración de salida PDF más allá del tamaño de página?**  
R: Explore propiedades adicionales de `CadRasterizationOptions` como `Resolution`, `BackgroundColor` y `DrawType` para afinar el resultado.

**P: ¿Dónde puedo encontrar documentación adicional de Aspose.CAD?**  
R: Visite la [documentation](https://reference.aspose.com/cad/net/) para referencias de API detalladas y ejemplos.

**P: ¿Hay una prueba gratuita disponible?**  
R: Sí, puede acceder a la prueba gratuita [here](https://releases.aspose.com/).

## Conclusión

Ahora ha aprendido cómo **establecer opciones de rasterización CAD** y usarlas para **exportar diseños DWG específicos a PDF** con Aspose.CAD para .NET. Este enfoque le brinda un control preciso sobre el proceso de conversión, permitiéndole integrar la funcionalidad CAD‑a‑PDF en cualquier aplicación C# de forma rápida y fiable.

---

**Última actualización:** 2026-03-13  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}