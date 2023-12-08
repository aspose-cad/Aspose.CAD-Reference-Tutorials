---
title: Exporte diseños CAD a formatos de imágenes rasterizadas en Aspose.CAD para .NET
linktitle: Exportar diseños CAD a formatos de imágenes rasterizadas
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Aprenda a exportar diseños CAD a imágenes rasterizadas utilizando Aspose.CAD para .NET. Siga nuestra guía paso a paso para una conversión perfecta.
type: docs
weight: 10
url: /es/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## Introducción

¿Está buscando convertir de manera eficiente diseños CAD a formatos de imágenes rasterizadas usando Aspose.CAD para .NET? Esta guía paso a paso lo guiará a través del proceso y le brindará instrucciones detalladas y fragmentos de código para que la tarea sea perfecta. Ya sea que sea un desarrollador experimentado o un recién llegado a Aspose.CAD, este tutorial se adapta a todos los niveles de experiencia.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de tener lo siguiente:

- Aspose.CAD para la biblioteca .NET: asegúrese de tener instalada la biblioteca Aspose.CAD. Si no, puedes descargarlo desde[Sitio web de Aspose.CAD](https://releases.aspose.com/cad/net/).

- Archivo de dibujo CAD: prepare un archivo de dibujo CAD (por ejemplo, conic_pyramid.dxf) que desee convertir a formatos de imagen rasterizada.

## Importar espacios de nombres

En su proyecto .NET, importe los espacios de nombres necesarios para aprovechar las funcionalidades de Aspose.CAD. Incluya los siguientes espacios de nombres al principio de su código:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: cargar el dibujo CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Cargar un dibujo CAD en una instancia de Imagen
using (var image = Image.Load(sourceFilePath))
{
    // Su código para cargar el dibujo CAD va aquí
}
```

## Paso 2: crear CadRasterizationOptions

```csharp
// Crear una instancia de CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Paso 3: especificar capas

```csharp
// Agregue el nombre de la capa a la lista de capas de CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Paso 4: crear JpegOptions

```csharp
// Cree una instancia de JpegOptions (o cualquier ImageOptions para formatos ráster)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 5: exportar a formato Jpeg

```csharp
// Exportar cada capa a formato Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Paso adicional: convertir todas las capas

Si desea convertir todas las capas, utilice el siguiente método:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Este método itera sobre todas las capas del dibujo CAD y exporta cada capa a un archivo Jpeg independiente.

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo exportar diseños CAD a formatos de imágenes rasterizadas utilizando Aspose.CAD para .NET. Este tutorial proporciona una guía completa para desarrolladores que buscan soluciones eficientes y confiables para la conversión de CAD.

## Preguntas frecuentes

### P1: ¿Puedo utilizar otros formatos de imagen para exportar?

 R1: Sí, puedes. Simplemente reemplace`JpegOptions` con las opciones del formato deseado, como`PngOptions` o`BmpOptions`.

### P2: ¿Hay una versión de prueba disponible?

 R2: Sí, puede explorar la funcionalidad de Aspose.CAD descargando la versión de prueba[aquí](https://releases.aspose.com/).

### P3: ¿Cómo puedo obtener soporte para Aspose.CAD?

 A3: Visite Aspose.CAD[foro](https://forum.aspose.com/c/cad/19) para soporte comunitario o considere comprar una licencia para soporte dedicado.

### P4: ¿Hay licencias temporales disponibles?

 R4: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo encontrar la documentación?

 A5: consulte la documentación detallada[aquí](https://reference.aspose.com/cad/net/).