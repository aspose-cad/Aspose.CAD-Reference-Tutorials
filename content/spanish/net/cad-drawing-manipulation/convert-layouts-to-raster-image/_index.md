---
title: Convierta diseños a imágenes rasterizadas en Aspose.CAD para .NET
linktitle: Convertir diseños a imágenes rasterizadas
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Convierta sin esfuerzo diseños CAD en imágenes rasterizadas utilizando Aspose.CAD para .NET. Mejore su desarrollo con potentes capacidades de manipulación CAD.
type: docs
weight: 12
url: /es/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## Introducción

¿Está buscando convertir fácilmente diseños a imágenes rasterizadas en sus aplicaciones .NET? ¡No busque más! Esta guía paso a paso lo guiará a través del proceso utilizando Aspose.CAD para .NET, una poderosa biblioteca que simplifica las tareas de diseño asistido por computadora (CAD).

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Aspose.CAD para la biblioteca .NET: descargue e instale la biblioteca desde[Página de descarga de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

- Entorno de desarrollo: asegúrese de tener un entorno de desarrollo .NET funcional configurado en su máquina.

- Documento para convertir: prepare un documento CAD que contenga los diseños que desea convertir a imágenes rasterizadas.

- Su directorio de documentos: reemplace el marcador de posición "Su directorio de documentos" en el código con la ruta a su directorio de documentos.

## Importar espacios de nombres

En primer lugar, importemos los espacios de nombres necesarios para que las funcionalidades de Aspose.CAD sean accesibles en su código.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: cargue el documento CAD

Comience cargando el documento CAD usando la biblioteca Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    // Su código para pasos adicionales irá aquí
}
```

## Paso 2: configurar las opciones de rasterización

 Crear una instancia de`CadRasterizationOptions` para establecer el ancho y alto de la página y especificar los diseños que desea convertir.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Paso 3: configurar TiffOptions para la imagen resultante

 Crear una instancia de`TiffOptions` para definir el formato de la imagen resultante.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 4: guarde la imagen resultante

Especifique la ruta de salida y guarde la imagen convertida.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Conclusión

¡Felicidades! Ha convertido con éxito diseños CAD a un formato de imagen rasterizada utilizando Aspose.CAD para .NET. Las posibilidades son amplias y esta guía sirve como punto de partida para sus iniciativas relacionadas con CAD.

## Preguntas frecuentes

### P1: ¿Aspose.CAD es compatible con todos los formatos CAD?

 R1: Aspose.CAD admite una amplia gama de formatos CAD, incluidos DWG, DXF, DWF, STL y más. Comprobar el[documentación](https://reference.aspose.com/cad/net/) para obtener una lista completa.

### P2: ¿Cómo puedo obtener una licencia temporal para Aspose.CAD?

 A2: Visita el[página de licencia temporal](https://purchase.aspose.com/temporary-license/)adquirir una licencia temporal para fines de prueba y evaluación.

### P3: ¿Dónde puedo encontrar soporte para Aspose.CAD?

 R3: Los foros son un gran lugar para buscar ayuda. Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para conectarse con la comunidad y obtener ayuda.

### P4: ¿Puedo probar Aspose.CAD gratis?

 R4: ¡Absolutamente! Toma tu[prueba gratis](https://releases.aspose.com/) para explorar las características y capacidades de Aspose.CAD.

### P5: ¿Dónde puedo comprar una licencia para Aspose.CAD?

 A5: Navegue hasta el[pagina de compra](https://purchase.aspose.com/buy) para comprar una licencia y desbloquear todo el potencial de Aspose.CAD.