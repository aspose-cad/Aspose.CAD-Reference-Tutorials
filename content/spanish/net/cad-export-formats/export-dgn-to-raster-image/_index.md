---
title: Exportar DGN a imagen rasterizada en Aspose.CAD para .NET
linktitle: Exportar DGN a imagen rasterizada
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Convierta DGN a imágenes rasterizadas sin esfuerzo utilizando Aspose.CAD para .NET. Explore la guía paso a paso y libere el poder de .NET en la manipulación de archivos CAD.
type: docs
weight: 13
url: /es/net/cad-export-formats/export-dgn-to-raster-image/
---
## Introducción

En el ámbito dinámico del desarrollo .NET, Aspose.CAD surge como una poderosa herramienta para manejar archivos de diseño asistido por computadora (CAD). Este tutorial profundiza en el proceso de exportación de archivos DGN a imágenes rasterizadas usando Aspose.CAD para .NET. Si está interesado en transformar sus archivos DGN en imágenes rasterizadas visualmente atractivas sin problemas, está en el lugar correcto.

## Requisitos previos

Antes de embarcarnos en este viaje, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.CAD para .NET: asegúrese de tener la biblioteca Aspose.CAD instalada en su proyecto .NET. Puede encontrar la biblioteca y la documentación relevante en el[sitio web](https://reference.aspose.com/cad/net/).

- Archivo DGN de muestra: tenga un archivo DGN listo para la conversión. En nuestro ejemplo, usaremos "Nikon_D90_Camera.dgn".

Ahora, profundicemos en la guía paso a paso.

## Importar espacios de nombres

En su proyecto .NET, comience importando los espacios de nombres necesarios para Aspose.CAD. Este paso le permite acceder a las clases y métodos necesarios para la conversión de DGN a imágenes rasterizadas.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: cargar el archivo DGN

 Comience cargando el archivo DGN en un`CadImage` objeto. Esto proporciona una base para operaciones posteriores.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Su código para su posterior procesamiento va aquí
}
```

## Paso 2: definir las opciones de rasterización

 Crear un`CadRasterizationOptions` objeto y establezca varias propiedades para personalizar el proceso de rasterización de acuerdo con sus requisitos.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Paso 3: crear el objeto JpegOptions

 Dado que nuestro objetivo es convertir el archivo DGN a JPEG, cree un`JpegOptions` objeto y asignar el previamente definido`CadRasterizationOptions` lo.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 4: guarde la imagen rasterizada

 Utilice el`Save` método de la`CadImage` clase para exportar el archivo DGN a una imagen rasterizada en el formato deseado, en este caso, un JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Conclusión

¡Felicidades! Ha seguido con éxito los pasos para exportar un archivo DGN a una imagen rasterizada utilizando Aspose.CAD para .NET. Este tutorial le ha proporcionado los conocimientos esenciales para integrar esta funcionalidad en sus proyectos .NET sin esfuerzo.

## Preguntas frecuentes

### P1: ¿Puedo exportar archivos DGN a formatos distintos de JPEG?

R1: Sí, Aspose.CAD para .NET admite varios formatos de salida. Puede modificar las opciones en consecuencia en el Paso 3.

### P2 ¿Cómo puedo manejar las excepciones durante el proceso de conversión?

R2: Asegúrese de tener un manejo de excepciones adecuado, como se demuestra en el código proporcionado, para abordar posibles problemas.

### P3: ¿Existe una versión de prueba disponible de Aspose.CAD para .NET?

 R3: Sí, puedes explorar el producto con una prueba gratuita. Visita[aquí](https://releases.aspose.com/) para más información.

### P4: ¿Dónde puedo buscar ayuda o discutir temas relacionados con Aspose.CAD para .NET?

 A4: Dirígete al[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoyo y debates de la comunidad.

### P5: ¿Cómo obtengo una licencia temporal de Aspose.CAD para .NET?

 A5: Visita[este enlace](https://purchase.aspose.com/temporary-license/)para adquirir una licencia temporal para sus necesidades de desarrollo.