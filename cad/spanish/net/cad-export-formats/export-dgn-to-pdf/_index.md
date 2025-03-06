---
title: Exportar DGN a PDF en Aspose.CAD para .NET
linktitle: Exportar DGN a PDF
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Aprenda a exportar archivos DGN a PDF sin esfuerzo con Aspose.CAD para .NET. Una guía paso a paso para una manipulación perfecta de archivos CAD.
weight: 12
url: /es/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DGN a PDF en Aspose.CAD para .NET

## Introducción

En el mundo del desarrollo .NET, Aspose.CAD es una poderosa biblioteca que facilita la manipulación y conversión de archivos CAD. Una tarea común que suelen encontrar los desarrolladores es exportar archivos DGN a formato PDF. En este tutorial, recorreremos el proceso paso a paso, utilizando Aspose.CAD para .NET.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de tener lo siguiente en su lugar:

- Un conocimiento práctico de C# y el marco .NET.
-  Aspose.CAD para la biblioteca .NET instalada. Puedes descargarlo[aquí](https://releases.aspose.com/cad/net/).
- Un archivo DGN de muestra, por ejemplo, "Nikon_D90_Camera.dgn" para este tutorial.

## Importar espacios de nombres

En su proyecto C#, comience importando los espacios de nombres necesarios:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: cargar el archivo DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Tu código aquí...
}
```

## Paso 2: configurar las opciones de rasterización

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Paso 3: crear opciones de PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 4: guardar como PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Conclusión

¡Felicidades! Ha exportado exitosamente un archivo DGN a PDF usando Aspose.CAD para .NET. Este tutorial cubrió los pasos esenciales, desde cargar el archivo DGN hasta configurar las opciones de rasterización y guardar el resultado como PDF.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para .NET sin conocimientos previos de CAD?

R1: ¡Absolutamente! Aspose.CAD simplifica las tareas CAD complejas, haciéndola accesible para desarrolladores con diversos orígenes.

### P2: ¿Dónde puedo encontrar más ejemplos y documentación para Aspose.CAD?

 A2: Explora el[documentación](https://reference.aspose.com/cad/net/) para guías completas y ejemplos.

### P3: ¿Hay una prueba gratuita disponible para Aspose.CAD?

R3: Sí, puedes obtener una prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener licencias temporales para Aspose.CAD?

 A4: Obtener licencias temporales[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Necesita ayuda o tiene preguntas?

A5: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para el apoyo de la comunidad.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
