---
title: Trabajar con archivos DWG en C# obtener el tamaño del diseño DWF
linktitle: Trabajar con archivos DWG en C# obtener el tamaño del diseño DWF
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Explore el poder de Aspose.CAD para .NET en el manejo de archivos DWG. Aprenda a extraer tamaños de diseño DWF sin esfuerzo usando C#.
type: docs
weight: 10
url: /es/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Introducción

En el ámbito del diseño asistido por computadora (CAD) y el desarrollo .NET, Aspose.CAD se presenta como una poderosa herramienta para manejar archivos DWG. Este tutorial lo guiará a través del proceso de trabajar con archivos DWG en C# y extraer el tamaño de un diseño DWF. Antes de profundizar en el código, asegurémonos de tener todo configurado para embarcarse en este viaje.

## Requisitos previos

Para seguir este tutorial sin problemas, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.CAD para .NET: asegúrese de tener instalado Aspose.CAD para .NET. Puedes descargarlo desde el[Página de descarga de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

Ahora que tiene las herramientas necesarias, saltemos al campo de la codificación.

## Importar espacios de nombres

Antes de comenzar a trabajar con el código, importemos los espacios de nombres necesarios:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Estos espacios de nombres proporcionarán las clases y métodos esenciales para manejar archivos CAD con Aspose.CAD en su aplicación C#.

## Paso 1: configure su entorno

Comience asegurándose de tener configurado el entorno correcto para su proyecto. Haga referencia a la biblioteca Aspose.CAD en su proyecto C#.

## Paso 2: definir rutas de archivos

Defina las rutas para su archivo DWG y el directorio de salida para los archivos JPG generados:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Paso 3: cargue la imagen DWF

Cargue la imagen DWF usando Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // El código para pasos adicionales irá aquí
}
```

## Paso 4: iterar a través de las páginas

Itere a través de las páginas de la imagen DWF:

```csharp
foreach (var page in image.Pages)
{
    // El código para pasos adicionales irá aquí
}
```

## Paso 5: obtenga información de diseño

Obtenga información de diseño de cada página:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Paso 6: configurar las opciones JPG

Configure opciones para guardar el diseño como un archivo JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // El código para pasos adicionales irá aquí
}
```

## Paso 7: determinar el tamaño de la página

Determine el tamaño del diseño DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// El código para pasos adicionales irá aquí
```

## Paso 8: configurar las dimensiones de la página

Configure las dimensiones de la página según el tipo de unidad:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Paso 9: guarde el archivo JPG

Guarde el archivo JPG con las opciones especificadas:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Ahora ha extraído con éxito el tamaño del diseño DWF del archivo DWG usando Aspose.CAD en C#. No dude en explorar más características y funcionalidades que ofrece Aspose.CAD para el desarrollo .NET.

## Conclusión

En este tutorial, hemos recorrido el proceso de trabajar con archivos DWG en C# usando Aspose.CAD. Si sigue estos pasos, no sólo podrá obtener el tamaño de un diseño DWF, sino también aprovechar las capacidades de Aspose.CAD para diversas tareas relacionadas con CAD en sus proyectos .NET.

## Preguntas frecuentes

### P1: ¿Aspose.CAD es compatible con los últimos formatos de archivos DWG?

 R1: Aspose.CAD admite varios formatos de archivos DWG, incluidas las últimas versiones. Referirse a[documentación](https://reference.aspose.com/cad/net/) para obtener detalles de compatibilidad específicos.

### P2: ¿Puedo utilizar Aspose.CAD para proyectos comerciales y personales?

R2: Sí, Aspose.CAD ofrece opciones de licencia flexibles para uso comercial y personal. Visita el[pagina de compra](https://purchase.aspose.com/buy) para más detalles.

### P3: ¿Cómo puedo obtener una licencia temporal para Aspose.CAD?

 R3: Puede obtener una licencia temporal de[aquí](https://purchase.aspose.com/temporary-license/) para fines de evaluación.

### P4: ¿Dónde puedo encontrar soporte para Aspose.CAD?

 R4: Para cualquier consulta o asistencia, visite el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P5: ¿Hay una prueba gratuita disponible para Aspose.CAD?

 R5: Sí, puede acceder a una versión de prueba gratuita de Aspose.CAD[aquí](https://releases.aspose.com/).